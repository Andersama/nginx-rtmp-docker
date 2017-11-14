# nginx-rtmp-docker
**Dockerfile for building lightweight nginx + rtmp module for replicating streams**

## Usage
`docker run -dp 1935:1935 unknowngeek/nginx-rtmp-ffmpeg`

If you want to use a custom nginx.conf file, create a volume mapping:

`docker run -dp 1935:1935 -v /path/to/my/custom/nginx.conf:/etc/nginx/nginx.conf unknowngeek/nginx-rtmp-ffmpeg`

## Troubleshooting
If you encounter an error like this:
```
[alert] could not open error log file: open() "/var/log/nginx/access.log" failed (13: Permission denied)
```

Then you are running an outdated version of Docker. See [the Docker documentation](https://docs.docker.com/engine/installation/) on how to get the latest version.

## More info
Docker Hub: https://hub.docker.com/r/unknowngeek/nginx-rtmp-ffmpeg/

Based on setup described on the OBS forums [here](https://obsproject.com/forum/resources/how-to-set-up-your-own-private-rtmp-server-using-nginx.50/).