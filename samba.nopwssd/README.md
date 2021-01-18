# Convert an existing Samba server to Docker

This Docker Compose configuration can be used to convert an existing
Samba server over to Docker with little effort. Just edit the
`docker-compose.yml` file to add your shares, set the timezone
`TZ` variable if desired, then bring the server up:

    docker-compose up -d --build

This assumes you have a working Samba installation, with configuration
in `/etc/samba` and library files in `/var/lib/samba`. If the paths
on the host machine are different, just edit them in the Compose file.

Based on/inspired by [dperson/samba](https://github.com/dperson/samba),
but modified to work with/convert existing (bare metal) installations
of Samba.

## Blog post

Please see my [blog post](https://alexlubbock.com/convert-samba-docker)
for the background behind this implementation, the pros and cons
compared to the [dperson/samba](https://github.com/dperson/samba)
version, and further notes on configuration.
