# sample-daytrader

DayTrader is a sample stock-trading application.
This organization contains a distributed version of DayTrader.
It uses five Spring Boot microservices.

## Repositories

| Repository | Description | Port |
| --- | --- | --- |
| [sample.daytrader.microservices](https://github.com/sample-daytrader/sample.daytrader.microservices) | Docker Compose, Makefile, and Helm files that deploy all services | - |
| [daytrader-web-service](https://github.com/sample-daytrader/daytrader-web-service) | Web user interface | 5443 |
| [daytrader-gateway-service](https://github.com/sample-daytrader/daytrader-gateway-service) | API gateway between the web interface and the backend services | 2443 |
| [daytrader-accounts-service](https://github.com/sample-daytrader/daytrader-accounts-service) | User accounts and profiles | 1443 |
| [daytrader-portfolios-service](https://github.com/sample-daytrader/daytrader-portfolios-service) | Portfolios, holdings, and orders | 3443 |
| [daytrader-quotes-service](https://github.com/sample-daytrader/daytrader-quotes-service) | Stock quotes and market summary | 4443 |

## Quick start

You must have Docker installed.

```sh
git clone https://github.com/sample-daytrader/sample.daytrader.microservices.git
cd sample.daytrader.microservices
make deploy
```

Then open <http://localhost:5443>.

The deployment uses the container images from `quay.io/daytrader`.
To build and run each service from source, run `make local`.
