---
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
#highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
aspectRatio: '16_/9'
routerMode: 'hash'
materia: 'TPSI'
as: '2022-2023'
version: '1.0.2'
---  


# JavaScript

No brain no pain!

<div class="pt-12">
  <span class="px-2 py-1">
    Premi spazio o <carbon:arrow-right class="inline"/> per la prossima slide
  </span>
</div>


---
layout: two-cols
---
https://javascript.info/

- stringhe e operatori stringhe
- array e operatori array


::right::

- frontend JS
- eventi e asyncrhonoous programming
- svelte js intro e installazione


--- #slide 1

# Developer Survey 2021

https://insights.stackoverflow.com/survey/2021


<img src="/media/js00.png" class="mx-auto w-160" />


--- #slide 2
 
# JavaScript

Most commonly used programming language

<img src="/media/js01.png" class="mx-auto w-105" />


--- #slide 3
preload: false
---

# JavaScript

I linguaggi più utilizzati nel mondo dello sviluppo software

<img src="/media/js02.png" class="mx-auto w-130" />

<arrow v-click="1" x1="800" y1="420" x2="700" y2="150" color="#0000ff" width="3" arrowSize="1" />

--- #slide N
 
# Hello JS World!

Il tag \<script\>

- Uno programma JavaScript è inserito in una pagina HTML, tramite il tag `<script>...</script>`
- Il tag **\<script\>** può essere inserito ovunque nella pagina, ma normalmente viene inserito nella sezione \<head\>
- Spesso, per ragioni di performance viene inserito al fondo della pagina, alla fine della sezione \<body\>

```html {all|6-8}
<!DOCTYPE html>
<html lang="it">
  <head>
      <meta charset="UTF-8" />
      <title>Hello JS World</title>
      <script>
        alert("Hello JS World!!");
      </script>
  </head>
  <body>
    My HTML page with JS code!
  </body>
</html>
```

--- #slide N
 
# Hello JS World!

Il tag \<script\>

- Il codice JavaScript contenuto nel tag \<script\> viene eseguito automaticamento al caricamento della pagina HTML.

![js03](/media/js03.png)


--- #slide N
 
# Hello JS World!

Il tag \<script\>

- Tuttavia questa non è una pratica corretta.
- Esattamente come per lo stile CSS è buona norma seprarare il codice HTML dal programma JavaScript
- Pertanto, il modo corretto di includere un programma JavaScript in una pagina HTML, è di usare un file esterno ***.js***

```html {all|6-7}
<!DOCTYPE html>
<html lang="it">
  <head>
      <meta charset="UTF-8" />
      <title>Hello JS World</title>
      <script src="/path/to/script.js"></script> <!-- link relativo -->
      <script src="http://URL/to/script.js"></script> <!-- link assoluto -->
  </head>
  <body>
    My HTML page with JS code!
  </body>
</html>
```

--- #slide N
 
# Hello JS World!

Il tag \<script\>

- E' possibile ovviamente referenziare lo scipt JS tramite una URL valida
  
  ```<script src="https://cdnjs.cloudflare.com/ajax/libs/lodash.js"></script>```

- Nel caso sia necessario, per pagine medio/complesse, si possono includere più script JS diversi

```html {all|6-8}
<!DOCTYPE html>
<html lang="it">
  <head>
      <meta charset="UTF-8" />
      <title>Hello JS World</title>
      <script src="https://url/to/script1/script1.js"></script>
      <script src="https://url/to/script2/script2.js"></script>
      <script src="https://url/to/script3/script3.js"></script>
  </head>
  <body>
    My HTML page with JS code!
  </body>
</html>
```


--- #slide N
 
# Esercizio js_01

Hello JS World!

1. Creare una pagina web basata sul codice delle slide precedenti e salvarla come *|cognome|_esercizio_js_01a.html*
2. Verificare l'esecuzione dello script JS all'avvio della pagina
3. Provare a modificare il codice JS
4. Creare una pagina web, che esegue il codice JS da file esterno e e salvarlo come *|cognome|_esercizio_js_01b.html* e *|cognome|_esercizio_js_01b.js*
5. Fornire il link github ai file con nome *|cognome|_esercizio_js_01a.html, |cognome|_esercizio_js_01b.html e |cognome|_esercizio_js_01b.js* 

--- #slide N
 
# Browser Developer Tools

&nbsp;

- L'esecuzione dello script può generare errori che però non sono visualizzati nella pagina HTML
- I moderni browser, offrono una serie di strumenti denominati ***Developer Tools***
- I tool di sviluppo più evoluti sono quelli di Chrome e Firefox
- Per accedere ai tool di sviluppo in Chrome basta premere <kbd>F12</kbd> o <kbd>CTRL + SHIFT + I</kbd>

![js04](/media/js04.png)

--- #slide N
 
 # Browser Developer Tools

https://developer.chrome.com/docs/devtools/

- **Elements**: Fornisce accesso al codice HTML e agli stili CSS. Utilissimo per fare il debugging di problematiche legate allo stile della pagina
- **Console**: Console JavaScript. Permette l'accesso al codice JS della pagina ed è utilissima per il debug
- **Sources**: Fornisce una panoramica sull'origina di tutte le risorse caricate dalla pagina
- **Network**: Permette di comprendere in modo dettagliato le operazioni di rete del browser
- **Performance**: Permette di registrare una sessione di navigazione ed analizzare in dettaglio le performance del browser e l'uso delle risorse
- **Memory**: Fornisce una visione dettagliata della memoria del browser durante l'esecuzione del codice JS
- **Application**: Fornisce accesso alle risorse dell'applicazione web (es: local storage, cookies, ...)
- **Security**: Offre una panoramica sugli aspetti di sicurezza della pagina (es: certificati SSL, ...)
- **Lighthouse**: Permette di iodentifficare e risolvere potenziali problemi lagati alla pagina web ottimizzandone le prestazioni
  
--- #slide N
 
# JS Console

REPL

- Per accedere direttamente alla console JS di Google Chrome basta premere  <kbd>CTRL + SHIFT + J</kbd>
- La console JS, oltre ad essere uno strumento di debugging è anche un **REPL**
- **REPL**: Read Evaluate Print Loop (https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop)
- Pertanto la console/REPL JS permette di eseguire direttamente del codice JS generico, permette di interagire con la pagina HTML
- Il REPL JS è un ottimo strumento per apprendere JavaScript direttamente nel browser
- Un metodo alternativo è usare **node.js** sul proprio PC

![js05](/media/js05.png)


--- #slide N

# JS Console

REPL

- Quando inseriamo una linea di codice nella console JS e premiamo <kbd>Enter</kbd> questo viene immediatamente eseguito
- Per inserire più linee è necessario premere <kbd>SHIFT + Enter</kbd> e solo alla fine, per eseguire tutto il blocco  premere <kbd>Enter</kbd>

![js06](/media/js06.png)

--- #slide N
 
# Esercizio js_02

JS REPL

1. Aprire la console JS
2. Eseguire lo script dell'esercizio js_01 direttamente dalla console JS

--- #slide N
 
# JS Back-End

Node.js

- Esiste un terzo modo per eseguire uno script JS
- Nel corso degli anni JS ha abbracciato diversi domini di esecuzione e si è spostato anche dal lato dello sviluppo back-end
- Oggi JS può essere eseguito su qualsiasi piattaforma:
  - schede embedded per mondo IoT (arduino e simili)
  - Web browser
  - Smart Phone
  - Lato server nel cloud e non

- Lo sviluppo JS lato back-end è reso possibile grazie a `Node.js`
- Node.js è un runtime JavaScript costruito sul motore JavaScript V8 di Chrome.
- Node.js permette l'esecuzione di applicazione back-end scritte in JS

--- #slide N
 
# JS Back-End

Node.js

- Node.js è
  - **Single Threaded**: c'è un solo thread di esecuzione (in contrapposizione del modello threaded di altri web server e application engine) 
  - **Non-Blocking I/O**: Il thread di esecuzione **NON** si ferma/blocca in attesa del completamento di operazioni di I/O (rete, disco, ...)
  - **Asynchronous**: L'esecuzione del codice è asincrona e basata su call back e non sequenziale. Le operazioni I/O sono eseguite in maniera asincrona rispetto al thread principale.

- Importante notare che Node.js  non è adatto a problemi CPU intensive, in quanto è single-threaded.
- **Pertanto risulta evidente che Node.js fornisce le migliori performance per applicazioni I/O intensive (rete)**
- Node.js è è un runtime JavaScript guidato da eventi asincroni (richieste HTTP) e progettato per creare applicazioni di rete scalabili.

--- #slide N
 
# JS Back-End

Node.js

![/media/js07.png](/media/js07.png)

--- #slide N
 
# JS Back-End

Node.js

- Importante notare che Node.js è scritto per un sistema operativo e non per un browser
- Pertanto non tutte le API sono disponibili
 
  <br />ES:<br />
  ```js
  alert("CIAO");
  ```
- Non può essere eseguito in Node.js e genera un errore
  <br />
  
  ```js
  Uncaught ReferenceError: alert is not defined
  ```

- Nota che Node.js svolge anche la funzione di REPL


--- #slide N
 
# Esercizio js_03

Node.js

Dato il seguente script JS

```js
var a =5;
var b = 7;
console.log(a+b);
```

1. Eseguire lo script nel REPL di Node.js, invocando `node` da console e inserendo le istruzioni su linee diverse
2. Creare un file |cognome|_esercizio_js_03.js contenente lo script sopra
3. Eseguire lo script da console
   
   ```bash
   node |cognome|_esercizio_js_03.js
   ```
4. Fornire il link github al file con nome *|cognome|_esercizio_js_03.js* 

--- #slide N
 
# Struttura del codice

Statements

- Un programma JavaScript, esattamente come in C/C++ e Java, è composto da una serie di ```statements```
- Uno **statement** è un costrutto sintattico o un comando/istruzione che esegue una specifica azione
- Per esempio abbiamo visto, nelle slide precedenti, lo statement **alert("Hello JS World!!");**
- Un programma JS è composto da uno o più statement
- Gli statement possono essere separati dal carattere ```;```

<br/>

```js
alert("Hello ");alert("JS ");alert("World!!");
```
<br/>


- Normalmente gli statement si scrivono su linee separate, per aumentare la leggibilità del codice

<br/>

```js
alert("Hello ");
alert("JS ");
alert("World!!");
```

--- #slide N
 
# Struttura del codice

Semicolons

- JavaScript permette di sostituire il terminatore di statement ```;```  con un  ```EOL``` (End of Line - Ritorno a Capo)
- Pertanto, tranne casi specifici, il carattere ```;``` può essere omesso

<br/>

```js
alert("Hello ")
alert("JS ")
alert("World!!")
```

<br/>

- In questo caso, l'interprete JavaScript riconosce il ritorno a capo come terminatore dello statement (;)
- Questo processo si chiama ***automatic semicolon insertion***
- Per esempio in C/C++ e Java ciò **NON** è permesso

--- #slide N
 
# Struttura del codice

Semicolons

- Tuttavia ci sono delle eccezzioni
- Non sempre un ritorno a capo viene automaticamente sostitutio da un **;**

<br/>

```js
alert(5 +
2);
```

<br/>

- In questo scenario, lo EOL dopo il +, **NON** viene sostituito con **;** ma solo come un normale ritorno a capo
- L'interprete comprende che terminando lo statement dopo il +, l'esperessione non sarebbe  valida ***5 + ????***
- Pertanto non sostituendo EOL con ; l'espressione risulta completa e l'interprete è in grado di eseguire correttamente lo statement.
- Da ciò ne consegue che, **i parametri di una funzione, possono essere forniti su più linee**.
- Ciò è vero anche in C/C++ e Java
- NOTA: L'interprete JS non è **SEMPRE** in grado di effettuare l'automatic semicolon insertion
<div style="background-color:green;color:yellow;padding:0px;">
  <p>Il mio stile, che deriva dal C, prevede quindi di inserire sempre <b>;</b> alla fine di ogni statement</p>
</div> 

--- #slide N
 
# Struttura del codice

Commenti

- In modo analogo a qualsiasi altro linguaggio di programmazione, una parte del codice **MOLTO** importante sono i *commenti*.
- Per codici non banali, è necessario aggiungere commenti che descrivono il funzionamento del codice e la motivazione di alcune scelte implementative.

Ci sono due tipi di commenti:
- **singola linea**: il commento inizia e finisce su un'unica linea
  
```js
// Questo è un commento su singola linea
alert("Commento singola linea"); //Anche questo è un commento valido
```

  - **multi linea**: il commento occupa 2 o più linee

```js
/*Questo è un
commento
multi linea*/
alert("Commento multi linea"); //Anche questo è un commento valido

```

--- #slide N
 
# Struttura del codice

Commenti

- I commenti nested non sono supportati

```js
/* Commento dentro un altro   
   /*  commento non valido*/
*/

```
<br />
<br />

- In VS Code è possibile inserire un commento, selezionando il codice e  premendo i tasi `CTRL + SHIFT + /`

<br />
<br />

- Ricorda che è una buona pratica di programmazione commentare in modo intelligente il codice
- La ***leggibilità*** del codice è un parametro molto importante. I commenti aumentano la comprensione e la capacità di leggere e comprender eil codice sorgente.
- I commenti del codice, sono l'equivalente della parafrasi in Italiano
- E' più facile leggere la divina commedia con la parafrasi o solo con i versi originali?
- Ecco per il codice sorgente è esattamente la stessa cosa.

--- #slide N
 
# Variabili

Tipizzazione

- Una variabile è un concetto astratto che non dipende dal linguaggio di programmazione.
- ***Una variabile è concettualmente un contenitore identificabile per un dato/valore.***
- In JavaScript le variabili implementano esattamente questo concetto, in modo del tutto analogo a C/C++ e Java.
- La differenza principale deriva dal fatto che C/C++ e Java sono linguaggi `fortemente tipizzati`
- Al contrario JavaScript è un linguaggio `debolmente tipizzato`.

- In un linguaggio ***fortemente tipizzato***, il programmatore è obbligato a specificare il tipo di ogni variabile e le assegnazioni posso avvenire solo tra tipi corenti.

```c
int num;

num = 4; // assegnazione valida
num = "ciao"; // errore - assegnazione invalida
```

--- #slide N
 
# Variabili

Tipizzazione

