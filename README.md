# coraine apt repository

Debian packages of [coraine](https://github.com/SEAMWARE/coraine), the NGSI-LD context broker - signed,
served by GitHub Pages at **https://seamware.github.io/apt**. Built and published by coraine's CI
(`.github/workflows/packages.yml`); nothing here is edited by hand.

```sh
curl -fsSL https://seamware.github.io/apt/coraine.gpg | sudo tee /usr/share/keyrings/coraine.gpg > /dev/null
echo "deb [signed-by=/usr/share/keyrings/coraine.gpg] https://seamware.github.io/apt $(. /etc/os-release; echo $VERSION_CODENAME) main" \
  | sudo tee /etc/apt/sources.list.d/coraine.list
sudo apt update && sudo apt install coraine
```

Ubuntu 26.04 (resolute), Ubuntu 24.04 (noble), Debian 13 (trixie); amd64 and arm64.
