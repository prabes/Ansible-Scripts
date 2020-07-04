
# Writing Ansible Automation for deploying Wordpress

Firstly, I tried installing and making it run manually cause I needed to know what it's takes to deploy wordpress in Ubuntu server.
I used NGINX, PHP and MySQL to configure the server. 

Now, I got the through information about tools I need to configure and steps I need to automate. 

### Creating A Inventory file

    $ code hosts.ini

I used vagrant for creating my virtual boxes and create my test enviroments.
So, I added followings to the inventory file.

    [appserver]
    192.168.33.10 ansible_user=vagrant

  * `ansible_user` is the user name to use when connecting to the host.
  *  Multiple or different hosts can be grouped in inventory file and picked for specific tasks in playbook.
  *  we can also write inventory file in JSON but I am new to YAML and like learning it.

### Creating A Playbook

  In Progress . . . 


### Adding SSH key

As I mentioned earlier, We need to add SSH key to perform tasks created in the playbook.
In order to do that, we need to add SSH key of your machine into `authorized_keys` of the specific `ansible_user`

Paste ssh key to `~/.ssh/authorized_keys` of that specific user connecting to the host.

### Running the playbook

Ansible provides us command as:

    $ ansible-playbook -i <inventory_file> <playbook>

ie,
    
    $ anisble-playbook -i wordpress.ini env_setup.yml