---
title: Atsargų žurnalai
description: Šioje temoje aprašyta, kaip galima naudoti atsargų žurnalus įvairių faktinių atsargų operacijų tipams registruoti.
author: perlynne
ms.date: 04/05/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalBOM, InventJournalCount, InventJournalCountTag, InventJournalLossProfit, InventJournalMovement, InventJournalTransfer, WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 51631
ms.assetid: 3fedeaaf-502f-483c-93d2-ab266828189e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a94c5371db10fa4f0090f2d177b1a01233ab0f30
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826040"
---
# <a name="inventory-journals"></a>Atsargų žurnalai

[!include [banner](../includes/banner.md)]

Šioje temoje aprašyta, kaip galima naudoti atsargų žurnalus įvairių faktinių atsargų operacijų tipams registruoti.

Atsargų žurnalai „Supply Chain Management‟ naudojami registruoti įvairių tipų fizinių atsargų operacijoms, pvz., išdavimų ir gavimų registravimui, atsargų judėjimui, komplektavimo specifikacijų (KS) kūrimui ir fizinių atsargų suderinimui. Panašiu būdu naudojami visi šie atsargų žurnalai, tik jie suskirstyti į skirtingus tipus.

## <a name="types-of-inventory-journals"></a>Atsargų žurnalų tipai
Galima rinktis iš toliau nurodytų atsargų žurnalų tipų.

-   Perkėlimas
-   Atsargų koregavimas
-   Perkėlimas
-   KS
-   Prekių gavimas
-   Gamybos įvestis
-   Skaičiavimas
-   Skaičiavimas pagal žymę

### <a name="movement"></a>Perkėlimas

Kai naudojate atsargų judėjimo žurnalą, pridėdami atsargas galite prie prekės pridėti išlaidas, tačiau turite rankiniu būdu papildomas išlaidas paskirstyti DK sąskaitai – kuriant žurnalą nurodyti DK korespondentinę sąskaitą. Šis atsargų žurnalo tipas naudingas, jei norite perrašyti numatytąsias registravimo sąskaitas.

### <a name="inventory-adjustment"></a>Atsargų koregavimas

Kai naudojate atsargų koregavimo žurnalą, pridėdami atsargų galite prie prekės pridėti išlaidų. Atsižvelgiant į prekių grupės registravimo profilio sąranką, papildomos išlaidos automatiškai registruojamos į konkrečią DK sąskaitą. Naudokite šį atsargų žurnalo tipą pelnu ir nuostoliu norėdami atnaujinti atsargų kiekius, kai prekė turėtų išlaikyti savo numatytąją DK korespondentinę sąskaitą. Registruojant atsargų koregavimo žurnalą, užregistruojamas atsargų gavimas arba išdavimas, pakeičiamos atsargų reikšmės bei sukuriamos DK operacijos.

### <a name="transfer"></a>Perkėlimas

Perkėlimo žurnalus galite naudoti norėdami prekes perkelti į sandėliavimo vietas, paketus ar produktų variantus, nesusiedami jokių išlaidų. Pavyzdžiui, prekes galite perkelti iš vieno sandėlio į kitą tos pačios įmonės sandėlį. Kai naudojate perkėlimo žurnalą, turite nurodyti tiek „iš‟, tiek „į‟ atsargų dimensijas (pvz., Teritorijos ir Sandėlio). Atitinkamai pakeičiamos turimos apibrėžtų atsargų dimensijų atsargos. Atsargų perkėlimai atspindi skubų medžiagos judėjimą. Tranzitinės atsargos nesekamos. Jei tranzitines atsargas reikia sekti, geriau naudokite perkėlimo užsakymą. Kai užregistruojate perkėlimo žurnalą, kiekvienos žurnalo eilutės sukuriamos dvi operacijos:

-   atsargų išdavimas vietoje „iš‟;
-   atsargų gavimas vietoje „į‟.

### <a name="bom"></a>KS

Kai KS skelbiate baigta, galite kurti KS žurnalą. Naudodami KS žurnalą galite registruoti KS tiesiogiai. Taip registruojant generuojamas produkto atsargų gavimas su susieta KS ir produktų, kurie yra įtraukti į KS, atsargų išdavimas. Šis atsargų žurnalo tipas yra naudingas paprastais ar didelės apimties gamybos scenarijais, kai maršrutų nereikia.

### <a name="item-arrival"></a>Prekių gavimas

Prekių gavimo žurnalą galite naudoti prekių gavimui registruoti (pvz., iš pirkimo užsakymų). Prekių gavimo žurnalą galima sukurti kaip gavimų valdymo dalį **Gavimų apžvalgos** puslapyje, arba žurnalo įrašą galite rankiniu būdu sukurti **Prekių gavimo** puslapyje. Jei įgalinate funkciją, kuria prekių gavimo žurnalo pavadinimas tikrina paėmimo vietas, „Supply Chain Management‟ gautoms prekėms ieško vietos ir, jei jos yra, generuoja gaunamų prekių vietų paskirtis.

### <a name="production-input"></a>Gamybos įvestis

Gamybos įeigos žurnalai veikia kaip prekių gavimo žurnalai, tik jie naudojami gamybos užsakymams.

### <a name="counting"></a>Skaičiavimas

