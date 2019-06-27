---
$category@: layout
formats:
- websites
- ads
teaser:
  text: Afficher des éléments dans une fenêtre modale "lightbox" en plein écran.
---

<!--- Reformatted by Reftar! for AMP (go/reftar) on 2019-06-13 -->
<!---
       Copyright 2015 The AMP HTML Authors. Tous droits réservés.

       Autorisation sous licence Apache, version 2.0 (la "Licence") ;
       n'utilisez ce fichier que dans le cadre de la Licence.
       Vous pouvez obtenir une copie de la Licence à l'adresse suivante :

       http://www.apache.org/licenses/LICENSE-2.0

       Sauf dispositions légales applicables ou accord écrit préalable, le logiciel distribué dans le cadre de la Licence est fourni "EN L'ÉTAT", À L'EXCLUSION DE TOUTE GARANTIE OU CONDITION DE QUELQUE NATURE QUE CE SOIT, expresse ou implicite.
       Consultez la Licence correspondant à la langue spécifique qui régit les autorisations et limitations applicables.
  -->

#amp-lightbox

<table>
  <tr>
    <td width="40%"><strong>Description</strong></td>
    <td>Affiche des éléments dans une fenêtre modale "lightbox" en plein écran.</td>
  </tr>
  <tr>
    <td width="40%"><strong>Script requis</strong></td>
    <td><code>&lt;script async custom-element="amp-lightbox" src="https://cdn.ampproject.org/v0/amp-lightbox-0.1.js"&gt;&lt;/script&gt;</code></td>
  </tr>
  <tr>
    <td class="col-fourty"><strong><a href="https://www.ampproject.org/docs/guides/responsive/control_layout.html">Mises en page compatibles</a></strong></td>
    <td>nodisplay</td>
  </tr>
  <tr>
    <td width="40%"><strong>Exemples</strong></td>
    <td>Consultez l'<a href="https://ampbyexample.com/components/amp-lightbox/">exemple de composant amp-lightbox</a> sur AMP By Example.</td>
  </tr>
</table>


##Comportement

Le composant `amp-lightbox` définit les éléments enfants qui s'affichent dans une superposition ou une fenêtre modale en plein écran. Lorsque l'utilisateur clique ou appuie sur un élément (un bouton, par exemple), l'identifiant `amp-lightbox` référencé dans l'attribut `on` de l'élément sélectionné affiche l'annonce Lightbox sur toute la surface de la fenêtre affichage et présente les éléments enfants du composant `amp-lightbox`.

La touche Échap permet de fermer le mode Lightbox. Vous pouvez également définir l'attribut `on` sur un ou plusieurs éléments de l'annonce Lightbox et définir sa méthode sur `close` pour fermer le mode Lightbox lorsque l'utilisateur appuie ou clique sur l'élément.

```html
<button on="tap:quote-lb">See Quote</button>
<amp-lightbox id="quote-lb" layout="nodisplay">
  <blockquote>"Don't talk to me about JavaScript fatigue" - Horse JS</blockquote>
  <button on="tap:quote-lb.close">Nice!</button>
</amp-lightbox>
```

