### Usage
`docker pull mcdull2020/server`

```
cat <<EOF > key
VPN_IPSEC_PSK=vpn
VPN_USER=vpn
VPN_PASSWORD=vpn
EOF
```
```
docker run \
    --name server \
    --env-file ./key \
    --restart=always \
    -p 500:500/udp \
    -p 4500:4500/udp \
    -d --privileged \
    mcdull2020/server
```
