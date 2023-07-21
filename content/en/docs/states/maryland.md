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
The following section describes the currently supported endpoints for the Maryland State API. The following table will be updated as new endpoints are added to the ClarityGov API.

## House

Maryland House of Delegates Data

### Get Delegates

Endpoint: `/md/house/members`

Returns a list of all delegates in the Maryland House of Delegates.

```python
from claritygov.api.state import State
from claritygov.api_client import ClarityAPIClient
from claritygov.api.house import House

api_client = ClarityAPIClient()
state = State(api_client, 'Maryland')
house = House(state)
members = house.get_house_members()
```