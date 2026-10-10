# coturn — Nextcloud Talk

## Objectif

Fournir un relais TURN pour les communications audio et vidéo
de Nextcloud Talk.

## Environnement

- Système hôte : Ubuntu
- Déploiement : Docker Compose
- Réseau : IPv4 publique sur le VPS

## Ports

| Port | Protocole | Utilisation |
|------|-----------|-------------|
| 3478 | UDP | Connexion TURN |
| 3478 | TCP | Connexion TURN de secours |
| 49160-49200 | UDP | Relais multimédia |

## Configuration

1. Créer un fichier `.env` local.
2. Renseigner le domaine TURN et le secret.
3. Adapter turnserver.conf.
4. Vérifier les règles de pare-feu.
5. Démarrer le service avec Docker Compose.

## Sécurité

Les secrets réels ne sont pas versionnés.
Les flux vers les réseaux privés doivent être filtrés.

## Documentation

https://nextcloud-talk.readthedocs.io/en/stable/coturn/
