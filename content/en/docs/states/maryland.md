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
from claritygov.services.legislators_service import get_state_house_members

# Returns a list of Delegate models. See claritygov.models.Delegate for more information on the model.
members = get_state_house_members('md')
# Print out the list of Delegates.
print(members)
```