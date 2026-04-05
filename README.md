# Startup Agents — Textile Seconde Main

Squad d'agents Claude qui tournent en automatique chaque jour pour développer la startup.

## Architecture

| Agent | Horaire | Rôle | Draft Gmail |
|-------|---------|------|-------------|
| [Veille Seconde Main](agents/veille-seconde-main.json) | 8h00 | Tendances, concurrents, opportunités | `[VEILLE]` |
| [Contenu Marketing](agents/contenu-marketing.json) | 10h00 | Posts Instagram, Reels, newsletter, fiches produit | `[CONTENU]` |
| [Récap & Planning](agents/recap-planning.json) | 18h00 | Bilan du jour + priorités demain | `[RÉCAP]` |

## Mode supervisé

Tous les agents créent des **drafts Gmail uniquement** — rien n'est publié ou envoyé sans validation manuelle.

## Gérer les agents

- Interface web : https://claude.ai/code/scheduled
- Les `trigger_id` dans chaque JSON correspondent aux IDs dans l'interface

## Modifier un prompt

1. Éditer le fichier JSON dans `agents/`
2. Commiter sur GitHub
3. Mettre à jour le trigger via l'interface https://claude.ai/code/scheduled ou via l'API Claude Code
