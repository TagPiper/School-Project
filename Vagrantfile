#!/bin/bash
read -p "Enter username : " username
egrep "^$username" /passwd >/dev/null
        if [ $? -eq 0 ]; then
                passwd $username
                echo "Password Updated."
                exit 1
        else
                echo "User does not exist."
                exit 1
fi
