# riak-zabbix
Zabbix template and setup guide to monitor Riak

1. Install these crontabs under the riak user

	```
    * * * * * /usr/sbin/riak-admin status > /var/lib/riak/riak_admin_status.tmp
	```

1. Deploy the attached `riak.conf` to `/etc/zabbix/zabbix_agentd.d/`

1. Import the attached `zbx_export_templates.xml` into Zabbix 2.x and apply to the relevant hosts and or groups