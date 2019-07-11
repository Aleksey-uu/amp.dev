---
$category@: layout
teaser:
  text: >-
    The amp-layout` component allows you to apply aspect-ratio based responsive
    layouts to any element. The `amp-layout` component works similarly to the
    layout.
$title: amp-layout
---

<!--- Reformatted by Reftar! for AMP (go/reftar) on 2019-06-13 -->
<!---
       Copyright 2016 The AMP HTML Authors. All Rights Reserved.

       Licensed under the Apache License, Version 2.0 (the "License");
     you may not use this file except in compliance with the License.
     You may obtain a copy of the License at

     http://www.apache.org/licenses/LICENSE-2.0

     Unless required by applicable law or agreed to in writing, software
     distributed under the License is distributed on an "AS-IS" BASIS,
     WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
     See the License for the specific language governing permissions and
     limitations under the License.
-->

#<a name="amp-layout"></a> `amp-layout`

<table>
  <tr>
    <td width="40%"><strong>Description</strong></td>
    <td>Conteneur générique polyvalent qui permet d'appliquer les <a href="https://www.ampproject.org/docs/guides/responsive/control_layout#the-layout-attribute">mises en page</a> AMP enrichies à n'importe quel élément.</td>
  </tr>
  <tr>
    <td class="col-fourty"><strong><a href="https://www.ampproject.org/docs/guides/responsive/control_layout.html">Mises en page compatibles</a></strong></td>
    <td>container, fill, fixed, fixed-height, flex-item, intrinsic, responsive</td>
  </tr>
</table>

##Aperçu

Le composant `amp-layout` vous permet d'appliquer à n'importe quel élément des mises en page réactives basées sur le format. Ce composant fonctionne de la même manière que l'attribut [layout](https://www.ampproject.org/docs/guides/responsive/control_layout#the-layout-attribute) sur les composants AMP existants, si ce n'est qu'il accepte des balises HTML comme éléments enfants. Les autres mises en page compatibles fonctionnent toutes avec `amp-layout` (fixed-height, fixed, etc.).

**Exemple**

Dans l'exemple ci-dessous, le composant `amp-layout` est utilisé pour créer un conteneur réactif autour d'un cercle tracé avec un code SVG intégré.

```html
<amp-layout layout="responsive" width="1" height="1">
  <svg viewBox="0 0 100 100">
    <circle cx="50%" cy="50%" r="40%" stroke="black" stroke-width="3" />
      Sorry, your browser does not support inline SVG.
    </svg>
  </amp-layout>
```

##Attributs

Cet élément inclut des [attributs communs](https://www.ampproject.org/docs/reference/common_attributes) étendus aux composants AMP.

##Validation

Consultez les [règles relatives à amp-layout](https://github.com/ampproject/amphtml/blob/master/validator/validator-main.protoascii) dans les spécifications du validateur AMP.
