---
title: "Duomenų importavimas iš „Excel“ duomenų objekto šablonų naudojant kelis darbalapius"
description: "Šioje temoje aprašoma, kaip naudojant „Excel“ duomenų objekto šablonus importuoti duomenis į „Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition“."
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: 84b9e9128d7ea6cdf9949549f4ab7a1c6c01691b
ms.contentlocale: lt-lt
ms.lasthandoff: 12/14/2017

---

# <a name="excel-templates-with-multiple-worksheets"></a>„Excel“ šablonai su keliais darbalapiais

„Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition“ duomenų valdymas palaiko „Microsoft Excel“ pagrįstus šablonus, skirtus duomenų objektams. Šiuose šablonuose gali būti vienas ar daugiau darbalapių. Šablonai su keliais darbalapiais dažnai naudojami, kai patogu tvarkyti duomenis viename faile ir importuoti juos į kelis duomenų objektus. Pavyzdys: vietos ir sandėliai.

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a>Failo įkėlimas vieną kartą ir susiejimas su visais objektais
Apžvelkime pavyzdį: turime vieną „Excel“ failą ir darbalapius pavadinimais **Vietos** ir **Sandėliai**. Norėdami nustatyti duomenų importavimo projektą, įtraukite pirmą duomenų objektą, **Vietos**, tada nusiųskite failą. Kaip šio objekto naudotiną darbalapį galėsite pasirinkti darbalapį **Vietos**.

Jei įtrauksite antrą objektą **Sandėliai** neuždarę formos **Įtraukti failą**, darbalapių peržvalgoje galėsite pasirinkti darbalapį **Sandėliai** ir jums nereikės dar kartą nusiųsti failo. Naują failą nusiųsti reikėtų tik jei darbalapio **Sandėliai** duomenys buvo į kitame faile.

![Keli darbalapiai](./media/AddFileMultipleWorkSheets.png) 

## <a name="fix-worksheet-to-entity-mapping"></a>Darbalapio susiejimo su objektu nustatymas

Darbalapio susiejimą su duomenų objektu importavimo užduotyje galima nustatyti naudojant tinklelį. Tinklelio stulpelyje **Darbalapis** rodomi susieto failo darbalapiai. Išplečiamajame meniu galite pasirinkti kitą darbalapį. Jei pasirinktas darbalapis jau susietas su objektu duomenų projekte, sistema paprašys patvirtinti pakeitimą. Rekomenduojame nustatyti visus susiejimus tinklelyje.

![Darbalapio susiejimo naujinimas](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a>Pakartotinis susiejimas su nauju failu

Tais atvejais, kai duomenų projekte reikia nusiųsti esamų objektų to pačio failo naują versiją arba visiškai naują failą, turite naudoti formą **Įtraukti failą** ir vėl įtraukti objektus, kaip juos įtrauktumėte pirmą kartą. Prieš tęsiant sistema patvirtins, kad norite perrašyti esamus objektus duomenų projekte. Objektų, kurie dar kartą neįtraukiami (arba neperrašomi), susiejimai (iš kito ankstesnio failo) išliks.

## <a name="upload-a-file-using-run-project"></a>Failo nusiuntimas naudojant parinktį Vykdyti projektą

Galite įkelti „Excel“ failą naudodami parinktį **Vykdyti projektą**, norėdami vykdyti importavimo projektą. Turite būti atsargūs ir nusiųsti tik failus, kuriuose yra darbalapiai, atitinkantys duomenų projekto duomenų objektų esamus susiejimus. Jei naujai nusiųstame faile darbalapių nerasta, sistema rodo klaidą ir importavimas sustabdomas. Jei objekto susiejimą su darbalapiu reikia keisti, pirmiausia reikia atnaujinti duomenų projekto susiejimus pačiame duomenų objekte, kad būtų galima naudoti failą formoje **Vykdyti projektą**.


