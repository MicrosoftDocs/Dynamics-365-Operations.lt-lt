---
title: Nustatyti ir generuoti gautinų sumų skirstymo pagal terminus informaciją
description: Šis vadovas jums padės nustatyti skirstymo pagal terminus laikotarpio apibrėžtį, pagal terminus skirstyti klientų balansus ir peržiūrėti balansus sąraše Pagal terminus suskirstytas balansas ir puslapyje Mokėjimų priežiūra.
author: mikefalkner
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 77b5dd5feb16cc3bd6d64b6520cc47087c5b5224
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834372"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a>Nustatyti ir generuoti gautinų sumų skirstymo pagal terminus informaciją

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šis vadovas jums padės nustatyti skirstymo pagal terminus laikotarpio apibrėžtį, pagal terminus skirstyti klientų balansus ir peržiūrėti balansus sąraše Pagal terminus suskirstytas balansas ir puslapyje Mokėjimų priežiūra. Šiame įraše naudojama demonstracinė įmonė USMF.


## <a name="create-an-aging-period-definition"></a>Kurti skirstymo pagal terminus laikotarpio apibrėžtį
1. Eikite į **Navigation pane > Modules > Credit and collections > Setup > Aging period definitions**.
2. Spustelėkite **Naujas**.
3. Lauke **Aging period definition** surinkite reikšmę.
4. Lauke **Description field**surinkite reikšmę.
5. Spustelėję **Add below**, įterpsite naują skirstymo pagal terminus laikotarpį.
6. Lauke **Period** įveskite aprašą, kuris bus rodomas skirstymo pagal terminus ataskaitose.
7. Lauke **Unit** įveskite skaičių.
8. Lauke **Interval** pasirinkite parinktį. DK laikotarpis suderina laikotarpį su DK kalendoriumi. Diena, savaite, mėnesiu, ketvirčiu ir metais pagal datos tipą apibrėžiamas intervalas. Parinktis Neribotas pasirenka visas operacijas prieš ankstesnį laikotarpį arba po jo – tai priklauso nuo to, ar tai pirmas, ar paskutinis laikotarpis.  
9. Lauke **Aging indicator** pasirinkite parinktį.
10. Pasirinkite laikotarpį tinklelio viršuje. Atnaujinti aprašą, kad būtų apibūdintas seniausias skirstymo pagal terminus laikotarpio apibrėžties laikotarpis
11. Lauke **Period** įveskite naują skirstymo pagal terminus laikotarpio aprašą.
12. Uždarykite puslapį.

## <a name="age-the-balances"></a>Balansus skirstyti pagal terminus
1. Pasirinkite **Credit and collections > Periodic tasks > Age customer balances**.
2. Lauke **Aging period definition** pasirinkite savo sukurtą skirstymo pagal terminus laikotarpio apibrėžtį.
    + Kiekvienos skirstymo pagal terminus laikotarpio apibrėžties galite turėti vieną momentinę kopiją.  
    + Visi klientai apdorojami pagal numatytąsias nuostatas. Šią pasirinktį galite naudoti apskaičiuoti vienam klientų mokėjimų priežiūros telkiniui.  
    + Iš operacijos pasirinkite datą, kurią naudosite skirstydami pagal terminus.  
    + Skirstymo pagal terminus datą pasirinkite „nuo‟. Numatytoji data yra šiandienos, tačiau, šį lauką pakeitę į Pasirinkta data, galėsite pasirinkti norimą datą. Paketiniam vykdymui naudokite šiandienos datą.  
3. Išplėskite **Company** diapazoną. Galite pasirinkti įmones, kurios bus įtrauktos į momentinę kopiją. Dabartinė įmonė pasirenkama pagal numatytąsias nuostatas.
4. Norėdami apdoroti momentinę kopiją, spustelėkite **Ok**. Apdorojimas šiek tiek užtruks, tad palaukite, kol išnyks slankiklis ir patikrinkite, ar pranešimų centre nėra pranešimo.

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a>Peržiūrėti balansus sąraše Pagal terminus suskirstyti balansai ir puslapyje Rinkinys
1. Pasirinkite **Credit and collections > Collections > Aged balances**. Sąrašo puslapyje rodomi kliento balansai. Skirstymo pagal terminus piktograma rodo seniausios operacijos skirstymo pagal terminus laikotarpį.  
2. Pasirinkite klientą, turintį balansą.
3. Norėdami peržiūrėti pagal terminus suskirstytus balansus, išplėskite **Aging fact** sritį. „FactBox‟ skirstymo pagal terminus laikotarpio apibrėžtis paimama iš numatytosios skirstymo pagal terminus apibrėžties, nurodytos parametruose. Ją keisti galite naudodami meniu Rinkti.  

