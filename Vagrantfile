#!/bin/bash
read -p "Enter username : " username
## Tim, you need to change line below to replace with /etc/passwd because there is no such file /passwd - comment by Svetlana Gluhova
# Svetlana, just added the changes per your comments
egrep "^$username" /etc/passwd >/dev/null
        if [ $? -eq 0 ]; then
                passwd $username
                echo "Password Updated."
                exit 1
        else
                echo "User does not exist."
                exit 1
fi
