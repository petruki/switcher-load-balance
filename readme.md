[![Build Status](https://travis-ci.com/petruki/switcher-balance.svg?branch=master)](https://travis-ci.com/petruki/switcher-balance)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=switcher-balance&metric=alert_status)](https://sonarcloud.io/dashboard?id=switcher-balance)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

![Switcher Load Balance: Load Balancing API](https://github.com/petruki/switcherapi-assets/blob/master/logo/switcherapi_loadbalance.png)

# Requirements  
- NodeJS
- Postman (optional for request examples)
- Coffee =D

# About  
**Switcher Load Balance** is a simple load balance developed especially for supporting CI environments.

Main features:
- Auto switch off when the current node is offline.
- Stateful configuration, no DB in between, the only latency is the network.
- Check node health via REST requests.
- API Key generated automatically after deployment.

# Configuration
1) npm install
2) Add .env-cmdrc file into the project directory.

Example:
```
{
  "dev": {
    "PORT": "3002",
    "SNODE1": "http://localhost:3000",
    "SNODE2": "https://switcher-api.herokuapp.com",
    "CHECK_ENDPOINT": "/check"
  },
  "prod": {
    "PORT": "3002",
    "SNODE1": "http://localhost:3000",
    "SNODE2": "https://switcher-api.herokuapp.com",
    "CHECK_ENDPOINT": "/check"
  },
  "test": {
    "PORT": "3002"
  }
}
```

## Donation
Donations for cookies and pizza are extremely welcomed.

[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=9FKW64V67RKXW&source=url)