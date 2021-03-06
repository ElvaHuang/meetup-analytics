# Graph-based analytics platform

A graph-based analytics platform to track and measure meetup.com groups growth over time. Identify community trends and see what people are meeting about in the world. 

![Meetup Analytics Dashboard](https://raw.githubusercontent.com/kbastani/meetup-analytics/master/docs/images/Meetup%20Analytics%20Dashboard%20-%20Screen.png)

Check out a demo of the dashboard: [Meetup Analytics NoSQL Dashboard](http://meetup-analytics-dashboard.herokuapp.com/)

## Documentation

Read the full project documentation here: [Graph-based Analytics Platform Docs](https://github.com/kbastani/meetup-analytics/blob/master/docs/DOCS.md)

## Architecture

![Graph-based Analytics System Diagram](https://raw.githubusercontent.com/kbastani/meetup-analytics/master/docs/images/graph-based-analytics-system-diagram.png)

* Front-end web-based dashboard in Node.js and bootstrap
* REST API via Neo4j Swagger in Node.js
* Data import services in Node.js
* Data storage in Neo4j graph database

### Prerequisites

* An instance of Neo4j (`>=2.1`) running locally - [http://www.neo4j.org/download](http://www.neo4j.org/download_thanks?edition=community&release=2.1.0-M01)
* A Meetup.com API Key for running data import services - [http://www.meetup.com/meetup_api/](http://www.meetup.com/meetup_api/)
* Installed `node.js` and `npm` on your machine

### Usage

Follow the directions below for each component of the platform.

#### Database

* Extract the Neo4j store files located in `neo4j/data.zip` to your Neo4j data directory `neo4j/data`
* Start the Neo4j server at `http://localhost:7474`

#### REST API

* From the terminal, go to the `api` directory of the project and run `npm install`, after `node_modules` are installed, run `node app`. The analytics REST API will be started at `http://localhost:3000`

#### Analytics Dashboard
* From the terminal, go to the `dashboard` directory of the project and run `npm install`, after `node_modules` are installed, run `node app`. The analytics dashboard will be started at `http://localhost:5000`

#### Data Import Scheduler
* From the terminal, go to the `scheduler` directory of the project and run `npm install`, after `node_modules` are installed, run `node app`. The Meetup group import scheduler will be started at `http://localhost:3001`. It will run once a day 5 minutes after midnight PST.

### Specifications

You can find the project specifications as a [GraphGist project](http://gist.neo4j.org) app at [Neo4j for Graph Analytics: Meetup.com Example](http://gist.neo4j.org/?e2e0e4469917729765fe)

### Feedback

Feedback is welcome. Reach out to me on Twitter [@kennybastani](http://www.twitter.com/kennybastani) if you are interested in contributing to this project. 

