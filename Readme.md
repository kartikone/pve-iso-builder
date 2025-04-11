## How to use

Please use the Debian system to execute this script ！

#### clean and build

```
apt install debootstrap squashfs-tools  xorriso -y
bash build.sh clean 
```

####  build without clean
```
bash build.sh
```

## install other package

edit build.sh

```
extra_pkg="ceph-common ceph-fuse iperf3 net-sriov-tools your_pkg"  #if you want install other package
```

add ceph

edit .cd-info

```
RELEASE='8.3'
ISORELEASE='3'
ISONAME='pxvirt'
PRODUCT='pxvirt'
PRODUCTLONG='pxvirt'
main_kernel="pve-kernel-6.6-openeuler"
extra_kernel=""
mirrors="https://mirrors.ustc.edu.cn" #debian mirror
pvemirrors="https://mirrors.ustc.edu.cn/proxmox/debian" #pve mirrors.
portmirrors="https://download.lierfang.com/pxcloud" #port mirrors
ceph="reef" # [  cephversion reef| squid | quincy ] see https://docs.pxvirt.lierfang.com/zh/repo.html
```
