<h1 align="center">Nginx cheat sheet</h1>

<a href="https://github.com/MatthijsReyers/cheat-sheets">All cheatsheets</a> - 
<a href="https://docs.nginx.com/">Nginx documentation</a>

<br>

## Table of contents

1. <a href="https://github.com/MatthijsReyers/cheat-sheets/blob/main/GDB.md#general-tips--tricks">General tips & tricks</a>
2. <a href="https://github.com/MatthijsReyers/cheat-sheets/blob/main/GDB.md#basic-example-commands">Hardening security</a>

<br>

## 1. Basic setup

### 
```
stuff here
```

<br>

## 2. Hardening security

### Disable leaking of OS and Nginx version.
By the default Nginx will send the nginx version and operating system in the `Server` HTTP header, by adding this line to the `http` directive 
in the main `/etc/nginx/nginx.conf` config file it will now only leak that the server is running on nginx (which could be derived from many other
things anyway):
```
server_tokens off;
```
