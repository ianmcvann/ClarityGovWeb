---
title: "Quick Start"
description: "One page summary of how to start a new Doks project."
lead: "One page summary of how to start a new Doks project."
date: 2020-11-16T13:59:39+01:00
lastmod: 2020-11-16T13:59:39+01:00
draft: false
images: []
menu:
  docs:
    parent: "prologue"
weight: 110
toc: true
---

## Requirements

- [Python3](https://www.python.org/downloads/) — 3.7 or newer
- pip3 — Python package manager, usually included in install.

## Start interacting with the ClarityGov API

### Install the ClarityGov Python client via PIP

```bash
pip3 install claritygov
```

### Create a new ClarityGov client and return all Maryland House Members


```python
from claritygov.api.state import State
from claritygov.api_client import ClarityAPIClient
from claritygov.api.house import House

api_client = ClarityAPIClient()
state = State(api_client, 'Maryland')
house = House(state)
members = house.get_house_members()
print(members)
```