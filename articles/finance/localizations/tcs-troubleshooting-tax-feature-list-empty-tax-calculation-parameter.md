---
title: Tuščias mokesčių priemonių sąrašas mokesčių skaičiavimo parametruose
description: Šioje temoje paaiškinama, kaip spręsti problemą, kai mokesčių funkcijų sąrašas mokesčių skaičiavimo parametrų puslapyje yra tuščias.
author: wangchen
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 5b87499042c9c4bfe76e182b170adf4f1cfeac4b
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/05/2022
ms.locfileid: "8389130"
---
# <a name="empty-tax-feature-list-in-tax-calculation-parameters"></a>Tuščias mokesčių priemonių sąrašas mokesčių skaičiavimo parametruose

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="symptom"></a>Požymis

Paskelbėte reguliavimo konfigūracijos tarnybos (RCS) funkciją, kad ją būtų galima naudoti "Microsoft"Dynamics 365 Finance. Tačiau kai atidarote finansus, **·** \> **·** \> **·** \> **eikite į Mokesčių nustatymo mokesčio konfigūracijos mokesčių skaičiavimo parametrus** ir **pabandykite pasirinkti reikšmę lauke Priemonės nustatymo pavadinimas**, verčių sąrašas yra tuščias.

## <a name="reason"></a>Priežastis

Taip atsitinka todėl, kad jūsų finansų aplinka ir RCS aplinka nėra to paties nuomininko atžvilgiu.

### <a name="rcs-tenant"></a>RCS nuomininkas

Norėdami rasti savo RCS nuomininko ID, atlikite šiuos veiksmus.

1. Kopijuoti visą RCS URL. Pavyzdžiui, URL gali būti `https://rcs-rts-sf-ed22b5aeea8-int-westus2.configure.global.int.dynamics.com/namespaces/817ff7a0-0d77-4aba-9360-3c9749e2c5de/?cmp=dat&mi=RCSFeatureDomainsWorkspace`.
2. Atidarykite InPrivate naršyklės langą, į adresų juostą įklijuokite RCS URL ir pasirinkite **Įvesti**. Jus nukreipia į prisijungimo puslapį, kur galima rasti RCS nuomininkų ID. Pavyzdžiui, jei prisijungimo puslapio `https://login.microsoftonline.com/d335a570-a05b-4bc5-8eb3-c42c65f9560d` URL yra, nuomininko ID yra informacija, kuri rodoma po `https://login.microsoftonline.com/`**d335a570-a05b-4bc5-8eb3-c42c65f9560d** ar.

### <a name="finance-environment-tenant-id"></a>Finansinės aplinkos nuomininko ID

Norėdami surasti savo finansų aplinkos nuomininkų ID, atlikite tuos pačius veiksmus, kuriuos ėjote norėdami surasti RCS nuomininką. Tačiau nukopijuokite ir įklijuokite visą savo finansų aplinkos URL, o ne visą RCS URL.

## <a name="resolution"></a>Paaiškinimas

Jei skiriasi dviejų nuomininkų ID, susiduriate su šioje temoje aprašoma problema. Jei jie vienodi, susiduriate su nesusijusia problema. Tokiu atveju rekomenduojame kreiptis į "Microsoft" palaikymo tarnybą.

### <a name="solution-1"></a>1 sprendimas

Pasirašykite savo RCS aplinką prie to paties nuomininko, kuriame yra prisiregistravę prie jūsų finansų aplinkos. Tada sukurkite ir publikuokite mokesčių priemonę.

### <a name="solution-2"></a>2 sprendimas

Bendrai naudoti mokesčių funkciją su finansų nuomininku RCS.

1. RCS eikite į globalizavimo **priemonių mokesčių** \> **skaičiavimą.**
2. Pasirinkite bendro naudojimo funkciją, tada skirtuke **Organizacijos** pasirinkite Bendrai **naudoti**.
3. Lauke Organizacijos **domeno** pavadinimas įveskite pavadinimą. Pavyzdžiui, įveskite **contoso.onmicrosoft.com**.
4. Pasirinkite **Bendrinti**.

![Bendrai naudoti su išorinės organizacijos išplečiamuoju dialogo langu.](media/ShareTaxFeature.png)
