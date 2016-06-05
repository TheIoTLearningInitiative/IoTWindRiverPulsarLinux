# NodeJS

```sh
root@cube-31-10-15-domE:~# smart install nodejs
Loading cache...
Updating cache...               ######################################## [100%]

Computing transaction...

Installing packages (2):
  nodejs-0.10.35-r0.0@core2_64           nodejs-npm-0.10.35-r0.0@core2_64       

4.0MB of package files are needed. 11.5MB will be used.

Confirm changes? (Y/n): Y
Fetching packages...                                                           
-> https://distro.windriver.com/.../nodejs-0.10.35-r0.0.core2_64.rpm           
-> https://distro.windriver.com/.../nodejs-npm-0.10.35-r0.0.core2_64.rpm       
nodejs-npm-0.10.35-r0.0.core2.. ######################################## [ 50%]
nodejs-0.10.35-r0.0.core2_64... ######################################## [100%]

                                                                               
Committing transaction...
Preparing...                    ######################################## [  0%]
   1:Installing nodejs-npm      ######################################## [ 50%]
   2:Installing nodejs          ######################################## [100%]

Saving cache...

root@cube-31-10-15-domE:~# 
```

```sh
root@cube-31-10-15-domE:~# node -v
v0.10.35
root@cube-31-10-15-domE:~# 
```

```sh
root@cube-31-10-15-domE:~# npm cache clean -f
npm WARN using --force I sure hope you know what you are doing.
root@cube-31-10-15-domE:~# npm install -g n
/usr/bin/n -> /usr/lib/node_modules/n/bin/n
n@2.1.0 /usr/lib/node_modules/n
root@cube-31-10-15-domE:~# n stable

     install : node-v6.2.1
       mkdir : /usr/local/n/versions/node/6.2.1
       fetch : https://nodejs.org/dist/v6.2.1/node-v6.2.1-linux-x64.tar.gz
######################################################################## 100.0%
   installed : v6.2.1

root@cube-31-10-15-domE:~# 
```

```sh
root@cube-31-10-15-domE:~# node
> 
```

```sh

```

```sh

```

```sh

```

```sh

```

```sh

```
