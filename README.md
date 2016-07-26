Project: Linux Server Configuration  - [Shyamala Prakash]
================================
1. Public IP Address 52.42.85.100
2. The ssh port is 2200
   ssh -i ~/.ssh/udacity_key.rsa root@52.42.85.100 -p 2200
3. URL for the hosted service:
    http://ec2-52-42-85-100.us-west-2.compute.amazonaws.com/
    
4. Software Installed and shell commands used:
   Installed the firewall ufw:
     ufw default deny incoming
     ufw default allow outgoing
     ufw allow ssh
     ufw allow 2200/tcp
     ufw allow www
     ufw allow ntp
     ufw enable
     
    edit /etc/ssh/sshd_config to listen on Port 2200
     
     
   Update Intalled packages: 
    apt-get update
    
    apt-get install python-pip
    
    pip install -U psycopg2
    
    pip install Flask
    
    pip install sqlalchemy
    
    apt-get install python-setuptools
    
    apt-get install git
    
    apt-get install postgresql postgresql-contrib
    
    apt-get install apache
    
    dpkg --connfigure -a
    
    apt-get install libapache2-mod-wsgi
    
    
    git config --global user.name "shyamala98"
    
    Edit /etc/postgresql/9.3/main/pg_hbs.conf
    
    userid used by the catalog application to connect to postgres is
    catalogdb, password:catalogdb
    Files:
    /var/www/html/catalog/catalog.wsgi
    
    edit the WSGI config file in:
    /etc/apache2/sites-available/000-default.conf
    
    Summary of the Resources: 
    I used several websites and stackoverflow responses to get the project done
    Here are a few:
    https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps
    https://www.digitalocean.com/community/tutorials/how-to-set-up-apache-virtual-hosts-on-ubuntu-14-04-lts
    http://themanbehindthecode.com/2012/01/10/adding-and-removing-available-apache-sites-in-ubuntu/
    Links provided in the forms were also very useful

5. grader_key.rsa
-----BEGIN RSA PRIVATE KEY-----
MIIEpAIBAAKCAQEAp8SCMR7HTO87v+o0eFV+sWDxKRR59XrXFnabM7ULT5UVkwsv
89yj1wFmBtMnmNqpUBk6swZtg+/2CrX1c7EPVw3jf/fnNw0d4al0OFFiWi4kjjkg
g+a6L16wz73EVzWc+S/j+MKs7YeXJewTzNaiFQVfiSL/C0IZlED+knHzzNYJ9KDo
+r9HhXkPEgipj6xuMtFgcYowJuz7ckn+hoyWO3kbG1TRruWGmEaFTj+x4K/ut0RN
6ewWDLNGRnWifgXiiQAin8rYX/HjL/KECXuUnAzz3LqbrsRF1fhZZ4qykWl7lIyM
xHF7Nqro2YjTp7AMp8E/oDOUq+r2U1+EOKpzXwIDAQABAoIBAQCEJjdDR/JHeL6A
6pQQIZAdWrY73KRAqFVanWyda0OQmWeYHxzTo33vM2vRfmxXbA4oSOdC85I6dj9B
qpjAW70wnoEQYQ7g/1UFVzxzzC+Dx4sF+JvTKmCIRbdSvDE3XMTcSEvzvC0JIV//
ABmMpZigpE3fsRBjJtsNO7ELW/Vl6ABLT+AdpgvQjgjQQhUZG1FQP19BwEP65wpp
ynkdtnrVwSGk6zU66XO9yOY7zFsvb4ebzmU664YkZJRbL/VsM+Mr9ozPV1JidZ03
7xtviUS545yTmaA3j0cg1lxC2vgEIpZcZzdT23zHiFZUOwCDHP6hQCLrZYn+uSem
13St4GuZAoGBAN3Sft2oe+N3Hw9QjJv39SxdnoIDXNZaXHslkbVJObv6lT6XBvrQ
xFMLThjwzn6RKUaP8nPLMuoFc5vQMsA22qayyQkubFCLEV9vhF6d9ZbTgX+u+C+R
p54/YCyD/PYLbEY2SEjAjkNBiGxv3qMbsdkZ3SS4TDqOfkE3MRCms3ejAoGBAMGd
5Qf58nPEq8lYCAUbV2CPpRj9rxXVsaVQkZJHuYgQ+eHpeBCSA97UVSbwqbavsWN6
siVzeXAvhbkr7cYlBkCc8dzPMEEY1yxmjl+BxCBubDCWC/7SG+6ivdvIaq09OOXZ
qMqgsCRy2bpQQg+q/AF8lxNdkb4JwF1LrG2VPgEVAoGBAJEHzHzeaMnrG3qm3pgn
QbyVJUq6KhvYDrlRcfgGfWIDT0sR8bVRg9sL/C7gWxJzlHoXKZ090PcjQ1gvgs8b
zk/JexmuqZDrrBsqzXATdPv9I6E44/ouEFqt8xKH5X91LoClgxNWGm2sziaf6f/Y
3qokd+tHOEfc3H2FOWY6qAJjAoGAbtG4EJuweTC9fq3jUUD3/y3YunghKac5WbzG
xWpGOCo3TGX8McfRbU4tOu+OxCDFsIG+y47PmDWrHXSWUM5KSNtL2C3Cmc/lAOXm
YaX9ou5xAFIxpXWPRURi1RRecq/TDERLx0a36vTNyEU9uogMW7F7KztoOtSMBRpW
JBbC+Y0CgYBXImNZo0cIURLjMffc4GQPMwygcUOmltyEKg+WPM0WLJ2R1wxU+E+9
WAb7SeOdORaBg8mWVDebfTrJwWzGRy9HhkBG8bRqfOIU6l6fxhYcoGUimragwSEI
rfsrNJwxmIXfv2LLbdpXrj3kFKWQX0kkNalgfgRiqhBikuIUQXtouQ==
-----END RSA PRIVATE KEY-----



    