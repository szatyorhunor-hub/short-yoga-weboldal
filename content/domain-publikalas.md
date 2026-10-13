# A shortyoga.fit domain publikálása

## Jelenlegi állapot

A weboldal publikálható statikus HTML/CSS/JavaScript, build vagy adatbázis nélkül. Tartalmazza a Facebook-oldal linkjét és az info@shortyoga.fit e-mailes elérhetőséget.

A felhasználó a domaint a Namecheapnél vásárolta, és Google Workspace levelezéshez használja. A weboldal még nincs feltöltve Netlifyra. Ebben a környezetben nincs beállított Netlify-hozzáférés vagy Namecheap DNS-szerkesztési hozzáférés. A domain DNS-lekérdezése az itteni környezetben átmeneti névfeloldási hibát adott; ebből nem következik, hogy a domain nem létezik vagy nincs megfelelően beállítva.

A domain bekötése, a feltöltés és a nyilvános HTTPS működése még nincs igazolva.

## Netlify-feltöltés

1. Jelentkezz be a saját Netlify-fiókodba.
2. A letölthető weboldal ZIP-csomagját csomagold ki. Az index.html, styles.css, script.js, netlify.toml és assets/ legyen együtt.
3. A Netlify kézi feltöltésénél töltsd fel a kicsomagolt mappát. Nincs build parancs; a publikálási könyvtár a mappa gyökere.
4. Ellenőrizd a kapott .netlify.app címen a weboldalt és a két programgombot.

Az automatikus, fiókon belüli API-feltöltéshez NETLIFY_AUTH_TOKEN nevű titkos hozzáférési követelményt mentettünk a környezet konfigurációs tervezetébe. A saját Netlify-fiók hozzáférési kulcsát a környezet biztonságos beállításaiban lehet megadni; ne kerüljön chatbe vagy fájlba. A követelmény mentése nem hozott létre kulcsot, nem jelentkezett be és nem publikálta az oldalt. A beállítások mentése és a környezet publikálása után először a fiókelérést kell ellenőrizni.

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
