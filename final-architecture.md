
|Problème|Conséquence|Solution|
| :--- | :--- | :--- |
| Postgres dans le même conteneur que l'API | Suppression des données a chaque nouveau pod | Séparer les deux avec StatefulSet et PVC |
| pas de readiness/liveness probes | Perdition du trafic | probes sur /health |
| Pas de request/limit | Affamation du nœud par un pod gourmant | Request/limits CPU et mémoire |

