# eblon-ai-skills

Dépôt des six skills locaux Codex. Chaque skill possède son propre sous-dossier et son fichier `SKILL.md`.

- `architect_fr/`
- `aws-saa-eblon/`
- `aws-solution-architect/`
- `aws-solution-design/`
- `solution_adr/`
- `ui-ux-pro-max/`

Les skills système, archives ZIP et sauvegardes ne sont pas inclus.

Sur le Mac, les six skills actifs dans `~/.codex/skills/` sont des liens symboliques vers les sous-dossiers de ce dépôt. Les modifications locales et les mises à jour récupérées avec `git pull` sont donc directement disponibles dans les fichiers utilisés par Codex. Les anciennes copies sont sauvegardées hors du dossier de découverte, dans `~/.codex/skills-backups/`.

GitHub ne synchronise pas automatiquement les ordinateurs : publier les changements avec `git push`, puis les récupérer avec `git pull` sur l’autre machine. Chaque machine doit installer les skills ou configurer ses propres liens vers son clone local. Les liens du Mac ne sont pas versionnés dans ce dépôt. La configuration du PC Windows reste à effectuer. Ne pas déplacer le dépôt local sans mettre à jour les liens.

## Provenance de ui-ux-pro-max

Créateur : nextlevelbuilder. Source : https://github.com/nextlevelbuilder/ui-ux-pro-max-skill

Révision source : `4aad0584d92131626b16d4ff4d77f0455385013c`. Licence MIT conservée dans `ui-ux-pro-max/LICENSE`. Les commandes de SKILL.md résolvent le dossier réel du skill sur chaque machine et utilisent un interpréteur Python 3 disponible (macOS, Linux ou Windows).
