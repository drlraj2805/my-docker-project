# IIEC-DOCKER-PROJECT
This project aims at setting up the content management app **DRUPAL** by setting up the entire infrastructure **using docker-compose**.

# My-docker-project
**Introduction**
+ This project is developed using **Docker** using Red Hat Enterprise Linux 8 as its host. Docker, launched in 2013 has become the standard for containerization technology. Docker technology has made the life of developers so simple. Using docker-compose, the setting up of the entire infrastructure including database launch is done using just one command.
+ This project is developed using **Docker** using **Red Hat Enterprise Linux 8** as its host. Docker, launched in 2013 has become the standard for containerization technology. Docker technology has made the life of developers so simple. Using docker-compose, the setting up of the entire infrastructure including database launch is done using just one command.


**SET-UP FOR PROJECT**

*Following are the pre-requisites to set-up the infrastructure:*
1. Docker needs to be installed on our base OS and we need to start the docker services.
   To start docker services permanently ```systemctl enable docker```.
2. We need to install the docker-compose software inorder to use it. To install docker- compose, follow the steps: * *Go to google --> In the search box search ```docker compose rpm``` --> Choose `Install Docker compose` --> Based on the base OS select whether Mac, Windows or Linux etc. --> Copy the command and paste it in the terminal of the base OS.
3. Pull the images from [docker image registry](hub.docker.com)
 - Pulling MySQL Image: Use `docker pull mysql:5.7` to download **MySQL version 5.7** image. I have used version 5.7 as it is considered the most compatible version with RHEL 8.
 - Pulling Drupal Image: Use `docker pull drupal:latest`
Set-up for project:-

@@ To create the entire infrastructure, we need to write code in **.yml** or **YAML
1. we have to create a directry for storing .yml file. for this use 'mkdir /dockercompose' in linux bash .name is is of your wish.
2.Inside dockercompose directory, we create our workspace. To go inside directory, use `cd /dockercompose.`
3. Create the **.yml** file using `vim docker-compose.yml`. docker-compose.yml is the default file where code is written. Since each compose file has same file name, it is a good practise to make seperate directory for each code.
4. Inside this .yml file we write our code. To start editing the text editor press * *i* * on the keyboard. After we finish writing the code, to save the file, press * *esc* * on the keyboard and type `:w` to save the file and `:q` to exit the file. To save and exit in one step, type`:wq` together.
5. Inside the directory itself run the command `docker-compose up` to launch all the containers in the infrastructure in one go. To launch the containers in background, use `docker-compose up -d`.
6. Our **Drupal** site is launched using mysql as database.
6. Our **Drupal** site is launched using MySQL as database.
7. To stop container, use `docker-compose stop` in another terminal on same directory or press left Ctrl + C.

**Introduction about drupal** :-
Drupal is a free and open-source content-management framework written in PHP and distributed under the GNU General Public License. It is used as a back-end framework for at least 2.1% of all Web sites worldwide ranging from personal blogs to corporate, political, and government sites including WhiteHouse.gov and data.gov.uk. It is also used for knowledge management and business collaboration.

here volume for drupal is created under the /var/www/html/....
and volume for mysql is created under /var/www/html/mysql..
