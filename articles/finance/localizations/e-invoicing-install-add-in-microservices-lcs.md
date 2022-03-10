---
title: Diekite priedą mikro paslaugoms „Lifecycle Services“
description: Šioje temoje paaiškinama, kaip įdiegti elektroninių SF išrašymo priedą ciklo Microsoft Dynamics tarnybose (LCS).
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a575f3e26489607dc2143ba05c941240969a0feb
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371972"
---
# <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Diekite priedą mikro paslaugoms „Lifecycle Services“

[!include [banner](../includes/banner.md)]

Elektroninių SF išrašymo tarnybos autentifikavimas reikalauja, kad "Microsoft Dynamics 365 Finance Dynamics 365 Supply Chain Management " arba aplinka būtų užregistruojama tarnybų platformoje Microsoft Dynamics, diegiant aplinkos priedą ciklo tarnybose (LCS).

Norėdami užregistruoti aplinką, atlikite šiuos veiksmus.

1. Prisijunkite prie jūsų LCS abonemento.
2. Projekto skelbimų skelbimų srityje pasirinkite LCS projektą.
2. Projekto **Aplinkos** ataskaitų srityje rinkitės savo talpinimo aplinką. Turi būti paleista jūsų pasirinkti aplinka.
3. **Power Platform Skirtuko Integravimas** skyriuje Aplinkos **papildiniai** pasirinkite **Diegti naują priedą**.
4. Rinkitės **SF siuntimas**.
5. Lauke **AAD programos ID** įveskite **„091c98b0-a1c9-4b02-b62c-7753395ccabe**. Ši vertė yra fiksuota vertė. Įsitikinkite, kad įvedate tik visuotinai unikalų identifikatorių (GUID). Įtraukite kitus simbolius, pvz., tarpus, kablelius, laikotarpius ar kabutes.
6. Lauke **AAD nuomotojo ID** įveskite savo „Azure” prenumeratos abonemento savininko ID. Jūsų Azure Active Directory nurodytas Azure AD nuomininkas turi būti tas pats nuomininkas, kuris naudojamas reguliavimo konfigūracijos tarnybos (RCS).
7. Peržiūrėkite sąlygas ir sąlygas, tada pažymėkite žymės langelį.
8. Pasirinkti **Diegti**. Po kelių minučių būsena turėtų pasikeisti iš **Diegiama** į **Įdiegta**. Gali tekti atnaujinti puslapį, kad būtų rodomas šis pakeitimas.

Elektroninių SF išrašymas paruoštas naudoti.

> [!NOTE]
> Įmonės paprastai turi kelias finansų arba tiekimo grandinės valdymo aplinkas. Šios aplinkos apima gamybos aplinkas, vartotojo priėmimo ir tikrinimo (UAT) aplinkas ir programavimo (sandbox) aplinkas. Turite pabaigti šią procedūrą visoms aplinkai, prie kurios norite prisijungti prie elektroninių SF išrašymo.
