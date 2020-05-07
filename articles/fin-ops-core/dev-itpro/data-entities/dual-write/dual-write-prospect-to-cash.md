---
title: Potencialių klientų pavertimas grynaisiais pinigais dvigubo rašymo funkcijoje
description: Šioje temoje pateikiama informacija apie potencialų klientą pavertimą grynaisiais pinigais dvigubo rašymo funkcijoje.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 57aabeef0ee94b4b13bbe6e3925bcafe1e809ab2
ms.sourcegitcommit: 984604fd651d74aa49a2d7513f096faaf49f9f27
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/18/2020
ms.locfileid: "3270293"
---
# <a name="prospect-to-cash-in-dual-write"></a>Potencialių klientų pavertimas grynaisiais pinigais dvigubo rašymo funkcijoje

[!include [banner](../../includes/banner.md)]



Svarbus daugumos įmonių tikslas – paversti potencialius klientus į klientus, o tada išlaikyti nuolatinius verslo ryšius su tais klientais. Naudojant „Microsoft Dynamics 365“ programas, potencialių klientų pavertimo grynaisiais pinigais procesas vyksta per pasiūlymus arba užsakymų apdorojimo darbo eigas, o finansai yra suderinami ir atpažįstami. Potencialių klientų pavertimo grynaisiais pinigais integravimas su dvigubo rašymo funkcija sukuria darbo eigą, kuri priima pasiūlymą ir užsakymą, kuris yra „Dynamics 365 Sales“ arba „Dynamics 365 Supply Chain Management“ programose, o pasiūlymas ir užsakymas tampa prieinami abiejose programose.

Programos sąsajose galite pasiekti apdorojimo būsenas ir informaciją apie sąskaitą faktūrą realiuoju laiku. Todėl galite lengviau valdyti savo funkcijas, pvz., produktų laikymą, atsargų tvarkymą ir papildymą programoje „Supply Chain Management“, nekurdami pasiūlymų ir užsakymų iš naujo.

![Dvigubo rašymo duomenų srautas potencialių klientų pavertime grynaisiais pinigais](../dual-write/media/dual-write-prospect-to-cash[1].png)

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka

Kad galėtumėte sinchronizuoti pardavimo pasiūlymus, turite atnaujinti šiuos parametrus.

### <a name="setup-in-sales"></a>Sąranka sprendime „Sales“

Pardavimuose eikite į **Parametrai \> Administravimas \> Sistemos parametrai \> Pardavimai** ir įsitikinkite, kad naudojami toliau nurodyti parametrai:

- Sistemos parinktis **Naudoti sistemos prizų skaičiavimą** nustatyta į **Taip**.
- Laukas **Nuolaidos skaičiavimo būdas** nustatytas į **Eilutės elementas**.

### <a name="sites-and-warehouses"></a>Svetainės ir sandėliai

„Supply Chain Management“ programoje laukai **Svetainė** ir **sandėlys** yra privalomi pasiūlymo eilutėms ir užsakymo eilutėms. Jei nustatysite svetainę ir sandėlį numatytuose užsakymo parametruose, tie laukai bus automatiškai nustatyti, kai pridėsite produktą į pasiūlymo eilutę ar užsakymo eilutę. 

### <a name="number-sequences-for-quotations-and-orders"></a>Pasiūlymų ir užsakymų numeracijos

Numeracijos, skirtos „Supply Chain Management“ ir „Sales“, neprijungtos, kai pasiūlymai ir užsakymai sukuriami ir sinchronizuojami „Sales“ ir „Supply Chain Management“ programose. Jei pardavimo užsakymas, sukurtas „Sales“ programoje, sinchronizuojamas į „Supply Chain Management“, jis turės tokį patį pardavimo užsakymo numerį „Supply Chain Management“ programoje. Norėdami užtikrinti, kad pardavimo užsakymo numeris nebūtų dubliuojamas, dviejose programose turite naudoti skirtingas numeravimo sistemas.

