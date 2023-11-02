# powerdns-arm
A custom Dockerfile for the authoritative and recursor image running on arm.

1. Clone the powerdns git repository:
```bash
git clone https://github.com/PowerDNS/pdns.git
```

2. Move to `pdns/builder` and clone the powerdns builder helper repository
```bash
cd pdns/builder
git clone https://github.com/PowerDNS/pdns-builder.git
```

3. Move the content of the powerdns builder helper repository in current builder dir
```bash
mv pdns-builder/* .
```

4. Overwrite the content of `pdns/builder-support/helpers/install_rust.sh` with the content of the provided `install_rust.sh`

5. Overwrite the `Dockerfile-{auth, recursor}` files found in the pdns root folder with the one provided in this repository

Now you can either build OR directly run the image using the provided `docker-compose.yaml` file
Build it directly on an ARM plateform such as raspberrypi
