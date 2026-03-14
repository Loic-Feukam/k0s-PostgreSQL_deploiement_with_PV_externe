
# Déploiement de PostgreSQL sur Kubernetes avec stockage persistant NFS (stockage externe)

Pour garantir la persistance des données, un serveur NFS externe est utilisé comme backend de stockage.
Ce serveur NFS servant de backend de stockage a été déployé et configuré au préalable. 
Ainsi, les données de la base de donnée ne dépendent pas du cycle de vie du Pod Kubernetes. 



  **Architecture**


L’architecture repose sur les composants suivants :

* Un Pod PostgreSQL déployé dans Kubernetes (with single-node).

* Un PersistentVolume (PV).

* Un PersistentVolumeClaim (PVC).

* Un serveur NFS externe servant de stockage.
