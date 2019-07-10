---
$category@: layout
formats:
- websites
- email
- ads
teaser:
  text: Görüntüleyenlerin içeriğin ana hatlarına göz atması ve istediklerinde seçtikleri bir bölüme atlaması için bir yol sağlar.
---

<!--- Reformatted by Reftar! for AMP (go/reftar) on 2019-06-13 -->
<!---
       Copyright 2016 The AMP HTML Authors. Tüm Hakları Saklıdır.

       Apache Lisansı, Sürüm 2.0 ("Lisans") ile lisanslıdır; bu dosyayı Lisans koşulları dışında kullanamazsınız.
       Lisansın bir kopyasını şu adresten edinebilirsiniz:

       http://www.apache.org/licenses/LICENSE-2.0

       Geçerli yasa tarafından gerekli görülmediği veya yazılı olarak bir sözleşme yapılmadığı sürece, Lisanslı olarak dağıtılan yazılım açıkça veya zımni olarak HİÇBİR GARANTİ VEYA KOŞUL SUNULMADAN "OLDUĞU GİBİ" dağıtılır.
       Lisans kapsamında belirli bir dilde sağlanan izinleri ve uygulanan kısıtlamaları öğrenmek için söz konusu dille ilgili Lisans'a bakın.
  -->

#amp-accordion

Görüntüleyenlerin içeriğin ana hatlarına göz atması ve herhangi bir bölüme atlaması için bir yol sağlar. Bu, bir bölümün birkaç cümlesi kaydırma gerektirdiğinde bile mobil cihazlar için yararlıdır.

<table>
  <tr>
    <td class="col-fourty"><strong>Zorunlu Komut Dosyası</strong></td>
    <td><code>&lt;script async custom-element="amp-accordion" src="https://cdn.ampproject.org/v0/amp-accordion-0.1.js"&gt;&lt;/script&gt;</code></td>
  </tr>
  <tr>
    <td class="col-fourty"><strong><a href="https://www.ampproject.org/docs/guides/responsive/control_layout.html">Desteklenen Düzenler</a></strong></td>
    <td>container</td>
  </tr>
  <tr>
    <td class="col-fourty"><strong>Örnekler</strong></td>
    <td><a href="https://ampbyexample.com/components/amp-accordion/">amp-accordion için ek açıklamalı kod örneği</a></td>
  </tr>
</table>


##Davranış

`amp-accordion` bileşeni, daraltılabilir ve genişletilebilir içerik bölümlerini görüntülemenize olanak tanır. `amp-accordion` bileşeninin en yakın alt öğelerinin her biri akordeondaki bir bölüm olarak kabul edilir. Bu düğümlerin her biri bir `<section>` etiketi olmalıdır.

* Bir `amp-accordion`, doğrudan alt öğeleri olarak bir veya daha fazla `<section>` öğesi içerebilir.
* Her bir `<section>` tam olarak iki doğrudan alt öğe içermelidir.
* İlk alt öğe (bölümün), bölümün başlığını temsil eder ve bir başlık öğesi (`h1` , `h2` , ..., `h6` , `header`) olmalıdır.
* İkinci alt öğe (bölümün), AMP HTML'de izin verilen herhangi bir etiket olabilir ve bölümün içeriğini temsil eder.
* Bir bölümün başlığı tıklandığında/dokunulduğunda bölüm genişler veya daralır.
* `amp-accordion` öğesindeki her bir bölümün daraltılmış/genişletilmiş durumu, oturum düzeyi için korunur. Bu durumu koruma özelliğini devre dışı bırakmak için `amp-accordion` öğesine `disable-session-states` özelliğini ekleyin.

####Örnek: Akordeon görüntüleme

Bu örnekte, sayfa yüklendiğinde üçüncü bölümün genişletildiği üç bölüm görüntülüyoruz.  Ayrıca, `disable-session-states` özelliğini ayarlayarak daraltılmış/genişletilmiş durumu korumayı devre dışı bıraktık.

<!--yerleşik örnek - ampproject.org'da görüntülenir -->

<div>
  <amp-iframe height="395" src="https://ampproject-b5f4c.firebaseapp.com/examples/ampaccordion.basic.embed.html" layout="fixed-height" sandbox="allow-scripts allow-forms allow-same-origin" resizable="">
    <div aria-label="Daha fazla göster" overflow="" tabindex="0" role="button">Tam kodu göster</div>
    <div placeholder=""></div>
  </amp-iframe>
</div>

