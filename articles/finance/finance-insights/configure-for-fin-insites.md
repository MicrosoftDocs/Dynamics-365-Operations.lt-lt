---
title: Finansų įžvalgų konfigūracija
description: Šioje temoje paaiškinami konfigūravimo veiksmai, kuriuos jums atlikus sistema galės naudotis modulio „Finance Insights” galimybėmis.
author: ShivamPandey-msft
ms.date: 01/27/2022
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
ms.openlocfilehash: b9bad6445e9e77688f66c6c4186422d7a898edd7
ms.sourcegitcommit: 7fc0a9a6440ac087292e9e76c26c67f56154b9e6
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/28/2022
ms.locfileid: "8051375"
---
# <a name="configuration-for-finance-insights"></a>Finansų įžvalgų konfigūracija

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

„Finance Insights“ sujungia „Microsoft“ teikiamas funkcijas Dynamics 365 Finance su Dataverse, Azure ir AI Builder teikti galingus prognozavimo įrankius jūsų organizacijai. Šioje temoje paaiškinami konfigūravimo veiksmai, kuriuos jums atlikus sistema galės naudotis modulio „Finance Insights” galimybėmis. Norėdami sėkmingai užbaigti šios temos procedūras, turite turėti sistemos administratoriaus ir sistemos tinkinimo priemonės prieigą [Power Portal administravimo centras](https://admin.powerplatform.microsoft.com/), Sistemos administratoriaus prieiga Dynamics 365 Finance ir prieiga prie aplinkos kūrimo Microsoft Dynamics Gyvenimo ciklo paslaugos (LCS).

> [!NOTE]
> Šios finansų įžvalgų nustatymo procedūros galioja versijoms Dynamics 365 Finance 10.0.21 ir naujesnės versijos.

## <a name="deploy-dynamics-365-finance"></a>„Dynamics 365 Finance“ diegimas

Norėdami talpinti aplinkas, atlikite šiuos veiksmus.

1. LCS sukurkite arba atnaujinkite a Dynamics 365 Finance aplinką. Aplinkai reikalinga programos versija 10.0.21 arba naujesnė.

    > [!NOTE]
    > Aplinka turi būti didelio prieinamumo (HA) aplinka. (Šis aplinkos tipas dar vadinamas 2 pakopos aplinka.) Norėdami gauti daugiau informacijos, žr. [Aplinkos planavimas](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

2. Jei konfigūruojate finansų įžvalgas smėlio dėžės aplinkoje, gali tekti nukopijuoti gamybos duomenis į tą aplinką, kad prognozės veiktų. Numatymo modelis naudoja kelių metų duomenis numatymams sukurti. „Contoso“ demonstraciniuose duomenyse nėra pakankamai istorinių duomenų, kad būtų galima tinkamai parengti numatymo modelį. 

## <a name="configure-your-azure-ad-tenant"></a>Konfigūruokite savo Azure AD nuomininkas

Azure Active Directory(Azure AD) turi būti sukonfigūruotas taip, kad jį būtų galima naudoti su Dataverse ir Microsoft Power Platform programos. Ši konfigūracija reikalauja, kad arba **Projekto savininkas** vaidmenį arba **Aplinkos vadybininkas** vartotojui turi būti priskirtas vaidmuo **Projekto saugumo vaidmuo** lauke LCS.

Patikrinkite, ar baigta ši sąranka:

- Tu turi **Sistemos administratorius** ir **Sistemos tinkinimo priemonė** prieiga prie „Power Portal“ administravimo centro.
- A Dynamics 365 Finance arba lygiavertė licencija taikoma vartotojui, diegiančiam „Finance Insights“ priedą.

Sekantis Azure AD programėlės registruotos Azure AD.

|  Prašymas                             | Programos ID                               |
|------------------------------------------|--------------------------------------|
| „Microsoft Dynamics ERP Microservices CDS“ | „703e2651-d3fc-48f5-942c-74274233dba8“ |
    
## <a name="configure-dataverse"></a>Konfigūruoti „Dataverse“

Norėdami sukonfigūruoti „Finance insights“, „Dataverse“ atlikite šiuos veiksmus.

- Atidarykite aplinkos puslapį LCS ir patikrinkite, ar **„Power Platform“** integravimo skyrius jau sąranka.

    - Jeigu Dataverse jau buvo nustatytas,Dataverse Turėtų būti pateiktas aplinkos pavadinimas, susietas su finansų aplinka.
    - Jeigu Dataverse dar nenustatytas, pasirinkite **Sąranka**. Nustatymas Dataverse aplinka gali užtrukti iki valandos. Sėkmingai užbaigus sąranką,Dataverse turi būti pateiktas aplinkos pavadinimas, su kuriuo susieta Finansų aplinkoje.
    - Jei ši integracija buvo nustatyta naudojant esamą Microsoft Power Platform aplinką, susisiekite su administratoriumi ir įsitikinkite, kad susieta aplinka nėra išjungtos.

        Daugiau informacijos žr [Įjungus Power Platform integracija](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md). 

        Norėdami pasiekti Microsoft Power Platform administratoriaus svetainę, eikite į <https://admin.powerplatform.microsoft.com/environments>.

## <a name="configure-the-finance-insights-add-in"></a>„Finance insights“ konfigūravimas

Jei anksčiau įdiegėte „Finance Insights“ papildinį, pašalinkite jį prieš atlikdami toliau nurodytą procedūrą.

> [!NOTE]
> Jei jau įdiegėte duomenų ežero priedą LCS, „Finance Insights“ naudos jį duomenims, kurių reikia prognozėms, išsaugoti. Jei dar neįdiegėte duomenų ežero papildinio LCS, „Finance Insights“ papildinys sukurs jums valdomą duomenų ežerą.

Norėdami įdiegti „Finance insights“ priedą, atlikite šiuos veiksmus.

1. Prisijunkite prie LCS, tada dešinėje puslapio pusėje, prie aplinkos pavadinimo pasirinkite **Išsami informacija**.
2. Skyriuje **Aplinkos papildiniai** pasirinkite **Diegti naują papildinį**.
3. RInkitės **„Finance insights“** priedą.
4. Sutikite su taisyklėmis ir sąlygomis, tada pasirinkite **Diegti**.

Papildinio įdiegimas gali užtrukti kelias minutes.

## <a name="one-last-thing"></a>Paskutinis dalykas...

Sėkmingai įdiegus priedą, gali praeiti iki valandos, kol galėsite įgalinti finansų įžvalgų funkcijas **Funkcijų valdymas** darbo vieta Dynamics 365 Finance. Jei nenorite tiek laukti, galite rankiniu būdu paleisti **Įžvalgų parengimo būsenos patikrinimas** procesas. 

1. Į Dynamics 365 Finance, eiti į **Sistemos administravimas \> Sąranka \> Procesų automatizavimas**.
2. Ant **Fono procesai** skirtukas, rasti **Įžvalgų parengimo būsenos patikrinimas** ir pasirinkite **Redaguoti**.
3. Nustatyti **Kitas egzekucija** lauke iki 30 minučių prieš dabartinį laiką.

   Šis pakeitimas turėtų priversti **Įžvalgų parengimo būsenos patikrinimas** kad procesas būtų paleistas nedelsiant.

   Po to, kai **Įžvalgų parengimo būsenos patikrinimas** procesas sėkmingai vykdomas, galite įgalinti finansų įžvalgų funkcijas **Funkcijų valdymas** darbo vieta.

> [!NOTE]
> Jei **Įžvalgų parengimo būsenos patikrinimas** procesas nevyksta, eikite į **Sistemos administravimas** > **Paklausimai** > **Paketiniai darbai**. Viduje konors **Procesų automatizavimo apklausų sistema** lauke, pakeiskite reikšmę į **Laukia** pradėti procesą. 
> 
## <a name="feedback-and-support"></a>Atsiliepimai ir palaikymas

Jei norite pateikti atsiliepimą arba jums reikia pagalbos, siųskite el. laišką adresu [Finansų įžvalgos (peržiūra)](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
