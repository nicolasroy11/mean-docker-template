# Overview

This is a quick development template meant to speed up the scaffolding of Docker-containerized MEAN applications with vs-code debugging extensions. There are three containers that can be run simultaneously using docker compose. First cd into the main folder:

```
$ cd mean-docker-template
```

 Then use Docker Compose

 ```
 $ docker-compose up -d
 ```

 This will build the three containers if they don't already exist, then start them.

 The project comes with a preconfigured .vscode/launch.json file which a "Docker: Attach to Node" configuration. To be able to use this, the alternate docker-compose.debug.yml file has to be invoked thus:

 ```
 docker-compose -f docker-compose.debug.yml up -d --build
 ```
Once that is running, in the debug dropdown menu, select "Docker: Attach to Node". You should now be able to set working breakpoints in the express-server js files.