---
title: "Data Standards"
description: ""
lead: ""
date: 2023-07-21T16:47:53-05:00
lastmod: 2023-07-21T16:47:53-05:00
draft: false
images: []
menu:
  docs:
    parent: "advanced"
weight: 999
toc: true
---

Standardized data formats are used throughout the ClarityGov API as much as possible. This section describes general notes about the data formats used in the API. State specific notes are available as applicable under each state section.

### Names

Names are tricky from a data collection standpoint. There are many different ways to represent names, and many different ways to represent the same name. For example, the name "John Smith" could be represented as:

- "John Smith"
- "Smith, John"
- "John A. Smith"
- "John A Smith"

and so on.

The ClarityGov API saves names in a standardized format in JSON with the following fields:

- `first_name`: The first name of the person. If this is initials, the initials should be separated by periods and spaced in between. For example "C. J. Smith" instead of "C.J. Smith". This name may also include a middle name if that name is represented in the source data as a first name. For example, if the source data has "J. Albert Smith", then the `first_name` field will contain "J. Albert".
- `last_name`: The last name of the person. Due to the way our data is stored, accents and other special characters are not supported in this field. For example, "García" will be stored as "Garcia". We are working to add this support in the future.
- `full_name` The full name of the person. This field is not used for matching, and is only included for convenience. It may include any applicable middle initials. For example, "John A. Smith" would be stored as "John A. Smith".