# deployment-monitor

[CircleCI Builds](https://circleci.com/gh/skilbjo/markets-etl)

[![CircleCI](https://circleci.com/gh/skilbjo/deployment-monitor/tree/master.svg?style=svg&circle-token=1427ed4bcdf8f82641a3db4f3ddb5dd87a543e58)](https://circleci.com/gh/skilbjo/deployment-monitor/tree/master)
[![Docker Repository on Quay](https://quay.io/repository/skilbjo/deployment-monitor/status "Docker Repository on Quay")](https://quay.io/repository/skilbjo/deployment-monitor)

## What

I've noticed my webserver stops working on both single board computers (I use
HAproxy to load balance) after ~2 weeks. Let's have a job the periodically
restarts them.

## Run manually

    src/monitor

## environment variables

    export foo=
