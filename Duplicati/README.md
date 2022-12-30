# _Docker-Compose_Duplicati

This is a yaml config file to install and configure a *Duplicati* contaniner to back up your server. Please run it with the following command and appropriate permissions:

    docker compose up -d

**Important:** please keep in mind that, *source* files & folders are stored under *"Computer/source"* so, please, expand the folders three and do not expect to see them under *"User Data"* or the *"/source"* folder in the root of the backup page.
