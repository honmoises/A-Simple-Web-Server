# A-Simple-Web-Server

## Requirements
- The target machine has to support YUM package management tool (RedHat, CentOS).

## Variable
- This is a role based Playbook, it will install two packages in the target host:
1. httpd
2. python3-mod_wsgi
- These are define as variables in the defaults of the role.
- 
- More packages can be installed since it uses the vars defined by the role.

Once installed it will restart the httpd service and copy a custom index.html
The page uses a custom message (defined in defaults), and should look like this one is completed successfully.


![image](https://user-images.githubusercontent.com/14948712/117051383-b7672800-acd3-11eb-9154-13725a6dd47b.png)


## Author 
Moises M.

Twitter: @Moises_Monge_M

## Date
May 4th, 2021
