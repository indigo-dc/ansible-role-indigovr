Install INDIGO-DC Virtual Router.
===========================================================================

Install INDIGO-DC Virtual Router [1]. The INDIGO-DC Virtual Router does not carry its own code. It consists of open components and all automation is contained in Ansible roles.

The purpose of the INDIGO-DC Virtual Router is establishing an overlay virtual private network to interconnect nodes in a cloud platofrm deployment even if deployed in multiple, geographically distant sites.


Getting Started
---------------
The roles are intended for automated deployment through the Infrastructure Manager [2]. They can be deployed manually with Ansible if required. Follow to section _Example Playbook_ for that.

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


Testing
-------

Automated testing framework for this component is not available.


Contributing
------------

Contributors are welcome. Contributions are accepted through GitHub's _Pull Request_ and _Review_ process.


Authors
-------

Martin Pustka: https://github.com/pumacze

Milan Ševčík: https://github.com/Majlen

Miguel Caballer: https://github.com/micafer

CESNET: https://github.com/CESNET

DEEP Hybrid-DataCloud: https://deep-hybrid-datacloud.eu

License
-------

Apache Licence v2 [3]

Acknowledgments
---------------

This work is being developed within the DEEP Hybrid-DataCloud project, funded from the European Union’s Horizon 2020 research and innovation programme under grant agreement No 777435.


References
----------

[1] https://github.com/CESNET/IndigoVR

[2] https://github.com/indigo-dc/im

[3] http://www.apache.org/licenses/LICENSE-2.0

