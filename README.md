# influxdb-plex

A python script for sending plex stats to influxdb

Forked from https://github.com/rickatnight11/collectd-plex

All I have done is strip out the collectd code and enable writing to influxdb

## Requirements

* Plex.tv authentication token (see included `get_auth_token.py` script)
* Plex Media Server
* influxdb

## Configuration

**Required:**

* `Host` - Plex server hostname
* `Port` - Plex server port
* `AuthToken` - Plex.tv authentication token

**Optional:**
* `HTTPS` - use HTTPS instead of HTTP (defaults to `True`)
* `Sessions` - collect active session count (defaults to `True`)
* `Movies` - collect movie counts (defaults to `True`)
* `Shows` - collect show counts (defaults to `True`)
* `Episodes` - collect episode counts (defaults to `True`)
* `Include` - sections to collect media counts for (assumes all, if excluded)
* `Exclude` - sections to ignore media counts for (assumes all, if excluded)

## Usage

python path/to/script/plex.py Host Port Authtoken

python path/to/script/plex.py -h for more info