Skaičiavimo žurnalai leidžia taisyti dabartines turimas registruotas prekių ar prekių grupių atsargas, ir tada faktinį fizinį kiekį registruoti, kad galėtumėte atlikti reikiamus koregavimus ir taip suderinti skirtumus. Skaičiavimo strategijas galima susieti su skaičiavimo grupėmis, kad būtų lengviau grupuoti prekes su įvairiomis charakteristikomis ir tas prekes būtų galima įtraukti į skaičiavimo žurnalą. Pvz., galite nustatyti, kad skaičiavimo grupės skaičiuotų prekes, kurios turi konkretų dažnį, arba prekes skaičiuoti, kai atsargos sumažėja iki tam tikro lygio. Informacijos apie tai, kaip apibrėžti skaičiavimo grupes, ieškokite [Apibrėžti atsargų skaičiavimo procesus](tasks/define-inventory-counting-processes.md).

### <a name="tag-counting"></a>Skaičiavimas pagal žymę

Žymių skaičiavimo žurnalai naudojami skaičiavimo partijai priskirti žymę su numeriu. Žymėje turėtų būti žymės numeris, prekės numeris ir prekės kiekis. Siekiant užtikrinti, kad žymė būtų naudojama tik vieną kartą, ir kad būtų panaudotos visos žymės, kiekvienas prekės numeris turėtų turėti unikalų žymių rinkinį, kuris turėtų savo numeraciją. Gali būti nustatytos trys kiekvienos žymės būsenos reikšmės.

-   **Panaudota** – skaičiuojamas šios žymės prekės numeris.
-   **Anuliuota** – šios žymės prekės numeris anuliuojamas.
-   **Nėra** – šios žymės prekės numerio nėra.

Registruojant žymių skaičiavimo žurnalą, pagal jo eilutes sukuriamas naujas skaičiavimo žurnalas. Daugiau informacijos apie žymių skaičiavimą ieškokite [Atsargų žymių skaičiavimas](inventory-tag-counting.md).

## <a name="working-with-journals"></a>Darbas su žurnalais
Vienu metu žurnalą gali pasiekti tik vienas vartotojas. Jei vienu metu pasiekti žurnalus ir kurti žurnalų eilutes turi keli naudotojai, jie turi pasirinkti tuo metu nenaudojamus žurnalus, kad būtų išvengta informacijos perrašymo. Situacijose, kai tą patį žurnalo tipą naudoja keli skyriai, naudinga sukurti keletą žurnalo pavadinimų (pvz., po vieną kiekvienam skyriui). Taip pat gali būti naudinga žurnalus padalyti, kad kiekviena registravimo procedūra būtų įvedama į savo unikalų atsargų žurnalą. Jei registravimo procedūros susietos su atsargų operacijomis, sukurkite vieną reguliaraus atsargų koregavimo žurnalą ir vieną atsargų skaičiavimo žurnalą.

## <a name="posting-journal-lines"></a>Žurnalo eilučių registravimas
Sukurtas žurnalo eilutes galite registruoti bet kuriuo metu tol, kol su preke neleisite atlikti papildomų operacijų. Į žurnalą įvesti duomenys lieka tame žurnale, net jei uždarote žurnalą neužregistravę eilučių.

## <a name="data-entity-support-for-inventory-journals"></a>Duomenų objekto atsargų žurnalų palaikymas

Duomenų objektai palaiko toliau nurodytų tipų scenarijus.
-    Sinchroninė paslauga („OData“)
-  Asinchroninis integravimas

Daugiau informacijos žr. [Duomenų objektai](../../dev-itpro/data-entities/data-entities.md).

> [!NOTE]
> Ne visuose atsargų žurnaluose „OData“ įjungta, todėl negalima naudoti „Excel“ duomenų jungties norint duomenis publikuoti, naujinti ir importuoti atgal į „Supply Chain Management“. 

Kitas skirtumas tarp žurnalo duomenų objektų yra galimybė naudoti sudėtinius objektus, kurie apima antraščių ir eilučių duomenis. Šiuo metu galite naudoti sudėtinius objektus, skirtus toliau nurodytiems elementams.
-   Atsargų koregavimo žurnalas
-   Atsargų perkėlimo žurnalas

Šie du atsargų žurnalai *atsargų inicijavimo* scenarijų palaiko tik kaip duomenų valdymo importavimo projekto dalį.
-  Kai žurnalo antraštės numeris nenurodytas, bet žurnalo tipo numeracija nurodyta, importavimo užduotis automatiškai sukurs žurnalo antraštes, skirtas 1000 eilučių. Pavyzdžiui, importuojant 2020 eilučių bus sukurtos toliau nurodytos trys žurnalo antraštės.
    -  1 antraštė: apims 1000 eilučių
    -  2 antraštė: apims 1000 eilučių
    -  3 antraštė: apims 20 eilučių
-  Laikoma, kad unikali eilutės informacija saugoma kiekvienoje atsargų dimensijoje, kuri gali būti produkto, saugyklos arba sekimo dimensija. Todėl neįmanoma importuoti žurnalo eilučių, jei tik datos laukas skiriasi to paties importavimo projekto eilutėse.

## <a name="additional-resources"></a>Papildomi ištekliai

[Duomenų objektai](../../dev-itpro/data-entities/data-entities.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]