- In modo opposto, in un linguaggio ***debolmente tipizzato***, il programmatore ***NON*** assegna un tipo alle variabili.
- Pertanto una variabile può contenere un qualsiasi tipo di dato che può cambiare a runtime
- I linguaggi di programmazione con questa caratteristica, come JS, sono anche chiama **dynamically typed**. 
- Infatti esistono i tipi di dati, ma alle variabili non è assegnato un tipo predeterminato.

<br />


```js
var num;

num = 4; // assegnazione valida
num = "ciao"; // anche quest'assegnazione è valida

```
<br />

- Questa caratteristica, tipica dei linguaggi interpretati, fornisce grande flessibilità al programmatore.
- Tuttavia ha anche alcuni difetti, soprattutto per chi è alle prime armi o per grossi progetti.

--- #slide N
 
# Variabili

Dichiarazione e Definizione

- In JavaScript, tradizionalmente  una variabile può essere definita tramite la keyword `var`
- Dalla specifica del 2015 chiamata ECMA6 o ES6 una variabile si può anche definire tramite la keyword `let`
  
<br />

```js
var numero; // dichiara una variabile di nome numero
let testo; // dichiara una variabile di nome testo

numero = 10; // assegna il valore int 10 alla variabile numero
testo = "ciao"; // Assegna la stringa "ciao" alla variabile testo

var numero = 20; // Dichiara ed assegna 20 alla variabile numero
let testo = "javascript"; // Dichiara ed assegna "javascript" alla variabile testo

let numero = 10, testo ="ciao";  // Definizione multipla di variabili su singola linea
// tuttavia per aumentare la leggibilità del codice 
// è una buona pratica dichiarare/definire una variabile per linea

```

--- #slide N
 
# Variabili

Regole sintattiche

<div style="background-color:green;color:yellow;padding: 10px;">
In JavaScript il nome di una variabile è determinata dalle seguenti regole:
<ol>
  <li>il nome può contenere solo lettere, numeri, i simboli $ e _</li>
  <li>il primo carattere non può essere un numero</li>
  <li>il nome non può essere una keyword riservata</li>
</ol>
</div>  

<br />

```js
// Dichiarazioni valide
let utente;
let nomeUtente; //camelCase
let nome_utente; //snake case (https://en.wikipedia.org/wiki/Naming_convention_(programming))
let NomeUtente; // pascal case
let $;
let _;

// Dichiarazioni non valide
let 1utente; // viola regola 2
let user-name; // viola regola 1
let uten*te; // viola regola 1
let 1_user; // viola regola 2
```

--- #slide N
 
# Variabili

Regole sintattiche

 ```js
 // Dichiarazioni non valide
 let class; // viola la regola 3
 let else; // viola la regola 3
 let catch; // viola la regola 3
 let this; // viola la regola 3
 ```

<br />

- Una lista di tutte le keyword riservate si può trovare qui: [JS Keywords](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#keywords)

- Importante notare che il nome delle variabili in JS è ***case sensitive***.

```js

let apple;
let Apple;

// Sono due variabili diverse
```

--- #slide N
 
# Variabili

var vs let

- Come visto una variabile può essere dichiarata con `var` o con `let`
- Apparentemente non c'è nessuna differenza
- Si fa notare che `var` fino al 2015 era l'unico modo di dichiarare una variabile in JS
- Normalmente in JS moderno `var` non viene più utilizzato
- Tuttavia siccome è ancora ampiamente diffuso in vecchi script è importante analizzare meglio le differenze

--- #slide N
 
# Variabili

var vs let

- le variabili dichiarate con `var` non hanno uno `scope`
- In altre parole in qualsiasi parte del programma siano dichiarate diventano globali

```js
var a = 10;

console.log(`valore di a ${a}`);

if (a == 10) {
  var b = 20;
}

console.log(`b è diventata globale, infatti a + b = ${a+b}`);

//output
alore di a 10
b è diventata globale, infatti a + b = 30
```

- Come si vede la dichiarazione di b nello scope dell'if ha assunto carattere globale, appunto ignorando lo scope

--- #slide N
 
# Variabili

var vs let


```js
var a = 10;
var b = 5;

console.log(`valore di a ${a}`);

if (a == 10) {
  var b = 20;
}

console.log(`b è diventata globale, infatti a + b = ${a+b}`);

//output
alore di a 10
b è diventata globale, infatti a + b = 30
```

- In questo caso l'effetto è deleterio, la variabile globale b (con valore 5) è stata sovrascritta dentro l'if
- Questo comportamento può generare errori difficilmente debuggabili e far perdere molto tempo


--- #slide N
 
# Variabili

var vs let

```js
var i = 10;
console.log(`il quadrato di i vale ${i * i}`);

for(var i = 0; i < 3; i++) {
  console.log("ciclo");
}

console.log(`il quadrato di i vale ${i * i}`);

//output

il quadrato di i vale 100
ciclo
ciclo
ciclo
il quadrato di i vale 9 

```

--- #slide N
 
# Variabili

var vs let

- L'introduzione di `let` risolve questo tipo di problematiche
- Le variabili dichiarate con `let` hanno validità **SOLO** all'interno dello scope in cui sono definite
- Questo evita le problematiche viste prima e riduce o elimina la tipologia di bug introdotti da **var**

```js
var i = 10;
console.log(`il quadrato di i vale ${i * i}`);

for(let i = 0; i < 3; i++) {
  console.log("ciclo");
}

console.log(`il quadrato di i vale ${i * i}`);

//output
il quadrato di i vale 100
ciclo
ciclo
ciclo
il quadrato di i vale 100

```


--- #slide N
 
# Variabili

var vs let

```js
var a = 10;
var b = 5;

console.log(`valore di a ${a}`);

if (a == 10) {
  let b = 20;
}

console.log(`b è diventata globale, infatti a + b = ${a+b}`);

//output
alore di a 10
b è diventata globale, infatti a + b = 15
```
<br />

<div style="background-color:green;color:yellow;padding: 10px;">
Dichiarare e definire SEMPRE le variabili usando <mark>let</mark>
</div>  


--- #slide N
 
# Costanti

- La specifica ES6 ha introdotto anche la keyword `const` per dichiarare una costante, cioè una variabile che non può essere riassegnata, e pertanto che mantiene costante il valore assegnato.
  
<br />

```js
let numero =5;
numero =6; // riassegnazione valida

cont numero =5;
numero = 6; //genera un errore: Uncaught TypeError: Assignment to constant variable.
```

<br />

- Una pratica comunemente adottata (fortemente consigliata) in JavaScript è quella di usare le costanti per nominare dei valori difficili da ricordare.
- Questo aumenta chairamente la leggibilità del codice.
- Normalmente questo tipo di costanti viene nominato usando caratteri tutti maiuscoli e separati da underscore.

```js
const ROSSO = "#F00";
const VERDE = "#0F0";
const BLU = "#00F";

```

--- #slide N
 
# Variabili

Best Practice

- I nomi assegnati alle variabili, sicuramente poco importanti per l'interprete o compilatore, al contrario sono molto importanti per i programmatori.
- Infatti da esse si può subito comprendere se il codice è stato scritto da un principiante o da uno sviluppatore professionista.
- Al fine di aumentare la leggibilità del codice è di `fondamentale` importanza assegnare i nomi alle variabili in modo che:
  - il significato sia ovvio
  - descriva la semantica del dato che memorizza
  - sia univoca
  - sia facilmente leggibile e comprensibile da un umano
  - non rappresenti abbreviazioni o contrazioni (es: a,b, c)
  - sia concisa ma descrittiva (es: dato, valore: hanno poco significato)
  
--- 

# JavaScript e DOM

modifichiamo una pagina HTML in JS

- Prima di continuare con l'apprendimento di JS vediamo come interagire con una pagina HTML
- Come abbiamo visto in precedenza, quando il browser carica una pagina viene creato un albero degli oggetti chiamato **DOM**
- ***JavaScript può accedere e leggere o modificare qualsiasi oggetto del DOM***
- Questo è un meccanismo molto potente che permette di "dare vita" alle pagine HTML trasformandole da semplice pagine da consultare ad applicazione web interattive.
- Questo è il paradigma in uso ormai da molti anni ed estremizzato con le Progressive Web App ai nostri giorni.

<br>
<div style="background-color:green; color:yellow;padding: 20px; font-weight:bold;box-shadow:8px 8px 10px #888888;border-radius:10px;">
Progressive Web App (PWA) è un termine, coniato in origine da Google, che si riferisce ad applicazioni web che vengono sviluppate e caricate come normali pagine web, ma che si comportano in modo simile alle applicazioni native quando utilizzate su un dispositivo mobile (smartphone)
</div>
--- 

# JavaScript e DOM

modifichiamo una pagina HTML in JS

- Un metodo molto importante dell'oggeto DOM *Document* è `getElementById(<id_componente>)`
- Questo è uno dei metodi più utilizzati nella manipolazione del DOM in vanilla JS
- Il metodo restituisce **l'oggetto HTML** cha un attributo **id** pari a *<id_componente>*.

<br>

```html
...
<p class="paragrafo" id="par1">
...
```

<br>

- Se non ci sono elementi con l'id specificato, il metodo restituisce `null`
- Si ricorda che è buona prassi assegnare un id univoco ad un oggetto HTML. In caso ciò non sia rispettato, getElementById restituisce il primo oggetto in ordine di apparizione nel codice sorgente.

--- 

# JavaScript e DOM

modifichiamo una pagina HTML in JS

- Esistono anche dei metodi simili che permettono di selezionare oggetti del DOM in base a:
  - `getElementsByClassName(classname)`: il metodo restituisce una collezionedi oggetti HTML che hanno la classe css specificata
  - `getElementsByName(object name)`: il metodo restituisce una collezione di oggetti HTML che hanno il nome specificato

<br>

```js
let paragrafo = document.getElementsByName("paragrafo");
NodeList [p#par1]0: p#par1length: 1[[Prototype]]: NodeList

let elements = docuement.getElementsByClassName("w3-bar");
HTMLCollection(2) [div.w3-bar.w3-card-2.notranslate, div.w3-bar.w3-left]
  0: div.w3-bar.w3-card-2.notranslate
  1: div.w3-bar.w3-left
  length: 2
  [[Prototype]]: HTMLCollection

```

--- 

# JavaScript e DOM

modifichiamo una pagina HTML in JS

- Una volta ottenuto l'oggetto HTML possiamo manipolarne qualsiasi suo aspetto in JS

<div class="grid grid-flow-col auto-cols-max gap-4">
<div>

```html
<p id="par1">
  Questo è un paragrafo di testo in una pagina HTML
</p>
<button onClick="cambia_stile">Premi qui!</button>
```
<br>

```js
function cambia_stile(){
  let el = document.getElementById("par1"); 
  el.style.color = "white";
  el.style.background = "green";
  el.style.padding = "10px";
  el.innerHTML="Questo è un paragrafo che non 
  esiste <br> nella pagina HTML, è stato 
  inserito dinamicamente <br>da JavaScript.";
}
```

</div>

<div>
<p id="par1">Questo è un paragrafo di testo in una pagina HTML</p>
<button  style="border: 1px solid black; border-radius: 5px; background-color:lightgray; padding: 5px;" onclick="let el=document.getElementById('par1'); el.style.color='white';el.style.background='green';el.style.padding='10px';el.innerHTML='Questo è un paragrafo che non esiste <br> nella pagina HTML, è stato inserito dinamicamente <br>da JavaScript.'">Premi qui!</button>
</div>
</div>

--- 

# JavaScript e DOM

modifichiamo una pagina HTML in JS

- Vediamo altri esempi:

<div class="grid grid-flow-col auto-cols-max gap-4">
<div>

```html
<h1 id="t1">Titolo 1</h1>
<h1 id="t2">Titolo 2</h1>
<h1 id="t3">Titolo 3</h1>
<h1 id="t4">Titolo 4</h1>
<button onClick="cambia_DOM">Premi qui!</button>
```
<br>

```js
function cambia_DOM(){
  let obj_t1 = document.getElementById("t1");
  let obj_t2 = document.getElementById("t2");
  let obj_t3 = document.getElementById("t3");
  let obj_t4 = document.getElementById("t1"); 
  
  obj_t1.innerHTML = "TITOLO UNO";
  obj_t2.style.color = "#88ccaa";
  obj_t3.innerHTML = "TITOLO TRE";
  obj_t4.style.text-decoration = "underline";
}
```

</div>

<div>
<h1 id="t1">Titolo 1</h1>
<h1 id="t2">Titolo 2</h1>
<h1 id="t3">Titolo 3</h1>
<h1 id="t4">Titolo 4</h1>

<button  style="border: 1px solid black; border-radius: 5px; background-color:lightgray; padding: 5px;" onclick='let obj_t1 = document.getElementById("t1");let obj_t2 = document.getElementById("t2");let obj_t3 = document.getElementById("t3");let obj_t4 = document.getElementById("t4");obj_t1.innerHTML = "TITOLO UNO";obj_t2.style.color = "#FF0000";obj_t3.innerHTML = "TITOLO TRE";obj_t4.style.textDecoration = "underline";'>Premi qui!</button>
</div>
</div>

--- 

# JavaScript e DOM

modifichiamo una pagina HTML in JS

- Vediamo altri esempi:

<div class="grid grid-flow-col auto-cols-max gap-4">
<div>

```html
<h1 class="titolo_pari">Titolo Pari</h1>
<h1 class="titolo_disp">Titolo Dispari</h1>
<h1 class="titolo_pari">Titolo Pari</h1>
<h1 class="titolo_disp">Titolo Dispari</h1>
<button onClick="cambia_DOM">Premi qui!</button>
```
<br>

```js
function cambia_DOM(){
  let pari = document.getElementsByClassName("titolo_pari");
  let disp = document.getElementsByClassName("titolo_disp");
  for(let i = 0; i < pari.length; i++) {
    let el = pari[i];
    el.style.backgroundColor = "red";
  }
  for(let j = 0; j < disp.length; j++) {
    let el = disp[j];
    el.style.backgroundColor = "green";
  }
}
```

</div>

<div>
<h1 class="titolo_pari">Titolo Pari</h1>
<h1 class="titolo_disp">Titolo Dispari</h1>
<h1 class="titolo_pari">Titolo Pari</h1>
<h1 class="titolo_disp">Titolo Dispari</h1>

<button  style="border: 1px solid black; border-radius: 5px; background-color:lightgray; padding: 5px;" onclick='let pari = document.getElementsByClassName("titolo_pari");let disp = document.getElementsByClassName("titolo_disp");for(let i = 0; i < pari.length; i++) {let el = pari[i];el.style.backgroundColor = "red";}for(let j = 0; j < disp.length; j++) {let el = disp[j];el.style.backgroundColor = "green";}
'>Premi qui!</button>
</div>
</div>


--- #slide N
 
# Esercizio js_04

modifichiamo una pagina HTML in JS

Dato il seguente script JS

1. Dato il file [esercizio_js_04.html](../support/esercizio_js_04.html) rinominarlo in |cognome|_esercizio_js_04.html
2. Aggiungere il file |cognome|_esercizio_js_04.js e definire una funzione chiamata ***modifica_stile*** in modo che:
   - tutti i titoli di primo livello abbiano un colore di foreground rosso
   - tutti i titoli di secondo livello abbiano un colore di foreground blue su sfondo giallo
   - tutti i titoli di secondo livello abbiano la dimensione del font pari a 40px 
   - tutti i titoli di secondo livello siano scritti solo in maiuscolo (usa il metodo `.toUpperCase()`)
   - il primo ed il quarto paragrafo abbiano un colore del testo (foreground) rosso
   - il secondo, quinto e ottavo paragrafo abbiano uno sfondo verde leggero
   - il terzo paragrafo sia scritto tutto in maiuscolo ed lo sfondo si un blue leggero
   - il sesto paragrafo sia scritto tutto in maiuscolo
   - il settimo paragrafo abbia uno stile del font *italico*
3. Fornire il link github al file con nome *|cognome|_esercizio_js_04.html*  e *|cognome|_esercizio_js_04.js*

--- #slide N
 
# Creiamo un elemento

Creare oggetti HTML in JS

- L'oggetto *document* del DOM mette a disposizione vari metodi
- Uno molto utile è `createElement("<element tag>"`
- Questo metodo crea un oggetto o elemento HTML identificato dal suo tag

Esempio:

```js
let h1 = document.createElement("h1"); //crea un oggetto h1
 
let h1_1 = document.createElement("h1"); //crea un'altro oggetto h1

let p = document.createElement("p"); //crea un oggetto di tipo p

```
<br />

- Da notare che il metodo *createElement* crea l'oggetto ma non lo aggiunge al DOM
- Importante ricordarsi che questo metodo crea un oggetto vuoto esattamente come se in html scrivessimo 
  
```html
<h1></h1>
```
  
--- #slide N
 
# Creiamo un elemento

Creare oggetti HTML in JS

- Pertanto per aggiungere un contenuto all'oggetto appena creato possiamo usare le proprietà o attributi:
  - ***innerTexT***: imposta il contenuto testuale dell'oggetto
  - ***innerHTML***: imposta il contenuto dell'oggetto considerando la sintassi HTML

Esempio:

```js
h1.innerText = "Titolo 1";
h1_1.innerHTML = "<u>Titolo 1_1</u>";
p.innerText = "Questo è un paragrafo";

```

--- #slide N
 
# Aggiungiamo un elemento

Aggiungere oggetti HTML al DOM in JS

- Per aggiungere un nuovo elemento al DOM dobbiamo utilizzare il metodo `append` dell'oggetto body
- Questo perchè sappiamo dall'HTML che tutti gli elementi sono *figli* di body
- Pertanto per aggiungere un nuovo elemento facciamo l'append in questo modo

<br />

```js
const body = document.body; //creo una referenza all'oggetto body

body.append(h1); //aggiunge l'oggetto h1 al body del documento
body.append(h1_1); //aggiunge l'elemento h1_1 al body del documento
body.append(p);//aggiunge l'elemento p al body del documento

```

--- #slide N
 
# Aggiungiamo un elemento

<img src="/media/js08.png" width="600" style="margin:auto;"/>

--- #slide N
 
# Rimuoviamo un elemento

Rimuovere oggetti HTML dal DOM in JS

- Per rimuovere un nuovo elemento dal DOM utilizziamo il metodo `remove()`
- In questo modo l'oggetto che invoca il metodo, viene rimosso dal DOM e pertanto non più visualizzato
- Nota che l'oggetto non viene distrutto e può essere riaggiunto in seguito

```js
h1.remove(); //rimuove l'oggetto h1 dal body del documento
h1_1.remove(); //rimuove l'elemento h1_1 dal body del documento
p.remove();  //rimuove l'elemento p dal body del documento
```  

--- #slide N

# Aggiunta di elementi nested

Creiamo una lista in JS

- Il metodo visto per la creazione i vusalizzazione di elementi HTML in modo dinamico è utilissimo nella creazioni di Web App
- Immaginiamo di voler visualizzare la lista degli studenti di una classe provenienti da un DataBase
- Il contenuto della lista non è noto quando scriviamo il markup della pagina HTML
- Pertanto creeremo la lista in modo dinamico a runtime tramite JavaScript
- Questo metodo è alla base dello sviluppo delle applicazioni Web e PWA

--- #slide N

# Aggiunta di elementi nested

Creiamo una lista in JS

```html
<body>
    <h1>Pagina Vuota</h1>
    <input id="cognome" type="text" placeholder="Cognome Studente"/>
    <button onclick="add_studente()">Aggiungi uno studente</button>
    <ul id="lista"></ul>
</body>
```

<br />

```js
function add_studente() {
            const ul = document.getElementById("lista");
            const cognome_str = document.getElementById("cognome").value;
            const li = document.createElement("li");
            li.innerText = cognome_str;
            ul.append(li);
        }
```

- Vedi esempio [empty_list.html](../support/empty_list.html)

---

# Interagiamo con l'utente

alert

- Spesso è utile fornire un feedback all'utente ed assicurarsi che venga recepito
- In questi casi si può utilizzare la funzione `alert("messaggio")` per visualizzare una **finestra modale** che mette tutta la pagina in attesa della pressione del tasto ***OK***

```js
alert("Assicurati di leggere le condizioni contrattuali");
```

<br />
<img src="/media/js11.png"  style="margin:auto;"/>

- La pagina rimane "bloccata" fino a che l'utente premte il pulsante OK
- In questo modo siamo sicuri che se l'utente procede nella consultazione della pagina ha volontariamente premuto il pulsante OK e pertanto si assume che abbia letto il messaggio.
---


# Interagiamo con l'utente

prompt

- La funzione `prompt("Messaggio", ["Valore di default"])` visualizza una finestra modale con una stringa ("Messaggio") e un input field. In questo caso ci sono due bottoni **OK** e **Cancel**
- La funzione restituisce:
  -   **null** in caso il pulsante Cancel/Annulla è premuto
  -   **"Valore di default"** in caso in cui l'utente non inserisce nessun input e preme OK
  -   **<valore inserito dall'utente>** in caso in cui l'utente inserisce un input e preme ok 
- Pertanto normalmente la funzione prompt si usa in un'assegnazione

```js
let risultato = prompt("Come ti chiami?", "Pinco Pallo");

console.log(risultato);

Mario // utente ha inserito Mario e premuto OK
Pinco Pallo // utente ha solo premuto OK
null // utente a premuto Cancel/Annulla o il tasto ESC
```
---

# Interagiamo con l'utente

prompt

```js
let risultato = prompt("Come ti chiami?", "Pinco Pallo");
if(risultato) {
    alert(`L'utente si chiama ${risultato}`);
} else {
    alert("L'utente non ha inserito il suo nome");
}
```
<br />
<div  style="display: flex; justify-content: center;">
<img src="/media/js12.png" width="350" style="float:left"/>
<img src="/media/js13.png" width="450" />
</div>
---

# Interagiamo con l'utente

confirm

- La funzione `confirm("Messaggio")` visualizza una finestra modale con il messaggio e due bottoni **OK** e **Cancel/Annulla**
- La funzione resitutisce un valore boolean in base al tasto premuto ***OK->true e Cancel -> false***

```js
let conferma = confirm("Hai letto le condizioni contrattuali?");
console.log(conferma);

