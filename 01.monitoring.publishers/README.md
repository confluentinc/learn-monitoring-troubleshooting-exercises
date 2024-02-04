# Case Study 1: Deciphering Cluster Load

## Setting up Confluent Cloud
### Cluster Setup
1. Create an account on https://confluent.cloud
1. Add the coupon code ????? to get ????? free 
1. Create a basic cluster
1. Click on Clients
1. Add a new client
1. Choose Python
1. Create Cluster Key
1. Copy client.properties.template to client.properties
1. Update client.properties file with
    1. bootstrap servers
    1. sasl.username (access key)
    1. sasl.password (secret key) 
    1. clusterid (lkc-???)
### Cloud API setup
1. Hamburger icon on top right corner
1. Choose Cloud API key
1. Add Key
1. Jot down access key and secret key
    This is very **dangerous** as it authorizes anyone with this credential to delete your cluster. Do not do this against a production cluster. See [Confluent Cloud documentation](https://docs.confluent.io/cloud/current/monitoring/metrics-api.html#add-the-metricsviewer-role-to-a-new-service-account) for the secure way to access the Metrics API