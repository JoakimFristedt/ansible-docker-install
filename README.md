# Install docker with ansible

## What does it do?

1. Installs python (For ansible to work)
2. Updates aptitude
3. Installs docker

## Setup ssh keys

```
cat ~/.ssh/id_rsa.pub | ssh root@<server-host-here> "cat >> ~/.ssh/authorized_keys"
```

## Add hosts

Add hosts to `hosts/targets`

## Run playbook

```
ansible-playbook -i hosts/targets -u <root-user-here> docker.yml
```