Pavyzdžiui, numeracija „Supply Chain Management“ programoje yra **1, 2, 3, 4, 5, ...**, o numeracija „Sales“ programoje yra **100, 99, 98, ...**. Jei kuriate 100 pardavimo užsakymų „Sales“ programoje, pardavimo numeris galiausiai bus sugeneruotas tas, kuris jau yra „Supply Chain Management“ programoje. Kitaip tariant, dvi numeracijos galiausiai sutaps su pardavimo užsakymais, sukurtais „Supply Chain Management“ ir „Sales“. Vietoje to galite naudoti numeraciją **F1, F2, F3, ...** „Supply Chain Management“ programoje, o numeraciją **C1, C2, C3, ...** „Sales“ programoje. Šios numeracijos niekada nepateiks pasikartojančių pardavimo užsakymų numerių.

## <a name="sales-quotations"></a>Pardavimo pasiūlymai

Pardavimo pasiūlymai gali būti kuriami programose „Sales“ arba „Supply Chain Management“. Jei kuriate pasiūlymą „Sales“ programoje, jis bus sinchronizuojamas su „Supply Chain Management“ realiuoju laiku. Taip pat jei kuriate pasiūlymą „Supply Chain Management“ programoje, jis bus sinchronizuojamas su „Sales“ realiuoju laiku. Atkreipkite dėmesį į toliau nurodytus punktus.

+ Pasiūlyme galite pridėti nuolaidą produktui. Šiuo atveju nuolaida bus sinchronizuojama su „Supply Chain Management“. Antraštės laukus **Nuolaida**, **Išlaidos** ir **Mokesčiai** valdo Tiekimo grandinės valdymo sąranka. Šioje sąrankoje nepalaikomas integravimo susiejimas. Vietoje to, laukai **Kaina**, **Nuolaida**, **Išlaidos** ir **Mokesčiai** išlaikyti ir tvarkomi „Supply Chain Management“ programoje.
+ Laukai **Nuolaidos %**, **Nuolaida** ir **Transportavimo suma**, esantys pardavimo pasiūlymo antraštėje yra skirti tik skaitymui.
+ Laukai **Transportavimo sąlygos**, **Pristatymo sąlygos** **Siuntimo būdas** ir **Pristatymo būdas** neįtraukti į numatytuosius susiejimus. Norėdami susieti šiuos laukus, turite nustatyti reikšmių susiejimą, kuris atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.

Jei taip pat naudojate sprendimą „Field Service”, nepamirškite iš naujo įgalinti parametro **Pasiūlymo eilutės greitasis kūrimas**. Iš naujo įgalinus parametrą galima toliau kurti pasiūlymo eilutes naudojant greitojo kūrimo funkciją.
1. Pereikite į „Dynamics 365 Sales” programą.
2. Viršutinėje naršymo juostoje pasirinkite parametrų piktogramą.
3. Pasirinkite **Išplėstiniai parametrai**.
4. Pasirinkite parinktį **Tinkinti sistemą**.
5. Pasirinkite meniu elementą **Pasiūlymo eilutė**.
6. Eikite į skyrių **Duomenų paslaugos** ir pasirinkite žymės langelį **Leisti greitąjį kūrimą**.

## <a name="sales-orders"></a>Pardavimo užsakymai

Pardavimo užsakymai gali būti kuriami programose „Sales“ arba „Supply Chain Management“. Jei kuriate pardavimo užsakymą „Sales“ programoje, jis bus sinchronizuojamas su „Supply Chain Management“ realiuoju laiku. Taip pat jei kuriate pardavimo užsakymą „Supply Chain Management“ programoje, jis bus sinchronizuojamas su „Sales“ realiuoju laiku. Atkreipkite dėmesį į toliau nurodytus punktus.

