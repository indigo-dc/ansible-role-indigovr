Install INDIGO-DC Virtual Router.
===========================================================================

Install INDIGO-DC Virtual Router [1].


Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

	# Node type it can be vrouter or centralpoint
	INDIGOVR_NODE_TYPE: vrouter
	# In case of vrouter node the IP of the centralpoint
	INDIGOVR_CENTRALPOINT_IP: 10.0.0.1
	# Node certificate
	INDIGOVR_CERT: |
	    -----BEGIN CERTIFICATE-----
	    -----END CERTIFICATE-----
	# Node key
	INDIGOVR_KEY:  |
	    -----BEGIN PRIVATE KEY-----
	    -----END PRIVATE KEY-----
	# CA certificate
	INDIGOVR_CA: | 
	    -----BEGIN CERTIFICATE-----
	    -----END CERTIFICATE-----


Example Playbook
----------------

This an example of how to install the application:

In the "vrouter" node:
```yml
  roles:
    - { role: 'indigo-dc.indigovr', INDIGOVR_CENTRALPOINT_IP: 'centralpoint_ip'}
```

In the "centralpoint" node:
```yml
  roles:
    - { role: 'indigo-dc.indigovr', INDIGOVR_NODE_TYPE: 'centralpoint' }
```

License
-------

Apache Licence v2 [2]

[1] https://github.com/CESNET/IndigoVR

[2] http://www.apache.org/licenses/LICENSE-2.0

