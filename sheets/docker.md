# Docker
* Build docker image
    * `docker build -f some/path/Dockerfile -t registery`

# Volume Creation
1. Create a volume from SMB network drive
    ```
    docker volume create --driver local --opt type=cifs --opt device=FULL/PATH --opt o=addr=HOST-NAME,username=USERNAME,password=PASSWORD,file_mode=0777,dir_mode=0777 --name VOLUMENAME
    ```
    * Common gotchas
        * HOST-NAME should not include `//`
        * FULL/PATH should have `/` path even on a windows machine
        * don't forget to replace PASSWORD with the actual password

1. Create volume from local folder
    ```
    docker volume create --name MY-VOLUME-NAME --opt type=none --opt device=/HOST/PATH/TO/VOLUME --opt o=bind
    ```




## Gotchas
1. you need to delete a volume before recreating it with differnet options. If you just pass in the different options with the same name it'll appear as if it worked but it won't change anything. 