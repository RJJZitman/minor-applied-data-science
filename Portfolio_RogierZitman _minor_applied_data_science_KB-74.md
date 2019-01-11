# Minor-applied-data-science

Dit is het portfolio van Toegepaste Wiskunde (HHS, te Delft) student Rogier Zitman m.b.t. het Ortho Eyes project, onderdeel van de minor Applied Data Science KB-74. In dit portfolio is opgenomen wat ik gedurende het Ortho-eyes project heb gedaan. Dit project is uitgevoerd met Dr. Tony Andrioli en drie medestudent: Kasper van der Hoofd, Luke de Keijzer en Vincent den Oord. 

Ortho-eyes is onderdeel van een onderzoek door Dr. Andrioli voor Dr. ir. J.H. (Jurriaan) de Groot, werkzaam bij het Leids Universitair Medisch Centrum (LUMC). 
 

# Dit portfolio is in de volgende wijze opgebouwd: 

**-Waarom deze minor en leerdoelen**

**-Online cursussen**

**-Jargon**

**-Algemene wiskunde**

**-Het project**

**-Presentaties**

**-Mijn bijdrage aan het paper**

**-Literatuur**

**-Overig**


## **-Waarom deze minor en persoonlijke leerdoelen**

Ik heb gekozen om de minor Applied Data Science KB-74 te volgen om een beter beeld te krijgen van Data Science en scripten, wat daar bij komt kijken en hoe dit procesmatig ingevuld kan worden.

Betreft Data Science wilde ik er graag weten welke toepassingen mogelijk zijn, hoe je van een probleem naar data gaat, wat voor technieken gebruikt kunnen worden om nuttige informatie uit een hoop data te filteren en dit om te zetten naar iets wat gebruikt kan worden in de maatschappij. Van het scripten wilde ik voornamelijk weten hoe je nou vooraf een goede rode draad voor jezelf/project uit kunt zetten om voor een lange periode gestructureerd dichter bij je eindproduct kan komen. Dit omdat bij mijn opleiding hier erg weinig nadruk op ligt.


## **-[Online cursussen](https://github.com/RJJZitman/minor-applied-data-science/issues/8#issue-398013713)**

