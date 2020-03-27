i# Netrek Server
## Build
`docker build -t netrek-server .`
## Run
`docker run -d  --name netrek-server -p 2592:2592 -p 2592:2592/udp netrek-server`
Mount volumes for netrek logs, etc.
`docker run -d --name netrek-server -p 2592:2592 -p 2592:2592/udp --read-only=true -v /data/netrek/server/:/usr/local/games/netrek-server-vanilla/var netrek-server`
