## File Permissions and Access Control Lists

Create a simple file and do ls -ltr to see the details of the files. As a task, change the user permissions of the file and note the changes after ls -ltr

2. File permissions :

Each of the three permissions are assigned to three defined categories of users. The categories are:

1.  user (u) : A user is the owner of the file.
2.  group (g) : Group is a collection of users.
3.  other (o) : Other is everyone that is not the owner or in the group.

There are three basic file system permissions, or modes, to files and directories:  1. read (r=4)   : The file can be opened, and its content viewed.

2. write (w=2)  : The file can be edited, modified, and deleted.

3. execute (e=1) : If the file is a script or a program, it can be run (executed).

The first character indicates the file type. It can be a regular file (-), directory (d), a symbolic link(l), or other special types of files. The following nine characters represent the file permissions, three triplets of three characters each.

The first triplet shows the owner permissions,

The second one group permissions, and

The last triplet shows everybody else permissions.

For change ownership: chown is used to change the ownership permission of a file or directory. Synax : chown <user_name> <file_name> eg. example : chown sayali demo.txt

for change group ownership: chgrp is used to change the gropu permission of a file or directory. Syntax : chgrp <group_name> <file_name> example: chgrp devopsgrp demo.txt

Set permission with numeric value: r(read)=4 w(write)=2 x(execute)=1

example chmod 751 demo.txt In above example, u = 7 = r(4)+w(2)+x(1) - user have read, write and execute permission. g = 5 = r(4)+x(1) - group have read and execute permission. 0 = 1 = e(1) - other have execute permission.

3 . Access Control list (ACL): ACLs allow us to apply a more specific set of permissions to a file or directory without changing the base ownership and permissions. Access control list (ACL) provides an additional, more flexible permission mechanism for file systems.

setfacl and getfacl are used for setting up ACL and showing ACL respectively.

For check ACL permission: Syntax . getfacl <name of file or directory> eg. getfacl demo.txt

For set ACL permission to user: Syntax : setfacl -m u:user:permissions /path_to_file eg. setfacl -m u:sayali:rwx /devops

For remove ACL permission of user: Syntax : setfacl -x u:user: /path_to_file eg. setfacl -x u:sayali: /devops

For set ACL permission to Group: Syntax : setfacl -m g:group:permissions /path_to_file eg. setfcal -m g:sayaligrp:rwx /devops

For remove ACL permission of group: Syntax : setfacl -x g:group: /path_to_file eg. setfacl -x g:sayaligrp: /devops

To remove all ACL permissions: Synatx: setfacl -b /path_to_file eg. setfacl -b /devops
