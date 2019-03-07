---
title: Duomenų importavimas iš „Excel“ duomenų objekto šablonų, kuriuose yra keletas darbalapių
description: Šioje temoje aprašoma, kaip naudojant „Excel“ duomenų objekto šablonus importuoti duomenis į „Microsoft Dynamics 365 for Finance and Operations“.
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 48239b48cbc24e34d74bbac36e8f827a15d7b840
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "351268"
---
# <a name="import-data-from-excel-data-entity-templates-that-have-multiple-worksheets"></a>Duomenų importavimas iš „Excel“ duomenų objekto šablonų, kuriuose yra keletas darbalapių

[!include [banner](../includes/banner.md)]

„Microsoft Dynamics 365 for Finance and Operations“ duomenų valdymas palaiko „Microsoft Excel“ pagrįstus šablonus, skirtus duomenų objektams. Šiuose šablonuose gali būti vienas ar daugiau darbalapių. Šablonai su keliais darbalapiais dažnai naudojami, kai patogu tvarkyti duomenis viename faile ir importuoti juos į kelis duomenų objektus. Pavyzdys: vietos ir sandėliai.

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
