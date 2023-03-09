1. su [other_user] - This command is used to switch the current user to another user.
2. id -u -n - This command prints the effective username of the current user.
3. groups - This command prints all groups the current user is part of.
4. sudo chown [new_user] [file_name] - This command changes the owner of a file to another user.
5. touch [file_name] - This command creates an empty file and assign it the name given by the user.
6. chmod [number] [filename] - This command adds the desired permission to the owner of the file hello.
7. chmod ugo+x [filename] - This command adds the execute permission for a file to the user, group and others
8. chmod --reference=reference_file file - This command mirrors the file permissions of one file to another file
9. chmod -R ugo+x . - This command is used to assign permissions to all files in the current working directory.
10. chgrp - This command is used to change the name of a group.
11. chown -R owner_name:group_name file_name - This command changes the owner and group name of a file.
12. chown -h owner:group filename - This command changes the owner and group names for symolic link files. 
