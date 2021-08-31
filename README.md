# wireguard-ui-docker

Dockerized `wireguard-ui`, a web user interface to manage your WireGuard setup.
For more information refer to [wireguard-ui repository](//github.com/ngoduykhanh/wireguard-ui).

## Usage

Example Docker Compose file can be found here: [docker-compose.yaml](https://github.com/ngoduykhanh/wireguard-ui/blob/master/docker-compose.yaml)

Remove or comment out `build: .` and replace `#image: ngoduykhanh/wireguard-ui:latest` lines:
```diff
  version: "3"

  services:
    wg:
-     build: .
-     #image: ngoduykhanh/wireguard-ui:latest
+     image: ghcr.io/im-mortal/wireguard-ui-docker:latest
      container_name: wgui
…
```

Also, adjust volume mount points to work with your setup. Then run:
```sh
docker-compose up
```


## Credits

All credit goes to [ngoduykhanh](//github.com/ngoduykhanh) and wireguard-ui's [contributors](//github.com/ngoduykhanh/wireguard-ui/graphs/contributors).
