# Instructions for setting up OAIC

This repo contains a collection of useful scripts to deploy Open AI Cellular RAN as fast and error-free as possible

## Get needed files

Make scripts executable by running the following command:
chmod +x ./\*.sh

## Install the RIC by running the provided script

    ./oaic_deploy.sh

## Install srsRAN by running the provided script

    ./srsran_deploy.sh

## Deploy the KPIMON xapps

To successfully test the xApp, a functioning environment of the Base Station and one or more UEs are required.

    ./kpimon_deploy.sh

# Other helpful stuff

During the deployment, I always had the problem of quickly switching back and forth between working states. I recommend using timeshift backups for this.

    sudo apt install timeshift

Create a first backup simply by executing the below command:

    sudo timeshift --create

List all your currently created system backup screenshots:

    sudo timeshift --list

Restore from the backup snapshot:

    sudo timeshift --restore --snapshot "<NAMEOFBACKUP>"

Delete selected backup snapshot:

    sudo timeshift --delete  --snapshot '<NAMEOFBACKUP>'
