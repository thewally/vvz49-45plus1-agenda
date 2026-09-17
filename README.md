# Speelagenda VVZ'49 45+ 1 7x7

Automatisch bijgewerkte agenda-feed (.ics) voor **VVZ '49 45+1** (7x7),
voor gebruik als abonnement in Google Calendar (of Apple/Outlook).

Fork van [vvz49-jo14-6-agenda](https://github.com/thewally/vvz49-jo14-6-agenda),
zonder de "Verzamelen"-items.

## Wat staat er in de agenda

- **Speeltijden**
- **Thuisteam - Uitteam**

## Hoe te gebruiken in Google Calendar

1. Ga naar https://calendar.google.com/calendar/r/settings/addbyurl
2. Plak de URL: `https://thewally.github.io/vvz49-45plus1-agenda/matches.ics`
3. Klik op **Agenda toevoegen**

De agenda wordt elke ochtend en avond automatisch bijgewerkt. Google
Calendar ververst de feed vervolgens op zijn eigen tempo (meestal binnen
12-24 uur).

## Achtergrond

Geen betaalde Voetbal.nl-app nodig: dit gebruikt de publieke widget-API
die VVZ'49's eigen website ook gebruikt om standen en programma te tonen.
Zie `scrape.py` voor details.

De Sportlink-widget `client_id` staat in de repository secret
`SPORTLINK_CLIENT_ID` (lokaal: zet 'm in de gelijknamige omgevingsvariabele)
-- niet in de code.

## Beperkingen

- Zoekt elke run automatisch de actuele teamcode/poule op, dus werkt door
  wanneer de KNVB halverwege het seizoen een nieuwe competitiefase indeelt.
