# Startup Agents — Textile Seconde Main

Squad d'agents Claude qui tournent en automatique chaque jour pour développer la startup.

## Architecture

| Agent | Horaire | Rôle | Draft Gmail |
|-------|---------|------|-------------|
| [Veille Seconde Main](agents/veille-seconde-main.json) | 8h00 | Tendances, concurrents, opportunités | `[VEILLE]` |
| [Contenu Marketing](agents/contenu-marketing.json) | 10h00 | Posts Instagram, Reels, newsletter, fiches produit | `[CONTENU]` |
| [Récap & Planning](agents/recap-planning.json) | 18h00 | Bilan du jour + priorités demain | `[RÉCAP]` |
| [Agent Commercial Prospection](agents/agent-commercial-prospection.json) | 9h00 lun-ven | Lit le Google Sheet, recherche LinkedIn, rédige messages | `[PROSPECT]` / `[PROSPECTION]` |
| [Veille B2B Senior](agents/veille-b2b-senior.json) | 7h00 lun-ven | Actualité marché, législation, tendances tech, mouvements concurrentiels, signaux faibles | `[VEILLE B2B]` |

## Mode supervisé

Tous les agents créent des **drafts Gmail uniquement** — rien n'est publié ou envoyé sans validation manuelle.

## Gérer les agents

- Interface web : https://claude.ai/code/scheduled
- Les `trigger_id` dans chaque JSON correspondent aux IDs dans l'interface

## Modifier un prompt

1. Éditer le fichier JSON dans `agents/`
2. Commiter sur GitHub
3. Mettre à jour le trigger via l'interface https://claude.ai/code/scheduled ou via l'API Claude Code
