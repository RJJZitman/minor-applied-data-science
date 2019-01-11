# minor-applied-data-science

Dit is het portfolio van Rogier Zitman m.b.t. het Ortho Eyes project, onderdeel van de minor Applied Data Science KB-74. In dit portfolio is opgenomen wat ik gedurende het Ortho-eyes project heb gedaan. Dit project is uitgevoerd met Dr. Tony Andrioli en drie medestudent: Kasper van der Hoofd, Luke de Keijzer en Vincent den Oord. 

Ortho-eyes is onderdeel van een onderzoek door Dr. Andrioli voor Dr. ir. J.H. (Jurriaan) de Groot, werkzaam bij het Leids Universitair Medisch Centrum (LUMC). 
 

# Dit portfolio is in de volgende wijze opgebouwd: 

**-Online cursussen**

**-Jargon**

**-Algemene wiskunde**

**-Het project**

**-Presentaties**

**-Mijn bijgrdage aan het paper**

**-Literatuur**

**-Overig**


## **-[Online cursussen](https://github.com/RJJZitman/minor-applied-data-science/issues/8#issue-398013713)**

Gedurende deze minor heb ik een aantal online cursussen gevolgd in python voor data science en machine learning. De python cursussen heb ik gedaan op Datacamp, leuk om te zien is dat ik er meer heb gedaan dan minimaal nodig. Screenshots waar de afgemaakte cursussen zijn afgebeeld vindt u [hier](https://github.com/RJJZitman/minor-applied-data-science/issues/1#issue-397295969).

Voor machine learning heb ik een deel van de andrew NG course op coursera gevolgd. Hier had ik relatief veel moeite mee. Daarom heb ik ook hier een week meer gedaan dan nodig. De screenshots hiervan zijn [hier](https://github.com/RJJZitman/minor-applied-data-science/issues/16#issue-398250503) te zien.


## **-[Jargon](https://github.com/RJJZitman/minor-applied-data-science/issues/7#issue-398013124)**

Aangezien het ortho eyes project zich afspeeld in de medische wereld was het in het begin voor iedereen flink wennen aan de latijnse benamingen voor lichaamsdelen. Dit creëerde  voornamelijk een extra moeilijkheidsgraad bij het begrijpen van de data en tijdens het inlezen van de casus en literatuur. Een overzicht met de belangrijkste medische termen is [hier](https://github.com/RJJZitman/minor-applied-data-science/issues/7#issue-398013124) te vinden.

Verder door ons gebruikt jargon kunt u onder [deze](https://github.com/RJJZitman/minor-applied-data-science/issues/16#issue-398250503) link vinden.


## **[-Algemene wiskunde](https://github.com/RJJZitman/minor-applied-data-science/issues/6#issue-397984781)**

**Wiskunde achter de data: 3D rotatiematrices en eulerhoeken**

De door het LUMC aangeleverde data waar mee is gewerkt, bestaat uit 3d rotatiematrices in eulerhoeken. Om dit voor iedereen in de groep vatbaar te maken, heb ik een uitleg gegeven over wat een rotatiematrix is, hoe je deze kan gebruiken en wat eulerhoeken zijn. Aan de hand van zowel een voorbeeld in 2d en waar een 3d rotatiematrix opgesteld kan worden. Een herschreven versie hiervan is te zien op [deze](https://github.com/RJJZitman/minor-applied-data-science/issues/6#issue-397984781) foto's. Het origineel heb ik niet meer aangezien dit op een whiteboard was gemaakt en er geen foto van gemaakt is. Wat betreft eulerhoeken heb ik het gehouden bij een manier van noteren. Wat hier mist is een vector in R3 en hoe een 3D rotatiematrix opgesteld kan worden. Dit heb ik toen wel uitgelegd aan de hand van de rotatiematrices over de x-, y- en z-as.

**Kleine dingen gedurende het project**

Verder zijn er gedurende het project een paar kleine probleemtpjes ontstaan door bijvoorbeeld berekeningen verkeerd uit te voeren, of niet weten waar de fout zit. Als iemand hier tegenaan liep, keek ik graag mee om te zoeken naar een oplossing. Voorbeelden hiervan zijn de SSS driehoeken gebruiken om de ellebooghoek te berekenen en een matrixvermenigvulding die bij hetzelfde programma niet goed ging waardoor een arm niet zijn lengte behield tijdens het maken van een beweging.

  
 ## **-De data**
 
 **Splitsingsstrategie**
 
Samen met Dr. Andrioli heb ik de splitsingstrategie van de data bedacht. Wij hebben gekozen om 90% van alle data te gebruiken als trainset en de overige 10% te gebruiken als testset, om niet aan te zitten tot aan het einde van het project. Verder hebben wij de trainset verdeeld in twee delen. Namelijk een dataset om te leren, met een omvang van 80% van de trainset, en 20% van deze trainset als validatie dataset. Dit zodat wij tussendoor de classifiers konden valideren voordat wij aan het uiteindelijke testdata zaten. Anders zouden we het gevaar lopen de classifiers af te stemmen op de testset, wat niet de bedoeling is. De hierboven genoemde percentages zijn gebaseerd op de hoeveelheid metingen. Let wel, in deze subsets zijn uitsluitend gehele patienten per set verwerkt, dus er is geen data van een patient in twee of meer van deze subsets verwerkt. Ter verduidelijking is [hier](https://github.com/RJJZitman/minor-applied-data-science/issues/10#issue-398014521) een schematische weergave van de splitsingstrategie.
 
**Oefeningen met elkaar vergelijken**

Bekend was dat de patienten per categorie een aantal bewegingen/oefeningen uit moesten voeren, hier komt immers de data uit voort. Maar onbekend was wat welke oefening in hield en of oefening X van categorie 1, 2, 3 of 4 overeen kwam met oefening Y uitgevoerd door een de patienten uit een andere categorie. Om hier inzicht in te verkrijgen zijn we de grafieken van de humerus gaan bekijken met het doel om overeenkomsten te vinden. Op deze manier hebben wij vijf oefeningen gevonden die in elke categroie voorkomt.

**Visualisatie van de ruwe data en de cleaned data meting van Kasper vergelijken/nabootsen**

In een poging om alle oefeningen in de vorm van een 3d animatie af te beelden, hebben we geprobeerd om de cleaned sensor data van Kaspers metingen een 3d animatie te maken die overeen kwam met de animatie van de bijbehorende ruwe sensordata. Hier heeft Luke veel tijd in gestoken, maar dit is niet gelukt. Ik ben het toen ook gaan proberen door met parameters te spelen, maar zonder succes.
  
  
**De data opschonen**

Om een beter resultaat uit de classifiers te halen, is besloten om de data handmatig op te schonen. Erg veel metingen hadden ruis en soms was één oefening twee of meerdere keren uitgevoerd tijdens één meting. Toen is hier een script voor gemaakt. Samen met Luke heb ik toen het gedeelte tussen de #-------'s van de code gemaakt. [De gehele code](https://datascience.hhs.nl:8888/user/15023869/notebooks/Data%20Verdubbelaar%20V2.0.ipynb) is hier te zien.

**De energie variabele berekenen**

Samen met luke het deel geschreven waarmee de oppervlakte van de grafiek die de rotatie van een beweging beschrijft tegenover de acceleratie waarmee die rotatie veranderd per sample. [Hier](https://github.com/RJJZitman/minor-applied-data-science/issues/14#issue-398023411) is een voorbeeld te zien van zo'n grafiek, met toelichting van de rekekening. Het gedeelte in de [code](https://datascience.hhs.nl:8888/user/15023869/notebooks/Patient%20level%20-%20Create%20dataset.ipynb) waar de oppervlakte lijst wordt gemaakt, is waar de oppervlakte van de grafiek wordt berekend.

  ~[Categorie X vs Y classifier](https://github.com/RJJZitman/minor-applied-data-science/issues/12#issue-398015615) met gemanipuleerde parameters

 ~[fixed samples](https://github.com/RJJZitman/minor-applied-data-science/issues/13#issue-398020413) van de grafiek gebruiken
 
  
-Presentaties
  ~week 4-->powerpoint
  ~week 8-->powerpoint
  ~week 17--> powerpoint is er nog niet
  ~openbare eindpresentatie over het gehele project--> zelfde als week 17
-Paper
 ~Opzet structuur met kasper+ overzicht van de inhoude per hoofdstuk
 ~Introductie herschreven en aangevuld
 ~Results gemaakt
 ~Discussion gemaakt
 ~geholpen met inhoud conclusion
 ~link naar paper.


-Literatuur

-Overig
 ~Reflectie
  -inhoudelijk:ook clustertechnieken
  -procesmatig
 ~cvb borrel
 ~Algemene terugblik













Sprint 1, week 1 en 2, 27-08-2018 tot 07-09-2018:

Gedurende deze sprint lag de nadruk erg op het helder krijgen van het doel waar wij, als groep, naartoe gaan werken de komende 20 weken en DataCamp cursussen voltooien in Pyhton 3 voor data science. Omdat ik de stip aan de horizon niet concreet kon beschrijven, ben ik hiervoor met meneer Andrioli voor gaan praten om dit helder te krijgen. Na afloop van dit gesprek had ik hier een stuk beter beeld van. Verder ben ik begonnen met de eerste aangeschreven Python cursussen op DataCamp en heb ik een begin gemaakt met literatuuronderzoek (Flock of Birds BEP verslag). 

Verder zijn er algemene afspraken gemaakt binnen de projectgroep. Bestanden worden gedeeld via Google Drive en we houden met behulp van Trello bij wat er per sprint gedaan moet worden.

Tot slot kregen we een voorbeeldmeting van de data waar dit project mee moet worden gewerkt. Dit voorbeeld bestond uit een paar cijfers zonder enige aanvullende informatie. Wel was bekend dat het om een rotatiematrix in Eulerhoeken ging. Om het voor de niet-wiskunde studenten in de groep duidelijk te maken wat dat inhoudt, heb ik een kleine presentatie gegeven waarin het doel van een rotatiematrix en hoe deze gebruikt dient te worden in een berekening uitgelegd in zowel 2D als 3D.


Sprint 2, week 3 en 4, 10-09-2018 tot 23-09-2018:

Deze sprint heb ik mij vooral bezig gehouden met de Python cursussen van Datacamp en de Machine Learning cursus op coursera. Aan het einde van de sprint liep ik vrij goedop schema voor beide. Deze sprint ben ik ook verder gegaan met literatuuronderzoek, ditmaal Meskers_etal_1998 en De_Groot_1999. Deze rapporten zijn, net zoals Flock of Birds aangeraden door onze opdrachtgever Dr. ir. J. H. (Jurriaan) de Groot. Dit was vrij lastige matarie om door heen te werken door de latijnse termen in het medisch jargon, maar ook dat gaat steeds meer op de automatische piloot.

Verder hebben we deze sprint de door het LUMC opgeschoonde dataset gekregen. Deze dataset is opgedeeld in vier patientgroepen of categoriën. Aan de hand hiervan heb ik met Luke de Keijzer een poging gedaan om inzicht te verkrijgen in de overeenkomsten tussen allen patiënten ingedeeld in alle categoriën. 



Hiervoor hebben wij voor de standaarddeviatie van de X- en Y- coördinaat van de clavicula van oefening vier tegen elkaar uit te zetten op, respectievelijk, de X-as en Y-as.



Aan het einde van week vier heb ik de wekelijkse presentatie gegeven.


Sprint 3, week 5 en 6, 24-09-2018 tot 07-10-2018:

Tijdens deze sprint zijn we begonnen met het maken van de eerste classifier. Het idee was dat dit om een vrij simpele classifier zou gaan op basis van een weinig variabelen. Ook hadden wij ons als doel gesteld bij deze classifier dat deze erg gemakkelijk uit te breiden moest zijn. Dit is aardig gelukt goed gelukt. Onderweg zijn we wel een probleem tegengekomen, bij een berekeing bleef de lengte van de arm niet constant. Na enige tijd na de code te kijken, bleek dit te gaan om het verkeerd uitvoeren van een matrixvermenigvuldiging. hiervoor heb ik een algemene uitgewerking van een matrixvermeigvuldiging uitgeschreven. Toen dat duidelijk was, was het probleem vrij snel opgelost en behield de arm haar oorspronkelijke lengte.

Ook hebben meneer Andrioli en ik een strategie gemaakt waarmee de dataset opgedeeld wordt in een train- en test dataset. Aan de hand van deze verdeling is de data opgedeeld en de testdata aan de kant gezet. Hier is, zoals het hoort, ook niet meer naar gekeken en is de hierboven genoemde classifier getraind op basis van de train dataset.

Ook deze sprint ben ik door gegaan met de coursera Machine Learning cursus en de DataCamp Python cursussen. De DataCamp cursussen zijn allemaal afgerond. Met de Machine Learning cursus ben ik nog bezig. Ik heb voor mijzelf het doel gesteld om hier meer aan te doen dan wat minimaal verwacht wordt vanuit de minor aangezien er technieken aan bod komen verder in de cursus die voor ons project nuttig kunnen zijn.


Sprint 4, week 7 en 8, 08-10-2018 tot 21-10-2018:

Deze sprint is de eerste classifier afgerond en uitgebreid. Alleen werkte deze classifiers op sample niveau en niet op patient nivea. Hierom zijn Kasper van der Hoofd en ik hiermee aan de slag gegaan. Deze "nieuwe" classifier kon twee van de vier patientgroepen goed van elkaar onderscheiden.

Hiernaast ben ik door gegaan met de cursussen op DataCamp en de machine learning course.

Tot slot heb ik de presentatie in week acht gegeven.


Sprint 5, week 9 en 10, 29-10-2018 tot 11-11-2018:

Aan het begin van deze sprint hebben we met de projectgroep en meneer Andrioli een moment genomen om alle gemaakte progressie op een rij te zetten. Toen dit voor iedereen helemaal helder was, hebben we het project nogmaals vastgesteld en een planning gemaakt voor de komende twaalf weken.

Aan de hand hiervan ben ik gaan kijken naar clustertechnieken en als kleine voorbereiding op de volgende sprints ben ik ook een klein beetje door gegaan met deep learning.
