
## EXPORTERING

report report report

### HTML5

Yada yada. Primära resurser för undersökningen: 

*    [Wiki på Geogebra](http://wiki.geogebra.org/en/Tutorial:Creating_HTML5_documents_with_GeoGebraWeb)
*    [Devsida](http://dev.geogebra.org/trac/wiki/GeoGebraWeb)


Bla bla. [Ladda ner paketet](http://dev.geogebra.org/download/web/GeoGebraWeb-latest.zip)! "These are not intended for end users"

Tungvikt. 212 filer, 55 megabyte. En översikt över innehållet:

<img src='./bilder/geogebraweb-content.png' />

Bla bla. Så, vad returneras? Se här:

<img src='./bilder/geogebraweb-export.png' />

För att extrahera en labbmodul ur det exporerade html-dokumentet krävs lite enkel handpåläggning. Själva appleten ryms i article-elementet. Denna är 'självförsörjande', och kan kopieras och integreras i ett annat html-dokument. Enda förutsättningen är att detta html-dokument laddar in filen `web.nocache.js` från GeoGebraWeb.

Nedan syns exempel på källkoden för ett minimalt dokument där två olika labbar exponeras. Exemplet ligger också live [här](http://krawaller.github.com/gleerups/export/applets.html).

<img src='./bilder/geogebraweb-composite.png' />

Notera att i exempelfilen så kan det hända att labbarna initialt är väldigt små, men sedan får sin rätta storlek när innehållet laddats. Detta gör då att övrigt innehåll på sidan förskjuts, vilket kan se oprofessionellt ut. Det är bland annat för att förhindra denna effekt som den ursprungliga exporteringen nästlade article-elementet i en tabell med given storlek, så om man vill säkerställa att ingen förskjutning sker så kan man helt enkelt behålla tabellen från exporteringen.


#### Jämförelse Geogebra-HTML

Trogen! Bla bla bla. Renderingen! Här först GeoGebra:

<img src='./bilder/comparison-geogebra.png' style='height: 60%; width=60%;' />

Samma labb i HTML:

<img src='./bilder/comparison-html.png' style='height: 60%; width=60%;' />


### Animerad GIF

Vid inklusion av enklare labbar i en digital kontext så skulle också animerad GIF kunna vara ett exporeringsalternativ. Animationen skapas utifrån en slider, så de labbar som bäst lämpar sig för detta format är de som innehåller (eller kan skrivas om till att innehålla) exakt 1 slider. 

Här är ett exempel där jag manipulerat laborationen om enhetscirkeln så att vinkeln bestäms utifrån en slider, som sedan fått definiera animationen:

<img src='./export/353_Enhetscirkeln.gif' />

Interaktiviteten är förlorad, men laborationen är nu reducerad till en enda .gif-fil som därmed är väldigt lätt att hantera. Det bör dock noteras att bildernas storlek inte är trivial; detta exempel är nästan exakt 2MB stort.