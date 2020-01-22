---
title: „Commerce” peržiūros aplinkos konfigūravimas
description: Šioje temoje paaiškinama, kaip sukonfigūruoti parengtą „Microsoft Dynamics 365 Commerce“ peržiūros aplinką.
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
ms.openlocfilehash: f19d03f3f2f5a9f6f7ba08b682277e4e3b764d10
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906144"
---
# <a name="configure-a-commerce-preview-environment"></a>„Commerce” peržiūros aplinkos konfigūravimas

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip sukonfigūruoti parengtą „Microsoft Dynamics 365 Commerce“ peržiūros aplinką.

## <a name="overview"></a>Peržiūrėti

Šios temos procedūras atlikite tik tada, kai „Commerce“ peržiūros aplinka yra parengta. Informacijos apie tai, kaip parengti „Commerce“ peržiūros aplinką, rasite temoje [„Commerce“ peržiūros aplinkos parengimas](provisioning-guide.md).

Kai „Commerce“ peržiūros aplinka visapusiškai parengta, pradėti ją vertinti galėsite tik atlikę papildomus po parengimo atliekamus konfigūravimo veiksmus. Norėdami atlikti šiuos veiksmus, turite naudoti „Microsoft Dynamics Lifecycle Services“ (LCS), „Dynamics 365 Commerce“ ir „Dynamics 365 Retail“.

## <a name="before-you-start"></a>Prieš pradedant

