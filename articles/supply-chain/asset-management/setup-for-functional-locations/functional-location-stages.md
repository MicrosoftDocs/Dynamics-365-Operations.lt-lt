---
title: Funkcinės vietos ciklo būsenos
description: Šioje temoje aprašoma, kaip nustatyti funkcinės vietos būsenas ir ciklo modelius modulyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 11f784e4c17ad5b764cadd914f4959f4be160913
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783455"
---
# <a name="functional-location-lifecycle-states"></a>Funkcinės vietos ciklo būsenos

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Šioje temoje aprašoma, kaip nustatyti funkcinės vietos ciklo būsenas ir ciklo modelius modulyje Turto valdymas. Funkcinės vietos ciklo būsenos reiškia galimas funkcinės vietos būsenas, pavyzdžiui, sukurta, aktyvioji ir pasibaigusi. Visas funkcines vietas, neatsižvelgiant į jų ciklo būseną, galite peržiūrėti sąrašo puslapyje **All functional locations**. Galite pakeisti funkcinės vietos būseną, pasirinkdami ją sąrašo puslapyje **Visos funkcinės vietos** ir pasirinkdami **Naujinti funkcinės vietos būseną**.

## <a name="set-up-functional-location-lifecycle-states"></a>Funkcinės vietos ciklo būsenų konfigūracija

1. Pasirinkite **Turto valdymas** > **Konfigūracija** > **Funkcinės vietos** > **Ciklo būsenos**.
2. Pasirinkite **New**, kad sukurtumėte naują funkcinės vietos būseną.
3. Lauke **Ciklo būsena** įterpkite būsenos ID, o lauke **Pavadinimas** įterpkite funkcinės vietos būsenos pavadinimą. Lauke **Ciklo modeliai** matote funkcinės vietos ciklo modelių, kuriuose naudojama funkcinės vietos būsena, skaičių.
4. FastTab **Bendra** perjungiklyje **Aktyvioji** pasirinkite „Taip“, jei funkcinė vieta turi būti aktyvi esant šiai būsenai.
5. Perjungiklyje **Kurti turtą** pasirinkite „Taip“, kad būtų galima automatiškai sukurti turtą, kurio pavadinimas sutaptų su funkcinės vietos pavadinimu, ir įdiegti jį funkcinėje vietoje esant šiai būsenai.  
>[!NOTE]
>Šis perjungiklis yra susijęs su lauku **Asset type**, esančiu **General** FastTab **Functional location types** formoje (**Asset management** > **Setup** > **Functional locations** > **Functional location types**).
6. Perjungiklyje **Pervardyti vietą** pasirinkite „Taip“, kad būtų galima pakeisti funkcinės vietos pavadinimą esant šiai būsenai.
7. Perjungiklyje **Naujos antrinės vietos** pasirinkite „Taip“, kad būtų galima įtraukti naujas funkcinės vietos antrines vietas esant šiai būsenai.
8. Perjungiklyje **Diegti turtą** pasirinkite „Taip“, kad esant šiai būsenai funkcinėje vietoje būtų galima diegti turtą.
9. Perjungiklyje **Naikinti funkcinę vietą** pasirinkite „Taip“, kad esant šiai būsenai būtų galima panaikinti funkcinę vietą.
10. Lauke **Ciklo būsena** pasirinkite turto būseną, jei norite, kad viso funkcinėje vietoje įdiegto turto ciklo būsena būtų automatiškai atnaujinama esant šiai būsenai. Pavyzdžiui: Pavyzdys: uždarius funkcinę vietą ir nustačius funkcinės vietos ciklo būseną „Pasibaigusi“, rekomenduojama automatiškai pakeisti toje funkcinėje vietoje įdiegto turto ciklo būseną į „Nenaudojamas“.


>[!NOTE]
>Funkcinės vietos ciklo būsenos, ciklo modeliai ir tipai yra susiję ir naudojami taip pat, kaip ir darbo užsakymo ciklo būsenos, darbo užsakymo ciklo modeliai ir darbo užsakymų tipai. 

## <a name="set-up-functional-location-lifecycle-models"></a>Funkcinės vietos ciklo modelių konfigūracija

Sukūrus funkcinių vietų būtinas ciklo būsenas, jas galima suskirstyti į grupes. Tai atliekama siekiant sukurti ciklo modelio srautą, kuris gali būti naudojamas skirtingų tipų funkcinėse vietose. Turėtų būti sukurtas bent vienas standartinis funkcinės vietos ciklo modelis.

1. Pasirinkite **Turto valdymas** > **Konfigūracija** > **Funkcinės vietos** > **Ciklo modeliai**.
2. Pasirinkite **New**, kad sukurtumėte naują ciklo modelį.
3. Lauke **Ciklo modelis** įterpkite ciklo modelio ID, o lauke **Pavadinimas** įterpkite ciklo modelio pavadinimą. Laukuose **Funkcinių vietų tipai** ir **Ciklo būsenos** matote funkcinių vietų tipų, naudojančių ciklo modelį, skaičių ir būsenų, pasirinktų ciklo modelyje, skaičių.
4. FastTab **Ciklo būsenos** pasirinkite būsenas, kurias reikėtų įtraukti į modelį. Tuo tikslu sekcijoje **Likusios ciklo būsenos** spustelėkite būseną ir spustelėkite mygtuką ![rodyklė pirmyn](media/02-setup-for-functional-locations.png).
5. Jei norite pasirinkti visas galimas modelio būsenas, spustelėkite mygtuką ![pasirinkti visus galimus etapus](media/03-setup-for-functional-locations.png). Visos būsenos perkeliamos į sekciją **Lifecycle states selected**.
6. Jei norite iš modelio pašalinti pasirinktą būseną, pasirinkite būseną sekcijoje **Lifecycle states selected**, tada spustelėkite mygtuką ![rodyklė atgal](media/04-setup-for-functional-locations.png).
7. Pasirinkę **Lifecycle state updates**, nustatysite, kurios ciklo būsenos gali būti susijusios su pasirinkta būsena.