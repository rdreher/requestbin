# RequestBin

Originally Created by [Jeff Lindsay](http://progrium.com)

Want to self-host your own RequestBin?
=====================
Run [RequestBin](https://github.com/Runscope/requestbin) from a Docker container.

[![Deploy](http://azuredeploy.net/deploybutton.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Frdreher%2Frequestbininazure%2Fmaster%2Fazuredeploy.json)

## Deploy your own instance using Docker on Azure

Create an Azure account if you haven't, then click the button above.

## Deploy your own instance using Docker locally

On the server/machine you want to host this, you'll first need a machine with
docker and docker-compose installed, then grab the [docker-compose.yml](https://github.com/rdreher/requestbin/blob/master/docker-compose.yml) file. You can
get the server running on port 8000 with:

`docker-compose up`
