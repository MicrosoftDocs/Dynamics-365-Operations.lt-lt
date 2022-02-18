---
title: Dynamics 365 Finance ir Dynamics 365 Supply Chain Management JAV vyriausybės bendruomenės debesyje (GCC)
description: Šioje temoje pateikiama informacija apie Microsoft Dynamics 365 JAV vyriausybės produktai, prieinami kvalifikuotoms vyriausybės ir privatiems subjektams.
author: hasaid
ms.date: 11/12/2021
ms.topic: article
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2021-11-09
ms.openlocfilehash: 0c8b88e5d190f6dc9beb9342909d1e489d4af10b
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062291"
---
# <a name="dynamics-365-finance-and-dynamics-365-supply-chain-management-in-us-government-community-cloud-gcc"></a>Dynamics 365 Finance ir Dynamics 365 Supply Chain Management JAV vyriausybės bendruomenės debesyje (GCC)

[!include [banner](../includes/banner.md)]



Pasirinkite Microsoft Dynamics 365 Jungtinių Valstijų (JAV) vyriausybės produktai yra prieinami kvalifikuotiems vyriausybės ir privatiems subjektams. Šie subjektai yra tik šių tipų:

- JAV federalinės, valstijos, vietos, genčių ir teritorinės vyriausybės subjektai
- Privatūs subjektai, kurie naudoja „Dynamics 365 US Government“, kad teiktų sprendimus vyriausybės subjektams arba kvalifikuotiems debesų bendruomenės nariams
- Privatūs subjektai, turintys klientų duomenis, kuriems taikomi vyriausybės teisės aktai, ir „Dynamics 365 US Government“ yra tinkama paslauga, atitinkanti reguliavimo reikalavimus.

Norėdami gauti informacijos, žr [„Dynamics 365“ JAV vyriausybė](/power-platform/admin/microsoft-dynamics-365-government).

## <a name="onboarding"></a>Onboarding

Norėdami užbaigti pradinį prisijungimą prie įgyvendinimo projekto Microsoft Dynamics Lifecycle Services (LCS), vadovaukitės instrukcijomis [Įgyvendinimo projekto dalis](../../../fin-ops-core/fin-ops/imp-lifecycle/onboard.md). Tačiau nenaudokite nuorodos į viešą LCS, pateiktą šiose instrukcijose. Vietoj to naudokite šį URL, kad atidarytumėte LCS, skirtą JAV vyriausybės bendruomenės debesiui (GCC):<https://gov.lcs.microsoftdynamics.us>.

