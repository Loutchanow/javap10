# BobApp

Clone project:

> git clone XXXXX

## Front-end

Go inside folder the front folder:

> cd front

Install dependencies:

> npm install

Launch Front-end:

> npm run start;

### Docker network

network create bobapp-net

### Docker

Build the container:

> docker build -t bobapp-front .

docker network connect bobapp-net bobapp-front

Start the container:

docker run --network bobapp-net -p 4200:80 --name bobapp-front -d bobapp-front

## Back-end

Go inside folder the back folder:

> cd back

Install dependencies:

> mvn clean install

Launch Back-end:

> mvn spring-boot:run

Launch the tests:

> mvn clean install

### Docker

Build the container:

> docker build -t bobapp-back .

docker network connect bobapp-net bobapp-back

Start the container:

docker run --network bobapp-net -p 8080:8080 --name bobapp-back -d bobapp-back
