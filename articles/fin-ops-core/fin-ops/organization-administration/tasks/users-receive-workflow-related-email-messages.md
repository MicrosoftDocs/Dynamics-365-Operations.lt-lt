---
title: Leidimas vartotojams gauti su darbo eiga susijusius el. laiškus
description: Galite sukonfigūruoti sistemą siųsti el. laiškus vartotojams, kai įvyksta su darbo eiga susiję įvykiai.
author: jasongre
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 368fe2fbf1f8a1adcabe37ced5ed942f9fb86fc8
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070430"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>Leidimas vartotojams gauti su darbo eiga susijusius el. laiškus

[!include [banner](../../includes/banner.md)]


[!INCLUDE [PEAP](../../../../includes/peap-1.md)]

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]