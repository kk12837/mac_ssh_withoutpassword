# mac_ssh_withoutpassword
steps to disable mac ssh password auth


cd ~/.ssh/

ssh-keygen -t rsa -P '' -f ~/.ssh/id_rsa

cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys

chmod go-w ~/

chmod 700 ~/.ssh

chmod 600 ~/.ssh/authorized_keys

sudo launchctl stop com.openssh.sshd

sudo launchctl start com.openssh.sshd
