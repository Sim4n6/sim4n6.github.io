---
title: Generate and Decode a QR image from cmdline
updated: 2019-07-28 18:30
---

#### Tools installation under GNU/Linux Debian

```
sudo apt install zbar-tools qrencode
```

#### Generate a QR image using cmd line

```
qrencode "Message-to-embed" -o qr.png
```

#### Decode a QR image using cmd line

```
zbarimg qr.png
```
