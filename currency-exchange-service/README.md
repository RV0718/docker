**docker commands to run to load and run the application**

# First Create the network. We will use this network to launch the container.
docker network create local-net
docker run -p 8000:8000 itd --net local-net --name currency-exchange ${image_id}
 - -p 8000:8000: this is to expose the container port to the host port
 - --net local-net : to mention the desired network under which we would like to launch the container
 - --name: is the name of the container
 - ${image_id}: is the id of the image to be launched
 - itd: to lauch the container in the interactive detached mode

# Example URL:
URL: http://{ip/host of the docker(or localhost) host}:8000/currency-exchange/from/USD/to/INR
http://localhost:8000/currency-exchange/from/USD/to/INR
