# # Bootstrap 4 Accordion Bileşenini özelleştirerek konum pozisyonlama

# TÜRKÇE
Merhaba; Bootstrap 4'ün Accordion Bileşenini Özelleştirerek daha fazla kullanıcı deneyimi sağlamak için ufak bir çalışma yaptım.


## Konum Pozisyonlama
Daraltılabilir öğelerin içinde çok fazla içerik olduğunu hayal edin. Belirli bir noktada, ikinci öğenin içindeki metni okudunuz, ardından üçüncü katlanabilir öğenin içeriğini görmek için tıkladınız. İkinci öğe otomatik olarak kapanır. Üçüncü katlanabilir öğe açılır. Üçüncü katlanılabilir öğenin başlangıcını görmek için geri kaydırmanız gerekir. Kullanıcı deneyimi açısından malesef iyi bir şey değil. O yüzden katlanabilir öğeye tıklandığında konumu pozisyonlamak gerekiyor. `Shown.bs.collapse` olayından yararlanarak basit bir düzeltme ile katlanabilir öğeyi kaydırma animasyonu ekleyerek en üst konumuna getirerek kullanıcı deneyimini arttırıyoruz. Bunu yapabilmek için aşağıdaki JavaScript kodunu ekliyoruz:

```javascript
$("#accordion").on("shown.bs.collapse", e => {
  $("html, body").animate(
    {
      scrollTop: $(e.target).prev().offset().top
    },
    400
  );
});
```

Demo Sayfası

[http://www.devasabilisim.com/github/bootstrapAccordionStyle/accordion-with-animating-the-position.html](http://www.devasabilisim.com/github/bootstrapAccordionStyle/accordion-with-animating-the-position.html)

# # Bootstrap 4 Accordion collapsible elements Animating The Position

# ENGLISH
Hello there; I've done a little work to provide more user experience by customizing the Accordion Component of Bootstrap 4.


## Animating The Position
imagine there’s a lot of content inside the collapsible elements. At a certain point you read the text inside the second element, after which you click to see the contents of the third collapsible item. The second item closes again, so now, in order to see the beginning of the third element, you’ll have to scroll back up. not great UX.

One simple fix, which takes advantage of the `shown.bs.collapse` event, is to fire a scroll animation to the top position of the associated control.

In order to do that we add the following JavaScript code:
```javascript
$("#accordion").on("shown.bs.collapse", e => {
  $("html, body").animate(
    {
      scrollTop: $(e.target).prev().offset().top
    },
    400
  );
});
```

Demo Pages

[http://www.devasabilisim.com/github/bootstrapAccordionStyle/accordion-with-animating-the-position.html](http://www.devasabilisim.com/github/bootstrapAccordionStyle/accordion-with-animating-the-position.html)
