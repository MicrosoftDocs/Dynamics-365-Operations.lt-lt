---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent Core HR“ (2018 m. spalio 1 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 for Talent Core HR“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 15b5fd7095a62aa9b7b79ebfcada667959b756aa
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/19/2019
ms.locfileid: "858749"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-1-2018"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent Core HR“ (2018 m. spalio 1 d.)

[!include [banner](includes/banner.md)]

**8.1.1035.0 versija**

Šioje temoje aprašomos naujos ir pakeistos „Core HR“ funkcijos.

## <a name="turn-off-electronic-payment-validation"></a>Elektroninių mokėjimų tikrinimo išjungimas

Elektroninio mokėjimo informacijos tikrinimas vykdomas, jei nustatote tiesioginį išmokų pervedimą darbo srityje **Darbuotojo savitarna** (ESS) arba tiesiogiai darbuotojo formoje. Ši parinktis suteikia galimybę netaikyti tikrinimo, jei jums nereikia tikrinti sumų ir likučio vertės. Ši funkcija yra naudinga, jei integruojate išorinę algalapių sistemą, kuriai taikomi skirtingi reikalavimai.

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a>Vadovo savitarna – tikslų įtraukimas komandos nariams naudojant plytelę Komandos efektyvumo tikslai

Prieš šį leidimą vadovai galėjo įtraukti tikslus darbuotojams atskirai naudodami efektyvumo tikslus, susietus su kiekvienu darbuotoju. Įdiegus šį naujinimą vadovai galės naudoti plytelę **Komandos efektyvumo tikslai** ir kurti naujus tikslus, pasirinkdami bet kurią iš jų tiesioginių ataskaitų.

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a>Vadovo savitarna – apžvalgų įtraukimas komandos nariams naudojant plytelę Komandos efektyvumo apžvalgos

Prieš šį leidimą vadovai galėjo įtraukti apžvalgas darbuotojams atskirai naudodami apžvalgas, susietas su kiekvienu darbuotoju. Įdiegus šį naujinimą vadovai galės naudoti plytelę **Komandos efektyvumo apžvalgos** ir kurti naujas apžvalgas, pasirinkdami bet kurią iš jų tiesioginių ataskaitų.

## <a name="configure-proration-options-by-leave-plan"></a>Proporcingo paskirstymo parinkčių konfigūravimas naudojant atostogų planą

Organizacijos paskirsto nedarbo laiką skirtingai pagal tai, kada darbuotojai prisijungia prie įmonės arba iš jos išeina. Kai kuriose organizacijose darbuotojams skiriamas visas jiems skirtas nedarbo laikas pirmąją darbo laiką, o kitos organizacijos tai paskirsto proporcingai. Šiame leidime pateikiamos naujos galimybės pasirinkti, kaip proporcingai paskirstyti premijas ir sukauptą nedarbo laiką naujiems organizacijos darbuotojams ir ją paliekantiems asmenims. Galimos parinktys: Proporcingai paskirstyta, Visas kaupimas ir Nėra kaupimo.

## <a name="other-changes"></a>Kiti pakeitimai

-   Atnaujintas objektas Darbuotojas – dabar plytelę **Asmeninis** galima atnaujinti naudojant „Excel“ įtraukimo / duomenų valdymo funkciją.

-   Saugos pakeitimai suteikia galimybę pašalinti darbuotojo savitarnos mokėjimo informacijos mygtukus **Naikinti** ir **Išjungti**.

## <a name="known-issue"></a>Žinoma problema

-   **Problema:** pridedant naują priedą prie darbininko, mygtukai **Naujas** ir **Redaguoti** yra pateikiami pilka spalva. **Problemos sprendimas:** prieš atidarydami priedo puslapį įsitikinkite, kad „FactBoxes“ laukai puslapyje **Darbininkas** yra uždaryti. Jei „FactBoxes“ laukai yra uždaryti, kai įkeliamas puslapis **Darbininkas**, **priedų** mygtukus bus galima naudoti. (Ši problema bus pašalinta kitame platformos naujinime.)
