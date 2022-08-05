# intent.ai technical assignment

Engineers at intent.ai build highly scaleable distributed systems in a microservices environment. The assignment is designed to evaluate real world activities that are involved with this role.

# Instructions

The goal of this exercise is to write a service in any programming language (golang is prefered) to integrate with our fake ad-exchange service, which is provided as a Docker container in the file docker-compose.yaml of this repository. Please refer to the Google's [OpenRTB documentation](https://developers.google.com/authorized-buyers/rtb/openrtb-guide) for information on how to interact with the API. The provided container expects only a single **env**  which meant to be the final service bidder endpoint. The bidder service should register itself with the ad-exchange so that it can receive requests.

A mapping of OpenRTB protocol can be found in [this repo](https://github.com/bsm/openrtb)

# What do we expect

- A service which can answer bid requests in OpenRTB made by the fake ad-exchange.
- A service which can have a way to pre-configure very basic ad campaigns (db, file-system or hardcoded) to bid with.
- The bidder should respect blocked IAB categories from the bid request.

An ideal solution should run in docker environment with docker compose command and include a Dockerfile in the solution. 

**Bonus point:** It would be nice if you could also capture some auction metrics, i.e distribution of bid requests per IAB category. 
