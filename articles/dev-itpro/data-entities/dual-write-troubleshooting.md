---
title: Duomenų integravimo trikčių šalinimo vadovas
description: Šioje temoje pateikiama trikčių šalinimo informacija apie duomenų integravimą tarp „Microsoft Dynamics 365 for Finance and Operations“ ir „Common Data Service“.
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
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797280"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Duomenų integravimo trikčių šalinimo vadovas

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a>Įjunkite priedo sekimą programoje „Common Data Service“ ir patikrinkite dvigubo rašymo priedo klaidos informaciją.

Jei susiduriate su problema ar klaida atlikdami dvigubo rašymo sinchronizavimą, galite patikrinti klaidas sekimo žurnale:

1. Prieš galėdami patikrinti klaidas, turite įjungti priedo sekimą naudodamiesi instrukcijomis, pateiktomis dalyje [Register plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs), kad įjungtumėte priedo sekimą. Dabar galite patikrinti klaidas.
2. Prisijungti prie „Dynamics 365 for Sales‟
3. Spustelėkite nustatymų piktogramą (pavara) ir pasirinkite **„Išplėstiniai parametrai“**.
4. Meniu **„Parametrai“** pasirinkite **„Tinkinimas“ > „Priedo sekimo žurnalas“**
5. Spustelėkite tipo pavadinimą **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**, kad būtų rodoma išsami klaidos informacija.

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a>Patikrinkite „Finance and Operations“ dvigubo rašymo sinchronizavimo klaidas

Atlikdami toliau nurodytus veiksmus galite patikrinti klaidas per testavimą:

+ Prisijunkite prie „LifeCycle Services“ (LCS).
+ Atidarykite LCS projektą, kurį pasirinkote dvigubo rašymo testavimui atlikti.
+ Eikite į debesies nuomojamas aplinkas.
+ Prisijunkite prie „Finance and Operations“ VM nuotolinio darbalaukio naudodami vietinį abonementą, kuris rodomas LCS.
+ Atidarykite įvykio peržiūrą. 
+ Pereikite į **„Programų ir paslaugų žurnalai“ > „Microsoft“ > „Dynamics“ > „AX-DualWriteSync“ > „Operacinis“**. Rodomos klaidos ir išsami informacija.

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a>Kaip atsieti ir susieti kitą „Common Data Service“ aplinką iš „Finance and Operations“

Saitus galite naujinti atlikdami šiuos veiksmus:

+ Pereikite į „Finance and Operations“ aplinką.
+ Atidarykite duomenų valdymą.
+ Paspauskite **„Susieti su CDS, skirtu programoms**.
+ Pasirinkite visus veikiančius susiejimus ir spustelėkite **„Stabdyti“**. 
+ Pasirinkite visus susiejimus ir spustelėkite **„Naikinti“**.

    > [!NOTE]
    > Parinktis **„Naikinti“** nebus rodoma, jei pasirinktas **„CustomerV3-Account“** šablonas. Jei reikia, atžymėkite. **„CustomerV3-Account“** yra senesnis sukonfigūruotas šablonas ir veikia su potencialių grynųjų pinigų sprendimu. Kadangi jis yra išleistasvisame pasaulyje, jis rodomas po visais šablonais.

+ Spustelėkite **„Atsieti aplinką“**.
+ Spustelėkite **Yes**, kad patvirtintumėte.
+ Norėdami susieti naują aplinką, vykdykite [diegimo vadove](https://aka.ms/dualwrite-docs)nurodytus veiksmus.

