# Une app par semaine

**Une application par semaine, codée avec l'IA. 100 % locale. Auditée en sécurité. Code ouvert.**

Chaque semaine, je conçois, je teste et je publie une application construite avec Claude et Claude Code. Tout se passe en public : le cadrage, les maquettes, les prompts, l'audit de sécurité et les erreurs de l'IA, y compris les miennes.

Le but : montrer qu'on peut vibe coder vite **et** proprement.

## Les règles de la série

| Règle | Ce que ça veut dire pour vous |
| --- | --- |
| 100 % locale | Aucun serveur, aucun compte, aucune donnée qui quitte votre appareil. Chaque version est testée sur une machine déconnectée. |
| Auditée | Chaque app passe un audit de sécurité par IA (posture d'attaquant, OWASP Top 10) et des outils automatiques. Le rapport est publié dans `AUDIT.md`. |
| Vérifiable | Les exécutables sont construits par GitHub Actions, jamais sur ma machine, et publiés avec leurs empreintes SHA-256. |
| Transparente | Les prompts clés et les décisions sont dans `PROMPTS.md`. La charte et les maquettes sont dans `design/`. |
| Ouverte | Code source sous licence MIT. |

## Les applications

| Semaine | Application | Format | Pour qui | Dépôt |
| --- | --- | --- | --- | --- |
| S1 | [Nom] — suivi des présences | PWA hors ligne | Clubs et associations | [lien] |
| S2 | [Nom] — dédoublonnage et rangement de photos par LLM local | Desktop | Tout le monde | [lien] |
| S3 | [Nom] — minuteur d'entraînement par intervalles | Android | Sportifs et professeurs | [lien] |
| S4 | Choisie par la communauté | — | — | — |

## La méthode, en 7 étapes

1. **Cadrer** : le besoin, l'utilisateur, les données, ce qui est hors périmètre.
2. **Designer** : charte graphique et maquettes, validées avant la première ligne de code.
3. **Générer** : Claude Code, guidé par un fichier `CLAUDE.md` qui fixe les règles.
4. **Tester** : pas de fonctionnalité sans son test.
5. **Auditer** : une session d'IA séparée joue l'attaquant, puis Semgrep, CodeQL, gitleaks et l'audit des dépendances prennent le relais.
6. **Corriger** : chaque problème trouvé est corrigé et documenté.
7. **Publier** : dépôt, release vérifiable, démo.

Le dépôt [`app-template`](https://github.com/une-app-par-semaine/app-template) contient tout ce point de départ : `CLAUDE.md`, prompt d'audit, checklist de release, workflows de sécurité. Servez-vous.

## Vérifier un téléchargement

Dans la page Releases de chaque app, téléchargez le fichier et `SHA256SUMS.txt`, puis :

```bash
sha256sum -c SHA256SUMS.txt --ignore-missing
```

Sous Windows (PowerShell) : `Get-FileHash .\fichier.exe -Algorithm SHA256`, puis comparez avec la ligne du fichier.

## Proposer la prochaine app

À partir de la semaine 4, les apps sont choisies parmi vos idées. Proposez la vôtre en commentaire de mes posts LinkedIn. Une seule condition : elle doit pouvoir tourner 100 % en local. L'auteur de l'idée retenue est cité.

## Signaler une faille

Utilisez le bouton **Report a vulnerability** de l'onglet Security du dépôt concerné. Merci de ne pas ouvrir d'issue publique pour une faille.

---

Par [Dimitri Lefebvre](https://www.linkedin.com/in/dimlefebvre60) · Je prends aussi des missions : applications sur mesure, audit de code généré par IA, formation au vibe coding maîtrisé.
