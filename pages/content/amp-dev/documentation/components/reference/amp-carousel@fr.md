---
$category@: layout
formats:
- websites
- email
- ads
teaser:
  text: Afficher plusieurs éléments de contenu similaires le long d'un axe horizontal.
---


<!---
       Copyright 2015 The AMP HTML Authors. Tous droits réservés.

       Autorisation sous licence Apache, version 2.0 (la "Licence") ;
       n'utilisez ce fichier que dans le cadre de la Licence.
       Vous pouvez obtenir une copie de la Licence à l'adresse suivante :

       http://www.apache.org/licenses/LICENSE-2.0

       Sauf dispositions légales applicables ou accord écrit préalable, le logiciel distribué dans le cadre de la Licence est fourni "EN L'ÉTAT", À L'EXCLUSION DE TOUTE GARANTIE OU CONDITION DE QUELQUE NATURE QUE CE SOIT, expresse ou implicite.
       Consultez la Licence correspondant à la langue spécifique qui régit les autorisations et limitations applicables.
  -->

#amp-carousel

Carrousel générique permettant d'afficher plusieurs éléments de contenu similaires le long d'un axe horizontal. Ce composant a été conçu pour offrir une flexibilité et des performances élevées.

<table>
  <tr>
    <td width="40%"><strong>Script requis</strong></td>
    <td><code>&lt;script async custom-element="amp-carousel" src="https://cdn.ampproject.org/v0/amp-carousel-0.1.js">&lt;/script></code></td>
  </tr>
  <tr>
    <td class="col-fourty"><strong><a href="https://www.ampproject.org/docs/guides/responsive/control_layout.html">Mises en page compatibles</a></strong></td>
    <td>
      <ul>
        <li>carrousel : fixed, fixed-height et nodisplay.</li>
        <li>diapositives : fill, fixed, fixed-height, flex-item, nodisplay et responsive.</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td width="40%"><strong>Exemples</strong></td>
    <td>AMP By Example :<ul>
      <li><a href="https://ampbyexample.com/components/amp-carousel/">Exemple de composant amp-carrousel</a></li>
      <li><a href="https://ampbyexample.com/advanced/image_galleries_with_amp-carousel/">Galeries d'images avec amp-carousel</a></li></ul></td>
    </tr>
  </table>

##Comportement

Chacun des éléments enfants immédiats du composant `amp-carousel` est considéré comme un élément du carrousel. Chacun de ces nœuds peut également comporter des éléments enfants HTML arbitraires.

Le carrousel se compose d'un nombre arbitraire d'éléments, ainsi que de flèches de navigation facultatives permettant d'avancer ou de reculer d'un seul élément.

Le carrousel change d'élément lorsque l'utilisateur balaie l'écran, utilise les touches fléchées ou clique sur une flèche de navigation facultative.

<!--embedded example - displays in ampproject.org -->

<div>
  <amp-iframe height="313" src="https://ampproject-b5f4c.firebaseapp.com/examples/ampcarousel.basic.embed.html" layout="fixed-height" sandbox="allow-scripts allow-forms allow-same-origin" resizable="">
    <div aria-label="Plus" overflow="" tabindex="0" role="button">Afficher l'intégralité du code</div>
    <div placeholder=""></div>
  </amp-iframe>
</div>

###Accéder à une diapositive spécifique

Si vous définissez une méthode pour l'attribut `on` d'un élément sur `tap:carousel-id.goToSlide(index=N)`, le carrousel ayant l'identifiant "carousel-id" passe à la diapositive suivante à index=N lorsque l'utilisateur appuie ou clique sur un élément (la première diapositive se situe à index=0, la deuxième à index=1 et ainsi de suite).

L'exemple suivant illustre un carrousel de trois images, sous lequel sont disposés des boutons d'aperçu. Lorsqu'un utilisateur clique sur l'un des boutons, l'élément de carrousel correspondant s'affiche.

<!--embedded example - displays in ampproject.org -->

<div>
  <amp-iframe height="878" src="https://ampproject-b5f4c.firebaseapp.com/examples/ampcarousel.advance-slide.embed.html" layout="fixed-height" sandbox="allow-scripts allow-forms allow-same-origin" resizable="">
    <div aria-label="Plus" overflow="" tabindex="0" role="button">Afficher l'intégralité du code</div>
    <div placeholder=""></div>
  </amp-iframe>
</div>

##Attributs

