## Notice

*when using aws ec2, scipy needs spec of instance type over the t2.small*

## Usage

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
ansible-playbook playbook.yml
```

## References

* http://supportex.net/blog/2014/10/ansible-installing-pyenv-centos/
* http://qiita.com/FGtatsuro/items/2366c93131c47aef8dfe