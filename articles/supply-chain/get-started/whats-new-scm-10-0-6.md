---
title: Kas nauja ar pasikeitė „Dynamics 365 Supply Chain Management“ 10.0.6 (2019 m. lapkritis)
description: Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 Supply Chain Management“ 10.0.6 funkcijos.
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 9ee25036488d2f7f24c1691d36239f3f34caf0cb
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/14/2020
ms.locfileid: "3802924"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a>Kas nauja ar pasikeitė „Dynamics 365 Supply Chain Management“ 10.0.6 (2019 m. lapkritis)

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Supply Chain Management“ 10.0.6 funkcijos. Šios versijos komponavimo numeris yra 10.0.234. Nors bendro pasiekiamumo data yra lapkričio mėn., naujos funkcijos prieinamos su ankstyvu leidimu spalio mėn. Daugiau informacijos apie versiją 10.0.6 žr. [Papildomi ištekliai](whats-new-scm-10-0-6.md#additional-resources).

## <a name="product-configuration-models-v2-data-entity"></a>Produkto konfigūracijos modelių V2 duomenų objektas

„Produkto konfigūracijos modelių“ duomenų objekto antra versija yra išleista (vadinama „produktų konfigūracijos modeliai V2“). Numatytasis šablonas „418 – produkto konfigūracijos modeliai“ taip pat turi būti toks, kad naudotų naują „produkto konfigūracijos modelių v2“ duomenų objektą importavimo / eksportavimo sistemos šablonuose. Šablonas nebus automatiškai atnaujinamas, todėl jums reikės įkelti šabloną iš numatytojo rankiniu būdu. V2 objektas eksportuoja vieną eilutę kaip atskirą failą priede, o ne įterpinį, sprendžiant v1 objekto dydžio apribojimus. 
 
Ką reikia daryti norint atlikti šį keitimą?
-    Kadangi v1 objektas buvo pasenęs, turite pradėti pereiti iš V1 į V2. Jei naudojate šabloną „418-produkto konfigūracijos modeliai“, galite spustelėti mygtuką „įkelti numatytuosius šablonus“ ir iš naujo įkelti šabloną „418 – produkto konfigūracijos modeliai“
-    Jei norite išlaikyti suderinamumą su esamomis sistemomis, galite kol kas tęsti naudojimąsi esamu šablonu ir (pasenusiu) v1 objektu, kol savo integracijas perkelsite į naują šabloną. 

## <a name="feature-management-enhancements"></a>Funkcijų valdymo pagerinimai
Funkcijų valdymas dabar leidžia įjungti visas naujas funkcijas pagal numatytuosius parametrus, prašyti patvirtinimo, kad būtų įjungta funkcija, ir įjungti visas dar neįjungtas funkcijas. 


## <a name="purchase-agreement-responsible-party"></a>Už pirkimo sutartį atsakinga šalis
Dabar turite galimybę apibrėžti pirminės ir antrinės atsakomybės šalis pirkimo sutarties klasifikacijos formoje ir iš jos parengiamoje pirkimo sutartyje.  Tai leidžia vartotojams pamatyti tai, kas praleista sutartyse.

## <a name="rfq-link-on-the-purchase-order-line"></a>RFQ saitas pirkimo užsakymo eilutėj
Galite įtraukti nuorodos saitą iš pirkimo užsakymo eilučių atgal į atitinkamas RFQ eilutes, iš kurių jos atsirado, kad vartotojas galėtų lengvai gauti papildomą pasiūlymo patvirtinimo dokumentą.

## <a name="additional-resources"></a>Papildomi ištekliai

### <a name="bug-fixes"></a>Klaidų ištaisymai
Norėdami gauti daugiau informacijos apie klaidų ištaisymus, įtrauktus į kiekvieną iš naujinimų, kurie yra 10.0.6 dalis, prisijunkite prie „Lifecycle Services“ (LCS) ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).

### <a name="platform-update-30"></a>Platformos „update 30“
„Microsoft Dynamics 365 Supply Chain Management“ 10.0.6 sudaro platformos 30 naujinimas. Norėdami daugiau sužinoti apie platformos 30 naujinimą, žr. [Kas nauja ar pakeista platformos 30 naujinime](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).

### <a name="dynamics-365-2019-release-wave-2-plan"></a>„Dynamics 365“: 2019 m. 2-os leidimo bangos planas
Norite sužinoti apie būsimas ir neseniai išleistas mūsų verslo programų ar platformos galimybes?

Peržiūrėkite [„Dynamics 365“: 2019 m. 2-os leidimo bangos planas](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/). Visą išsamią informaciją užfiksavome viename dokumente, kurį galite naudoti planuodami.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Pašalintos ir pasenusios „Supply Chain Management“ funkcijos

Temoje [Pašalintos arba pasenusios funkcijos „Dynamics 365 Supply Chain Management“](removed-deprecated-features-scm-updates.md) aprašomos „Supply Chain Management“ funkcijos, kurios yra pašalintos, yra suplanuotos pašalinti arba yra pasenusios.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Prieš pašalinant iš produkto bet kokią funkciją, pranešimas apie nebenaudojimą bus paskelbtas [Pašalintos arba pasenusios funkcijos „Dynamics 365 Supply Chain Management“](removed-deprecated-features-scm-updates.md) temoje 12 mėnesių prieš pašalinimą.

Atlikus keitimus, kurie paveikia tik kompiliavimo laiką, bet yra dvejatainiškai suderinami su smėlio dėžės ir gamybos aplinka, nebenaudojimo laikas bus trumpesnis nei 12 mėnesių. Paprastai, tai yra funkciniai naujinimai, kuriuos reikia atlikti kompiliatoriui.
