	Installation Mysql,apache2,PHP

1-MySQL:
~$ sudo su      

~# cd /usr/local/etc

Telechargement d’un code source mysql

Etap 1:Decompression et desarchivage:

~/cd/usr/local/src # bunzip2 /home/user/mysql-8.0.36

~/cd/usr/local/src # tar -xvf /home/user/mysql-8.0.36

~/cd/usr/local/src # cd mysql-8.0.36

Etape 2:Installation :dependance boost-1-77-0

Telechargement d’un code source boost
	
 	Decompression et desarchivage:

~/cd/usr/local/src/ #bunzip2 /home/user/boost-1-77-0.tar.bz2

~/cd/usr/local/src/mysql-8.0.36 $ tar -xvf /home/user/boost-1-77-0 .tar

~/cd/usr/local/src/mysql-8.0.36 # cd boost-1-77-0

~/cd/usr/local/src/mysql-8.0.36 /boost-1-77-0#ls -a

~/cd/usr/local/src/mysql-8.0.36/boost-1-77-0# README

~/cd/usr/local/src/mysql-8.0.36/boost-1-77-0# ./bootstrap.sh

~/cd/usr/local/src/mysql-8.0.36# ./b2

~/cd/usr/local/src/ mysql-8.0.36 # ./b2 install

Etape 3:installation mysql 

~/cd/usr/local/src/mysql-8.0.36/ boost-1-77-0 #mkdir build

~/cd/usr/local/src/mysql-8.0.36/boost-1-77-0# cd build

~/cd/usr/local/src/mysql-8.0.36/boost-1-77-0/build# cmake
  
   no error

~/cd/usr/local/src/ mysql-8.0.36/boost-1-77-0/build# make

~/cd/usr/local/src/mysql-8.0.36/boost-1-77-0/build# make install

verification : mysql --version 



	2-Apache2:

~$ sudo su      

~# cd /usr/local/src
	
 	Decompression et desarchivage:

~/cd/usr/local/src # bunzip2 /home/mit/httpd_version.tar.bz2

~/cd/usr/local/src # tar -xvf /home/mit/httpd_version.tar

Etape1:Installation des dependances :

apr:
	Decompression et desarchivage :

~/cd/usr/local/src #cd httpd_version

~/cd/usr/local/src/httpd #gunzip2 /home/mit/apr_version.tar.gz

~/cd/usr/local/src/httpd # tar -xvf /home/mit/apr_version.tar

~/cd/usr/local/src/httpd #cd apr_version

~/cd/usr/local/src/httpd/apr_version #./configure

~/cd/usr/local/src/httpd/apr_version r#make

~/cd/usr/local/src/httpd/apr_version# make install

~/cd/usr/local/src/httpd/apr_version #cd ..

apr-util:

 	Decompression et desarchivage;

~/cd/usr/local/src/httpd #cd apr-util_version

~/cd/usr/local/src/httpd/apr-util_version# ./configure
	
 	Eroor : ./configure not found
~/cd/usr/local/src/httpd/apr-util_version# ./configure –with-apr=/usr/local/apr/bin/apr-1-config

~/cd/usr/local/src/httpd/apr-util_version #make && make install
	
 prce :
	Decompression et desarchivage;
~/cd/usr/local/src/httpd#cd prce_version

~/cd/usr/local/src/httpd/cd prce_version# ./configure

       fatal-error:expart.h:no such file

~/cd/usr/local/src/httpd/cd prce_version#apt install libexpat1.dev

~/cd/usr/local/src/httpd/cd prce_version# ./configure

~/cd/usr/local/src/httpd/cd prce_version# make && make install

 Etape 2: Installation apache2

~/cd/usr/local/src/httpd_version$#./configure –prefix=/usr/local/apache2 –with-prce=/usr/local/bin –enable-so
~/cd/usr/local/src/httpd_version# make && make install
verification: apache2 -v

	3-PHP:

~$sudo su

~# php_source

~#cd php_source
	telechargement d’un code source php

 Etape 1:
~/php_source#gunzip /home/mit/php-8.3.6.tar.zip

~/php_source#tar -xvf /home/mit/php-8.3.6.tar

~/php_source# cd php-8.3.6

~/php_sources/php-8.3.6#more README.md

 	
  	Etape 2: installation php en suivant les instructions données par README.md

~/php_sources/php-8.3.6# apt install -y pkg-conf build-essential autoconf bison re2c \ libxm12-dev libsqlete3-dev

~/php_sources/php-8.3.6# ./buildconf

~/php_sources/php-8.3.6# ./configure

~/php_sources/php-8.3.6#  make 

sans erreur

~/php_sources/php-8.3.6#  make installer

verification:php --version


