# Container Cluster

This is the configuration for the master servers in a kubernetes cluster

## Getting Started

Clone the repository to your home directory and make changes there.  You can push changes from there using the ansible-playbook command, or commit and push you changes back to the git repository and the ansible runner will push changes to the server.


### Prerequisites

To run this script you will need ansible-playbook available on your workstation or home server.  If you don't need to push changes from your working copy, you can just check changes into gitlab and the ansible-runner will push the changes.

To push changes, your ssh key must be on the cluster node server in the /root/.ssh/authorized_keys file.


## Deployment

To deploy to live servers, verify that your ssh key is on the server, then check the host file to make sure it refers to the servers that you expect.

Copy 'hosts.example' to 'hosts' and replace the hostnames


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
