# _Docker-Compose_Eclipse-Mosquitto
The script will create a container for running Eclipse Mosquitto MQTT broker with Docker.
Remember to modify the name of the container in the script with your own.

Instructions:
 - create the directory structure before running the yaml file.
 - The full and original mosquitto.config file from Eclipse.org can be found at https://github.com/eclipse/mosquitto/blob/master/mosquitto.conf
   documentation can be found here https://mosquitto.org/man/mosquitto-conf-5.html
 - Remember to configure/enable the following keys:
    - password_file /mosquitto/config/<password_filename>
    - persistence true #default is false
    - persistence_location /mosquitto/data
    - log_dest file /mosquitto/log/<filename>
    - listener 1883 0.0.0.0 #default configuration accepts connections only from local-to-mqtt-server clients
 - To configure a username/password use the following commands:
    1) attach to the running docker container ==> sudo docker exec -it <container_name> sh
    2) change directory to where configuration are stored ==> cd /mosquitto/config
    3) execute the following command and follow the instruction on the screen ==> mosquitto_passwd -c /mosquitto/config/<password_filename> <username>
    4) if everything is running fine you should have a <password_filename> in your persistent folder 
