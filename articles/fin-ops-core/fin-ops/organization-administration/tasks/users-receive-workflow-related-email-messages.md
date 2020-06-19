---
title: Leidimas vartotojams gauti su darbo eiga susijusius el. laiškus
description: Galite sukonfigūruoti sistemą siųsti el. laiškus vartotojams, kai įvyksta su darbo eiga susiję įvykiai.
author: jasongre
manager: AnnBe
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40ad380c7bfb2b3fc518b0278286ae03532668ed
ms.sourcegitcommit: 4db8c30c2f26af1896938dd3ece3756577374ecb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/01/2020
ms.locfileid: "3416558"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>Leidimas vartotojams gauti su darbo eiga susijusius el. laiškus

[!include [banner](../../includes/banner.md)]

Galite sukonfigūruoti sistemą siųsti el. laiškus vartotojams, kai įvyksta su darbo eiga susiję įvykiai. Pvz., galima siųsti el. laiškus vartotojams, kai jiems priskiriami dokumentai, kuriuos reikia patvirtinti. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.

1. Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Užklausos > Paketinė užduotis**.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. **Veiksmų srityje** spustelėkite **Vartotojo parinktys**.
4. Spustelėkite skirtuką **Darbo eiga**. Įsitikinkite, ar skyrius **Pranešimai** išplėstas. Skyriuje **Pranešimai** galite nurodyti, kaip vartotojui turėtų būti pranešta apie įvykius, susijusius su darbo eiga.  
5. Lauke **Eilutės elemento darbo eigos pranešimo tipas** pasirinkite parinktį.
    - Sugrupuota – pranešimai apie eilučių elementus sugrupuojami į vieną el. laišką.
    - Po vieną – el. laiškas siunčiamas apie kiekvieną eilutės elementą.  
    - Jeigu norite, kad vartotojas pranešimus gautų kliente, pažymėkite žymės langelį **Siųsti pranešimus el. paštu**.  
6. Spustelėkite **Įrašyti**.
7. Uždarykite puslapį.

> [!NOTE]
> Darbo eigos el. pašto šablonai bus gaunami arba iš sistemos el. pašto šablonų arba organizacijos el. pašto šablonų, atsižvelgiant į tai, ar darbo eiga yra sistemos lygio (ne įmonei būdingas), ar organizacijos lygio (būdinga įmonei) darbo eiga.
