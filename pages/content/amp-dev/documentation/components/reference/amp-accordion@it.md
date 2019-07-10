---
$category@: layout
formats:
- websites
- email
- ads
teaser:
  text: Permette ai visualizzatori di dare un'occhiata alla struttura dei contenuti e passare a una sezione a loro scelta.
---

<!--- Reformatted by Reftar! for AMP (go/reftar) on 2019-06-13 -->
<!---
       Copyright 2016 The AMP HTML Authors. Tutti i diritti riservati.

       Rilasciato ai sensi della Licenza Apache, versione 2.0 (la "Licenza");
     è possibile utilizzare questo file esclusivamente in conformità con la Licenza.
     Una copia della Licenza è disponibile all'indirizzo

     http://www.apache.org/licenses/LICENSE-2.0

     Se non diversamente imposto dalla legge vigente o concordato per iscritto,
     il software rilasciato ai sensi della Licenza viene distribuito "COSÌ COM'È",
     SENZA GARANZIE O CONDIZIONI DI ALCUN TIPO, esplicite o implicite.
     Leggi la Licenza per conoscere le autorizzazioni e le limitazioni in vigore
     specifiche della lingua previste dalla Licenza.
-->

#amp-accordion

Permette ai visualizzatori di dare un'occhiata alla struttura dei contenuti e passare a qualsiasi sezione. Questa funzione è utile per i dispositivi mobili dove anche solo un paio di frasi rendono indispensabile lo scorrimento per raggiungere una sezione.

<table>
  <tr>
    <td class="col-fourty"><strong>Script obbligatorio</strong></td>
    <td><code>&lt;script async custom-element="amp-accordion" src="https://cdn.ampproject.org/v0/amp-accordion-0.1.js"&gt;&lt;/script&gt;</code></td>
  </tr>
  <tr>
    <td class="col-fourty"><strong><a href="https://www.ampproject.org/docs/guides/responsive/control_layout.html">Layout supportati</a></strong></td>
    <td>container</td>
  </tr>
  <tr>
    <td class="col-fourty"><strong>Esempi</strong></td>
    <td><a href="https://ampbyexample.com/components/amp-accordion/">Esempio di codice annotato per amp-accordion</a></td>
  </tr>
</table>


##Comportamento

Il componente `amp-accordion` ti permette di mostrare sezioni di contenuti comprimibili ed espandibili. Ciascuno degli elementi secondari immediati del componente `amp-accordion` viene considerato una sezione di accordion. Ognuno di questi nodi deve essere un tag `<section>`.

* Un componente `amp-accordion` può contenere uno o più elementi `<section>` come elementi secondari diretti.
* Ciascun elemento `<section>` deve contenere esattamente due elementi secondari diretti.
* Il primo elemento secondario della sezione deve essere un elemento di intestazione (un `header` `h1`, `h2`, ..., `h6`) e rappresenta l'intestazione della sezione.
* Il secondo elemento secondario della sezione può essere un qualsiasi tag consentito in HTML AMP e rappresenta i contenuti della sezione.
* Facendo clic o toccando l'intestazione di una sezione, questa si espande o si comprime.
* Lo stato compresso/espanso di ogni sezione nell'elemento `amp-accordion` viene mantenuto al livello di sessione. Per disattivare la conservazione di questo stato, aggiungi l'attributo `disable-session-states` all'elemento `amp-accordion`.

####Esempio: visualizzazione di un accordion

In questo esempio vengono visualizzate tre sezioni, in cui la terza viene espansa al caricamento della pagina.  Inoltre, abbiamo disattivato la conservazione dello stato compresso/espanso impostando `disable-session-states`.

<!--embedded example - displays in ampproject.org -->

<div>
  <amp-iframe height="395" src="https://ampproject-b5f4c.firebaseapp.com/examples/ampaccordion.basic.embed.html" layout="fixed-height" sandbox="allow-scripts allow-forms allow-same-origin" resizable="">
    <div aria-label="Espandi" overflow="" tabindex="0" role="button">Mostra il codice completo</div>
    <div placeholder=""></div>
  </amp-iframe>
</div>

