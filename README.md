# "Hello, World!" via HTTP

Deploy a "Hello, World!" using a small HTTP server.

## How to use this Makejail

Using [appjail-director](https://github.com/DtxdF/director):

```sh
git clone https://github.com/DtxdF/hello-http-makejail.git
cd ./hello-http-makejail
appjail-director up
```

Using the Makejail:

```sh
appjail makejail \
    -j hello-http \
    -f gh+DtxdF/hello-http-makejail \
    -o virtualnet=":<random> default" \
    -o nat
```

Output:

```console
$ fetch -qo - http://hello-http
Hello, world!
UUID: d29dfd75-7d48-4b3b-a1b9-771b6317c373
```
