# Setting up development environment

## Clone
First use [git](http://git-scm.com/) to clone this repo:

    git clone {TODO: add stash URL}
    cd quickfixj-bridge-parent

## Build
UMF is built with [Maven](http://maven.apache.org/).

    mvn clean install

The above will build the prototype and run all unit tests.

## Run Bank services (open new Terminal tab)
    cd quickfixj-bank
    mvn exec:java

## Run Bridge services (open new Terminal tab)
    cd quickfixj-bridge
    mvn exec:java

## Run Venue services (open new Terminal tab)
    cd quickfixj-venue
    mvn exec:java

## Explore
* Monitor the logs output to the console by each applications
* Venue simulator periodically subscribes to different symbols, receive quotes and then cancels RFQs
* Bridge is passing messages between the venue and the bank
* Bank simulator generates quotes in response to RFQ requests
