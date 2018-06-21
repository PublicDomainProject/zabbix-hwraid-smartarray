# HP Smart Array RAID controller monitoring extension

## Check:
- controller, cache, battery health
- logical volumes health
- physical drives health and temperature
- auto-discovery and agentd-side send data procedure

## Installation notes:
1. Install the [`zabbix.smartarray`](zabbix.smartarray) cron job into `/etc/cron.d`
2. Install the [`hp-raid-smart-array.conf`](hp-raid-smart-array.conf) Zabbix user
   parameters into your Zabbix agent's
   [`Include`](https://www.zabbix.com/documentation/3.0/manual/appendix/config/zabbix_agentd)
   directory (usually `/etc/zabbix/zabbix_agentd.d`).
3. Import the [`hp-smart-array-template.xml`](hp-smart-array-template.xml) into
   your Zabbix server.
4. Add the template to your host (or stack template)
5. Check if new data arrives


## Tested on:
- HP Smart Array P410
- HP Smart Array P222

- cache and battery may NOT shows on P410;
- some drives models may not show temperature (Seagate).
