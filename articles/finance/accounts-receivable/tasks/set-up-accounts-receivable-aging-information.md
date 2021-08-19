---
title: Nustatyti ir generuoti gautinų sumų skirstymo pagal terminus informaciją
description: Šis vadovas jums padės nustatyti skirstymo pagal terminus laikotarpio apibrėžtį, pagal terminus skirstyti klientų balansus ir peržiūrėti balansus sąraše Pagal terminus suskirstytas balansas ir puslapyje Mokėjimų priežiūra.
author: mikefalkner
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2468beea898de6367c655b54d89c1faab1e4435506bd21019c970af32d215729
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713287"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a>Nustatyti ir generuoti gautinų sumų skirstymo pagal terminus informaciją

[!include [banner](../../includes/banner.md)]

Šis vadovas jums padės nustatyti skirstymo pagal terminus laikotarpio apibrėžtį, pagal terminus skirstyti klientų balansus ir peržiūrėti balansus sąraše Pagal terminus suskirstytas balansas ir puslapyje Mokėjimų priežiūra. Šiame įraše naudojama demonstracinė įmonė USMF.


## <a name="create-an-aging-period-definition"></a>Kurti skirstymo pagal terminus laikotarpio apibrėžtį
1. Eikite į **naršymo sritį > Moduliai > Kreditas ir mokėjimai > Sąranka > Skirstymo pagal terminus laikotarpio apibrėžimai**.
2. Spustelėkite **Naujas**.
3. Lauke **Skirstymo pagal terminus laikotarpio apibrėžimai** surinkite reikšmę.
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Spustelėdami **Įtraukti po** įterpsite naują skirstymo pagal terminus laikotarpį.
6. Lauke **Laikotarpis** įveskite aprašą, kuris bus rodomas skirstymo pagal terminus ataskaitose.
7. Lauke **Vienetas** įveskite skaičių.
8. Lauke **Intervalas** pasirinkite parinktį. DK laikotarpis suderina laikotarpį su DK kalendoriumi. Diena, savaite, mėnesiu, ketvirčiu ir metais pagal datos tipą apibrėžiamas intervalas. Parinktis Neribotas pasirenka visas operacijas prieš ankstesnį laikotarpį arba po jo – tai priklauso nuo to, ar tai pirmas, ar paskutinis laikotarpis.  
9. Lauke **Skirstymo pagal terminus indikatorius** pasirinkite parinktį.
10. Pasirinkite laikotarpį tinklelio viršuje. Atnaujinti aprašą, kad būtų apibūdintas seniausias skirstymo pagal terminus laikotarpio apibrėžties laikotarpis
11. Lauke **Laikotarpis** įveskite naują skirstymo pagal terminus laikotarpio aprašą.
12. Uždarykite puslapį.

## <a name="age-the-balances"></a>Balansus skirstyti pagal terminus
1. Pasirinkite **Kreditas ir mokėjimai > Periodinės užduotys > Pagal terminus suskirstyti klientų balansus**.
2. Lauke **Skirstymo pagal terminus laikotarpio apibrėžimas** pasirinkite savo sukurtą skirstymo pagal terminus laikotarpio apibrėžtį.
    + Kiekvienos skirstymo pagal terminus laikotarpio apibrėžties galite turėti vieną momentinę kopiją.  
    + Visi klientai apdorojami pagal numatytąsias nuostatas. Šią pasirinktį galite naudoti apskaičiuoti vienam klientų mokėjimų priežiūros telkiniui.  
    + Iš operacijos pasirinkite datą, kurią naudosite skirstydami pagal terminus.  
    + Skirstymo pagal terminus datą pasirinkite „nuo‟. Numatytoji data yra šiandienos, tačiau, šį lauką pakeitę į Pasirinkta data, galėsite pasirinkti norimą datą. Paketiniam vykdymui naudokite šiandienos datą.  
3. Išplėskite **Įmonė** diapazoną. Galite pasirinkti įmones, kurios bus įtrauktos į momentinę kopiją. Dabartinė įmonė pasirenkama pagal numatytąsias nuostatas.
4. Norėdami apdoroti momentinę kopiją, spustelėkite **Gerai**. Apdorojimas šiek tiek užtruks, tad palaukite, kol išnyks slankiklis ir patikrinkite, ar pranešimų centre nėra pranešimo.

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a>Peržiūrėti balansus sąraše Pagal terminus suskirstyti balansai ir puslapyje Rinkinys
1. Pasirinkite **Kreditas ir mokėjimai > Mokėjimų peržiūra > Suskirstyti pagal terminus balansai**. Sąrašo puslapyje rodomi kliento balansai. Skirstymo pagal terminus piktograma rodo seniausios operacijos skirstymo pagal terminus laikotarpį.  
2. Pasirinkite klientą, turintį balansą.
3. Norėdami peržiūrėti pagal terminus suskirstytus balansus, išplėskite **Skirstymo pagal terminus faktas** sritį. „FactBox‟ skirstymo pagal terminus laikotarpio apibrėžtis paimama iš numatytosios skirstymo pagal terminus apibrėžties, nurodytos parametruose. Ją keisti galite naudodami meniu Rinkti.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]