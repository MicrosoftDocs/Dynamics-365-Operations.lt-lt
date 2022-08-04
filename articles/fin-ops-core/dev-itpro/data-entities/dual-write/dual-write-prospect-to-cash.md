---
title: Potencialių klientų pavertimas grynaisiais pinigais dvigubo rašymo funkcijoje
description: Šiame straipsnyje pateikta informacija apie dvigubo rašymo potencialų klientą ir grynuosius pinigus.
author: RamaKrishnamoorthy
ms.date: 01/07/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: f44574abddb71e1a994ae60960e8c9c79242aff0
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112119"
---
# <a name="prospect-to-cash-in-dual-write"></a>Potencialių klientų pavertimas grynaisiais pinigais dvigubo rašymo funkcijoje

[!include [banner](../../includes/banner.md)]

Svarbus daugumos įmonių tikslas – paversti potencialius klientus į klientus, o tada išlaikyti nuolatinius verslo ryšius su tais klientais. Naudojant „Microsoft Dynamics 365“ programas, potencialių klientų pavertimo grynaisiais pinigais procesas vyksta per pasiūlymus arba užsakymų apdorojimo darbo eigas, o finansai yra suderinami ir atpažįstami. Potencialių klientų pavertimo grynaisiais pinigais integravimas su dvigubo rašymo funkcija sukuria darbo eigą, kuri priima pasiūlymą ir užsakymą, kuris yra „Dynamics 365 Sales“ arba „Dynamics 365 Supply Chain Management“ programose, o pasiūlymas ir užsakymas tampa prieinami abiejose programose.

Programos sąsajose galite pasiekti apdorojimo būsenas ir informaciją apie sąskaitą faktūrą realiuoju laiku. Todėl galite lengviau valdyti savo funkcijas, pvz., produktų laikymą, atsargų tvarkymą ir papildymą programoje „Supply Chain Management“, nekurdami pasiūlymų ir užsakymų iš naujo.

![Dvigubo rašymo duomenų srautas potencialių klientų pavertime grynaisiais pinigais.](../dual-write/media/dual-write-prospect-to-cash[1].png)

Informacijos apie klientų ir kontaktų integravimą ieškokite [Integruotas kliento šablonas](customer-mapping.md). Daugiau informacijos apie produkto integravimą žiūrėkite [Bendroji produkto patirtis](product-mapping.md).

> [!NOTE]
> „Dynamics 365 Sales” tiek klientas, tiek potencialus klientas nurodo į lentelės **Sąskaita** įrašą, kur stulpelis **Ryšio tipas** yra **Potencialus klientas** arba **Klientas**. Jei jūsų verslo **logika** **apima** sąskaitos kvalifikacijos procesą, kuriame sukuriamas sąskaitos įrašas ir pirmiausia jį galima naudoti kaip potencialų klientą, o tada kaip klientas, tas įrašas sinchronizuojamas su finansų ir operacijų programa tik tada, kai jis yra klientas ().`RelationshipType=Customer` Jei norite, kad eilutė **Sąskaita** būtų sinchronizuojama kaip potencialus klientas, tada reikalinga pasirinktinė schema potencialaus kliento duomenų integravimui.

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka

Kad galėtumėte sinchronizuoti pardavimo pasiūlymus, turite atnaujinti šiuos parametrus.

### <a name="setup-in-sales"></a>Sąranka sprendime „Sales“

Pardavimuose eikite į **Parametrai \> Administravimas \> Sistemos parametrai \> Pardavimai** ir įsitikinkite, kad naudojami toliau nurodyti parametrai:

- Sistemos parinktis **Naudoti sistemos kainų skaičiavimą** nustatyta į **Taip**.
- Stulpelis **Nuolaidos skaičiavimo būdas** nustatytas į **Eilutės elementas**.

### <a name="sites-and-warehouses"></a>Svetainės ir sandėliai

„Supply Chain Management“ stulpeliai **Svetainė** ir **sandėlis** yra privalomi pasiūlymo ir užsakymo eilutėms. Jei nustatysite svetainę ir sandėlį numatytuose užsakymo parametruose, tie stulpeliai bus automatiškai nustatyti, kai pridėsite produktą į pasiūlymo eilutę ar užsakymo eilutę. 

