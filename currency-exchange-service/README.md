##docker commands to run to load and run the application

docker network create local-net


docker run -p 8000:8000 --net local-net --name currency-exchange ${image_id}
#docker run itd -p 8000:8000 --net local-net --name currency-exchange ${image_id}


URL: http://localhost:8000/currency-exchange/from/USD/to/INR
