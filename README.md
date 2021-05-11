# A-Simple-Web-Server

## Requirements
- The target machine has to support YUM package management tool (RedHat, CentOS).

## Variable

- This is a role based Playbook, it will install two packages in the target host:
1. httpd
2. python3-mod_wsgi

- These are define as variables under "vars" in the role "a-simple-web-server".
- More packages can be installed since it uses the vars defined by the role.

## How to Execute
- ansible-playbook main.yml -K
- -K is option, required for the elevation of the user privileges.

## Output

[ansible@ansible-lab A-Simple-Web-Server]$ ansible-playbook main.yml -K
BECOME password:

PLAY [This is my role-based playbook] **********************************************************

TASK [Gathering Facts] *************************************************************************
ok: [lab1]

TASK [a-simple-webserver : install httpd packages] *********************************************
ok: [lab1] => (item=httpd)
ok: [lab1] => (item=python3-mod_wsgi)

TASK [a-simple-webserver : copy index.html] ****************************************************
ok: [lab1]

TASK [a-simple-webserver : start httpd] ********************************************************
ok: [lab1]

PLAY RECAP *************************************************************************************
lab1                       : ok=0    changed=4    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

We expect 4 changes:
1. Install httpd.
2. Install python3-mod-wgsi
3. Copy the index.html
4. Start the web server.

http://lab1
![image](https://user-images.githubusercontent.com/14948712/117051383-b7672800-acd3-11eb-9154-13725a6dd47b.png)


## Author 
Moises M.

Twitter: @Moises_Monge_M

## Date
May 4th, 2021
