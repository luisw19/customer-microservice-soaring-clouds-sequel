#  Node based on Debian GNU/Linux 8 -must be used as kafka-avro errors with non-debian based distros
FROM node:9

# Create Orders API directory and copy source to it
RUN mkdir -p /usr/src/api
COPY . /usr/src/api

# Set working dir
WORKDIR /usr/src/api

#Install kafka-avro dependencies e.g. Cyrus SASL, etc
RUN apt-get update && apt-get install -y \
curl \
build-essential \
groff-base \
libdb-dev \
libssl1.0.0 libssl-dev libiodbc2 libiodbc2-dev libsasl2-2 libsasl2-dev \
sasl2-bin

############ Install kafka-avro and dependenies
RUN npm install express --save
RUN npm install --save mongoose
RUN npm install body-parser --save
RUN npm install bcrypt --save
RUN npm install cors
RUN npm install kafka-avro --save

############
RUN npm install

EXPOSE 8080
CMD [ "npm", "start" ]
