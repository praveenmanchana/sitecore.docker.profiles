## Docker Profiles with sitecore XM

This is a sample repositry demonstrating the usage of docker profiles with sitecore. 

### Pre-Requisites

1. Docker (Desktop version or Enterprise)
2. docker-compose version 1.28 or greater (https://github.com/docker/compose/releases/tag/1.28.0). *Added support of profiles*

### Usage

1. `.\init.ps1 -LicenseXmlPath <Your License Path>` to setup your env file with required values and also generate self-signed certs for traefik
2. `docker-compose --profile xm0 up -d` - to bring up XM0 configuration
3. `docker-compose --profile xm1 up -d` - to bring up XM1 configuration
4. `.\clean.ps1` to clean up local data folders

### Applications

Below is the list of applications and URLs that can be accessed for relevant profiles.
|Role|Profile|URL|
|:-|:-|:-|
|Solr| *xm0*, *xm1*|https://localhost:8984/solr|
|SQL|*xm0*, *xm1*|localhost,14330|
|ID| *xm0*, *xm1*|https://id.localhost|
|CM| *xm0*, *xm1*|https://cm.localhost/sitecore|
|CD| *xm1*|https://cd.localhost|

