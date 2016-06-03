# WP_Dock

README has not well written yet! (You have to wait a while)

WP_Dock is a docker compose project for WordPress. It supports both HHVM and PHP7. For now it only supports one at the time. In the future will also support HHVM and PHP-FPM as backup when HHVM fails. MySQL is the only supported database for now. This project only supports NGINX and will not support Apache in the future.

##Installation guide

  - First you have to download [Docker Toolbox][1] if you haven't already.
  - Download/Clone this project.
  - Download WordPress, copy it inside the folder and rename it to 'app'.
  - Navigate with terminal inside docker folder.
  - `docker-compose up -d nginx` // It builds docker containers using 'docker-compose.yml' as its configuration
  - `docker-machine ip default`  // To see the ip of the VM machine that this project runs on
  - Open your browser to that IP and you will see the WordPress installation guide.
  - Don't forget to change the WP configuration to
     - databaseName -> 'databasename'
     - databaseUser -> 'username'
     - databasePassword -> 'secret'

Note: Also the host on WP configuration should be the ip of the machine (`docker-machine ip default`)

Things to improve/add in the future:
  - Make the host dynamic not with hardcoded IP
  - Make HHVM as primary and PHP-FPM as fallback (optional option)
  - Add more databases
  - Separate WordPress folder from upload, plugins, themes folders
  - Create a workflow for dev to production deployment

[1]: https://www.docker.com/products/overview#/docker_toolbox