Baigę pradinį prisijungimą, vadovaukitės instrukcijomis [Projekto įtraukimas](../lifecycle-services/project-onboarding.md). Dar kartą naudokite [LCS skirta GCC](https://gov.lcs.microsoftdynamics.us) vietoj viešųjų LCS.

## <a name="environment-deployment"></a>Aplinkos diegimas

Baigę projekto parengimą, galite peržiūrėti papildomas LCS galimybes, kurios aprašytos [„Finance and Operations“ programų klientams skirtos gyvavimo ciklo paslaugos (LCS).](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md). Tada pereikite prie aplinkos diegimo.

- Norėdami įdiegti „Microsoft“ valdomas aplinkas per LCS, vadovaukitės instrukcijomis [„Finance and Operations“ programų klientams skirtos gyvavimo ciklo paslaugos (LCS).](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md#new-deployment-experience).
- Apie debesyje priglobtas aplinkas žr [Diegti ir pasiekti kūrimo aplinkas](../../../fin-ops-core/dev-itpro/dev-tools/access-instances.md). Taip pat turite užbaigti Resource Manager įtraukimo į savo jungtis procesą, kaip aprašyta [Užbaikite „Azure Resource Manager“ įtraukimo į JAV vyriausybės gyvavimo ciklo paslaugų projektus procesą](arm-onbarding-us-goverment.md).

> [!NOTE]
> JAV vyriausybės LCS projektuose palaikomos tik „Azure Government“ specifinės „Azure“ prenumeratos.

## <a name="features-that-arent-available"></a>Funkcijos, kurių nėra

Kai kurių funkcijų nebus galima įdiegti GCC arba jų nebus galima naudoti su „Dynamics 365“ GCC. Pavyzdžiui,Azure DevOps Paslaugos nebus teikiamos GCC. Tačiau vietoje Azure DevOps arba viešas Azure DevOps paslaugomis galima naudotis. Norėdami gauti daugiau informacijos apie funkcijų prieinamumą, žr [Verslo programos JAV vyriausybės funkcijos prieinamumas](https://aka.ms/BAPFunctionalParity).

## <a name="frequently-asked-questions"></a>Dažniausiai užduodami klausimai

### <a name="are-dynamics-365-finance-and-dynamics-365-supply-chain-management-supported-in-gcc-high"></a>Yra Dynamics 365 Finance ir Dynamics 365 Supply Chain Management palaikoma GCC-High?

Ne. Dynamics 365 Finance ir Dynamics 365 Supply Chain Management palaikomos tik GCC.

### <a name="can-i-use-public-azure-devops-with-finance-and-supply-chain-management-in-gcc"></a>Ar galiu naudoti viešą Azure DevOps su finansų ir tiekimo grandinės valdymu GCC?

Taip, galite naudoti viešą Azure DevOps paslaugas, jei neturite reikalavimų sprendimui, sertifikuotam Federalinės rizikos ir įgaliojimų valdymo programos (FEDRAMP). Arba galite naudoti Azure DevOps Serveris.

### <a name="can-i-deploy-a-cloud-hosted-environment-tier-1-development-environment-on-an-azure-commercial-subscription"></a>Ar galiu įdiegti debesyje priglobtos aplinkos Tier-1 kūrimo aplinką „Azure“ komercinėje prenumerata?

Ne. Į [LCS skirta GCC](https://gov.lcs.microsoftdynamics.us), turite naudoti Azure Government prenumeratą, kad įdiegtumėte debesies prieglobos aplinką.

### <a name="what-can-i-do-if-i-need-a-package-from-the-shared-asset-library-but-it-isnt-available-in-lcs-for-gcc"></a>Ką daryti, jei man reikia paketo iš bendrinamų išteklių bibliotekos, bet jo nėra GCC skirtoje LCS?

Tą patį paketą galite atsisiųsti iš bendrinamų išteklių bibliotekos [viešoji LCS](https://lcs.dynamics.com). Arba jūsų partneris gali padėti jums atsisiųsti paketą.

### <a name="is-the-code-upgrade-tool-available-in-gcc"></a>Ar GCC galimas kodo atnaujinimo įrankis?

Ne, kodo atnaujinimo įrankis šiuo metu nepasiekiamas GCC. Tačiau galite sukurti perspektyvų projektą [viešoji LCS](https://lcs.dynamics.com) ir naudokite kodo atnaujinimo įrankį. Atminkite, kad potencialiuose projektuose negalėsite įdiegti aplinkų.

### <a name="can-my-partner-open-a-support-ticket-on-my-behalf"></a>Ar mano partneris gali atidaryti paramos bilietą mano vardu?

Taip. Tačiau jei jūsų partneris naudoja ne GCC tapatybę, palaikymo bilietas bus nukreiptas į viešąją palaikymo eilę. Norėdami atidaryti palaikymo bilietus, rekomenduojame naudoti kliento GCC teisę LCS.

## <a name="see-also"></a>Taip pat žiūrėkite

- [„Dynamics 365“ JAV vyriausybė](/power-platform/admin/microsoft-dynamics-365-government)
- [Verslo programos JAV vyriausybės funkcijos prieinamumas](https://aka.ms/BAPFunctionalParity).
- [„Lifecycle Services“ (LCS) vartotojo vadovas](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Visuotinio debesies diegimo apžvalga](../../../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
