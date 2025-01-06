---
title: Team
nav:
  order: 2
  tooltip: About our team
---

# {% include icon.html icon="fa-solid fa-users" %}Team

<!-- Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. -->
## Professor

{% include list.html data="members" component="portrait" filter="role == 'prof'" %}



## PhD Students

{% include list.html data="members" component="portrait" filter="role == 'phd'" %}

## Undergraduate Students

{% include list.html data="members" component="portrait" filter="role == 'undergrad'" %}