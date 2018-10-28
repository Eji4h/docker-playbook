# docker-playbook
Ansible playbook for install docker and docker-compose all of host in you control.

## Notation
Make sure [Ansible](http://docs.ansible.com/ansible/latest/intro_installation.html) is already installed.

## Create user

```console
$ ansible-playbook docker-playbook.yml
```
This command wll show promt ask docker edition, channel, version, users to docker group and docker-compose version. <br />

_**`users to docker group need use [ ] cover, if you have more than one user to add in docker group.`**_ <br />
Sample:
```console
What is user to add to docker group []: [ "user1", "user2" ]
```
<br />

Options: <br />
-k, --ask-pass
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
ask for connection password (if you don't login with ssh-key). <br />
-K, --ask-become-pass
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
ask for privilege escalation password (if you' don't login with root). <br />
--limit=HOST
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
select host to install docker and docker-compose. <br />
--become-user=BECOME_USER
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
run operations as this user (default=root). <br />

Sample:
```console
$ ansible-playbook docker-playbook.yml -K
```
