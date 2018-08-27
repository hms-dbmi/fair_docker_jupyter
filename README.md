This repository can be used to create fully reproducible analyses 
on the NHANES datasets as curated and loaded into the i2b2/tranSMART 18.1 
Quickstart application.

System Requirements:

At least 8GB of ram.
At least 80GB of free hard drive space.
docker-machine installed and working
A high speed internet connection, you will be downloading about 40GB of applications and data.

To prepare your environment to host the research appliance, run this command:

docker-machine create -d virtualbox --virtualbox-disk-size "80000" --virtualbox-memory "8192" --virtualbox-cpu-count "2" nhanes
eval $(docker-machine env nhanes)

If you reboot your computer, you may need to restart the docker-machine also like this:

docker-machine start nhanes
eval $(docker-machine env nhanes)

If you are done with your work and want to reclaim all your hard drive space:

docker-machine rm nhanes


In order to start your research project, you should first fork this repository to your own.

This new fork you will create on your GitHub account will serve as documentation
of your research process.

Once you have forked the repo, clone your fork and run `docker-compose pull` 
in the forked copy.

This will take a really long time the first time you run it, just be patient. It
could realistically take an hour or two for the initial download but 30 minutes
is typical.

If you get messages like "the remote end has hung up unexpectedly" just re-run
`docker-compose pull` until everything successfully downloads.

Once downloaded, run `docker-compose up -d`, this will start the research appliance.

Browse your JupyterNotebook by copy pasting the output of the following command into
your browser address bar:

$(docker-machine ls | grep nhanes | awk '{ print $5 }' | sed s/tcp/http/ | sed s/2376/80/)

You can develop your analysis in this jupyter notebook as you normally would. There
are just a few extra pieces:

You have sudo access through the jupyterhub terminal. If you have to run anything
there you should also add the commands to the update_os2.sh script. This will help
you publish your eventual images.

If you install anything using the R built in package systems from within
your notebook, those should be added to the dependencies2.r script also.

TODO: Documentation on publishing your images and finalizing the repo for research