+ Galite aktyvinti ir sinchronizuoti užsakymus iš „Sales“ tik tada, jei visi užsakyme esantys produktai gaunami iš „Finance and Operations“ programų. Todėl produktuose negali būti atliekami rašymai.
+ Nuolaidų skaičiavimas ir apvalinimas:

    - „Sales“ nuolaidos skaičiavimo modelis skiriasi nuo Tiekimo grandinės valdymo nuolaidos skaičiavimo modelio. Tiekimo grandinės valdyme galutinė nuolaidos suma pardavimo eilutėje gali būti nuolaidos sumų ir nuolaidos procentų kombinacijos suma. Jei ši galutinė nuolaidos suma eilutėje padalinama pagal kiekį, gali būti taikomas apvalinimas. Tačiau apvalinimo taikymas nėra svarstomas, jei suapvalinta vieneto nuolaidos suma sinchronizuojama su „Sales“. Norint padėti užtikrinti, kad visa nuolaidos suma iš pardavimo eilutės „Supply Chain Management“ programoje yra tinkamai sinchronizuota su „Sales“, visa suma turi būti sichronizuota neskirstant jos pagal eilutės kiekį. Todėl turite apibrėžti nuolaidos apskaičiavimo būdą kaip **EIlutės elementas** „Sales“ programoje.
    - „Sales“ pardavimo užsakymo eilutę sinchronizuojant su „Supply Chain Management“, naudojama visos eilutės nuolaidos suma. Tiekimo grandinės valdyme nėra lauko, kuriame būtų galima saugoti visą nuolaidos eilutės sumą, todėl suma yra suskirstoma pagal kiekį ir saugoma lauke **Eilutės nuolaida**. Skirstymo metu bet koks įvykstantis apvalinimas išsaugomas pardavimo eilutės lauke **Pardavimo mokesčiai**.

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>Pavyzdys: Sinchronizavimas iš „Sales“ į „Supply Chain Management“

Turite šį pardavimo užsakymą:

+ **„Sales“:** kiekis = 3, atskiros eilutės nuolaida = 10,00 USD
+ **„Supply Chain Management“:** Kiekis = 3, eilutės nuolaidos suma = 3,33 USD, pardavimo mokestis = -0,01 USD

Jeigu sinchronizuojate „Supply Chain Management“ su „Sales“, gausite tokį rezultatą:

+ **„Supply Chain Management“:** Kiekis = 3, eilutės nuolaidos suma = 3,33 USD, pardavimo mokestis = -0,01 USD
+ **„Sales“:** kiekis = 3, atskiros eilutės nuolaida = (3 × 3,33 USD) + 0,01 USD = 10,00 USD

## <a name="dual-write-solution-for-sales"></a>Dvigubo rašymo sprendimas, skirtas „Sales“

Į objektą **Užsakymas** buvo įtraukti nauji laukai, rodomi puslapyje. Dauguma šių laukų rodomi „Sales“ skirtuke **Integravimas**. Yra keli specialūs laukai:

+ Lauke **Apdorojimo būsena** rodoma „Supply Chain Management“ užsakymo apdorojimo būsena. Šis laukas užrakintas ir rodo tik „Supply Chain Management“ užsakymo būseną. Galimos šios vertės:

    + **Aktyvus** – būsena, kai užsakymas „Sales“ suaktyvinamas naudojant mygtuką **Aktyvinti**.
    + **Pritarta**
    + **Pristatyta**
    + **Išrašyta SF**
    + **Iš dalies pristatyta**
    + **Iš dalies išrašyta SF**
    + **Paimta**
    + **Atšaukta**

    Šioje lentelėje parodyta, kaip apdorojimo būsena susieta su **CRM būsenos kodo** verte.

    | Apdorojimo būsena           | CRM būsenos kodas    |
    |-----------------------------|--------------------|
    | Aktyvi                      | Nauja / laukiama / sulaikyta |
    | Patvirtinta / išrinkta            | Vykdoma        |
    | Iš dalies pristatyta         | Dalinis            |
    | Pristatyta                   | Atlikta           |
    | Išrašyta SF / iš dalies išrašyta SF | Išrašyta SF           |
    | Atšaukta                    | Nėra pinigų           |

+ Mygtukai **Kurti sąskaitą faktūrą** ir **Atšaukti užsakymą** puslapyje **Pardavimų užsakymai** yra paslėpti „Sales“.
+ Reikšmė **Pardavimų užsakymo būsena** išliks **Aktyvi**, kad padėtų užtikrinti, jog „Supply Chain Management“ keitimai galėtų būti perkelti į „Sales“ pardavimų užsakymą. Norėdami valdyti šią veikimo būdą, numatytąją **Būsenos kodas \[Būsena\]** reikšmę nustatykite į **Aktyvi**.

