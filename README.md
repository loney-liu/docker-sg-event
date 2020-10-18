## Install

#### Clone git repo

```
$git clone https://github.com/loney-liu/docker-sg-event
```

#### Required submodule [python-api](https://github.com/shotgunsoftware/python-api) and [shotgunEvents](https://github.com/shotgunsoftware/shotgunEvents)

```
$cd docker-sg-event/python-api
$git submodule init
$git submodule update


$cd docker-sg-event/shotgunEvents
$git submodule init
$git submodule update
```

#### Configure shotgunEvents

'''
- Copy docker-sg-event/shotgunEvents/src/shotgunEventDaemon.conf to docker-sg-event/
- Modify docker-sg-event/shotgunEventDaemon.conf
- Copy docker-sg-event/env/evnet-variables.env.example to docker-sg-event/env/evnet-variables.env
- Modify docker-sg-event/env/evnet-variables.env to add shotgun url and script users/keys
- Copy plugin to docker-sg-event/plugins
'''

#### Switch between python2 and python3

Edit docker-sg-event/docker-compose.yml

```
      # dockerfile: ./build/py2/Dockerfile
      dockerfile: ./build/py3/Dockerfile
```

#### Build shotgunEvents

```
$ sudo docker-compose build
```

#### Start shotgunEvents

```
$ sudo docker-compose up -d
```

#### Stop shotgunEvents

```
$ sudo docker-compose down
```