---
title: "Tiekėjo sąskaitų faktūrų automatizavimas"
description: "Šioje temoje paaiškinamos funkcijos, pasiekiamos iki galo automatizuojant tiekėjų SF – net ir SF su priedais."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 00de566dcfbd3eb8c72816f66599863fa6cd1a41
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---
# <a name="vendor-invoice-automation"></a>Tiekėjo sąskaitų faktūrų automatizavimas

[!include[banner](../includes/banner.md)]

Šioje temoje paaiškinamos funkcijos, pasiekiamos iki galo automatizuojant tiekėjų SF – net ir SF su priedais.

Organizacijos, kurios nori supaprastinti savo mokėtinų sumų (AP) procesus, dažnai identifikuoja SF apdorojimą kaip vieną iš svarbiausių proceso sričių, kuri turi būti efektyvesnė. Daugeliu atvejų šios organizacijos popierinių SF apdorojimą perduoda trečiųjų šalių optinio ženklų atpažinimo (OCR) paslaugų teikėjui. Tada jie gauna SF metaduomenis, kuriuos galima perskaityti kompiuteriu, kartu su nuskaitytu kiekvienos SF vaizdu. Siekiant padėti automatizuoti sukuriamas „paskutinės mylios“ sprendimas, kad būtų galima panaudoti šiuos artefaktus SF išrašymo sistemoje. „Microsoft Dynamics 365 for Finance and Operations“, „Enterprise“ leidimas, dabar standartiškai suteikia šį „paskutinės mylios“ automatizavimą su SF automatizavimo sprendimu.

## <a name="solution-context"></a>Sprendimo kontekstas

SF automatizavimo sprendimas suteikia standartinę sąsają, kuri gali priimti SF antraštės ir eilučių metaduomenis bei SF priedus. Bet kokia išorinė sistema, kuri gali sugeneruoti artefaktus, atitinkančius šią sąsają, galės siųsti informacijos santrauką į „Finance and Operations“, kad būtų galima automatiškai apdoroti SF ir priedus.

Pateiktame paveikslėlyje parodytas integravimo scenarijaus pavyzdys, kuriame „Contoso“ bendradarbiauja su OCR paslaugų tiekėju dėl tiekėjo SF apdorojimo. „Contoso“ tiekėjai siunčia SF paslaugų teikėjui el. paštu. Naudodamas OCR apdorojimą paslaugų teikėjas sugeneruoja SF metaduomenis (antraštė ir / arba eilutės) ir nuskaito SF vaizdą. Tada integravimo sluoksnis transformuoja šiuos artefaktus taip, kad „Finance and Operations“ galėtų juos naudoti.

![Integravimo scenarijaus pavyzdys](media/vendor_invoice_automation_01.png)

Jei būtinas SF integravimas, galimi keli anksčiau nurodyto scenarijaus variantai. Duomenų perkėlimas yra kitas naudojimo atvejis, kai ši sąsaja gali būti naudojama norint sukurti „Finance and Operations“ SF ir priedus.

### <a name="solution-components"></a>Sprendimo komponentai

Sprendimo pagrindą sudaro šie komponentai:

+ SF antraštės, SF eilučių ir SF priedų duomenų objektai
+ SF išimčių apdorojimas
+ SF priedų peržiūros vienas šalia kito žiūryklė

Likusioje šios temos dalyje pateikiami išsamūs šių sprendimų komponentų aprašai.

## <a name="data-entities"></a>Duomenų objektai

Duomenų paketas yra darbo vienetas, kuris turi būti išsiųstas į „Finance and Operations“, kad būtų galima sukurti SF antraštes, SF eilutes ir SF priedus. Šie duomenų objektai naudojami artefaktams, kurie sudaro duomenų paketą:

+ Tiekėjo SF antraštė
+ Tiekėjo SF eilutė
+ Tiekėjo SF dokumento priedas

Tiekėjo SF dokumento priedas yra naujas duomenų objektas, pristatomas kaip šios funkcijos dalis. Tiekėjo SF antraštės objektas buvo pakeistas, kad palaikytų priedus. Tiekėjo SF eilutės objektas nebuvo modifikuotas šioje funkcijoje.

Šioje temoje nėra išsamaus duomenų paketo apibrėžimo. Joje taip pat nepaaiškinta, kaip sukurti duomenų paketus. Šią informaciją rasite [Duomenų objektų ir paketų sistema](../../dev-itpro/data-entities/data-entities-data-packages.md).

Norėdami greitai sugeneruoti bandymo duomenis, kurie apima SF ir priedus, atlikite šiuos veiksmus.

