# ansible


## target preprocess
```
sudo apt-get update
sudo apt install -y openssh-server

sudo service ssh start

hostname -I
```

## ansible client
```
docker compose up -d
```

## target postprocess
```
sudo service ssh stop
sudo apt purge openssh-server
```