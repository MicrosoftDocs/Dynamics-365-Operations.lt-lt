---
title: Finansų žinių konfigūracija
description: Šiame straipsnyje paaiškinami konfigūravimo veiksmai, kurie įgalins jūsų sistemą naudoti galimybes, galimas finansų žinių bazėse.
author: ShivamPandey-msft
ms.date: 09/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 05bf5fe5a5ff86bbf52ed58ee6b1e84c15bf2c1e
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573200"
---
# <a name="configuration-for-finance-insights"></a>Finansų žinių konfigūracija

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finansų įžvalgos sujungia funkcijas iš Microsoft Dynamics "365 Finance Dataverse" su "Azure AI Builder " ir teikia galinga prognozės įrankius jūsų organizacijai. Šiame straipsnyje paaiškinami konfigūravimo veiksmai, kurie įgalins jūsų sistemą naudoti galimybes, galimas finansų žinių bazėse. Kad sėkmingai užbaigtumėte šiame straipsnyje nurodytas procedūras, turite turėti prieigą prie sistemos administratoriaus [ir sistemos pritaikymo priemonės "Power Portal](https://admin.powerplatform.microsoft.com/)" administravimo centre, "Dynamics 365 Finance Microsoft Dynamics " sistemos administratoriaus prieigą ir prieigą prie aplinkos kūrimo ciklo tarnybose (LCS).

> [!NOTE]
> Šios finansų žinių nustatymo procedūros taikomos "Dynamics 365" 10.0.21 ir vėlesnės versijos finansų versijoms.

## <a name="deploy-dynamics-365-finance"></a>Diegti "Dynamics 365" finansus

Norėdami talpinti aplinkas, atlikite šiuos veiksmus.

1. LCS sukurkite arba atnaujinkite "Dynamics 365" finansų aplinką. Aplinkai reikia programos 10.0.21 arba naujesnės versijos.

    > [!NOTE]
    > Aplinka turi būti didelio užimtumo (HA) aplinka. (Šis aplinkos tipas dar vadinamas 2 pakopos aplinka.) Norėdami gauti daugiau informacijos, žr. [Aplinkos planavimas](/fin-ops-core/fin-ops/imp-lifecycle/environment-planning).

2. Jei konfigūruojate finansų žinių apdorojimo informaciją sandūrų aplinkoje, prieš numatant gali tekti nukopijuoti gamybos duomenis į tą aplinką. Numatymo modelis naudoja kelių metų duomenis numatymams sukurti. "Contoso" demonstraciniai duomenys neturi pakankamai praeities duomenų, kad būtų galima iš anksto parengti numatymo modelį. 

## <a name="configure-your-azure-ad-tenant"></a>Konfigūruoti savo nuomininką Azure AD

Azure Active Directory(Azure AD) turi būti sukonfigūruota taip, kad ją būtų galima naudoti kartu Dataverse su programomis Microsoft Power Platform. Šiai konfigūracijai reikia, kad **"Project Owner** **·** **·**" vaidmuo arba aplinkos tvarkytuvo vaidmuo būtų priskirtas vartotojui LCS lauke Projekto saugos vaidmuo.

Patikrinkite, ar baigtas šis nustatymas:

- Turite sistemos **administratoriaus ir** sistemos **pritaikymo vartotojo** prieigą maitinimo portalo administravimo centre.
- "Dynamics 365" finansų arba ekvivalentinės licencijos taikoma vartotojui, diegiantiems finansų žinių priedą.
- Šios programėlės Azure AD užregistruotos Azure AD.

    |  Taikymas                             | Programos ID                               |
    |------------------------------------------|--------------------------------------|
    | „Microsoft Dynamics ERP Microservices CDS“ | „703e2651-d3fc-48f5-942c-74274233dba8“ |

    Norėdami patikrinti, ar prašymas užregistruotas Azure AD, patikrinkite **visų prašymų** sąrašą. Daugiau informacijos rasite Peržiūrėkite [įmonės programas](/azure/active-directory/manage-apps/view-applications-portal).
  
    Jei programa neužregistruota, susisiekite su Azure AD palaikymo tarnyba.
  
## <a name="configure-dataverse"></a>Konfigūruoti „Dataverse“

Norėdami sukonfigūruoti „Finance insights“, „Dataverse“ atlikite šiuos veiksmus.

- Atidarykite aplinkos puslapį LCS ir patikrinkite, ar **„Power Platform“** integravimo skyrius jau sąranka.

    - Jei Dataverse jau nustatytas, reikia išvardyti Dataverse aplinkos pavadinimą, susietą su finansų aplinka.
    - Jei Dataverse dar nenustatyta, pasirinkite **Nustatymas**. Aplinkos nustatymas Dataverse gali užtrukti iki valandos. Sėkmingai užbaigus nustatymą, reikia Dataverse išvardyti aplinkos pavadinimą, susietą su finansų aplinka.
    - Jei šis integravimas buvo nustatytas su esama Microsoft Power Platform aplinka, kreipkitės į administratorių, kad įsitikintumėte, jog susieta aplinka nėra išjungtos būsenos.

        Daugiau informacijos rasite Integravimo [įgalinimas Power Platform](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md). 

        Norėdami pasiekti administratoriaus Microsoft Power Platform svetainę, eikite į <https://admin.powerplatform.microsoft.com/environments>.

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

Sėkmingai įdiegus priedą, jis gali užtrukti iki valandos, **kol** galėsite įjungti finansų žinių funkcijas "Dynamics 365" finansų funkcijų valdymo darbo srityje. Jei nenorite laukti taip ilgai, galite rankiniu būdu paleisti žinių parengimo **būsenos tikrinimo** procesą. 

1. Programoje "Dynamics 365 Finance" eikite į sistemos **administravimo nustatymo \> proceso \> automatizavimą**.
2. Skirtuke **Fono procesai** raskite žinių **apsaugos būsenos tikrinkite** ir pasirinkite **Redaguoti**.
3. Nustatykite **kitą vykdymo** lauką 30 minučių prieš dabartinį laiką.

   Šis pakeitimas turi priversti žinių parengimo **būsenos tikrinimo procesą** vykdyti nedelsiant.

   Sėkmingai paleidus **žinių apsaugos būsenos tikrinimo** procesą, galite įgalinti finansų žinių funkcijas funkcijų **valdymo darbo** srityje.

> [!NOTE]
> Jei nepavyksta **paleisti žinių apdorojimo būsenos** tikrinimo proceso, **eikite į sistemos administravimo užklausas** > **paketines** > **užduotis**. Proceso automatizavimo **apklausų sistemos** lauke pakeiskite vertę į Laukiama **,** kol bus inicijuotas procesas. 
> 
## <a name="feedback-and-support"></a>Atsiliepimai ir palaikymas

Jei norite pateikti atsiliepimą arba, jei jums reikia pagalbos, siųskite el. laišką [finansų žinių (peržiūra)](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
