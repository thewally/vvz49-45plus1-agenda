# VVZ '49 45+1 agenda

Automatisch bijgewerkte agenda-feed (.ics) voor **VVZ '49 45+1** (7x7),
voor gebruik als abonnement in Google Calendar (of Apple/Outlook).

Fork van [vvz49-jo14-6-agenda](https://github.com/thewally/vvz49-jo14-6-agenda),
zonder de "Verzamelen"-items -- hier staan alleen de wedstrijden zelf in
de agenda.

Geen betaalde Voetbal.nl-app nodig: dit gebruikt de publieke widget-API
die VVZ'49's eigen website ook gebruikt om standen en programma te tonen.
Zie `scrape.py` voor details.

## Hoe toevoegen aan Google Calendar

1. Ga naar https://calendar.google.com/calendar/r/settings/addbyurl
2. Plak de URL naar `matches.ics` in deze repo (raw.githubusercontent.com-
   of GitHub Pages-link)
3. Klik op **Agenda toevoegen**

De agenda wordt elke ochtend en avond automatisch bijgewerkt via GitHub
Actions (`.github/workflows/update.yml`); Google Calendar ververst de feed
vervolgens op zijn eigen tempo (meestal binnen 12-24 uur).

## Configuratie

De Sportlink-widget `client_id` staat in de repository secret
`SPORTLINK_CLIENT_ID` (lokaal: zet 'm in de gelijknamige omgevingsvariabele)
-- niet in de code, om te voorkomen dat hij publiek in de git-historie
terechtkomt.

## Beperkingen

- Zoekt elke run automatisch de actuele teamcode/poule op, dus werkt door
  wanneer de KNVB halverwege het seizoen een nieuwe competitiefase indeelt.
