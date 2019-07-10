
---
$category@: ads-analytics
formats:
- websites
- ads
- stories
teaser:
  text: Sayfa görüntülemelerini saymak için bir izleme pikseli.
---

<!--- Reformatted by Reftar! for AMP (go/reftar) on 2019-06-13 -->
<!---
       Copyright 2015 The AMP HTML Authors. Tüm Hakları Saklıdır.
       
       Apache Lisansı, Sürüm 2.0 ("Lisans") ile lisanslıdır; bu dosyayı Lisans koşulları dışında kullanamazsınız.
       Lisansın bir kopyasını şu adresten edinebilirsiniz:
       
       http://www.apache.org/licenses/LICENSE-2.0
       
       Geçerli yasa tarafından gerekli görülmediği veya yazılı olarak bir sözleşme yapılmadığı sürece, Lisanslı olarak dağıtılan yazılım açıkça veya zımni olarak HİÇBİR GARANTİ VEYA KOŞUL SUNULMADAN "OLDUĞU GİBİ" dağıtılır.
       Lisans kapsamında belirli bir dilde sağlanan izinleri ve uygulanan kısıtlamaları öğrenmek için söz konusu dille ilgili Lisans'a bakın.
  -->

#<a name="amp-pixel"></a> `amp-pixel`

[İçindekiler]

<table>
  <tr>
    <td class="col-fourty"><strong>Açıklama</strong></td>
    <td>Sayfa görüntülemelerini saymak için tipik bir izleme pikseli olarak kullanılabilir.</td>
  </tr>
  <tr>
    <td class="col-fourty"><strong><a href="https://www.ampproject.org/docs/guides/responsive/control_layout.html">Desteklenen Düzenler</a></strong></td>
    <td>fixed, nodisplay</td>
  </tr>
  <tr>
    <td class="col-fourty"><strong>Örnekler</strong></td>
    <td>Örneklerle AMP <a href="https://ampbyexample.com/components/amp-pixel/">amp-pixel örneği</a> sayfasına bakın.</td>
  </tr>
</table>

##Davranış

`amp-pixel` bileşeni, basit bir `img` izleme pikseli gibi davranır. Tek bir URL alır ancak istekte bulunulurken URL dizesindeki bileşenle değiştirilebilen değişkenler sağlar. Daha ayrıntılı bilgi için [değişiklikler](#substitutions) bölümüne bakın.

Bu temel örnekte `amp-pixel`, belirtilen URL'ye basit bir GET isteği gönderir ve sonucu yoksayar.

```html
<amp-pixel src="https://foo.com/tracker/foo"
    layout="nodisplay"></amp-pixel>
  ```
  
  [tip type="note"]
Analiz isteklerinin yönlendirme üstbilgisindeki AMP URL'leri işlenirken `usqp` parametresini çıkarın veya yoksayın. Bu parametre, Google tarafından Google AMP Önbelleği denemelerinin tetiklenmesi amacıyla kullanılır.
[/tip]

##Özellikler

#####src (gerekli)

`https` protokolü olması gereken bir uzak uç nokta basit URL'si.

#####referrerpolicy (isteğe bağlı)

Bu özellik, `<img>` öğesindeki `referrerpolicy` özelliğine benzer ancak yalnızca `no-referrer` değeri kabul edilir. `referrerpolicy=no-referrer` belirtilirse `referrer` üstbilgisi, HTTP isteğinden kaldırılır.

```html
<amp-pixel src="https://foo.com/tracker/foo"
    layout="nodisplay"
    referrerpolicy="no-referrer"></amp-pixel>
  ```
  
#####allow-ssr-img (isteğe bağlı)

AMP4ADS reklam öğelerinde kullanılan bu özellik, doğrulama sonrası dönüşümün parçası olarak, bir img öğesinin doğrudan amp-pixel öğesine yerleştirilmesiyle ping komutunun AMP çalışma zamanı getirme/yürütme işlemine paralel olarak gönderilmesine olanak tanınabileceğini belirtir.
Bunun, URL içindeki makroların GENİŞLETİLMEYECEĞİ anlamına gelir. Bu nedenle, yalnızca src'de mevcut değillerse kullanın.

#####common attributes

Bu öğe, genişletilmiş [ortak özellikleri](https://www.ampproject.org/docs/reference/common_attributes) AMP bileşenlerine ekler.

##Değişiklikler

`amp-pixel`, tüm standart URL değişkeni değişikliklerine izin verir.
Daha fazla bilgi için [Değişiklik Kılavuzu](../spec/amp-var-substitutions.md) dokümanına bakın.

Aşağıdaki örnekte, `https://foo.com/pixel?0.8390278471201` gibi bir istekte bulunabilir. Burada, RANDOM değeri, her gösterimden sonra rastgele oluşturulur.

```html
<amp-pixel src="https://foo.com/pixel?RANDOM"
    layout="nodisplay"></amp-pixel>
  ```
  
##Stil

`amp-pixel` şekillendirilmemelidir.

##Doğrulama

AMP doğrulayıcı spesifikasyonundaki [amp-pixel kurallarına](https://github.com/ampproject/amphtml/blob/master/validator/validator-main.protoascii) bakın.
