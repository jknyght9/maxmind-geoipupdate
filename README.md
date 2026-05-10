# Maxmind GeoIP Update

This project contains a docker container template that pulls and updates geoip location information from Maxmind.

## Requirements

This does require an account and license key. Create a free account by visiting [https://www.maxmind.com/en/account/login](https://www.maxmind.com/en/account/login).

## Quick Start

1. Copy the example environment file and update it with your account ID and license key:

```shell
cp .env.example .env
```

2. Start the container:

```shell
docker compose up -d
```

3. Check the health status:

```shell
docker compose ps
```

### GeoIP Database

All three databases (ASN, Country, City) will be stored in the `geoip_data` folder. This will be updated every 72 hours as long as the container is running.

### GreymHatter Integration

To attach to the shared `greymhatter` Docker network, copy the override file:

```shell
cp compose.override.yml.example compose.override.yml
docker compose up -d
```

## References

[https://dev.maxmind.com/geoip/updating-databases](https://dev.maxmind.com/geoip/updating-databases)

## Legal / License

This project is open source and distributed under the MIT License.

> This software is provided "as is", without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and noninfringement. In no event shall the authors be liable for any claim, damages, or other liability, whether in an action of contract, tort, or otherwise, arising from, out of, or in connection with the software or the use or other dealings in the software.

---

## Author

Created by Jacob Stauffer | CISSP, GCFA, GREM, OSCP — Contributions and PRs welcome!

<a href="https://www.buymeacoffee.com/jstauffer" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>
