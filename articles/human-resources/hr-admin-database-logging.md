---
title: Duomenų bazės registravimo konfigūravimas ir valdymas
description: Galite sekti lentelių ir laukų pakeitimus „Dynamics 365 Human Resources” naudodami duomenų bazės registravimą.
author: andreabichsel
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8057ebd0bc061c6bf78d8674c45e0885ffce681c
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467654"
---
# <a name="configure-and-manage-database-logging"></a>Duomenų bazės registravimo konfigūravimas ir valdymas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Galite sekti lentelių ir laukų pakeitimus „Dynamics 365 Human Resources” naudodami duomenų bazės registravimą. Šioje temoje aprašoma, kaip:

- Tvarkyti duomenų bazės registravimo saugą ir efektyvumą
- Nustatyti duomenų bazės registravimą
- Valyti duomenų bazės žurnalus

## <a name="overview-of-database-logging"></a>Duomenų bazės registravimo peržiūrą

Duomenų bazės registravimo funkcija stebi „Microsoft Dynamics 365 Human Resources” lentelių ir laukų pakeitimus. Šie pakeitimai apima įterpimo, atnaujinimo arba naikinimo veiksmus. Duomenų bazės registravimas išsaugo lentelių arba laukų, esančių duomenų bazės žurnalo lentelėje, keitimų įrašą.

Verslas duomenų bazės registravimą naudoja šiais tikslais:

- Kurti konkrečių lentelių, kuriose yra slaptos informacijos, keitimų audito įrašą.
- Sekti vienkartines operacijas. Duomenų bazės registravimas nėra skirtas automatinėms operacijoms, paleidžiamoms paketinėse užduotyse.

## <a name="security-for-database-logging"></a>Duomenų bazės registravimo sauga

Duomenų bazės žurnaluose gali būti slaptų duomenų. Riboti prieigą, kad būtų galima naudoti tik tuos saugos vaidmenis, kuriems reikalinga prieiga prie žurnalo duomenų.

## <a name="database-logging-and-performance"></a>Duomenų bazės registravimas ir našumas

Nors verslo perspektyva yra vertingas, duomenų bazės registravimas gali būti brangus išteklių naudojimo ir valdymo srityje. Duomenų bazės registravimą galima naudoti šiais tikslais:

- Duomenų bazės žurnalo lentelė gali greitai plėstis ir padidinti duomenų bazės dydį. Augimas priklauso nuo užregistruotų duomenų kiekio, kurį nusprendėte saugoti. Pagal numatytuosius nustatymus, duomenų bazės žurnalo lentelėje palaikomi tik 30 dienų žurnalo duomenys. 

- Duomenų bazės registravimas gali neigiamai paveikti ilgai trunkančius automatinius procesus, pvz., ilgai trunkančius duomenų importavimus.

### <a name="best-practices"></a>Geriausia praktika

Norėdami padidinti našumą, apribokite žurnalo įrašus pasirinkdami konkrečius laukus registruoti, o ne ištisas lenteles. Norint palaikyti bendrą našumą, duomenų bazės registravimas apribotas 20 lentelių.

> [!NOTE]
> Tik naujinimai gali būti registruojami atskiruose laukuose.

## <a name="set-up-database-logging"></a>Nustatyti duomenų bazės registravimą

Galite naudoti **Duomenų bazės pakeitimų registravimas** vedlį, kad nustatytumėte duomenų bazės registravimą. Vedlys suteikia lanksčią galimybę nustatyti lentelių arba laukų registravimą.

1. Eikite į **Sistemos administravimas > Saitai > Duomenų bazė > Duomenų bazės žurnalo nustatymas**. Pasirinkite **Nauja**, kad įjungtumėte **Registravimo duomenų bazės pakeitimai** vedlį.
2. Baikite vykdyti vedlio žingsnius.

## <a name="clean-up-database-logs"></a>Valyti duomenų bazės žurnalus

Galite naikinti dalį arba visus duomenų bazės žurnalus naudodami šias parinktis:

- Pasirinkite konkrečios lentelės visus žurnalus.
- Pasirinkite konkrečius duomenų bazės žurnalo tipus.
- Pasirinkite datą ir laiką, kada buvo sukurtas žurnalas.

Norėdami nustatyti duomenų bazės žurnalo valymą, atlikite šiuos veiksmus: 

1. Eikite į **Sistemos administravimas > Saitai > Duomenų bazė > Duomenų bazės žurnalas**. Pasirinkite **Valyti žurnalą**.

2. Pasirinkite žurnalų, kuriuos reikia panaikinti, pasirinkimo būdą įvesdami vieną iš šių pasirinkčių:

   - Lentelės ID
   - Žurnalo tipas
   - Sukūrimo data ir laikas

3. Naudokite **Duomenų bazės žurnalo valymas** skirtuką, kad nustatytumėte, kada paleisti žurnalo valymo užduotį. Pagal numatytuosius nustatymus, duomenų bazės žurnalai prieinami 30 dienų.


[!INCLUDE[footer-include](../includes/footer-banner.md)]