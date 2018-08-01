---
title: "Standartinių savikainų būtinosios sąlygos"
description: "Šioje temoje aprašomi pagrindiniai standartinių savikainų naudojimo veiksmai."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 338e0847ea91ee2582df0aab3e31a97c4f24113e
ms.openlocfilehash: 016eec12c31398beede7fdddc4548ec196ebd704
ms.contentlocale: lt-lt
ms.lasthandoff: 06/25/2018

---

# <a name="prerequisites-for-standard-costs"></a>Standartinių savikainų būtinosios sąlygos

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomi pagrindiniai standartinių savikainų naudojimo veiksmai. Vėlesni veiksmai priklauso nuo įmonės operacijų. Pavyzdžiui, veiksmai skiriasi negamybinėje aplinkoje, gamybinėje aplinkoje, nenaudojančioje nukreipimų, ir gamybinėje aplinkoje, naudojančioje nukreipimus. 

Norėdami nustatyti standartines savikainas, atlikite tolesnius veiksmus.

**1. Sukurkite standartinių savikainų prekių modelių grupę.**

Naudokite puslapį **Prekių modelių grupės**, norėdami sukurti naują standartinių savikainų grupę ir priskirti atsargų modelį **Standartinė savikaina**. Prekių modelio grupės identifikatorius turi turėti prasmę, pvz., **Stand. išlaidos**. Norėdami nurodyti, kad grupė turėtų leisti neigiamas finansines atsargas, ir kad ji turėtų registruoti faktines atsargas bei finansines atsargas, pažymėkite žymės langelius. Ši standartinių savikainų grupė bus paskirta prekėms.

**2. Nustatykite DK sąskaitas, kurios yra susijusios su nuokrypiu nuo standartinės savikainos.** 

Norėdami nustatyti DK sąskaitas, kurios yra susijusios su nuokrypiu nuo standartinės savikainos, naudokite puslapį **Sąskaitų planas**. Šios DK sąskaitos turi būti nustatytos prieš jas priskiriant puslapyje **Registravimas**. DK sąskaitos gali atspindėti prekių grupes ir savikainų grupes.

**3. Prekių registravimui priskirkite DK sąskaitas, kurios yra susijusios su nuokrypiu nuo standartinės savikainos.** 

Norėdami priskirti DK sąskaitas, kurios yra susijusios su nuokrypiu nuo standartinės savikainos, naudokite puslapį **Registravimas**. Nuokrypio DK sąskaitą galite nurodyti pagal prekę (ar prekių grupę) ir pagal savikainos grupę (ar kainos grupės tipą), arba galite nurodyti, kad DK sąskaita taikoma visoms prekėms ir visoms savikainų grupėms. Šios parinktys atitinka lentelių, grupių ir visų savikainų santykiams. 

Prieš nustatydami prekių registravimo taisykles, naudokite puslapį **Operacijų deriniai**, kad įjungtumėte išlaidų santykius (lentelėms, grupėms ir viskam).

**4. Nustatykite atsargų parametrus, kurie yra susiję su standartine savikaina.** 

-  Norėdami nustatyti du kaštų kontrolės parametrus, kurie yra susiję su standartiniais kaštais, naudokite puslapio **Atsargų apskaitos strategijų sąranka > Parametrai** skirtuką **Atsargų apskaita**.

    -  Lauke **Išlaidų paskirstymas** pasirinkite **Nėra** arba **Antrinė DK**. Jei pasirenkate **Antrinė DK**, išlaidų paskirstymas yra *aktyvus*. Aktyvus išlaidų paskirstymas yra svarbus skaičiavimui, išlaikymui ir išlaidų grupės segmentavimo peržiūrai visoje standartinių išlaidų komponentų kelių lygių produkto struktūroje. Kai išlaidų paskirstymas yra aktyvus, galite pateikti ir analizuoti atsargas, nebaigtą gamybą (NG) ir parduotų prekių išlaidas išlaidų grupei viename lygyje, keliuose lygiuose ar visame formate. Kai išlaidų paskirstymas yra aktyvus, suaktyvinus pagamintos prekės išlaidas, išlaidų grupių segmentavimas bus saugomas prekės išlaidų įraše. 

    -  Jei pasirinksite **Nėra**, standartinių savikainų prekių išlaidų grupės segmentavimas nebus tvarkomas. Kitaip tariant, pagamintos prekės standartinė savikaina bus apskaičiuota ir tvarkoma kaip viena suma be išlaidų grupių segmentavimo. Pagamintų komponentų išlaidų įnašai bus sujungti į vieną sumą.

-  Lauke **Nuokrypiai nuo standarto** pasirinkite **Susumuota** arba **Pagal išlaidų grupę**. Jei pasirenkate **Pagal išlaidų grupę**, galite nustatyti pirkimo kainų nuokrypius ir gamybos nuokrypius pagal išlaidų grupę. Tai taip pat galite nustatyti keturis gamybos nuokrypių tipus: partijos dydis, kiekis, kaina ir pakaitalų nuokrypiai. Jei pasirenkate **Susumuota**, negalite nustatyti nuokrypių pagal išlaidų grupę ir negalite nustatyti keturių gamybos nuokrypių tipų. Galite peržiūrėti tik susumuotus gamybos nuokrypius.

-  Standartinė nuokrypių strategija veikia nepriklausomai nuo išlaidų paskirstymo strategijos. Kitaip tariant, galite pasirinkti išlaidų paskirstymo strategiją **Nėra** ir pasirinkti išlaidų grupės nuokrypius taip, kad gamybos nuokrypiai pagal išlaidų grupę vis tiek bus užfiksuoti.

**5. Sukurkite standartinių savikainų įkainojimo versijas.** 

Norėdami sukurti vieną ar kelias standartinių savikainų įkainojimo versijas, naudokite puslapį **Įkainojimo versijos nustatymas**. Kiekviena įkainojimo versija turi būti sukurta pagal įkainojimo tipą **Standartinė savikaina** ir turi leisti į turinį įtraukti išlaidų duomenis.

**6. Paruoškite esamą klientą naudoti standartines savikainas.** 

Klientai, norintys pakeisti savo esamus komponentus į standartinių savikainų atsargų modelį, turi naudoti puslapį **Standartinių išlaidų konvertavimai**.


<a name="related-topics"></a>Susijusios temos
--------

[Standartinės savikainos konvertavimo peržiūra](standard-cost-conversion-overview.md)


