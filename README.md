# cacti_rrdclean_42
Cacti rrdclean 0.42 

When visiting http://cacti/plugins/rrdclean/rrdcleaner.php, [^] the following errors are logged to cacti.log:

CMDPHP: Poller[0] ERROR: SQL Assoc Failed!, Error:'1146', SQL:"SELECT plugin_rrdclean.id, plugin_rrdclean.name, plugin_rrdclean.last_mod, plugin_rrdclean.size, plugin_rrdclean.name_cache, plugin_rrdclean.local_data_id, plugin_rrdclean.data_template_id, plugin_rrdclean.data_template_name FROM (plugin_rrdclean) WHERE (plugin_rrdclean.name like '%%%%') OR (plugin_rrdclean.name_cache like '%%%%') OR (plugin_rrdclean.data_template_name like '%%%%') ORDER BY name ASC LIMIT 0,100"
CMDPHP: Poller[0] ERROR: SQL Cell Failed!, Error:'1146', SQL:"SELECT ROUND(SUM(plugin_rrdclean.size),2) FROM plugin_rrdclean WHERE (plugin_rrdclean.name like '%%%%') OR (plugin_rrdclean.name_cache like '%%%%') OR (plugin_rrdclean.data_template_name like '%%%%')"
CMDPHP: Poller[0] ERROR: SQL Cell Failed!, Error:'1146', SQL:"SELECT COUNT(plugin_rrdclean.name) FROM plugin_rrdclean WHERE (plugin_rrdclean.name like '%%%%') OR (plugin_rrdclean.name_cache like '%%%%') OR (plugin_rrdclean.data_template_name like '%%%%')"


As the error code states, plugin_rrdclean does not exist. No errors are logged into cacti.log when installing or enabling rrdclean.

SVN#2110 available as plugins/rrdclean/branches/v0.42

As per: http://bugs.cacti.net/view.php?id=2330

http://forums.cacti.net/viewtopic.php?f=19&t=41425&p=262240&hilit=plugin_rrdclean.name#p262240

The file has also been included here. 'thewizard' originally found the new file, I've just included this here for future ease of use.

fletch-jellyfish

#P.s. you will need to run this, on the folder when you move it into the plugins directory:
/cacti/plugins# chown -R cacti:cacti rrdclean/ 
