---
title: "Prekių skirstymas iš gamybos užsakymų į pakrovimo rampas"
description: "Šioje temoje aprašoma, kaip valdyti prekių skirstymo medžiagos procesą, kai iš gamybos linijos siunčiamų prekių transportavimo rampai pranešama, kad procesas baigtas."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCrossDockOpportunityPolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 62194012cfbe101d19e9de3254afb004da79a562
ms.contentlocale: lt-lt
ms.lasthandoff: 03/08/2018

---

# <a name="cross-docking-from-production-orders-to-outbound-docks"></a>Prekių skirstymas iš gamybos užsakymų į pakrovimo rampas

[!include[banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip valdyti prekių skirstymo medžiagos procesą, kai iš gamybos linijos siunčiamų prekių transportavimo rampai pranešama, kad procesas baigtas.

<a name="introduction"></a>Įžanga
------------

Prekių skirstymas nuo gamybos iki siunčiamų prekių transportavimo vietos svarbus gamintojams, gaminantiems didelius kiekius prekių, kurie nori išsiųsti pabaigtus produktus iš karto, kai tik iš gamybos linijų gaunamas pranešimas, kad jie baigti. Tikslas yra išsiųsti produktus paskirstymo centrams, kurie įsikūrę netoli kliento poreikio, o ne kaupti atsargas gamybos vietoje.

Jei nėra tiesioginės produkto paklausos, jis turi būti atidedamas gamybos vietos sandėlio vietose. Šis procesas taip pat vadinamas *Prekių skirstymas pagal aplinkybes*, kuris reiškia, kad, jei yra paklausa siųsti produktą, reikėtų pasinaudoti šia galimybe, o ne atidėti produktą saugoti vidinėje atmintyje.

Toliau pateikiamame pavyzdyje nurodomi trys srauto, prasidedančio gamybos linijos (2) pabaigoje, variantai.

Gamybos išeigos vietoje (3) pranešama, kad produktas baigtas ir keltuvo vairuotojas šioje vietoje (3) pasiima padėklą.

-   Jei yra suplanuota veikla (6), kurią atliekant produktas bus perkeliamas iš gamybos (1) į platinimo centrą (7), tada sistema nukreips sunkvežimio vairuotoją padėklą iškrauti įlankos durų vietoje (4).
-   Jei priekabai jau paskirtos įlankos durys, sunkvežimio vairuotojas bus nukreiptas iškrauti produktą tiesiogiai priekabą.
-   Jei nėra suplanuotos produkto perkėlimo veiklos, keltuvo vairuotojas bus nukreiptas atidėti produktą kurioje nors vidaus sandėlio (5) vietoje.

[![prekių skirstymas pagal aplinkybes](./media/scenario1.png)](./media/scenario1.png)

## <a name="configure-cross-docking"></a>Prekių skirstymo konfigūravimas
Prekių skirstymo procesą galite konfigūruoti **darbo strategijose**. Darbo strategija apima darbo užsakymo tipą, vietą ir produktą. Toliau pateikiamame pavyzdyje sukonfigūruotas produkto X ir vietos Y prekių skirstymas.

#### <a name="work-order-types"></a>Darbo užsakymo tipai

-   Darbo užsakymo tipas: pagamintos prekės, atidėti
-   Darbo kūrimo metodas: prekių skirstymas
-   Prekių skirstymo strategijos pavadinimas: perkėlimo užsakymai

#### <a name="inventory-locations"></a>Atsargų vietos

-   Sandėlio Nr.: 51
-   Buvimo vieta: Y

#### <a name="products"></a>Produktai

-   Prekės numeris: X

Šiuo metu gali būti konfigūruojamas tik dviejų tipų darbo užsakymų prekių skirstymas:

-   Baigtos prekės atidėtos
-   Sudėtinis produktas ir šalutinis produktas atidėti

Dalyje **Prekių skirstymo strategija** nurodote, kuri tipų dokumentai taikytini skirstant prekes. Šiuo metu palaikomas tik vieno tipo dokumentas **Perkėlimo užsakymai**. Toliau pateiktame pavyzdyje pavaizduota prekių skirstymo strategijos konfigūracija.

### <a name="cross-docking-policy-name-transfer-order"></a>Prekių skirstymo strategijos pavadinimas: perkėlimo užsakymas

-   Eilės numeris: 10
 -   Darbo užsakymo tipas: leidimas perkelti
-   Būtina nurodyti prekių skirstymo poreikio vietą: ne
-   Prekių skirstymo strategija: data ir laikas

### <a name="sequence-number"></a>Eilės numeris

Dalyje **Eilės numeris** nurodomas dokumento tipo prioritetas. Šiuo metu palaikomas tik vieno tipo dokumentas **Perkėlimo išdavimas**. Todėl eilės numeris tampa tinkamas tik tada, kai palaikoma daugiau darbo užsakymų tipų.

### <a name="cross-docking-policy"></a>Prekių skirstymo strategija

Nustatant prakių skirstymo strategiją taip pat nustatomas perkėlimo tvarkos poreikia pagal svarbą. Pavyzdžiui, jei yra keli to paties produkto perkėlimo užsakymai, užsakymų svarba nustatoma pagal suplanuotus ant krovinio nurodytus ir su perkėlimo užsakymu susietus datą ir laiką. Suplanuotą datą ir laiką galima nustatyti tiesiogiai ant krovinio arba su kroviniu susietoje dalyje **Paskyros grafikas**. Svarba nustatoma pagal prekių skirstymo strategiją. Šiuo metu yra tik viena strategija: **Data ir laikas**.

### <a name="cross-docking-demand-requires-location"></a>Būtina nurodyti prekių skirstymo poreikio vietą

Prekių skirstymo strategijoje galite nustatyti kriterijų, pagal kurį būtų reikalaujama, kad perkėlimo užsakymuose būtų nurodyta priskirta vieta, kad būtų galima atlikti prekių skirstymą. Šis kriterijus nustatytas lauke **Būtina nurodyti prekių skirstymo poreikio vietą**. Su kroviniu susietame paskyros grafike nurodyta vieta naudojama kaip galutinė skirstomų prekių vieta. Galutinė skirstomų prekių vieta nustatoma pagal darbo užsakymo tipo **Padėjimas** dalies **Perkėlimo išdavimas** vietos nurodymą. Gali būti naudinga nustatyti scenarijaus lauką **Būtina nurodyti prekių skirstymo poreikio vietą**, kuriame baigtos prekės turėtų būti skirstomos tik tada, jei įlankos durims priskirta priekaba. Tokiu atveju prekės perkeliamos tiesiogiai iš gamybos eilutės į priekabą. Įlankos durims priskyręs priekabą naudotojas priskirs paskyros grafiko vietą, todėl toje vietoje bus galima atlikti prekių skirstymą. Tolesniuose skyriuose išsamiai paaiškinami du pavyzdžiai.

#### <a name="scenario-1--cross-docking-from-production-to-transfer-orders"></a>1 scenarijus – Prekių skirstymas iš gamybos užsakymų į perkėlimo užsakymus

Po to, kai produktas gamybos eilutėje paskeliamas baigtu, jis perkeliamas į įlankos durų vietą ir ten yra įkeliamas į sunkvežimį ir nugabenamas į paskirstymo centrą. Naudokite įmonės USMF.

1.  Įgalinkite naują prekių skirstymo skaičių seką. Eikite į puslapį **Numeracijos** ir paspauskite mygtuką **Generuoti** . Vedlys padės jums atlikti šį procesą.
2.  Sukurkite prekių skirstymo strategiją. Eikite į puslapį **Prekių skirstymo strategija** ir sukurkite naują strategiją pavadinimu **Perkėlimo užsakymo prekių skirstymas**. Atkreipkite dėmesį, kad galite pasirinkti tik vieną darbo užsakymo tipą – **Perkėlimo išdavimas**, o vienintelė galima prekių skirstymo strategija yra **Data ir laikas**.
3.  Sukurkite darbo strategiją. Eikite į puslapį **Darbo strategijos** ir sukurkite naują darbo strategiją pavadinimu **Paskirstymas L0101**.
4.  Nustatykite, kad perkėlimo užsakymų kroviniai būtų kuriami automatiškai. Naudodami sandėlio parametrus nustatykite, kad sukūrus perkėlimo užsakymus kroriniai būtų kuriami automatiškai. Krovinys yra būtinoji sąlyga, kad perkėlimo užsakymą būtų galima naudoti prekių skirstymui.
5.  Nustatykite prekių krovinio susiejimą. Eikite į puslapį **Prekių krovinio siejimas** ir nustatykite standartinį prekių grupės **CarAudio** krovinio šabloną. Atliekant šį susiejimą sukūrus perkėlimo užsakymą krovinio šablonas į krovinį bus įterpiamas automatiškai.
6.  Sukurkite perkėlimo užsakymą. Sukurkite prekės numerio L0101 perkėlimo užsakymą. Kiekis = 20.
7.  Paskelbkite perkėlimo užsakymą iš krovinio planavimo darbo srities. Skirtuke **Siuntimas** pasirinkite krovinio planavimo darbo srities meniu elementą ir krovinio eilutės meniu **Išleidimas** pasirinkite **Išleidimas į sandėlį**. Dabar sukuriama perkėlimo užsakymo bangos eilutė, kurios tipas – **Perkėlimo išdavimas**.
8.  Sukurkite gamybos užsakymą. Eikite į sąrašo puslapį **Gamybos užsakymas** ir sukurkite produkto L0101 gamybos užsakymą. Kiekis = 20. Įvertinkite padėtį ir pradėkite vykdyti gamybos užsakymą. Atkreipkite dėmesį, kad ir toliau naudojama lauko **Registruoti išrinkimo dokumentą dabar** parinktis **Ne**.
9.  Naudodamiesi mobiliuoju įrenginiu praneškite, kad baigta. Eikite į mobiliojo įrenginio portalą ir pasirinkite meniu elementą **Skelbimas baigtu ir atidėjimas**. Dabar naudodamiesi rankiniu įrenginiu praneškite, kad prekė L0101 baigta. Kiekis = 10. Atkreipkite dėmesį, kad padėjimo vieta yra **BAYDOOR**. Šią vietą galima naudojant darbo užsakymo tipo **Padėjimas** vietos direktyvą **Perkėlimo išdavimas**. Taip pat atkreipkite dėmesį, kad sukurtas ir užbaigtas darbas, kurio tipas **Perkėlimo išdavimas**. Detalizuodami perkėlimo užsakymo darbo informaciją patvirtinkite darbą.
10. Dabar iš mobiliojo įrenginio praneškite apie papildomus 10 vienetų. Atkreipkite dėmesį, kad padėjimo vieta vėl yra **BAYDOOR**. Taip pat atkreipkite dėmesį, kad sukurtas naujas darbas, skirtas papildomiems 10 vienetų, kurio tipas **Perkėlimo išdavimas**.
11. Dabar naudodami gamybos užsakymą pabandykite paleisti dar 20 vienetų, o po to naudodami rankinį įrenginį praneškite, kad 20 ae baigtas. Šį kartą vietą **LP-001** siūloma naudoti kaip atidavimo vietą. Šią vietą galima rasti naudojant dalies **Baigtų prekių atidėjimas** vietos nurodymą. Šis vietos nurodymas naudojamas todėl, kad nėra kitos prekių skirstymo galimybės. Prekės LP-001 perkėlimo užsakymas buvo visiškai įvykdytas atlikus dvi prekių skirstymo veiklas, nurodytas 9 ir 10 veiksmuose. Atkreipkite dėmesį, kad darbas, kurio tipas **Baigtų prekių atidėjimas**, buvo sukurtas ir apdorotas.

#### <a name="scenario-2---cross-docking-from-production-to-transfer-orders-with-an-appointment-schedule"></a>2 scenarijus – prekių skirstymas nuo gamybos iki perkėlimo užsakymų, kuriuose nurodytas paskyros grafikas

Po to, kai gamybos eilutėje pranešama, kad produktas yra baigtas, jis perkeliamas į įlankos durų vietą, kuri nurodyta įlankos durų vietų paskyros grafike. Naudokite įmonės USMF.

1.  Pakeiskite prekių skirstymo strategiją. Pakeiskite prekių skirstymo strategiją, kurią sukūrėte 1 scenarijuje pažymėdami žymės langelį **Norint pamatyti prekių skirstymo poreikį, reikia nurodyti vietą**.
2.  Sukurkite naują perkėlimo užsakymą.
3.  Atidarykite dalį **Krovinio planavimo darbo sritis**.
4.  Iš krovinio planavimo darbo srities eikite į skyrių **Kroviniai** ir meniu **Transportavimas** pasirinkę **Paskyros grafikas** sukurkite naują paskyros grafiką. Atkeipkite dėmesį, kad paskyros grafike yra nuoroda į lauke **Užsakymo numeris** nurodytą perkėlimo užsakymą. Lauke **Suplanuota pradžios data / laikas vietoje** galite nustatyti paskyros datą ir laiką. Šie data ir laikas bus naudojami, kai atliekant prekių skirstymo procesą prekių skirstymo poreikis tampa prioritetiniu. Pagal šiame lauke nustatytus datą ir laiką bus atnaujintas atitinkamo krovinio laukas **Suplanuota krovinio siuntimo data ir laikas**. Nuo „FastTab“ skirtuke **Siuntimo informacija** nurodytos vietos priklauso tai, į kokią vietą bus siunčiamas tas perkėlimo užsakymas.
5.  Dalyje **Krovinio planavimo darbo sritis** paleiskite į sandėlį.
6.  Sukurkite gamybos užsakymą, skirtą prekei, kurios numeris **L0101**, ir nustatykite būseną **Pradėta**, nurodydami kiekį 20.
7.  Naudodamiesi mobiliuoju įrenginiu praneškite, kad baigta.
8.  Eikite į mobiliojo įrenginio portalą ir pasirinkite meniu elementą **Skelbimas baigtu ir atidėjimas**.
9.  Naudodamiesi rankiniu įrenginiu paskelbkite, kad prekė **L0101** baigta. Atkreipkite dėmesį, kad dabar padėjimo vieta yra **BAYDOOR 2**. Šią vietą galima rasti paskyros grafike, o ne vietos nurodyme **Perkėlimo kvitas**.

### <a name="additional-information"></a>Papildoma informacija

-   Prekių skirstymo scenarijus gali būti taikomas pagal paketą ir seriją kontroliuojamoms prekėms, kai rezervacijų hierarchijoje virš vietos ir po vieta nurodomos paketo ir serijos numerio dimensijos. 



