---
title: Inheritance
tags: 
 - klasse
 - class
 - superklasse
 - subklasse
 - parent
 - child
description:
---

# Inheritance

## Don't Repeat Yourself

Klassen zijn een goede manier om het DRY principe te respecteren. Met een klasse moeten de fields en methods van die klasse maar 1x worden geschreven, terwijl elk object van die klasse er toegang tot heeft.

Het gebeurt echter vaak dat verschillende klassen een aantal fields en methods delen. In het voorbeeld hieronder bevatten `Leerling` en `Leraar` beide een field `id` en een field `naam`. Nog belangrijker is dat deze fields in beide klasse semantisch hetzelfde zijn: in beide klassen heeft bijvoorbeeld de field `naam` hetzelfde doel. In dit geval is het doel om "de naam van een persoon" op te slaan.

In een klasse `klas` is het field `naam` semantisch verschillend: hier wordt niet de naam van een persoon bijgehouden, maar wel de "naam van een klasgroep".

<img src="{{ site.baseurl }}/assets/img/inheritance_1.png" alt="klassediagram" style="height: auto; max-width: 100%">

Wanneer verschillende klassen een aantal fields of methods delen die semantisch hetzelfde zijn, wordt het DRY principe weer geschonden. Op verschillende plaatsen in de code kunnen methods en fields die hetzelfde doen teruggevonden worden. Met behulp van inheritance kan dit voorkomen worden.

## Inheritance

Inheritance ('overerving') is een manier om fields en methods die semantisch hetzelfde zijn in een aparte klasse te zetten. Deze klasse wordt dan de **superklasse** genoemd.

De klassen waaruit deze fields en methods werden weggehaald, worden dan aangeduid als subklassen. **De subklassen 'erven' de eigenschappen van de superklasse** (de fields en methods) en kunnen daar dus gebruik van maken.

In het voorbeeld hieronder zijn er 2 klassen `Leraar` en `Leerling` gedefinieerd:

<pre class="prettyprint linenums lang lang-JS">
Javascript
class Leerling {
	constructor(naamLeerling, leeftijdLeerling) {
		this._naam = "";
		this._leeftijd = 0;
		this._hoed = null;
	}
}

class Leraar {
	constructor(naamLeerling, leeftijdLeerling) {
		this._naam = "";
		this._leeftijd = 0;
		this._diplomas = [];
	}
}
</pre>
<pre class="prettyprint linenums lang lang-PHP">
class Leerling {	
	private $_naam = "";
	private $_leeftijd = 0;
	private $_hoed = null;
}

class Leraar {	
	private $_naam = "";
	private $_leeftijd = 0;
	private $_diplomas = array();
}
</pre>
<pre class="prettyprint linenums lang lang-CS">
class Leerling {	
	string _naam = "";
	int _leeftijd = 0;
	int _hoed = null;
}

class Leraar {	
	string _naam = "";
	int _leeftijd = 0;
	int _diplomas = [];
}
</pre>

Beide klassen hebben een field `naam` en een field `leeftijd` die semantisch hetzelfde zijn. Het DRY principe wordt dus geschonden.

Daarom wordt er nu een derde klasse gemaakt: `Persoon`. Persoon wordt de **superklasse** van `Leerling` en `Leraar`. `Leerling` en `Leraar` worden vervolgens aangeduid dat ze overerven van de klasse Persoon. Dit zijn de **subklassen** van de klasse Persoon.

<pre class="prettyprint linenums lang lang-JS">
class Persoon {
	constructor(naamLeerling, leeftijdLeerling) {
		this._naam = "";
		this._leeftijd = 0;
	}
}

class Leerling extends Persoon { // extends duid aan dat er wordt overgeërfd
	constructor(naamLeerling, leeftijdLeerling) {
		this._hoed = null;
	}
}

class Leraar extends Persoon {   // extends duid aan dat er wordt overgeërfd
	constructor(naamLeerling, leeftijdLeerling) {
		this._diplomas = [];
	}
}
</pre>
<pre class="prettyprint linenums lang lang-PHP">
class Persoon {	
	private $_naam = "";
	private $_leeftijd = 0;
}

class Leerling extends Persoon { // extends duid aan dat er wordt overgeërfd
	private $_hoed = null;
}

class Leraar extends Persoon {   // extends duid aan dat er wordt overgeërfd
	private $_diplomas = array();
}
</pre>
<pre class="prettyprint linenums lang lang-CS">
class Persoon {	
	string _naam = "";
	int _leeftijd = 0;
}

class Leerling : Persoon {	 // : duid aan dat er wordt overgeërfd
	int _hoed = null;
}

class Leraar : Persoon {	 // : duid aan dat er wordt overgeërfd
	int _diplomas = [];
}
</pre>

Er wordt terug helemaal voldaan aan het DRY principe.
