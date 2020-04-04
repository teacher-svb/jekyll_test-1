---
title: Klassen
tags: 
 - klasse
 - class
 - constructor
 - field
 - method
 - klassediagram
description:
---

# Klassen

## Wat is een klasse?
Een klasse is een groep variabelen en functies die bij elkaar horen waar je een naam aan geeft. Klassen zijn, nog veel meer dan functies, hèt middel bij uitstek om ons aan het DRY principe te houden. 

Een klasse is in feite een complex datatype dat je zelf maakt. Vanaf een klasse gemaakt is, kunnen objecten worden aangemaakt met als datatype de naam van die klasse. In volgend voorbeeld wordt een klasse `Leerling` gemaakt:

<pre class="prettyprint linenums lang lang-JS">
class Leerling {		// KLASSE
}
</pre>
<pre class="prettyprint linenums lang lang-PHP">
class Leerling {		// KLASSE
}
</pre>
<pre class="prettyprint linenums lang lang-CS">
public class Leerling {		// KLASSE
}
</pre>

Wanneer die klasse gemaakt is kan je een variabele van het datatype `Leerling` aanmaken:

<pre class="prettyprint linenums lang lang-JS">
let voorbeeldLeerling = new Leerling();		// OBJECT
</pre>
<pre class="prettyprint linenums lang lang-PHP">
$voorbeeldLeerling = new Leerling();		// OBJECT
</pre>
<pre class="prettyprint linenums lang lang-CS">
Leerling voorbeeldLeerling = new Leerling();	// OBJECT
</pre>

In dit voorbeeld wordt dus een variabele gemaakt met de naam `voorbeeldLeerling`. In die variabele wordt een waarde (object) bewaard van het datatype Leerling door `new Leerling()` aan te roepen.

**Opgelet!** Uiteraard is een lege klasse `Leerling` nogal zinloos. De bedoeling is dat de klasse wordt gevuld met functies en variabelen die bij een leerling horen.

## Fields

In een klasse kunnen variabelen worden opgeslagen.

Om deze waardes op te slaan, zijn variabelen nodig die bij de klasse Leerling horen, ook wel klasse-variabelen genoemd. Een klasse-variabele wordt ook wel eens een field of member genoemd.

<pre class="prettyprint linenums lang lang-JS">
class Leerling {
	constructor(naamLeerling, leeftijdLeerling) {
		this._naam = "Sam";	// _naam is een klasse-var
		this._leeftijd = 18;	// _leeftijd is een klasse-var
	}
}
let voorbeeldLeerling = new Leerling();
</pre>
<pre class="prettyprint linenums lang lang-PHP">
class Leerling {	
	private $_naam = "Sam";		// _naam is een klasse-variabele
	private $_leeftijd = 18;	// _leeftijd is een klasse-variabele
}
$voorbeeldLeerling = new Leerling();	
</pre>
<pre class="prettyprint linenums lang lang-CS">
class Leerling {	
	string _naam = "Sam";	// _naam is een klasse-variabele
	int _leeftijd = 18;	// _leeftijd is een klasse-variabele
}
Leerling voorbeeldLeerling = new Leerling();
</pre>

In bovenstaand voorbeeld heeft de klasse Leerling dus 2 variabelen:
 - `_naam`
 - `_leeftijd`

Deze variabelen kunnen gebruikt worden in héél de klasse Leerling, omdat het klasse variabelen zijn. 

## Methods

In een klasse kunnen ook functies worden gedefinieerd. Deze klase-functies worden methods genoemd. Een method is een functie die enkel werkt voor instanties van de klasse waarin die method is geschreven.

Bijvoorbeeld:

De klasse Leerling krijgt een method `Slaap()`. Deze method toont de tekst "zzzzzzzz" in de console. Elke variabele van het datatype Leerling kan nu de functie `Slaap()` gebruiken door `mijnVariabele.Slaap();` aan te roepen.

Probeer je echter de method `Slaap()` aan te roepen zonder een object krijg je een foutmelding: `Slaap` is not defined. Het programma meldt hier letterlijk: de functie `Slaap()` bestaat niet. Dit is correct, want er bestaat enkel een method genaamd `Slaap()`. Wil je een method aanroepen, dan heb je een object nodig van het juiste datatype.

<pre class="prettyprint linenums lang lang-JS">
class Leerling {
	Slaap() {
		console.log("zzzzzzzzzzzzzzzzz");
	}
}
let voorbeeldLeerling = new Leerling();
voorbeeldLeerling.Slaap(); 	// toont zzzzzzz in de console
</pre>
<pre class="prettyprint linenums lang lang-PHP">
class Leerling {
	function Slaap() {
		echo "zzzzzzzzzzzzzzzzz";
	}
}
$voorbeeldLeerling = new Leerling();
voorbeeldLeerling->Slaap(); 	// toont zzzzzzz in de console
</pre>
<pre class="prettyprint linenums lang lang-CS">
class Leerling {
	void Slaap() {
		console.log("zzzzzzzzzzzzzzzzz");
	}
}
Leerling voorbeeldLeerling = new Leerling();
voorbeeldLeerling.Slaap(); 	// toont zzzzzzz in de console
</pre>

## De constructor

In de volgende code staat iets vreemds:

