# Instructies voor Codex / ChatGPT en andere agents

Lees eerst CLAUDE.md en WORKSPACE.md in deze map; daar staan installatie, structuur en overdracht. Claude en Codex gebruiken dezelfde checkout (C:\DIN Code\<repositorynaam>); maak geen tweede kopie.

## Samenwerkregels (meerdere pc's, meerdere agents)

1. Begin met `git status --short --branch` en `git fetch origin`. Heb je lokale wijzigingen die je niet kent: stop en vraag het na.
2. Werk nooit tegelijk met twee agents of vanaf twee pc's op dezelfde branch of dezelfde bestanden.
3. Eén taak = één branch (`feat/...`, `fix/...`, `docs/...`). Nooit direct op de standaardbranch; geen force-push.
4. Haal updates op met `git pull --ff-only`.
5. Commit alleen bedoelde bestanden (`git add <bestanden>`), geen `git add -A`.
6. Push voor je stopt of van pc wisselt: `git push -u origin HEAD`. Chats worden niet door Git overgedragen.
7. Leg aan het einde in WORKSPACE.md (sectie "Overdracht") vast: branch, wijzigingen, uitgevoerde controles, resterend werk en benodigde lokale instellingen. Commit en push dat.
8. Geen geheimen, .env-bestanden, uploads of klantgegevens in Git. Die komen uit de wachtwoordmanager of de hosting.
