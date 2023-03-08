# Video to audio microservices converter
  Result of a course in Microservice Architecture and System Design

## Description

This is a microservices application that converts video files to audio files. It is written in Python using modules such as Flask, MongoDB, GridFS.

Each service is containarized using Docker.

It also has all the manifests for creating them in a Kubernetes cluster, it suffices to run:

> kubectl apply -f ./manifests/

  in each of the services and it would be up and running for its use.

There are 6 services running:

 - Authentication
 - Conversion
 - Gateway
 - MySQL instance
 - Notification
 - Rabbit mq

with the unique access point to Gateway using the host "mp3converter.com" specified in the [ingress.yaml](/python/src/gateway/manifests/ingress.yaml) file. This was done by using a tunneling service.