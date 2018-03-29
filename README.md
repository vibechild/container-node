# Container Cluster Node Prep

This ansible script does all of the prep work to get a node ready for use in a kubernetes cluster

## Getting Started

Clone the repository to your home directory and make changes there.  You can push changes from there using the ansible-playbook command.


### Prerequisites

To run this script you will need ansible-playbook available on your workstation or home server. 

To push changes, your ssh key must be on the cluster node server in the /root/.ssh/authorized_keys file.


## Deployment

Copy 'hosts.example' to 'hosts' and replace the hostnames

To deploy to live servers, verify that your ssh key is on the server, then check the host file to make sure it refers to the servers that you expect.


```
ansible-playbook deploy.yml -i hosts --check
```

Will test your access and the status of the server

```
ansible-playbook deploy.yml -i hosts
```

Will actually make the changes to the server.


## Contributing

Request developer access to this repository and submit a merge request.

## Versioning

There is currently only a master branch, because there are only one type of servers.

## Authors

* **Devin** - *Initial work* - [Private Repo](https://version-control.service.vibechild.net/devin) [Public Repo](https://github.com/vibechild)
