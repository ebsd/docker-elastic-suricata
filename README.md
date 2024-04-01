# docker-elastic-suricata

Ceci est une stack elastic - kibana - filebeat - suricata.
Le module suricata de filebeat est activé dans `filebeat/filebeat/modules.d/suricata.yml`.

Lire le fichier `.env` pour quelques configs.

## elastic et kibana

Le docker-compose.yml est basé sur :
https://github.com/elastic/elasticsearch/blob/main/docs/reference/setup/install/docker/docker-compose.yml

L'authorité de certification est partagée entre les différents conteneurs : elastic, kibana et filebeat.

## filebeat

Le fichier `filebeat/filebat.yml` doit être possédé par root.

Les logs du conteneur Suricata sont partagés avec le conteneur Filebeat via un volume :
`suricatadata:/var/log/suricata`.


