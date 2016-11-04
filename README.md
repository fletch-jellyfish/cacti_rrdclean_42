# cacti_rrdclean_42
Cacti rrdclean 0.42 

When visiting http://cacti/plugins/rrdclean/rrdcleaner.php, [^] the following errors are logged to cacti.log:

CMDPHP: Poller[0] ERROR: SQL Assoc Failed!, Error:'1146', SQL:"SELECT plugin_rrdclean.id, plugin_rrdclean.name, plugin_rrdclean.last_mod, plugin_rrdclean.size, plugin_rrdclean.name_cache, plugin_rrdclean.local_data_id, plugin_rrdclean.data_template_id, plugin_rrdclean.data_template_name FROM (plugin_rrdclean) WHERE (plugin_rrdclean.name like '%%%%') OR (plugin_rrdclean.name_cache like '%%%%') OR (plugin_rrdclean.data_template_name like '%%%%') ORDER BY name ASC LIMIT 0,100"
CMDPHP: Poller[0] ERROR: SQL Cell Failed!, Error:'1146', SQL:"SELECT ROUND(SUM(plugin_rrdclean.size),2) FROM plugin_rrdclean WHERE (plugin_rrdclean.name like '%%%%') OR (plugin_rrdclean.name_cache like '%%%%') OR (plugin_rrdclean.data_template_name like '%%%%')"
CMDPHP: Poller[0] ERROR: SQL Cell Failed!, Error:'1146', SQL:"SELECT COUNT(plugin_rrdclean.name) FROM plugin_rrdclean WHERE (plugin_rrdclean.name like '%%%%') OR (plugin_rrdclean.name_cache like '%%%%') OR (plugin_rrdclean.data_template_name like '%%%%')"


As the error code states, plugin_rrdclean does not exist. No errors are logged into cacti.log when installing or enabling rrdclean.
