# Local Python DNS Server

A Dockerized simple local DNS server implemented in Python.

## Host requirement(s)
- **Docker**: [[Installation Guide](https://docs.docker.com/engine/install/)]
- **Docker Compose**: [[Installation Guide](https://docs.docker.com/compose/install/)]

## Configuration
The domain-to-IP mappings are defined in the dns_server.py file. Update the DOMAIN_TO_IP dictionary with your desired mappings:
```
# DNS server configuration
DOMAIN_TO_IP = {
    'a.com.': '192.168.1.100',
    'b.com.': '192.168.1.101',
}
```

## Usage
1.  Clone this repository and navigate to project folder
```
git clone https://github.com/NotYuSheng/Local-Python-DNS-Server.git
cd Local-Python-DNS-Server
```

2.  Build the Docker images:
```
docker-compose build
```

3.  Run images
```
docker-compose up
```

## Acknowledgements
- [Hackernoon - How to Set Up a Local DNS Server With Python](https://hackernoon.com/how-to-set-up-a-local-dns-server-with-python)
