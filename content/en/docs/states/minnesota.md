---
title: "Minnesota"
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
The following section describes the data accessible for Minnesota via the ClarityGov API. Note that the following page may be inaccurate, and should be used for quick reference only. Generated API docs are available [here](https://api.claritygov.com/docs/). 

## House
### Get Delegates 
Endpoint: `/mn/house/members`

Description: Returns a list of all delegates in the Maryland House of Delegates.

```python
from claritygov.services.legislators_service import get_state_house_members

# Returns a list of Delegate models. See claritygov.models.Delegate for more information on the model.
members = get_state_house_members('mn')
# Print out the list of Delegates.
print(members)
```

### Get Senators
Endpoint: `/mn/senate/senators`

Description:  Returns a list of senators.
