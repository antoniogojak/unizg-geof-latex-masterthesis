# 🎓 LaTeX predložak za diplomski rad Geodetskog fakulteta

Ovo je LaTeX predložak namijenjen pisanju diplomskog rada na Sveučilištu u Zagrebu Geodetskom fakultetu. Temelji se na službenom Word predlošku, ali s poboljšanjima radi bolje formatiranosti.

Sam predložak Worda nije dobro sređen. Navodi se jedan način stilizacije teksta, a drugi je postavljen. Općenito stilizacija jednog elementa varira kroz uvodne stranice i samu razradu. Ovdje je postavljeno da odgovara preporučenom, a ujedno i lijepo izgleda.

Nisu navedeni načini pisanja i upute kao u službenom predlošku, već je pokazano kako koristiti LaTeX funkcije koje će najčešće poslužiti za pisanje rada.

**Preporuka:** Prije pisanja diplomskog rada u LaTeX-u, radite zadatke kao tehnička izvješća i slično.

**Zašto LaTeX?** Glavna prednost LaTeX-a je da ćete na kraju imati čisti dokument — sve stilizacije teksta su jasno navedene, te nije kao u Wordu da će biti raznih stilova. Osobito se to primijeti pri velikim radovima gdje ima puno preinaka, upravo kao što su diplomski radovi.

## ⚙️ Zaglavlje predloška

Dalje je razjašnjeno zaglavlje LaTeX predloška za lakšu prilagodbu, osobito onima koji nisu vješti u LaTeX-u.

Za predložak se koristi `report`. Najbolje je za ovu vrstu rada, ali se mijenja stilizacija naslova, podnaslova, tablica sadržaja, popisa slika i tablica da odgovara traženim stilovima.

Postavljeni paketi za jezik i kodiranje omogućuju pravilni prikaz hrvatskih znakova i copy-paste iz PDF-a.

Font je postavljen na `newtx`, koji najsličnije odgovara Times New Roman. `lmodern` je dodan kao opcija. Smatram da je čitljiviji na ekranima pa sam ga koristio osobito tijekom radnih verzija rada. Još je koristan jer kada se PDF učita u Word, on ga puno lakše raspozna pa nema neželjeno spojenih riječi. To će poslužiti kada se šalje mentoru na pregled za ostavljanje komentara.

Uvedene su varijable `mybindingoffset` i `myhalfbindingoffset`. Binding offset je dodatni odmak s lijeve strane uz margine za uvez. Polovina offseta se koristi samo u izjavi o izvornosti da pozadinska grafika pletera bude centrirana. Preporučam za tiskanu verziju ostaviti na 0.2 inča, a za web verziju oboje postaviti na 0.

Propred je postavljen na jednostruki razmak i razmak od pola retka između odlomaka.

Učitavaju se biblioteke za postavljanje zaglavlja i podnožja, korištenje boja, za slike — prikaz mjesta u tekstu na kojem se pojavljuju, i učitavanje PDF datoteka. Dalje su postavljene biblioteke za tablice. Postavljena je stilizacija opisa slika i tablica. Biblioteke za liste i formule. Formule se numeriraju od početka rada od 1 nadalje. Hiperveze za skakanje na linkove za slike, tablice, citiranja i slično.

U zaglavlju su stvorene varijable `mytitle` i `myauthor`, pa je dovoljno tu unijeti podatke i kasnije se automatski povlače gdje se trebaju pojavljivati naslov rada i ime. Također se tu unosi sažetak i ključne riječi.

PDF/A metapodaci će se trebati dodati samo prije uploada na Dabar. Odkomentiraj `%` na počecima redova i provjerite podatke. Nisam uspješno direktno iz LaTeX-a uspio postaviti stvaranje PDF/A datoteke, već samo zapis metapodataka. Kasnije je spremljeno putem Adobe Acrobata kao PDF/A-2b.

Postavlja se pogon za citiranje koji je `biblatex` i stil APA na hrvatskom jeziku, te datoteka koja sadrži zapise radova.

Prilagođeno je citiranje dva autora da između bude „i“, jer po defaultu se samo nižu prezimena.

Prema zadanom predlošku fakulteta, literatura sadrži dio za internetske izvore. Stvoren je taj stil citiranja i definirano kako se prikazuje unutar teksta i u popisu literature. `biblatex` koristi tip `@online`. Citirat će se kao internetski izvor ako unutar ključnih riječi sadrži `url`. Dakle, treba biti `keywords = {url}` da se citira kao internetski izvor.

Postavljena je putanja za mapu u kojoj se nalaze slike. Učitavaju se biblioteke za prikaz popisa slika i tablica i njihove prilagodbe uvlačenja i točkanja do broja stranice.

Postavljena je putanja za mapu u kojoj se nalaze slike. Učitavaju se biblioteke za prikaz popisa slika i tablica i njihove prilagodbe uvlačenja i točkanja do broja stranice.

`\setlength{\cftbeforechapskip}{8pt}` Ovim se u sadržaju definira razmak između poglavlja — prilagoditi prema potrebi i željama.

Predefinirani su odmak i stil poglavlja, naslova, podnaslova — isto tako i za tablice da izgledaju identično naslovima. Formatirano je uvlačenje na popisu slika i tablica.

## 📄 Tijelo rada

Definirana je naslovna stranica. Nije potrebno ništa mijenjati osim mjesta i datuma.

Podatke u izjavi o izvornosti i tablici o diplomskom radu je potrebno ručno pregledati i ispraviti.

- **Izjava o izvornosti:** JMBAG, rođen/rođena, datum i mjesto rođenja
- **Tablica o diplomskom radu:** Automatski se povlači ime i prezime, naslov, broj stranica, a ostalo je potrebno ručno unijeti. Dalo bi se automatizirati brojanje tablica i slika, ali našao sam prekomplicirane funkcije. Ako dodaješ svoje funkcije, onda pripazi da ne broji slike i tablice prije Uvoda i/ili iz Priloga.

U zahvali prilagoditi odmak od vrha stranice da skladno izgleda, ovisno koliko opširna zahvala bude — ili inače samo postaviti `\newpage` ako će biti prazna stranica.

Sadržaj stilski ne odgovara potpuno Word predlošku. Vidio sam kroz diplomske radove da prolaze različito stilizirani — velika slova za naslove, numerirano s točkama i bez, razmaci i slične varijacije. Postavljeno je sada da odgovara približno predlošku, a da ostaje pregledno.

Dalje su navedeni primjeri tablica, formula, slika i citiranja.

Pri svakom poglavlju dodati `\thispagestyle{fancy}` za prikaz zaglavlja.

Grafika hrvatskog pletera (`Pleter.pdf`) izrađena je u Illustratoru pomoću kistova Tomislava Čara: [http://tomislaw.info/blog/2012/12/13/hrvatski-nacionalni-pleter/](http://tomislaw.info/blog/2012/12/13/hrvatski-nacionalni-pleter/)

## 🧪 Testirano

Predložak je testiran u **TeXstudio 4.8.4** s kompajliranjem pomoću **pdfLaTeX** i bibliografijom putem **biber**.

## 🤝 Doprinosi

Ako primijetite nešto što nedostaje, može se poboljšati ili dodatno srediti — slobodno se uključite!

Najlakše ćete kroz konkretan rad uočiti što bi se moglo doraditi ili dodati.