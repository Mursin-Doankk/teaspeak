# install TeaspeakServer
```
apt-get update
```
apt-get upgrade
```
apt-get install curl
```
apt-get install ffmpeg (Just if you want Costum TeaSpeak musicbot)
```
apt-get install youtube-dl (Just if you want Costum TeaSpeak musicbot)
```
apt-get install screen
```
apt-get install libnice10 -y
```
For your own security, do not run TeaSpeak or any other closed source program on your root account,
Create another user for it.
Create a new user called TeaSpeak, for example:

adduser teaspeak

Login to the new created user:

su teaspeak

Download the latest version with the links below:

64bit:
wget -O TeaSpeak.tar.gz https://repo.teaspeak.de/server/linux/amd64/TeaSpeak-$(curl -k https://repo.teaspeak.de/server/linux/amd64/latest).tar.gz;

32bit:
wget -O TeaSpeak.tar.gz https://repo.teaspeak.de/server/linux/x86/TeaSpeak-$(curl -k https://repo.teaspeak.de/server/linux/x86/latest).tar.gz;

Extract the ".tar.gz" file and delete it:

tar -xzf TeaSpeak.tar.gz
rm TeaSpeak.tar.gz

Start the server using a screen session so it keeps running in the background and doesn't shut itself down when you leave your SSH session:

screen -AmdS TeaSpeak-Server
screen -x
./teastart_minimal.sh

Save your token and your query-login data into wordpad or wherever you can get it back anytime.

Close the session again with CTRL+C

Now edit the config file whith your needs (Ports: 10011 and 30033)
After you've completely edited your config file, you can start the server using:

./teastart.sh start

Stop it by using:

./teastart.sh stop

To detach from the screen session, press:

CTRL + A and CTRL +D

Done, you got your server running on port 9987!
