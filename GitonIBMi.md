## Steps to setup SSH key for git clone

1.`ssh -V`
2.`ssh-keygen -t rsa -b 2048 -C "email@example.com"`
3. When prompted for passphrase give a password to use RSA key in future ***Do not forget this passphrase ***
4. Copy key from "/home/user/.ssh/id_rsa.pub into your hosting service provider settings.
5. Start SSH agent `eval $(ssh-agent -s)`
6. Add SSh key to SSH agent `ssh-add ~/.ssh/id_rsa`.
7. Add github/gitlab to known host `ssh-keyscan github.com >> ~/.ssh/known_hosts`.
