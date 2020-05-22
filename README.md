# OSSonIBMi
Getting started with open source in IBMi 

1. Login to your IBMi 
2. Run sql script from [bootstrap.sql](./bootstrap.sql)
3. Add path permanently to user profile. 
  - `CALL QP2TERM `
  - `echo 'PATH=/QOpenSys/pkgs/bin:$PATH' >> $HOME/.profile && echo 'export PATH' >> $HOME/.profile`
4. Restart your session.
5. `CALL QP2TERM` 
6. Run ` yum --version `. Boom yum is intalled.
7. yum is the package manager for rpm. 
8. `yum group install "Development tools"`

> Reference link : https://bitbucket.org/ibmi/opensource/src/master/docs/yum/