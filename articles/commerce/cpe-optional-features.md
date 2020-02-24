---
title: Pasirinktinių „Dynamics 365 Commerce” peržiūros aplinkos funkcijų konfigūravimas
description: Šioje temoje paaiškinama, kaip sukonfigūruoti pasirenkamas „Microsoft Dynamics 365 Commerce“ peržiūros aplinkos funkcijas.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 43b23b9ef881b2ab2f3d005d4ba761848a7fa4ed
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024734"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-preview-environment"></a>Pasirinktinių „Dynamics 365 Commerce” peržiūros aplinkos funkcijų konfigūravimas


[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip sukonfigūruoti pasirenkamas „Microsoft Dynamics 365 Commerce“ peržiūros aplinkos funkcijas.

## <a name="prerequisites"></a>Būtinieji komponentai

Jei norite įvertinti operacines el. pašto funkcijas, turi būti įvykdytos šios būtinosios sąlygos:

- Turite pasiekiamą el. pašto serverį (paprastųjų pašto siuntų protokolo \[SMTP\] serverį), kuris gali būti naudojamas iš „Microsoft Azure“ prenumeratos, kurioje sukonfigūravote peržiūros aplinką.
- Turite pasiekiamus serverio visiškai apibrėžtą domeno vardą (FQDN) / IP adresą, SMTP prievado numerį ir autentifikavimo informaciją.

Jei norite įvertinti skaitmeninių išteklių valdymo funkcijas tiesiogiai naudodami daugiakanalės platformos vaizdus, turite turėti savo turinio valdymo sistemos (TVS) nuomotojo vardą. Nurodymai, kaip rasti šį vardą, pateikiami toliau šioje temoje. >>>(K: kur yra nurodymai?)

## <a name="configure-the-image-back-end"></a>Vaizdų posistemio konfigūravimas

### <a name="find-your-media-base-url"></a>Pagrindinio medijos URL radimas

> [!NOTE]
> Kad galėtumėte atlikti šią procedūrą, turite atlikti dalyje [Svetainės nustatymas programoje „Commerce“](cpe-post-provisioning.md#set-up-your-site-in-commerce) nurodytus veiksmus.

1. Prisijunkite prie „Commerce“ svetainių valdymo įrankio naudodami URL, kurį pasižymėjote inicijuodami el. prekybą jos konfigūravimo metu (žr. [El. prekybos inicijavimas](provisioning-guide.md#initialize-e-commerce)).
1. Atidarykite **„Fabrikam“** svetainę.
1. Kairėje esančiame meniu pasirinkite **Ištekliai**.
1. Pasirinkite bet kurį vieną vaizdo išteklių.
1. Dešinėje esančiame ypatybių inspektoriuje suraskite ypatybę **Viešasis URL**. Jos reikšmė yra URL. Toliau pateikiamas pavyzdys.

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.

1. Paskutinį URL identifikatorių (pirmiau pateiktame pavyzdyje – **MA1nQC**) pakeiskite eilute **search?fileName=**. Toliau parodyta, kaip atrodo taip pakeistas URL pavyzdys.

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    Šis URL yra jūsų pagrindinis medijos URL. Jį pasižymėkite.

### <a name="update-the-media-base-url"></a>Pagrindinio medijos URL naujinimas

1. Prisijunkite prie „Dynamics 365 Retail“.
1. Naudodami kairėje esantį meniu, nueikite į **Moduliai \> „Retail“ \> Kanalo sąranka \> Kanalo profiliai**.
1. Pasirinkite **Redaguoti**.
1. Dalyje **Profilio ypatybės** ypatybės **Pagrindinis medijos serverio URL** reikšmę pakeiskite savo anksčiau sukurtu pagrindiniu medijos URL.
1. Kairėje esančiame sąraše prie kanalo **Numatytasis** pasirinkite kitą kanalą.
1. Dalyje **Profilio ypatybės** pasirinkite **Įtraukti**.
1. Kaip įtrauktos ypatybės raktą pasirinkite **Pagrindinis medijos serverio URL**. Kaip ypatybės reikšmę įveskite savo anksčiau sukurtą pagrindinį medijos URL.
1. Pasirinkite **Įrašyti**.

## <a name="configure-the-email-server"></a>El. pašto serverio konfigūravimas

> [!NOTE]
> SMTP serveris arba el. pašto paslauga, kuriuos čia įvedate, turi būti pasiekiami „Azure“ prenumeratoje, kurią naudojate aplinkoje.

1. Prisijunkite prie „Retail“.
1. Naudodami kairėje esantį meniu, nueikite į **Moduliai \> Sistemos administravimas \> Sąranka \> El. paštas \> El. pašto parametrai**.
1. Skirtuko **SMTP parametrai** lauke **Siunčiamo pašto serveris** įveskite savo SMTP serverio ar el. pašto tarnybos FQDN arba IP adresą.
1. Lauke **SMTP prievado numeris** įveskite prievado numerį. (Jei nenaudojate saugiųjų jungčių lygmens \[SSL\], numatytasis prievado numeris yra **25**.)
1. Jei reikalinga autentifikacija, įveskite reikšmes laukuose **Vartotojo vardas** ir **Slaptažodis**.
1. Pasirinkite **Įrašyti**.
1. Pasirinkite **Atnaujinti**.
1. Skirtuko **Bandomasis el. laiškas** lauke **El. pašto teikėjas** pasirinkite **SMTP**.
1. Lauke **Gavėjas** įveskite el. pašto adresą, kuriuo bandomasis el. laiškas turi būti pristatytas.
1. Pasirinkite **Išsiųsti bandomąjį el. laišką**.

## <a name="configure-email-templates"></a>El. laiškų šablonų konfigūravimas

Kiekvieno operacinio įvykio, dėl kurio norite siųsti el. laiškus, el. laiškų šabloną turite atnaujinti galiojančiu siuntėjo el. pašto adresu.

1. Prisijunkite prie „Retail“.
1. Naudodami kairėje esantį meniu, nueikite į **Moduliai \> Organizacijos administravimas \> Sąranka \> Organizacijos el. laiškų šablonai**.
1. Pasirinkite **Rodyti sąrašą**.
1. Su kiekvienu sąraše esančiu šablonu atlikite toliau nurodytus veiksmus.

    1. Lauke **Siuntėjo el. paštas** įveskite siuntėjo el. pašto adresą.
    1. Nebūtina: lauke **Siuntėjo vardas** įveskite vardą, kuris turi būti naudojamas kaip siuntėjo vardas.

1. Pasirinkite **Įrašyti**.

## <a name="customize-email-templates"></a>El. laiškų šablonų tinkinimas

Galbūt norėsite el. laiškų šablonus tinkinti, kad juose būtų naudojami skirtingi vaizdai. Arba galbūt norėsite atnaujinti šablonų saitus, kad jų paskirties vieta būtų jūsų peržiūros aplinka. Šia procedūra paaiškinama, kaip atsisiųsti numatytuosius šablonus, juos tinkinti ir atnaujinti sistemos šablonus.

1. Naudodami žiniatinklio naršyklę, į vietinį kompiuterį atsisiųskite [„Microsoft Dynamics 365 Commerce“ peržiūros numatytųjų el. laiškų šablonų ZIP failą](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip). Šiame faile yra tolesni HTML dokumentai.

    - Užsakymo patvirtinimo šablonas
    - Dovanų kortelės išdavimo šablonas
    - Naujo užsakymo šablonas
    - Paketo užsakymo šablonas
    - Paėmimo užsakymo šablonas

1. Tinkinkite šablonus naudodami teksto arba HTML rengyklę. [Palaikomų atpažinimo ženklų](#supported-tokens-in-the-email-template) sąrašą rasite tolesnėje šios temos dalyje.
1. Prisijunkite prie „Retail“.
1. Naudodami kairėje esantį meniu, nueikite į **Moduliai \> Organizacijos administravimas \> Sąranka \> Organizacijos el. laiškų šablonai**.
1. Išskleiskite sąrašą kairėje, kad pamatytumėte visus šablonus.
1. Su kiekvienu norimu tinkinti šablonu atlikite tolesnius veiksmus.

    1. Pasirinkite šabloną sąraše.
    1. Dalyje **El. laiško turinys** iš sąrašo pasirinkite tinkamą kalbos versiją. (Numatytoji kalba yra **en-us**.)
    1. Dalyje **El. laiško turinys** pasirinkite **Redaguoti**. Atsiranda sritis **Nusiųsti el. laiškų šabloną**.
    1. Pasirinkite **Naršyti** ir suraskite HTML failą, kuriame yra tinkintas turinys.
    1. Pasirinkite **Nusiųsti**. Šablonas nusiunčiamas į sistemą ir rodoma peržiūra.
    1. Pasirinkite **Gerai**.
    1. Nebūtina: tinkinkite šablono ypatybę **Tema**.
    1. Pasirinkite **Įrašyti**.

### <a name="supported-tokens-in-the-email-template"></a>Palaikomi el. laiškų šablono atpažinimo ženklai

Generuojant el. laišką šie atpažinimo ženklai pakeičiami faktinėmis reikšmėmis, kurios taikomos klientui ir jo užsakymui.

#### <a name="sales-order"></a>Pardavimo užsakymas

Toliau nurodyti atpažinimo ženklai taikomi bendram pardavimo užsakymui.

| Atpažinimo ženklo pavadinimas | Atpažinimo ženklas |
|-------------------|-------|
| Užsakymo numeris      | %salesid% |
| Kliento pavadinimas   | %customername% |
| Pristatymo adresas  | %deliveryaddress% |
| Sąskaitų siuntimo adresas   | %customeraddress% |
| Užsakymo data        | %shipdate% |
| Pristatymo režimas     | %modeofdelivery% |
| Nuolaida          | %discount% |
| PVM         | %tax% |
| Užsakymo suma       | %total% |

#### <a name="sales-line"></a>Pardavimo eilutė

Tolesni atpažinimo ženklai pakeičiami kiekvieno užsakymo produkto reikšmėmis.

> [!NOTE]
> Atpažinimo ženklą **Produktų sąrašas – pradžia** įdėkite HTML bloko, kuris kartojamas su kiekvienu produktu, pradžioje, o atpažinimo ženklą **Produktų sąrašas – pabaiga** įdėkite bloko pabaigoje.

| Atpažinimo ženklo pavadinimas      | Atpažinimo ženklas |
|------------------------|-------|
| Produktų sąrašas – pradžia   | \<!--%tablebegin.salesline% --\> |
| Produktų sąrašas – pabaiga     | \<!--%tableend.salesline%--\> |
| Produkto pavadinimas           | %lineproductname% |
| Aprašymas            | %lineproductdescription% |
| Kiekis               | %linequantity% |
| Eilutės vieneto kaina        | %lineprice% (tikrinti) |
| Iš viso eilutės elementų        | %linenetamount% |
| eilutės nuolaida          | %linediscount% |
| Siuntimo data              | %lineshipdate% |
| Įsigijimo metodas     | %linedeliverymode% |
| pristatymo adresas       | %linedeliveryaddress% |
| Eilutės pardavimo vienetas | %lineunit% |

## <a name="additional-resources"></a>Papildomi ištekliai

[„Dynamics 365 Commerce“ peržiūros aplinkos apžvalga](cpe-overview.md)

[„Dynamics 365 Commerce“ peržiūros aplinkos parengimas](provisioning-guide.md)

[„Dynamics 365 Commerce“ peržiūros aplinkos konfigūravimas](cpe-post-provisioning.md)

[DUK apie „Dynamics 365 Commerce“ peržiūros aplinką](cpe-faq.md)

[„Microsoft Lifecycle Services“ (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[„Retail Cloud Scale Unit“ (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[„Microsoft Azure“ portalas](https://azure.microsoft.com/features/azure-portal)

[„Dynamics 365 Commerce“ svetainė](https://aka.ms/Dynamics365CommerceWebsite)
