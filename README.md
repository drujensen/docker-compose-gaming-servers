# Docker Compose Gaming Servers

This repository contains docker compose files for starting several different Gaming Servers

## Setup

On an Ubuntu server, create a  directoy for the volumes.  Look in the volumes mapping to see what directory to create.  For example, for the minecraft server:
```bash
mkdir /home/ubuntu/mc
```

For the ports, make sure your server allows them to be accessible from the internet.

For the password and other configurations, check the environment variables and change appropriately.

## Usage
I like to map an alias for `docker-compose` to `dc` to make it easier to run.  Add this to your `.bash_profile`
```bash
alias d="docker"
alias dc="docker-compose"
```

To start a server:
```bash
dc -f mc.yml up -d
```

To view the logs:
```bash
dc -f mc.yml logs -f
```

To stop a server:
```bash
dc -f mc.yml down
```

To clean up docker:
```bash
docker system prune --volumes
```
