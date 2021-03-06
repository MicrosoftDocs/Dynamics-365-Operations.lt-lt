---
title: Konfigūruokite pasirinktas savybes „Dynamics 365 Commerce“ vertinimo aplinkoje
description: Šiame skyriuje paaiškinama, kaip sukonfigūruoti pasirenkamas funkcija „Microsoft Dynamics 365 Commerce“ vertinimo aplinkoje.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0a93429e836d818458f11f6f6821fda237edc291
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936985"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a>Pasirinktinių „Dynamics 365 Commerce” vertinimo aplinkos funkcijų konfigūravimas

[!include [banner](includes/banner.md)]

Šiame skyriuje paaiškinama, kaip sukonfigūruoti pasirenkamas funkcija „Microsoft Dynamics 365 Commerce“ vertinimo aplinkoje.

## <a name="prerequisites"></a>Būtinieji komponentai

Jei norite įvertinti operacines el. pašto funkcijas, turi būti įvykdytos šios būtinosios sąlygos:

- Turite prieinamą elektroninio pašto serverį („Simple Mail Transfer Protocol“ \[SMTP\] serverį), kuris gali būti naudojamas „Microsoft Azure“ prenumeratai, kuria aprūpinote savo vertinimo aplinką.
- Turite pasiekiamus serverio visiškai apibrėžtą domeno vardą (FQDN) / IP adresą, SMTP prievado numerį ir autentifikavimo informaciją.

## <a name="configure-the-image-back-end"></a>Vaizdų posistemio konfigūravimas

### <a name="find-your-media-base-url"></a>Pagrindinio medijos URL radimas

