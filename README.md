## 自编译lede_openwrt用DL包 
使用机型，树莓派3B+ </br>
make menuconfig前三项选择，
![image](https://github.com/user-attachments/assets/cf6a69b1-309d-4ecf-a904-c85565b0111b)

Target Images的内核空间Kernel partition size (in MiB) ,给他差不多1G，以避免编译固件的时候，勾选太多东西，
导致编译出来的固件，烧写到设备上以后，不能读写、保存。
![image](https://github.com/user-attachments/assets/f35107e8-bb0f-4ecc-856d-0fdf8b9f29df)

近期dl包编译时间：2024-10-25
此为较为干净的版本（对于部分人来说，部分依赖库、依赖包没用）
可能有部分没有覆盖到，比如linux5.15   linux5.4  linux6.1这几个源码文件。


文件清单：</br>
acl-2.3.1.tar.gz</br>
argp-standalone-1.3.tar.gz</br>
attr-2.5.1.tar.gz</br>
autoconf-2.69.tar.xz</br>
autoconf-archive-2021.02.19.tar.xz</br>
automake-1.15.1.tar.xz</br>
automake-1.16.5.tar.gz</br>
backports-6.1.24.tar.xz</br>
bc-1.07.1.tar.gz</br>
bcm27xx-userland-c4fd1b8986c6d6d4ae5cd51e65a8bbeb495dfa4e.tar.gz</br>
bcm27xx-utils-2024-01-18.tar.xz</br>
binutils-2.40.tar.xz</br>
bison-3.8.2.tar.xz</br>
bpftools-2022-03-08-04c465fd.tar.xz</br>
broadcom-wl-4.150.10.5.tar.bz2</br>
broadcom-wl-5.100.138.tar.bz2</br>
btrfs-progs-v5.16.1.tar.xz</br>
busybox-1.36.0.tar.bz2</br>
bzip2-1.0.8.tar.gz</br>
ca-certificates_20211016.tar.xz</br>
c-ares-1.18.1.tar.gz</br>
cgroupfs-mount-2020-06-26-05494281.tar.xz</br>
cmake-3.25.2.tar.gz</br>
containerd-1.7.18.tar.gz</br>
coremark-2022-07-27.tar.gz</br>
coreutils-9.3.tar.xz</br>
cpio-2.13.tar.bz2</br>
cpio-2.15.tar.bz2</br>
cryptodev-linux-1.13.tar.gz</br>
curl-8.6.0.tar.bz2</br>
cypress-firmware-5.10.9-2022_0909.tar.xz</br>
cypress-firmware-5.4.18-2021_0812.tar.xz</br>
cypress-nvram-2019-09-03-e7b78df2.tar.xz</br>
dl_list.txt</br>
dnsmasq-2.88.tar.xz</br>
docker-27.0.2.tar.gz</br>
dockerd-27.0.2.tar.gz</br>
dosfstools-4.2.tar.gz</br>
dropbear-2022.82.tar.bz2</br>
dtc-1.6.1.tar.xz</br>
e2fsprogs-1.46.5.tar.xz</br>
e2fsprogs-1.47.0.tar.xz</br>
ELFkickers-3.2.tar.gz</br>
elfutils-0.188.tar.bz2</br>
etherwake_1.09.orig.tar.gz</br>
expat-2.5.0.tar.xz</br>
f2fs-tools-1.16.0.tar.gz</br>
fakeroot_1.29.orig.tar.gz</br>
findutils-4.9.0.tar.xz</br>
firewall-2022-02-17-4cd7d4f3.tar.xz</br>
firmware-utils-2022-12-15-bd856eff.tar.xz</br>
flex-2.6.4.tar.gz</br>
fortify-headers-1.1.tar.gz</br>
fstools-2023-01-22-1ea5855e.tar.xz</br>
fstools-2024-01-22-08cd7083.tar.xz</br>
fullconenat-2022-02-13-108a36cb.tar.xz</br>
fwtool-2019-11-12-8f7fe925.tar.xz</br>
gcc-11.3.0.tar.xz</br>
gcc-11.3.0.tar.xz.dl</br>
gcc-11.3.0.tar.xz.hash</br>
gdb-14.1.tar.xz</br>
gengetopt-2.23.tar.xz</br>
gmp-6.2.1.tar.xz</br>
go1.17.13.src.tar.gz</br>
go1.20.14.src.tar.gz</br>
go1.23.1.src.tar.gz</br>
go1.4-bootstrap-20171003.tar.gz</br>
gperf-3.1.tar.gz</br>
hostapd-2022-07-29-b704dc72.tar.xz</br>
iproute2-6.2.0.tar.xz</br>
ipset-7.17.tar.bz2</br>
ipset-7.21.tar.bz2</br>
iptables-1.8.7.tar.bz2</br>
iw-5.19.tar.xz</br>
json-c-0.16-nodoc.tar.gz</br>
json-c-0.17-nodoc.tar.gz</br>
jsonfilter-2018-02-04-c7e938d6.tar.xz</br>
libcap-2.68.tar.xz</br>
libdeflate-1.17.tar.xz</br>
libev-4.33.tar.gz</br>
libiwinfo-2023-05-17-c9f5c3f7.tar.xz</br>
libiwinfo-2024-03-08-8ffb8bfd.tar.xz</br>
libmnl-1.0.5.tar.bz2</br>
libnl-tiny-2022-11-01-db3b2cdb.tar.xz</br>
libnl-tiny-2023-07-01-d433990c.tar.xz</br>
libpcap-1.10.3.tar.gz</br>
libressl-3.7.0.tar.gz</br>
libseccomp-2.5.4.tar.gz</br>
libselinux-3.5.tar.gz</br>
libsepol-3.3.tar.gz</br>
libsodium-1.0.18.tar.gz</br>
libtool-2.4.2.tar.xz</br>
libtool-2.4.7.tar.xz</br>
libubox-2022-09-27-ea560134.tar.xz</br>
libuv-v1.48.0.tar.gz</br>
libwebsockets-4.3.2.tar.gz</br>
linux-5.15.148.tar.xz</br>
linux-6.1.112.tar.xz</br>
linux-6.1.112.tar.xz.1</br>
linux-6.1.112.tar.xz.dl</br>
linux-6.1.112.tar.xz.hash</br>
linux-atm-2.5.2.tar.gz</br>
linux-firmware-20231211.tar.xz</br>
linux-firmware-20240909.tar.xz</br>
lua-5.1.5.tar.gz</br>
LuaSrcDiet-0.12.1.tar.bz2</br>
lzma-4.65.tar.bz2</br>
lzo-2.10.tar.gz</br>
m4-1.4.19.tar.xz</br>
make-ext4fs-2020-01-05-5c201be7.tar.xz</br>
mbedtls-2.28.5.tar.gz</br>
meson-0.61.5.tar.gz</br>
miniupnpd-2.0.20170421.tar.gz</br>
mklibs_0.1.45.tar.xz</br>
mpc-1.3.1.tar.gz</br>
mpfr-4.2.0.tar.xz</br>
mtd-utils-2.1.5.tar.bz2</br>
mtools-4.0.42.tar.bz2</br>
musl-1.2.4.tar.gz</br>
musl-fts-1.2.7.tar.xz</br>
ncurses-6.4.tar.gz</br>
netifd-2021-06-04-50381d0a.tar.xz</br>
nghttp2-1.51.0.tar.xz</br>
ninja-1.11.1.tar.gz</br>
nlbwmon-2021-09-01-d82c910c.tar.xz</br>
odhcp6c-2021-01-09-53f07e90.tar.xz</br>
odhcpd-2021-06-19-564d25e5.tar.xz</br>
openssl-3.0.13.tar.gz</br>
openssl-3.0.15.tar.gz</br>
openwrt-keyring-2022-03-25-62471e69.tar.xz</br>
opkg-2022-02-24-d038e5b6.tar.xz</br>
patch-2.7.6.tar.xz</br>
patchelf-0.17.2.tar.bz2</br>
pcre2-10.42.tar.bz2</br>
pcre-8.45.tar.bz2</br>
pdnsd-1.2.9b-par.tar.xz</br>
pkgconf-1.9.3.tar.xz</br>
ppp-2.4.9.git-2021-01-04.tar.xz</br>
procd-2023-01-16-190f13a7.tar.xz</br>
quilt-0.67.tar.gz</br>
rpcd-2023-01-21-c0df2a7a.tar.xz</br>
rpi-firmware-3673be308132de102fdff491d1333d9d0f823557-bootcode.bin</br>
rpi-firmware-3673be308132de102fdff491d1333d9d0f823557-fixup4cd.dat</br>
rpi-firmware-3673be308132de102fdff491d1333d9d0f823557-fixup4.dat</br>
rpi-firmware-3673be308132de102fdff491d1333d9d0f823557-fixup4x.dat</br>
rpi-firmware-3673be308132de102fdff491d1333d9d0f823557-fixup_cd.dat</br>
rpi-firmware-3673be308132de102fdff491d1333d9d0f823557-fixup.dat</br>
rpi-firmware-3673be308132de102fdff491d1333d9d0f823557-fixup_x.dat</br>
rpi-firmware-3673be308132de102fdff491d1333d9d0f823557-LICENCE.broadcom</br>
rpi-firmware-3673be308132de102fdff491d1333d9d0f823557-start4cd.elf</br>
rpi-firmware-3673be308132de102fdff491d1333d9d0f823557-start4.elf</br>
rpi-firmware-3673be308132de102fdff491d1333d9d0f823557-start4x.elf</br>
rpi-firmware-3673be308132de102fdff491d1333d9d0f823557-start_cd.elf</br>
rpi-firmware-3673be308132de102fdff491d1333d9d0f823557-start.elf</br>
rpi-firmware-3673be308132de102fdff491d1333d9d0f823557-start_x.elf</br>
runc-1.1.13.tar.gz</br>
sed-4.9.tar.xz</br>
shadowsocks-libev-3.3.5.tar.gz</br>
squashfskit-v4.14.tar.xz</br>
tar-1.34.tar.xz</br>
tini-0.19.0.tar.gz</br>
ttyd-1.6.3.tar.gz</br>
u-boot-2023.01.tar.bz2</br>
ubox-2022-08-13-4c7b720b.tar.xz</br>
ubus-2022-06-01-2bebf93c.tar.xz</br>
ucert-2020-05-24-00b921d8.tar.xz</br>
uci-2021-10-22-f84f49f0.tar.xz</br>
uclient-2021-05-14-6a6011df.tar.xz</br>
ucode-2023-01-09-8dad974b.tar.xz</br>
uhttpd-2022-10-31-23977554.tar.xz</br>
usign-2020-05-23-f1f65026.tar.xz</br>
ustream-ssl-2022-12-08-9217ab46.tar.xz</br>
util-linux-2.38.1.tar.xz</br>
util-linux-2.39.3.tar.xz</br>
vlmcsd-svn1113.tar.gz</br>
vsftpd-3.0.5.tar.gz</br>
wget-1.21.3.tar.gz</br>
wireless-regdb-2022.08.12.tar.xz</br>
wol-0.7.1.tar.gz</br>
wolfssl-5.5.4-stable.tar.gz</br>
xray-core-1.3.1.tar.gz</br>
xz-5.4.1.tar.bz2</br>
zip30.tar.gz</br>
zlib-1.2.13.tar.xz</br>
zstd-1.5.5.tar.gz</br>


以下是我个人编译自用的openwrt，make download -j8所下载的内容，
可以自行选择将主域名加入代理，或者直连，
或者可以手动进行下载，然后放置dl目录，以便于后续编译。
File: .gdb-14.1.tar.xz URL: </br>
File: .gcc-11.3.0.tar.xz URL: </br>
File: .binutils-2.40.tar.xz URL: </br>
File: .gcc-11.3.0.tar.xz URL: </br>
File: .fortify-headers-1.1.tar.gz URL: </br>
File: .linux-5.15.148.tar.xz URL: </br>
File: .musl-1.2.4.tar.gz URL: https://mirror.iscas.ac.cn/kernel.org/linux/kernel/v5.x/linux-5.15.148.tar.xz</br>
File: .adguardhome-frontend-0.107.53.tar.gz URL: https://musl.libc.org/releases/musl-1.2.4.tar.gz</br>
File: .lucihttp-2023-03-15-9b5b683f.tar.xz URL: https://github.com/AdguardTeam/AdGuardHome/releases/download/v0.107.53/AdGuardHome_frontend.tar.gz</br>
File: .attr-2.5.1.tar.gz URL: https://sources.cdn.openwrt.org/lucihttp-2023-03-15-9b5b683f.tar.xz</br>
File: .cgroupfs-mount-2020-06-26-05494281.tar.xz URL: http://git.savannah.nongnu.org/cgit/attr.git/snapshot/attr-2.5.1.tar.gz</br>
File: .btrfs-progs-v5.16.1.tar.xz URL: </br>
File: .cgi-io-2022-08-10-901b0f04.tar.xz URL: </br>
File: .containerd-1.7.18.tar.gz URL: https://mirror.iscas.ac.cn/kernel.org/linux/kernel/people/kdave/btrfs-progs/btrfs-progs-v5.16.1.tar.xz</br>
File: .coremark-2022-07-27.tar.gz URL: https://sources.cdn.openwrt.org/cgi-io-2022-08-10-901b0f04.tar.xz</br>
File: .coreutils-9.3.tar.xz URL: https://codeload.github.com/eembc/coremark/tar.gz/eefc986ebd3452d6adde22eafaff3e5c859f29e4?/coremark-2022-07-27.tar.gz</br>
File: .dns2tcp-1.1.2.tar.gz URL: https://downloads.sourceforge.net/dns2socks/SourceCode.zip</br>
File: .docker-27.0.2.tar.gz URL: https://codeload.github.com/zfl9/dns2tcp/tar.gz/v1.1.2?/dns2tcp-1.1.2.tar.gz</br>
File: .v2.28.1.tar.gz URL: https://codeload.github.com/docker/cli/tar.gz/v27.0.2?/docker-27.0.2.tar.gz</br>
File: .dockerd-27.0.2.tar.gz URL: https://codeload.github.com/docker/compose/tar.gz/v2.28.1?/v2.28.1.tar.gz</br>
File: .adguardhome-0.107.53.tar.gz URL: https://codeload.github.com/moby/moby/tar.gz/v27.0.2?/dockerd-27.0.2.tar.gz</br>
File: .etherwake_1.09.orig.tar.gz URL: https://codeload.github.com/AdguardTeam/AdGuardHome/tar.gz/v0.107.53?/adguardhome-0.107.53.tar.gz</br>
File: .libev-4.33.tar.gz URL: http://ftp.debian.org/debian/pool/main/e/etherwake/etherwake_1.09.orig.tar.gz</br>
File: .libseccomp-2.5.4.tar.gz URL: http://dist.schmorp.de/libev/Attic/libev-4.33.tar.gz</br>
File: .libsodium-1.0.18.tar.gz URL: https://github.com/seccomp/libseccomp/releases/download/v2.5.4/libseccomp-2.5.4.tar.gz</br>
File: .libuv-v1.48.0.tar.gz URL: https://download.libsodium.org/libsodium/releases/libsodium-1.0.18.tar.gz</br>
File: .libwebsockets-4.3.2.tar.gz URL: https://dist.libuv.org/dist/v1.48.0/libuv-v1.48.0.tar.gz</br>
File: .lzo-2.10.tar.gz URL: https://codeload.github.com/warmcat/libwebsockets/tar.gz/v4.3.2?/libwebsockets-4.3.2.tar.gz</br>
File: .microsocks-1.0.4.tar.gz URL: http://www.oberhumer.com/opensource/lzo/download/lzo-2.10.tar.gz</br>
File: .miniupnpd-2.0.20170421.tar.gz URL: https://codeload.github.com/rofl0r/microsocks/tar.gz/v1.0.4?/microsocks-1.0.4.tar.gz</br>
File: .nano-7.2.tar.xz URL: http://miniupnp.tuxfamily.org/files/miniupnpd-2.0.20170421.tar.gz</br>
File: .nghttp2-1.51.0.tar.xz URL: https://mirrors.aliyun.com/gnu/nano/nano-7.2.tar.xz</br>
File: .nlbwmon-2021-09-01-d82c910c.tar.xz URL: https://github.com/nghttp2/nghttp2/releases/download/v1.51.0/nghttp2-1.51.0.tar.xz</br>
File: .parted-3.4.tar.xz URL: https://sources.cdn.openwrt.org/nlbwmon-2021-09-01-d82c910c.tar.xz</br>
File: .pdnsd-1.2.9b-par.tar.xz URL: https://github.com/PCRE2Project/pcre2/releases/download/pcre2-10.42/pcre2-10.42.tar.bz2</br>
File: .runc-1.1.13.tar.gz URL: https://sources.openwrt.org/pdnsd-1.2.9b-par.tar.xz</br>
File: .smartmontools-7.4.tar.gz URL: https://codeload.github.com/opencontainers/runc/tar.gz/v1.1.13?/runc-1.1.13.tar.gz</br>
File: .tcping-0.3-db9101834732dac9aaa59dbb7fb9c74612dbf723.tar.gz URL: https://mirror2.openwrt.org/sources/pdnsd-1.2.9b-par.tar.xz</br>
File: .tini-0.19.0.tar.gz URL: https://sources.openwrt.org/tcping-0.3-db9101834732dac9aaa59dbb7fb9c74612dbf723.tar.gz</br>
File: .ttyd-1.6.3.tar.gz URL: https://codeload.github.com/krallin/tini/tar.gz/v0.19.0?/tini-0.19.0.tar.gz</br>
File: .udns-0.4.tar.gz URL: https://mirror2.openwrt.org/sources/tcping-0.3-db9101834732dac9aaa59dbb7fb9c74612dbf723.tar.gz</br>
File: .vlmcsd-svn1113.tar.gz URL: http://ftp.vim.org/pub/vim/unix/vim-8.2.tar.bz2</br>
File: .wget-1.21.3.tar.gz URL: https://codeload.github.com/Wind4/vlmcsd/tar.gz/svn1113?/vlmcsd-svn1113.tar.gz</br>
File: .xray-core-24.10.16.tar.gz URL: https://mirrors.aliyun.com/gnu/wget/wget-1.21.3.tar.gz</br>
File: .neturl-1.1-1.tar.gz URL: https://codeload.github.com/XTLS/Xray-core/tar.gz/v24.10.16?/xray-core-24.10.16.tar.gz</br>
File: .mosdns-5.3.3.tar.gz URL: https://codeload.github.com/golgote/neturl/tar.gz/v1.1-1?/neturl-1.1-1.tar.gz</br>
File: .shadowsocks-v1.21.2.aarch64-unknown-linux-musl.tar.xz URL: https://codeload.github.com/IrineSistiana/mosdns/tar.gz/v5.3.3?/mosdns-5.3.3.tar.gz</br>
File: .shadowsocksr-libev-2.5.3.tar.gz URL: </br>
File: .simple-obfs-0.0.5.tar.xz URL: https://codeload.github.com/shadowsocksrr/shadowsocksr-libev/tar.gz/2.5.3?/shadowsocksr-libev-2.5.3.tar.gz</br>
File: .cypress-firmware-5.4.18-2021_0812.tar.xz URL: https://sources.cdn.openwrt.org/simple-obfs-0.0.5.tar.xz</br>
File: .cypress-nvram-2019-09-03-e7b78df2.tar.xz URL: https://sources.cdn.openwrt.org/cypress-firmware-5.4.18-2021_0812.tar.xz</br>
File: .linux-firmware-20231211.tar.xz URL: https://sources.openwrt.org/simple-obfs-0.0.5.tar.xz</br>
File: .wireless-regdb-2022.08.12.tar.xz URL: https://mirror2.openwrt.org/sources/simple-obfs-0.0.5.tar.xz</br>
File: .cryptodev-linux-1.13.tar.gz URL: https://raw.githubusercontent.com/raspberrypi/firmware/3673be308132de102fdff491d1333d9d0f823557/boot/LICENCE.broadcom</br>
File: .vsftpd-3.0.5.tar.gz URL: https://raw.githubusercontent.com/raspberrypi/firmware/3673be308132de102fdff491d1333d9d0f823557/boot/fixup4.dat</br>
File: .libcap-2.68.tar.xz URL: https://raw.githubusercontent.com/raspberrypi/firmware/3673be308132de102fdff491d1333d9d0f823557/boot/fixup4x.dat</br>
File: .json-c-0.16-nodoc.tar.gz URL: https://raw.githubusercontent.com/raspberrypi/firmware/3673be308132de102fdff491d1333d9d0f823557/boot/start.elf</br>
File: .libnl-tiny-2022-11-01-db3b2cdb.tar.xz URL: http://www.netfilter.org/projects/libmnl/files/libmnl-1.0.5.tar.bz2</br>
File: .libubox-2022-09-27-ea560134.tar.xz URL: https://sources.cdn.openwrt.org/libnl-tiny-2022-11-01-db3b2cdb.tar.xz</br>
File: .ncurses-6.4.tar.gz URL: https://sources.cdn.openwrt.org/libubox-2022-09-27-ea560134.tar.xz</br>
File: .openssl-3.0.13.tar.gz URL: https://mirrors.aliyun.com/gnu/ncurses/ncurses-6.4.tar.gz</br>
File: .readline-8.2.tar.gz URL: https://downloads.sourceforge.net/pcre/pcre-8.45.tar.bz2</br>
File: .uclient-2021-05-14-6a6011df.tar.xz URL: https://raw.githubusercontent.com/raspberrypi/firmware/3673be308132de102fdff491d1333d9d0f823557/boot/start_cd.elf</br>
File: .ustream-ssl-2022-12-08-9217ab46.tar.xz URL: https://sources.cdn.openwrt.org/uclient-2021-05-14-6a6011df.tar.xz</br>
File: .wolfssl-5.5.4-stable.tar.gz URL: https://sources.cdn.openwrt.org/ustream-ssl-2022-12-08-9217ab46.tar.xz</br>
File: .firewall-2022-02-17-4cd7d4f3.tar.xz URL: https://github.com/wolfSSL/wolfssl/archive/v5.5.4-stable/wolfssl-5.5.4-stable.tar.gz</br>
File: .netifd-2021-06-04-50381d0a.tar.xz URL: https://sources.cdn.openwrt.org/firewall-2022-02-17-4cd7d4f3.tar.xz</br>
File: .dnsmasq-2.88.tar.xz URL: https://sources.cdn.openwrt.org/netifd-2021-06-04-50381d0a.tar.xz</br>
File: .fullconenat-2022-02-13-108a36cb.tar.xz URL: https://raw.githubusercontent.com/raspberrypi/firmware/3673be308132de102fdff491d1333d9d0f823557/boot/start4.elf</br>
File: .hostapd-2022-07-29-b704dc72.tar.xz URL: https://mirror2.openwrt.org/sources/fullconenat-2022-02-13-108a36cb.tar.xz</br>
File: .ppp-2.4.9.git-2021-01-04.tar.xz URL: https://sources.cdn.openwrt.org/hostapd-2022-07-29-b704dc72.tar.xz</br>
File: .backports-6.1.24.tar.xz URL: https://sources.cdn.openwrt.org/ppp-2.4.9.git-2021-01-04.tar.xz</br>
File: .uhttpd-2022-10-31-23977554.tar.xz URL: http://mirror2.openwrt.org/sources/backports-6.1.24.tar.xz</br>
File: .bpftools-2022-03-08-04c465fd.tar.xz URL: https://sources.cdn.openwrt.org/uhttpd-2022-10-31-23977554.tar.xz</br>
File: .iproute2-6.2.0.tar.xz URL: https://sources.cdn.openwrt.org/bpftools-2022-03-08-04c465fd.tar.xz</br>
File: .iw-5.19.tar.xz URL: https://netfilter.org/projects/iptables/files/iptables-1.8.7.tar.bz2</br>
File: .libiwinfo-2023-05-17-c9f5c3f7.tar.xz URL: https://mirror.iscas.ac.cn/kernel.org/software/network/iw/iw-5.19.tar.xz</br>
File: .ca-certificates_20211016.tar.xz URL: https://sources.cdn.openwrt.org/libiwinfo-2023-05-17-c9f5c3f7.tar.xz</br>
File: .fstools-2023-01-22-1ea5855e.tar.xz URL: https://ftp.debian.org/debian/pool/main/c/ca-certificates/ca-certificates_20211016.tar.xz</br>
File: .fwtool-2019-11-12-8f7fe925.tar.xz URL: https://sources.cdn.openwrt.org/fstools-2023-01-22-1ea5855e.tar.xz</br>
File: .openwrt-keyring-2022-03-25-62471e69.tar.xz URL: https://mirror.leaseweb.com/debian/pool/main/c/ca-certificates/ca-certificates_20211016.tar.xz</br>
File: .opkg-2022-02-24-d038e5b6.tar.xz URL: https://mirror.netcologne.de/debian/pool/main/c/ca-certificates/ca-certificates_20211016.tar.xz</br>
File: .procd-2023-01-16-190f13a7.tar.xz URL: https://sources.cdn.openwrt.org/ca-certificates_20211016.tar.xz</br>
File: .rpcd-2023-01-21-c0df2a7a.tar.xz URL: https://sources.cdn.openwrt.org/procd-2023-01-16-190f13a7.tar.xz</br>
File: .ubus-2022-06-01-2bebf93c.tar.xz URL: https://sources.cdn.openwrt.org/rpcd-2023-01-21-c0df2a7a.tar.xz</br>
File: .ubox-2022-08-13-4c7b720b.tar.xz URL: https://sources.cdn.openwrt.org/ubus-2022-06-01-2bebf93c.tar.xz</br>
File: .uci-2021-10-22-f84f49f0.tar.xz URL: https://sources.cdn.openwrt.org/ubox-2022-08-13-4c7b720b.tar.xz</br>
File: .bcm27xx-userland-c4fd1b8986c6d6d4ae5cd51e65a8bbeb495dfa4e.tar.gz URL: https://sources.cdn.openwrt.org/uci-2021-10-22-f84f49f0.tar.xz</br>
File: .usign-2020-05-23-f1f65026.tar.xz URL: </br>
File: .e2fsprogs-1.47.0.tar.xz URL: https://sources.cdn.openwrt.org/usign-2020-05-23-f1f65026.tar.xz</br>
File: .f2fs-tools-1.16.0.tar.gz URL: https://mirror.iscas.ac.cn/kernel.org/linux/kernel/people/tytso/e2fsprogs/v1.47.0/e2fsprogs-1.47.0.tar.xz</br>
File: .jsonfilter-2018-02-04-c7e938d6.tar.xz URL: https://git.kernel.org/pub/scm/linux/kernel/git/jaegeuk/f2fs-tools.git/snapshot/f2fs-tools-1.16.0.tar.gz</br>
File: .lua-5.1.5.tar.gz URL: https://sources.cdn.openwrt.org/jsonfilter-2018-02-04-c7e938d6.tar.xz</br>
File: .ucode-2023-01-09-8dad974b.tar.xz URL: https://www.lua.org/ftp/lua-5.1.5.tar.gz</br>
File: .util-linux-2.38.1.tar.xz URL: https://sources.cdn.openwrt.org/ucode-2023-01-09-8dad974b.tar.xz</br>
</br>
