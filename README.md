# WEX-PRICES-SERVICE

[Zen test 004](http://telegra.ph/Zen-test-004-03-30)

## Install & Run

```sh
git clone https://github.com/alexbadm/wex-prices-service.git
cd wex-prices-service
docker-compose up -d db
# Wait for the database to initialize, and then you can start by:
docker-compose up -d
```

Go to [localhost:4000](http://localhost:4000) to receive the data.
The app gives the prices of all currency pairs from the wex.nz exchange averaged over the last 10 minutes.
