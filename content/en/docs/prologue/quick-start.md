---
title: "Quick Start"
description: "One page summary of how to start a new Doks project."
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
from claritygov.services.legislators_service import get_state_house_members

# Returns a list of Delegate models. See claritygov.models.Delegate for more information on the model.
members = get_state_house_members('md')
# Print out the list of Delegates.
print(members)
```