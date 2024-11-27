# Access-list and Object Group processing role

## Introduction
This role takes as input text files containing access-lists and object-group configurations.  They are parsed and then applied to the device.  Additions, subtractions, and modifications 

## Role Variables

| variable | description | default |
|----------|-------------|---------|
| _obj_files | List of files containing object-group configurations | none |
| _acl_files | List of files containing access-list configurations | none |

### Note regarding object-groups:
Ansible does not currently have a module for Cisco IOS object groups.  They are processed using a textfsm template to turn them into structured data.  This is then applied to the device.  If a change is necessary, the entire object-group is removed and replaced.

# License

```
Copyright (c) 2024 Peter Bruno <peter.e.bruno@faa.gov>

Permission to use, copy, modify, and distribute this software for any
purpose with or without fee is hereby granted, provided that the above
copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR
ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN
ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF
OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
```

### Author Information
Peter Bruno, 2024