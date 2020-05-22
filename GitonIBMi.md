## Steps to setup SSH key for git clone


1. `ssh -V`
1. `ssh-keygen -t rsa -b 2048 -C "email@example.com"`
1. When prompted for passphrase give a password to use RSA key in future ***Do not forget this passphrase ***
1. Copy key from "/home/user/.ssh/id_rsa.pub into your hosting service provider settings.
1. Start SSH agent `eval $(ssh-agent -s)`
1. Add SSh key to SSH agent `ssh-add ~/.ssh/id_rsa`.
1. Add github/gitlab to known host `ssh-keyscan github.com >> ~/.ssh/known_hosts`.
