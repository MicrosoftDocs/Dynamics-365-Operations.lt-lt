---
title: Dynamics 365 Finance ir Dynamics 365 Supply Chain Management JAV vyriausybės bendruomenės debesyje (GCC)
description: Šioje temoje pateikiama informacija Microsoft Dynamics apie 365 JAV vyriausybės produktus, kuriuos gali naudoti reikalavimus atitinkanti vyriausybė ir juridiniai subjektai.
author: hasaid
ms.date: 11/12/2021
ms.topic: article
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2021-11-09
ms.openlocfilehash: 17702ada5bf75a44652e194c2555a83e76e7a36b
ms.sourcegitcommit: 9f8da0ae3dcf3861e8ece2c2df4f693490563d5e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2021
ms.locfileid: "7817470"
---
# <a name="dynamics-365-finance-and-dynamics-365-supply-chain-management-in-us-government-community-cloud-gcc"></a>Dynamics 365 Finance ir Dynamics 365 Supply Chain Management JAV vyriausybės bendruomenės debesyje (GCC)

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Pasirinkite Microsoft Dynamics 365 Jungtinių Valstijų (JAV) vyriausybės produktus gali naudoti reikalavimus atitinkanti vyriausybė ir juridiniai subjektai. Šie objektai apribojami šiais tipais:

- JAV federaliniai, valstijos, vietos, tribalinės ir teritoriniai vyriausybės subjektai
- Privačios objektai, naudojantys "Dynamics 365" JAV vyriausybę, siekiant pateikti sprendimus vyriausybės subjektams arba kvalifikuotų debesies bendruomenės nariams
- Juridiniai subjektai, kurie turi klientų duomenis, kuriems taikomi vyriausybės įstatymai, o "Dynamics 365" JAV vyriausybė yra tinkama tarnyba, kuri atitinka reguliavimo reikalavimus

Daugiau informacijos ieškokite ["Dynamics 365" JAV vyriausybė](/power-platform/admin/microsoft-dynamics-365-government).

## <a name="onboarding"></a>Onboarding

Norėdami baigti diegimo projekto inicialų nurodymą vykdymo ciklo tarnybose (LCS), vadovaukitės diegimo projekto Microsoft Dynamics [instrukcijomis](../../../fin-ops-core/fin-ops/imp-lifecycle/onboard.md). Tačiau nenaudokite nuorodos į viešąjį LCS, kuris pateikiamas tose instrukcijose. Tokiu atveju naudokite toliau nurodytą URL, norėdami atidaryti LCS, skirtas JAV vyriausybės bendruomenės debesyje (GCC): <https://gov.lcs.microsoftdynamics.us>

