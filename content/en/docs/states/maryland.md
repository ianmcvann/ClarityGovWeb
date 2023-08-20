---
title: "Maryland"
description: ""
lead: ""
date: 2023-07-21T16:47:53-05:00
lastmod: 2023-07-21T16:47:53-05:00
draft: false
images: []
menu:
  docs:
    parent: "states"
weight: 999
toc: true
---
The following section describes the data accessible for Maryland via the ClarityGov API. Note that the following page may be inaccurate, and should be used for quick reference only. Generated API docs are available [here](https://api.claritygov.com/docs/). 

## House
### Get Delegates 
Endpoint: `/md/house/members`

Description: Returns a list of all delegates in the Maryland House of Delegates.

```python
from claritygov.services.legislators_service import get_state_house_members

# Returns a list of Delegate models. See claritygov.models.Delegate for more information on the model.
members = get_state_house_members('md')
# Print out the list of Delegates.
print(members)
```

### Get Senators
Endpoint: `/md/senate/senators`

Description:  Returns a list of senators.

## Bills

### Get Bills by Session
Endpoint: `/md/bills/{year}`

Description: Returns a list of all bills from the current session.
### Get Bills By Session and Chamber
Endpoint: `/md/bills/{year}/house` or `/md/bills/{year}/senate`

Description: Returns a list of all bills in that chamber by session.
### Get Bill Details by Chamber, Session, and Bill Number
Endpoint: `/md/bills/{year}/{chamber}/{bill_number}`

Description: Returns bill details about a bill by number.

## Votes

### Get All Votes for Bill in Session
Endpoint: `/md/votes/{session}/{bill_number}`

Description: Returns all votes in list format for a particular bill.
### Get Votes for Bill in Session by Chamber
Endpoint: `/md/votes/{session}/{chamber}/{bill_number}`

Description: Returns votes in a specific chamber for a particular bill.

## Committees

### Get Committees By State, Session, and Chamber
Endpoint: `/md/committees/{session}/{chamber}`

Description: Returns basic committee details for a specific chamber. 
