---
title: Įgalinti „Power BI” Visuotinę atsargų apskaitą
description: Šioje temoje aprašoma, kaip įgalinti „Microsoft Power BI” Visuotinei atsargų apskaitai.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d7979ed18b98ee6133774cd91bc866d6fca92d5f
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273197"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a>Įgalinti „Power BI” Visuotinę atsargų apskaitą

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

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
    1. **Visuotinės atsargų apskaitos parametruose** išplėskite **Parametrus** ir atnaujinkite visus parametrus, kaip reikalinga.

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
