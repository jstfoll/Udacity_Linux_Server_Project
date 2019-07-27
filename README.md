# Udacity_Linux_Server_Project



- Login into amazon light sail.
- Once you are login into the site, click `Create instance`. 
- Choose `Linux/Unix` platform, `OS Only` and  `Ubuntu 16.04 LTS`.
- Wait for the instance to start up.


All system packages have been updated to most recent versions.


As per yoor review now only allowing connections for SSH (port 2200), HTTP (port 80), and NTP (port 123).




To login to root user directly use the light_key.rsa in the github repo and ssh using the following command

ssh -i light_key.rsa -p 2200 ubuntu@13.233.111.112


To run any commands plese note that password is password

I have created user grader 

login to it from your machine with command 

ssh -i grader_key -p 2200 grader@13.233.111.112

The contents of grader_key is submitted in  "Notes to Reviewer" field.

To run any sudo commands please note that password for grader is also password

Public IP of the instance:13.233.111.112
links:http://ec2-13-233-111-112.ap-south-1.compute.amazonaws.com/
http://13.233.111.112/

after you ssh into the instance as grader with the above command cd the below command to see the code base

cd /var/www/catalog/


## Folder structure

The folder structure

``` 
/var/www/catalog
    |-- catalog.wsgi
    |__ /catalog             # Our Application Module
         |-- __init__.py
         |-- data.py
         |-- database.py
         |-- /models
              |-- __init__.py
              |-- category.py
              |-- item.py
              |__ user.py   
         |-- /static
              |__ styles.css
         |-- /templates
              |-- about.html
              |-- base.html
              |-- categories.html
              |-- delete_item.html 
              |-- edit_item.html
              |-- login.html
              |-- new_item.html
              |__ show_item.html
         |-- /utils
              |__ lorem_ipsum_generator.py
         |-- /venv3          # Virtual Environment
         |__ /views
              |-- __init__.py
              |-- about.py
              |-- api.py
              |-- auth.py
              |-- category_view.py
              |-- item_view.py
              |__ user_view.py
```

