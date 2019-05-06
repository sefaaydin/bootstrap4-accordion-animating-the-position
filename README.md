# # Bootstrap 4 Accordion Style

# TÜRKÇE
Merhaba; Bootstrap 4'ün Accordion Bileşenini Özelleştirerek daha fazla kullanıcı deneyimi sağlamak için ufak bir çalışma yaptım. Bu çalışma da 2 farklı senaryo oluşturdum. 

 - 1. Senaryo :  katlanabilir bütün alanları birbirinden bağımsız ayrı ayrı açabilme özelliği
 - 2. Senaryo : Katlanabilir alanlardan hangisine tıklarsak o alanın konum pozisyonlaması


## 1. Senaryo

Bazen birden fazla daraltılabilir öğenin aynı anda açık olmasını isteyebiliriz. Bunun için `data-parent` özelliğini tüm daraltılabilir öğelerden kaldırın.
```html
    <div id="accordion" class="myaccordion">
      <div class="card">
        <div class="card-header" id="headingOne">
          <h2 class="mb-0">
            <button class="d-flex align-items-center justify-content-between btn btn-link collapsed" data-toggle="collapse" data-target="#collapseOne" aria-expanded="false" aria-controls="collapseOne">
              Undergraduate Studies
              <span class="fa-stack fa-sm">
                <i class="fas fa-circle fa-stack-2x"></i>
                <i class="fas fa-plus fa-stack-1x fa-inverse"></i>
              </span>
            </button>
          </h2>
        </div>
        <div id="collapseOne" class="collapse" aria-labelledby="headingOne">
          <div class="card-body">
            <ul>
              <li>Computer Science</li>
              <li>Economics</li>
              <li>Sociology</li>
              <li>Nursing</li>
              <li>English</li>
            </ul>
          </div>
        </div>
      </div>
      <div class="card">
        <div class="card-header" id="headingTwo">
          <h2 class="mb-0">
            <button class="d-flex align-items-center justify-content-between btn btn-link collapsed" data-toggle="collapse" data-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
              Postgraduate Studies
              <span class="fa-stack fa-2x">
                <i class="fas fa-circle fa-stack-2x"></i>
                <i class="fas fa-plus fa-stack-1x fa-inverse"></i>
              </span>
            </button>
          </h2>
        </div>
        <div id="collapseTwo" class="collapse" aria-labelledby="headingTwo">
          <div class="card-body">
            <ul>
              <li>Informatics</li>
              <li>Mathematics</li>
              <li>Greek</li>
              <li>Biostatistics</li>
              <li>English</li>
              <li>Nursing</li>
            </ul>
          </div>
        </div>
      </div>
      <div class="card">
        <div class="card-header" id="headingThree">
          <h2 class="mb-0">
            <button class="d-flex align-items-center justify-content-between btn btn-link collapsed" data-toggle="collapse" data-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
              Research
              <span class="fa-stack fa-2x">
                <i class="fas fa-circle fa-stack-2x"></i>
                <i class="fas fa-plus fa-stack-1x fa-inverse"></i>
              </span>
            </button>
          </h2>
        </div>
        <div id="collapseThree" class="collapse" aria-labelledby="headingThree">
          <div class="card-body">
            <ul>
              <li>Astrophysics</li>
              <li>Informatics</li>
              <li>Criminology</li>
              <li>Economics</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
```

## 2. Senaryo : Konum Pozisyonlama
Daraltılabilir öğelerin içinde çok fazla içerik olduğunu hayal edin. Belirli bir noktada, ikinci öğenin içindeki metni okudunuz, ardından üçüncü katlanabilir öğenin içeriğini görmek için tıkladınız. İkinci öğe otomatik olarak kapanır. Üçüncü katlanabilir öğe açılır. Üçüncü katlanılabilir öğenin başlangıcını görmek için geri kaydırmanız gerekir. Kullanıcı deneyimi açısından malesef iyi bir şey değil. O yüzden katlanabilir öğeye tıklandığında konumu pozisyonlamak gerekiyor. `Shown.bs.collapse` olayından yararlanarak basit bir düzeltme ile katlanabilir öğeyi kaydırma animasyonu ekleyerek en üst konumuna getirerek kullanıcı deneyimini arttırıyoruz. Bunu yapabilmek için önceki demoya aşağıdaki JavaScript kodunu ekliyoruz:




# Customize Bootstrap 4’s Accordion Component

## English :


2.  Scenario : Animating The Position Consider the following scenario: imagine there’s a lot of content inside the collapsible elements. At a certain point you read the text inside the second element, after which you click to see the contents of the third collapsible item. The second item closes again, so now, in order to see the beginning of the third element, you’ll have to scroll back up. not great UX.

Demo Pages

[http://www.devasabilisim.com/github/bootstrapAccordionStyle/accordion-with-animating-the-position.html](http://www.devasabilisim.com/github/bootstrapAccordionStyle/accordion-with-animating-the-position.html)