[tip type="success"]
Daha fazla `amp-accordion` demosu için [Örneklerle AMP](https://ampbyexample.com/components/amp-accordion/) sitesini ziyaret edin.
[/tip]

###Etkinlikler

Aşağıdaki etkinlikler, `accordion` `section` öğesinde tetiklenir.

<table>
  <tr>
    <td width="40%"><strong><code>expand</code></strong></td>
    <td>Bu etkinlik, daraltılmış durumdan genişletilmiş duruma değişen hedef <code>section</code> öğesinde tetiklenir. Halihazırda genişletilmiş olan <code>section</code> öğesinde <code>expand</code> çağrısının bu etkinliği tetiklemeyeceğine dikkat edin.</td>
  </tr>
  <tr>
    <td width="40%"><strong><code>collapse</code></strong></td>
    <td>Bu etkinlik, genişletilmiş durumdan daraltılmış duruma değişen hedef <code>section</code>  öğesinde tetiklenir. Halihazırda daraltılmış olan <code>section</code>  öğesinde <code>collapse</code> çağrısının bu etkinliği tetiklemeyeceğine dikkat edin.</td>
  </tr>
</table>

###İşlemler

<table>
  <tr>
    <td width="40%"><strong><code>expand</code></strong></td>
    <td>Bu etkinlik, daraltılmış durumdan genişletilmiş duruma değişen hedef <code>section</code> öğesinde tetiklenir. Halihazırda genişletilmiş olan <code>section</code> öğesinde <code>expand</code> çağrısının bu etkinliği tetiklemeyeceğine dikkat edin.</td>
  </tr>
  <tr>
    <td width="40%"><strong><code>toggle</code></strong></td>
    <td>Bu işlem, <code>amp-accordion</code> öğesinin <code>expanded</code> ve <code>collapsed</code> durumları arasında geçiş yapar. Bağımsız değişken olmadan çağrıldığında, akordeonun tüm bölümlerinin durumu değişir. <code>section</code> bağımsız değişkeni ve değer olarak ilgili  <code>id</code> bilgisiyle tek bir bölüm belirtilebilir.</td>
  </tr>
  <tr>
    <td width="40%"><strong><code>expand</code></strong></td>
    <td>Bu işlem, bir <code>amp-accordion</code> öğesini genişletir. Öğe halihazırda <code>expanded</code> durumundaysa bu durumda kalır. Bağımsız değişken olmadan çağrıldığında, akordeonun tüm bölümleri genişletilir. <code>section</code>  bağımsız değişkeni ve değer olarak ilgili <code>id</code> bilgisiyle tek bir bölüm belirtilebilir.</td>
  </tr>
  <tr>
    <td width="40%"><strong><code>collapse</code></strong></td>
    <td>Bu işlem, bir <code>amp-accordion</code> öğesini daraltır. Öğe halihazırda daraltılmışsa bu durumda kalır. Bağımsız değişken olmadan çağrıldığında, akordeonun tüm bölümlerini daraltır. <code>section</code>  bağımsız değişkeni ve değer olarak ilgili <code>id</code> bilgisiyle tek bir bölüm belirtilebilir.</td>
  </tr>
</table>

####Özellikler

<table>
  <tr>
    <td width="40%"><strong><code>animate</code></strong></td>
    <td>Tüm akordeon bölümlerinin genişletilmesini/daralmasını animasyonla göstermek için <code>&lt;amp-accordion&gt;</code> öğesinde bu özelliği ayarlayın.</td>
  </tr>
  <tr>
    <td width="40%"><strong><code>disable-session-states</code></strong></td>
    <td>Akordeonun daraltılmış/genişletilmiş durumunu korumayı devre dışı bırakmak için <code>&lt;amp-accordion&gt;</code> öğesinde bu özelliği ayarlayın.</td>
  </tr>
  <tr>
    <td width="40%"><strong><code>expanded</code></strong></td>
    <td>Sayfa yüklendiğinde bölümü genişletilmiş olarak görüntülemek için bir <code>&lt;section&gt;</code> öğesinde bu özelliği ayarlayın.</td>
  </tr>
  <tr>
    <td width="40%"><strong><code>expand-single-section</code></strong></td>
    <td>Her seferinde yalnızca bir <code>&lt;section&gt;</code> öğesinin genişletilmesine izin vermek için <code>&lt;amp-accordion&gt;</code> öğesinde bu özelliği ayarlayın. Kullanıcı bir <code>&lt;section&gt;</code> öğesine odaklanırsa önceden genişletilmiş olan diğer <code>&lt;section&gt;</code> öğeleri daraltılır.</td>
  </tr>
</table>

##Stil

* `amp-accordion` öğe seçicisini serbest bir şekilde biçimlendirmek için kullanabilirsiniz.
* `amp-accordion` öğeleri her zaman `display: block` değerindedir.
* `<section>`, başlık ve içerik öğeleri kayan özellikte olamaz.
* Bölüm genişletildiğinde, `<section>` öğesinde bir `expanded` özelliği bulunur.
* İçerik öğesi, `overflow: hidden` ile temizlenip sabitlenir; dolayısıyla, kaydırma çubukları olamaz.
* `<amp-accordion>`, `<section>`, başlık ve içerik öğelerinin kenar boşlukları 0 değerine ayarlanır ve özel stillerde geçersiz kılınabilir.
* Hem üstbilgi hem de içerik öğeleri `position: relative` değerine sahiptir.

##Doğrulama

AMP doğrulayıcı spesifikasyonunda [amp-accordion kurallarına](https://github.com/ampproject/amphtml/blob/master/extensions/amp-accordion/validator-amp-accordion.protoascii) bakın.