### <a name="number-sequences-for-quotations-and-orders"></a>Pasiūlymų ir užsakymų numeracijos

Numeracijos, skirtos „Supply Chain Management“ ir „Sales“, neprijungtos, kai pasiūlymai ir užsakymai sukuriami ir sinchronizuojami „Sales“ ir „Supply Chain Management“ programose. Jei pardavimo užsakymas, sukurtas „Sales“ programoje, sinchronizuojamas į „Supply Chain Management“, jis turės tokį patį pardavimo užsakymo numerį „Supply Chain Management“ programoje. Norėdami užtikrinti, kad pardavimo užsakymo numeris nebūtų dubliuojamas, dviejose programose turite naudoti skirtingas numeravimo sistemas.

Pavyzdžiui, numeracija „Supply Chain Management“ programoje yra **1, 2, 3, 4, 5, ...**, o numeracija „Sales“ programoje yra **100, 99, 98, ...**. Jei kuriate 100 pardavimo užsakymų „Sales“ programoje, pardavimo numeris galiausiai bus sugeneruotas tas, kuris jau yra „Supply Chain Management“ programoje. Kitaip tariant, dvi numeracijos galiausiai sutaps su pardavimo užsakymais, sukurtais „Supply Chain Management“ ir „Sales“. Vietoje to galite naudoti numeraciją **F1, F2, F3, ...** „Supply Chain Management“ programoje, o numeraciją **C1, C2, C3, ...** „Sales“ programoje. Šios numeracijos niekada nepateiks pasikartojančių pardavimo užsakymų numerių.

## <a name="sales-quotations"></a>Pardavimo pasiūlymai

Pardavimo pasiūlymai gali būti kuriami programose „Sales“ arba „Supply Chain Management“. Jei kuriate pasiūlymą „Sales“ programoje, jis bus sinchronizuojamas su „Supply Chain Management“ realiuoju laiku. Taip pat jei kuriate pasiūlymą „Supply Chain Management“ programoje, jis bus sinchronizuojamas su „Sales“ realiuoju laiku. Atkreipkite dėmesį į toliau nurodytus punktus.

+ Pasiūlyme galite pridėti nuolaidą produktui. Šiuo atveju nuolaida bus sinchronizuojama su „Supply Chain Management“. Antraštės stulpelius **Nuolaida**, **Išlaidos** ir **Mokesčiai** valdo „Supply Chain Management” sąranka. Šioje sąrankoje nepalaikomas integravimo susiejimas. Vietoj to, stulpeliai **Kaina**, **Nuolaida**, **Išlaidos** ir **Mokesčiai** yra pralaikomi ir tvarkomi „Supply Chain Management“.
+ Stulpeliai **Nuolaidos %**, **Nuolaida** ir **Transportavimo suma**, esantys pardavimo pasiūlymo antraštėje yra tik skaitymui skirti stulpeliai.
+ Stulpeliai **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** nėra įtraukti į numatytuosius susiejimus. Norėdami susieti šiuos stulpelius, turite nustatyti reikšmių schemą, atitinkančią organizacijų, tarp kurių lentelė sinchronizuojama, duomenis.

Jei taip pat naudojate sprendimą „Field Service”, nepamirškite iš naujo įjungti parametro **Kainos linijos greitasis kūrimas**. Iš naujo įgalinus parametrą galite toliau kurti pasiūlymo eilutes naudojant greitojo kūrimo funkciją.

1. Pereikite į „Dynamics 365 Sales” programą.
2. Viršutinėje naršymo juostoje pasirinkite parametrų piktogramą.
3. Pasirinkite **Išplėstiniai parametrai**.
4. Pasirinkite parinktį **Tinkinti sistemą**.
5. Pasirinkite meniu elementą **Pasiūlymo eilutė**.
6. Eikite į skyrių **Duomenų paslaugos** ir pasirinkite žymės langelį **Leisti greitąjį kūrimą**.

## <a name="sales-orders"></a>Pardavimo užsakymai

