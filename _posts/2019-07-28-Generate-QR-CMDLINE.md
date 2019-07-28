---
title: How to generate/decode a QR image from cmd line ?
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

#### Terminal recording

<a href="https://asciinema.org/a/H4QUaFZ7eLvCQ0NzccxvsTf6h" target="_blank"><img src="https://asciinema.org/a/H4QUaFZ7eLvCQ0NzccxvsTf6h.svg" /></a>