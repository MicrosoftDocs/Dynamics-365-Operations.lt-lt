---
title: Įdiekite priedą, skirtą „Lifecycle Services“ mikro paslaugoms
description: Šiame straipsnyje paaiškinama, kaip įdiegti elektroninių SF išrašymo priedą ciklo Microsoft Dynamics tarnybose (LCS).
author: gionoder
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 938b00192acc0ff5534239f2f280792471181fad
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710814"
---
# <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Įdiekite priedą, skirtą „Lifecycle Services“ mikro paslaugoms

[!include [banner](../includes/banner.md)]

Elektroninių SF išrašymo Microsoft Dynamics tarnybos autentifikavimas reikalauja užregistruoti savo "365 Dynamics 365 Supply Chain Management Microsoft Dynamics " finansus arba aplinką tarnybų platformoje, įdiegdami papildinį savo aplinkai ciklo tarnybose (LCS).

Norėdami užregistruoti aplinką, atlikite šiuos veiksmus.

1. Prisijunkite prie jūsų LCS abonemento.
2. Projekto skelbimų skelbimų srityje pasirinkite LCS projektą.
2. Projekto **Aplinkos** ataskaitų srityje rinkitės savo talpinimo aplinką. Turi būti paleista jūsų pasirinkti aplinka.
3. **Power Platform Skirtuko Integravimas** skyriuje Aplinkos **papildiniai** pasirinkite **Diegti naują priedą**.
4. Rinkitės **SF siuntimas**.
5. **Lauke AAD programos ID** įveskite fiksuotą vertę **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Ši vertė visada fiksuota. Įsitikinkite, kad įvedate tik visuotinai unikalų identifikatorių (GUID). Įtraukite kitus simbolius, pvz., tarpus, kablelius, laikotarpius ar kabutes.
6. Lauke **AAD nuomotojo ID** įveskite savo „Azure” prenumeratos abonemento savininko ID. Jūsų Azure Active Directory nurodytas Azure AD nuomininkas turi būti tas pats nuomininkas, kuris naudojamas reguliavimo konfigūracijos tarnybos (RCS).
7. Peržiūrėkite sąlygas ir sąlygas, tada pažymėkite žymės langelį.
8. Pasirinkti **Diegti**. Po kelių minučių būsena turėtų pasikeisti iš **Diegiama** į **Įdiegta**. Gali tekti atnaujinti puslapį, kad būtų rodomas šis pakeitimas.

Elektroninių SF išrašymas paruoštas naudoti.

> [!NOTE]
> Įmonės paprastai turi kelias finansų arba tiekimo grandinės valdymo aplinkas. Šios aplinkos apima gamybos aplinkas, vartotojo priėmimo ir tikrinimo (UAT) aplinkas ir programavimo (sandbox) aplinkas. Turite pabaigti šią procedūrą visoms aplinkai, prie kurios norite prisijungti prie elektroninių SF išrašymo.