Gedurende deze minor heb ik een aantal online cursussen gevolgd in python voor data science en machine learning. De python cursussen heb ik gedaan op Datacamp, leuk om te zien is dat ik er meer heb gedaan dan minimaal nodig. Screenshots waar de afgemaakte cursussen zijn afgebeeld vindt u [hier](https://github.com/RJJZitman/minor-applied-data-science/issues/1#issue-397295969).

Voor machine learning heb ik een deel van de andrew NG course op coursera gevolgd. Hier had ik relatief veel moeite mee. Daarom heb ik ook hier een week meer gedaan dan nodig. De screenshots hiervan zijn [hier](https://github.com/RJJZitman/minor-applied-data-science/issues/16#issue-398250503) te zien.


## **-[Jargon](https://github.com/RJJZitman/minor-applied-data-science/issues/7#issue-398013124)**

Aangezien het ortho eyes project zich afspeeld in de medische wereld was het in het begin voor iedereen flink wennen aan de latijnse benamingen voor lichaamsdelen. Dit creëerde  voornamelijk een extra moeilijkheidsgraad bij het begrijpen van de data en tijdens het inlezen van de casus en literatuur. Een overzicht met de belangrijkste medische termen is [hier](https://github.com/RJJZitman/minor-applied-data-science/issues/17#issue-398335580) te vinden.

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

Samen met luke het deel geschreven waarmee de oppervlakte van de grafiek die de rotatie van een beweging beschrijft tegenover de acceleratie waarmee die rotatie veranderd per sample. Hieronder is een voorbeeld te zien van zo'n grafiek, met toelichting van de berekening. Het gedeelte in de [code](https://datascience.hhs.nl:8888/user/15023869/notebooks/Patient%20level%20-%20Create%20dataset.ipynb) waar de oppervlakte lijst wordt gemaakt, is waar de oppervlakte van de grafiek wordt berekend.

![energie grafiek](https://user-images.githubusercontent.com/43171217/50998168-f0899600-1526-11e9-827a-e37b262a4059.png)

Omdat de punten op de grafiek een kromme vormen, hebben wij in plaats van het verschil van twee integralen te nemen de oppervlakte onder de boven- en onderkant van deze kromme numeriek benaderd. Als sample X+1 links van sample X lag, werd de waarde voor de oppervlakte als positief beschouwd en als sample X+1 rechts van sample X lag werd deze als negatief beschouwd. De absolute som van deze waarden geeft dan de op de afbeelding gemarkeerde oppervlakte.

**De categorie X vs Y classifier**

Luke en vincent zijn begonnen met een classifier die twee categoriën van elkaar moet onderscheiden. Na een tijdje heb ik dit overgenomen en afgemaakt.

Omdat categorie 2 en 3 niet goed uit elkaar te halen waren, ben ik toen de parameters gaan manipuleren om te onderzoeken of dat een positieve invloed had op de prestaties van deze classifier. Dit heb ik gedaan om logistieke regressie te simuleren. Helaas had dit geen positief effect op de prestaties van de classifier. U kunt [hier](https://datascience.hhs.nl:8888/user/15023869/notebooks/Classifier%202%20vs%203%20v1.1Logistic%20Regression.ipynb) de uiteindelijke code inzien.

**Fixed samples van de grafiek**

Nadat de max value classefiers niet goed genoeg werkten, besloten we om meerdere vaste punten op de grafiek mee te nemen dan alleen een maximum. Ik ben hier toen mee begonnen. [Dit script](https://datascience.hhs.nl:8888/user/15023869/notebooks/Fixed%20samples%20op%20de%20grafiek%20pakken.ipynb) is uiteindelijk niet gebruikt en afgemaakt omdat we overgingen op een andere stragetie om deze punten te kiezen.

 
  
## **-Presentaties**

Gedurende deze minor moest elke week een presentatie gegeven worden. In het begin zou iedereen om de drie weken dit op zich nemen. In  [week vier](https://github.com/RJJZitman/minor-applied-data-science/blob/master/Ortho%20Eyes%20presentatie%20week%204.pdf) en [week acht](https://github.com/RJJZitman/minor-applied-data-science/blob/master/Ortho%20Eyes%20presentatie%20week%208.pdf) heb ik de presentatie verzorgd. Ook ga ik, samen met Luke, de presentatie in week 17 en de laatste en openbare presentatie geven waar het gehele project onder handen wordt genomen. Deze presentatie zijn op het moment van schrijven nog niet gemaakt, dus kunnen zij nog niet in dit portfolio worden opgenomen.

In vergelijking met ander groepsleden heb ik niet veel presentaties gegeven. Dit mede door tweemaal overmacht* en omdat ik relatief veel ervaring met presentaties heb en hierom liever de kans aan mijn groepsgenoten gaf.


## [**-Paper**](https://github.com/RJJZitman/minor-applied-data-science/blob/master/paper_ortho_eyes.pdf)

Ook aan het paper behorend bij het Ortho eyes project heb ik mijn bijdrage geleverd. Deze is hieronder puntsgewijs uiteengezet.

- Opzet van de structuur gemaakt, met een overzicht van de inhoud per hoofdstuk. Samen met Kasper.
- De introductie herschreven en aangevuld voor de laatste versie.
- Het hoofdstuk 'Resuts' gemaakt.
- Het hoofdstuk 'Discussion' gemaakt.
- Samen met Kasper het hoofdstuk 'Conclusion' gemaakt.
- Hier is een [link](https://github.com/RJJZitman/minor-applied-data-science/blob/master/paper_ortho_eyes.pdf) naar het paper.


## **-Literatuur**

Aan het begin van de minor heb ik mij ook in enige literatuur verdiept. Onze opdrachtgever (J.H. de Groot) heeft ons toendertijd een aantal artikelen opgestuurd op het gebied van onze opdracht. Hieronder is een lijst met alle, door mij bestudeerde, literatuur gecategoriseerd weergegeven.

**Het verkrijgen van inzicht in het onderwerp.**

- [De Groot, 1997](https://github.com/RJJZitman/minor-applied-data-science/blob/master/DeGroot_1997.pdf)
- [De Groot, 1999](https://github.com/RJJZitman/minor-applied-data-science/blob/master/DeGroot_1999.pdf)
- [Meskers, etal 1998](https://github.com/RJJZitman/minor-applied-data-science/blob/master/Meskers_etal_1998b.pdf)
- [Wu, etal 2005](https://github.com/RJJZitman/minor-applied-data-science/blob/master/Wu_etal_2005.pdf)

**Het BEP eindrapport (van de studenten die het Flock of Birds systeem hebben ontwikkeld), om een beter beeld van het meetsysteem te verkrijgen.**
- [BEP rapport Flock of Birds](https://github.com/RJJZitman/minor-applied-data-science/blob/master/Final_Report%20TUDElft%20FLock%20of%20Birds.pdf)

**Het paper van het groep voor ons om mijzelf in te lezen in de geboekte resultaten en daardoor beter onze eigen doelstelling te begrijpen.**
- [Paper vorige Ortho Eyes projectgroep](https://github.com/RJJZitman/minor-applied-data-science/blob/master/Paper%20van%20vorige%20jaar.pdf)


## **Overig**

**Zelfreflectie**

Inhoudelijk ben ik erg tevreden met wat ik heb geleerd de afgelopen 17 weken. Wat betreft programmeren in Python kan ik nu meer dan een for lus maken, wat eerst niet het geval was. Ook heb ik erg veel geleerd van de online cursussen en het bestuderen en begrijpen van de code van mijn projectgenoten. Zelf scripten is nog zeker niet mijn sterkste kant, maar ik heb wel een hoop ervaring in opgedaan in het genereren van code en de code van andere bestuderen, begrijpen en waar nodig debuggen.

Wat betreft de Data Science, zoals door de hierboven genoemde online cursussen van zowel Datacamp en de machine learning course van Andrew NG heb ik nu een stuk beter beeld op welke manier je om kan gaan met verschillende typen data. Verder is het Ortho Eyes project voor mij een erg duidelijk voorbeeld van een probleem in de maatschappij, omgezet in een probleem waarvan de oplossingen liggen in data. Naar welke variabelen men kan kijken, waarom wel het één en niet het ander. Machine learning vond ik in het begin erg lastig, omdat de wiskunde op een voor mij onverwachte manier werd gebruikt. Het waren eerst voornamelijk voorgebakken recepten, waarvan je moest weten dat ze werkten en hoe je ze kon gebruiken. De waarom miste bij mij. Maar tijdens het studeren voor het  tentamen begon het kwartje steeds meer te vallen. Hierdoor ben ik van mening dit leerdoel te hebben behaald.

Aan het begin van de minor is het mij niet gelukt om direct een rode draad richting het einddoel te maken. Dit komt mede doordat erg werd aangemoedigd om met SCRUM te werken waardoor wij om de twee weken de komende twee weken invulden en niet zo zeer naar 10 weken verderop keken. Het gevolg hiervan was wel dat ik een nieuwe werkwijze heb meegemaakt en ik zie zeker het nut ervan in, hier ben ik erg blij mee. Ook ga ik hier bij mijn volgende projecten gebruik van maken, door vooraf te bedenken wat er per "sprint" gedaan kan worden en zo toch enigszins die rode draad te creëeren. Hoewel ik deze, voor mij toen onbekende en verassende, werkwijze niet had voorzien, heb ik een extra middel om voor mijzelf een goed overzicht te behouden over de behaalde resultaten en wat welke activiteiten nog in het verschiet liggen. Hiermee ben ik met betrekking tot dit leerdoel erg tevreden en beschouw ik het als behaald.

Tot slot brengt het interpeteren van zowel de eind- als de tussenresultaten gedurende het Ortho Eyes project mij op mijn laatste vooraf gestelde leerdoel; de gevonden resultaten omzetten in een oplossing voor het probleem waar het project uit is voortgekomen. De vorm van resultaten was voor mij nieuw. Aan de hand van een percentage bepalen wat je nou eigenlijk hebt gedaan en dat evalueren om een goede volgende stap te kunnen zetten. Dit werd mij vrij snel duidelijk en zeker aan het eind van het project kon ik goed verwoorden wat er is gebeurd, waarom de behaalde resultaten als wel of niet positief beschouwd kunnen worden en wat het betekend voor het probleem en daarmee onze opdrachtgever. Toen ik dit leerdoel opstelde, ging het voornamelijk om het laatste, de terugkoppeling naar de oorsprong van het project, en ik kijk erg positief terug over mijn progressie in dit opzicht. Een geslaagd leerdoel dus.

Over het algmeen kijk ik positief terug op de minor en het bijbehorende project. Ik heb er erg veel van geleerd en het heeft veel enthausiasme voor het vakgebied gecreëerd bij mij.


**-CVB borrel**
Tijdens de minor zijn wij als groep ook uitgenodig op een CVB borrel waar wij onze (tussen)resultaten konden presenteren. Dit was een leuke en gezellige middag.
![cvb-borrel](https://user-images.githubusercontent.com/43171217/51042519-d4383880-15bc-11e9-933e-4d41f33642da.jpg)



*Eenmaal wegens ziekte en eenmaal wegens een crematie.
