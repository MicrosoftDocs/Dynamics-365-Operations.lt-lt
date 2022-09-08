---
title: Ieškos rezultatų modulis
description: Šiame straipsnyje aprašomi ieškos rezultatų moduliai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: eeb7cd0769fcb866a3d7dcc03e8e87daf24b2c5d
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405299"
---
# <a name="search-results-module"></a>Ieškos rezultatų modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomi ieškos rezultatų moduliai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.

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

Norėdami įtraukti ieškos rezultatų modulį į svetainės generatoriaus kategorijos puslapį, atlikite šiuos veiksmus.

1. Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.
1. Teksto laukelyje **Naujas šablonas** įveskite pavadinimą **Paieškos rezultatai** ir tada rinkitės **Gerai**.
1. Teksto atminties **atminties** atminties lape pasirinkite daugtaškį (...), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite modulį **Numatytasis** puslapis, tada pasirinkite **Gerai**.
1. Modulyje **Numatytasis** puslapis esantis **pagrindiniame atminties** atminties lape pasirinkite daugtaškį (...), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite konteinerio **modulį**, tada pasirinkite **Gerai**.
1. Konteinerio **laiko** atminties atminties dalyje pasirinkite daugtaškį (...), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti** modulius pasirinkite modulį **Naršymo nuoroda ir** pasirinkite **Gerai**.
1. Ypatybių juostoje **Džiūvėsėlis** įveskite vertę **1** skirtą **Minimaliems atsitikimams**.
1. Konteinerio **laiko** atminties atminties dalyje pasirinkite daugtaškį (...), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti** modulius pasirinkite ieškos **rezultatų modulį**, tada pasirinkite **Gerai**.
1. Ypatybių juostoje **Paieškos rezultatai** įveskite vertę **1** skirtą **Minimalūs atsitikimai** ir tuomet nustatykite visas kitas reikiamas ypatybes paieškos rezultatų moduliui. Nustatydami šias ypatybes šablone užtikrinate, kad bet kokie tinkinimai konkrečios kategorijos puslapyje automatiškai apims šiuos nustatymus.
1. Pasirinkite **Baigti redagavimą**, o tada pasirinkite **Publikuoti**, kad publikuotumėte šabloną.
1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. Dialogo lange **Kurti naują puslapį**, po Puslapio **pavadinimas** įveskite Kategorijos **puslapį** ir pasirinkite **Pirmyn**.
1. Dalyje **Pasirinkti šabloną** pasirinkite **Ieškos rezultatų šabloną**, kurį sukūrėte, tada pasirinkite **Pirmyn**.
1. Dalyje **Pasirinkti maketą** pasirinkite puslapio maketą (pvz., Lankstusis **maketas**) ir pasirinkite **Pirmyn**.
1. Dalyje **Peržiūrėti ir baigti** peržiūrėkite puslapio konfigūraciją. Jei reikia redaguoti puslapio informaciją, pasirinkite **Atgal**. Jei puslapio informacija teisinga, pasirinkite Kurti **puslapį**.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="inventory-aware-search-results-module"></a>Atsargų žinomos ieškos rezultatų modulis

Ieškos rezultatų modulis gali būti sukonfigūruotas įtraukti atsargų duomenis ir suteikti tokią patirtį:

- Kartu su produktais rodyti atsargų lygio etiketes.
- Slėpti ne atsargose produktus iš produktų sąrašo.
- Rodyti ne atsargose produktus produktų sąrašo pabaigoje.
- Palaiko atsargų produktų filtravimą.

Norėdami įgalinti šią patirtį, pirmiausia **turite įgalinti patobulinto el. komercijos** produktų aptikimo funkciją, kad ji būtų žinoma apie atsargas, o tada sukonfigūruoti keletą būtinųjų parametrų "Commerce Headquarters". Daugiau informacijos ieškokite atsargų [produktų sąraše](inventory-aware-product-listing.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Numatytojo kategorijos nukreipimo puslapio ir ieškos rezultatų puslapio apžvalga](category-search-page-overview.md)

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[Greito rodinio modulis](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
