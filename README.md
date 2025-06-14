# Home Assistant Addons by barneyonline

This repository provides the following addons for Home-Assistant:

- Home-Assistant-Matter-Hub

## Installation

Simple add this repository to your Add On Store in Home-Assistant:

1. Open the UI of your Home Assistant instance
2. Go to `Settings` -> `Add-Ons` -> `Add-On Store`
3. Click the three dots in the top-right corner and select `Repositories`
4. Paste the repository URL (`https://github.com/barneyonline/home-assistant-addons`) into the text-field and click "Add"
5. Refresh your Add-On Store and Install the Add-On

## Building and publishing the add-on image

The add-ons in this repository reference Docker images hosted on GitHub
Container Registry (GHCR). If you want to build and test your own version,
create the Docker image and push it to GHCR:

```bash
docker login ghcr.io
docker build -t ghcr.io/<your_user>/home-assistant-matter-hub-addon:latest ./hamh_test
docker push ghcr.io/<your_user>/home-assistant-matter-hub-addon:latest
```

Home Assistant will pull this image when installing the add-on. Ensure the
image is public or that your Home Assistant instance is authenticated to GHCR
so it can access the image.

