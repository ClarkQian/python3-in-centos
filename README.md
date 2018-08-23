# python3-in-centos
How to install python3 in centos 7


#1. install package
yum -y groupinstall "Development tools"
yum -y install zlib-devel bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel gdbm-devel db4-devel libpcap-devel xz-devel
 
#2. download python3
wget https://www.python.org/ftp/python/3.6.2/Python-3.6.2.tar.xz
 
#3. make a directory to install python3
mkdir /usr/local/python3 

#4. unzip the python3 zip file and then install python3
tar -xvJf  Python-3.6.2.tar.xz
cd Python-3.6.2
./configure --prefix=/usr/local/python3
make && make install
 
#5. create shortcuts about python3 and pip3
ln -s /usr/local/python3/bin/python3 /usr/bin/python3
ln -s /usr/local/python3/bin/pip3 /usr/bin/pip3
