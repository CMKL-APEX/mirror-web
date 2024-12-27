# CMKL Mirrors

* Fork from tuna/mirror-web License with GPLv2

### Docker

Download following assets before build:
```bash
cd mirror-web
mkdir -p static/status
wget https://mirrors.tuna.tsinghua.edu.cn/static/tunasync.json -O static/tunasync.json
wget https://mirrors.tuna.tsinghua.edu.cn/static/tunet.json -O static/tunet.json
wget https://mirrors.tuna.tsinghua.edu.cn/static/status/isoinfo.json -O static/status/isoinfo.json

```


Build In Docker：
```bash
cd mirror-web
docker build -t builden -f Dockerfile.build .
docker run -it -v /path/to/mirror-web/:/data builden
```