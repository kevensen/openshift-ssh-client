# SSH Client for OpenShift

## Usage
First you must create a secret in your project
```bash
$ oc secrets new ssh-secret ssh-privatekey=${HOME}/.ssh/id_rsa
```

