# update-digital-ocean-ip

Docker image for periodically updating subdomain ip address on Digital Ocean

## Usage

Using Docker

```bash
docker run -it $(docker build -q .) -e TOKEN=<your_token> -e DOMAIN=<your_domain> -e RECORD_ID=<your_record_id>
```

Using Docker Compose

There is a `docker-compose-example.yml` file that can be used as a template for your own `docker-compose.yml` file.

Once any necessary changes have been made, you can run the following command to start the service:

```bash
docker-compose up -d
```

## Useful commands

* **Retrieving list of subdomain records**: `curl -H "Authorization: Bearer $TOKEN" "https://api.digitalocean.com/v2/domains/$DOMAIN/records" | jq`
