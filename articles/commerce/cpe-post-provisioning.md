---
title: Sukonfigūruokite „Dynamics 365 Commerce“ vertinimo aplinką
description: Šiame skyriuje paaiškinama, kaip sukonfigūruoti pirkimą internetu, pasiėmimą parduotuvėje „Microsoft Dynamics 365 Commerce“ vertinimo aplinką, po to kai ji buvo parengta.
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fa92a581a96de6bed26b4a0c6601ebd9d5088347
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993430"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a>Sukonfigūruokite „Dynamics 365 Commerce“ vertinimo aplinką

[!include [banner](includes/banner.md)]

Šiame skyriuje paaiškinama, kaip sukonfigūruoti pirkimą internetu, pasiėmimą parduotuvėje „Microsoft Dynamics 365 Commerce“ vertinimo aplinką, po to kai ji buvo parengta.

## <a name="overview"></a>Peržiūra

Pabaikite šio skyriaus procedūras po to, kai jūsų Komercijos vertinimo aplinka buvo parengta ir sukonfigūruota. Dėl informacijo, kaip nustatyti savo Komercijos vertinimo aplinką po jos nustatymo, žr. [Komercijos vertinimo aplinkos nustatymas](provisioning-guide.md).

Po to kai jūsų Komercijos vertinimo aplinka buvo parengta iki galo, papildomas jos parengimo konfigūravimo žingsniai turi būti pateikti iki tol, kol pradėsite vertinti aplinką. Norėdami atlikti šiuos veiksmus, turite naudoti „Microsoft Dynamics Lifecycle Services“ (LCS) ir „Dynamics 365 Commerce“.

## <a name="before-you-start"></a>Prieš pradedant

