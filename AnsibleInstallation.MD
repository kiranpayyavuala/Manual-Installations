#### On RHEL 8.x server

Install Python, to use just python, use "alternatives" command.
   ```sh 
   yum install python3 -y
   alternatives --set python /usr/bin/python3
   ```
CheckRunning python -V should show default Python version configured
   ```sh 
   python --version
   ```
Install python-pip package manager
   ```sh 
   yum -y install python3-pip
   ```

Create a new user for ansible administration & grant admin access to the user
   ```sh 
   useradd ansible
   passwd ansible
   ```
 Below command adds ansadmin to sudoers file. But we strongly recommended using "visudo" command if you are aware vi or nano editor.  (on Control node and Managed host)
   ```sh
   echo "ansible ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers
   ```

```sh 
   # sed command replaces "PasswordAuthentication no to yes" without editing file 
    sed -ie 's/PasswordAuthentication no/PasswordAuthentication yes/' /etc/ssh/sshd_config
    sudo service sshd reload
   ``` 

#### Install Ansible as a ansadmin user (on Control node)
   ```sh 
   su - ansible
   pip3 install ansible
   ``` 
check for ansible version 
   ```sh
   ansible --version
      
      ansible 2.7.6
         config file = None
         configured module search path = ['/home/ansible/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
         ansible python module location = /home/ansible/.local/lib/python3.6/site-packages/ansible
         executable location = /home/ansible/.local/bin/ansible
         python version = 3.6.6 (default, Oct 16 2018, 01:53:53) [GCC 8.2.1 20180905 (Red Hat 8.2.1-3)]
   ```
