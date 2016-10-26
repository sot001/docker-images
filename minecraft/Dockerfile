# feed the beast minecraft
FROM openjdk:8-jre

# whoami
MAINTAINER Kristian Sotiroff <kristians@gmail.com>

# settings
ENV MC_HOME /home/minecraft

# bootstrapping
# create minecraft user with home 
RUN useradd -d "$MC_HOME" -u 1000 -m -s /bin/bash minecraft

# change ownership of mc dir
RUN chown minecraft:minecraft "$MC_HOME"

# copy across start file
ADD files/start /start 

# make it executable
RUN chmod +x /start

# open the port up
EXPOSE 25565

# run start script
CMD ["/start"]