[tip type="read"]
Pour afficher des images dans une annonce Lightbox, vous pouvez également utiliser le composant [`<amp-image-lightbox>`](https://www.ampproject.org/docs/reference/components/amp-image-lightbox).
[/tip]

##Attributs

<table>
  <tr>
    <td width="40%"><strong>animate-in (facultatif)</strong></td>
    <td>Définit le style d'animation pour l'ouverture de l'annonce Lightbox. Par défaut, cet attribut est défini sur <code>fade-in</code>. Les valeurs valides sont <code>fade-in</code>, <code>fly-in-bottom</code> et <code>fly-in-top</code>.
      <br><br>
        <strong>Remarque</strong> : Les préréglages d'animation <code>fly-in-*</code> modifient la propriété <code>transform</code> de l'élément <code>amp-lightbox</code>. Évitez de transformer directement l'élément <code>amp-lightbox</code>. Si vous devez appliquer une transformation, définissez-la plutôt sur un élément imbriqué.</td>
      </tr>
      <tr>
        <td width="40%"><strong>close-button (obligatoire sur les annonces AMP HTML)</strong></td>
        <td>Affiche un en-tête de bouton de fermeture en haut de l'annonce Lightbox. Cet attribut n'est obligatoire et valide qu'avec les <a href="#a4a">annonces AMP HTML</a>.</td>
      </tr>
      <tr>
        <td width="40%"><strong>id (obligatoire)</strong></td>
        <td>Identifiant unique de l'annonce Lightbox.</td>
      </tr>
      <tr>
        <td width="40%"><strong>layout (obligatoire)</strong></td>
        <td>Doit être défini sur <code>nodisplay</code>.</td>
      </tr>
      <tr>
        <td width="40%"><strong>scrollable (facultatif)</strong></td>
        <td>Lorsque l'attribut <code>scrollable</code> est utilisé, l'internaute peut faire défiler le contenu de l'annonce Lightbox si sa taille est supérieure à la hauteur définie pour ce mode.
          <br><br>
            <strong>Remarque</strong> : L'attribut <code>scrollable</code> n'est pas autorisé lorsque l'élément <code><amp-lightbox></code> est utilisé dans une annonce AMP HTML. Pour plus d'informations, consultez la section <a href="#a4a">Utiliser amp-lightbox dans des annonces AMP HTML</a>.</td>
          </tr>
          <tr>
            <td width="40%"><strong>scrollable (facultatif)</strong></td>
            <td></td>
          </tr>
        </table>

##Application d'un style

Vous pouvez appliquer un style au composant `amp-lightbox` à l'aide d'une feuille de style (CSS) standard.

##Actions

Le composant `amp-lightbox` présente les actions que vous pouvez [déclencher avec la syntaxe de l'attribut "on" d'AMP](https://www.ampproject.org/docs/reference/amp-actions-and-events) :

<table>
  <tr>
    <th width="20%">Action</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><code>open</code> (par défaut)</td>
    <td>Ouvre le mode Lightbox.</td>
  </tr>
  <tr>
    <td><code>close</code></td>
    <td>Ferme le mode Lightbox.</td>
  </tr>
</table>

##<a id="a4a"></a> Utiliser `amp-lightbox` dans des annonces AMP HTML

[tip type="note"]
Le composant `amp-lightbox` à utiliser dans les annonces AMP HTML est proposé à titre [expérimental](https://www.ampproject.org/docs/reference/experimental) et est actuellement en cours de développement. Pour utiliser `amp-lightbox` dans des annonces AMP HTML, [activez le test `amp-lightbox-a4a-proto`](http://cdn.ampproject.org/experiments.html).
[/tip]

Notons quelques différences selon que le composant `amp-lightbox` est utilisé dans des documents AMP standards ou dans des [annonces écrites dans le langage AMP HTML](../amp-a4a/amp-a4a-format.md) :

###Attribut close-button obligatoire

L'attribut `close-button` est obligatoire pour les annonces AMP HTML. Cet attribut permet d'afficher un en-tête en haut de votre annonce Lightbox. L'en-tête contient un bouton de fermeture et un libellé qui indique "Ad" (Annonce). Cet en-tête est obligatoire pour :

* définir une interface utilisateur cohérente et prévisible pour les annonces AMP HTML ;
* s'assurer qu'il existe toujours un moyen de quitter le mode Lightbox ; autrement, la création risquerait de "pirater" le contenu du document hôte via une annonce Lightbox.

L'attribut `close-button` est obligatoire et n'est autorisé que dans les annonces AMP HTML. Dans les documents AMP standards, vous pouvez afficher un bouton de fermeture à tout moment dans le cadre du contenu `<amp-lightbox>`.

###Le mode Lightbox déroulant n'est pas autorisé

Le mode Lightbox déroulant n'est pas autorisé pour les annonces AMP HTML.

###Arrière-plan transparent

Lorsque vous utilisez `<amp-lightbox>` dans des annonces AMP HTML, l'arrière-plan de votre élément `<body>` devient transparent, car l'exécution AMP redimensionne et réaligne le contenu de votre création avant le développement du mode Lightbox. Cela permet d'éviter un "saut" visuel de la création pendant l'affichage du mode Lightbox. Si un arrière-plan est nécessaire pour votre création, définissez-la sur un conteneur intermédiaire (comme un `<div>` plein écran) au lieu d'utiliser l'élément `<body>`.

Lorsque l'annonce AMP HTML est diffusée dans un environnement tiers (dans un document non AMP, par exemple), la création est centrée par rapport à la fenêtre d'affichage, puis elle est développée. Cela est dû au fait que les cadres iFrame tiers doivent utiliser une API postMessage pour activer des fonctionnalités telles que le redimensionnement des cadres (qui est de type asynchrone). Commencer par le centrage de la création permet donc une transition en douceur, sans sauts d'images.

###Exemples de transitions dans le mode Lightbox pour les annonces AMP HTML

Dans les exemples ci-dessous, vous pouvez voir comment la transition recherche une annonce AMP HTML dont l'attribut `animate-in="fly-in-bottom"` est défini sur l'élément Lightbox pour une annonce AMP HTML dans un friendly iframe et pour une annonce AMP HTML dans un iFrame tiers.

#####Sur des friendly iframes (provenant, par exemple, d'un cache AMP)

<amp-img alt="annonce Lightbox dans un friendly iframe" width="360" height="480" src="https://github.com/ampproject/amphtml/raw/master/spec/img/lightbox-ad-fie.gif" layout="fixed">
  <noscript>
    <img alt="annonce Lightbox dans un friendly iframe" src="../../spec/img/lightbox-ad-fie.gif">
    </noscript>
  </amp-img>

#####Sur des cadres iFrame tiers (par exemple, en dehors du cache AMP)

<amp-img alt="annonce Lightbox dans un iFrame 3p" width="360" height="480" src="https://github.com/ampproject/amphtml/raw/master/spec/img/lightbox-ad-3p.gif" layout="fixed">
  <noscript>
    <img alt="annonce Lightbox dans un iFrame 3p" src="../../spec/img/lightbox-ad-3p.gif">
    </noscript>
  </amp-img>

##Validation

Consultez les [règles relatives à amp-lightbox](https://github.com/ampproject/amphtml/blob/master/extensions/amp-lightbox/validator-amp-lightbox.protoascii) dans les spécifications du validateur AMP.
