# feed the beast minecraft
FROM sotirk/minecraft-ftb:1.0

# whoami
MAINTAINER Kristian Sotiroff <kristians@gmail.com>

# INSTALL BITS
RUN apt-get update && apt-get install -y vim wget curl

# bootstrapping
#RUN mkdir /home/ftb
ADD FTBInstall.sh /home/ftb/FTBInstall.sh
RUN /home/ftb/FTBInstall.sh
