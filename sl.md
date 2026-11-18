---
title: Finora – Politika zasebnosti
lang: sl
permalink: /sl
---

[English](en)

# Politika zasebnosti – Finora

Velja od: 18. 11. 2026

Ta politika zasebnosti opisuje, kako aplikacija **Finora** (Android in Windows) ravna z vašimi podatki. Aplikacijo razvija in objavlja posameznik Anže Arzenšek iz Slovenije (v nadaljevanju »razvijalec« ali »mi«).

## Na kratko

- Finora deluje brez strežnika, brez uporabniškega računa in brez oglasov.
- Vsi vaši finančni podatki so shranjeni samo na vaši napravi, v šifrirani bazi.
- Razvijalec do vaših transakcij, izpiskov, računov ali nastavitev nima dostopa in jih ne prejema.
- Aplikacija na Androidu nima dovoljenja za dostop do interneta, zato sama ne more pošiljati podatkov nikamor.
- Podatki zapustijo napravo samo, če to sami izberete: ko shranite varnostno kopijo ali izvoz na izbrano mesto ali ko nam pišete po e-pošti.

## 1. Podatki, ki jih obdeluje aplikacija na vaši napravi

Finora obdeluje podatke, ki jih vnesete ali uvozite sami:

- uvožene bančne izpiske (PDF, CSV, XLSX, camt.053) in iz njih prebrane transakcije: datum, znesek, prejemnik ali plačnik, namen, IBAN, stanje;
- račune, kategorije, pravila za kategoriziranje, proračune, naučene postavitve izpiskov in nastavitve aplikacije;
- PIN za zaklep (shranjen samo kot zgoščena vrednost, izračunana z algoritmom Argon2id; samega PIN-a aplikacija ne shrani).

Ti podatki so shranjeni v zasebni mapi aplikacije, v bazi, šifrirani s SQLCipher (AES-256). Ključ baze hrani varna shramba operacijskega sistema (Android Keystore oziroma zaščita podatkov v Windows). Samodejno kategoriziranje in prepoznavanje ponavljajočih se plačil potekata v celoti na napravi.

Izvirne datoteke izpiskov aplikacija prebere ob uvozu; shrani le transakcije in podatke, potrebne za prepoznavo istega izpiska v prihodnje.

**Biometrija.** Če vklopite odklep s prstnim odtisom ali obrazom, preverjanje opravi operacijski sistem (Android BiometricPrompt oziroma Windows Hello). Finora biometričnih podatkov nikoli ne vidi in ne shrani; od sistema dobi le odgovor »uspešno« ali »neuspešno«.

**Varnostne kopije Androida.** Samodejno varnostno kopiranje Androida (v Google Drive) je za Finoro izklopljeno, zato se podatki aplikacije ne kopirajo v oblak brez vaše vednosti.

**Posnetki zaslona.** Aplikacija privzeto prepreči posnetke zaslona in prikaz vsebine v pregledu odprtih aplikacij. To lahko izklopite v Nastavitvah.

Za te podatke razvijalec ni upravljavec v smislu Splošne uredbe o varstvu podatkov (GDPR), ker jih ne zbira, ne prejema in nima dostopa do njih. Z njimi upravljate sami.

## 2. Ko podatki zapustijo napravo po vaši izbiri

- **Varnostna kopija.** Ko ustvarite varnostno kopijo, jo aplikacija šifrira (AES-256-GCM, ključ izpeljan z Argon2id iz vašega gesla oziroma obnovitvenega ključa) in shrani na mesto, ki ga izberete v sistemskem izbirniku datotek (npr. v mapo na napravi, na ključek ali v storitev v oblaku, kot je Google Drive). Za datoteko, shranjeno pri tretji osebi, veljajo pogoji te storitve. Brez gesla ali obnovitvenega ključa vsebine kopije ni mogoče prebrati – tudi razvijalec je ne more.
- **Izvoz CSV in PDF.** Izvoz transakcij ali poročila ni šifriran. Datoteko shranite, kamor sami izberete, in zanjo odgovarjate sami.
- **Deljenje v Finoro.** Ko izpisek v Finoro pošljete iz druge aplikacije (»Deli«, »Odpri z …«), ga Finora prebere samo za uvoz.

## 3. Podatki, ki jih prejme razvijalec

### 3.1 E-pošta (povratna informacija in podpora)

Gumb »Pošlji povratno informacijo« odpre vašo aplikacijo za e-pošto z osnutkom sporočila na naslov anze.ar@gmail.com. Sporočilo pošljete sami in pred pošiljanjem vidite vso vsebino. Če aplikacija v osnutek vpiše tehnične podatke (npr. verzijo aplikacije in sistema), jih lahko pred pošiljanjem izbrišete.

Ko nam pišete, prejmemo vaš e-naslov, ime (če ga prikazuje vaš e-poštni program) in vsebino sporočila. Uporabimo jih samo za odgovor in za izboljšanje aplikacije. Pravna podlaga je naš zakoniti interes, da odgovorimo na vaše vprašanje (člen 6(1)(f) GDPR). Sporočila hranimo, dokler je to potrebno za obravnavo, in jih izbrišemo najpozneje 2 leti po zadnji korespondenci, prej pa na vašo zahtevo. V sporočilo ne vpisujte zneskov, številk računov ali drugih finančnih podatkov.

