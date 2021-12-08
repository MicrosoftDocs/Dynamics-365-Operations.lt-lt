---
title: Finansų žinių konfigūracija
description: Šioje temoje paaiškinami konfigūravimo veiksmai, kuriuos jums atlikus sistema galės naudotis modulio „Finance Insights” galimybėmis.
author: ShivamPandey-msft
ms.date: 11/19/2021
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
ms.openlocfilehash: 6183e8a7500e9deff0ebf6b5dec8842ad4ca94cb
ms.sourcegitcommit: 6a9f068b59b62c95a507d1cc18b23f9fd80a859b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/20/2021
ms.locfileid: "7827033"
---
# <a name="configuration-for-finance-insights"></a>Finansų žinių konfigūracija

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Modulyje „Finance Insights” sujungiamos „Microsoft Dynamics 365 Finance“ ir „Dataverse“, „Azure“ bei „AI Builder“ funkcijos, kad jūsų organizacijai būtų suteikiami galingi prognozavimo įrankiai. Šioje temoje paaiškinami konfigūravimo veiksmai, kuriuos jums atlikus sistema galės naudotis modulio „Finance Insights” galimybėmis. Kad būtų sėkmingai užbaigtos šios temos procedūros, turite turėti sistemos administratoriaus ir sistemos pritaikymo priemonės prieigą ["Power Portal" administravimo centre](https://admin.powerplatform.microsoft.com/), sistemos administratoriaus prieigą ir prieigą prie aplinkos kūrimo ciklo tarnyboseDynamics 365 Finance Microsoft Dynamics (LCS).

> [!NOTE]
> Šios finansų žinių nustatymo procedūros taikomos Dynamics 365 Finance 10.0.21 ir vėlesnės versijos versijoms.

## <a name="deploy-dynamics-365-finance"></a>„Dynamics 365 Finance“ diegimas

Norėdami talpinti aplinkas, atlikite šiuos veiksmus.

1. LCS sukurkite arba atnaujinkite Dynamics 365 Finance aplinką. Aplinkai reikia programos 10.0.21 arba naujesnės versijos.

    > [!NOTE]
    > Aplinka turi būti didelio užimtumo (HA) aplinka. (Šis aplinkos tipas dar vadinamas 2 pakopos aplinka.) Norėdami gauti daugiau informacijos, žr. [Aplinkos planavimas](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

2. Jei konfigūruojate finansų žinių apdorojimo informaciją sandūrų aplinkoje, prieš numatant gali tekti nukopijuoti gamybos duomenis į tą aplinką. Numatymo modelis naudoja kelių metų duomenis numatymams sukurti. "Contoso" demonstraciniai duomenys neturi pakankamai praeities duomenų, kad būtų galima iš anksto parengti numatymo modelį. 

## <a name="configure-your-azure-ad-tenant"></a>Konfigūruoti savo Azure AD nuomininką

Azure Active Directory(Azure AD) turi būti sukonfigūruota taip, kad ją būtų galima naudoti kartu su Dataverse Microsoft Power Platform programomis. Šiai konfigūracijai reikia, kad "Project Owner" vaidmuo arba aplinkos tvarkytuvo vaidmuo būtų priskirtas **vartotojui** **·** **LCS** lauke Projekto saugos vaidmuo.

Patikrinkite, ar baigtas šis nustatymas:

- Turite sistemos **administratoriaus** ir sistemos **pritaikymo vartotojo prieigą maitinimo** portalo administravimo centre.
- Vartotojui, diegiantiems finansų žinių Dynamics 365 Finance priedą, taikoma arba ekvivalentinė licencija.

Šios Azure AD programėlės Azure AD užregistruotos.

|  Prašymas                             | Programos ID                               |
|------------------------------------------|--------------------------------------|
| „Microsoft Dynamics ERP Microservices CDS“ | „703e2651-d3fc-48f5-942c-74274233dba8“ |
    
## <a name="configure-dataverse"></a>Konfigūruoti „Dataverse“

Norėdami sukonfigūruoti „Finance insights“, „Dataverse“ atlikite šiuos veiksmus.

- Atidarykite aplinkos puslapį LCS ir patikrinkite, ar **„Power Platform“** integravimo skyrius jau sąranka.

    - Jei Dataverse jau nustatytas, reikia išvardyti aplinkos pavadinimą, susietą su Dataverse finansų aplinka.
    - Jei Dataverse dar nenustatyta, pasirinkite **Nustatymas**. Aplinkos nustatymas Dataverse gali užtrukti iki valandos. Sėkmingai užbaigus nustatymą, reikia Dataverse išvardyti aplinkos pavadinimą, susietą su finansų aplinka.
    - Jei šis integravimas buvo nustatytas su esama aplinka, kreipkitės į administratorių, kad įsitikintumėte, jog susieta aplinka nėra Microsoft Power Platform išjungtos būsenos.

        Daugiau informacijos rasite Integravimo [Power Platform](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md) įgalinimas. 

        Norėdami pasiekti Microsoft Power Platform administratoriaus svetainę, eikite <https://admin.powerplatform.microsoft.com/environments> į.

## <a name="configure-the-finance-insights-add-in"></a>„Finance insights“ konfigūravimas

Jei anksčiau įdiegėte finansų žinių priedą, pašalinkite jį prieš pradėdami nurodytą procedūrą.

> [!NOTE]
> Jei jau įdiegėte duomenų į LCS, finansų įžvalgos jį naudos, kad įrašytumėte numatymams reikalingus duomenis. Jei dar neįdiegsite duomenų į LCS, finansų įžvalgų duomenų priedas jums sukurs valdomų duomenų tipą.

Norėdami įdiegti „Finance insights“ priedą, atlikite šiuos veiksmus.

1. Prisijunkite prie LCS, tada dešinėje puslapio pusėje, prie aplinkos pavadinimo pasirinkite **Išsami informacija**.
2. Skyriuje **Aplinkos papildiniai** pasirinkite **Diegti naują papildinį**.
3. RInkitės **„Finance insights“** priedą.
4. Sutikite su sąlygomis ir pasirinkite **Diegti**.

Papildinio įdiegimas gali užtrukti kelias minutes.

## <a name="one-last-thing"></a>Vienas paskutinis...

Sėkmingai įdiegus priedą, jis gali užtrukti iki valandos, kol galėsite įgalinti finansų žinių funkcijas funkcijų **valdymo** darbo Dynamics 365 Finance srityje. Jei nenorite laukti taip ilgai, galite rankiniu būdu paleisti žinių **parengimo būsenos tikrinimo** procesą. 

1. Įeikite Dynamics 365 Finance į sistemos administravimo nustatymo proceso **\>\> automatizavimą.**
2. Skirtuke **Fono** procesai raskite žinių apsaugos būsenos **tikrinkite** ir pasirinkite **Redaguoti**.
3. Nustatykite **kitą** vykdymo lauką 30 minučių prieš dabartinį laiką.

   Šis pakeitimas turi priversti **žinių parengimo būsenos tikrinimo procesą** vykdyti nedelsiant.

   Sėkmingai paleidus žinių apsaugos būsenos tikrinimo procesą, galite įgalinti finansų žinių funkcijas **funkcijų** valdymo darbo **srityje**.

## <a name="feedback-and-support"></a>Atsiliepimai ir palaikymas

Jei norite pateikti atsiliepimą arba, jei jums reikia pagalbos, siųskite el. laišką finansų [įžvalgoms (peržiūra)](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
