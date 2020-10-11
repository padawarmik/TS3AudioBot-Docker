# TS3AudioBot-Docker

![Docker](https://github.com/CookieCr2nk/TS3AudioBot-Docker/workflows/Docker/badge.svg?branch=master)

This is the TS3AudioBot in a Docker Container based on Debian Buster with dotnet runtime 3.1

# Usage / Parameters

Setup the data directory

```
mkdir -p /opt/ts3audiobot/data
chown -R 9999:9999 /opt/ts3audiobot/data
```

Run the initial setup to generate all the initial configuration files:

```docker run --rm -v /opt/ts3audiobot/data:/data -it hcr.io/cookiecr2nk/ts3audiobot:latest```

After the initial configuration setup has finished, stop the server with CTRL-C and configure your bot in the configuration files accordingly. Then run the actual container again as a daemon:

```docker run --name ts3audiobot -d -p 58913:58913 -v /opt/ts3audiobot/data:/data hcr.io/cookiecr2nk/ts3audiobot:latest```


#Docker Image Building

* Docker Build:  ```docker build -f Dockerfile . ```

# Contribution

Feel free to make an feature request or an pull request.

# Ressources

This Dockerfile uses minimal ressources.

# TS3AudioBot Version

This image was build on develop_linux_x64 with version ```develop_linux_x64 0.12.0-alpha.52```
