---
title: Containment
weight: 3
---

La cellule de crise devrait décider et suivre les actions suivantes :

1. Déconnecter d'Internet le périmètre infecté.
2. Isoler le périmètre infecté, le déconnecter de tout réseau.
3. Si des systèmes critiques pour la poursuite de l'activité métier ne peuvent être déconnectés, les laisser en place après s'être assuré qu'ils ne peuvent constituer un vecteur d'infection ou appliquer des méthodes de contournement éprouvées.
4. Neutraliser les vecteurs de propagation, ceux-ci pouvant être n'importe quoi, du trafic réseau à la faille logicielle. Des contre-mesures adaptées peuvent être prises (correctifs, blocage de trafic, désactivation d'équipements...), comme les techniques suivantes :

   - Utilitaire de déploiement des correctifs (WSUS),
   - Politiques de groupes Windows (GPO),
   - Règles de pare-feux,
   - Procédures opérational.

5. Répeter les étapes 2 à 4 sur chaque sous-périmètre infecté jusqu'à l'arrêt de la prolifération du ver. Dans la mesure du possible, suivre l'infection avec des outils d'analyse (console antivirale, journaux des serveurs, appels au support).

La prolifération du ver doit être suivie.

### Périphériques mobiles

S'assurer qu'aucun ordinateur portable, PDA ou périphérique de stockage amovible ne peut être utilisé comme vecteur de propagation du ver. Dans la mesure du possible, bloquer toutes leurs connexions.

Demander aux utilisateurs de suivre scrupuleusement les consignes.

À la fin de cette étape, l'infection devrait être engiguée.
