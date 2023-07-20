*INSTALLATION OF MYSQL*

*STEP 1*: Go to http://pgp.mit.edu/

*STEP 2*: Type mysql-build@oss.oracle.com in the search bar and click on  "Do the search."

*YOU HAVE TO BE VERY PATIENT BECAUSE THAT SITE IS ON COLOS*

*STEP 3:* The search results gives you links to download the key. Click on the KEY ID or User ID to get your key.
It will redirect you to another page.

Copy the key. Start from where ----BEGIN PGP...." and. Stop at ----END PGP

*Copy everything in that block. If you omit it, the gpg will not recognize it when you want to import.*

*STEP 4:* Save what you copied in step 4 somewhere on your system. Possibly your notepad.

*STEP 5:* Login to your web server. Create a new file to save your key using the command:

touch signature.key

*STEP 6* Add the key you saved on your system into the file using the command:

nano signature.key

Add and save the content, then exit.

*STEP 7:* run gpg --import signature.key

It will import the public key.

*STEP 8:* run sudo apt-key add signature.key

The response you will get is "ok"

*STEP 9:*. run sudo sh -c 'echo "deb http://repo.mysql.com/apt/ubuntu bionic mysql-5.7" >> /etc/apt/sources.list.d/mysql.list'

*STEP 10:* run sudo apt-get update


*STEP 11:* run sudo apt-cache policy mysql-server

*STEP 12:*  run sudo apt install -f mysql-client=5.7* mysql-community-server=5.7* mysql-server=5.7*

*STEP 13:* your package configuration will ask you for a strong password. Use something you can remember or you can leave it blank by pressing enter.


Your installation will run successfully if you follow the above listed process accordingly.

Repeat the same process for web server 2.

*Good luck*
Resources
Read or watch:

What is a primary-replica cluster
MySQL primary replica setup
Build a robust database backup strategy

General
What is the main role of a database
What is a database replica
What is the purpose of a database replica
Why database backups need to be stored in different physical locations
What operation should you regularly perform to make sure that your database backup strategy actually works
