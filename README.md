# connect to vm and disable gdm
```bash
sudo systemctl disable gdm
sudo systemctl stop gdm
curl -fsSL https://tailscale.com/install.sh | sh
sudo systemctl enable --now tailscaled
sudo tailscale up --token
```


```
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker vmadmin
```

# remember to run cf tunnel
```
docker run cloudflare/cloudflared:latest tunnel --no-autoupdate run --token CHANGEMEEEE
```
# make /data and mount
