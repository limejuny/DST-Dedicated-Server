* Cloning

```bash
$ mkdir ~/.klei
$ git clone --recurse-submodules https://github.com/eggmoid/DST-Dedicated-Server.git ~/.klei/DoNotStarveTogether
```

* Update

```bash
$ git pull --recurse-submodules
```

* Run docker images
  * The server may take up to ~15min to fully start.
  * as of Oracle Cloud ```VM.Standard.E2.1.Micro``` instance.

```bash
$ docker run --rm --name dst-server -d -v ${HOME}/.klei/DoNotStarveTogether:/data -p 10999-11000:10999-11000/udp -p 12346-12347:12346-12347/udp -it dst-server:latest
```
