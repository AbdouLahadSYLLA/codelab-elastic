## FileBeat

Positive
: Voici la documentation utile pour cette étape
  * [Documentation de FileBeat](https://www.elastic.co/guide/en/beats/filebeat/current/index.html) 

Nous allons à présent activer **Filebeat** afin d'indexer et visualiser les logs générés par **NGINX** et par **Kibana**

Afin de configurer Filebeat, vous devez modifier le fichier disponible dans l'image fournie ; `/etc/filebeat/filebeat.yml`

- Faites les modifications nécessaires pour activer `Filebeat` dans notre solution:
  - Activer la sortie Elasticsearch
  - Configurer la connexion avec Kibana
  - Activer le module `nginx`
  - Indexer les logs générées par Kibana. (les logs se situent dans `/var/log/kibana/kibana.log`)
  - Activer le monitoring, afin de monitorer vos agents `Filebeat` (paramètre `xpack.monitoring.enabled`)

- Démarrer Filebeat :
```
cd /elastic-stack
ansible-playbook 4_configure-filebeat.yml
```
- Visualiser les données depuis Kibana, ainsi que les dashboards automatiquement crées pour Nginx. 

### Étape suivante

[PacketBeat](https://github.com/Gillespie59/codelab-elastic/tree/devfest-nantes/steps/step3.md)