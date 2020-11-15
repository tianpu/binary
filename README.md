# xunsearch 1.4.15
```diff
- ./packages/libevent-2.0.21-stable.tar.bz2 
+ ./packages/libevent-2.1.12-stable.tar.bz2 

./packages/xunsearch-1.4.14.tar.bz2/src/global.h  
L17  
- #define	DEFAULT_BACKLOG		63			// default backlog for listen()   
+ #define	DEFAULT_BACKLOG		1024			// default backlog for listen()   

./packages/xunsearch-1.4.14.tar.bz2/src/import.cc  
L927  
- system(XAPIAN_DIR "/bin/xapian-compact -n " DEFAULT_DB_NAME "_a " DEFAULT_DB_NAME " " DEFAULT_DB_NAME "_c");  
+ system(XAPIAN_DIR "/bin/xapian-compact -b 32K -n " DEFAULT_DB_NAME "_a " DEFAULT_DB_NAME " " DEFAULT_DB_NAME "_c"); 

./packages/xunsearch-1.4.14.tar.bz2/src/xs-optimize.sh.in  
L32  
- bin/xapian-compact $home/$d $home/${d}_tmp 
+ bin/xapian-compact -b 32K $home/$d $home/${d}_tmp 

./setup.sh
L334
- ./configure --prefix=$prefix >> ../setup.log 2>&1
+ ./configure --prefix=$prefix --disable-openssl >> ../setup.log 2>&1
```
freebsd 12.2R passed

# phpmyadmin
```diff
./phpmyadmin/libraries/classes/Header.php 
- x-content-type-options: nosniff 
- x-frame-options: sameorigin 
- x-xss-protection: 1; mode=block 

./phpmyadmin/config.inc.php 
+ custom lines
```
