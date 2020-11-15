
# **Steps To run the application in a container**

## Commands:
- First build and run the container of the currency-exchange service. As this service is independent on any other service and can be tested separately.
- Now, follow the steps mention in the README.md of the currency-exchange-service.
- Second build and run the container of the currency-conversion-service. This should be the second service to be launcged otherwise it will fail at the startup as it consumes currency-exchange-service internally to get the data.
- Follow the steps mention in the README.md of currency-conversion-service.
