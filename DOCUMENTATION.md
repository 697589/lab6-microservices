# The two microservices are running and registered (two terminals, logs screenshots)
Description | Web interface |  Logs
:-------------------------:|:-------------------------:|:-------------------------:
Account microservice | ![account](screens/t1_accounts_ms_screen.png) | ![account](screens/t1_accounts_log_port_2222.png)
Web microservice | ![web](screens/t1_web_ms_screen.png) | ![web](screens/t1_web_ms_log.png)

# The service registration service has the two microservices registered (a third terminal, dashboard screenshots)
Description | Web interface |  Logs
:-------------------------:|:-------------------------:|:-------------------------:
Eureka server | ![eureka](screens/t2_registration_ms_screen.png) | ![eureka](screens/t2_registration_ms_log.png)

# A second account microservice is running in the port 4444 and it is registered (a fourth terminal, log screenshots).
The [application.yml](./accounts/src/main/resources/application.yml) file of the account microservice was modified with the port 4444 instead of the 2222.

Web interface
:-------------------------:
![all](screens/t3_web_ms_screen.png)

Log (registration microservice)
:-------------------------:
![all](screens/t3_registration_ms_log.png)

Log (accounts microservice)
:-------------------------:
![all](screens/t3_accounts_ms_log_port_4444.png)

# A brief report describing what happens when you kill the microservice with port 2222. Can the web service provide information about the accounts? Why?
Yes, the service will still work because, as the Eureka dashboard shows, there is still one ACCOUNTS-SERVICE service running (The log screenshot below shows how the backup service has handled the new query).

Web interface
:-------------------------:
![all](screens/t4_web_ms_screen.png)

Log (accounts microservice)
:-------------------------:
![all](screens/t4_accounts_ms_log_port_4444.png)