<table>
  <tr>
    <td width="40%"><strong>type</strong></td>
    <td>Indique le type d'affichage des éléments du carrousel :
      <ul>
        <li><code>carousel</code> (type par défaut) : toutes les diapositives sont affichées et l'utilisateur peut les faire défiler horizontalement. Ce type n'accepte que les mises en page suivantes : <code>fixed</code>, <code>fixed-height</code> et <code>nodisplay</code>.</li>
        <li><code>slides</code> : affiche une seule diapositive à la fois. Ce type accepte les mises en page suivantes : <code>fill</code>, <code>fixed</code>, <code>fixed-height</code>, <code>flex-item</code>, <code>nodisplay</code> et <code>responsive</code>.</li>
      </ul></td>
    </tr>
    <tr>
      <td width="40%"><strong>height (obligatoire)</strong></td>
      <td>Indique la hauteur du carrousel, en pixels.</td>
    </tr>
    <tr>
      <td width="40%"><strong>controls (facultatif)</strong></td>
      <td>Affiche les flèches gauche et droite de manière permanente pour permettre à l'utilisateur de parcourir les éléments du carrousel sur des appareils mobiles.
          Par défaut, les flèches de navigation disparaissent au bout de quelques secondes sur l'écran du mobile.
          La visibilité des flèches peut également être contrôlée en appliquant un style, et une requête média peut être utilisée pour n'afficher les flèches qu'à certaines largeurs d'écran. Sur un ordinateur, les flèches sont toujours affichées, sauf si un seul élément enfant est présent.</td>
      </tr>
      <tr>
        <td width="40%"><strong>data-next-button-aria-label (facultatif)</strong></td>
        <td>Définit le libellé ARIA du bouton <code>amp-carousel-button-next</code>. Si aucune valeur n'est indiquée, le libellé ARIA est défini par défaut sur "Next item in carousel" (Élément suivant dans le carrousel).</td>
      </tr>
      <tr>
        <td width="40%"><strong>data-prev-button-aria-label (facultatif)</strong></td>
        <td>Définit le libellé ARIA du bouton <code>amp-carousel-button-prev</code>. Si aucune valeur n'est indiquée, le libellé ARIA est défini par défaut sur "Previous item in carousel" (Élément précédent dans le carrousel).</td>
      </tr>
      <tr>
        <td width="40%"><strong>data-button-count-format (facultatif)</strong></td>
        <td>Chaîne de format sous la forme <code>(%s of %s)</code>, utilisée comme suffixe du libellé ARIA pour <code>amp-carousel-button-next</code>/<code>amp-carousel-button-prev</code>. Cet attribut fournit aux utilisateurs d'un lecteur d'écran des informations sur leur progression dans le carrousel. Si aucune valeur n'est indiquée, la valeur par défaut est "(%s of %s)".</td>
      </tr>
      <tr>
        <td width="40%"><strong>autoplay (facultatif)</strong></td>
        <td>Passe à la diapositive suivante sans intervention de l'utilisateur.<br>
          Si cet attribut est renseigné sans valeur :
          <ul>
            <li>Par défaut, le carrousel change de diapositive toutes les 5 000 millisecondes (5 secondes) ; cet intervalle peut être modifié à l'aide de l'attribut <code>delay</code>.</li>
            <li>Le cas échéant, l'attribut <code>loop</code> est associé à <code>amp-carousel</code>.</li>
            <li>Au moins deux diapositives sont nécessaires pour que la lecture automatique puisse avoir lieu.</li>
            <li>L'attribut s'applique uniquement aux carrousels dont le paramètre est <code>type=slides</code>.</li>
          </ul>
          Si cet attribut est renseigné avec une valeur :
          <ul>
            <li>Le cas échéant, l'attribut <code>loop</code> est associé à <code>amp-carousel</code>.</li>
            <li>L'attribut <code>loop</code> est supprimé une fois que le nombre requis de boucles a été effectué.</li>
          </ul></td>
        </tr>
        <tr>
          <td width="40%"><strong>delay (facultatif)</strong></td>
          <td>Définit le délai avant le passage à la diapositive suivante, en millisecondes, lorsque l'attribut <code>autoplay</code> est activé. L'attribut <code>delay</code> s'applique uniquement aux carrousels dont le paramètre est <code>type=slides</code>.</td>
        </tr>
        <tr>
          <td width="40%"><strong>loop (facultatif)</strong></td>
          <td>Permet à l'utilisateur d'aller au-delà du premier ou du dernier élément. Le carrousel doit contenir au moins trois diapositives pour que la lecture en boucle soit effectuée. L'attribut <code>loop</code> s'applique uniquement aux carrousels dont le paramètre est <code>type=slides</code>.
            <em>Exemple : Affiche un carrousel de diapositives avec les attributs "controls", "looping" et "autoplay" différé.</em>
            <!--embedded example - displays in ampproject.org -->
            <div>
              <amp-iframe height="446" src="https://ampproject-b5f4c.firebaseapp.com/examples/ampcarousel.controls.embed.html" layout="fixed-height" sandbox="allow-scripts allow-forms allow-same-origin" resizable="">
                <div aria-label="Plus" overflow="" tabindex="0" role="button">Afficher l'intégralité du code</div>
                <div placeholder=""></div>
              </amp-iframe>
            </div></td>
          </tr>
          <tr>
            <td width="40%"><strong>common attributes</strong></td>
            <td>Cet élément inclut des <a href="https://www.ampproject.org/docs/reference/common_attributes">attributs communs</a> étendus aux composants AMP.</td>
          </tr>
        </table>

##Application d'un style

* Vous pouvez utiliser le sélecteur d'éléments `amp-carousel` pour appliquer un style librement.
* Vous pouvez utiliser le sélecteur de classes `.amp-carousel-slide` pour cibler des éléments du carrousel.
* L'état visuel d'un bouton `amp-carousel` désactivé est masqué.
* Par défaut, `.amp-carousel-button` utilise une image SVG intégrée comme image de fond pour les boutons. Vous pouvez remplacer cette image par votre propre image ou fichier SVG, comme dans l'exemple ci-dessous.

*Exemple : Image SVG intégrée `.amp-carousel-button` par défaut*

```css
.amp-carousel-button-prev {
  left: 16px;
  background-image: url('data:image/svg+xml;charset=utf-8,<svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 18 18"><path d="M15 8.25H5.87l4.19-4.19L9 3 3 9l6 6 1.06-1.06-4.19-4.19H15v-1.5z" fill="#fff" /></svg>');
}
```

*Exemple : Remplacement de l'image SVG intégrée `.amp-carousel-button` par défaut*

```css
.amp-carousel-button-prev {
  left: 5%;
  background-image: url('data:image/svg+xml;charset=utf-8,<svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 18 18"><path d="M11.56 5.56L10.5 4.5 6 9l4.5 4.5 1.06-1.06L8.12 9z" fill="#fff" /></svg>');
}
```

##Validation

Consultez les [règles relatives à amp-carousel](https://github.com/ampproject/amphtml/blob/master/extensions/amp-carousel/validator-amp-carousel.protoascii) dans les spécifications du validateur AMP.
