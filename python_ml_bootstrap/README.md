ansible-ipython-bootstrap
====

## Usage

### SSH setting

```
$ vim ~/.ssh/config
```

```text:~/.ssh/config
Host ec2_bootstrap
  HostName ec2-XXX-XXX-XXX-XXX.ap-northeast-1.compute.amazonaws.com
  User ubuntu
  IdentityFile ~/.ssh/hoge.pem
```

### Run playbook

```
$ ansible-playbook tasks/main.yml
```

### Run ipython notebook server

1. ssh to ec2
2. apply virtualenv venv
3. run server

```
$ ssh ec2_bootstrap

ubuntu@ip-xxx-xxx-xxx-xxx:~$ . venv/bin/activate
(venv)ubuntu@ip-xxx-xxx-xxx-xxx:~$ ipython notebook --profile=nbserver
```

Open browser and access `http://ec2-XXX-XXX-XXX-XXX.ap-northeast-1.compute.amazonaws.com:8888/` .


```
$ ipython notebook --profile=nbserver
```

## References

* http://supportex.net/blog/2014/10/ansible-installing-pyenv-centos/
* http://qiita.com/FGtatsuro/items/2366c93131c47aef8dfe
