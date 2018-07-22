---
# Background
Company would like to manage the blog easier and everything automated. Infrastructure as a code is one part that must be done first on adopting DevOps works. And it requires knowledges to implement all things to automated and centralised.
The company is looking for a DevOps Engineer. And prepare a test for a new DevOps Engineer candidate.

So, Here I go. I'm asked to create a deployment script to manage the blog deployment.

# Requirements

- Python

  python >= 2.6

- Ansible

  Required ansible, can be installed from pip

  ```$ sudo pip install ansible```

- Python Modules

  - dopy

  ```sudo pip install dopy```


# How to Launch a Droplet

```ansible-playbook -i inventory.ini launch_droplet.yml --extra-vars="droplet_name=blog droplet_size=1gb digitalocean_token=$YOUR_TOKEN_API" --tag launch_droplet```

# How to Setup Droplet

```ansible-playbook -i inventory.ini blog.yml```

# How to Deploy Docker Compose

```Env=staging/production```

```ansible-playbook -i inventory.ini blog.yml --tag deploy-compose --extra-vars="docker_compose=blog env=$env"```

- I'm Ready...