### 3.2 Statistika zrušitev in delovanja (Android vitals)

Če ste v nastavitvah Androida dovolili pošiljanje podatkov o uporabi in diagnostiki Googlu, Google zbira podatke o zrušitvah in zamrznitvah aplikacij na vaši napravi (npr. model naprave, verzija Androida, sled sklada ob zrušitvi). Razvijalec v Google Play Console vidi te podatke v **združeni obliki, brez podatkov, ki bi vas neposredno identificirali**, in jih uporabi samo za odpravljanje napak. To nastavitev upravljate v nastavitvah Androida oziroma Googla, ne v Finori. Za ta podatek je upravljavec Google (glej poglavje 4).


## 4. Googlove storitve

Aplikacija iz Google Play uporablja naslednje Googlove storitve. Podatke pri tem obdeluje Google kot samostojni upravljavec po svoji politiki zasebnosti (<https://policies.google.com/privacy>); razvijalec teh podatkov ne prejme, razen kot je navedeno spodaj.

- **Google Play (namestitev, posodobitve, Android vitals).** Google obdeluje podatke, potrebne za namestitev in posodabljanje aplikacij, ter po vaši nastavitvi diagnostične podatke (poglavje 3.2).
- **Play In-App Review (ocena v aplikaciji).** Aplikacija vas lahko občasno povabi k oceni. Okno prikaže Google Play; oceno in komentar pošljete Googlu, ki ju objavi v trgovini skladno s svojimi pravili. Razvijalec vidi javne ocene kot vsi drugi (v zaprtem testiranju ocene vidi samo razvijalec). Oceno lahko izbrišete v Google Play.
- **Play In-App Updates (obvestilo o novi verziji).** Aplikacija lahko prek Google Play preveri, ali je na voljo nova verzija, in vam ponudi posodobitev. Pri tem Google Play uporabi podatke o napravi, verziji aplikacije in nameščenih modulih; razvijalec teh podatkov ne prejme.

Te storitve tečejo prek aplikacije Trgovina Google Play na vaši napravi; Finora sama ne vzpostavlja internetne povezave.

## 5. Česa ne počnemo

- Ne prikazujemo oglasov in ne uporabljamo oglaševalskih identifikatorjev.
- Ne uporabljamo analitike ali sledenja uporabi.
- Ne prodajamo in ne delimo podatkov s tretjimi osebami.
- Ne povezujemo se z vašo banko; transakcije pridejo v aplikacijo samo iz datotek, ki jih uvozite sami.
- Ne zbiramo lokacije, stikov, fotografij ali drugih podatkov z naprave.

## 6. Hramba in izbris podatkov

Podatki v aplikaciji ostanejo na napravi, dokler jih ne izbrišete:

- posamezne transakcije, uvoze, račune, kategorije in pravila lahko izbrišete v aplikaciji (izbrisane transakcije so 30 dni v košu, nato se samodejno izbrišejo);
- vse podatke izbrišete z odstranitvijo aplikacije ali v nastavitvah Androida (Aplikacije → Finora → Shramba → Počisti podatke);
- ob pozabljenem PIN-u brez obnovitvenega ključa aplikacija ponudi izbris vseh podatkov.

Varnostne kopije in izvoze, ki ste jih shranili sami, izbrišete sami na mestu, kamor ste jih shranili. Ker razvijalec vaših podatkov nima, jih ne more izbrisati ali obnoviti namesto vas.

## 7. Varnost

Podatke na napravi ščitijo šifrirana baza, zaklep s PIN-om ali biometrijo, samodejni zaklep po nedejavnosti in omejitev števila poskusov vnosa PIN-a. Varnostne kopije so šifrirane. Popolne varnosti ni mogoče zagotoviti; za varnost naprave (zaklep zaslona, posodobitve sistema) skrbite sami.

## 8. Otroci

Finora ni namenjena otrokom, mlajšim od 15 let, in od njih zavestno ne zbiramo podatkov.

## 9. Vaše pravice

Za podatke, ki jih prejmemo (poglavje 3), imate pravico do dostopa, popravka, izbrisa, omejitve obdelave, ugovora in prenosljivosti ter pravico, da kadar koli prekličete privolitev. Zahtevo pošljite na anze.ar@gmail.com; odgovorimo najpozneje v enem mesecu.

Pritožbo lahko vložite pri nadzornem organu: **Informacijski pooblaščenec Republike Slovenije**, Dunajska cesta 22, 1000 Ljubljana, <https://www.ip-rs.si>.

## 10. Spremembe politike

Politiko lahko posodobimo, npr. ob novih funkcijah. Novo različico objavimo na tem naslovu s posodobljenim datumom; ob bistvenih spremembah vas obvestimo tudi v opombah ob izdaji.

## 11. Kontakt

Anže Arzenšek
E-pošta: anze.ar@gmail.com
