FROM openjdk:8

RUN apt-get -y update --fix-missing
RUN apt-get upgrade -y

# Install tools & libraries
RUN apt-get -y install apt-utils nano wget dialog \
    build-essential git curl libcurl3 libcurl3-dev zip


#CMD ["sh", "-c", "/root/bin/auth.sh -vC start ; /root/bin/world.sh -vC start"]