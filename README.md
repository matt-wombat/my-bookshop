# My Bookshop - SAP Developers Tutorial für CAP Business Application

Welcome to the My Bookshop tutorial project.

Here a application is built with CDS entirely on local environment with Visual Studio Code and then deployed to the SAP Business Technology Platform.

It is based on the SAP Developers Tutorial Build a Business Application Using CAP for Node.js:

https://developers.sap.com/mission.cp-starter-extensions-cap.html

## Contents

It contains these folders and files, following our recommended project layout:

File or Folder | Purpose
---------|----------
`app/` | content for UI frontends goes here
`db/` | your domain models and data go here
`srv/` | your service models and code go here
`package.json` | project metadata and configuration
`readme.md` | this getting started guide


## Next Steps

### Run in Local Terminal

- Open a new terminal and run `cds watch` 
- (in VS Code simply choose _**Terminal** > Run Task > cds watch_)
- Start adding content, for example, a [db/schema.cds](db/schema.cds).

### Deploy to SAP Business Technology Platform

- Login: `cf login`
- Create service: `cf create-service hana hdi-shared my-bookshop-db`
- Build: `cds build --production`
- Push Database: `cf push -f gen/db`
- Push Service: `cf push -f gen/srv --random-route`

