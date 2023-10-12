Docker Environment for WordPress with Apache
===

Run WordPress through Apache effortlessly.
Local domain is ***wp.local***

### Install
- Download zip or clone repo. Place files on the host.
- Run following.

```bash
$ chmod u+x .config/docker-entrypoint.sh

# run services
$ docker-compose up -d
```

### SSL Certificates
Create certificate before run services.

```bash
# Generate SSL certificates with mkcert (.pem files)
$ chmod u+x .config/create-certs.sh
$ sh .config/create-certs.sh

# Then run this command to create a certificate file
$ openssl x509 -outform der -in .config/certs/cert.pem -out .config/certs/cert.crt
```

After certificate creation install it to Trusted Root Certification Authorities.


**Don't forget add wp.local to your hosts file.** 

That's it.

### Author
Levon Midoyan - [@levonmidoyan](https://github.com/levonmidoyan)

### License
MIT
