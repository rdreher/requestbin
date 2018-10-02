# RequestBin

Originally Created by [Jeff Lindsay](http://progrium.com)

Want to self-host your own RequestBin?
=====================
Run [RequestBin](https://github.com/Runscope/requestbin) from a Docker container.

[![Deploy](http://azuredeploy.net/deploybutton.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Frdreher%2Frequestbin%2Fmaster%2Fdeployment%2Fazuredeploy.json)

## Deploy your own instance using Docker on Azure

This is a self-hosted version of RequestBin that runs on Azure Container Instances. Create an Azure account if you haven't, then click the button above.

Running the RequestBin web site on Azure have the following costs associated with its resources:

* Azure Function (Dynamic Plan) - Pay Per Use
* Azure Container Instance 1 CPU / 1 GB RAM for the RequestBin web site 
* Azure Container Instance 1 CPU / 1 GB RAM for the Redis cache

### Accessing the site
After the template deployment is complete you can access RequestBin web site using the following urls: 

* If you need HTTPS, you must use `https://<name-specified-during-deployment>.azurewebsites.net`.
* You can also access it using the ACI domain at `http://<name-specified-during-deployment>.<regionname-of-resourcegroup>.azurecontainer.io` where `<regionname-of-resourcegroup>` e.g. could be `centralus` if you created the resource group in that region. Note this URL doesn't support HTTPS, as that is yet to come for ACI, which why it is included the Azure function reverse proxy template, as you most likely need HTTPS. 

## Deploy your own instance using Docker locally
On the server/machine you want to host this, you'll first need a machine with
docker and docker-compose installed, then grab the [docker-compose.yml](https://github.com/rdreher/requestbin/blob/master/docker-compose.yml) file. You can
get the server running on port 8000 with:

`docker-compose up`