// true se l'utente preme OK
// false se l'utente preme Cancel o Annulla
```

<br />
<img src="/media/js14.png" width="450" style="margin: auto;"/>

--- #slide N
 
# Esercizio js_05

Aggiungiamo elementi dinamici


1. Dato il file [empty.html](../support/empty.html) rinominarlo in |cognome|_esercizio_js_05.html ed aggiungere il riferimento al file |cognome|_esercizio_js_05.js
2. Creare una pagina HTML e il relativo codice JS in modo che:
   - Vengano richiesti all'utente il nome e la media dei voti di uno studente
   - Alla pressione di un bottone il nome e la media inseriti vengano aggiunti ad una linea di una tabella
   - Alla pressione di un secondo bottone, tutte le linee pari vengano colorate di blue e tutte le linee dispari di rosso
3. Fornire il link github al file con nome *|cognome|_esercizio_js_05.html*  e *|cognome|_esercizio_js_05.js*

--- #slide N
 
# Modifichiamo la classe di un elemento

CSS dinamico in JS

- Oltre a modificare il testo e il contenuto di un elemento HTML può essere utile modificare il suo stile in modo dinamico
- Per far ciò in modo agevole, il metodo pi+ utilizzato e l'aggiunta o la rimozione di una o più classi CSS ad un elemento
- In tal modo da JS si può facilmente variare l'aspetto di un elemento in funzione di specifici stati della logica della pagina
- Ogni elemento HTML ha una proprietà chiamta `classList` che fornisce la lista delle classi CSS applicate all'elemento stesso

```js
ul.classList
DOMTokenList(3) ['bordo', 'rosso', 'verde', value: 'bordo rosso verde']
0: "bordo"
1: "rosso"
2: "verde"
length: 3
value: "bordo rosso verde"
``` 

--- #slide N
 
# Modifichiamo la classe di un elemento

CSS dinamico in JS

- L'oggetto restituito da *classList* mette a disposizione tre metodi molto utili:
  - `add("<classe>")`: aggiunge una classe alla lista delle classi CSS applicate all'elemento
  - `remove("<classe>")`: rimuove una classe dalla lista delle classi CSS applicate all'elemento
  - `toggle("<classe>")`: se la classe è presente la rimuove, mentre se non è presente l'aggiunge

```js
ul.classList
DOMTokenList [value: '']

ul.classList.add("verde")
ul.classList.toggle("bordo")
DOMTokenList(2) ['verde', 'bordo', value: 'verde bordo']

ul.classList.toggle("bordo")
DOMTokenList ['verde', value: 'verde']

ul.classList.remove("verde")
DOMTokenList [value: '']

```

- Vedi esempio [empty_list_class.html](../support/empty_list_class.html)

--- #slide N
 
# Esercizio js_06

Aggiungiamo elementi dinamici


1. Partendo dai file |cognome|_esercizio_js_05.html e |cognome|_esercizio_js_05.js modificarli in modo che:
   - Sia presente un bottone "Grassetto" che se premuto faccia diventare tutti gli elementi della lista in grassetto
   - Sia presente un bottone "Blue" che se premuto faccia diventare tutti gli elementi della lista di colore Blue
   - Sia presente un bottone "Bordo" che se premuto faccia comparire un bordo attorno alla lista in caso non sia presente e rimuova tale bordo in caso sia già presente
   - Ogni modificazione allo style deve avvenire tramite una o più classi CSS
2. Fornire il link github al file con nome *|cognome|_esercizio_js_06.html*  e *|cognome|_esercizio_js_06.js*

--- #slide N
 
# Esercizio js_07

Rubrica JS

<img src="/media/js14_a.png" style="margin: auto;"/>

--- #slide N
 
# Esercizio js_07

Rubrica JS


Partendo dai template [rubrica_js_template.html](../support/rubrica_js_template.html) e [rubrica_js_template.css](../support/rubrica_js_template.css), si richiede di realizzare una web app (in Js vanilla) che implementa una rubrica telefonica con le seguenti funzionalità:

1. L'utente può inserire un nuovo contatto in rubrica (pulsante 2) se tutti i campi sono forniti, altrimenti deve visualizzare un messaggio di allerta con testo appropriato 
2. L'utente può rimuovere un contatto presente in rubrica  premendo il pulsante 3
3. L'utente può cercare un contatto in rubrica per cognome o numero di telefono tramite pulsante 1.
4. Il contatto ricercato viene visualizzato nella parte superiore dell'interfaccia in modo che sia possibile modificarne i suoi campi e successivamente aggiornare la rubrica tramite il pulsante 2
5. Consegnare su github i file dell'applicazione rispettivamente nominati *|cognome|_esercizio_js_07.html*,  *|cognome|_esercizio_js_07.css* e *|cognome|_esercizio_js_07.js*

--- #slide N
 
# Esercizio js_08

ToDo JS

<img src="/media/js14_b.png" style="margin: auto;"/>

--- #slide N
 
# Esercizio js_08

ToDo JS


Si richiede di realizzare una web app (in Js vanilla) che implementa una ToDo list con le seguenti funzionalità:

1. L'utente può inserire un nuovo ToDO item e selezionare la priorità tra 3 livelli (Bassa, Media, Alta) se tutti i campi sono forniti, altrimenti deve visualizzare un messaggio di allerta con testo appropriato 
2. L'utente inserisce un nuovo ToDo item premendo l'icona 1
3. Una volta inserito un nuovo ToDO Item, viene visualizzato in modo che la priorità sia rappresentata da un'icona diversa per i 3 livelli di priorità (vedi figura)
4. L'utente può marcare il ToDo Item come completo/attivo tramite click sull'icona 2. In caso di item completato il testo del ToDo Item deve essere barrato (vedi figura). In caso di item attivo il testo deve essere senza barra
5. L'utente può rimuovere un ToDo item completo o no premendo l'icona 3
6.  Consegnare su github i file dell'applicazione rispettivamente nominati *|cognome|_esercizio_js_08.html*,  *|cognome|_esercizio_js_08.css* e *|cognome|_esercizio_js_08.js*

--- 

# Data Types

Tipi di dato

- Java Script definisce 7 tipi di dato
  1. **Number**
  2. **BigInt**
  3. **String**
  4. **Boolean**
  5. **null**
  6. **undefined**
  7. **object**

--- #slide N
 
# Data Types

Number

- Rappresenta sia numeri interi che decimali (floating point) nel formato IEEE-754 a 64 bit

<br />

```js
let intero = 12833; // definizione valida
let decimale = 19.34; // definizione valida
```
<br />

- JavaScript è intelligente e riesce a gestire tipi diversi in maniera flessibile

<br />

```js
let n1 = 10; // definizione valida
let n2 = 10.3; // definizione valida
let n3 = 10.0;

