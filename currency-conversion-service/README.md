#docker commands to run to load and run the application

docker network create local-net


docker run -p 8100:8100 --net test --name currency-conversion --link currency-exchange --env CURRENCY_EXCHANGE_URI=currency-exchange  ${image_id}

http://localhost:8100/currency-conversion/from/USD/to/INR/23
