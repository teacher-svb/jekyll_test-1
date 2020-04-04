---
title: Semantiek
tags: 
 - instructie
 - commentaar
description:
---



# SEMANTIEK


## Het doel van een element

Een belangrijk principe in web-ontwikkeling is dat je elementen gebruikt waarvoor ze dienen, niet vanwege hoe ze eruit zien in de browser. Dit heet de semantiek (het doel) van een element.

De semantiek van een element maakt duidelijk wat de bedoeling is van dat gedeelte in jouw HTML-code. Bijvoorbeeld: het &lt;p> element maakt duidelijk dat dit gedeelte een tekst-alinea zal bevatten.

Voor sommige elementen heeft de semantiek vooral te maken met hoe ze eruit zien. In dat geval zal de browser er vaak ook voor zorgen dat die semantiek ook zichtbaar is. Bijvoorbeeld: het &lt;b> en &lt;i> element hebben een duidelijke semantiek. Zij tonen vette of schuine tekst.  <br>
Ook het &lt;p> element is hier een voorbeeld van: er wordt steeds voor en na een alinea wat extra spatie gelaten door de browser.

Door het juiste semantische element te gebruiken, geef je aan de jezelf, andere web-ontwikkelaars en de browser extra informatie over de inhoud van je website.


## Foute voorbeelden

Hieronder vind je enkele voorbeelden hoe elementen **fout **gebruikt kunnen worden.



*   &lt;blockquote>: Sommige mensen gebruiken dit element om eender welke tekst aan de linkerkant te laten inspringen. <br>
**Wat is wel juist?** &lt;blockquote> is een element dat dient om een quote op je website te tonen.
*   &lt;p>: sommige mensen gebruiken &lt;p>&nbsp;&lt;/p> om een extra spatie toe te voegen in een tekst. <br>
**Wat is wel juist?** Gebruik hiervoor het &lt;br> element.
*   &lt;h1>-&lt;h6>: alle heading-elementen maken tekst groter of kleiner, vet of schuingedrukt. Als de inhoud echter geen koptekst is, mag je deze elementen niet gebruiken hiervoor!  <br>
**Wat is wel juist?** Gebruik CSS om tekst groter, kleiner, vet of schuingedrukt te maken.


## Onzichtbare semantiek

Alle HTML elementen hebben een semantiek, maar bij een aantal elementen is die semantiek niet zo zichtbaar als in de voorbeelden hierboven. Deze elementen zien er exact hetzelfde uit als een ander element, en doen exact hetzelfde, maar hebben toch **een andere betekenis**. <br>
Bijvoorbeeld: Zo is het &lt;header> element eigenlijk heel gelijkaardig aan een &lt;footer> element. De semantiek is echter heel verschillend. 

| website met &lt;div> elementen  | website met block-elementen |
| ------------- | ------------- |
| <img src="https://docs.google.com/a/google.com/drawings/d/12345/export/png" width="80%" alt="drawing">  | <img src="https://docs.google.com/a/google.com/drawings/d/12345/export/png" width="80%" alt="drawing">  |
| De linkse website werd opgebouwd met &lt;div> elementen.  | De rechtse website werd opgebouwd met block-elementen die semantisch veel juister zijn.  |

