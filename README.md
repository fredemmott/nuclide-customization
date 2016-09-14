Tested with standard system ruby on OSX 10.11.6, and HHVM 3.15.0 running in docker.

Configuration
=============

This depends on two files:
 - `~/.dev_container`: plain text, single line - name of docker image to execute hh_client in
 - `~/.container_paths.json`: `Map<ContainerName,Map<HostPath,ContainerPath>`

For example:

```
typhon:~ fred$ cat ~/.dev_container
romantic_keller
typhon:~ fred$ cat ~/.container_paths.json
{
  "romantic_keller": {
    "/Users/fred/hackdev": "/root/hackdev"
  }
}
```

Usage
=====

Run like hh_client from a terminal window. You can also configure Nuclide to use it in the `nuclide-hack` package settings inside atom - specify the full path.