Pardavimo užsakymai gali būti kuriami programose „Sales“ arba „Supply Chain Management“. Jei kuriate pardavimo užsakymą „Sales“ programoje, jis bus sinchronizuojamas su „Supply Chain Management“ realiuoju laiku. Taip pat jei kuriate pardavimo užsakymą „Supply Chain Management“ programoje, jis bus sinchronizuojamas su „Sales“ realiuoju laiku. Atkreipkite dėmesį į toliau nurodytus punktus.

+ Įrašomieji produktai „Dynamics 365 Sales” bus rodomi kaip produktų kategorijos „Dynamics 365 Supply Chain Management”.
+ Nuolaidų skaičiavimas ir apvalinimas:

    - „Sales“ nuolaidos skaičiavimo modelis skiriasi nuo Tiekimo grandinės valdymo nuolaidos skaičiavimo modelio. Tiekimo grandinės valdyme galutinė nuolaidos suma pardavimo eilutėje gali būti nuolaidos sumų ir nuolaidos procentų kombinacijos suma. Jei ši galutinė nuolaidos suma eilutėje padalinama pagal kiekį, gali būti taikomas apvalinimas. Tačiau apvalinimo taikymas nėra svarstomas, jei suapvalinta vieneto nuolaidos suma sinchronizuojama su „Sales“. Norint padėti užtikrinti, kad visa nuolaidos suma iš pardavimo eilutės „Supply Chain Management“ programoje yra tinkamai sinchronizuota su „Sales“, visa suma turi būti sichronizuota neskirstant jos pagal eilutės kiekį. Todėl turite apibrėžti nuolaidos apskaičiavimo būdą kaip **EIlutės elementas** „Sales“ programoje.
    - „Sales“ pardavimo užsakymo eilutę sinchronizuojant su „Supply Chain Management“, naudojama visos eilutės nuolaidos suma. „Supply Chain Management” nėra stulpelio, kuriame būtų galima saugoti visą nuolaidos eilutės sumą, todėl suma yra suskirstoma pagal kiekį ir saugoma **Eilutės nuolaida** stulpelyje. Skirstymo metu bet koks įvykstantis apvalinimas išsaugomas **Pardavimo mokesčiai** pardavimo eilutės stulpelyje.

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>Pavyzdys: Sinchronizavimas iš „Sales“ į „Supply Chain Management“

Turite šį pardavimo užsakymą:

+ **„Sales“:** kiekis = 3, atskiros eilutės nuolaida = 10,00 USD
+ **„Supply Chain Management“:** Kiekis = 3, eilutės nuolaidos suma = 3,33 USD, pardavimo mokestis = -0,01 USD

Jeigu sinchronizuojate „Supply Chain Management“ su „Sales“, gausite tokį rezultatą:

+ **„Supply Chain Management“:** Kiekis = 3, eilutės nuolaidos suma = 3,33 USD, pardavimo mokestis = -0,01 USD
+ **„Sales“:** kiekis = 3, atskiros eilutės nuolaida = (3 × 3,33 USD) + 0,01 USD = 10,00 USD

## <a name="dual-write-solution-for-sales"></a>Dvigubo rašymo sprendimas, skirtas „Sales“

Į lentelę **Užsakymas** buvo įtraukti nauji stulpeliai, rodomi puslapyje. „Sales“ skirtuke **Integravimas** rodoma dauguma šių stulpelių. Daugiau informacijos apie tai, kaip susieti būsenos stulpeliai, žiūrėkite [Pardavimo užsakymo būsenos stulpelių susiejimo nustatymas](sales-status-map.md).

+ Mygtukai **Kurti sąskaitą faktūrą** ir **Atšaukti užsakymą** puslapyje **Pardavimų užsakymai** yra paslėpti „Sales“.
+ Reikšmė **Pardavimų užsakymo būsena** išliks **Aktyvi**, kad padėtų užtikrinti, jog „Supply Chain Management“ keitimai galėtų būti perkelti į „Sales“ pardavimų užsakymą. Norėdami valdyti šią veikimo būdą, numatytąją **Būsenos kodas \[Būsena\]** reikšmę nustatykite į **Aktyvi**.

## <a name="invoices"></a>Sąskaitos faktūros

