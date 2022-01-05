# Inleiding
## Doel en doelgroep

Dit document beschrijft een aantal Best Practices voor de DigiKoppeling Grote Berichten.

Het document is bestemd voor architecten en ontwikkelaars die op basis van DigiKoppeling Grote Berichten gegevens willen uitwisselen. Zie onderstaande tabel bij welke taken dit document ondersteunt. De koppelvlakstandaard Grote Berichten beschrijft verplichtingen voor het toepassen van Grote Berichten. Dit document is een aanvulling hierop en heeft tot doel ontwikkelaars te informeren en adviseren over de te volgen werkwijze bij het toepassen van de Koppelvlakstandaard Grote Berichten.

| Afkorting | Rol                             | Taak                                                                                                       | Doelgroep? |
| --- |---------------------------------| --- |------------|
| [MT]      | Management                      | Bevoegdheid om namens organisatie (strategische) besluiten te nemen.                                       | **Nee**    |
| [PL]      | Projectleiding                  | Verzorgen van de aansturing van projecten.                                                                 | **Nee**    |
| [A&D]     | Analyseren & ontwerpen (design) | Analyseren en ontwerpen van oplossings-richtingen. Het verbinden van Business aan de IT.                   | **Nee**    |
| [OT&B]    | Ontwikkelen, testen en beheer   | Ontwikkelt, bouwt en configureert de techniek conform specificaties. Zorgen voor beheer na ingebruikname.  | **Ja**     |

## Opbouw Digikoppeling documentatie

Digikoppeling is beschreven in een set van documenten. Deze set is als volgt opgebouwd:


![Overzicht van de onderdelen van de Digikoppeling Standaard, de standaard is onderverdeeld in normatieve en ondersteunende onderdelen](https://publicatie.centrumvoorstandaarden.nl/alg/media/DK_Specificatie_structuur.svg "Opbouw documentatie Digikoppeling")




## Doel en scope van Digikoppeling

DigiKoppeling biedt de mogelijkheid om op een sterk gestandaardiseerde wijze berichten uit te wisselen tussen service aanbieders en service afnemers. De uitwisseling tussen partijen wordt in drie lagen opgedeeld:

- Inhoud: Op deze laag worden de afspraken gemaakt over de inhoud van het uit te wisselen bericht, dus de structuur, semantiek en waardebereiken.  
    DigiKoppeling houdt zich **niet** met de inhoud bezig, ‘heeft geen boodschap aan de boodschap’.

- Logistiek: Op deze laag bevinden zich de afspraken betreffende transportprotocollen (HTTP), messaging (SOAP), beveiliging (authenticatie en encryptie) en betrouwbaarheid. **Dit is de DigiKoppeling-laag.**

- Transport: deze laag verzorgt het daadwerkelijke transport van het bericht.

DigiKoppeling richt zich dus uitsluitend op de logistieke laag. Deze afspraken staan in de koppelvlakstandaards en andere voorzieningen. In het geval van WUS en ebMS2 komt de logistieke laag overeen met de ‘header’ van het bericht en gaat de ‘body’ uitsluitend over de inhoud. In het geval van Digikoppeling Grote Berichten is een deel van de logistieke informatie opgenomen in de ‘body’ van het bericht in de vorm van gestandaardiseerde meta-data.

### Leidend principe

De koppelvlakstandaarden dienen te leiden tot een maximum aan interoperabiliteit met een minimum aan benodigde ontwikkelinspanning. Daarom wordt gekozen voor bewezen interoperabele internationale standaarden.

DigiKoppeling maakt berichtenuitwisseling mogelijk op basis van de ebXML/ebMS2 en WUS families van standaarden inclusief de daarbij behorende verwante standaarden.

Aan te sluiten overheidsorganisaties hebben aangegeven op een uniforme manier (één stekker) te willen aansluiten aan DigiKoppeling. Organisaties die beschikken over eigen middleware (ESB, broker) kunnen de aansluiting aan DigiKoppeling, de adapters, in het algemeen realiseren via voorzieningen in die middleware.

## Koppelvlak & koppelvlakstandaard

Een koppelvlak is een interface die volgens vergaande standaards de gegevensuitwisseling verzorgt. Het werken met vaste standaards is essentieel voor een koppelvlak. Hierdoor wordt implementatie vergemakkelijkt. Ook wordt het mogelijk diverse soorten berichten door te sturen met een grote mate van interoperabiliteit.

Eén van de belangrijkste eisen die door de overheid gesteld wordt bij de inrichting van generieke voorzieningen is dat er niet veel maatwerk ontwikkeld hoeft te worden, maar dat er van “off the shelf” commercieel of OPEN geleverde software gebruik gemaakt kan worden. Voor DigiKoppeling, dus voor de logistieke laag, betreft dat het niet willen ontwikkelen van software voor de adapters.

Dit doel kan bereikt (benaderd) worden doordat gekozen wordt voor internationale (de jure of de facto) vastgelegde standaards, die door “alle” leveranciers interoperabel zijn geïmplementeerd. Ingeval van Grote Berichten is gebruik gemaakt van een optioneel deel uit de http 1.1 standaard. Hierdoor is het mogelijk om de overdracht te hervatten op het punt van afbreken door een toevallige storing. Zowel standaard servers als clients ondersteunen dit, maar aan de client kant moet de optie ook expliciet gebruikt worden.

Een andere eis is dat met name afnemers gebruik kunnen maken van één “stekker” (één logistiek koppelpunt).

### Specificatie van de koppelvlakstandaard

De koppelvlakspecificatie beschrijft de eisen waar de adapters aan moeten

voldoen om interoperabel met elkaar te kunnen communiceren.

DigiKoppeling gaat over logistiek, dus over de envelop en niet over de

inhoud. De hele set info die tezamen nodig is voor een complete generieke

DigiKoppeling koppelvlakdefinitie (Raamwerk Specificatie genoemd)

bestaat uit:

- interfacedefinitie “on the wire”, (voorbeeld)listing van SOAP headers, en

- informatie over velden en hun specifieke inhoud.

## Opbouw van dit document

Hoofdstuk 1 bevat een aantal algemene inleidende onderwerpen. Hoofdstuk 2 beschrijft de Best Practices voor verschillende scenario's. Hoofdstuk 3 ten slotte bevat generieke use-cases waarin van deze standaard gebruik gemaakt kan worden.

Begrippen en afkortingen worden toegelicht in het document “Digikoppeling_Architectuur”. Deze zit in de Digikoppeling aansluitkit.

Dit document en andere documentatie is beschikbaar op [www.logius.nl/digikoppeling](http://www.logius.nl/digikoppeling)