1. Prisijunkite prie savo „Finance and Operations“ egzemplioriaus.
1. Eikite į **Mokėtinos sumos** > **SF** > **Laukiančios tiekėjo SF**.
1. Sukurkite SF, kuriose yra eilučių ir priedų.

    > [!NOTE]
    > Priedai turi būti antraštės priedai. Šiuo metu tiekėjo SF dokumento priedo objektas nepalaiko eilučių priedų.

1. Atidarykite darbo sritį **Duomenų valdymas**.
1. Sukurkite eksportavimo užduotį, kurioje yra tiekėjo SF antraštė, tiekėjo SF eilutė ir tiekėjo SF dokumento priedų objektų.
1. Eksportuokite duomenis.
1. Atsisiųskite eksportuotus duomenis kaip paketą. Dabar galite naudoti paketą norėdami importuoti duomenis į paskirties egzempliorius bandymo tikslais.

### <a name="determining-the-legal-entity-for-an-invoice"></a>SF juridinio subjekto nustatymas

SF, importuotas naudojant duomenų paketus, galima susieti su juridiniu subjektu, kuriam jos priklauso dviem būdais:

+ Importavimo užduotis, kuri apdoroja SF, importuoja ją į tą pačią įmonę, kurioje užduotis buvo suplanuota **Duomenų valdymo** darbo srityje. Kitaip sakant, užduoties įmonė nustato įmonę, kuriai priklauso SF.
+ Kai duomenų paketas, kuriame yra SF, išsiunčiamas į „Finance and Operations“, kvietyklė (t. y. integracijos programa, kuri veikia ne programoje „Finance and Operations“) gali aiškiai nurodyti įmonės ID HTTP užklausoje. Šiuo atveju nepaisoma įmonės konteksto, kuriame vykdoma apdorojimo užduotis programoje „Finance and Operations“, ir SF importuojamos į įmonę, kuri perduoda naudojant HTTP užklausą.

> [!NOTE]
> Šis veikimas yra standartinis duomenų valdymo veikimas. Kalbant apie SF tai paaiškinta dėl išsamumo.

## <a name="exception-processing"></a>Išimties apdorojimas

Tokiais atvejais, kai tiekėjo SF pasiekia „Finance and Operations“ naudojant integraciją, mokėtinų sumų komandos narys turi galėti lengvai apdoroti nesėkmingų SF išimtis ir iš tokių SF sukurti laukiančias SF. Šis tiekėjo SF išimčių apdorojimas dabar yra „Finance and Operations“ dalis.

### <a name="exceptions-list-page"></a>Išimčių sąrašo puslapis

Naujas SF išimčių sąrašo puslapis yra pasiekiamas atsidarius **Mokėtinos sumos** > **SF** > **Importavimo triktys** > **Tiekėjo SF, kurių nepavyko importuoti**. Šiame puslapyje rodomi visi tiekėjo SF antraščių įrašai iš tiekėjo SF antraščių duomenų objekto išdėstymo lentelės. Atkreipkite dėmesį, kad tuos pačius įrašus galite peržiūrėti iš **Duomenų valdymo** darbo srities, kurioje galite atlikti tuos pačius veiksmus, kurie pateikiami išimčių tvarkymo funkcijoje. Tačiau UI, kurią pateikia išimčių tvarkymo funkcija, yra optimizuota funkciniam vartotojui.

![Išimčių sąrašo puslapis](media/vendor_invoice_automation_02.png)

Šiame sąrašo puslapyje yra tokie laukai, gaunami naudojant informacijos santrauką:

+ **Įmonė** – įmonė, kuriai priklauso SF
+ **Klaidos pranešimas** – klaidos pranešimas, kurį duomenų valdymo sistema išleidžia, kad paaiškintų, kodėl nepavyko sukurti SF
+ **Numeris** – SF numeris
+ **SF kodas**
+ **Pavadinimas** – tiekėjo pavadinimas
+ **Tiekėjo sąskaita**
+ **Pirkimo užsakymas** – SF pirkimo užsakymo (PO) numeris
+ **Registravimo data**
+ **SF data**
+ **SF aprašas**
+ **Valiuta**
+ **Žurnalas**
+ **Eilutės nuoroda** – identifikatorius, gaunamas iš išorinės sistemos

    > [!NOTE]
    > Eilutės nuoroda nėra SF ID.

Šiame sąrašo puslapyje taip pat yra peržiūros sritis, kurią galite naudoti šiais būdais:

+ Peržiūrėkite visą klaidos pranešimą, kad stulpelio **Klaidos pranešimas** nereikėtų išplėsti tinklelyje.
+ Peržiūrėkite visą SF priedų sąrašą, jei su SF gauta kokių nors priedų.

Sąrašo puslapis palaiko šiuos veiksmus:

+ **Redaguoti** – atidarykite išimties įrašą redagavimo režimu, kad būtų galima išspręsti problemas.
+ **Parinktys** – pasiekite standartines parinktis, esančias sąrašo puslapiuose. Galite naudoti parinktį **Įtraukti į darbo sritį** norėdami prisegti išimčių sąrašo puslapį prie darbo srities kaip sąrašą arba plytelę.