Pardavimo sąskaitos faktūros kuriamos „Supply Chain Management“ programoje ir sinchronizuojamos su „Sales“. Atkreipkite dėmesį į toliau nurodytus punktus.

+ Į lentelę **Sąskaita faktūra** įtrauktas ir puslapyje rodomas **Sąskaitos faktūros numeris** stulpelis.
+ Puslapyje **Pardavimo užsakymas** esantis mygtukas **Kurti sąskaitą faktūrą** yra paslėptas, nes sąskaitos faktūros bus kuriamos „Supply Chain Management“ programoje ir sinchronizuojamos su „Sales“. Puslapio **Sąskaita faktūra** redaguoti negalima, nes sąskaitos faktūros bus sinchronizuojamos iš „Supply Chain Management“.
+ **Pardavimų užsakymo būsenos** reikšmė automatiškai keičiama į **Išrašyta sąskaita faktūra**, kai susijusi „Supply Chain Management“ sąskaita faktūra sinchronizuojama į „Sales“. Be to, pardavimo užsakymo, iš kurio buvo sukurta sąskaita faktūra, savininkas priskiriamas sąskaitos faktūros savininku. Todėl pardavimo užsakymo savininkas gali peržiūrėti sąskaitą faktūrą.
+ Stulpeliai **Transportavimo sąlygos**, **Pristatymo sąlygos** ir **Pristatymo būdas** neįtraukti į numatytuosius susiejimus. Norėdami susieti šiuos stulpelius, turite nustatyti reikšmių schemą, atitinkančią organizacijų, tarp kurių lentelė sinchronizuojama, duomenis.

## <a name="templates"></a>Šablonai

Potencialių klientų pavertimą grynaisiais pinigais sudaro pagrindinių lentelių schemų, veikiančių kartu interaktyviai naudojant duomenis, rinkinys, kaip parodyta tolesnėje lentelėje.

| „Finance and operations” programos | „Customer engagement“ programos | Aprašymas |
|-----------------------------|-----------------------------------|-------------|
[Visi produktai](mapping-reference.md#138) | msdyn_globalproducts | |
[Klientai V3](mapping-reference.md#101) | sąskaitos | |
[Klientai V3](mapping-reference.md#116) | kontaktai | |
[V2 kontaktai](mapping-reference.md#221) | msdyn_contactforparties | |
[CDS pardavimo užsakymų antraštės](mapping-reference.md#217) | salesorders | |
[CDS pardavimo užsakymo eilutės](mapping-reference.md#216) | salesorderdetails | |
[CDS pardavimo pasiūlymo antraštė](mapping-reference.md#215) | pasiūlymai | |
[CDS pardavimo pasiūlymo eilutės](mapping-reference.md#214) | quotedetails | |
[Išleisti produktai V2](mapping-reference.md#189) | „msdyn_sharedproductdetails” | |
[Pardavimo SF antraštės V2](mapping-reference.md#118) | SF | Pardavimo SF antraščių V2 lentelėje, kuri yra finansų ir operacijų programoje, yra pardavimo užsakymų SF ir laisvos formos SF. „Dataverse” taikomas dvigubo rašymo filtras, kuris išfiltruos visus laisvos formos sąskaitos faktūros dokumentus. |
[Pardavimo sąskaitos faktūros eilutės V2](mapping-reference.md#117) | invoicedetails | |
[Pardavimo užsakymo kilmės kodai](mapping-reference.md#186) | „msdyn_salesorderorigins” | |

Daugiau informacijos apie kainų sąrašus rasite [Bendroji produkto patirtis](product-mapping.md).

## <a name="limitations"></a>Apribojimai

- Grąžinimo užsakymai nėra palaikomi.
- Kredito pažymos nėra palaikomos.
- Bendriesiems duomenims, pavyzdžiui, klientui ir tiekėjui, turi būti nustatytos finansinės dimensijos. Kai klientas įtraukiamas į pasiūlymą arba pardavimo užsakymą, su kliento įrašu susijusios finansinės dimensijos į užsakymą įtraukiamos automatiškai. Šiuo metu dvigubas rašymas neapima finansinių dimensijų duomenų, skirtų bendriesiems duomenims.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

