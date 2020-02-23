# Udagram with Microservices

Udagram is a simple cloud application developed alongside the Udacity Cloud Engineering Nanodegree. It allows users to register and log into a web client, post photos to the feed, and process photos using an image filtering microservice.

The project is split into 2 parts:
1. [The Simple Frontend](/frontend) A basic **Ionic** client web application which consumes the RestAPI Backend. 
2. [The RestAPI Backend Microservices](/restapis), **Node-Express** RestAPI microservices (user, feed etc.)

### Setup and Run Backend

Before you begin, set these environment variables first:

```
export PORT=<local_port_to_be_used>
export POSTGRESS_USERNAME=<your_udagram_postgress_username>;
export POSTGRESS_PASSWORD=<your_udagram_postgress_password>;
export POSTGRESS_DB=<your_udagram_postgress_db_name>;
export POSTGRESS_HOST=<your_udagram_postgress_db_host>;
export AWS_REGION=<your_aws_region>;
export AWS_PROFILE=<your_aws_profile_name>;
export AWS_BUCKET=<your_udagram_s3_bucket_name>;
export JWT_SECRET=<jwt_secret>;
```

In the microservice folder that you wish to run:

1. `npm i` to install the dependencies
2. `npm run dev` to run the microservice

### Setup and Run Frontend

In the frontend folder:

1. `npm i` to install the dependencies
2. `ionic serve` to run the app

### Configure The Backend Endpoint in Frontend

Ionic uses enviornment files located in `./src/enviornments/enviornment.*.ts` to load configuration variables at runtime. By default `environment.ts` is used for development and `enviornment.prod.ts` is used for production. The `apiHost` variable should be set to your server url either locally or in the cloud.

### Building the Static Frontend Files

Build artifacts are located in `./www`. To build from source:

```
ionic build
```
