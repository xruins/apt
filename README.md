# xruins APT repository

This repository is published via GitHub Pages and serves Debian/Ubuntu packages for `amd64` and `arm64`.

## Add to `sources.list.d`

1. Import the repository signing key:

```bash
curl -fsSL https://xruins.github.io/apt/public.key | sudo gpg --dearmor -o /usr/share/keyrings/xruins-apt.gpg
```

2. Add the repo to `sources.list.d`:

```bash
echo "deb [arch=amd64,arm64 signed-by=/usr/share/keyrings/xruins-apt.gpg] https://xruins.github.io/apt/ stable main" | sudo tee /etc/apt/sources.list.d/xruins-apt.list
```

3. Update and install packages:

```bash
sudo apt-get update
sudo apt-get install -y ab-av1 vmagent
```