> n1 == n2
false
> n2 == n3
false
> n1 == n3
true
```

--- #slide N
 
# Data Types

Number

- JavaScript definisce alcuni `special numeric value`:
  - `Infinity`: rappresenta il concetto di infinito. E' un valore speciale maggiore di qualsiasi altro Number. 
  - `-Infinity`: viceversa rappresenta il concetto di - infinito.E' un valore speciale minore di qualsiasi altro Number
  - `NaN`: **Not a Number** rappresenta un errore computazionale, il risultato di un'operazione  matematica incorretta o indefinita.

<br />

```js
> 1/0
Infinity
> console.log(Infinity)
Infinity
> console.log(-Infinity)
-Infinity
> "ciao" / 2
NaN
> 5 * "ciao"
NaN
```

--- #slide N
 
# Data Types

Number

- JavaScript ci permette di rappresentare i numeri in modi diversi

```js
> let bilion1 = 1000000000
> let bilion2 = 1_000_000_000
> let bilion3 = 1e9
> bilion1 == bilion2
true
> bilion2 == bilion3
true
> bilion1 == bilion3
true

> let nano1 = 0.000000001
> let nano2 = 1e-9
> let nano3 = 0.000_000_001
> nano1 == nano2
true
> nano2 == nano3
true
> nano1 == nano3
true
```

--- #slide N
 
# Data Types

Number

- Anche i numeri da informatici (esadecimale e binario) possono essere rappresentati facilmente

```js
> let h1 = 0xab
> let h2 = 0xAB
> h1 == h2
true

> let b1 = 0b11111111
> let o1 = 0o377
> let d1 = 255
> b1 == o1
true
> o1 == d1
true
> b1 == d1
true
```

--- #slide N
 
# Data Types

Number

- JavaScript mette a disposizione il metodo `toString(base)` che restituisce una stringa del numero in base &nbsp;`<base>`

```js
let n = 255
> n.toString(2)
'11111111'
> n.toString(16)
'ff'
> n.toString(8)
'377' // facile, no? :)

> 255.toString(2)
Uncaught SyntaxError: Invalid or unexpected token

255..toString(2) 
'11111111'

> (255).toString(2) //nota il .. o () per applicare il metodo ad un numero e non una variabile
'11111111'

```

--- #slide N
 
# Data Types

Number

- JavaScript mette a disposizione 4 metodi per arrotondare un numero:
  - **Math.floor**: restituisce il numero intero più grande minore o uguale al numero da arrotondare
  - **Math.ceil**:  restituisce il numero arrotondato al numero intero più grande maggiore del numero dato

<br />

```js
//floor 
> Math.floor(3.6)
3
> Math.floor(-3.6)
-4

//ceil
> Math.ceil(3.6)
4
> Math.ceil(-3.6)
-3
```

--- #slide N
 
# Data Types

Number

- JavaScript mette a disposizione 4 metodi per arrotondare un numero:
  - **Math.round**: arrotonda il numero all'intero più vicino
  - **Math.trunc**:  restituisce la parte intera del numero dato

<br />

```js
//round
> Math.round(3.6)
4
> Math.round(3.3)
3
> Math.round(-3.6)
-4
> Math.round(-3.3)
-3
//trunc
> Math.trunc(3.6)
3
> Math.trunc(-3.6)
-3
```

--- #slide N
 
# Data Types

Number

- Riassumiamo i metodi di arrotondamento

<br />

|      | Math.floor | Math.ceil | Math.round | Math.trunc |
| ---- | ---------- | --------- | ---------- | ---------- |
| 3.1  | 3          | 4         | 3          | 3          |
| 3.6  | 3          | 4         | 4          | 3          |
| -1.1 | -2         | -1        | -1         | -1         |
| -1.6 | -2         | -1        | -2         | -1         |


--- #slide N
 
# Data Types

Number

- JavaScript mette a disposizione il metodo `toFixed(cifre)` che permette di arrotondare un numero ad un numero specifico di cifre

<br />

```js
> let d1 = 124.4533442;

> d1.toFixed(3)
'124.453'
> d1.toFixed(2)
'124.45'
> d1.toFixed(1)
'124.5'
> d1.toFixed(0)
'124'

```

--- #slide N
 
# Data Types

BigInt

- Il tipo *Number* può rappresentare numeri nel range [da - 2<sup>53</sup> a 2<sup>53</sup>]
- Normalmente questo è un range sufficiente per la maggior parte delle situazioni
- Se serve rappresentare numeri al difuori di questo range, si può ricorrere al tipo `BigInt`
- **BigInt** può avere una lunghezza arbitraria aggiungendo `n` al termine del numero intero

<br />

```js
let large = 1234567890098765432112345678900987654321n;

> large + 1
Uncaught TypeError: Cannot mix BigInt and other types, use explicit conversions
> 
> 
> large + 1n
1234567890098765432112345678900987654322n

```

--- #slide N
 
# Data Types

String

- Una stringa è una successione di caratteri ascii. Tuttavia il tipo ***carattere*** non esiste.
- In JS una stringa può essere racchiusa tra:
  - "stringa": Doble quotes o virgolette
  - 'string': Single quote o apici
  - \`stringa con dentro un altra ${stringa}\`: Backticks

- Single e Double quotes non hanno nessuna reale differenza e possono essere utilizzati in modo intercambiabile, ma non mixati insieme
- "stringa" è valido
- 'stringa' è valido
- "stringa' **non** è valido

--- #slide N
 
# Data Types

String

- Il Backtick serve per includere una stringa una variabile che verrà poi sostuituita con il suo valore a run-time

<br />

```js
let nome = "Mario";
let cognome = "Rossi";
console.log(`Il sig. ${nome} ${cognome} è presente`); 
//stampa Il sig. Mario Rossi è presente

let altezza = 160;
console.log(`Il sig. ${nome} ${cognome} è alto ${altezza} cm`); 
//stampa Il sig. Mario Rossi è alto 160 cm

let b =  10;
let h = 20;
console.log(`Il rettangolo ha area pari a ${b * h} cm2`); 
// stampa Il rettangolo ha area pari a 200 cm2
```


--- #slide N
 
# Data Types

Boolean

- Il tipo boolean rappresenta uno stato logico è può assumere solo due valori:
  - `true` : vero
  - `false` : falso

<br />

```js
let isOpen = false;
let isClosed = true;
let isBigger = 5 > 2; // true
let isEqual = 3 == 2; //false

```

--- #slide N
 
# Operatori Logici

I 4 operatori booleani

- `||` : OR logico
- `&&` : AND logic
- `!` : NOT logico
- `??`: Nullish coalescing operator

- funzionano esattamente come in C/C++ e Java

```js
true || true -> true
true || false -> true
false || true -> true
false || false -> false
true && true -> true
true && false -> false
false && true -> false
false && false -> false
!true -> false
!false -> true
```

--- #slide N
 
# Operatori Logici

I 4 operatori booleani

- Tuttavia in JS gli operatori logici non si applicano solo a valori Booleani
- Funzionano con qualsiasi tipo e sono molto potenti

```js
1 || 0 -> 1
0 || 1 -> 1
0 || 3 -> 3
"ciao" || 1  -> ciao
"" || 1  -> 1

"ciao" || "mario" || "rossi" -> "ciao"
"" || "mario" || "rossi" -> "mario"
"" || "" || "rossi" -> "rossi"
```

Quindi spesso l'operatore || viene spesso usato per trovare il primo valore vero o impostare un default

```js 
let nome = ""; let cognome = "";
let utente = nome || cognome || "anonimo"; --> anonimo

let nome = "";let cognome = "Rossi";
let utente = nome || cognome || "anonimo"; --> Rossi
```

--- #slide N
 
# Operatori Logici

I 4 operatori booleani

- Importante notare che viene applicato il principio di `short-circuit evaluation`
- In altre parole un espressione con l'operatore ||, partendo da sinistra valuta tutte le espressioni finchè ne trova una vera
- Non appena trova un espressione vera la valutazione viene interrotta

```js
prompt("Come ti chiami?") || alert("Non hai inserito nessun nome");
```

- Se l'utente al prompt inserisce una stringa (il suo nome) allora l'espressione dopo || non viene valutata e quindi l'alert non visdualizzato
- Se l'utente non inserisce una stringa, il risultato del prompt è falso pertanto l'espressione dopo || viene valutata e quindi eseguita

Il codice è equivalente a: 

```js
if (prompt("Come ti chiami?") == false) {
  alert("Non hai inserito nessun nome")
}
```

--- #slide N
 
# Operatori Logici

I 4 operatori booleani

- Anche l'operatore && si applica a tutti i tipi e non solo quelli booleani
- Pertanto questo operatore trova il primo valore falso
- Infatti le esperesisoni vengono valutate da sinistra a destra fino a che ne trova una falsa. A questo punto le successive espressioni non sono valutatre
- Se sono tutte vere restiusce il valore dell'ultima espressione

```js
1 && 0 -> 0
1 && 6 -> 6
1 && 6 && 0 -> 0
11 && 0 && 6 -> 0

let nome = "Mario";
let cognome = "Rossi";
let utente = nome && cognome && nome + cognome;

if (nome && cognome) {
  utente = nome + cognome;
}
```


--- #slide N
 
# Operatori Logici

I 4 operatori booleani

- Importante notare che l'operatore **&&** ha una priorità superiore all'operatore **||**
  
```js
a && b || c && dd -> (a && b) || (c && d)

a && b && c && dd -> ((a && b) && c) && d

a || b && c || d -> (a || (b && c)) || d
```

<br />

- Bisogna fare sempre molta attenzione alla precedenza degli operatori, specie in espressioni complesse

- Esiste un uso di && per compattare il codice ma in genere riduce la leggibilità del codice

```js
let x = 1;

(x > 0) && alert("il valore è maggiore di zero");

if (x > 0) alert("il valore è maggiore di zero");

```

--- #slide N
 
# Operatori Logici

I 4 operatori booleani

- L'operatore **!** ha la precedenza maggiore di tutti
- Pertanto la precedenza degli operatori è: `!` -> `&&` -> `||`

```js
!a && b -> (!a) && b

a && b || !c -> (a && b) || (!c)
```

--- #slide N
 
# Operatori Logici

I 4 operatori booleani

- L'operatore **??** chiamato *Nullish coalescing operator* verifica se il primo operando è definito (esiste ed ha un valore valido)
- In caso positivo restituisce la prima espressiome altrimenti la seconda

```js
a ?? b -> restituisce a se è valida e definita altrimenti b
"ciao" ?? false -> "ciao"
undefined ?? "errore" -> "errore"

let user;
alert(user ?? "utente invalido") -> "utente invalido"
user = "Mario Rossi";
alert(user ?? "utente invalido") -> "Mario Rossi"

let result = a ?? b;

let result;
if (a ! = null && a ! = undefined) //no spazio tra ! e =
  reult = a;
else
  result = b;
```

--- #slide N
 
# Esercizio js_09

Operatori Booleani

1. Creare una pagina HTML con il relativo Javascript, usando **prompt() e alert()**, che richieda delle credenziali di login Username e Password in base alla seguente logica:

<img src="/media/js09.png" width="400" style="margin: auto;"/>
<br />

1. Fornire il link github al file con nome *|cognome|_esercizio_js_07.html*  e *|cognome|_esercizio_js_07.js*


--- #slide N
 
# Data Types

null

- JS definisce un valore speciale chiamato `null`

<br />

```js
let age = null; // la variabile age ha un valore non noto
```
<br />


- In JavaScript `null` non è un puntatore nullo come in C o altri linguaggi
- `null` è un valore speciale che definisce il valore di una variabile come "niente", "vuoto" o ancor meglio ***valore non noto***

--- #slide N
 
# Data Types

undefined

- In modo simile a null, JS definisce un valore speciale chiamato `undefined`
- Un valore ***undefined*** significa che la variabile ha un ***valore non assegnato***

<br />

```js
let age; // la variabile ha un valore non definito

```

--- #slide N
 
# Operatori Base

operatore unario

- Un operatori si dice ***unario*** quando viene applicato ad un singolo operando

```js
let x = 1;

x = -x; // - è un operatore unario che inverte il segno del suo operando

let y = 3;

let z = y - x; // - è l'operazione di sottrazione ed ha 2 operandi y e x

```


--- #slide N
 
# Operatori Base

operatore unario

- Tuttavia l'operatore ***+*** ha anche una versiona unaria

```js
let x = 1;
let y = -3;

console.log(+1); // 1 nessun effetto
console.log(+y) // -3 nessun effetto

let str1 = "5";
let str2 = "4";
console.log(+str1 + +str2); // 9 
console.log(Number(str1) +  Number(str2)) // 9
```

- Pertanto l'operatore unario + converte il suo operando in numero

```js
console.log(+true) // 1
console.log(+undefined) // NaN

```

--- #slide N
 
# Operatori Base

Operatori matematici

- Gli operatori matematici binari sono i seguenti:
  - `+`: addizione
  - `-`: sottrazione
  - `*`: moltiplicazione
  - `\`: divisione (non intera)
  - `%`: resto della divisione intera
  - `**`: elevamento a potenza

```js
6 / 4 // 1.5

5 % 2 // 1  
8 % 3 // 2 
6 % 3 // 0

2**3 // 8

36**(1/2) // 6
```

--- #slide N
 
# Operatori Base

Precedenze

- Gli operatori hanno una precedenza
- Gli operatori matematici rispettano la precedenza convenzionale
- La tabella completa delle precedenze è disponibile qui 

[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence)

- Come si può vedere + unitario ha precedenza sul + binario

--- #slide N
 
# Operatori Base

operatori di assegnazione

- L'operatore `=` è l'operatore di assegnazione
- Genericamente l'espresisone di assegnazione si rappresenta così

```js
let left-value = right-value;
```

dove **left-value** rappresenta una variabile a cui viene assegnato il valore dell'espressione **right-value**

- Siccome **=** è un operatore(a differenza di altri linguaggi (C/C++)) l'assegnazione restituisce un valore che coincide con il right-value dell'espressione

- Pertanto l'assegnazione

```js
let left-value = right-value;
```

- assegna right-value alla variabile left-value e restituisce right-value


--- #slide N
 
# Operatori Base

operatori di assegnazione

```js
let a = 10; 
let b = 20;
let str = "dieci";

let b = c = d = 1; 
// 1 viene assegnato a d che restituisce 1 che viene assegnato a c 
// che restitutisce 1 che viene assegnato a b

let c = 4 + (a = b - 3)  // 21
// ad a viene assegnato il valore b - 3 (17) che viene sommato a 4 

console.log(a); // 17

console.log(b); // 20

console.log(c); // 21
```

--- #slide N
 
# Operatori Base

modify-in-place operator

```js
let n = 4;
n = n + 2; // 6
n = n * 2; // 12