### <a name="exception-details-page"></a>Išimčių informacijos puslapis

Paleidus redagavimo režimą, rodomas SF, kurioje yra problemų, išimčių informacijos puslapis. Jei yra kokių nors priedų, SF ir numatytasis priedas išimčių informacijos puslapyje rodomi vienas šalia kito.

![Išimčių informacijos puslapis](media/vendor_invoice_automation_03.png)

Ankstesniame paveikslėlyje nėra jokių gautos tiekėjo SF antraštės eilučių. Todėl eilučių skyrius yra tuščias.

Išimčių informacijos puslapis palaiko šią operaciją:

+ **Kurti laukiančią SF** – kai apdorodami išimtis išsprendžiate SF problemas, galite spustelėti šį mygtuką, kad sukurtumėte laukiančią SF. Laukiančios SF kuriamos fone (kaip nesinchroninė operacija).

### <a name="shared-service-vs-organization-based-exception-processing"></a>Bendrai naudojama paslauga ir organizacija pagrįstas išimčių apdorojimas

Išimčių sąrašo puslapis palaiko standartines saugos struktūras, kurias **Duomenų valdymo** darbo sritis palaiko apdorojant išdėstymo įrašus. SF importavimo užduotį galima apsaugoti šiais būdais:

+ Pagal vartotojo vaidmenį
+ Pagal vartotoją
+ Pagal juridinį subjektą

![Importavimo užduotis, apsaugota pagal vartotojo vaidmenį ir juridinį subjektą](media/vendor_invoice_automation_04.png)

Jei sukonfigūruota SF importavimo užduoties sauga, išimčių sąrašo puslapis atsižvelgia į šiuos parametrus. Vartotojai galės matyti tik SF išimčių įrašus, kuriuos šis nustatymas leis jiems matyti.

Pvz., „Contoso“ nusprendė apdoroti SF išimtis pagal juridinį subjektą. Todėl SF importavimo užduoties sauga konfigūruojama taip, kad juridinio subjekto A vartotojas galėtų matyti tik SF išimtis juridiniame subjekte A, o juridinio subjekto B vartotojas galėtų matyti tik SF išimtis juridiniame subjekte B. Toks nustatymas leidžia atskirti SF išimčių tvarkymo pareigas.

Be to, „Contoso“ gali nuspręsti netaikyti jokios saugos, kad tie patys vartotojai galėtų apdoroti SF išimtis visuose juridiniuose subjektuose. Šis nustatymas įgalina SF išimčių tvarkymo bendrai naudojamų paslaugų scenarijų.

## <a name="side-by-side-attachment-viewer"></a>Priedų peržiūros vienas šalia kito žiūryklė

Kad galėtumėte lengvai peržiūrėti tiekėjo SF priedus, šiuose puslapiuose, kurie naudojami apdorojant SF, dabar pateikiama priedų žiūryklė:

+ **Išimčių tvarkymas**
+ **Laukiančių tiekėjo SF** puslapis (taip pat pasiekiamas SF peržiūros procese)
+ **SF žurnalo** užklausų puslapis (tik užregistruotoms SF)

Čia pateiktos pagrindinės funkcijos, kurias suteikia priedų žiūryklė:

+ Peržiūrėkite visus priedų tipus, kuriuos palaiko dokumentų tvarkymas (failus, vaizdus, URL ir pastabas).
+ Peržiūrėkite kelių puslapių TIFF failus.
+ Su vaizdo failais atlikite nurodytus veiksmus:
  + Pažymėkite vaizdo dalis.
  + Užblokuokite vaizdo dalis.
  + Į vaizdą įtraukite komentarų.
  + Padidinkite ir sumažinkite vaizdo mastelį.
  + Nustatykite panoraminį vaizdą.
  + Anuliuokite ir perdarykite veiksmus.
  + Pritaikykite vaizdo dydį.

> [!NOTE]
> Šie veiksmai galimi tik vaizdo failams (JPEG, TIFF, PNG ir t. t.). Visi šiais veiksmais atlikti vaizdo pakeitimai įrašomi vaizdo faile. Šiuo metu priedų žiūryklė neapima versijų kūrimo arba audito galimybių.

### <a name="default-attachment"></a>Numatytasis priedas

Jei tiekėjo SF yra daugiau nei vienas priedas, galite vieną iš dokumentų nustatyti kaip numatytąjį priedą puslapyje **Priedai**. Parinktis **Numatytasis priedas** yra nauja į funkciją įtraukta parinktis. Ši parinktis taip pat yra tiekėjo SF dokumentų priedų duomenų objekte. Todėl numatytąjį priedą galima nustatyti integruojant.

