## Ansible Scripts

### Find Sources
  
[Playbook and Inventory files](https://github.com/prabes/Ansible-Scripts/commit/9968cd31c3bf13ffd0b186555752824925dda437)  
[Using Vars and Handlers](https://github.com/prabes/Ansible-Scripts/commit/ac41842e4524a309be5a9611af0e658f6d03da37)  
[Working with roles](https://github.com/prabes/Ansible-Scripts/tree/Working-with-Roles)  

### Running Playbook

* Clone this repo to your local. Make sure you're on master branch
* Adjust variables for your enviroments
* Run with `ansible-playbook -i <inventory_file.ini> <playbook.yml>`

### Expected Result

This playbook should make wordpress running on the targeted machine, with all `php-dependencies`, `mysql-server`, `nginx` and `wordpress`. 
