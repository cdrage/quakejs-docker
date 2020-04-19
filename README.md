A fully local and Dockerized server of quakejs.
-----

The purpose of this project was to create a fully independent quakejs server that doesn't need any content served from the internet.
Hence, once pulled, this does not need to connect to any external provider, ie. content.quakejs.com. Nor does this server need to be proxied/served/relayed from http://www.quakejs.com/

Simply pull the image [treyyoder/quakejs](https://hub.docker.com/r/treyyoder/quakejs) and run it:

```
docker run -d --name quakejs -e SERVER=<SERVER NAME OR IP> -e HTTP_PORT=<HTTP_PORT> -p <HTTP_PORT>:80 -p 27960:27960 treyyoder/quakejs:latest
```

Example:

```
docker run -d --name quakejs -e SERVER=10.0.0.2 -e HTTP_PORT=8080 -p 8080:80 -p 27960:27960 treyyoder/quakejs:latest
```

Send all you friends/coworkers the link: ex. http://10.0.0.2:8080 and happy fragging ;)

Credits:

Thanks to @begleysm with [his fork](https://github.com/begleysm/quakejs) of [quakejs](https://github.com/inolen/quakejs) and [documentation](https://steamforge.net/wiki/index.php/How_to_setup_a_local_QuakeJS_server_under_Debian_9_or_Debian_10)
