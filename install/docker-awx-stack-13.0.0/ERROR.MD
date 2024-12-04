# ERROR WHEN INSTALLER

### fatal: [127.0.0.1]: FAILED! => {"changed": false, "msg": "Configuration error - kwargs_from_env() got an unexpected keyword argument 'ssl_version'"} 

```
 There is a bug in the latest Docker version (7.0) causing this. The workaround is using a slightly older version of Docker in the Python pip environment when installing Ansible AWX:
```

```
pip uninstall docker
pip install docker==6.1.3
```


### Encountering "Error while fetching server API version: Not supported URL scheme http+docker

```
change version request: from 2.32.2 => 2.30.0 
    pip list
    pip install requests==2.30.0
```

### All PACKAGE INSTALL

```
pip3 install docker==6.13
pip3 install docker-compose==1.29.2
```

- pip3 --version

```
pip 22.0.2 from /usr/lib/python3/dist-packages/pip (python 3.10)
```

- pip3 show docker
```
Name: docker
Version: 6.1.3
Summary: A Python library for the Docker Engine API.
Home-page: https://github.com/docker/docker-py
Author:
Author-email:
License: Apache License 2.0
Location: /usr/local/lib/python3.10/dist-packages
Requires: packaging, requests, urllib3, websocket-client
Required-by: docker-compose
```

- pip3 show docker-compose

```
Name: docker-compose
Version: 1.29.2
Summary: Multi-container orchestration for Docker
Home-page: https://www.docker.com/
Author: Docker, Inc.
Author-email:
License: Apache License 2.0
Location: /usr/local/lib/python3.10/dist-packages
Requires: distro, docker, dockerpty, docopt, jsonschema, python-dotenv, PyYAML, requests, texttable, websocket-client
Required-by:
```

- docker --version
```
Docker version 24.0.5, build ced0996
```
- docker-compose --version
```
Docker Compose version v2.29.6
```