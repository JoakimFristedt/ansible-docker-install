# Install docker with ansible and create swarm

## What does it do?

1. Installs python (For ansible to work)
2. Updates aptitude
3. Installs docker
4. Creates swarm
5. Adds managers & workers to swarm

## Setup ssh keys

```
cat ~/.ssh/id_rsa.pub | ssh root@<server-host-here> "cat >> ~/.ssh/authorized_keys"
```

## Add hosts

Add hosts to `hosts/targets`

## Run install docker playbook

```
ansible-playbook -i hosts/targets -u <root-user-here> docker.yml
```

## Run swarm playbook

```
ansible-playbook -i hosts/targets -u <root-user-here> swarm.yml
```
