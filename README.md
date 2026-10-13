# Short Yoga

A meglévő Carrd-oldal kimásolt szövegére épülő, reszponzív weboldal. Törtfehér, mélyzöld és réz árnyalatok, indiai ihletésű boltív és visszafogott lótuszmotívumok.

## Indítás

Nincs telepítendő függőség vagy build. Python 3 szükséges a helyi kiszolgáláshoz:

```sh
cd /workspace/short-yoga-weboldal
python3 -m http.server 8000 --bind 0.0.0.0
```

Az `index.html` közvetlenül böngészőben is megnyitható. Közzétételkor az `index.html`, `styles.css`, `script.js` és az `assets/` mappa együtt szükséges; bármely statikus tárhelyen kiszolgálhatók.

Egyszerű kézi feltöltéshez a `publikalas/` mappát használd. Az ottani `index.html` egyetlen fájlban tartalmazza a teljes formázást, képet és működést; a teljes `publikalas/` mappa feltölthető a Netlify Drop felületére. A különálló, gyökérkönyvtári forrásfájlok a további szerkesztéshez maradnak meg.

## Tartalom

Az eredeti szakaszok sorrendje megmaradt: nyitó rész, miért született meg a Short Yoga, mit kapsz, gyakorlatok/programok, módszer, előnyök, kinek ajánlott.

- Az 5 napos ingyenes program gombja a megadott e-mail-cím-gyűjtő Google-űrlapra mutat.
- A 14 napos program ára **9 900 Ft**. A napi 15–20 perces, otthoni PDF-program bemutatása a felhasználó által feltöltött dokumentumra épül.
- Nincsenek konkrét gyakorlatnevek, videóígéretek vagy kitalált szolgáltatások. A PDF fizetős tartalmát nem tesszük közzé.
- A nyitókép AI-val készített hangulatkép, nem a programhoz tartozó helyszín fényképe.
- A láblécben kis Facebook-ikon és a megadott Facebook-oldal, valamint a kattintható **info@shortyoga.fit** szerepel.

## Ellenőrzés

Chromium böngészőben ellenőrizve 360, 390, 600, 768, 1024 és 1440 px szélességen: nincs vízszintes kilógás, a helyi kép és fájlok betöltődnek, a szakaszhivatkozások és a mobilmenü működnek. JavaScript nélkül is elérhető a navigáció és a két program gombja. A célcímek az eredeti kérésben megadott linkek; az űrlapok elküldését nem teszteltük.

## Carrd

Ez a tároló önálló, elkészült weboldalt tartalmaz. A `shortyoga.carrd.co` élő oldalát nem módosítottuk: nincs közvetlen, bejelentkezett Carrd-szerkesztési hozzáférésünk. Az átvezetéshez lásd a [Carrd útmutatót](content/carrd-atvezetes.md).

A saját **https://shortyoga.fit** cím Netlifyra mutat. A felhasználó a publikalas/ mappát kézzel feltöltötte, beállította a Namecheap DNS-rekordjait, és a saját böngészőjében elérte az oldalt. A projekt Make public művelete és a kijelentkezett, nyilvános elérés ellenőrzése még hátravan. A beállításokat és az ellenőrzés kereteit a [publikálási útmutató](content/domain-publikalas.md) rögzíti. További forrásmódosításokhoz a kézi Netlify-feltöltést meg kell ismételni; a GitHub-frissítés önmagában nem frissíti a kézzel feltöltött oldalt.
