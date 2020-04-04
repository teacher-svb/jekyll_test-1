---
title: Structuur
tags: 
 - instructie
 - commentaar
description:
---



# STRUCTUUR

HTML bepaalt de structuur van een website. Deze structuur bestaat uit blokken waarin ofwel inhoud, ofwel andere, kleinere blokken worden geplaatst.

Het volgende voorbeeld toont hoe een website wordt onderverdeeld in vier blokken, en hoe het linkse blok op zich ook weer wordt onderverdeeld in vier kleinere blokken.

![drawing](https://docs.google.com/a/google.com/drawings/d/12345/export/png) 


Als web-ontwikkelaar helpt het om een duidelijk beeld van de structuur van de website te hebben voordat er wordt begonnen met HTML code te schrijven. Daarom is het een goed idee om bij een ontwerp zelf **een schets** te **maken** die toont hoe de hoofdstructuur en substructuren in elkaar zitten.

Een goede structuur zorgt ervoor dat je code gemakkelijker leesbaar is voor jezelf en andere programmeurs. Wanneer later opmaak en layout worden toegevoegd aan de website, zorgt een goede structuur er ook voor dat wijzigingen gemakkelijk en snel kunnen geimplementeerd worden. \
In het voorbeeld hiernaast zie je 2 websites met dezelfde structuur, maar een andere layout.


## Block elementen

Structuur wordt gegeven door middel van block elementen zoals het <code>&lt;<strong>div</strong>></code> element. Je kan bijvoorbeeld de gehele website als  één <code>&lt;<strong>div</strong>></code> element bekijken, waarin 4 verschillende <code>&lt;<strong>div</strong>></code> elementen worden geplaatst. Dit vertaalt zich dan naar de volgende code:


<pre>
&lt;div>
	&lt;div id="1">
	&lt;/div>

	&lt;div id="2">
	&lt;/div>

	&lt;div id="3">
	&lt;/div>

	&lt;div id="4">
	&lt;/div>
&lt;/div>
</pre>



Deze hoofdstructuur kan dan gemakkelijk uitgebreid worden met een **substructuur**:


<pre>
&lt;div>
	&lt;div id="1">
		&lt;div id="1.1">
		&lt;/div>

		&lt;div id="1.2">
		&lt;/div>

		&lt;div id="1.3">
		&lt;/div>

		&lt;div id="1.4">
		&lt;/div>
	&lt;/div>

	&lt;div id="2">
	&lt;/div>

	&lt;div id="3">
	&lt;/div>

	&lt;div id="4">
	&lt;/div>
&lt;/div>
</pre>




