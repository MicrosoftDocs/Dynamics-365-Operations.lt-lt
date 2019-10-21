---
title: Vartotojas gali pasiekti „Core HR“, bet ne programas „Onboard“ ar „Attract“
description: Šioje temoje aiškinama, kaip išspręsti problemą, kai vartotojas gali pasiekti „Microsoft“ „Dynamics 365 Talent – Core HR“, bet negali pasiekti programų „Attract“ arba „Onboard“.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 80b1f8aeabfd033f393463f4be5a61447377f2d9
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009311"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a>Vartotojas gali pasiekti „Core HR“, bet ne programas „Onboard“ ar „Attract“

[!include [banner](includes/banner.md)]

**Aplinkos informacija**

- „Microsoft Dynamics Lifecycle Services“ (LCS) diegimą atliko vartotojas A.
- Vartotojas A įtraukė vartotoją B kaip „Microsoft“ „Dynamics 365 Talent: Core HR Core HR“ vartotoją.

**Išduoti**

Vartotojas B gali pasiekti „Core HR“, bet negali pasiekti programų „Talent: Attract“ arba „Talent: Onboard“. Vietoj to, vartotojui bandant apsilankyti **„Experience“ programose** jis nukreipiamas į bandomosios versijos aplinką.

**Sprendimas**

B vartotojas turi būti priskirtas prie teisių, suteikiančių galimybę peržiūrėti „Microsoft PowerApps“ aplinką, kurią vartotojas A sukūrė parengimo proceso metu.

Daugiau informacijos ieškokite dalyje [„Talent“ parengimas](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

**Ilgalaikis sprendimas**

„Microsoft“ ketina automatiškai priskirti atitinkamas teises „Onboard“ arba „Attract“, kai vartotojas įtraukiamas į „Core HR“.
