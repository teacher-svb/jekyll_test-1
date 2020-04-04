---
title: Elementen
tags: 
 - instructie
 - commentaar
description:
---


# ELEMENTEN


## HTML tags

Een webpagina dient om inhoud te laten zien aan een bezoeker. HTML dient om die inhoud aan te duiden als tekst, titel, lijst, link, … Tags zijn de codewoorden die HTML gebruikt om aan te duiden waar elk deel van de inhoud voor dient.

Een tag is een **codewoord tussen een kleiner dan (&lt;) en groter dan (>) teken.**

HTML heeft een lijst[^2] met codewoorden die je kan gebruiken (je mag codewoorden niet verzinnen). Afhankelijk van welk codewoord je gebruikt, wordt de inhoud aangeduid als iets anders.


<pre>
&lt;img>		→ duidt een afbeelding (image) aan
&lt;video>		→ duidt een video aan
&lt;h1>		→ duidt een koptekst (heading niveau 1) aan
</pre>


Er bestaan 2 soorten tags:



1. Openingstags:		<code>&lt;<strong>h1</strong>>		</code>Duidt aan waar de inhoud (koptekst) begint
2. Sluitingstags:		<code>&lt;/<strong>h1</strong>>		</code>Duidt aan waar de inhoud (koptekst) eindigt

<pre>
&lt;p>dit is een paragraaf&lt;/p> en dit niet meer	→ duidt een paragraaf aan
&lt;a>dit is een link&lt;/a> en dit niet meer		→ duidt een link aan
&lt;h1>dit is een koptekst&lt;/h1> en dit niet meer	→ duidt een koptekst aan
</pre>




## Elementen

Een **HTML-element** is een blok code, bestaande uit een **openingstag**, **inhoud** en **sluitingstag**.


<pre>
&lt;p> Dit is een paragraaf element. &lt;/p>
&lt;h1> Dit is een koptekst element. &lt;/h1>
</pre>


In HTML kan inhoud niet bestaan zonder dit tussen een openingstag en sluitingstag te plaatsen. HTML wordt gebruikt om inhoud toe te voegen aan een website, dus spreken we nooit over het schrijven van tags, maar over het schrijven van elementen.


### Zelfsluitende elementen

**Sommige elementen voegen de inhoud die ze aanduiden zelf toe.** 



*   <code>&lt;<strong>hr</strong>></code> (horizontal rule) duidt een horizontale regel aan, en voegt die zelf ook toe.
*   <code>&lt;<strong>br</strong>></code> (break) duidt een witregel aan in tekst, en voegt die witregel zelf ook toe.

Je kan hier zelf geen inhoud meer aan toevoegen, want deze elementen doen dit zelf al. Deze speciale elementen bestaan dus <strong>enkel uit een openingstag</strong>, zonder inhoud of sluitingstag.


<pre>
&lt;p>
	Dit is een gewoon element.
&lt;/p>
Hieronder volgt een zelfsluitend element (zonder sluitingstag!):
&lt;hr>				→ toevoegen en aanduiden van een horizontale lijn
</pre>



## Nesten

Het **nesten** van elementen wilt zeggen dat je **een element insluit in een ander element**. Het ingesloten element is deel van de inhoud van het andere element.

Bijvoorbeeld: Hieronder is het h1-element (groen) ingesloten door het body-element (rood):


<pre>
&lt;body>
	&lt;h1>
		Dit element is genest in het body element.
		Dit element is deel van de inhoud van het body element.
	&lt;/h1>
&lt;/body>
</pre>


Of een iets uitgebreider voorbeeld:


<pre>
&lt;html>
	&lt;body>
		&lt;h1>
			Dit is een kop1-element.
		&lt;/h1>
		&lt;p>
			Dit is een paragraaf. Hierin staat meestal wat meer tekst!
			<b>Deze tekst wordt in het vet weergegeven.</b>
		&lt;/p>
	&lt;/body>
&lt;/html>
</pre>


Hierboven wordt duidelijk gemaakt dat:



*   Het `h1` element en het `p` element zijn genest in het `body` element.
*   In het `p` element is een `b` element genest.
*   De **inhoud** van het <code>&lt;<strong>body</strong>></code>-element bestaat uit het <code>&lt;<strong>h1</strong>></code>-element, het <code>&lt;<strong>p</strong>></code>-element, het <code>&lt;<strong>b</strong>></code> element dat in het <code>&lt;<strong>p</strong>></code>-element steekt, en de teksten in de elementen <code>&lt;<strong>h1</strong>></code>, <code>&lt;<strong>p</strong>></code> en <code>&lt;<strong>b</strong>> </code>


## Indentatie

Indentatie is **het aantal spaties voor elke lijn code**, dat aanduidt **in welk element die lijn code is genest**.

Hoewel indentatie in HTML niet verplicht is, helpt het om de leesbaarheid van je code enorm te verhogen. Als je indentatie correct is, kan je in één oogopslag zien op hoe je code genest is.

In het volgende voorbeeld staat het aantal indentaties aangeduid door zwarte lijnen voor elke lijn code.


![drawing](https://docs.google.com/a/google.com/drawings/d/12345/export/png) 

Zo zie je dat:

*   Het `p` element niet genest is
*   De elementen `ul` en `ol` genest zijn in het `p` element
*   Alle `li` elementen genest zijn in een `ul` of `ol` element


## Coding Guidelines

Hoewel HTML niet hoofdlettergevoelig is, worden alle tag-namen in **lowercase** geschreven.

Bij het schrijven van code let je steeds op de correcte **indentatie**.


## Samenvatting

HTML wordt geschreven door middel van **elementen**. 

Een **element** bestaat uit **code** en **inhoud**. 



*   De code van een element wordt geschreven met **tags**. 
*   **Inhoud** is de tekst die wordt weergegeven op de website.

**Een tag** is een codenaam tussen de driehoekige haakjes &lt; en >. De codenaam in een tag wordt de **tagnaam** genoemd.

Elementen bestaat meestal uit een **openingstag**, gevolgd door **inhoud**, en afgesloten door een **sluitingstag**.


<pre>
&lt;tag>							<-- openingstag
 Deze tekst wordt weergeven.					<-- inhoud
&lt;/tag>							<-- sluitingstag
</pre>


De **openingstag** dient om aan te duiden **waar een bepaald stukje inhoud begint**, de **sluitingstag duidt** vervolgens **aan waar die inhoud stopt**.

Een **sluitingstag** begint met een **forward slash**, een openingstag niet. 

Een **zelfsluitende tag** is een tag **die geen sluitingstag nodig heeft**.

Het **nesten** van elementen wilt zeggen dat je **een element insluit in een ander element**. 

