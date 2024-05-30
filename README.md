# ansible


## pre process
```
sudo apt-get update
sudo apt install -y openssh-server
sudo sed -i 's/#Port 22/Port 2222/' /etc/ssh/sshd_config
sudo service ssh start

hostname -I
```

## ansible client
```
sudo apt-get update
sudo apt-get install ansible

sudo apt-get update
sudo apt install sshpass

ansible-playbook -i inventory playbook.yaml
```

## post process
```
sudo service ssh stop
sudo apt purge openssh-server
sudo sed -i 's/Port 2222/#Port 22/' /etc/ssh/sshd_config
```