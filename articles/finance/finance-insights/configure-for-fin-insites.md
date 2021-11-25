---
title: Finansų įžvalgų konfigūracija
description: Šioje temoje paaiškinami konfigūravimo veiksmai, kuriuos jums atlikus sistema galės naudotis modulio „Finance Insights” galimybėmis.
author: ShivamPandey-msft
ms.date: 1/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 5668d3ddff777645b4f1c6608f025d0c5a63208a
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752983"
---
# <a name="configuration-for-finance-insights"></a>Finansų įžvalgų konfigūracija

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Modulyje „Finance Insights” sujungiamos „Microsoft Dynamics 365 Finance“ ir „Dataverse“, „Azure“ bei „AI Builder“ funkcijos, kad jūsų organizacijai būtų suteikiami galingi prognozavimo įrankiai. Šioje temoje paaiškinami konfigūravimo veiksmai, kuriuos jums atlikus sistema galės naudotis modulio „Finance Insights” galimybėmis. Norėdami sėkmingai atlikti šioje temoje aprašytas procedūras, turite turėti sistemos administratoriaus ir sistemos pritaikymo specialisto prieigą ["Power Portal" administravimo centre](https://admin.powerplatform.microsoft.com/), sistemos administratoriaus prieigą Dynamics 365 Finance ir prieigą prie aplinkos kūrimo Microsoft Dynamics "Lifecycle Services" (LCS).

> [!NOTE]
> Šios "Finance insights" nustatymo procedūros galioja Dynamics 365 Finance 10.0.21 ir naujesnės versijos versijoms.

## <a name="deploy-dynamics-365-finance"></a>„Dynamics 365 Finance“ diegimas

Norėdami talpinti aplinkas, atlikite šiuos veiksmus.

1. LCS sukurkite arba atnaujinkite Dynamics 365 Finance aplinką. Aplinkai reikia 10.0.21 arba naujesnės programos versijos.

    > [!NOTE]
    > Aplinka turi būti didelio prieinamumo (HA) aplinka. (Šis aplinkos tipas dar vadinamas 2 pakopos aplinka.) Norėdami gauti daugiau informacijos, žr. [Aplinkos planavimas](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

2. Jei konfigūruojate "Finance" įžvalgas smėlio dėžės aplinkoje, gali tekti nukopijuoti gamybos duomenis į tą aplinką, kol prognozės veiks. Numatymo modelis naudoja kelių metų duomenis numatymams sukurti. "Contoso" demonstraciniuose duomenyse nėra pakankamai istorinių duomenų, kad būtų galima tinkamai apmokyti prognozės modelį. 

## <a name="configure-dataverse"></a>Konfigūruoti „Dataverse“

Norėdami sukonfigūruoti „Finance insights“, „Dataverse“ atlikite šiuos veiksmus.

- Atidarykite aplinkos puslapį LCS ir patikrinkite, ar **„Power Platform“** integravimo skyrius jau sąranka.

    - Jei jis jau nustatytas, turi „Dataverse“ būti pateiktas su aplinka susietas aplinkos „Finance“ sąrašu.
    - Jei jis dar nenustatytas, pasirinkite **Sąranka**. Aplinkos nustatymas Dataverse gali užtrukti iki valandos. Kai sąranka sėkmingai baigta, Dataverse turėtų būti nurodytas aplinkos pavadinimas, susietas su finansų aplinka.

## <a name="configure-the-finance-insights-add-in"></a>„Finance insights“ konfigūravimas

Jei anksčiau įdiegėte "Finance insights" papildinį, pašalinkite jį prieš atlikdami šią procedūrą.

> [!NOTE]
> Jei jau įdiegėte duomenų ežero priedą LCS, "Finance" įžvalgos jį naudos duomenims, reikalingiems prognozėms, įrašyti. Jei dar neįdiegėte duomenų ežero priedo LCS, "Finance insights" papildinyje bus sukurtas valdomas duomenų ežeras.

Norėdami įdiegti „Finance insights“ priedą, atlikite šiuos veiksmus.

1. Prisijunkite prie LCS, tada dešinėje puslapio pusėje, prie aplinkos pavadinimo pasirinkite **Išsami informacija**.
2. Skyriuje **Aplinkos papildiniai** pasirinkite **Diegti naują papildinį**.
3. RInkitės **„Finance insights“** priedą.
4. Sutikite su sąlygomis, tada pasirinkite **Diegti**.

Papildinio įdiegimas gali užtrukti kelias minutes.

## <a name="one-last-thing"></a>Paskutinis dalykas...

Sėkmingai įdiegus priedą, gali praeiti iki valandos, kol galėsite įgalinti "Finance insights" funkcijas **darbo srityje Funkcijų** Dynamics 365 Finance valdymas. Jei nenorite taip ilgai laukti, galite neautomatiniu būdu paleisti **įžvalgų parengimo būsenos tikrinimo** procesą. 

1. Dalyje Dynamics 365 Finance eikite į **Sistemos administravimo \> sąrankos \> proceso automatizavimas**.
2. Skirtuke **Fono procesai** raskite **įžvalgų parengimo būsenos tikrinimą** ir pasirinkite Redaguoti **·**.
3. Nustatykite **lauką Kitas vykdymas** likus 30 minučių iki dabartinio laiko.

   Šis pakeitimas turėtų priversti **įžvalgų parengimo būsenos tikrinimo** procesą vykdyti nedelsiant.

   Sėkmingai **paleidus įžvalgų parengimo būsenos tikrinimo** procesą, galite įgalinti "Finance insights" funkcijas **darbo srityje Funkcijų** valdymas.

## <a name="feedback-and-support"></a>Atsiliepimai ir palaikymas

Jei norite pateikti atsiliepimą arba jei jums reikia palaikymo, siųskite el. laiškus ["Finance insights" (peržiūra).](mailto:fiap@microsoft.com)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
