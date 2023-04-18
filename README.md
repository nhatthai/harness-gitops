# Harness Deployments
Example: setup a deployment pipeline in Harness and deploy webapi to Azure Service Apps

### Setup
+ Create a Harness Account
+ Create a Project
![Overview](./images/harness-overview.png)

+ Install a Harness Delegates
Run a command in Command line(I am using my Machine as docker delegate)
    ```
    docker run --cpus=1 --memory=2g \
        -e DELEGATE_NAME=docker-delegate \
        -e NEXT_GEN="true" \
        -e DELEGATE_TYPE="DOCKER" \
        -e ACCOUNT_ID=0bKPVrNUQ2uni0e728NSgw \
        -e DELEGATE_TOKEN=MjJkM2JlMTcxNjMxYTZiYjQ5NmNiNWMwM2YwOGM1YTQ= \
        -e LOG_STREAMING_SERVICE_URL=https://app.harness.io/gratis/log-service/ \
        -e MANAGER_HOST_AND_PORT=https://app.harness.io/gratis harness/delegate:23.03.78904
    ```

![Docker Delegate](./images/docker-delegate.png)


![Harness Delegate](./images/harness-delegate.png)


+ Add Role in Azure
![Add Roles](./images/Add-Roles.png)

+ Create Harness Key
![Harness Key](./images/creating-harness-key.png)

+ Create a connector to Azure
![Harness Connector](./images/azure-harness-cloud.png)

+ Create a Harness Service
![Harness Service](./images/harness-service.png)

+ Create a Harness Pipeline
![Harness Swap Lost](./images/harness-swap-lots.png)

### Result
+ Web API
![Web API](./images/webapi.png)