Tik vienas dokumentas gali būti nustatytas kaip numatytasis priedas. Nustačius dokumentą kaip numatytąjį priedą jis automatiškai rodomas priedų žiūryklėje, kai atidaroma SF. Jeigu kaip numatytojo priedo nenustatote jokio dokumento, žiūryklė automatiškai nerodo jokio priedo, kai atidaroma SF.

### <a name="showhide-invoice-attachments"></a>Rodyti / slėpti SF priedus

Naujas mygtukas, pasiekiamas **Išimčių apdorojimo**, **Laukiančios SF** ir **SF žurnalo** užklausų puslapiuose, leidžia matyti arba paslepia priedų žiūryklę.

### <a name="security"></a>Sauga

Nurodyti priedų žiūryklės veiksmai kontroliuojami naudojant vaidmenimis pagrįstą saugą:

+ Žymėjimas
+ Blokuoti
+ Komentaras

### <a name="pending-vendor-invoices-page"></a>Laukiančių tiekėjo SF puslapis

Šios teisės suteikia tik skaitymo prieigą arba skaitymo / rašymo prieigą prie priedų žiūryklės, norint atlikti žymėjimo, blokavimo ir komentavimo veiksmus:

+ **Tvarkyti tiekėjo SF vaizdą** – ši teisė suteikia skaitymo / rašymo prieigą.
+ **Peržiūrėti tiekėjo SF vaizdą** – ši teisė suteikia tik skaitymo prieigą.

Šios pareigos suteikia tik skaitymo arba skaitymo / rašymo prieigą prie priedų žiūryklės norint atlikti šiuos veiksmus:

+ **Tvarkyti tiekėjo SF** – šiai pareigai priskiriama teisė tvarkyti tiekėjo SF vaizdą.
+ **Pateikti užklausą dėl tiekėjo SF būsenos** – šiai pareigai priskiriama teisė peržiūrėti tiekėjo SF vaizdą.

Šie vaidmenys suteikia tik skaitymo arba skaitymo / rašymo prieigą prie priedų žiūryklės norint atlikti šiuos veiksmus:

+ **Mokėtinų sumų klerkas** ir **Mokėtinų sumų vadovas** – tiekėjo SF tvarkymo pareiga priskiriama šiems vaidmenims.
+ **Mokėtinų sumų klerkas**, **Mokėtinų sumų vadovas**, **Mokėtinų sumų centralizuotų mokėjimų klerkas** ir **Mokėtinų sumų mokėjimų klerkas** – užklausų pateikimo dėl tiekėjo SF būsenos pareiga priskiriama šiems vaidmenims.

### <a name="invoice-exception-details-page"></a>SF išimčių informacijos puslapis

Šios teisės suteikia tik skaitymo prieigą arba skaitymo / rašymo prieigą prie priedų žiūryklės, norint atlikti žymėjimo, blokavimo ir komentavimo veiksmus.

> [!NOTE]
> Vaidmenys, kurie nurodyti šiame skyriuje, suteikia tik skaitymo prieigą prie SF vaizdų priedų žiūryklėje. Jei vaidmeniui reikia ir rašymo prieigos prie vaizdų, galite suteikti rašymo prieigą tam vaidmeniui naudodami čia aprašytą teisę ir pareigą.

+ **Tvarkyti tiekėjo SF antraštės objekto vaizdą** – ši teisė suteikia skaitymo / rašymo prieigą prie SF vaizdų priedų žiūryklėje.
+ **Peržiūrėti tiekėjo SF antraštės objekto vaizdą** – ši teisė suteikia tik SF vaizdo skaitymo rodinį priedų žiūryklėje.

Šios pareigos suteikia tik skaitymo prieigą prie priedų žiūryklės norint atlikti šiuos veiksmus:

+ **Tvarkyti tiekėjo SF** – šiai pareigai priskiriama teisė tvarkyti tiekėjo SF antraštės objekto vaizdą.

Šie vaidmenys suteikia tik skaitymo prieigą prie priedų žiūryklės norint atlikti šiuos veiksmus:

+ **Mokėtinų sumų klerkas** ir **Mokėtinų sumų vadovas** – tiekėjo SF tvarkymo pareiga priskiriama šiems vaidmenims.

Pagal numatytuosius nustatymus, jei vartotojo vaidmuo suteikia bet kurio puslapio redagavimo teises, vartotojas taip pat turės redagavimo teises priedų žiūryklėje ir galės atlikti žymėjimo, blokavimo bei komentavimo veiksmus. Tačiau jei yra scenarijų, kai tam tikras vaidmuo turi turėti redagavimo teises puslapyje, bet ne priedų žiūryklėje, tada galima naudoti tinkamas teises iš ankstesnio sąrašo.

