# DevOPs
Setup, best practices, etc for devops in Visual Studio Online

## Azure Docker Build Agent
1. Create a vm in Azure portal.
1. [Install Docker](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04)
1. [Install Azure Agent](https://docs.microsoft.com/en-us/azure/devops/pipelines/agents/v2-windows?view=azure-devops)
1. Configure Azure Agent to run as service `sudo ./svc.sh` from agent folder.
1. Configure docker to run under current user `sudo usermod -aG docker yourusername`
1. Confirm agent status in Visual Studio Online. 

## VSO Build Using Azure Docker Build Agent
> Assumes build of application is included in docker file. 
1. Create a new build pipe. 
1. Add the docker build task. 
1. Point to your existing Docker registry. 
