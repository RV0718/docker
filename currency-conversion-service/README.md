# **docker commands to load and run the application in a container**

## Commands:
- go to the root directory of the project 
- mvn clean build
- docker build -t {repo name}:tag . <br />
  - -t: is used to tag your build.
  - Ex: -t abc/currency-exchange:1.0.0-SNAPSHOT
  - .: is there if you're running the docker build command from the root directory of the project. Else you can use the -f to provide the docker file path.
- docker network create local-net 
  - First we will create the docker network. We will use this network to launch the container.
- docker run -p 8100:8100 itd --net local-net --name currency-conversion --link currency-exchange --env CURRENCY_EXCHANGE_URI=currency-exchange ${image_id}
  - -p 8100:8100: this is to expose the container port to the host port
  - --net local-net : to mention the desired network under which we would like to launch the container
  - --name: is the name of the container
  - ${image_id}: is the id of the image to be launched
  - itd: to lauch the container in the interactive detached mode
  - --link: used to provide the link between the container. If the container of service A is depends on container of service B, then used the link flag.
  - --env: used to provide the runtime value of any parameters.

# Example URL:
URL: http://{ip/host of the docker(or localhost) host}:8100/currency-conversion/from/USD/to/INR/23

Ex: http://localhost:8100/currency-conversion/from/USD/to/INR/23