1. Prisijunkite prie [LCS portalo](https://lcs.dynamics.com).
1. Nueikite į savo projektą.
1. Viršutiniame meniu pasirinkite **Aplinkos diegimo debesyje įrankis**.
1. Sąraše pasirinkite savo aplinką.
1. Aplinkos informacijoje dešinėje, pasirinkite **Prisijungti prie aplinkos**. Būsite nukreipti į komercijos būstinę.
1. Įsitikinkite, kad viršutiniame dešiniajame kampe pasirinktas juridinis subjektas **USRT**.

Po parengimo veiksmų komercijos būstinėje, įsitikinkite, kad **USRT** juridinis asmuo yra visuomet pasirinktas.

## <a name="configure-the-point-of-sale"></a>Sukonfigūruokite prekybos tašką

### <a name="associate-a-worker-with-your-identity"></a>Darbuotojo susiejimas su jūsų tapatybe

Tam, kad susietumėte darbuotoją su savo tapatybe, atlikite šiuos veiksmus Komercijos būstinėje.

1. Naudodami kairėje esantį meniu, nueikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Darbuotojai \> Darbininkai**.
1. Sąraše raskite ir pasirinkite šį įrašą **000713 - Andrew Collette**.
1. Veiksmų juostoje pasirinkite **Komercija**.
1. Pasirinkite **Susieti esamą tapatybę**.
1. Lauko **Ieškoti naudojant el. paštą** dešinėje esančiame lauke **El. paštas** įveskite savo el. pašto adresą.
1. Pasirinkite **Ieškoti**.
1. Pasirinkite įrašą su savo vardu.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Įrašyti**.

### <a name="activate-cloud-pos"></a>Aktyvinti debesies EKA

„Cloud POS“ įjungimui, atlikite šiuos veiksmus LCS.

1. Viršutiniame meniu pasirinkite **Aplinkos diegimo debesyje įrankis**.
1. Sąraše pasirinkite savo aplinką.
1. Aplinkos informacijoje dešinėje, pasirinkite **Prisijungti prie debesies prekybos taško**.
1. Pasirinkite **Kitas** tam, kad atvertumėte **Prieš pradžią** teksto laukelį.
1. Palikite **Serverio URL** laukelį tokį, koks yra. Pasirinkite **Toliau**.
1. Prisijunkite naudodami savo „Microsoft Azure Active Directory“ („Azure AD“) paskyrą.
1. **Parduotuvės pavadinimo** laukelyje pasirinkite **San Franciskas** ir tuomet pasirinkite **Kitas**.
1. Dalyje **Registras ir įrenginys** pasirinkite **SANFRAN-1**.
1. Pasirinkite **Aktyvinti**. Esate atjungiami ir nukreipiami į EKA prisijungimo puslapį.
1. Dabar galite prisijungti prie debesies EKA funkcijų naudodami operatoriaus ID **000713** ir slaptažodį **123**.

## <a name="set-up-your-site-in-commerce"></a>Svetainės nustatymas programoje „Commerce“

Jūsų vertinimo vietos komercijoje nustatymo pradžiai, atlikite šiuos žingsnius.

1. Prisijunkite prie vietos kūrėjo naudodami URL, kurį užsirašėte pradėdami „e-Commerce“ parengimo metu (žr. [Pradėti „e-Commerce“](provisioning-guide.md#initialize-e-commerce)).
1. Pasirinkite svetainę **„Fabrikam“**, kad atidarytumėte svetainės sąrankos dialogo langą.
1. Pasirinkite domeną, kurį įvedėte inicijuodami el. prekybą.
1. Kaip numatytąjį kanalą pasirinkite **„Fabrikam“ išplėstinė internetinė parduotuvė**. (Įsitikinkite, kad pasirinkote **išplėstinę** internetinę parduotuvę.)
1. Kaip numatytąją kalbą pasirinkite **lt-lt**.
1. Lauko **Kelias** reikšmę palikite tokią, kokia yra.
1. Pasirinkite **Gerai**. Atsiranda svetainės puslapių sąrašas.

## <a name="enable-jobs"></a>Užduočių įgalinimas

Norėdami programoje „Commerce“ įjungti užduotis, atlikite toliau nurodytus veiksmus.

1. Prisijunkite prie aplinkos (būstinėje).
1. Naudodami kairėje esantį meniu, nueikite į **Mažmeninė prekyba ir prekyba \> Užklausos ir ataskaitos \> Paketines užduotys**.

    Likusius šios procedūros veiksmus reikia atlikti su kiekviena iš tolesnių užduočių.

    * Apdoroti mažmeninės prekybos el. paštu siunčiamą pranešimą
    * Produkto prieinamumas
    * P-0001
    * Užsakymų sinchronizavimo užduotis

1. Naudodami spartųjį filtrą, užduoties galite ieškoti pagal pavadinimą.
1. Jei darbo būsena yra **Vykdoma**, atlikite šiuos žingsnius:

    1. Pasirinkite įrašą.
    1. Veiksmų srities skirtuke **Paketinė užduotis** pasirinkite **Keisti būseną**.
    1. Pasirinkite **Atšaukti**, tuomet pasirinkite **OK**.

Pasirinktinai, taip pat galite nustatyti sutapimo intervalą ties (1) minute šiems veiksmams:

* Mažmenos užsakymo elektroninio pašto pranešimo darbo apdorojimas
* P-0001 darbas
* Užsakymų sinchronizavimo užduotis

### <a name="run-full-data-synchronization"></a>Vykdyti visą duomenų sinchronizavimą

Visų duomenų sinchronizavimo komercijoje vykdymui, atlikite šiuos veiksmus komercijos būstinėje.

1. Naudodami kairėje esantį meniu, nueikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Prekybos tvarkaraštis \> Kanalo duomenų bazė**.
1. Pasirinkite kanalą pavadinimu **scXXXXXXXXX**.
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

Po parengimo ir konfigūravimo žingsnių atlikimo, galite pradėti naudoti savo vertinimo aplinką. Naudokite komercijos vietos kūrėjo URL tam, kad eitumėte į autorizavimo patirtį. Naudokite komercijos vietos kūrėjo URL tam, kad eitumėte į mažmenos kliento vietos patirtį.

Tam, kad sukonfigūruotumėte pasirenkamas jūsų Komercijos vertinimo aplinkos savybes, žr. [Konfigūruoti pasirenkamas savybes savo Komercijos vertinimo aplinkoje](cpe-optional-features.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[„Dynamics 365 Commerce“ vertinimo aplinkos peržiūra](cpe-overview.md)

[Parenkite „Dynamics 365 Commerce“ vertinimo aplinką](provisioning-guide.md)

[Konfigūruokite pasirinktas savybes „Dynamics 365 Commerce“ vertinamoje aplinkoje](cpe-optional-features.md)

[Sukonfigūruokite „BOPIS“ „Dynamics 365 Commerce“ vertinamoje aplinkoje](cpe-bopis.md)

[„Dynamics 365 Commerce“ vertinimo aplinkos DUK](cpe-faq.md)

[„Microsoft Lifecycle Services“ (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[„Retail Cloud Scale Unit“ (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[„Microsoft Azure“ portalas](https://azure.microsoft.com/features/azure-portal)

[„Dynamics 365 Commerce“ svetainė](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]