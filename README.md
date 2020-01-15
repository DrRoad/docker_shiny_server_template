# docker_shiny_server_template
A simple template to deploy 1 (or more) shiny apps to a localhost or cloud server.

# Installation
```
git clone https://github.com/bradlindblad/docker_shiny_server_template
```

# Usage
## Setup
- Place your app.R file in srv/shinyapps
- If your app needs more libraries, add them to the third command in the Dockerfile
- If you find that your libraries don't work, you may need to further install linux dependencies, which you can append to the second command in the Dockerfile


## Build 
cd into the root and run:
```
sudo docker build . -t {your tag name here}
```

At this point you should have a docker image available

## Run

Run the image with the following command:

```
docker run --rm -p 3838:3838 {your tag name here}

```

## View the app in a browser

Go to a browser and view the app on localhost (linux in this case):

```
Enter in browser:
localhost:3838
```