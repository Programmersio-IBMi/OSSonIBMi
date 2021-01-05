  1. `/QOpenSys/pkgs/bin/bash`
  2. Connect to system using SSH
  3. Run command: `export PATH=/QOpenSys/pkgs/bin:$PATH`
  4. Create a directory to hold your git repos
  5. Setup git to use ssh key
  6. Add the SSH key to the SSH agent:  `eval $(ssh-agent -s)`
	  1. Add RSA key to SHH with: `ssh-add ~/.ssh/id_rsa`
  7. Clone the repo to your directory
  8. Run gmake
  9. https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
