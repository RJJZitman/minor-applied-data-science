# minor-applied-data-science

Dit is het portfolio van Rogier Zitman m.b.t. het Ortho Eyes project, onderdeel van de minor Applied Data Science KB-74. In dit portfolio is opgenomen wat ik gedurende het Ortho-eyes project heb gedaan. Dit project is uitgevoerd met Dr. Tony Andrioli en drie medestudent: Kasper van der Hoofd, Luke de Keijzer en Vincent den Oord.

Ortho-eyes is onderdeel van een onderzoek door Dr. Andrioli voor Dr. ir. J.H. (Jurriaan) de Groot, werkzaam bij het Leids Universitair Medisch Centrum (LUMC).


Dit portfolio is in de volgende wijze opgebouwd:
-Online cursussen
  ~Coursera andrew NG machine learning course
  ~Datacamp courses
-Jargon
  ~Medisch jargon
  ~Jargon gebruikt in het paper
-Wiskunde
  ~Wiskunde achter de data: 3D rotatiematrices en eulerhoeken
  ~SSS driehoeken om de ellebooghoek te berekenen
-De data
  ~Splitsingsstrategie bedenken
  ~Visualisatie van de ruwe data en de meting van Kasper vergelijken/nabootsen
  ~De data opschonen
  ~De energie variabele berekenen
  ~Parameters manipuleren om lineaire regressie the simuleren
-Classifiers waar ik aan heb meegewerkt  
  ~[classifier X vs Y LR manipulated parameters](https://datascience.hhs.nl:8888/user/15023869/notebooks/Classifier%202%20vs%203%20v1.1Logistic%20Regression.ipynb)
  
  ~[DataCleaner, wiskunde](https://datascience.hhs.nl:8888/user/15023869/notebooks/Data%20Verdubbelaar%20V2.0.ipynb)
  
  ~[gedeelte oppervlakte berekenen-->energy variabele](https://datascience.hhs.nl:8888/user/15023869/notebooks/Patient%20level%20-%20Create%20dataset.ipynb)
  
 ~[fixed samples op de grafiek pakken](https://datascience.hhs.nl:8888/user/15023869/notebooks/Fixed%20samples%20op%20de%20grafiek%20pakken.ipynb)
  
-Presentaties
  ~week 4
  ~week 8
  ~week 17
  ~openbare eindpresentatie over het gehele project
-Paper
-Literatuur
-Overig

Coursera andrew NG:
Mijn voortgang van de andrew NG machine learning course is hier te vinden:
https://github.com/RJJZitman/minor-applied-data-science/issues/3#issue-397733258

Datacamp courses:
In de links staan screenshots met de datacamp courses die ik heb voltooid, dit zijn er meer dan minimaal nodig.
https://github.com/RJJZitman/minor-applied-data-science/issues/1#issue-397295969



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