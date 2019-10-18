---
title: Duomenų integravimo trikčių šalinimo vadovas
description: Šioje temoje pateikiama duomenų integravimo tarp „Finance and Operations“ programų ir „Common Data Service” trikčių šalinimo informacija.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: c16268338085d414468f17362294fb7e933d1b57
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249114"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Duomenų integravimo trikčių šalinimo vadovas

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a>Įjunkite priedo sekimo žurnalus programoje „Common Data Service“ ir patikrinkite dvigubo rašymo priedo klaidų išsamią informaciją

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Jei atlikdami dvigubo rašymo sinchronizavimą susiduriate su problema arba klaida, atlikite šiuos veiksmus, kad patikrintumėte klaidas sekimo žurnale.

1. Prieš tikrindami klaidas, turite įjungti priedo sekimo žurnalus. Instrukcijas rasite vadovo [Mokymo priemonė: įrašykite ir užregistruokite priedą](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) skyriuje „Sekimo žurnalų peržiūrėjimas“.

    Dabar galite tikrinti klaidas.

2. Prisijunkite prie „Microsoft Dynamics 365 Sales“.
3. Pasirinkite mygtuką **Parametrai** (krumpliaračio simbolis) ir pasirinkite **Išplėstiniai parametrai**.
4. Meniu **Parametrai** pasirinkite **Tinkinimas\> Priedo sekimo žurnalas**.
5. Pasirinkite **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** kaip tipo pavadinimą, kad būtų rodoma išsami klaidos informacija.

## <a name="inspect-dual-write-synchronization-errors"></a>Tikrinti dvigubo rašymo sinchronizavimo klaidas

Atlikite šiuos veiksmus, kad galėtumėte tikrinti klaidas per testavimą.

1. Prisijunkite prie „Microsoft Dynamics“ portale „Lifecycle Services“ (LCS).
2. Atidarykite LCS projektą, kad atliktumėte dvigubo rašymo testavimą.
3. Pasirinkite **Aplinkos diegimo debesyje įrankis**.
4. Sukurkite nuotolinį darbalaukį, skirtą programos virtualiajai mašinai (VM), pasinaudoję LCS rodoma vietine paskyra.
5. Atidarykite įvykių peržiūros programą. 
6. Eikite į **Programų ir paslaugų žurnalai\> „Microsoft“\> „Dynamics“\> „AX-DualWriteSync“\> Veikia** Rodomos klaidos ir išsami informacija.

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a>Atsiekite vieną „Common Data Service“ aplinką nuo programos ir susiekite kitą aplinką.

Norėdami atnaujinti saitus atlikite toliau nurodytus veiksmus.

1. Eikite į programos aplinką.
2. Atidarykite duomenų valdymą.
3. Pasirinkite **Programėlių CDS saitas**.
4. Pasirinkite visus vykdomus susiejimus ir tada pasirinkite **Stabdyti**.
5. Pasirinkite visus susiejimus ir tada pasirinkite **Naikinti**.

    > [!NOTE]
    > Parinktis **Naikinti** nepasiekiama, jei pasirinktas **„CustomerV3-Account“** šablonas. Išvalykite šio šablono žymėjimą, kaip nurodyta. **„CustomerV3-Account“** yra senesnis sukonfigūruotas šablonas ir veikia su potencialių grynųjų pinigų sprendimu. Jis rodomas visuose šablonuose, nes buvo išleistas visose šalyse.

6. Pasirinkite **Atsieti aplinką**.
7. Kad patvirtintumėte operaciją, pasirinkite **Taip**.
8. Norėdami susieti naują aplinką, vykdykite [diegimo vadove](https://aka.ms/dualwrite-docs)nurodytus veiksmus.
