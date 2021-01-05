
### Configration to run Jenkins file without any conversion issues. 
```bash
export PATH=/QOpenSys/pkgs/bin:/home/GAJENDER/.ssh:$PATH;
export TERM=xterm;
export SHELL=/QOpenSys/usr/bin/bsh;
export SHLVL=1;
cd /var/jenkins;
java -jar jenkins.war --httpPort=6123
````
### Converion issue can be avoided using the following update 

the JV1 version of Java sometimes seems to do some errant ASCII->EBCDIC conversions when it shouldn't. 
For running Jenkins, I'd recommend using the OpenJDK 11 rpm: https://ibmi-oss-docs.readthedocs.io/en/latest/java11/JAVA11_EARLY_ACCESS.html

### in jenkins Console following commands can be used to automate the makefile with spool conversion 

```bash
#!/QOpenSys/usr/bin/qsh

gmake -s >> gmakeOutput.txt;

exitCode="$?";

/usr/bin/iconv -t UTF-8 -f 819 gmakeOutput.txt > converted.txt;

/QOpenSys/usr/bin/sh ;

tail -20000 converted.txt | /usr/bin/iconv -t 37 -f 819;

rm gmakeOutput.txt;
rm converted.txt;

if test $exitCode -gt 0
then
	false
else
	true
fi
````