1. Prisijunkite prie [LCS portalo](https://lcs.dynamics.com).
1. Nueikite į savo projektą.
1. Viršutiniame meniu pasirinkite **Aplinkos diegimo debesyje įrankis**.
1. Sąraše pasirinkite savo aplinką.
1. Dešinėje esančioje informacijos apie aplinką srityje pasirinkite **Visa informacija**.
1. Pasirinkite **Prisijungimas**, kad atidarytumėte meniu, tada – **Įeiti į aplinką**.
1. Įsitikinkite, kad viršutiniame dešiniajame kampe pasirinktas juridinis subjektas **USRT**.

## <a name="configure-the-point-of-sale-in-lcs"></a>Elektroninio kasos aparato konfigūravimas portale LCS

### <a name="associate-a-worker-with-your-identity"></a>Darbuotojo susiejimas su jūsų tapatybe

Norėdami susieti darbuotoją su jūsų tapatybe portale LCS, atlikite tolesnius veiksmus.

1. Naudodami kairėje esantį meniu, nueikite į **Moduliai \> „Retail“ \> Darbuotojai \> Darbuotojai**.
1. Sąraše raskite ir pasirinkite šį įrašą **000713 - Andrew Collette**.
1. Veiksmų srityje pasirinkite **„Retail“**.
1. Pasirinkite **Susieti esamą tapatybę**.
1. Lauko **Ieškoti naudojant el. paštą** dešinėje esančiame lauke **El. paštas** įveskite savo el. pašto adresą.
1. Pasirinkite **Ieškoti**.
1. Pasirinkite įrašą su savo vardu.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Įrašyti**.

### <a name="activate-cloud-pos"></a>Aktyvinti debesies EKA

Norėdami portale LCS aktyvinti debesies EKA, atlikite tolesnius veiksmus.

1. Viršutiniame meniu pasirinkite **Aplinkos diegimo debesyje įrankis**.
1. Sąraše pasirinkite savo aplinką.
1. Dešinėje esančioje informacijos apie aplinką srityje pasirinkite **Visa informacija**.
1. Pasirinkite **Prisijungti**, kad atidarytumėte meniu, tada – **Įeiti į debesies elektroninį kasos aparatą**, kad atidarytumėte elektroninį kasos aparatą (EKA).
1. Pasirinkite **Toliau**.
1. Prisijunkite naudodami savo „Microsoft Azure Active Directory“ („Azure AD“) paskyrą.
1. Dalyje **Parduotuvės pavadinimas**pasirinkite **San Fransiskas**.
1. Pasirinkite **Toliau**.
1. Dalyje **Registras ir įrenginys**pasirinkite **SANFRAN-1**.
1. Pasirinkite **Aktyvinti**. Esate atjungiami ir nukreipiami į EKA prisijungimo puslapį.
1. Dabar galite prisijungti prie debesies EKA funkcijų naudodami operatoriaus ID **000713** ir slaptažodį **123**.

## <a name="set-up-your-site-in-commerce"></a>Svetainės nustatymas programoje „Commerce“

Norėdami pradėti nustatyti peržiūros svetainę programoje „Commerce“, atlikite tolesnius veiksmus.

1. Prisijunkite prie svetainių valdymo įrankio naudodami URL, kurį pasižymėjote inicijuodami el. prekybą jos konfigūravimo metu (žr. [El. prekybos inicijavimas](provisioning-guide.md#initialize-e-commerce)).
1. Pasirinkite svetainę **„Fabrikam“**, kad atidarytumėte svetainės sąrankos dialogo langą.
1. Pasirinkite domeną, kurį įvedėte inicijuodami el. prekybą.
1. Kaip numatytąjį kanalą pasirinkite **„Fabrikam“ išplėstinė internetinė parduotuvė**. (Įsitikinkite, kad pasirinkote **išplėstinę** internetinę parduotuvę.)
1. Kaip numatytąją kalbą pasirinkite **lt-lt**.
1. Lauko **Kelias** reikšmę palikite tokią, kokia yra.
1. Pasirinkite **Gerai**. Atsiranda svetainės puslapių sąrašas.

## <a name="enable-jobs-in-retail"></a>Užduočių įjungimas programoje „Retail“

Norėdami programoje „Retail“ įjungti užduotis, atlikite toliau nurodytus veiksmus.

1. Prisijunkite prie aplinkos (būstinėje).
1. Naudodami kairėje esantį meniu, nueikite į **„Retail“ \> Užklausos ir ataskaitos \> Paketines užduotys**.

    Likusius šios procedūros veiksmus reikia atlikti su kiekviena iš tolesnių užduočių.

    * Apdoroti mažmeninės prekybos el. paštu siunčiamą pranešimą
    * Produkto prieinamumas
    * P-0001
    * Užsakymų sinchronizavimo užduotis

1. Naudodami spartųjį filtrą, užduoties galite ieškoti pagal pavadinimą.
1. Jei užduoties būsena yra **Sulaikyta**, atlikite tolesnius veiksmus.

    1. Pasirinkite įrašą.
    1. Veiksmų srities skirtuke **Paketinė užduotis** pasirinkite **Keisti būseną**.
    1. Pasirinkite **Laukiama**, tada – **Gerai**.

### <a name="run-full-data-synchronization-in-retail"></a>Visų duomenų sinchronizavimas programoje „Retail“

Norėdami sinchronizuoti visus duomenis programoje „Retail“, atlikite toliau nurodytus veiksmus.

1. Naudodami kairėje esantį meniu, nueikite į **Moduliai \> „Retail“ \> Būstinės sąranka \> Duomenų apsikeitimo valdymas \> Kanalo duomenų bazė**.
1. Kairėje esančiame sąraše pasirenkamas kanalas **Numatytasis**. Pasirinkite kitą galimą kanalą. Šio kanalas pavadinimas – **scXXXXXXXXX**.
1. Veiksmų srityje pasirinkite **Visas duomenų sinchronizavimas**.
1. Įveskite **9999** kaip paskirstymo grafiką.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Gerai**.

### <a name="test-credit-card-information-to-do-test-purchases"></a>Bandomosios kredito kortelės informacija bandomiesiems pirkimams atlikti

Norėdami svetainėje atlikti bandomąsias operacijas, galite naudoti tolesnę bandomosios kredito kortelės informaciją.

- **Kortelės numeris:** 4111-1111-1111-1111
- **Galiojimo pabaigos data:** 10/20
- **Kortelės tikrinimo vertės (CVV) kodas:** 737

> [!IMPORTANT]
> Bandomojoje svetainėje niekada esant jokioms aplinkybėms nenaudokite faktinės kredito kortelės informacijos.

## <a name="next-steps"></a>Kiti veiksmai

Kai parengimo ir konfigūravimo veiksmai baigti, esate pasirengę vertinti peržiūros aplinką. Naudodami „Commerce“ svetainių valdymo įrankio URL, galite pradėti naudoti kūrimo funkcijas. Naudodami „Commerce“ svetainės URL, galite pradėti naudoti mažmeninės prekybos klientų svetainės funkcijas.

Norėdami konfigūruoti pasirenkamas „Commerce“ peržiūros aplinkos funkcijas, žr. [Pasirenkamų „Commerce“ peržiūros aplinkos funkcijų konfigūravimas](cpe-optional-features.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[„Commerce” peržiūros aplinkos apžvalga](cpe-overview.md)

[„Commerce” peržiūros aplinkos parengimas](provisioning-guide.md)

[Pasirenkamų „Commerce” peržiūros aplinkos funkcijų konfigūravimas](cpe-optional-features.md)

[DUK apie „Commerce” peržiūros aplinką](cpe-faq.md)

[„Microsoft Lifecycle Services“ (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[„Retail Cloud Scale Unit“ (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[„Microsoft Azure“ portalas](https://azure.microsoft.com/features/azure-portal)

[„Dynamics 365 Commerce“ svetainė](https://aka.ms/Dynamics365CommerceWebsite)

[„Dynamics 365 Retail“ žinyno ištekliai](../retail/index.md)
