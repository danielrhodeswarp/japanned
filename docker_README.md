INSTRUCTIONS FOR EMBERJS DOCKER TEMPLATE

(for v3)
- as for v2 (but note the interactive container will always fail to run just on 'docker-compose up') but then can do [docker-compose run danielrhodeswarp-emberjs-interactive]
    (and su to 'node' user) for ember CLI stuff :-)

(for v2)

- docker-compose up [will build OK but then error on running ("exited with code 1"), this is ok]
- [first time only] docker run -v "$PWD"/ember_project:/ember_project -it emberjs_danielrhodeswarp-emberjs-app-server bash
    (logs you in where you can su to node user then generate the working ember fileset thus:

    cd /ember_project
    su node
    ember init
    npm install
    exit
    exit
    )
    NOW docker-compose up will start both the app and test server which you can see at
    localhost:4200 and localhost:7357 !!(respectively)

(for v1) docker-compose run --service-ports danielrhodeswarp-emberjs2-node bash

GOALS
[todo] all extras (Watchman, PhantomJS) installed
[done] dev web server (and the liveReload thing) and test server running all the time
[done] interactive shell for ember CLI commands


TODO
[] database or summat for Ember Data
[] multiple emberjs proj support
[] user configurable version of node to use
[] user configurable version of emberjs to use
[] user configurable port forwarding (or summat on the docker CLI)
