
####  WORK INSTALL Daemon20

check version

```bash
See This Version 
strings /lib/x86_64-linux-gnu/libm.so.6 | grep GLIBC_
GLIBC_2.2.5
GLIBC_2.4
GLIBC_2.15
GLIBC_2.18
GLIBC_2.23
GLIBC_2.24
GLIBC_2.25
GLIBC_2.26
GLIBC_2.27
GLIBC_PRIVATE


cd /usr/local
wget http://ftp.gnu.org/gnu/glibc/glibc-2.29.tar.gz

sudo su

tar -zxvf glibc-2.29.tar.gz
cd glibc-2.29
mkdir build
cd build/
../configure --prefix=/usr/local --disable-sanity-checks

make -j4
make install

```
After 

```bash
cd /lib/x86_64-linux-gnu
ll

cp /usr/local/lib/libm-2.29.so /lib/x86_64-linux-gnu/

ln -sf libm-2.29.so libm.so.6

strings /lib/x86_64-linux-gnu/libm.so.6 | grep GLIBC_

Go to RUN D20

DONE !

```



