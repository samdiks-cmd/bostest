# bostest — werkmap en overdracht

GitHub: https://github.com/samdiks-cmd/bostest

Windows-werkmap: `C:\DIN Code\bostest`. Standaardbranch: `main`.

## Lokaal starten en structuur

Placeholder/testrepository; bij inventarisatie op 4 oktober 2026 geen applicatiecode aangetroffen. Het werkende Business OS-project staat in samdiks-cmd/businessOSv2. Deze repository wordt bewaard als apart project; geen installatie- of startcommando zolang er geen applicatie is.

## Werken vanaf meerdere pc's

Gebruik op Windows C:\DIN Code\<repositorynaam>; op andere systemen een lokale projectmap buiten Google Drive/OneDrive. Elke projectmap is een eigen Git-repository. GitHub bewaart code en commits; lokale instellingen, dependencies en runtime-data worden per pc ingericht.

Begin met `git status --short --branch` en `git fetch origin`. Ga alleen met een schone werkmap naar de gewenste branch. Haal updates op met `git pull --ff-only`. Gebruik voor nieuwe taken een eigen branch, bijvoorbeeld `git switch -c feat/omschrijving`.

Controleer voor vertrek `git diff`, commit alleen bedoelde bestanden met `git add <bestanden>` en `git commit -m "Beschrijving"`. Push de werkbranch met `git push -u origin HEAD`, ook wanneer de taak nog niet af is. Haal op de andere pc dezelfde branch op met `git fetch origin` en `git switch --track origin/<branch>` (of `git switch <branch>` als die lokaal bestaat), gevolgd door `git pull --ff-only`. Werk niet gelijktijdig op dezelfde branch vanaf twee pc's.

Wijzigingen op een werkbranch komen via een pull request terug op de standaardbranch. Respecteer bestaande review- en CI-regels. Vermijd force-pushes. Git synchroniseert geen niet-gecommitteerde bestanden.

## Overdracht tussen Codex en Claude

Open Claude Code in deze projectmap en lees eerst CLAUDE.md, eventuele AGENTS.md en deze handleiding. Gebruik dezelfde checkout als Codex; maak geen tweede kopie in een AI-specifieke map. Werk niet tegelijk in dezelfde bestanden. Controleer bestaande lokale wijzigingen voordat je verdergaat.

Werk aan het einde van een sessie een taakoverdracht bij met de branch, uitgevoerde wijzigingen, controles en resterend werk. Commit en push die overdracht op de werkbranch; een losse chat wordt niet door Git gesynchroniseerd.

## Instellingen en gegevens

Neem geheimen over via een wachtwoordmanager. Voorbeeldconfiguraties bevatten alleen placeholders. .gitignore voorkomt nieuwe toevoegingen; reeds gecommitteerde gegevens of geheimen worden er niet uit de geschiedenis mee verwijderd. Productiedata, uploads en live CMS-inhoud horen bij de hosting en worden niet overschreven bij een code-deploy. Gebruik Google Drive voor documenten en gedeelde bronbestanden, niet voor de actieve Git-checkout of dependencies.

## Overdracht van Codex — 4 oktober 2026

De repository is geïnventariseerd en lokaal gekloond in de genoemde map. Deze wijziging voegt documentatie voor meerdere pc's en een ingang voor Claude toe. Bestaande applicatiecode, deployment, productiegegevens en standaardbranch zijn niet heringericht. Dependencies zijn nog niet geïnstalleerd; applicatie/buildtests zijn niet uitgevoerd voor deze documentatiewijziging.

Volgende stap bij een nieuwe taak: controleer de actuele Git-status, branch, bestaande projectinstructies en benodigde lokale configuratie. Raadpleeg de pull request voor de status van deze documentatiewijziging.
