# sharingiscaring
A simple vagrant box with super simple task to make it simple sharing files

Execute `VBoxManage  list bridgedifs` to find the list of interface available for bridging

Edit setting.yml file with your setting and copy it to .setting.yml

`vagrant up` and your share folder should be accessible with the given username and passwords.

To access with write access, use vagrant user with smbpassword you configured.

Note: I havent bother adding firewall rule or changing default vagrant ssh password so you should `vagrant ssh` and change vagrant password or using ufw to set some firewall rule if you worry. I just need something quick to share file =p