let n = 4;
n += 2; // 6 (n = n + 2)
n *= 2; // 12 (n = n * 2)
n -= 3; // 9 (n = n - 3)
n /= 3; // 3 (n = n / 3)
```

--- #slide N
 
# Operatori Base

increment/decrement operators prefisso e postfisso

- Esattamente come in C/C++ gli operatori unari **++** e **--** hanno due forme:
  - **prefissa**: l'operatore in forma prefissa prima viene applicato e poi restrituisce il nuovo valore calcolato
  - **postfissa**: l'operatore in forma postfissa restituisce l'operando passato e poi calcola il nuovo valore

FORMA PREFISSA  

```js
let n = m = 2;
n = n + 1;
m = m - 1;
console.log(n); // 3
console.log(m); //2

//lo stesso codice può essere scritto usando l'operatore in forma prefissa

let n = m = 2;
console.log(++n); // 3 l'operatore ++ prefisso prima incrementa il valore e poi lo restituisce
console.log(--m); // 1 l'operatore -- prefisso prima decrementa il valore e poi lo restituisce
```

--- #slide N
 
# Operatori Base

increment/decrement operators prefisso e postfisso

- Esattamente come in C/C++ gli operatori unari **++** e **--** hanno due forme:
  - **prefissa**: l'operatore in forma prefissa prima viene applicato e poi restrituisce il nuovo valore calcolato
  - **postfissa**: l'operatore in forma postfissa restituisce l'operando passato e poi calcola il nuovo valore

FORMA POSTFISSA  

```js
let n = m = 2;
console.log(n); // 2
n = n + 1;

console.log(m); // 2
m = m - 1;

//lo stesso codice può essere scritto usando l'operatore in forma postfissa

let n = m = 2;
console.log(n++); // 2 l'operatore ++ postfisso restituisce il valore prima di incrementarlo 
console.log(m--); // 2 l'operatore -- postfisso restituisce il valore prima di decrementarlo 
```

--- #slide N
 
# Data Types

Operatore typeof

- L'operatore `typeof(arg)` resitutisce il tipo associato all'argomento *arg*.
- E' utile per verificare il tipo di una variabile ed agire di conseguenza o semplicemente fare una verifica sul tipo usato. 

```js
typeof(undefined) // "undefined"

typeof(0) // "number"

typeof(2.34) // "number"

typeof(10n) // "bigint"

typeof(true) // "boolean"

typeof("foo") // "string"

let user = { nome: 'Mario', cognome: 'Rossi' };

typeof(user) //"object"

```

--- #slide N
 
# Data Types

Conversione o Casting

- Nella maggioranza dei casi i tipi vengono convertiti automaticamente in JS
- Per esempio la funzione alert converte il suo parametro in una stringa per poterlo visualizzare correttamente

```js
alert("hello world!"); // no casting questa è già una string
alert(10); //converte 10 in "10" per poterlo visualizzare
alert(11+4); //valuta l'espressione e il risultato viene convertito in stringa. 
Cosa viene visualizzato?

// ci sono anche alcune doppie conversioni
alert("12" / "4") // "3"

//e alcune eccezioni

alert("12" + "4") // "124"

```

<br />
<div style="background-color: green;color: white;padding: 10px;">
NOTA: l'operatore + è l'operatore di concatenazione di stringhe
</div>
--- #slide N
 
# Data Types

Conversione o Casting

- Se invece vogliamo o abbiamo la necessità di convertire a stringa usiamo la funzione `String(<valore>)` che restituisce una rappresentazione di valore come stringa

```js
String(11 + 4) // "15"

String(true) // "true"

String(NaN) // "NaN"

```


--- #slide N
 
# Data Types

Conversione o Casting

- Possiamo anche convertire un valore in numero tramite la funzione `Number(<valore>)`

```js
Number("3") // 3

Number("     6      ") // 6

Number("3" + "2") // 32

Number("3" / "2") // 1.5

// casi notevoli

Number(undefined) // NaN

Number(null) // 0

Number(true) // 1

Number(false) // 0

Number("") // 0
```

--- #slide N
 
# Data Types

Conversione o Casting

-  Possiamo anche convertire un valore in boolean tramite la funzione `Boolean(<valore>)`

```js
Boolean(1) // true

Boolean(0) // false

Boolean("ciao") // true

Boolean("") // false

Boolean(null) // false

Boolean(undefined) // false

Boolean(NaN) // false
```

---

# Confronti

operatori di confronto

- In JavaScript, sono presenti i comuni operatori di confronto con un comportamento identico al C/C++ e molto altri linguaggi
- Questi operatori sono utilizzati per creare delle espressioni logiche che resitutisco un valore **Boolean**
- Pertanto un'espressione di confronto può resitutire o **True** o **False**

```js
let a = 10;
let b = 7;
let c = 2;

console.log(a > b); // true
console.log(a > = b); // true
console.log(b < a); // true
console.log(b < = a); // true 
console.log(a == b); // false
console.log(a ! = c); // true
```

<div style="background-color:green;color:yellow;padding:10px;margin-top:20px;">
NOTA: per ragioni grafiche è presente uno spazio, ma in JavaScrip va rimosso 
<mark>a  >= b</mark> e non a >&nbsp;&nbsp;= b
</div>

---

# Confronti

operatori di confronto

```js
let a = 10;
let b = 7;
let c = 2;

let d = a == b; // d vale false
let d = (a == b); // d vale false

let d = a ! = b; // d vale true
let d = (a ! = b); // d vale true

console.log(a < b + 4);  // true
console.log(a < (b + 4));  // true
```

<br />

- L'operatore di uguaglianza <mark>==</mark> e disuguaglianza <mark>!=</mark> si scrivono come in C/C++
- In particolare in JavaScript **==** si chiama `Regular equality check`, per identificare che fà un confronto di uguaglianza regolare o convenzionale    

---

# Confronti

operatori di confronto

```js
console.log('2' > 1); // true

console.log("04" < 2); // false

console.log(true == 1); // true

console.log(false == 0); // true

console.log(true > 5); //false

console.log("02" < "03"); //true

```

<br />

- Quindi risulta evidente che JavaScript quando usa l'operatore <mark>==</mark> effettua una conversione dei tipi per essere sicuro di confrontare numeri

---

# Confronti

operatori di confronto

```js
let a = 0;
let b = "0";

console.log(a == b); // true

console.log(Boolean(a) == Boolean(b)); // false
```

<br />
<div style="background-color:green;color:yellow;padding:10px;margin-top:20px;">
E' molto importante ricordarsi questa regola e il funzionamento dell'operatore <mark> Regular equality check</mark>
</div>

---

# Confronti

operatori di confronto

- JavaScript definisce anche un'altro operatore di uguaglianza <span style="background-color: rgb(248,248,248);padding: 1px 5px 1px 5px; border-radius: 6px; border: 1px solid black;">===</span> chiamato `Strict equality check`
- Questo operatore non esiste in altri linguaggi come il C/C++
- Questo operatore al contrario di **==** effettua un controllo di uguaglianza sui suo i operandi <mark>SENZA</mark> effettuare una conversione di tipo
- E' anche definito l'operatore di disuguaglianza strict <span style="background-color: rgb(248,248,248);padding: 1px 5px 1px 5px; border-radius: 6px; border: 1px solid black;">!==</span>  
```js
let a = 0;
let b = "0";

console.log(a == b); // true  "0" è convertito in numero

console.log(a === b); // false i due operandi sono di tipo diverso 

console.log(a == false); // true

console.log(a === false); // false

```

<br />

- Questo ci permette di differenziare 0 da false
 
---

# Conditional Branching

if...else if...else...?

- Spesso abbiamo la necessità di eseguire un blocco di codice al verificarsi di una specifica condizione
- Come, nella quasi totalità dei linguaggi di programmazione, possiamo utilizzare lo statement `if`
- `if (<condizione>)` valuta l'espressione booleana e se è True esegue il blocco di codice seguente

```js
if (n == 3) {
  n = n + 7 / 2;
  console.log(n);
}

let anni = prompt("Quanti anni hai?", '');
if (anni = 16) {
  console.log("Probabilmente sei uno studente!!");
}

//forma contratta
if (anni == 16) console.log("Probabilmente sei uno studente!!");
```

<div style="background-color:green;color:yellow;padding:10px;margin-top:20px;">
La forma non contratta aumenta la leggibilità del codice
</div>

---

# Conditional Branching

if...else if...else...?

- In caso in cui vogliamo eseguire blocchi mutuamente esclusivi al verificarsi o meno di una condizione possiamo usare lo statement `if...else`

```js
let anni = prompt("Quanti anni hai?", '');

if (anni < 25) {
  console.log("Probabilmente sei uno studente!!");
} else {
  console.log("Probabilmente sei un lavoratore o un disoccupato");
}
```

- In questo caso se la variabile anni assume valore inferiore a 25 viene eseguito solamente il blocco di codice immediatamente successivo
- In caso contrario viene eseguito solamente il blocco di codice successivo ad **else**
<div style="background-color:green;color:yellow;padding:10px;margin-top:20px;">
I due blocchi di codice vengono SEMPRE eseguiti in modo mutuamente esclusivo
</div>

---

# Conditional Branching

if...else if...else...?

- Esistono casi in cui vogliamo valutare una serie di espressioni
- In questo scenario utilizziamo lo statement `if...else if...else`

```js
let anni = prompt("Quanti anni hai?", '');

if (anni < 25) {
  console.log("Probabilmente sei uno studente!!");
} else if (anni > 24 && anni < 55) {
  console.log("Probabilmente sei un lavoratore o un disoccupato");
} else if (anni > 54 && anni < 67) {
  console.log("Probabilmente hai molta esperienza nel tuo lavoro");
} else {
  console.log("Probabilmente sei un pensionato");
}
```

- In questo caso ci sono 4 blocchi mutuamente esclusivi di codice
- Solo un blocco di codice viene eseguito in funzione del valore della variabile anni, quindi in funzione di quale espressione assume valore True
  
---

# Conditional Branching

if...else if...else...?

- In certi casi viene utilizzato lo statement if...else per assegnare delle variabili
- In taluni, ed altri casi, è possibile utilizzare l'operatore `?` (question mark operator)
- Permette di esprimere un costrutto if...else in maniera molto compatta

`
condizione ?  valore-True : valore-False;
`

- L'operatore `?` valuta la condizione. 
- In caso sia valutata a True restituisce **valore-True**. 
- In caso contrario restituisce **valore-False**
  
```js
let anni = prompt("Quanti anni hai?", '');

let studente = anni < 25 ? True : False;

let professione = anni < 25 ? "Studente" : "Lavoratore";
```

---

# Conditional Branching

if...else if...else...?

- Ovviamente l'operatore `?` può essere usato in sequenza

```js
let anni = prompt("Quanti anni hai?", '');

if (anni < 25) {
  console.log("Probabilmente sei uno studente!!");
} else if (anni > 24 && anni < 67) {
  console.log("Probabilmente sei un lavoratore o un disoccupato");
} else {
  console.log("Probabilmente sei un pensionato");
}

let occupazione = (anni < 25) ? "Studente" : (anni > 24 && anni < 67) ? "Lavoratore" : "Pensionato";
```

<div style="background-color:green;color:yellow;padding:10px;margin-top:20px;">
L'operatore <mark>?</mark> in alcuni casi può migliorare la leggibilità e compattezza del codice.<br /><br />
In altri casi può rendere il codice poco leggibile e incomprensibile.<br /><br />
Utilizzarlo con parsimonia solo quando è vantaggioso.
</div>

---

# Switch

if multipli

- Come abbiamo visto tramite il costrutto `if...else if...else` possiamo valutare il verificarsi di una serie di condizione esclusive
- Tuttavia quando il numero di queste condizione è maggiore di 2 o 3, il codice risulta pesante da leggere e poco elegante o poco espressivo
- In taluni scenari possiamo usare lo statement `switch` che permette di raggiungere lo stesso obiettivo in modo più elegante
  
---

# Switch

if multipli


```js
switch (<valore>) {
  case <primo valore>:
    //blocco di codice eseguito se <valore> === <primo valore>
    [break];
  case <secondo valore>:
    //blocco di codice eseguito se <valore> === <secondo valore>
    [break];
  case <terzo valore>:
    //blocco di codice eseguito se <valore> === <terzo valore>
    [break];
  default:
    //blocco di codice eseguito se <valore> !== <primo|secondo|terzo valore>
}   
```

- Lo statement `break` è opzionale e serve a segnare la fine del blocco di codice eseguito per un particolare caso dello switch
- Se break viene omesso, l'esecuzione continua con il blocco di codice successivo
- `default` è opzionale e se presente deve essere l'ULTIMO statement dello switch
---

# Switch

if multipli

```js

let anni = prompt("Quanti anni hai?", '');

switch(Number(anni)) {
  case 25:
    console.log("Forse sei uno studente");
    console.log("o forse sei un neolaureato");
    break;
  case 35:
    console.log("Se nel pieno dell'attività lavorativa");
    break;
  case 67:
  case 68:
    console.log("Sei pensionato");
    break;
  default:
    console.log("Non riesco a capire cosa fai");
}
```

---

# Switch

if multipli

- Sia switch che case accettano una qualsiasi esperessione.
- La cosa importante che vengano valutate allo stesso tipo in quanto switch usa uno Strick equity check

```js
let a = 10;
let b = 5 * 2;

switch(++a) {
  case b:
    console.log("a è uguale a b");
    console.log(a);
    console.log(b);
    break;
  case b + 1:
    console.log("a è uguale a b + 1");
    console.log(a);
    console.log(b);
    break;
  default:
    console.log("non conosco il valore di a");
}
```

---

# Cicli

repeat yourself

-  In JS i cicli base sono esattamente uguali a quelli del C/C++
-  I 3 cicli principali sono
     1. `while`
     2. `do...while`
     3. `for`

- Ci sono anche altri tipi di cicli che analizzeremo in seguito

---

# Cicli

repeat yourself

-  Il ciclo **while** assume la seguente forma:

```js
while (condizione) {
  blocco codice
}
```

- `blocco codice` viene eseguito fintantochè la `condizione` risulta vera
- Pertanto se condizione all'inizio è falsa il ciclo non viene mai eseguito

```js
let a = 5;
while (a > 0) {
  console.log(`il numero è ${a--}`);
}