> [!NOTE]
> Kad galėtumėte atlikti šią procedūrą, turite atlikti dalyje [Svetainės nustatymas programoje „Commerce“](cpe-post-provisioning.md#set-up-your-site-in-commerce) nurodytus veiksmus.

1. Prisijunkite prie komercijos svetainės kūrėjo naudodami URL, kurį užsirašėte pradėdami „e-Commerce“ parengimo metu (žr. [Pradėti „e-Commerce“](provisioning-guide.md#initialize-e-commerce)).
1. Atidarykite **„Fabrikam“** svetainę.
1. Meniu kairėje pasirinkite **Medijos biblioteka**.
1. Pasirinkite bet kurį vieną vaizdo išteklių.
1. Dešinėje esančiame ypatybių inspektoriuje suraskite ypatybę **Viešasis URL**. Jos reikšmė yra URL. Toliau pateikiamas pavyzdys.

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.

1. Paskutinį URL identifikatorių (pirmiau pateiktame pavyzdyje – **MA1nQC**) pakeiskite eilute **search?fileName=**. Toliau parodyta, kaip atrodo taip pakeistas URL pavyzdys.

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    Šis URL yra jūsų pagrindinis medijos URL. Jį pasižymėkite.

### <a name="update-the-media-base-url"></a>Pagrindinio medijos URL naujinimas

1. Prisijunkite prie komercijos būstinės.
1. Naudodami kairėje esantį meniu, nueikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Kanalo profiliai**.
1. Pasirinkite **Redaguoti**.
1. Dalyje **Profilio ypatybės** ypatybės **Pagrindinis medijos serverio URL** reikšmę pakeiskite savo anksčiau sukurtu pagrindiniu medijos URL.
1. Pasirinkite kanalą pavadinimu **scXXXXXXXXX**.
1. Dalyje **Profilio ypatybės** pasirinkite **Įtraukti**.
1. Kaip įtrauktos ypatybės raktą pasirinkite **Pagrindinis medijos serverio URL**. Kaip ypatybės reikšmę įveskite savo anksčiau sukurtą pagrindinį medijos URL.
1. Pasirinkite **Įrašyti**.

## <a name="configure-and-test-the-email-server"></a>Konfigūruokite ir testuokite elektroninio pašto serverį

> [!NOTE]
> SMTP serveris arba el. pašto paslauga, kuriuos čia įvedate, turi būti pasiekiami „Azure“ prenumeratoje, kurią naudojate aplinkoje.

1. Prisijunkite prie komercijos būstinės.
1. Naudokite meniu kairėje ir eikite į **Moduliai \> Mažmena ir komercija \> Būstinės sąranka \> Parametrai \> Elektroninio pašto parametrai**.
1. Skirtuko **SMTP parametrai** lauke **Siunčiamo pašto serveris** įveskite savo SMTP serverio ar el. pašto tarnybos FQDN arba IP adresą.
1. Lauke **SMTP prievado numeris** įveskite prievado numerį. (Jei nenaudojate saugiųjų jungčių lygmens \[SSL\], numatytasis prievado numeris yra **25**.)
1. Jei reikalingas autentifikavimas, įveskite reikšmes laukuose **Vartotojo vardas** ir **Slaptažodis**.
1. Pasirinkite **Įrašyti**.
1. Pasirinkite **Atnaujinti**.
1. Skirtuko **Bandomasis el. laiškas** lauke **El. pašto teikėjas** pasirinkite **SMTP**.
1. Lauke **Gavėjas** įveskite el. pašto adresą, kuriuo bandomasis el. laiškas turi būti pristatytas.
1. Pasirinkite **Išsiųsti bandomąjį el. laišką**.

## <a name="configure-email-templates"></a>El. laiškų šablonų konfigūravimas

Kiekvieno operacinio įvykio, dėl kurio norite siųsti el. laiškus, el. laiškų šabloną turite atnaujinti galiojančiu siuntėjo el. pašto adresu.

1. Prisijunkite prie komercijos būstinės.
1. Naudokite meniu kairėje ir eikite į **Moduliai \> Mažmena ir komercija \> Būstinės sąranka \> Parametrai \> Organizaciniai elektroninio pašto šablonai**.
1. Pasirinkite **Rodyti sąrašą**.
1. Su kiekvienu sąraše esančiu šablonu atlikite toliau nurodytus veiksmus.

    1. Lauke **Siuntėjo el. paštas** įveskite siuntėjo el. pašto adresą.
    1. Nebūtina: lauke **Siuntėjo vardas** įveskite vardą, kuris turi būti naudojamas kaip siuntėjo vardas.

1. Pasirinkite **Įrašyti**.

## <a name="customize-email-templates"></a>El. laiškų šablonų tinkinimas

Galbūt norėsite el. laiškų šablonus tinkinti, kad juose būtų naudojami skirtingi vaizdai. Arba jums reikėtų atnaujinti nuorodas į šablonus tam, kad jie galėtų patekti į jūsų vertinimo aplinką. Šia procedūra paaiškinama, kaip atsisiųsti numatytuosius šablonus, juos tinkinti ir atnaujinti sistemos šablonus.

1. Tinklo naršyklėje atsisiųskite [„Microsoft Dynamics 365 Commerce“ vertinimo numatytųjų el. pašto šablonų archyvuotą failą](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) į savo vietos kompiuterį. Šiame faile yra tolesni HTML dokumentai.

    - Užsakymo patvirtinimo šablonas
    - Dovanų kortelės išdavimo šablonas
    - Naujo užsakymo šablonas
    - Paketo užsakymo šablonas
    - Paėmimo užsakymo šablonas

1. Tinkinkite šablonus naudodami teksto arba HTML rengyklę. [Palaikomų atpažinimo ženklų](#supported-tokens-in-the-email-template) sąrašą rasite tolesnėje šios temos dalyje.
1. Prisijunkite prie „Commerce“.
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
| Užsakymo numeris      | „%salesid%“ |
| Kliento pavadinimas   | „%customername%“ |
| Pristatymo adresas  | „%deliveryaddress%“ |
| Sąskaitų siuntimo adresas   | „%customeraddress%“ |
| Užsakymo data        | „%shipdate%“ |
| Pristatymo režimas     | „%modeofdelivery%“ |
| Nuolaida          | „%discount%“ |
| PVM         | „%tax%“ |
| Užsakymo suma       | „%total%“ |

#### <a name="sales-line"></a>Pardavimo eilutė

Tolesni atpažinimo ženklai pakeičiami kiekvieno užsakymo produkto reikšmėmis.

> [!NOTE]
> Atpažinimo ženklą **Produktų sąrašas – pradžia** įdėkite HTML bloko, kuris kartojamas su kiekvienu produktu, pradžioje, o atpažinimo ženklą **Produktų sąrašas – pabaiga** įdėkite bloko pabaigoje.

| Atpažinimo ženklo pavadinimas      | Atpažinimo ženklas |
|------------------------|-------|
| Produktų sąrašas – pradžia   | \<!--%tablebegin.salesline% --\> |
| Produktų sąrašas – pabaiga     | \<!--%tableend.salesline%--\> |
| Produkto pavadinimas           | „%lineproductname%“ |
| aprašymas            | „%lineproductdescription%“ |
| Kiekis               | „%linequantity%“ |
| Eilutės vieneto kaina        | %lineprice% (patikrinti) |
| Iš viso eilutės elementų        | „%linenetamount%“ |
| eilutės nuolaida          | „%linediscount%“ |
| Siuntimo data              | „%lineshipdate%“ |
| Įsigijimo metodas     | „%linedeliverymode%“ |
| pristatymo adresas       | „%linedeliveryaddress%“ |
| Eilutės pardavimo vienetas | „%lineunit%“ |

## <a name="additional-resources"></a>Papildomi ištekliai

[„Dynamics 365 Commerce“ vertinimo aplinkos peržiūra](cpe-overview.md)

[Parenkite „Dynamics 365 Commerce“ vertinimo aplinką](provisioning-guide.md)

[Sukonfigūruokite „Dynamics 365 Commerce“ vertinimo aplinką](cpe-post-provisioning.md)

[Sukonfigūruokite „BOPIS“ „Dynamics 365 Commerce“ vertinamoje aplinkoje](cpe-bopis.md)

[„Dynamics 365 Commerce“ vertinimo aplinkos DUK](cpe-faq.md)

[„Microsoft Lifecycle Services“ (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[„Retail Cloud Scale Unit“ (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[„Microsoft Azure“ portalas](https://azure.microsoft.com/features/azure-portal)

[„Dynamics 365 Commerce“ svetainė](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]