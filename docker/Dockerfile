FROM nginx:latest

RUN apt update
RUN apt install sudo git -y
RUN useradd -rm -d /home/admin -s /bin/bash -g root -G sudo -u 1001 admin
RUN cd /var
RUN sudo mkdir -p www/html/lsac/2023/internal
RUN sudo apt install python3 wget gnupg -y
RUN wget -qO - https://www.mongodb.org/static/pgp/server-6.0.asc | sudo apt-key add -
RUN echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/6.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-6.0.list
RUN sudo apt update
RUN sudo apt install -y mongodb-org
RUN sudo mkdir /etc/nginx/sites-available
RUN sudo mkdir /etc/nginx/sites-enabled