## <a name="invoices"></a>Sąskaitos faktūros

Pardavimo sąskaitos faktūros kuriamos „Supply Chain Management“ programoje ir sinchronizuojamos su „Sales“. Atkreipkite dėmesį į toliau nurodytus punktus.

+ Į objektą **Sąskaita faktūra** įtrauktas ir puslapyje rodomas laukas **Sąskaitos faktūros numeris**.
+ Puslapyje **Pardavimo užsakymas** esantis mygtukas **Kurti sąskaitą faktūrą** yra paslėptas, nes sąskaitos faktūros bus kuriamos „Supply Chain Management“ programoje ir sinchronizuojamos su „Sales“. Puslapio **Sąskaita faktūra** redaguoti negalima, nes sąskaitos faktūros bus sinchronizuojamos iš „Supply Chain Management“.
+ **Pardavimų užsakymo būsenos** reikšmė automatiškai keičiama į **Išrašyta sąskaita faktūra**, kai susijusi „Supply Chain Management“ sąskaita faktūra sinchronizuojama į „Sales“. Be to, pardavimo užsakymo, iš kurio buvo sukurta sąskaita faktūra, savininkas priskiriamas sąskaitos faktūros savininku. Todėl pardavimo užsakymo savininkas gali peržiūrėti sąskaitą faktūrą.
+ Laukai **Transportavimo sąlygos**, **Pristatymo sąlygos** ir **Pristatymo būdas** neįtraukti į numatytuosius susiejimus. Norėdami susieti šiuos laukus, turite nustatyti reikšmių susiejimą, kuris atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.

## <a name="templates"></a>Šablonai

Potencialių klientų pavertimą grynaisiais pinigais sudaro pagrindinių objektų schemų, veikiančių kartu interaktyviai naudojant duomenis, rinkinys, kaip parodyta tolesnėje lentelėje.

| „Finance and Operations” programėlės | Modeliu grįstos programos „Dynamics 365“ | aprašymas |
|-----------------------------|-----------------------------------|-------------|
| Pardavimo SF antraštės V2    | SF                          |             |
| Pardavimo sąskaitos faktūros eilutės V2      | invoicedetails                    |             |
| CDS pardavimo užsakymų antraštės     | salesorders                       |             |
| CDS pardavimo užsakymo eilutės       | salesorderdetails                 |             |
| Pardavimo užsakymo kilmės kodai    | msdyn\_salesorderorigins          |             |
| CDS pardavimo pasiūlymo antraštė  | pasiūlymai                            |             |
| CDS pardavimo pasiūlymo eilutės   | quotedetails                      |             |

Čia yra susiję pagrindinių objektų schemos, skirtos potencialių klientų pavertimui grynaisiais pinigais:

+ [Klientai V3 su sąskaitomis](customer-mapping.md#customers-v3-to-accounts)
+ [CDS kontaktai V2 su kontaktais](customer-mapping.md#cds-contacts-v2-to-contacts)
+ [Klientai V3 su kontaktais](customer-mapping.md#customers-v3-to-contacts)
+ [Išleisti produktai V2 su msdyn_sharedproductdetails](product-mapping.md#released-products-v2-to-msdyn_sharedproductdetails)
+ [Visi produktai su msdyn_globalproducts](product-mapping.md#all-products-to-msdyn_globalproducts)
+ [Kainoraštis](product-mapping.md)

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [sales invoice](includes/SalesInvoiceHeaderV2Entity-invoice.md)]

[!include [sales invoice line](includes/SalesInvoiceLineV2Entity-invoicedetail.md)]

[!include [sales order header](includes/SalesOrderHeaderCDSEntity-salesorder.md)]

[!include [sales order line](includes/SalesOrderLineCDSEntity-salesorderdetails.md)]

[!include [sales order origin](includes/SalesOrderOriginEntity-msdyn-salesorderorigin.md)]

[!include [sales quotation header](includes/SalesQuotationHeaderCDSEntity-quote.md)]

[!include [sales quotation line](includes/SalesQuotationLineCDSEntity-QuoteDetails.md)]
