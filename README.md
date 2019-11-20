# xunsearch-full-1.4.14-openssl111.tar.bz2 
```diff
- ./packages/libevent-2.0.21-stable.tar.bz2 
+ ./packages/libevent-2.1.11-stable.tar.bz2 

./packages/xunsearch-1.4.14.tar.bz2/configure  
L5390  
- #if _EVENT_NUMERIC_VERSION >= 0x02000000  
+ #if EVENT__NUMERIC_VERSION >= 0x02000000  

./setup.sh
L334
- ./configure --prefix=$prefix >> ../setup.log 2>&1
+ ./configure --prefix=$prefix --disable-openssl >> ../setup.log 2>&1
```
freebsd 12.1 passed