<pre class="prettyprint linenums lang lang-JS">
class Leerling {
}

let voorbeeldLeerling = new Leerling();
</pre>
<pre class="prettyprint linenums lang lang-PHP">
class Leerling {
}

$voorbeeldLeerling = new Leerling();
</pre>
<pre class="prettyprint linenums lang lang-CS">
class Leerling {
}

Leerling voorbeeldLeerling = new Leerling();
</pre>

Hoewel de klasse Leerling géén haakjes heeft, moet een object ervan worden aangemaakt door new Leerling() te schrijven: de naam van de klasse, gevolgd door haakjes. Dit komt doordat elke klasse automatisch een speciale functie heeft genaamd de constructor.

De constructor is een speciale functie die een nieuw object aanmaakt. Het datatype van dat object is de klasse waar de constructor toe behoort. De lijn code `new Leerling()` doet eigenlijk het volgende:

 1. new geeft aan dat de constructor moet worden aangeroepen.
 2. `Leerling()` geeft aan dat de constructor van de klasse `Leerling` gebruikt moet worden.

De constructor is zoals elke andere method, maar heeft een paar beperkingen:

 - De constructor geeft niets terug: hij mag dus het keyword return niet bevatten.
 - De constructor kan maar één keer worden aangeroepen per object: enkel bij het aanmaken van een object.
 - De signature is anders: bestaat enkel uit de naam van de functie en de parameters
 
Elke klasse heeft een constructor, zelfs als die niet wordt geschreven. Als je een klasse maakt zonder constructor, wordt er (stiekem) toch een lege constructor gemaakt.

<pre class="prettyprint linenums lang lang-JS">
class Leerling {
	constructor() {
	}
}
let voorbeeldLeerling = new Leerling();	// Dit roept de constructor aan
</pre>
<pre class="prettyprint linenums lang lang-PHP">
class Leerling {	
	function __construct() {
	}
}
$voorbeeldLeerling = new Leerling();	// Dit roept de constructor aan
</pre>
<pre class="prettyprint linenums lang lang-CS">
class Leerling {	
	public Leerling() {
	}
}
Leerling voorbeeldLeerling = new Leerling(); // Dit roept de constructor aan
</pre>

De constructor wordt ook gebruikt om klasse-variabelen een waarde te geven bij het aanmaken van een object. De constructor is immers een method zoals elke andere. Geef je de constructor-functie een parameter, dan moet je die parameter ook invullen bij het aanroepen.

Het voorbeeld hieronder toont een klasse Leerling met twee fields: `_naam` en `_leeftijd`. De constructor krijgt twee parameters: `naamLeerling` en `leeftijdLeerling`. In de constructor worden de parameter-waardes doorgegeven aan de fields.

<pre class="prettyprint linenums lang lang-JS">
class Leerling {
	constructor(naamLeerling, leeftijdLeerling) {
		this._naam = naamLeerling;		
		this._leeftijd = leeftijdLeerling;	
	}
}

// Dankzij de constructor wordt _naam gelijk aan "Sam" en _leeftijd 18
let voorbeeldLeerling = new Leerling("Sam", 18);
</pre>
<pre class="prettyprint linenums lang lang-PHP">
class Leerling {	
	private $_naam = "";		
	private $_leeftijd = 0;		

	function __construct($naamLeerling, $leeftijdLeerling) {
		$this->_naam = $naamLeerling;
		$this->_leeftijd = $leeftijdLeerling;
	}
}

// Dankzij de constructor wordt _naam gelijk aan "Sam" en _leeftijd 18
$voorbeeldLeerling = new Leerling("Sam", 18);	
</pre>
<pre class="prettyprint linenums lang lang-CS">
class Leerling {	
	string naam = "";		
	int _leeftijd = 0;	

	public Leerling(string naamLeerling, int leeftijdLeerling) {
		this._naam = naamLeerling;
		this._leeftijd = leeftijdLeerling;
	}
}

// Dankzij de constructor wordt _naam gelijk aan "Sam" en _leeftijd 18
Leerling voorbeeldLeerling = new Leerling("Sam", 18);
</pre>

## Klasse Diagrammen
Klassen (en de objecten die daarmee gemaakt worden) zijn de essentie van Object Georiënteerd Programmeren. De meeste moderne programma's zijn gebaseerd op dit systeem.

Programmeurs gebruiken daarom vaak klasse diagrammen om te laten zien hoe een programma in elkaar steekt, zonder dat iemand daarvoor de code van het programma moet openen. Een klasse diagram is een snelle, overzichtelijke manier om te tonen welke variabelen en functies een klasse allemaal bevat.

Een klasse diagram heeft daarom 3 vakken:

 1. In het bovenste vak vind je de naam van de klasse
 2. In het middenste vak vind je de fields van de klasse.
	Fields worden geschreven als volgt:
      - naamVanField : datatype
 3. In het onderste vak vind je de methods van de klasse
 	Methods worden geschreven als volgt:
    - NaamVanMethod ( naamParameter1 : datatype, naamParam2 : datatype) : returntype

Vaak hebben klassediagrammen ook losstaande tekstvakken met extra informatie over de methods of fields.

<img src="{{ site.baseurl }}/assets/img/klassen_1.jpg" alt="klassediagram" style="max-width: 50%">
