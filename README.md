Install INDIGO-DC Virtual Router.
===========================================================================

Install INDIGO-DC Virtual Router [1].


Role Variables
--------------

Description of all the variables that can be passed to this role is along their default values in defaults/main.yml.

Example Playbook
----------------

This an example of how to install the application:

In the "vrouter" node:
```yml
  roles:
  - role: indigo-dc.indigovr
    INDIGOVR_NODE_TYPE: vrouter
    INDIGOVR_CENTRALPOINT_IP: 'centralpoint_ip'
```

In the "standalone" node:
```yml
  roles:
  - role: indigo-dc.indigovr
    INDIGOVR_NODE_TYPE: standalone
    INDIGOVR_CENTRALPOINT_IP: 'centralpoint_ip'
```

In the "centralpoint" node:
```yml
  roles:
  - role: indigo-dc.indigovr
    INDIGOVR_NODE_TYPE: 'centralpoint'
```

License
-------

Apache Licence v2 [2]

[1] https://github.com/CESNET/IndigoVR

[2] http://www.apache.org/licenses/LICENSE-2.0

