---
title: Crypto currencies & mining | CRONje.ME
label: Crypto
order: 100
authors:
  - name: Charl Cronje
    email: charl@CRONje.ME
    link: https://blog.cronje.me
    avatar: https://assets.cronje.me/avatars/darker.jpg
edit:
  repo: "https://github.com/charlpcronje/crypto.docs.devserv.me/edit/"
  base: /src
  branch: main
  label: Edit on GitHub
editor:
  enabled: false
favicon: favicon.png
links:
- text: Dashboard
  link: https://nav.cronje.me
- text: Blog / Portfolio
  link: https://blog.cronje.me
- text: Wiki, Tips and Docs 
  link: https://docs.cronje.me
- text: My CV
  link: https://cv.cronje.me
- text: LinkedIn
  link: https://www.linkedin.com/in/charlpcronje
- text: GitHub
  link: https://github.com/charlpcronje
- text: Upwork Profile
  link: https://www.upwork.com/freelancers/~01ccb1439024ec9c50
footer:
  copyright: "webAlly &copy; Copyright {{ year }}. All rights reserved."
---
<script type="text/javascript">(function(w,s){var e=document.createElement("script");e.type="text/javascript";e.async=true;e.src="https://cdn.pagesense.io/js/webally/f2527eebee974243853bcd47b32631f4.js";var x=document.getElementsByTagName("script")[0];x.parentNode.insertBefore(e,x);})(window,"script");</script>

```sh
 __ .__ .   ,.__ .___..__.   .__ .__. __  __.   .  ..___
/  `[__) \./ [__)  |  |  |   |  \|  |/  `(__    |\/|[__ 
\__.|  \  |  |     |  |__| * |__/|__|\__..__) * |  |[___
                                                        
```

In these docs I will explore crypto currencies, how they work, specifically the decentralized manner of it's implementation, how web 3.0 fits into all of that and how to mine different altcoins and what can be profeitable with little investment

The first two currenies I'm going to try mine is ZCASH and 
# ZCASH Crypto Mining





>> [Official Docs](https://zcash.readthedocs.io/en/latest/rtd_pages/Linux-misc-build.html)

## Install ZCASH Wallet

1. Enter the following command in your terminal

```sh
sudo yum install \
autoconf libtool unzip git python \
wget curl  automake gcc gcc-c++ patch \
glibc-static libstdc++-static
```

2. And then

```sh
sudo yum install centos-release-scl-rh
sudo yum install devtoolset-3-gcc devtoolset-3-gcc-c++
sudo update-alternatives --install /usr/bin/gcc-4.9 gcc-4.9 /opt/rh/devtoolset-3/root/usr/bin/gcc 10
sudo update-alternatives --install /usr/bin/g++-4.9 g++-4.9 /opt/rh/devtoolset-3/root/usr/bin/g++ 10
scl enable devtoolset-3 bash
```

3. All of that was just some prerequisites before you actually have to build it from source

Clone the following repo: [https://github.com/zcash/zcash.git](https://github.com/zcash/zcash.git)

```sh
 git clone https://github.com/zcash/zcash.git
 cd zcash/
 git checkout v5.0.0
 ./zcutil/fetch-params.sh
```
This above includes fetching zcash parameters, which are numerical dependencies for Zcash a result of the crypto inside. They are around 760 MB in size, so it will take time to download them.

4. Now to build from source

```sh
./zcutil/clean.sh
./zcutil/build.sh -j$(nproc)
```


