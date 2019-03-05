# ansible-automates-Cisco-lab

## How to start 

- Clone this repo in your VM instance for Cisco lab.
- Check if the directory /tmp/tower_install exist.
```
ls -la /tmp/tower_install
```
- Copy the files tower-backup to /tmp/tower_install
```
sudo cp -v CiscoLab/tower-backup* /tmp/tower_install
```
- Load the backup in Tower. 
```
sudo /tmp/tower_install/setup.sh -r 
```
- Refresh your inventory 
```
udo awx-manage inventory_import --inventory-name "Cisco lab inventory" --source ~/networking-workshop/lab_inventory/hosts
```
- Using your browser, connect to Tower and login with
```
User: admin
Pass: ansible
```
- Use the license file to license your Ansible Tower. 
- From Tower UI refresh the SSH Private Key for the Web Servers, using the file: 
```
/home/student1/.ssh/aws-private.pem
```
- Check the connection with your Web Servers running a command from Tower.
- Go to your templates, and check that all runs OK. 

- If you have any question, please raise your hand and ask to your instructors.
- Enjoy!!! :)
