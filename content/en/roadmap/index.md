---
title: "Roadmap"
description: "Report incorrect data to us"
date: 2020-08-27T19:23:18+02:00
lastmod: 2020-08-27T19:23:18+02:00
contributors: ["Ian McVann"]
draft: false
images: []
---

### Introduction

Hello and welcome to the ClarityGov API roadmap. This page is a living document that outlines the current and future development of the ClarityGov API. If you have any questions or suggestions, please contact us using the report form [here](/report).

My name is [Ian McVann](https://github.com/ianmcvann) and I am the developer of the ClarityGov API. I am a current college student majoring in International Affairs and Computer Science at the [George Washington University](https://www.gwu.edu/). This project is a passion project of mine that I work on in my spare time, as I believe that government data should be free and accessible to all.

ClarityGov API is a free, public developer API for accessing government legislative data in a standardized format. The API is currently in beta and is being actively developed, and is subject to change. 

### Architecture

The ClarityGov service is broken into currently 5 components:
- Backend - The backend is responsible for collecting data from government sources and storing it in our database. This is not publicly accessible, but is where the most development is currently taking place.
- [Server](https://api.claritygov.com) - The server is responsible for serving the data to the public. This is where the API is hosted, and is publicly accessible.
- [Swagger Docs](https://api.claritygov.com/docs) - The Swagger Docs are automatically generated from the server and are publicly accessible. They are the most up to date documentation for the API.
- [Python Package](https://pypi.org/project/claritygov/) - The Python Package is publicly accessible. It is the easiest way to interact with the API without using manual requests directly.
- [Documentation](https://claritygov.com) - The documentation is manually written and is publicly accessible. It is intended to provide a high level overview of the API.

### Development - July 2023

Maryland is the first state to be added to the ClarityGov API. The following data is currently available for Maryland:
- Bills
- Legislators
- Votes (Partial, needs verification)

The following data is currently being added:
- Committees

Once the Maryland data is complete, I need to update the Python Package to include the new data (including structure changes). I also need to update the documentation to include the new data.

The goal is for the development process to look something like:

`
Backend Changes -> Server Changes -> Swagger Doc Changes -> Python Package Changes -> Documentation Changes
`

Notably, this means that there may be points where the API or Python package is not fully functional. I will try to minimize this as much as possible, but it is inevitable. It also means that there may be endpoints that are not documented, not included yet in the Python package (but are in [REST](https://api.claritygov.com/docs)), or that the documentation is not up to date. If you find any issues, please [report them](/report) along with any incorrect API data. I will try to fix any issues as soon as possible.

### August 2023

Great progress has been made in the past month. 
* Votes and Committees have been added to the API backend for Maryland.
* Google Sheets integration is almost complete and ready for user testing. It is currently in closed beta, but will be released soon.
* The Python package has been updated to include the new data. The documentation has also been updated to include the new data.

Immediate next steps are:
* Get Google Sheets integration out to first users.
* Add a monitoring script to the backend to ensure that the data is up to date, tracking new bills as they are created/voted on.

The second part in particular I believe should be prioritized before new state additions. Once that's done, I will be able to add new states much more quickly. The next state will be Minnesota. 
