---
title: Priežiūros darbuotojai ir darbuotojų grupės
description: Šioje temoje aprašomi priežiūros darbuotojai ir darbuotojų grupės modulyje „Turto valdymas“.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
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
ms.openlocfilehash: c85fc24cdf0b3cd1a188ccf0f477ffbfa5fab960
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783450"
---
# <a name="maintenance-workers-and-worker-groups"></a>Priežiūros darbuotojai ir darbuotojų grupės

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Šioje temoje aprašomi priežiūros darbuotojai ir darbuotojų grupės modulyje „Turto valdymas“. Modulyje „Turto valdymas“ galite priskirti priežiūros darbuotojus prie funkcinių vietovių. (Norėdami gauti daugiau informacijos apie funkcines vietas, žr. [Create functional locations](../functional-locations/create-functional-locations.md).) Ši funkcija gali būti naudinga, jei, pavyzdžiui, planuojate mašinos, kurios funkcinė vietovė yra 01, priežiūros užduotį ir norite priskirti priežiūros darbuotojus iš tos pačios vietovės užduočiai atlikti.

Taip pat galite kurti priežiūros darbuotojų grupes ir su jais susieti priežiūros darbuotojus. Ši funkcija naudinga, kai atliekate paprastą darbo užsakymo planavimą ir norite darbo užsakyme suplanuoti priežiūros darbuotojų grupę. Galite naudoti priežiūros darbuotojus ir priežiūrą atliekančių darbuotojų grupes, kad nustatytumėte pageidautinus priežiūros darbuotojus ir už priežiūrą atsakingus darbuotojus. 


## <a name="create-workers"></a>Kurti darbininkus

1. Pasirinkit **Asset management** \> **Setup** \> **Workers** \> **Workers**.
2. Spustelėkite **New**, norėdami į sąrašą įtraukti naują darbuotoją.
3. Lauke **Worker** pasirinkite darbuotoją.
4. Nustatykite parinktį **Aktyvus** į **Taip**, kad darbo užsakymams suplanuotumėte darbuotoją.

    „FastTab“  skirtuke **Bendra** laukai **Išteklius** ir **Aprašas** automatiškai užpildomi, jei darbuotojui buvo parinktas išteklius. Laukas **Kalendorius** taip pat užpildomas automatiškai, jei darbuotoją nustatėte kaip išteklių ir tam ištekliui puslapyje **Ištekliai** priskyrėte kalendorių (**Organizacijos administravimas**\>**Ištekliai**\>**Ištekliai**).

5. „FastTab“ skirtuke **Grupės** pasirinkite **Pridėti**, tada darbuotojui parinkite priežiūros darbuotojų grupę. Pardavimo grupėje gali būti daugiau nei vienas darbuotojas.
6. Naudojant standartinę konfigūraciją, darbuotojo narystė grupėje įsigalios ir niekada nebaigs galioti nuo tos dienos, kai pridėsite grupę. Ši data rodoma lauke **Effective**. Norėdami matyti lauką **Effective**, pasirinkite **View**\>**All**. Jei darbuotojo narystė grupėje turėtų būti apribota tam tikram laikotarpiui, norėdami nustatyti periodą, naudokite laukus **Galiojantis** ir **Galiojimo pabaiga**.
7. „FastTab“ skirtuke **Funkcinės vietovės** pasirinkite **Pridėti**ir pasirinkite priežiūros darbuotojo funkcinę grupę. Taip pat nurodykite, kuri vietovė yra pirminė darbuotojo funkcinė vietovė.

    > [!NOTE]
    > Kai darbuotojui pridedate funkcinę vietovę, visas aktyvus turtas, kuris yra susijęs su tomis funkcinėmis vietovėmis, rodomas įvairiuose meniu elementuose, tokiuose kaip **Mano aktyvus turtas** ir **Mano aktyvios funkcinės vietovės**. Jie taip pat rodomi turto peržvalgose, atsirandančiose kuriant naują turtą, priežiūros užklausą arba darbo užsakymą.

    „FastTab“ skirtuko **Informacija** laukuose rodomas priežiūros darbuotojų grupių ir funkcinių vietovių, su kuriomis susijęs pasirinktas priežiūros darbuotojas, skaičius.

## <a name="create-worker-groups"></a>Darbuotojų grupių kūrimas

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Darbuotojai** \> **Priežiūros darbuotojų grupės**.
2. Spustelėkit **New**, norėdami į sąrašą įtraukti naują darbuotoją.
3. Lauke **Priežiūros darbuotojų grupė** įveskite grupės ID.
4. Tada lauke **Pavadinimas** įveskite pavadinimą.
5. „FastTab“ skirtuke **Darbuotojai** pasirinkite **Pridėti**ir darbuotojų grupei pasirinkite priežiūros darbuotoją. Norėdami sužinoti apie laukus **Galiojantis** ir **Galiojimo pabaiga**, žiūrėkite ankstesnės procedūros 6 veiksmą.
6. Jei išteklių grupė turėtų būti susieta su pasirinkta priežiūros darbuotojų grupe, pasirinkite **Kopijuoti iš išteklių grupės**. Lauke **Grupė** pasirinkite išteklių grupę, iš kurios kopijuosite kalendoriaus parametrus. Po to, lauke **Darbuotojų grupė** pasirinkite darbuotojų grupę, kad į ją nukopijuotumėte išteklių grupės kalendoriaus parametrus. Šis veiksmas svarbus tik tada, kai norite, kad planuojant darbo užsakymą, priežiūros darbuotojai galėtų naudoti su ištekliumi (darbo centru) susijusį kalendorių.

    „FastTab“ skirtuko **Informacija** lauke nurodomas priežiūros darbuotojų, kurie buvo pridėti į pasirinktą darbuotojų grupę, skaičius.
