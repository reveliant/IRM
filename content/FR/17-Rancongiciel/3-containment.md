---
title: Containment
weight: 3
---
- Déconnecter du réseau tous les systèmes qui ont été identifiés comme compromis
- Si le système ne peut être isolé, déconnecter tous les disques partagés (`NET USE x: \\unc\path\ /DELETE`)
- Bloquer le trafic vers les serveurs C&C du rançongiciel identifié
- Envoyer les échantillons non détectés au fournisseur de la solution de sécurité du poste de travail
- Envoyer les URL, noms de domaines et adresses IP non catégorisés comme malveillant au fournisseur de la solution de sécurité périmétrique
