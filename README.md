# AMQP Web Services

Welcome to RabbitMQ Web Services! This README will guide you through setting up, running, and contributing to the application.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Contact](#contact)

## Overview

AMQP Web Services is a Advanced Message Queuing Protocol web services Using (RabbitMQ & Worker Service).

## Features

- RabbitMQ
- Background Services

## Prerequisites

- [.Net] (version 8.0.0)
- [VS 2022]
- [Docker](https://www.docker.com/) (optional, for running RabbitMQ in a container)

## Installation

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/abdooAhmed/AMQP-WebServices-.git
   ```
2. Setting up RabbitMQ
   i. Install Docker from the following link : https://docs.docker.com/engine/install/
   ii. Start Docker
   iii. At the command prompt or terminal, pull down the latest container image for RabbitMQ on Docker and run it
   `docker run -it --rm --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq`
3. setting up Database
   i.Navigate to the DB directory
   ii.Run "Northwind4SQLServer.sql" file in your MSSM Studio

## Usage

1. Running Locally :
   1. To start the application locally, open "AMQP & Background Services.sln" file in VS 2024
   2. Start the Northwind.WebApi.Service project without debugging "Click right on Northwind.WebApi.Service project Debug -> Start without Debuging"
   3. Start the Northwind.WebApi.Client.Mvc project without debugging so that we can send messages to the RabbitMQ queue
   4. In the MVC website, click Send a message, and then enter a message of apples and a product ID of 1 ,Repeat for bananas and 2, and cherries and 3.
   5. Start the Northwind.Background.Workers project without debugging, and note the three messages are processed from the queue

## Contact

-If you have any questions or feedback, please reach out to me at [abdulrahman.ahmed.abdulah@gmail.com].