> il numero è 5
> il numero è 4
> il numero è 3
> il numero è 2
> il numero è 1
```

---

# Cicli

repeat yourself

-  Il ciclo **do...while** assume la seguente forma:

```js
do {
  blocco codice
} while (condizione);
```

- `blocco codice` viene eseguito fintantochè la `condizione` risulta vera
- Pertanto il ciclo viene eseguito **SEMPRE ALMENO** 1 volta

```js
let a = 5;
do {
  console.log(`il numero è ${a--}`);
} while (a > 0);

> il numero è 5
> il numero è 4
> il numero è 3
> il numero è 2
> il numero è 1
```

---

# Cicli

repeat yourself

-  Il ciclo **for** assume la seguente forma:

```js
for (begin; condition; step) {
  blocco codice
}
```

- lo statement `begin` viene eseguito **una sola volta** all'inizio del ciclo e setta la condizione iniziale
- `condition` viene valutato prima di ogni iterazione. Se **true** l'iterazione avviene, se **false** il ciclo termina
- `step` incrementa la variabile di controllo dopo l'esecuzione dell'iterazione corrente 
- Pertanto il ciclo viene eseguito finchè la `condition` è vera e può **NON ESSERE MAI** eseguito

```js
for(let a = 5; a > 0; a--) {
  console.log(`il numero è ${a}`);
}
> il numero è 5
> il numero è 4
> il numero è 3
> il numero è 2
> il numero è 1
```

---

# Cicli

repeat yourself

-  Le componenti `begin` e `step` del ciclo **for** sono opzionali
-  Pertanto i seguenti cicli for sono validi

```js
let i = 0;
for (;i < 3; i++) console.log(i);

let i = 0;
for (;i < 3;) {
  console.log(i);
  i++;
}
```

-  Se rimuoviamo anche la `condition` otteniamo un ciclo infoinito

```js
for (;;) {
  console.log("loop");
}
```

---

# Cicli

repeat yourself

- Spesso è necessario avere la possibilità di interrompere un ciclo prima che la condizione d'uscita diventi falsa
- Per esempio immaginiamo di voler eseguire la somma dei numeri inseriti dall'utente e di visualizzarla quando l'utente smette di inserire numeri o inserisce zero

```js
let sum = 0;

while (true) {
  let value = +prompt("Inserisci un numero", '');
  if (!value) break;
  sum += value;
}
alert( 'Somma dei numeri inseriti pari a: ' + sum );
```

- Quindi la parola chiave `break` quando invocata interrompe immediatamente il ciclo in corso e passa il controllo alla linea di codice successiva al ciclo stesso.
- Un ciclo while infinito con **break** è molto utile quando la condizione di uscita non può essere evrificata ne all'inizio ne alla fine del ciclo

---

# Cicli

repeat yourself

- Ci sono casi in cui è necessario interrompere l'iterazione corrente, senza uscire dal ciclo, e saltare subito all'iterazione successvia
- Per esempio per stampare i numeri pari compresi nell'intervallo 1-10 possiamo avvalerci della keyword `continue`

```js
for (let i = 1; i <= 10; i++) {
  if (i % 2) continue;
  console.log(i);
}
> 2
> 4
> 5
> 6
> 10
```

- **continue** ci permette di ridurre il livello di nesting rendendo il codice più leggibile e manutenibile

---

# Cicli

repeat yourself

-  Come visto tramite la parola `break` possiamo uscire da un ciclo
-  Ma come possiamo uscire da più cicli nested tra di loro?
-  Per fare ciò utilizziamo una `label` in questo modo

```js
uscita:for (let r= 0; r < 3; r++) {
          for (let c = 0; c < 3; c++) {
            let cella = prompt(`Valore della cella [${r},${c}]`);
            if (!cella) break uscita;
            console.log(`Cella [${r},${c}] = ${cella}`);
          }
       }
alert("Hai interrotto l'inserimento");
```

- In caso in cui l'utente non inserisce nulla il flusso del programma salta all'istruzione successiva alla label indicata (**uscita**). Pertanto alert viene eseguito.
- Importante notare che questo meccanismo **NON** permette un salto incodizionato ovunque nel codice ma può essere solo chiamato dall'interno di un ciclo

---

# Funzioni

don't repeat yourself

- Le funzioni sono i "mattoni" del codice sorgente di un programma
- Una funzione è un blocco univoco di codice che può essere richiamato in una o più parti del codice
- Le funzioni permettono di suddividere il programma in blocchi autonomi e di rispettare il principio [DRY](https://it.wikipedia.org/wiki/Don%27t_repeat_yourself)
- Una funzione dovrebbe assolvere ad un unico compito
- Una funzione in JS può essere definita tramite la seguente sintassi chiamata `function declaration`:

```js
function <nome funzione>() {
  codice funzione
}
```
- La keyword `function` apre la definizione di una funzione
- Segue il nome della funzione (spesso si adotta una convenzione come [snake_case](https://it.wikipedia.org/wiki/Snake_case), [came_case](https://it.wikipedia.org/wiki/Notazione_a_cammello) o altro)
- Il blocco di codice che implementa la funzione è racchiuso tra {}

```js
function show_message() {
  alert("Messaggio da ripetere");
}
```

---

# Funzioni

don't repeat yourself

- Le variabili dichiarate in una funzione sono `locali` e pertanto visibili solo all'interno della funzione stessa
- Ovviamente una funzione ha accesso a tutte le variabili esterne o globali

```js
function funzione() {
    let internal = "io sono interna";
    global = "sono modificata dalla funzione";
    console.log(internal);
}
let global = "io sono globale";
console.log(global);
> io sono globale

funzione();
> io sono interna

console.log(internal);
> Uncaught ReferenceError: internal is not defined

console.log(global);
> sono modificata dalla funzione
```

---

# Funzioni

don't repeat yourself

- Tuttavia se una variabile locale ha lo stesso nome di una globale, quest'ultima viene **oscurata** in quanto la variabile locale ha precedenza

```js
function funzione() {
    let internal = "io sono interna";
    let global = "anche io sono interna";
    console.log(internal);
    console.log(global);
}

let global = "io sono globale";
console.log(global);
> io sono globale

funzione();
> io sono interna
> anche io sono interna

console.log(global);
> io sono globale
```

---

# Funzioni

don't repeat yourself

- Spesso è necessario fornire uno o più parametri ad una funzione

```js
function <nome funzione>(<par 1>, <par 2>, ..., <par N>) {
  codice funzione
}
```

- I patrametri sono racchiusi tra le () e separati da una virgola

```js
function modify_parameters(param1, param2) {
  console.log(`Ecco i parametri ${param1}, ${param2} passati alla funzione`);
}

modify_parameters(10, 20);

//output
Ecco i parametri 10, 20 passati alla funzione
```
---

# Funzioni

don't repeat yourself

<div style="background-color:green;color:yellow;padding:10px;margin-top:20px;">
In JS esiste solo il passaggio per valore dei parametri
</div>

<br />


```js
function modify_parameters(param1, param2) {
  console.log(`Ecco i parametri ${param1}, ${param2} originali`);
  param1 = param1 + 20;
  param2 = param2 + 20;
  console.log(`Ecco i parametri ${param1}, ${param2} alla fine della funzione`);
}

let p1 = 10;
let p2 = 11;

console.log(`Ecco le variabili prima della chiamata a funzione ${p1}, ${p2}`);
modify_parameters(p1, p2);
console.log(`Ecco le variabili dopo la chiamata a funzione ${p1}, ${p2}`);

```


---

# Funzioni

don't repeat yourself

```js
//output
Ecco le variabili prima della chiamata a funzione 10, 11

Ecco i parametri 10, 11 originali

Ecco i parametri 30, 31 alla fine della funzione

Ecco le variabili dopo la chiamata a funzione 10, 11
```

<br />

- Come si vede i parametri attuali non sono modificati dalla funzione, a conferma del passaggio per valore
  
---

# Funzioni

don't repeat yourself

- I parametri di una funzione possono essere anche degli oggetti
- In tal caso viene passato per valore un *reference* (in C/C++ un puntatore) all'oggetto
- Pertanto è possibile modificare gli attributi dell'oggetto
- In ogni caso il passaggio del parametro è sempre per valore

```js
function capitalize(par1) {
  par1.nome = par1.nome.toUpperCase();
}
let utente = {
  nome: "Antonio",
  eta: 48
}
console.log(utente);
capitalize(utente);
console.log(utente);

//output
{nome: 'Antonio', eta: 48}
{nome: 'ANTONIO', eta: 48}
```

---

# Funzioni

don't repeat yourself

- Se un parametro di una funzione, non viene passato durante la chiamata, questo assume il valore di **undefined**


```js
function merge(nome, cognome) {
  console.log(`ciao ${nome} ${cognome}`);
}

merge("Antonio", "Mancuso");
> ciao Antonio Mancuso

merge("Antonio");
> ciao Antonio undefined

```

---

# Funzioni

don't repeat yourself

- Per ovviare a questo problema. possiamo specificare un valore di **deafult** per i parametri di una funzione
- In tal modo se il parametro non viene passato, assumerà il valore di default e non undefined


```js
function merge(nome, cognome = "Mancuso") {
  console.log(`ciao ${nome} ${cognome}`);
}

merge("Antonio", "Mancuso");
> ciao Antonio Mancuso

merge("Antonio");
> ciao Antonio Mancuso

```

---

# Funzioni

don't repeat yourself

- Importante notare che il parametro di default non deve essere necessariamente un tipo base, ma può essere un espressione qualsiasi, purchè sia valida in JS


```js
function merge(nome, cognome = "Mancuso".toUpperCase()) {
  console.log(`ciao ${nome} ${cognome}`);
}

merge("Antonio", "Mancuso");
> ciao Antonio Mancuso

merge("Antonio");
> ciao Antonio MANCUSO

```

---

# Funzioni

don't repeat yourself

- Siccome un parametro di default può essere una qualsiasi espressione, ne consegue che può anche essere una funzione

```js
function get_from_db() {
  console.log("cerco il cognome di default nel DB");
  return "MaNcUsO";
}

function merge(nome, cognome = get_from_db()) {
  console.log(`ciao ${nome} ${cognome}`);
}

merge("Antonio", "Mancuso");
> ciao Antonio Mancuso

merge("Antonio");
> ciao Antonio MaNcUsO
```

---

# Funzioni

don't repeat yourself

- Un altro modo di definire un parametro di default o alternativo è tramite l'uso dell'operatore ||

```js
function merge(nome, cognome) {
  cognome = cognome || "MancUSO";

  console.log(`ciao ${nome} ${cognome}`);
}

merge("Antonio", "Mancuso");
> ciao Antonio Mancuso

merge("Antonio");
> ciao Antonio MancUSO
```

---

# Funzioni

don't repeat yourself

- Esattamente come in C/C++ una funzione restituisce **sempre** un valore
- Una funzione che non resitutisce esplicitamente un valore restituisce **undefined**

```js
function somma(a, b) {
  let s = a + b;
}

let sum  = somma(10, 5);
console.log(sum);

> undefined
```

---

# Funzioni

don't repeat yourself

- Una funzione può restituire un valore esplicito, al chiamante, tramite la keyword `return`
- La keyword `return` può apparire in qualunque punto della funzione

```js
function somma(a, b) {
  return a + b;
}

let sum = somma(10, 5);
console.log(sum);
> 15

function confronto(a, b) {
  if (a > b)
    return "maggiore";
  else
    return "minore";
}

console.log(confronto(10, 20));
> minore

```

---

# Funzioni

don't repeat yourself

- Se `return` viene invocato senza argomento esso resituirà **undefined**

```js
function confronto(a, b) {
  if (a > b)
    return "maggiore";
  else
    return;
}

console.log(confronto(20, 10));
> maggiore 

console.log(confronto(10, 20));
> undefined
```

---

# Funzioni

don't repeat yourself

- Il valore restituito da una funzione può essere qualsiasi espressione valida JS

```js
function record(nome, cognome, eta) {
  return {
    nome: nome,
    cognome: cognome,
    eta: eta
  }
}

let utente = record("Antonio", "Mancuso", "47");
console.log(utente);

> {nome: 'Antonio', cognome: 'Mancuso', eta: '47'}
  cognome: "Mancuso"
  eta: "47"
  nome: "Antonio"

```


---

# Funzioni

don't repeat yourself

- Pertanto una funzione può restituire un oggetto o addirittura un'altra funzione

```js
function operazione(operator) {
  function somma(a, b) { return a + b; }

  function diff(a, b) { return a - b; }

  if (operator == "+")
    return somma;
  else if (operator == "-")
    return diff;
}

let res = operazione("+")(5, 3);
console.log(res);
> 8

let res = operazione("-")(5, 3);
console.log(res);
> 2

```

---

# Funzioni

don't repeat yourself

- In JS esistono sintassi alternative per definire una funzione
- Per esempio si può definire una funzione tramite un assegnamento (o ***binding***)
- Questa sintassi prende il nome di `function expression`
  
```js
const somma = function(a, b) {
  return a + b;
};

console.log(somma(5,3));

> 8
```

- In questo caso la funzione è di tipo `anonymous` in quanto non viene specificato un nome
- La funzione anonima viene assegnata alla variabile somma
- In C questa funzionalità si ottiene tramite complessi puntatori a funzione, mentre in JS è una semplice assegnazione


---

# Funzioni

don't repeat yourself

- In JS le <mark>funzioni anonime sono usate molto spesso</mark>, soprattutto come parametri di altre funzioni
- La funzione `setTimeout(<function>, timeout)` chiama la funzione **function** ogni **timeout** millisecondi

```js
function tick() {
  console.log("tick");
}

setInterval(tick, 1000);
```
<br />

- Vediamo un modo più veloce e pratico di usare setInterval usando una funzione anonima

```js
setInterval(function () {
    console.log('tick')
}, 1000);
```

---

# Funzioni

don't repeat yourself

- In JS una funzione non è uno speciale costrutto
- La sintassi `function expression` ci permette di assegnare una funzione ad una variabile
- Da ciò possiamo desumere che una funzione in JS è un valore
- Tuttavia anche una funzione dichiarata con la sintassi `function declaration` può essere assegnata ad una variabile

```js
function somma(a, b) {
  return a + b;
}
let sum = somma;
console.log(sum(2, 4));
> 6

console.log(sum);
>ƒ somma(a, b) {
>  return a + b;
>}
```

---

# Funzioni

don't repeat yourself

- Un'importante differenza tra **function declaration** e **function expression** è lo scope e validità della funzione
- Per una **function declaration** la funzione può essere richiamata in un punto qualsiasi del codice, anche prima della sua definizione

```js
console.log(somma(3, 5));

