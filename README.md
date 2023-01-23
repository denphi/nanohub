# Nanohubtools

A set of tools/apps to run on nanohub

## Installation

```bashv
pip install nanohub
```

## Nanohub Remote


```python

import nanohub.remote as nr
auth_data = {
  'client_id': XXXXXXXX,
  'client_secret': XXXXXXXX,
  'grant_type': 'password',
  'username': XXXXXXXX,
  'password': XXXXXXXX
}

# to get username and password, register on nanohub.org (https://nanohub.org/register/)
# to get client id and secret, create a web application (https://nanohub.org/developer/api/applications/new), use "https://127.0.0.1" as Redirect URL

session = nr.Session(auth_data)

```

## Nanohub UIDL

```python

from nanohub.uidl.teleport import TeleportProject, TeleportElement
from nanohub.uidl.material import MaterialContent
from nanohub.uidl.auth import AUTH

Project = TeleportProject("My App")
Component = Project.root
Component.addStateVariable("myvariable", {"type":"boolean", "defaultValue": True})


```




