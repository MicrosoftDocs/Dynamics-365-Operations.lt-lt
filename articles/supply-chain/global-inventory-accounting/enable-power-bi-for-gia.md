---
title: Įgalinti „Power BI” Visuotinę atsargų apskaitą
description: Šiame straipsnyje aprašoma, kaip įgalinti Microsoft Power BI visuotinių atsargų apskaitą.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 757d969cf9d1ebc12aeb34b0810fc291e47dffad
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906072"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a>Įgalinti „Power BI” Visuotinę atsargų apskaitą

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Galite prisegti plyteles, ataskaitų sritis ir ataskaitas iš savo [„PowerBI.com”](https://powerbi.com/) paskyros į savo „Microsoft Dynamics 365” programos darbo sritį.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš įgalindami „Power BI” ataskaitas privalote atitikti šias būtinąsias sąlygas:

- Turite būti sistemos administratorius „Dynamics 365” programoje.
- Privalote turėti [„PowerBI.com”](https://powerbi.com/) paskyrą.
- Privalote turėti bent vieną ataskaitų sritį ir ataskaitą savo „Power BI” paskyroje.
- Turite būti savo „Azure Active Directory” („Azure AD”) paskyros administratorius.
- „Azure AD” domenas turi būti tas pats domenas, kurį naudojote savo [„PowerBI.com”](https://powerbi.com/) paskyrai.

## <a name="setup"></a>Sąranka

Norėdami nustatyti „Power BI” integravimą, atlikite šiuos veiksmus.

1. Prisijunkite prie [„Microsoft Dynamics” „Lifecycle Services” (LCS)](https://lcs.dynamics.com/Logon/Index).
1. Eikite į **Bendrai naudojamo turto biblioteką**, pasirinkite **„Power BI” ataskaitos modelį** kaip turto tipą ir atsisiųskite **Visuotinės atsargų apskaitos** paketą. 
1. Prisijunkite prie [„PowerBI.com”](https://app.powerbi.com/) ir įkelkite **Visuotinės atsargų apskaitos** „Power BI” ataskaitos failą atlikdami šiuos veiksmus:

    1. Pasirinkite **Naujas**.
    1. Pasirinkite **Įkelti failą**.
    1. Pasirinkite **Visuotinės atsargų apskaitos** „Power BI” ataskaitos failą.

1. Sukonfigūruokite **Visuotinės atsargų apskaitos** „Power BI” ataskaitą atlikdami šiuos veiksmus:

    1. Eikite į **Mano darbo sritis**, suraskite Visuotinės atsargų apskaitos duomenų rinkinį, o tada iš meniu **Parinktys** pasirinkite **Parametrai**.
    1. **Visuotinės Atsargų Apskaitos parametruose** išplėskite **Parametrus** ir atnaujinkite visus parametrus, kaip reikalinga. Ypatingai patikrinkite šiuos parametrus:
        1. Perrašyti numatytąsias URL vertes naudojant **Dataverse vertes, rastas**"Power platform **" aplinkos informacija LCS ("** Power platform" integravimo **skyriuje**).
        1. Perrašykite numatytąsias aplinkos **ID** vertes naudodami vertes, kurios **LCS** aplinkos informacija (skyriuje Valdyti **aplinką**).
        1. Pasirinkite redagavimo **kredencialų** saitą, esantį šalia **CDS žymos** duomenų šaltinio **kredencialų** skyriuje. Tada prisijunkite prie savo Dataverse paskyros naudodamiesi **OAuth2** autentifikavimo metodą.
    1. Patvirtinkite, kad Power BI rodo rasta **Mano darbo sritis \> Ataskaitos \> Visuotinė Atsargų Apskaita** dabar veikia tinkamai ir rodo turinį iš jūsų sistemos.

1. Užregistruokite programą, kaip aprašyta [PowerBI.com integravimo konfigūravimas](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).
1. Integruokite **Visuotinės atsargų ataskaitos** „Power BI” ataskaitos failą į „Dynamics 365 Supply Chain Management” atlikdami šiuos veiksmus:

    1. Eikite į **Sistemos administravimas \> Sąranka \> PowerBI.com konfigūracija**.
    1. Pasirinkite **Redaguoti**.
    1. Pasirinkite **Įgalinti PowerBI.Com integravimą**.
    1. Lauke **Programos ID** įveskite programos ID.
    1. Lauke **Programos raktas** įveskite programos raktą.
    1. Pasirinkite **Įrašyti**.

1. Atnaujinkite puslapį, kad atsirastų „Power BI” prisijungimo dialogo langas.
1. Skirtuke **Parinktys** pasirinkite **Atidaryti ataskaitos katalogą**, o tada pasirinkite **Visuotinės atsargų apskaitos** „Power BI” ataskaitos failą, kurį įkėlėte anksčiau.
1. Atnaujinkite puslapį. Turėtumėte pamatyti, kad jūsų ataskaita įtraukta.
1. Dalyje **„Power BI” ataskaitos** pasirinkite **Visuotinės atsargų apskaitos** nuorodą.

Daugiau informacijos rasite [PowerBI.com integravimo konfigūravimas](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).
