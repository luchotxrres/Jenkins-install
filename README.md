# Jenkins install Linux Deb/Ubuntu
Getting Started Jenkins

# Download Jenkins

`wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -`

`sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'`

`sudo apt-get update`

`sudo apt-get install jenkins`

# Start Jenkins

`sudo /etc/init.d/jenkins start|stop|restart`

[Browse to Localhost](http://localhost:8080)

# Unlock Jenkins

**Administration Password**

Copy `sudo cat /var/lib/jenkins/secrets/initialAdminPassword`

# Commons Failures

#### If your `/etc/init.d/jenkins` file fails to start Jenkins
##### Edit the `/etc/default/jenkins` to replace the line `----HTTP_PORT=8080----` with `----HTTP_PORT=8081----`
Here, "8081" was chosen but you can put another port available.