function somma(a, b) {
  return a + b;
}

console.log(somma(6, 1));
> 8
> 7
```

- Come si vede la prima linea è eseguita correttamente anche se la dichiarazione della funzione somma avviene dopo nel codice
- Questo perchè le funzioni dichiarate in questo modo hanno scope globale e l'interprete JS le valuta prima dell'esecuzione delle altre linee di codice

---

# Funzioni

don't repeat yourself

- Per una **function expression** la funzione può essere richiamata solo dopo che l'assegnazione è avvenuta
- Pertanto se si richiama la funzione prima che essa sia definita l'interprete genera un errore

```js
console.log(somma(3, 5));

let somma = function(a, b) {
  return a + b;
}

console.log(somma(6, 1));

> Uncaught SyntaxError: Identifier 'somma' has already been declared

```

- Infatti la funzione somma è definitia solo alla linea 3, pertanto la linea 1 non può essere eseguita correttamente

--- 

# Funzioni

don't repeat yourself

```js
function prodotto(a ,b) {
  return a * b;
}

let mul = prodotto;

console.log(prodotto(2, 3));
>6

console.log(mul(2, 3));
>6
```

<br />

- Pertanto un'aspetto molto importante da ricordare è

<div style="background-color: green;color: yellow; padding: 10px; margin:10px;">
In JS una funzione è sempre un valore &lt;right-value&gt;
</div>

---

# Funzioni

don't repeat yourself

- Considerando il fatto che una funzione è sempre un valore, possiamo dedurre la possibilità di passare una funzione come parametro di un'altra funzione

```js
function buttonAction1() {
  console.log("Pulsante premuto");
}

function onButtonClick(button, action) {
  console.log("Il bottone è stato premuto, ora eseguiamo la sua azione");
  action();
}

onButtonClick(null, buttonAction1);

> Il bottone è stato premuto, ora eseguiamo la sua azione
> Pulsante premuto

```

---

# Funzioni

don't repeat yourself

```js
function buttonAction1() {
  console.log("Pulsante premuto");
}

function buttonAction2() {
  console.log("The button has been pressed");
}


function onButtonClick(button, action) {
  console.log("Il bottone è stato premuto, ora eseguiamo la sua azione");
  action();
}

onButtonClick(null, buttonAction2);

> Il bottone è stato premuto, ora eseguiamo la sua azione
> The button has been pressed

```
---

# Funzioni

don't repeat yourself

- Considerando gli esempi precedenti, le funzioni buttonAction1() e buttonAction2() prendono il nome di `callback functions`
- In quanto queste funzioni sono richiamate da un'altra funzione
- Le callback in JS sono usate spessissimo ed in molti casi

<img src="/media/js15.png" class="mx-auto w-160" />

- Per esempio una callback può essere passata ad una funzione di libreria che la invocherà al momento opportuno

---

# Funzioni

don't repeat yourself

- Vediamo un esempio.

```js
function alert_saluti(name) {
  alert('Hello ' + name);
}

function console_saluti(name) {
  console.log('Hello ' + name);
}

function processUserInput(callback) {
  var name = prompt('Per favore inserisci il tuo nome.');
  callback(name);
}

processUserInput(alert_saluti);
processUserInput(console_saluti);
```

- Come si vede possiamo cambiare il comportamento di processUserInput senza modificarne il codice
- Le `callback` sono all abase della programmazione ad eventi asincrona tipica di JS

---

# Funzioni

don't repeat yourself

- Un'altro scenario che si incontra spesso, specie nei framework e librerie JS, è l'esecuzione di una funzione anonima

```js
let c = 20;

(function(a, b) {
  let c = 10;
  console.log(a + b + c);
})(5, 3);

>18 
```
<br />

- Questo tipo di funzioni si chiama `self-invoked function`
- *Lo scopo principale di questo tipo di funzioni è di eseguire del codice una sola volta, senza "sporcare" lo scope globale*
- Ogni variabile dichiarata nella funzione rimane locale alla funzione
  
---

# Funzioni

don't repeat yourself

- ES6 ha aggiunto un terzo modo di definire una funzione, e specificatamente ha definito le `arrow function`
- Queste funzioni sono caratterizzate dall'uso di un segno **arrow** `=>`, da qui il loro nome
- Lo scopo delle arrow function è di rendere ancora più compatta la notazione usata per esprimere un anonymous function

```js
let message = function () {
  console.log("messaggio anonimo");
};

message();
> messaggio anonimo
```
- la keyword function è evidentemente superflua 

```js
let message = () => console.log("messaggio anonimo");

message();
> messaggio anonimo
```

---

# Funzioni

don't repeat yourself

- In modo analogo anche una funzione con parametri può essere espressa come `arrow function`

```js
let somma = function(a, b) {
  console.log(a + b);
};
somma(5, 3);
> 8 


let somma = (a, b) => console.log(a + b);
somma(5, 3);
> 8 
```

- arrow **=>** vine dopo i parametri e prima del body della funzione
- Pertanto può essere facilmente letta in questo modo: questi input/parametri generano un risultato attraverso questo blocco di codice (body della funzione)

---

# Funzioni

don't repeat yourself

- Quando la funzione ha un solo parametro, le parentesi possono essere omesse

```js
let positivo = (n) => n > 0 ? true: false;
console.log(positivo(4));
> true 

let positivo = n => n > 0 ? true: false;
console.log(positivo(4));
> true 
```

---

# Funzioni

don't repeat yourself

- Quando la funzione ha più linee si esprime così

```js
let multiline = (a, b) => {
  console.log("Eseguo la somma di a e b");
  return a + b;
}

console.log(multiline(4, 5));
> Eseguo la somma di a e b
> 9

let log = () => {
  console.log("log line1");
  console.log("log line2");
}

log();
> log line 1
> log line 2
```


---

# Funzioni

don't repeat yourself

- Vediamo come invocare la funzione setInterval attraverso una arrow function
```js
setInterval(function () {
    console.log('tick')
}, 1000);


setInterval(() => console.log('tick'), 1000);
```

- Si può facilemente notare l'uso delle arrow function rende la notazione snella e più compatta

<br />

<div style="background-color: green;color: yellow; padding: 10px; margin:10px;">
Le arrow function sono utilizzate spessissimo in JavaScript moderno
</div>

--- #slide N
 
# JS Objects

- Tutti i tipi incontrati fino ad ora, sono chiamati tipi **primitivi** in qunto esprimono un solo valore (intero, decimale, stringa, booleano)
- Un tipo ***Oggetto*** al contrario rappresenta un tipo di dato aggregato, una collezione di informazioni più o meno complessa (molto simile alle struct del C)
- Un oggeto in JS è un *array associativo o dizionario*, detto ***Object Literals***

<img src="/media/js10a.png" width="200" style="float: right;" />

- Un oggetto si crea con `{...}` 
- Dentro le parentesi si specifica una serie di attributi nella forma `key:value`
- Dove **key** o **property value** è una stringa e **value** può assumere qualsiasi valore (int, string, array, object)
  

```js
let utente = {
  "nome": "Mario",
  "cognome": "Rossi",
  "anni": 20
}
{nome: 'Mario', cognome: 'Rossi', anni: 20}
```

--- #slide N
 
# JS Objects

- Siccome l'attributo key è sempre una stringa le virgolette " possono essere omesse in quanto implicite
- Pertanto l'oggetto utente può anche essere definito in questo modo

<br>

```js
let utente = {
  nome: "Mario",
  cognome: "Rossi",
  anni: 20
}
{nome: 'Mario', cognome: 'Rossi', anni: 20}
```

<br>

- Siccome il valore *value* può essere di qualsiasi tipo, se è una stringa deve essere racchiuso tra "virgolette" o 'apici'

--- #slide N
 
# JS Objects

- Per accedere alle proprietà o attributi dell'oggetto si una la notazione con il `.` o ***dot notation***

<br />

```js
console.log(utente.nome); -> Mario
console.log(utente.cognome); -> Rossi

utente.nome = "Pino"; 

```

<br />

- Possiamo aggiungere o rimuovere proprità anche dopo la definizione dell'oggetto
  
```js
utente.altezza = 170; //eta non esiste e viene creata

{nome: 'Mario', cognome: 'Rossi', eta: 30, altezza: 170}

delete utente.cognome; //rimuove la proprità cognome

{nome: 'Mario', eta: 30, altezza: 170}

```

--- #slide N
 
# JS Objects

- Pertanto possiamo definire un oggetto vuoto

<br>

```js
let utente = {}
```

<br>


- e sucecssivamente aggiungere le proprietà dell'oggetto sia con la dot notation che con le []

<br>


```js
utente.nome = "Mario";
utente["cognome"] = "Rossi";
utente.altezza = 170;
```

--- #slide N
 
# JS Objects

- Per accedere alle proprietà dell'oggetto si può anche usare la notazione con le parentesi `[<key> ]`


sia con "virgolette"
```js
console.log(utente["nome"]); -> Mario
console.log(utente["cognome"]); -> Rossi

utente["nome"] = "Pino";
utente["eta"] = 45;
```

che con 'apici'
```js
console.log(utente['nome']); -> Mario
console.log(utente['cognome']); -> Rossi

utente['nome'] = "Pino";
utente['eta'] = 45;
```

--- #slide N
 
# JS Objects

- In Javascript se si accede ad una proprietà non esistente verrà restituito il valore **unidefined** (Questo è diverso dal C++ o Java)
- Quindi risulta spesso utile verificare la presenza di una chiave o proprietà in un oggetto
- La verifica se una chiave è presente o meno nell'oggetto si può fare con l'operatore `in`

<br>

```js
let utente = {
  nome: "Mario",
  cognome: "Rossi"
}

"nome" in utente -> true
"genere" in utente -> false
```

--- #slide N
 
# JS Objects

- Per accedere a tutte le chiavi di un oggetto si può usare il metodo ***keys*** dell'oggetto ***Object***, passando l'oggetto da enumerare come parametro

<br>

```js
let utente = {
  nome: "Mario",
  cognome: "Rossi"
}

Object.keys(utente);
(2) ['nome', 'cognome']

utente.altezza = 170

Object.keys(utente);
(3) ['nome', 'cognome', 'altezza']
```

<br>

- Restituisce un array con tuttle le chiavi dell'oggetto

--- #slide N
 
# JS Objects

- Un altro metodo per accedere a tutte le chiavi di un oggetto è quello di usare un particolare ciclo denominato `for..in` loop
- Questo loop ha la seguente forma
  
```js
for(key in object) {
  esegui il blocco di docice per ogni chiave o proprietà dell'oggetto object
}
```

<br>

```js
let utente = {
  nome: "Mario",
  cognome: "Rossi"
}

for(let chiave in utente) {
    console.log(`la chiave ${chiave} ha valore ${utente[chiave]}`);
}
la chiave nome ha valore Mario
la chiave cognome ha valore Rossi
```

--- #slide N
 
# JS Objects

- Dalla teoria OOP sappiamo che un oggetto incapsula dati e metodi
- Da JS sappiamo che una funzione è un *right-value* che può essere assegnato
- Pertanto è possibile assegnare una funzione (function declaration) ad una *key* di un object literal
- In questo modo possiamo specificare i metodi per un oggetto JS

 ```js
 let utente = {
  nome: "Mario",
  cognome: "Rossi"
}

utente.speak = function () {
    console.log("Ciao io sono un utente");
}

{ nome: 'Mario', cognome: 'Rossi', speak: [Function (anonymous)] }

utente.speak();
Ciao io sono un utente
 ```

--- #slide N
 
# JS Objects

- E' anche possibile creare un metodo di un oggetto tramite una function expression

<br>

 ```js
 let utente = {
  nome: "Mario",
  cognome: "Rossi"
}

const speak = function () {
    console.log("Ciao io sono un utente");
}

utente.speak = speak;

{ nome: 'Mario', cognome: 'Rossi', speak: [Function (anonymous)] }

utente.speak();
Ciao io sono un utente
 ```

--- #slide N
 
# JS Objects

- E' anche possibile creare un metodo di un oggetto tramite una arrow function

<br>

 ```js
let utente = {
  nome: "Mario",
  cognome: "Rossi"
}

utente.speak = () => console.log("Ciao io sono un utente");


{ nome: 'Mario', cognome: 'Rossi', speak: [Function (anonymous)] }

utente.speak();
Ciao io sono un utente
 ```


--- #slide N
 
# JS Objects

- Possiamo anche specificare il metodo direttamente nell'object literals

<br>

 ```js
let utente = {
  nome: "Mario",
  cognome: "Rossi",
  speak: function() {
    console.log("Ciao io sono un utente");
  }
}

{ nome: 'Mario', cognome: 'Rossi', speak: [Function (anonymous)] }

utente.speak();
Ciao io sono un utente
 ```

--- #slide N
 
# JS Objects

- JS permette anche una scorciatoia nella definizione dei metodi di un oggetto

<br>

 ```js
let utente = {
  nome: "Mario",
  cognome: "Rossi",
  speak() {
    console.log("Ciao io sono un utente");
  }
}

{ nome: 'Mario', cognome: 'Rossi', speak: [Function (anonymous)] }

utente.speak();
Ciao io sono un utente
 ```
<br>

- Insomma, come sempre JS offre molti modi diversi di raggiungere lo stesso risultato

--- #slide N
 
# JS Objects

- Siccome un oggetto incapsula dati e metodi è necessario poter accedere ai dati dell'oggetto da dentro i metodi dell'oggetto
- Per esempio se volessimo che il metodo speak salutasse con il nome ed il cognome, sarebbe necessario accedere aglia ttributi *nome* e *cognome*
- Per far ciò utilizziamo la keywork `this`, che permette di accedere l'oggetto stesso


 ```js
let utente = {
  nome: "Mario",
  cognome: "Rossi",
  speak() {
    console.log(`Ciao io sono l'utente ${this.nome} ${this.cognome}`);
  }
}

{ nome: 'Mario', cognome: 'Rossi', speak: [Function (anonymous)] }

utente.speak();
Ciao io sono l'utente Mario Rossi
 ```


--- #slide N
 
# JS Objects

- Vediamo il caso in cui un metodo è condiviso tra più oggetti

```js

let speak = function () { console.log(`Ciao io sono l'utente ${this.nome} ${this.cognome}`); }

let utente1 = {
  nome: "Mario",
  cognome: "Rossi",
  speak: speak
}
let utente2 = {
  nome: "Giuseppe",
  cognome: "Verdi",
  speak: speak
}

> utente1.speak()
Ciao io sono l'utente Mario Rossi

