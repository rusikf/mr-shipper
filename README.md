# shipper
Easy going shipment for your docker-compose apps

## Install

` $ gem install mr-shipper`

## Configure

You need to create your own `shipper.yml` file with the content similar to:

```yaml
services:
  frontend:
    path: "../sample-fronted"
    before_build:
      - "yarn build"
    repo: "<dockerhub-nickname>/sample-fronted"
  backend:
    path: "../sample-backend"
    repo: "<dockerhub-nickname>/sample-backend"
host: 
  ssh_entry: "user@host"
  location: "~/apps/sample"
```

## Use

`$ ship`

And so.. that's all for now. 
To be expanded with more cooler configurations for different hosts and so on..