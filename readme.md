# Overview

This is a quick development template meant to speed up the scaffolding of Docker-containerized MEAN applications with vs-code debugging extensions. There are three containers (angular-client, express-server, and mongodb) that are run simultaneously and properly connected using docker compose. First cd into the main folder:

```
$ cd mean-docker-template
```

 Then use Docker Compose

 ```
 $ docker-compose up -d
 ```

 This will build the three containers if they don't already exist, then start them. You can now view the application in a browser at http://localhost:4200/, which is the entry point of the Angular app. The api the Angular client connects to for CRUD operations is reachable on http://localhost:3000/.

 The project comes with a preconfigured .vscode/launch.json file which a "Docker: Attach to Node" configuration. To be able to use this, the alternate docker-compose.debug.yml file has to be invoked thus:

 ```
 docker-compose -f docker-compose.debug.yml up -d --build
 ```
Once that is running, in the debug dropdown menu, select "Docker: Attach to Node". You should now be able to set working breakpoints in the express-server js files.