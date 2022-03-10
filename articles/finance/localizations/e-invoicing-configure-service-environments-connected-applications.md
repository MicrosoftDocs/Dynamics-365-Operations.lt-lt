---
title: Konfigūruoti paslaugų aplinkas ir prijungtas programas
description: Šioje temoje pateikiama informacija apie tai, kaip konfigūruoti jūsų aptarnavimo aplinkas ir susijusias programas.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c3366e75b4a6d3f33a1aac9e444236d9ae57c829
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371918"
---
# <a name="configure-service-environments-and-connected-applications"></a>Konfigūruoti paslaugų aplinkas ir prijungtas programas

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie tai, kaip konfigūruoti jūsų aptarnavimo aplinkas ir susijusias programas. Šiame procese yra trys veiksmai. 1 veiksmas yra privalomas, 2 ir 3 žingsniai nėra privalomi.

## <a name="step-1-create-a-service-environment"></a>1 žingsnis: aptarnavimo aplinkos kūrimas

Kurdami savo paslaugų aplinką, nurodykite vartotojų, kurie gali joje įdiegti globalizavimo funkcijas, sąrašą. Pasirinktinai kai kuriems scenarijams nustatykite išorinių programų, kurios gali palaikyti ryšį su elektroninių SF išrašymo tarnyba, sąrašą. Jei jas naudosite savo scenarijuose, nustatykite numeraciją.

Norėdami atlikti šį veiksmą, žr. [tarnybos aplinkas](e-invoicing-service-environments.md).

## <a name="step-2-add-certificates-and-secrets"></a>2 žingsnis: sertifikatų ir paslapčių pridėjimas

Pridėkite nuorodą prie rakto saugyklos Microsoft Azure ir paslapčių, kad jas būtų galima naudoti savo scenarijuose. Šis žingsnis privalomas, jei pardavimo galimybių apdorojimo veiksmai naudoja sertifikatus ir slaptus duomenis skaitmeniniam pasirašymui ar bendravimui su išorinėmis tinklo paslaugomis.

Norėdami atlikti šį veiksmą, žr. [kliento sertifikatus ir paslapytus](e-invoicing-customer-certificates-secrets.md).

## <a name="step-3-configure-connected-applications"></a>3 žingsnis: prijungtų programų konfigūravimas

Norėdami nustatyti Dynamics 365 Finance Dynamics 365 Supply Chain Management ryšį tarp programų ir elektroninių SF išrašymo, turite sukonfigūruoti finansų arba tiekimo grandinės valdymą, kad iškvietimas būtų skirtas elektroninių SF išrašymo paslaugai kurti ir paruošti verslo duomenis suvienodinta struktūra, kurią galima pakeisti reikiamo elektroninio formato. Programos taip pat turi tinkamai apdoroti tarnybos atsakymus. Šią konfigūraciją galite tiesiogiai užpildyti savo finansų arba tiekimo grandinės valdymo aplinkoje arba galite užbaigti ją reguliavimo konfigūracijos tarnybos (RCS). Jei įjungsite konfigūraciją RCS, galėsite įdiegti ją į savo finansų arba tiekimo grandinės valdymo aplinką. Šiame etape užregistruosite prijungtą programą parametrų diegimui.

Norėdami užbaigti šį veiksmą, žr. [Programos, prijungtos](e-invoicing-connected-applications.md).
