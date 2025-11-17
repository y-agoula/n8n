# Weerbericht en smoes-generator om niet naar school te gaan
Dagelijks een weerbericht met een smoes om niet naar school te gaan. Bij regen krijg je een herinnering dat je de juiste keuze hebt gemaakt. Is het zonnig? (wat het nooit is in Nederland) Dan is het tijd om naar buiten te gaan, maar niet naar school he! 🌦️😆

##  Over dit project
Dit n8n-project combineert een dagelijks weerbericht met een unieke smoes-generator en extra meldingen via e-mail en Discord.

- Dagelijks een creatief weerbericht in verhaalvorm.
- Smoes-generator – Krijg een originele reden waarom je vandaag niet naar school hoeft. 
- Regenmelding – Een herinnering als het regent, zodat je weet dat je de juiste keuze hebt gemaakt om thuis te blijven. 
- Stormmelding – Waarschuwing als de wind 70 km/u of harder is. 
- Zonnemelding – Notificatie bij mooi weer, zodat je weet dat het tijd is om naar buiten te gaan. 

Alle meldingen worden verzonden via e-mail en Discord. 

## Functionaliteiten
- Automatische Weerupdates – Haalt actuele weerdata op via de OpenWeather API.
- AI Smoes-Generator – Laat ChatGPT een smoes bedenken op basis van het weer.
- Waarschuwingen voor Extreem Weer – Regen-, storm- en zonnemeldingen.
- E-mail & Discord Notificaties – Dagelijkse updates rechtstreeks in je inbox of Discord-kanaal.
- Supabase Database – Gebruik PostgreSQL in de cloud voor opslag.
- Docker Deployment – Draai n8n eenvoudig via Docker.
- Ngrok Integratie – Externe toegang tot je n8n instance via een beveiligde tunnel.

## Technologieën
- n8n – Workflow automation
- Docker – Voor eenvoudige installatie en uitvoering
- Supabase (PostgreSQL) – Cloud database voor opslag
- OpenWeather API – Haalt weergegevens op
- ChatGPT API – Genereert creatieve smoesjes
- Ngrok – Zorgt voor externe toegang tot je n8n-instance
- E-mail & Discord Webhooks – Versturen van meldingen


## Installatie & Gebruik
1. Clone de repository:
````bash
git clone https://github.com/YYSSSFF/n8n.git
````
2. Start n8n (Docker of lokaal):
``` bash
winpty (als je Windows gebruikt) docker run -it --rm \
 --name n8n \
 -p 5678:5678 \
 -e DB_TYPE=postgresdb \
 -e DB_POSTGRESDB_DATABASE=postgres \
 -e DB_POSTGRESDB_HOST=<SUPBASE_HOST_PARAMETER> \
 -e DB_POSTGRESDB_PORT=5432 \
 -e DB_POSTGRESDB_USER=<SUPABASE_USER_PARAMETER> \
 -e DB_POSTGRESDB_SCHEMA=public \
 -e DB_POSTGRESDB_PASSWORD=<SUPABASE_DATABASE_PASSWORD> \
 -e N8N_ENCRYPTION_KEY=<ENCRYPTION_KEY> \
 docker.n8n.io/n8nio/n8n
```
3. Importeer de n8n workflow JSON en stel je API-keys in (OpenWeather & ChatGPT).
4. Voeg je e-mail en Discord-webhook toe in de workflow.
5. Geniet van dagelijkse weerupdates met een twist!

## License
Dit project is gelicenseerd onder de MIT License – Gebruik, wijzig en deel het vrij!
