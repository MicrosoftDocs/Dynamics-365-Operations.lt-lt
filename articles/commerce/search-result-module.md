---
title: Ieškokite rezultatų modulio
description: Šioje temoje aprašomi paieškos rezultatų moduliai ir aprašoma, kaip juos įtraukti į saito puslapius „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c3fce73b1827de12bc8d40e1abb43ad000b8aa1c38812221dfae95010513ede1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712410"
---
# <a name="search-results-module"></a>Ieškos rezultatų modulis

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šioje temoje aprašomi paieškos rezultatų moduliai ir aprašoma, kaip juos įtraukti į saito puslapius „Microsoft Dynamics 365 Commerce“.

Paieškos rezultatų modulis grąžina produkto paieškos rezultatus ir taikomų perdirbimo įrankių sąrašą produktams. Paieškos rezultatų moduliai „Dynamics 365 Commerce“ saituose gali būti naudojami siekiant apimti puslapius šiais scenarijais:

- Paieškos rezultatai, kuriuos pradėjo vartotojo paieška
- Paieškos rezultatai, kurie rodo konkretų produktų rinkinį, tokį kaip „Į parduotuvę panašios paieškos“
- Produktų, priklausančių kategorijai, sąrašai

Daugiau informacijos apie kategoriją ir paieškos rezultatų puslapius rasite [Numatytos kategorijos užsklandos puslapis ir paieškos rezultatų puslapio apžvalga](category-search-page-overview.md).

Tolesnis paveikslėlis rodo paieškos rezultatų puslapio pavyzdį kategorijai „Fabrikam“ saite.

![Paieškos rezultatų puslapio pavyzdys „Fabrikam“ svetainėje.](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a>Paieškos rezultatų modulio ypatybės

Tolesnėje lentelėje išvardytos paieškos rezultato modulių ypatybės kartu su jų vertėmis ir aprašais.

| Ypatybė | Reikšmės | aprašymas |
|----------|--------|-------------|
| Prekių skaičius viename puslapyje | Sveikasis skaičius | Prekių skaičius, kuris turi būti rodomas kiekviename puslapyje. |
| Leisti atgal į PDP | **Teisinga** arba **Klaidinga** | Jei ši ypatybė nustatyta į **Teisinga**, kai vartotojas pasirenka produktą paieškos rezultatų puslapyje, atvertas džiūvėsėlio naršymas produkto išsamios informacijos puslapyje (PDP) rodys „Grįžti į rezultatus“ nuorodą. |
| Išplėsti tikslinimo meniu | **Visi**, **1**, **2**, **3** ar **4** | Pagrindinių apdirbėjų skaičius, kuris turi būti išplečiamas užkrovus puslapį. Pavyzdžiui, jei ši ypatybė yra nustatyta į **3**, pirmieji trys apdirbėjai puslapyje bus išplėsti. |
| Slėpti kategorijų hierarchijos rodymą | **Teisinga** arba **Klaidinga** | Jei ši ypatybė yra nustatyta į **Teisinga**, kategorijos hierarchija rodoma puslapyje bus paslėpta. Ši ypatybė turi būti nustatyta į **Teisingą** jei naudojate [džiūvėsėlio modulį](add-breadcrumb.md) tam, kad jis parodytų kategorijos hierarchiją.|
| Į paieškos rezultatus įtraukite produkto atributus | **Teisinga** arba **Klaidinga** | Jei ši ypatybė yra nustatyta į **Teisinga**, atributai bus grąžinami produktams paieškos rezultatuose. Nepaisant to, kad šie atributai gali būti rodomi „Commerce“ saite, būtinas plėtinys.|
| Rodyti priskyrimo kainas | **Teisinga** arba **Klaidinga** | Jei ši ypatybė yra nustatyta į **Teisinga**, prisijungimo kainos produktams bus rodomos paieškos rezultatuose, kai prisijungęs vartotojas naršo puslapyje. |
| Tikslinimo skydo naujinimas | **Teisinga** arba **Klaidinga** | Jei ši ypatybė nustatyta kaip **Teisinga**, tikslinimo skydas bus atnaujintas pasirinkus tikslinimo priemones. Šiuo režimu kai kurios kelių pasirinkimų tikslinimo priemonės elgsis kaip vieno pasirinkimo tikslinimo priemonės, atnaujinus tikslinimo skydą. |

> [!IMPORTANT]
> „Commerce” 10.0.16 versijos leidime ir vėlesniuose konfigūracija **Rodyti priskyrimo kainas** galima naudoti norint rodyti priskyrimo kainas puslapyje.
>
> „Commerce” 10.0.20 versijos leidime ir vėlesniuose konfigūraciją **Naujinti tikslinimo skydą** galima naudoti norint atnaujinti tikslinimo skydą tikslinimo priemonės pasirinkimo metu.

## <a name="supported-modules"></a>Palaikomi moduliai

Paieškos rezultatų modulis palaiko [greito rodinio modulį](quick-view-module.md), kuris leidžia vartotojams peržiūrėti produkto informaciją ir įtraukti prekes į vežimėlį iš paieškos rezultatų puslapio.

## <a name="add-a-search-results-module-to-a-category-page"></a>Įtraukite paieškos rezultatų modulį į kategorijų puslapį

Norėdami įtraukti paieškos rezultatų modulį į kategorijų puslapį, atlikite šiuos žingsnius.

1. Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.
1. Teksto laukelyje **Naujas šablonas** įveskite pavadinimą **Paieškos rezultatai** ir tada rinkitės **Gerai**.
1. Vietoje **tekstas** pasirinkite daugtaškį (...), ir tada rinkitės **Įtraukite modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Numatytasis puslapis**, tada pasirinkite **Gerai**.
1. Vietoje **Pagrindinis** modulyje **Numatytas puslapis** rinkitės daugtaškį (...) ir tada rinkitės **Įtraukite modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.
1. Vietoje **Talpykla** pasirinkite daugtaškį (...), ir tada rinkitės **Įtraukite modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Naršymo kelias**, tada pasirinkite **Gerai**.
1. Ypatybių juostoje **Džiūvėsėlis** įveskite vertę **1** skirtą **Minimaliems atsitikimams**.
1. Vietoje **Talpykla** pasirinkite daugtaškį (...), o tada pasirinkite **Įtraukite modulį**.
1. Teksto laukelyje **Įtraukti modulį** pasirinkite **Paieškos rezultatai** modulį, o tada pasirinkite **Gerai**.
1. Ypatybių juostoje **Paieškos rezultatai** įveskite vertę **1** skirtą **Minimalūs atsitikimai** ir tuomet nustatykite visas kitas reikiamas ypatybes paieškos rezultatų moduliui. Nustatydami šias ypatybes šablone užtikrinate, kad bet kokie tinkinimai konkrečios kategorijos puslapyje automatiškai apims šiuos nustatymus.
1. Pasirinkite **Baigti redagavimą**, o tada pasirinkite **Publikuoti**, kad publikuotumėte šabloną.
1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. Teksto laukelyje **Rinkitės šabloną** pasirinkite **Paieškos rezultatai** sukurtą šabloną, įveskite **Kategorijos puslapis** skirtą **Puslapio pavadinimas** ir tada rinkitės **Gerai**. Kadangi visos vertės yra nustatytos šablone, puslapis yra parengtas publikuoti.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Numatytojo kategorijos nukreipimo puslapio ir ieškos rezultatų puslapio apžvalga](category-search-page-overview.md)

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[Greito rodinio modulis](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
