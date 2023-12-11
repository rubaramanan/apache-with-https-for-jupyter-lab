# apache-with-https-for-jupyter-lab

### Requirements

* Docker
* Docker compose

### Steps

1. Clone Repo

```bash
git clone https://github.com/rubaramanan/apache-with-https-for-jupyter-lab.git

cd apache-with-https-for-jupyter-lab
```

2. Generate key file
```bash
openssl genrsa 2048 > server.key

openssl req -new -x509 -nodes -sha256 -days 365 -key server.key -out server.crt
```

3. Start the service
```bash
docker-compose up -d
```