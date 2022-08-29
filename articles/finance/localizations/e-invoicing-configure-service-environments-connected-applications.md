---
title: Paslaugų aplinkų ir prijungtų programų konfigūravimas
description: Šiame straipsnyje pateikiama informacija apie tai, kaip konfigūruoti savo aptarnavimo aplinkas ir susijusias programas.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 8ede98cfad685992bad3fb643ea46d6adcb08487
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269538"
---
# <a name="configure-service-environments-and-connected-applications"></a>Paslaugų aplinkų ir prijungtų programų konfigūravimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie tai, kaip konfigūruoti savo aptarnavimo aplinkas ir susijusias programas. Šiame procese yra trys veiksmai. 1 veiksmas yra privalomas, 2 ir 3 žingsniai nėra privalomi.

## <a name="step-1-create-a-service-environment"></a>1 žingsnis: aptarnavimo aplinkos kūrimas

Kurdami savo paslaugų aplinką, nurodykite vartotojų, kurie gali joje įdiegti globalizavimo funkcijas, sąrašą. Pasirinktinai kai kuriems scenarijams nustatykite išorinių programų, kurios gali palaikyti ryšį su elektroninių SF išrašymo tarnyba, sąrašą. Jei jas naudosite savo scenarijuose, nustatykite numeraciją.

Norėdami atlikti šį veiksmą, žr. [tarnybos aplinkas](e-invoicing-service-environments.md).

## <a name="step-2-add-certificates-and-secrets"></a>2 žingsnis: sertifikatų ir paslapčių pridėjimas

Pridėkite nuorodą prie rakto saugyklos Microsoft Azure ir paslapčių, kad jas būtų galima naudoti savo scenarijuose. Šis žingsnis privalomas, jei pardavimo galimybių apdorojimo veiksmai naudoja sertifikatus ir slaptus duomenis skaitmeniniam pasirašymui ar bendravimui su išorinėmis tinklo paslaugomis.

Norėdami atlikti šį veiksmą, žr. [kliento sertifikatus ir paslapytus](e-invoicing-customer-certificates-secrets.md).

## <a name="step-3-configure-connected-applications"></a>3 žingsnis: prijungtų programų konfigūravimas

Norėdami nustatyti "Dynamics 365 Dynamics 365 Supply Chain Management " finansų ar programų ir elektroninių SF išrašymo ryšį, turite sukonfigūruoti finansų arba tiekimo grandinės valdymą, kad būtų galima iškviesti elektroninių SF išrašymo tarnybą ir paruošti verslo duomenis suvienodinta struktūra, kurią galima pakeisti reikiamo elektroninio formato. Programos taip pat turi tinkamai apdoroti tarnybos atsakymus. Šią konfigūraciją galite tiesiogiai užpildyti savo finansų arba tiekimo grandinės valdymo aplinkoje arba galite užbaigti ją reguliavimo konfigūracijos tarnybos (RCS). Jei įjungsite konfigūraciją RCS, galėsite įdiegti ją į savo finansų arba tiekimo grandinės valdymo aplinką. Šiame etape užregistruosite prijungtą programą parametrų diegimui.

Norėdami užbaigti šį veiksmą, žr. [Programos, prijungtos](e-invoicing-connected-applications.md).
