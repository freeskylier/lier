To run Lantern on a server, you simply need to set a flag to build it in headless mode and then tell it to run on any local address as opposed to binding to localhost (so that it's accessible from other machines). You can do this as follows:

1. Check out the Lantern source code and do preliminary setup -- see https://github.com/getlantern/lantern
1. ```HEADLESS=true make docker-linux```
1. ```lantern_linux_amd64 --addr 0.0.0.0:8787``` or ```lantern_linux_386 --addr 0.0.0.0:8787```