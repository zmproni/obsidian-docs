```bash
cat /etc/lsb-release #Check ubuntu version

sudo apt-get install gnupg curl #TODO: Check significance of this software

#Import MongoDB public GPG key
curl -fsSL https://pgp.mongodb.com/server-7.0.asc | \
   sudo gpg -o /usr/share/keyrings/mongodb-server-7.0.gpg \
   --dearmor

#Create list file for version of ubuntu
echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-7.0.gpg ] https://repo.mongodb.org/apt/ubuntu jammy/mongodb-org/7.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-7.0.list

sudo apt-get update #Reload local package database

sudo apt-get install -y mongodb-org #Install latest stable version of MongoDB


``` 