[tip type="success"]
Per vedere altre demo relative ad `amp-accordion`, visita il sito [AMP By Example](https://ampbyexample.com/components/amp-accordion/).
[/tip]

###Eventi

The events below will be triggered on `section`s of `accordion`.

<table>
  <tr>
    <td width="40%"><strong><code>expand</code></strong></td>
    <td>Questo evento viene attivato nella <code>section</code> target che passa dallo stato compresso a quello espanso. Tieni presente che questo evento non si attiva chiamando <code>expand</code> in una <code>section</code> già espansa.</td>
  </tr>
  <tr>
    <td width="40%"><strong><code>collapse</code></strong></td>
    <td>Questo evento viene attivato nella <code>section</code> target che passa dallo stato espanso a quello compresso. Tieni presente che questo evento non si attiva chiamando <code>collapse</code> in una <code>section</code> già compressa.</td>
  </tr>
</table>

###Azioni

<table>
  <tr>
    <td width="40%"><strong><code>expand</code></strong></td>
    <td>Questo evento viene attivato nella <code>section</code> target che passa dallo stato compresso a quello espanso. Tieni presente che questo evento non si attiva chiamando <code>expand</code> in una <code>section</code> già espansa.</td>
  </tr>
  <tr>
    <td width="40%"><strong><code>toggle</code></strong></td>
    <td>Questa azione attiva o disattiva gli stati <code>expanded</code> e <code>collapsed</code> di <code>amp-accordion</code>. Quando viene chiamata senza argomenti, attiva o disattiva tutte le sezioni dell'accordion. Puoi specificare una singola sezione con l'argomento <code>section</code> e l' <code>id</code> corrispondente come valore.</td>
  </tr>
  <tr>
    <td width="40%"><strong><code>expand</code></strong></td>
    <td>Questa azione espande un <code>amp-accordion</code>. Se è già <code>expanded</code>, resterà tale. Quando viene chiamata senza argomenti, espande tutte le sezioni dell'accordion. Puoi specificare una singola sezione con l'argomento <code>section</code> e l' <code>id</code> corrispondente come valore.</td>
  </tr>
  <tr>
    <td width="40%"><strong><code>collapse</code></strong></td>
    <td>Questa azione comprime un <code>amp-accordion</code>. Se è già compresso, resterà tale. Quando viene chiamato senza argomenti, comprime tutte le sezioni dell'accordion. Puoi specificare una singola sezione con l'argomento <code>section</code> e l' <code>id</code> corrispondente come valore.</td>
  </tr>
</table>

####Attributi

<table>
  <tr>
    <td width="40%"><strong><code>animate</code></strong></td>
    <td>Imposta questo attributo nell'<code>&lt;amp-accordion&gt;</code> per aggiungere un'animazione all'espansione/compressione di tutte le sezioni dell'accordion.</td>
  </tr>
  <tr>
    <td width="40%"><strong><code>disable-session-states</code></strong></td>
    <td>Imposta questo attributo nell'<code>&lt;amp-accordion&gt;</code> per disattivare la conservazione dello stato compresso/espanso dell'accordion.</td>
  </tr>
  <tr>
    <td width="40%"><strong><code>expanded</code></strong></td>
    <td>Imposta questo attributo in una <code>&lt;section&gt;</code> per mostrarla in stato espanso al caricamento della pagina.</td>
  </tr>
  <tr>
    <td width="40%"><strong><code>expand-single-section</code></strong></td>
    <td>Imposta questo attributo nell'<code>&lt;amp-accordion&gt;</code> per consentire solo una <code>&lt;section&gt;</code> espansa alla volta. Se l'utente si concentra su una <code>&lt;section&gt;</code>, tutte le <code>&lt;section&gt;</code> precedentemente espanse verranno compresse.</td>
  </tr>
</table>

##Stili

* Puoi utilizzare il selettore di elementi `amp-accordion` per modificare lo stile come preferisci.
* Gli elementi `amp-accordion` sono sempre `display: block`.
* Gli elementi `<section>`, dell'intestazione e dei contenuti non consentono il floating.
* Quando la sezione è espansa, l'elemento `<section>` ha un attributo `expanded`.
* L'elemento dei contenuti è fissato in modo chiaro con `overflow: hidden`, quindi non può presentare barre di scorrimento.
* I margini degli elementi `<amp-accordion>`, `<section>`, dell'intestazione e dei contenuti sono impostati su 0 e possono essere sovrascritti in stili personalizzati.
* Gli elementi dell'intestazione e dei contenuti sono `position: relative`.

##Convalida

Consulta le [regole amp-accordion](https://github.com/ampproject/amphtml/blob/master/extensions/amp-accordion/validator-amp-accordion.protoascii) nella specifica dello strumento di convalida AMP.
