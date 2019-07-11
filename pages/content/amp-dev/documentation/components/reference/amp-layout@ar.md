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
    <td width="40%"><strong>الوصف</strong></td>
    <td>عنصر حاوية عام متعدد الأغراض يطبّق <a href="https://www.ampproject.org/docs/guides/responsive/control_layout#the-layout-attribute">تنسيقات</a> AMP القوية على أي عنصر.</td>
  </tr>
  <tr>
    <td class="col-fourty"><strong><a href="https://www.ampproject.org/docs/guides/responsive/control_layout.html">التنسيقات المعتمدة</a></strong></td>
    <td>container وfill وfixed وfixed-height وflex-item وintrinsic وresponsive</td>
  </tr>
</table>

##نظرة عامة

يتيح لك المكّوِن `amp-layout` تطبيق تصميمات استجابة تستند إلى نسبة العرض إلى الارتفاع على أي عنصر. يعمل المكوِّن `amp-layout` بشكل مشابه للسمة [layout](https://www.ampproject.org/docs/guides/responsive/control_layout#the-layout-attribute) على مكونات AMP الموجودة لكنه يتيح عمل ترميز HTML كعناصر ثانوية. وتعمل جميع التنسيقات الأخرى مع `amp-layout` (مثل fixed-height وfixed وغيرها).

**مثال**

يستخدم المثال `amp-layout` لإنشاء حاوية استجابة حول دائرة مرسومة بالتنسيق SVG المضمّن.

```html
<amp-layout layout="responsive" width="1" height="1">
  <svg viewBox="0 0 100 100">
    <circle cx="50%" cy="50%" r="40%" stroke="black" stroke-width="3" />
    Sorry, your browser does not support inline SVG.
  </svg>
</amp-layout>
```

##السمات

يتضمن هذا العنصر [السمات المشتركة](https://www.ampproject.org/docs/reference/common_attributes) التي تشمل مكونات AMP.

##التحقق

اطِّلع على [قواعد amp-layout](https://github.com/ampproject/amphtml/blob/master/validator/validator-main.protoascii) في مواصفات مدقق AMP.
