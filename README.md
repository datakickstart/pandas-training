# pandas-training

## Setup
### Install Docker for Mac
First download and install Docker, a container service we will use to run the environment for the training.  You can download from https://store.docker.com/editions/community/docker-ce-desktop-mac

Click button “Get Docker CE for Mac (Stable)”

Then follow install instructions...
double click Docker.dmg  
drag icon to Applications folder  

### Setup folder with data
Open terminal and run:  
sudo mkdir -p /tmp/notebook/data  
sudo chmod -R 777 /tmp/notebook  
curl -o /tmp/notebook/data/vehicle_stops.jsonl https://s3-us-west-2.amazonaws.com/dvannoy-public/sample_data/vehicle_stops_newline_delimited.json


### Install Zeppelin docker image
Start docker application

Then open Terminal and run:
docker pull dylanmei/zeppelin  
(this will cause it to download the docker image for Zeppelin)

Then start up Zeppelin by running:
docker run --rm -p 8080:8080 -v /tmp/notebook:/usr/zeppelin/notebook --name zeppelin dylanmei/zeppelin

Confirm it is working by browsing to http://localhost:8080



