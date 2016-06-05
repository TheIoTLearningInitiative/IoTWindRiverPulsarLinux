# Labs

```sh
root@cube-31-10-15-domE:~# git clone https://github.com/xe1gyq/TheIoTLearningInitiative.git
Cloning into 'TheIoTLearningInitiative'...
fatal: unable to access 'https://github.com/xe1gyq/TheIoTLearningInitiative.git/': server certificate verification failed. CAfile: /etc/ssl/certs/ca-certificates.crt CRLfile: none
root@cube-31-10-15-domE:~# 
```

```sh
root@cube-31-10-15-domE:~# git config --global http.sslverify false
root@cube-31-10-15-domE:~# git clone https://github.com/xe1gyq/TheIoTLearningInitiative.git
Cloning into 'TheIoTLearningInitiative'...
remote: Counting objects: 63, done.
remote: Compressing objects: 100% (16/16), done.
remote: Total 63 (delta 9), reused 0 (delta 0), pack-reused 43
Unpacking objects: 100% (63/63), done.
Checking connectivity... done.
root@cube-31-10-15-domE:~# 
```

```sh
root@cube-31-10-15-domE:~# cd TheIoTLearningInitiative/
root@cube-31-10-15-domE:~/TheIoTLearningInitiative# git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/embeddedlinux
  remotes/origin/master
  remotes/origin/windriver
root@cube-31-10-15-domE:~/TheIoTLearningInitiative# 
```

```sh
```

```sh
```

```sh
```

```sh
```



