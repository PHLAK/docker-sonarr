docker-sonarr
==============

Docker image for Sonarr client.

[![](https://images.microbadger.com/badges/image/phlak/sonarr.svg)](http://microbadger.com/#/images/phlak/sonarr "Get your own image badge on microbadger.com")

Running the Container
---------------------

In order to persist configuration data when upgrading your container you should create a named data
volume. This is not required but is _highly_ recommended.

    docker volume create --name sonarr-data

After the data volume has been created run the daemon container with the named data volume:

    docker run -d -p 8989:8989 -v sonarr-data:/home/sonarr/.config/NzbDrone -v /path/to/shows:/srv/shows --name sonarr-client phlak/sonarr

#### Optional 'docker run' Arguments

`--restart always` - Always restart the container regardless of the exit status. See the Docker
                     [restart policies](https://goo.gl/OI87rA) for additional details.

Troubleshooting
---------------

Please report bugs to the [GitHub Issue Tracker](https://github.com/PHLAK/docker-sonarr/issues).

Copyright
---------

This project is liscensed under the [MIT License](https://github.com/PHLAK/docker-sonarr/blob/master/LICENSE).
