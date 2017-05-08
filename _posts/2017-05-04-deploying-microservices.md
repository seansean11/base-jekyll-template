---
date: 2017-01-15
title: Deploying microservices in the real world
description: Denver Code Club Meetup
categories:
  - platform
  - devops
  - microservices
type: Talk
---

# CI/CD
- Need a centralized code repository
  - Need a hook to kick off the build process
- Automated builds
  - Run integration and unit tests
- Automated deployment

## Deployment Pipelines
i.e. `git push -> unit tests -> Elastic Beanstalk`

i.e. `git push -> unit tests -> test AWS account -> integration tests/e2e tests/stress tests -> production -> manual judgement -> stable aws account`

## Cattle not pets
- pets: server or server pairs that are treated as indeispensable or unique systems that can never be down
- cattle: more than two servers, that are built using automated tools, and are designed for failure, where no servers are irreplaceable

## Types of deployments
- Blue/green: 2 load balancers that point to the 2 different versions of the application