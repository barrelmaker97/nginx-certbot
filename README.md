# Boilerplate for nginx with Let’s Encrypt on docker-compose

`init-letsencrypt.sh` fetches and ensures the renewal of a Let’s
Encrypt certificate for one or multiple domains in a docker-compose
setup with nginx.
This is useful when you need to set up nginx as a reverse proxy for an
application.

## Installation
1. [Install docker-compose](https://docs.docker.com/compose/install/#install-compose).

2. Clone this repository:

        git clone https://github.com/barrelmaker97/nginx-certbot.git

3. Modify configuration:
    - Add your domains and email addresses to init-letsencrypt.sh
    - Modify nginx configuration at `data/nginx/nginx.conf` to suit your needs (Security Headers, Logging, etc.)
    - Add as many servers as you would like in `data/nginx/servers`
    - Setup your static site by replacing the volume in the docker-compose (if you choose to keep that server)

4. Run the init script:

        ./init-letsencrypt.sh

## License
All code in this repository is licensed under the terms of the `MIT License`. For further information please refer to the `LICENSE` file.
