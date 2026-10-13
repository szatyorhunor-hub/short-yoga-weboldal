# A shortyoga.fit domain publikálása

## Jelenlegi állapot

A weboldal publikálható statikus HTML/CSS/JavaScript, build vagy adatbázis nélkül. Tartalmazza a Facebook-oldal linkjét és az info@shortyoga.fit e-mailes elérhetőséget.

A felhasználó a domaint a Namecheapnél vásárolta, és Google Workspace levelezéshez használja. Az önálló publikálási változatot kézzel feltöltötte Netlifyra: https://amazing-frangollo-4b0079.netlify.app. Az elsődleges domain https://shortyoga.fit; a www.shortyoga.fit a Netlifyban az elsődleges címre irányít.

A felhasználó 2026. október 13-án jelezte, hogy a saját domaines oldal működik. A beküldött képernyőképen a Netlify DNS-ellenőrzése sikeres volt. A Namecheap képernyőképén az A rekord @ → 75.2.60.5 és a CNAME rekord www → amazing-frangollo-4b0079.netlify.app szerepel; a meglévő Google Workspace TXT-rekordok megmaradtak. A HTTPS működését a felhasználó igazolta, nem az itteni hálózatról végzett független kérés. Levelezési küldés/fogadás és űrlapbeküldés nem volt a teszt része.

## Netlify-feltöltés

1. Jelentkezz be a saját Netlify-fiókodba.
2. A GitHub short-yoga-site ágáról letöltött ZIP-csomagot csomagold ki, és keresd meg a publikalas/ mappát. Az ottani index.html a formázást, képet és JavaScriptet is tartalmazza.
3. A Netlify kézi feltöltésénél a teljes publikalas/ mappát töltsd fel. Nincs build parancs. A gyökérkönyvtári többfájlos forrás index.html fájlját önmagában ne töltsd fel; annak külön CSS-, JavaScript- és képfájlokra van szüksége.
4. Ellenőrizd a kapott .netlify.app címen a weboldalt és a két programgombot.

Az automatikus, fiókon belüli API-feltöltéshez NETLIFY_AUTH_TOKEN nevű titkos hozzáférési követelményt mentettünk a környezet konfigurációs tervezetébe. Ez nem volt szükséges a sikeres kézi publikáláshoz, és nincs beállított Netlify- vagy Namecheap API-hozzáférés ebben a környezetben. Későbbi API-alapú frissítéshez a saját Netlify-fiók hozzáférési kulcsát a környezet biztonságos beállításaiban lehet megadni; ne kerüljön chatbe vagy fájlba. A követelmény mentése önmagában nem jelentkezik be és nem publikál weboldalt.

## Domain hozzáadása

1. A Netlify webhely domainbeállításainál add hozzá a shortyoga.fit domaint. Ez legyen az elsődleges cím.
2. Ha a www.shortyoga.fit változatot is használni szeretnéd, add hozzá azt is.
3. A Netlify által megjelenített külső DNS-utasításokat kövesd. A gyökérdomain (@) célrekordját a szolgáltató ajánlásából kell átvenni; ismeretlen webhelyhez nem találunk ki IP-címet.
4. A www CNAME célja az adott, már létrehozott Netlify-webhely .netlify.app címe legyen.

## Namecheap és a levelezés

A Namecheap kezelőfelületén a Domain List → Manage → Advanced DNS alatt ellenőrizhetők a rekordok, ha a domain DNS-ét a Namecheap kezeli. Ha egyéni névszervereket használsz, a módosításokat a DNS-t ténylegesen kezelő szolgáltatónál kell végezni.

Őrizd meg a Google Workspace levelezéséhez tartozó MX, SPF, DKIM, DMARC és ellenőrző TXT rekordokat. A weboldal címéhez tartozó @ és www webes rekordok beállítására van szükség. A meglévő levelezési rekordok megőrzéséhez nincs szükség névszervercserére.

## Végső ellenőrzés

A megfelelő DNS-beállítás után ellenőrizni kell a Netlify domainellenőrzését, a HTTPS-tanúsítvány kiadását és a shortyoga.fit nyilvános megnyitását. Az oldalon látható info@shortyoga.fit link mailto hivatkozás; önmagában nem hoz létre postafiókot vagy nem igazolja a levelezés működését.
