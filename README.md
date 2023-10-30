# Maxmind GeoIp Update

This project contains a docker container template that pulls and updates geoip location information from Maxmind. 

## Requrements

This does require an account and license key. Create a free account by visiting [https://www.maxmind.com/en/account/login](https://www.maxmind.com/en/account/login).

## Usage

Update the `config.env` file with your account_id and license_key. Then navigate to the folder containing the docker-compose.yml file and run the command:

```shell
docker-compose up -d 
```

## GeoIP Database

All three databases (ASN, Country, City) will be stored in the `geoip_data` folder. This will be updated periodically as long as the container is running.

## References

[https://dev.maxmind.com/geoip/updating-databases](https://dev.maxmind.com/geoip/updating-databases)
