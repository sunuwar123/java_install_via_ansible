# java_install_via_ansible

This playbook is to install specific version of Java.

The first step is to download the java tar.gz file and place it under roles/Java_install/files directory
The java_home variable can be defined according to your requirement. In my case I have placed it under /opt/ansible folder.

If the java version is changed in your case, you then have to rename with_items in the roles/tasks/main.yml

Also the hosts should be according to the target machine and needs to be defined under hosts

To execute the playbook you can use below command

ansible-playbook -i hosts -vv playbook.yml -K

If you are executing it via root user then -K is not needed.
