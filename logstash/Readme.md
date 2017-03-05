# Logstash (ELK Stack) Stuff

[logstash/filebeat.geopoint.template.json](https://github.com/thedonvaughn/elk/blob/master/logstash/filebeat.geopoint.template.json)
 - filebeat index template for Logstash to include a geo_point type.  This allows you to use tile map.
 - Compat with version 5.2.x
 - Fixes: The "filebeat-*" index pattern does not contain any of the following field types: geo_point

### To use:

Assuming your logstash server can be reached at http://localhost:9200 

- [user@localhost]$ curl -XPUT 'http://localhost:9200/_template/filebeat?pretty' -d@/path/to/filebeat.geopoint.template.json
