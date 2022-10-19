# vscale-wireguard-vpn-setup

Bash script that installs WireGuard VPN on a Linux-based VPS

## Installation

Run script with `sh`

```bash
sh -c "$(wget https://raw.githubusercontent.com/borisevstratov/vscale-wireguard-vpn-setup/master/setup.sh -O -)"
```

## Set up client devices

100 peers are available by default.

### iOS/Android

Generate tunnel QR codes

```bash
docker exec -it wireguard /app/show-peer 1
```

### Mac/Windows

Copy configuration information

```bash
cat ~/wireguard/config/peer1/peer1.conf 
```

## Misc

Restart WireGuard

```bash
docker-compose -f ~/wireguard/docker-compose.yml up -d
```