Užbaigę inicialų nurodymą, vadovaukitės projekto [...](../lifecycle-services/project-onboarding.md) nurodymu. Dar kartą naudokite [GCC LCS,](https://gov.lcs.microsoftdynamics.us) o ne viešąjį LCS.

## <a name="environment-deployment"></a>Aplinkos diegimas

Užbaigę projekto įsk. galite peržiūrėti papildomas LCS galimybes, kurios aprašomos vykdymo ciklo tarnybose [(LCS), Finance and Operations skirtose programėlių](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md) klientams. Tada pereiti prie aplinkos diegimo.

- Norėdami diegti "Microsoft" valdomas aplinkas naudodami LCS, vadovaukitės programų klientų [naudojimo ciklo tarnybose (LCS) Finance and Operations pateiktomis](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md#new-deployment-experience) instrukcijomis.
- Daugiau informacijos apie debesyje nuomojamas aplinkas [žr. Deploy ir access development](../../../fin-ops-core/dev-itpro/dev-tools/access-instances.md) environments. Taip pat turite užbaigti savo jungčių išteklių tvarkytuvo diegimo procesą, kaip aprašyta "Azure" išteklių vadovo paslaugų planavimo procese, skirtame JAV vyriausybės ciklo [tarnybų](arm-onbarding-us-goverment.md) projektams.

> [!NOTE]
> JAV vyriausybės LCS projektuose palaikomi tik "Azure" vyriausybės palaikomi tik "Azure" vyriausybės abonementai.

## <a name="features-that-arent-available"></a>Funkcijos, kurių nėra

Kai kurios funkcijos nebus galimos diegti GCC arba jų nebus galima naudoti su "Dynamics 365" GCC. Pvz., Azure DevOps GCC paslaugos nebus galimos. Tačiau gali būti naudojamos Azure DevOps vietinės arba Azure DevOps viešos paslaugos. Išsamesnės informacijos apie priemonių prieinamumą žr. [verslo programų JAV vyriausybės priemonių](https://aka.ms/BAPFunctionalParity) prieinamumą.

## <a name="frequently-asked-questions"></a>Dažniausiai užduodami klausimai

### <a name="are-dynamics-365-finance-and-dynamics-365-supply-chain-management-supported-in-gcc-high"></a>Ar Dynamics 365 Finance Dynamics 365 Supply Chain Management GCC-High palaikomos ir palaikomos?

Ne. Dynamics 365 Finance ir Dynamics 365 Supply Chain Management palaikomos tik GCC.

### <a name="can-i-use-public-azure-devops-with-finance-and-supply-chain-management-in-gcc"></a>Ar aš norėčiau naudoti Azure DevOps viešąją su finansų ir tiekimo grandinės valdymu GCC?

Taip, galite naudotis viešomis paslaugomis, jei neturite reikalavimų dėl sprendimo, kurį patvirtino federalinių rizikos ir autorizavimo Azure DevOps valdymo programa (FEDRAMP). Taip pat galite naudoti Azure DevOps serverį.

### <a name="can-i-deploy-a-cloud-hosted-environment-tier-1-development-environment-on-an-azure-commercial-subscription"></a>Ar "Azure" komerciniame abonemente galima įdiegti debesyje nuomojamą "Tier-1" programavimo aplinką?

Ne. [LCS, skirtame](https://gov.lcs.microsoftdynamics.us) GCC, turite naudoti "Azure" vyriausybės abonementą norėdami įdiegti "Azure" nuomojamą aplinką debesyje.

### <a name="what-can-i-do-if-i-need-a-package-from-the-shared-asset-library-but-it-isnt-available-in-lcs-for-gcc"></a>Ką daryti, jei reikia paketo iš bendrai naudojamų turtų bibliotekos, bet jo nėra LCS, skirtame GCC?

Tą patį paketą galite atsisiųsti iš viešose [LCS naudojamos bendrai naudojamo turto](https://lcs.dynamics.com) bibliotekos. Taip pat jūsų partneris gali padėti atsisiųsti paketą.

### <a name="is-the-code-upgrade-tool-available-in-gcc"></a>Ar kodo atnaujinimo įrankį galima naudoti GCC?

Ne, kodo atnaujinimo įrankio šiuo metu GCC nėra. Tačiau galite sukurti potencialaus kliento projektą [viešajame LCS](https://lcs.dynamics.com) ir naudoti kodo naujinimo įrankį. Atkreipkite dėmesį, kad negalėsite įdiegti aplinkos potencialių klientų projektuose.

### <a name="can-my-partner-open-a-support-ticket-on-my-behalf"></a>Ar mano partneris gali atidaryti palaikymo bilietą mano vardu?

Taip. Tačiau, jei jūsų partneris naudoja ne GCC tapatybę, palaikymo bilietas bus nukreiptas į viešąją palaikymo eilę. Rekomenduojame LCS naudoti kliento GCC teisę atidaryti palaikymo bilietus.

## <a name="see-also"></a>Taip pat žiūrėkite

- ["Dynamics 365" JAV vyriausybė](/power-platform/admin/microsoft-dynamics-365-government)
- [Verslo programų JAV vyriausybės priemonių](https://aka.ms/BAPFunctionalParity) pasiekiamumas.
- [„Lifecycle Services“ (LCS) vartotojo vadovas](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Visuotinio debesies diegimo apžvalga](../../../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