> utente2.speak()
Ciao io sono l'utente Giuseppe Verdi
```

--- #slide N
 
# JS Objects

- Come si vede dall'output quando il metodo speak viene invocato sull'oggetto utente1 stampa i valori assegnati alle properità nome e cognome (Mario Rossi)
- In modo analogo quando il metodo speak viene invocato sull'oggetto utente2 stampa i valori assegnati alle properità nome e cognome (Giuseppe Verdi)
- Questo perchè nel modo speak abbiamo referenziato gli attributi nome e cognome tramite la keywork *this*
- Pertanto *this.nome* significa prendi il valore dell'attributo nome come definito nell'oggetto ocrrente (utente1 o utente2)
- Questo è uno dei principi cardini della OOP e in JS il suo funzionamento è molto simile ad altri linguaggi come Java/C++

--- #slide N
 
# JS Objects

- Nell'esempio precedente abbiamo visto che possiamo creare più oggetti (utente1 e utente2) definendo due object literals identici
- Per ottimizziare il codice e rispettare il principio *DRY* abbiamo condiviso un unico metodo speak tra i due oggetti
- Tuttavia non è ancora ottimale dover ridefinire l'object literal per ogni oggetto utente che si vuole creare (pensiamo a 1000 utenti)
- Per risolvere questo problema JS mette a disposizione il concetto di `costruttore`
- Il costruttore di un oggetto permette di condividere in modo metodi e attributi tra oggetti diversi
  
--- #slide N
 
# JS Objects

- Il `costruttore` è una funzione che crea un oggetto ed assegna attributi e metodi
- Una volta definito il costruttore è possibile *costruire* o instanziare un numero qualsiasi di oggetti identici (nella struttura e non nei dati)

<br>

```js
let Utente = function(nome, cognome) {
    this.nome = nome,
    this.cognome = cognome,
    this.speak = function () { 
        console.log(`Ciao io sono l'utente ${this.nome} ${this.cognome}`);
    }
}
```

<br>

- In questo modo abbiamo definito il costruttore dell'oggetto Utente
- In JS per convenzione il nome del costruttore inizia con una lettera Maiuscola

--- #slide N
 
# JS Objects

- Ora che abbiamo il costruttore, passiamo all'instanziazione di oggetti tramite la keywotd `new`

<br>

```js
let utente1 = new Utente("Mario", "Rossi");
let utente2 = new Utente("Giuseppe", "Verdi"); 
```

<br>

- Questi due oggetti hanno esattamente la stessa struttura, due attributi ed un metodo, ma ovviamente durante l'instanziazione abbiamo assegnato valori differenti

<br>

```js
>utente1.speak()
Ciao io sono l'utente Mario Rossi

>utente2.speak()
Ciao io sono l'utente Giuseppe Verdi
```

--- #slide N

# JS Objects

- Un'importante caratteristica della OOP è la possibilità di estendere oggetti esistenti con metodi propri
- In JS per aggiungere un metodo ad un costruttore esistente si utilizza la keywork `prototype`
- Tutti i costruttori anno la proprietà *prototype* a cui è possibile aggiungere nuovi metodi
- Vediamo come aggiungere un metodo che rende nome e cognome tutti maiuscoli
  
```js
const upper = function () {
    this.nome = this.nome.toUpperCase();
    this.cognome = this.cognome.toUpperCase();
}

Utente.prototype.maiuscolo = upper;

> utente1.speak()
Ciao io sono l'utente Mario Rossi

> utente1.maiuscolo()
> utente1.speak()
Ciao io sono l'utente MARIO ROSSI
```

--- #slide N
 
# JS Objects

- OOP definisce il concetto di `classe` come un template per creare successivamente oggetti tutti aventi le stesse priprietà
- Quindi il *costruttore* e il *prototype* di JS sono qualcosa di molto simile
- Tuttavia JS mette a disposizione anche il concetto e la keyword `class` per creare delle classi da cui si instanzieranno degli oggetti simili
- La sintassi è la seguente:
  
<br>

```js
class MyClass {
  constructor() { ... }
  metodo1() { ... }
  metodo2() { ... }
  .....
  metodoN() { ... }
}
```

--- #slide N
 
# JS Objects

- Vediamo come implementare l'esempio precedente con una classe

```js
class Utente {
    constructor(nome, cognome) {
        this.nome = nome;
        this.cognome = cognome;
    }

    speak() { 
        console.log(`Ciao io sono l'utente ${this.nome} ${this.cognome}`);
    }

    maiuscolo() {
        this.nome = this.nome.toUpperCase();
        this.cognome = this.cognome.toUpperCase();
    }
}
```

--- #slide N
 
# JS Objects

- Ora instanziamo i due oggetti utente1 e utente2 come negli esempi precedenti

<br>

```js
let utente1 = new Utente("Mario", "Rossi");
let utente2 = new Utente("Giuseppe", "Verdi");

> utente1.speak()
Ciao io sono l'utente Mario Rossi

> utente1.maiuscolo()
> utente1.speak()
Ciao io sono l'utente MARIO ROSSI

> utente2.speak()
Ciao io sono l'utente Giuseppe Verdi

> utente2.maiuscolo()
> utente2.speak()
Ciao io sono l'utente GIUSEPPE VERDI
```

--- #slide N
 
# JS Objects

- Quindi il costrutto della classe è un modo elegante ed in linea con i principi OOP per creare un costruttore, degli attributi e dei metodi
- In effetti quello che avviene all'interno del motore JS quando definiamo una classe è esattamente quanto visto prima con *costruttore* e *prototype*

<img src="/media/js16.png" class="mx-auto my-8 w-150" />

--- #slide N
 
# Esercizio js_10

JS Objects

- Per svolgere l'esercizio 10 è necessario utilizzare un form
- Vediamo qui il classico modo di processare il form client-side e non server-side

<br>

```html
<form id="<id form>">
  	.....
  	<input type="submit" value="Submit" onclick="process_form()">
</form>
```
<br>

- collego un *event handler* chiamato process_form all'evento click sul pulsante submit del form

--- #slide N
 
# Esercizio js_10

JS Objects

- Ora inibisco il normale funzionamento del form per gestirlo client-side e non server-side
- Aggiungo un event handler all'inizio del file .js

<br>

```js
// aggiunge un handler all'evento DOMContentLoaded
// che viene generato quando la pagina HTML ha terminato il suo caricamento
document.addEventListener("DOMContentLoaded", function() {
    
    // ricata l'oggetto DOM del form
    let form_utente = document.getElementById(<id form>);
    
    //aggiunge un handler all'evento submit del form
    //in modo da inibire il normale funzionamento (invio del form verso il server)
    form_utente.addEventListener("submit", function(event) {
        event.preventDefault();
    }); 
});
```

--- #slide N
 
# Esercizio js_10

JS Objects

- Infine definisco l'event_handler per il processamento del form

<br>

```js
//processa il form quando l'utente preme submit
function process_form() {
  console.log("process form");
  form = document.forms[< form><];
  console.log(form.elements[<id elemento form>].value);
}
```

<br>

- In questo modo quando l'utente preme il pulsante submit del form, il form stesso non sarà inviato al server ***event.preventDefault()***
- Nell'handler di processamento del form posso accedere ai vari campi del form <br> ***form.elements[&lt;id elemento form&gt;].value***
- Questo è il classico modo di processare un form lato client-side grazie a JS
  

--- #slide N
 
# Esercizio js_10

JS Objects

1. Creare una pagina HTML e JS contenente un form di registrazione utente
2. Il form deve contener ei seguenti campi
   1. nome
   2. cognome
   3. età
   4. colore dei capelli
3. Alla pressione del pulsante submit, il codice deve:
   - Creare un oggetto vuoto di nome **User** con i relativi attributi valorizzati con i valori inseriti nel form
   - Definire un metodo dell'oggetto chiamato **descrivi**
   - Scandire dinamicamente tutte le proprietà dell'oggetto ed aggiungere dinamicamente alla pagina HTML un tag **p** con il valore della proprietà letta

--- #slide N
 
# Esercizio js_10

JS Objects

   - Invocare il metodo *descrivi* che deve stampare su console il segunete messaggio: "ciao io sono l'utente &lt;nome&gt; &lt;cognome&gt; di anni &lt;età&gt; e con i capelli color &lt;colore dei capelli&gt;", dove i valori tra &lt;&gt; sono sostituiti con le proprietà dell'oggetto
   - Rimuovere le proprietà **età** e **colore dei capelli** dall'oggetto e con un ciclo aggiungere dinamicamente alla pagina HTML un tag **p** con il valore della proprietà rimanenti
4. Fornire il link github al file con nome *|cognome|_esercizio_js_10.html*  e *|cognome|_esercizio_js_10.js*
 
---
 
# Array

Definizione 

- Un array è una struttura dati che permette di rappresentare una collezione ordinata di valori
- In JS, al contrario di molti altri linguaggi (C/C++), un array può essere una collezione non omogenea di valori. Questa flessibilità è di grande utilità in molti casi
- Pertanto si può avere un array di interi, un array di stringhe, un array di interi e stringe, un array di oggetti, etc...
- Vediamo come si dichiara un array in JS


```js   
let frutti = new Array(); // dichiara un array vuoto
let frutti = []; // dichiara un array vuoto
```

- Normalmente in JS si utilizza la seconda notazione in quanto più compatta e veloce
- E' anche comune assegnare dei valori all'array durante la dichiarazione

```js
let frutti = ["mele", "pere", "ciliegie"]; //array omogeneo di stringhe
let numeri = [1, 2, 5, 9, 3]; //array omogeneo di numeri
let frutti_numeri = [1, "mele", 2, "pere", 5, "ciliegie"]; //array non omogeneo di stringhe e numeri
```

---
 
# Array

Accesso 

- In JS l'accesso agli elementi di un array avviene per indice
- `Gli array partono dall'indice  0`

<br>

```js
let frutti_numeri = [1, "mele", 2, "pere", 5, "ciliegie"]; 

> console.log(frutti_numeri[0]);
1

> console.log(frutti_numeri[3]);
pere

> console.log(frutti_numeri[5]);
ciliegie

```  

---
 
# Array

Modifica di un array

- Gli elementi di un array possono essere modificati con una semplice assegnazione

<br>

```js
let frutti_numeri = [1, "mele", 2, "pere", 5, "ciliegie"]; 

console.log(frutti_numeri)
[ 1, 'mele', 2, 'pere', 5, 'ciliegie' ]

frutti_numeri[0] = "nespole";
frutti_numeri[1] = 18;

> console.log(frutti_numeri)
[ 'nespole', 18, 2, 'pere', 5, 'ciliegie' ]
```

---
 
# Array

Aggiungere elementi

- L'aggiunta di nuovi elementi all'array avviene tramite una semplice assegnazione

```js
let frutti_numeri = [1, "mele", 2, "pere", 5, "ciliegie"]; 

console.log(frutti_numeri)
[ 1, 'mele', 2, 'pere', 5, 'ciliegie' ]

frutti_numeri[6] = "nespole";
frutti_numeri[7] = "fragole";
frutti_numeri[8] = 32;


> console.log(frutti_numeri)
[ 1, 'mele', 2, 'pere', 5, 'ciliegie', 'nespole', 'fragole', 32 ]
```

---
 
# Array

Lunghezza di un array

- Per conoscere la lunghezza di un array si può utilizzare la proprietà `length` dell'oggetto Array

```js
let frutti_numeri = [1, "mele", 2, "pere", 5, "ciliegie"]; 

>console.log(`L'array contiene ${frutti_numeri.length} elementi`);
L'array contiene 6 elementi
```

- Un modo per scandire tutti gli elementi di un array (in stile C/C++ ma poco orientato allo stile JS) è:

```js
let frutti_numeri = [1, "mele", 2, "pere", 5, "ciliegie"]; 

for(let i = 0; i < frutti_numeri.length; i++)
    console.log(`L'elemento [${i}] dell'array contiene ${frutti_numeri[i]}`);

L'elemento [0] dell'array contiene 1
L'elemento [1] dell'array contiene mele
L'elemento [2] dell'array contiene 2
L'elemento [3] dell'array contiene pere
L'elemento [4] dell'array contiene 5
L'elemento [5] dell'array contiene ciliegie
```

---
 
# Array

Accesso a specifici elementi

- Spesso è utili accedere a specifici elementi di un array, o meglio ad elementi in una specifica posizione
- Per esempio è utile accedere al primo elemento o all'ultimo elemento di un array oppure al 3 elemento di un array
- In questi casi ci in soccorso il metodo `at(<indice>)` dell'oggetto Array
- Il metodo ***at(&lt;indice&gt;)*** restituisce l'elemento dell'array presente alla posizione *indice*

```js
let frutti_numeri = [1, "mele", 2, "pere", 5, "ciliegie"]; 

>console.log(frutti_numeri.at(0));
1
>console.log(frutti_numeri.at(1));
mele

>console.log(frutti_numeri[frutti_numeri.length - 1]); //accede all'ultimo elemento dell'array
ciliegie

>console.log(frutti_numeri.at(frutti_numeri.length - 1); //accede all'ultimo elemento dell'array
ciliegie
```

---
 
# Array

- Pertanto, fino ad ora, il metodo *at* è uguale all'accesso per indice all'array
- Tuttavia questo è vero solo per indici positivi. 
- Ma cosa succede se l'indice di accesso è negativo?

<br>

```js
let frutti_numeri = [1, "mele", 2, "pere", 5, "ciliegie"]; 

>console.log(frutti_numeri[-1]);
undefine

>console.log(frutti_numeri.at(-1)); // accede all'ultimo elemento dell'array
ciliegie
```

<br>

- Pertanto per indici positivi .at() è uguale ad array[i]
- Per indici negativi .at() parte a contare dall fondo dell'array
- Quindi *.at(-1)* restituisce l'ultimo elemento dell'array
- Quindi *.at(-2)* restituisce il penultimoe elemento dell'array

<img src="/media/js17.png" width="350" style="float:right; position: relative; bottom: 120px;"/>
---
 
# Array

- x

---
 
# Array

- x

---
 
# Array

- x

---
 
# Array

- x

---
 
# Array

- x

---
 
# Array

- x

---
 
# Array

- x

---
 
# Array

- x

---
 
# Array

- x

---
 
# Array

- x

---
 
# Array

- x

---
 
# Array

- x

---
 
# Array

- x



<svg id="svg-filter">
    <filter id="svg-blur">
        <feGaussianBlur in="SourceGraphic" stdDeviation="10"></feGaussianBlur>
    </filter>
</svg>