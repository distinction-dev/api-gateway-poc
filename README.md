# ai-marketer-api-gateway
This repository only contains the API Gateway as it is a shared resource.  
Additional resources are also deployed which exist as fallbacks for Default Responses as well to configure the messages for Auth Responses.

## How to use
You should configure your service like so.
```yaml
service: <Name of service>

provider:
  apiGateway:
    restApiId: ${env:API_GATEWAY_ID}
    restApiRootResourceId: ${env:REST_API_ROOT_ID}
```
Since these stacks don't output anything, the following table describes these values
| Name                      | Description                                                    | Uat        | Alpha      | Beta       | Blue       |
| ------------------------- | -------------------------------------------------------------- | ---------- | ---------- | ---------- | ---------- |
| Api Gateway Rest Api Id   | Used to attach multiple stacks to a single api gateway         | 1b99vh58ma | gx5ynhqc0g | hc9zaqyxh6 | 0r0bbfbqxf |
| Rest Api Root Resource Id | Used to attach multiple stacks to the root resource of the api | fixbg8gr4i | uvbpoib3na | t0cuwakn0l | k7bct1ugka |

*This table was generated using tablemark*


This api gateway has been deployed in 4 environments across 2 accounts
* Account - **Dev**:
  * UAT

* Account - **PROD**:
  * BETA
  * BLUE
  * GREEN


## Workflows
* Deployment:  
  Deploys an api-gateway to 4 environments on a push to master
