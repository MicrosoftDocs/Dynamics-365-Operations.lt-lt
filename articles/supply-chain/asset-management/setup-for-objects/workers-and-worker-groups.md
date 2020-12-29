---
title: Priežiūros darbuotojai ir darbuotojų grupės
description: Šioje temoje aprašomi priežiūros darbuotojai ir darbuotojų grupės modulyje „Turto valdymas“.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetWorkerGroupCopyFromResourceGroup, EntAssetWorkerGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29fb487f02c28dbe940a1e00891f1e7ed20135b2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433497"
---
# <a name="maintenance-workers-and-worker-groups"></a>Priežiūros darbuotojai ir darbuotojų grupės

[!include [banner](../../includes/banner.md)]

 

Šioje temoje aprašomi priežiūros darbuotojai ir darbuotojų grupės modulyje „Turto valdymas“. Modulyje „Turto valdymas“ galite priskirti priežiūros darbuotojus prie funkcinių vietovių. (Norėdami gauti daugiau informacijos apie funkcines vietas, žr. [Funkcinių vietų kūrimas](../functional-locations/create-functional-locations.md).) Ši funkcija gali būti naudinga, jei, pavyzdžiui, planuojate mašinos, kurios funkcinė vietovė yra 01, priežiūros užduotį ir norite priskirti priežiūros darbuotojus iš tos pačios vietovės užduočiai atlikti.

Taip pat galite kurti priežiūros darbuotojų grupes ir su jais susieti priežiūros darbuotojus. Ši funkcija naudinga, kai atliekate paprastą darbo užsakymo planavimą ir norite darbo užsakyme suplanuoti priežiūros darbuotojų grupę. Galite naudoti priežiūros darbuotojus ir priežiūrą atliekančių darbuotojų grupes, kad nustatytumėte pageidautinus priežiūros darbuotojus ir už priežiūrą atsakingus darbuotojus. 


## <a name="create-workers"></a>Kurti darbininkus

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Darbuotojai** \> **Darbuotojai**.
2. Spustelėkite **Naujas**, norėdami į sąrašą įtraukti naują darbuotoją.
3. Lauke **Darbuotojas** pasirinkite darbuotoją.
4. Nustatykite parinktį **Aktyvus** į **Taip**, kad darbo užsakymams suplanuotumėte darbuotoją.

    „FastTab“ skirtuke **Bendra** laukai **Išteklius** ir **Aprašas** automatiškai užpildomi, jei darbuotojui buvo parinktas išteklius. Laukas **Kalendorius** taip pat užpildomas automatiškai, jei darbuotoją nustatėte kaip išteklių ir tam ištekliui puslapyje **Ištekliai** priskyrėte kalendorių (**Organizacijos administravimas**\>**Ištekliai**\>**Ištekliai**).

5. „FastTab“ skirtuke **Grupės** pasirinkite **Pridėti**, tada darbuotojui parinkite priežiūros darbuotojų grupę. Pardavimo grupėje gali būti daugiau nei vienas darbuotojas.
6. Naudojant standartinę konfigūraciją, darbuotojo narystė grupėje įsigalios ir niekada nebaigs galioti nuo tos dienos, kai pridėsite grupę. Ši data rodoma lauke **Galioja**. Norėdami matyti lauką **Galioja** pasirinkite **Peržiūrėti** \> **Visi**. Jei darbuotojo narystė grupėje turėtų būti apribota tam tikram laikotarpiui, norėdami nustatyti periodą, naudokite laukus **Galiojantis** ir **Galiojimo pabaiga**.
7. „FastTab“ skirtuke **Funkcinės vietovės** pasirinkite **Pridėti** ir pasirinkite priežiūros darbuotojo funkcinę grupę. Taip pat nurodykite, kuri vietovė yra pirminė darbuotojo funkcinė vietovė.

    > [!NOTE]
    > Kai darbuotojui pridedate funkcinę vietovę, visas aktyvus turtas, kuris yra susijęs su tomis funkcinėmis vietovėmis, rodomas įvairiuose meniu elementuose, tokiuose kaip **Mano aktyvus turtas** ir **Mano aktyvios funkcinės vietovės**. Jie taip pat rodomi turto peržvalgose, atsirandančiose kuriant naują turtą, priežiūros užklausą arba darbo užsakymą.

    „FastTab“ skirtuko **Informacija** laukuose rodomas priežiūros darbuotojų grupių ir funkcinių vietovių, su kuriomis susijęs pasirinktas priežiūros darbuotojas, skaičius.

## <a name="create-worker-groups"></a>Darbuotojų grupių kūrimas

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Darbuotojai** \> **Priežiūros darbuotojų grupės**.
2. Spustelėkit **Naujas**, norėdami į sąrašą įtraukti naują darbuotoją.
3. Lauke **Priežiūros darbuotojų grupė** įveskite grupės ID.
4. Tada lauke **Pavadinimas** įveskite pavadinimą.
5. „FastTab“ skirtuke **Darbuotojai** pasirinkite **Pridėti** ir darbuotojų grupei pasirinkite priežiūros darbuotoją. Norėdami sužinoti apie laukus **Galiojantis** ir **Galiojimo pabaiga**, žiūrėkite ankstesnės procedūros 6 veiksmą.
6. Jei išteklių grupė turėtų būti susieta su pasirinkta priežiūros darbuotojų grupe, pasirinkite **Kopijuoti iš išteklių grupės**. Lauke **Grupė** pasirinkite išteklių grupę, iš kurios kopijuosite kalendoriaus parametrus. Po to, lauke **Darbuotojų grupė** pasirinkite darbuotojų grupę, kad į ją nukopijuotumėte išteklių grupės kalendoriaus parametrus. Šis veiksmas svarbus tik tada, kai norite, kad planuojant darbo užsakymą, priežiūros darbuotojai galėtų naudoti su ištekliumi (darbo centru) susijusį kalendorių.

    „FastTab“ skirtuko **Informacija** lauke nurodomas priežiūros darbuotojų, kurie buvo pridėti į pasirinktą darbuotojų grupę, skaičius.
