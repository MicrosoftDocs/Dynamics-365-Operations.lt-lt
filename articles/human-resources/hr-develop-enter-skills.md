---
title: Įgūdžių įvedimas
description: Darbuotojai ir vadovai gali įvesti įgūdžius „Dynamics 365 Human Resources” platformoje.
author: twheeloc
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 32f08fa45c023c587d89623a12f101f50ef4a5fb
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693009"
---
# <a name="enter-skills"></a>Įgūdžių įvedimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Galite įvesti darbuotojų, pretendentų ar kontaktų tikslinius arba faktinius įgūdžius „Dynamics 365 Human Resources” platformoje. Tikslinis įgūdis yra įgūdis, kurį asmuo planuoja pasiekti. Faktinis įgūdis yra įgūdis, kurį asmuo šiuo metu turi.

## <a name="create-a-workflow-to-auto-approve-skills"></a>Darbo eigos kūrimas automatiniam įgūdžių patvirtinimui

Norėdami įvesti įgūdžius, kuriems nereikia patvirtinimo, turite sukurti darbo eigą, automatiškai patvirtinančią įgūdžius.

> [!NOTE]
> Darbuotojų įvestiems įgūdžiams visada reikalingas vadovo patvirtinimas. Ši darbo eiga tik automatiškai patvirtina įgūdžius, kuriuos įvedė vadovai savo darbuotojų vardu.

1. Darbo erdvėje **Personalo valdymas** rinkitės **Nuorodos**.

2. Dalyje **Sąranka** pasirinkite **Personalo darbo eigos**.

3. Pasirinkite **Naujas**.

4. Srityje **Kurti darbo eigą** pasirinkite **Darbuotojo įgūdžiai**.

   [![Pasirinkite darbuotojo įgūdžių darbo eigą.](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)

5. Dialogo lange **Atidaryti šį failą?** pasirinkite **Atidaryti**. Paraginti įveskite savo kredencialus.

6. Darbo eigos rengyklėje pasirinkite darbo eigos elementą **Patvirtinti įgūdžius** ir nuvilkite jį į drobę.

   [![Darbo eigos elemento Patvirtinti įgūdžius pasirinkimas.](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)

7. Sujunkite elementą **Pradėti** su **Patvirtinti įgūdžius 1** elementu, o tada sujunkite **Patvirtinti įgūdžius 1** elementą su **Baigti** elementu. Jums gali tekti slinkti žemyn, kad pamatytumėte elementą **Baigti**. Galite nuvilkti jį arčiau kitų elementų.

   [![Sujunkite darbo eigos elementus.](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)

8. Du kartus spustelėkite darbo eigos elementą **Patvirtinti įgūdžius 1**, o tada dešiniuoju pelės mygtuku spustelėkite **1 veiksmo** elementą. Dešiniuoju pelės mygtuku spustelėkite **1 veiksmo** elementą, o tada pasirinkite **Ypatybės**.

9. Lange **Ypatybės** pasirinkite **Sąlyga** kairiojoje naršymo srityje.

10. Pasirinkite **Vykdyti šį veiksmą tik tada, kai įvykdytos nurodytos sąlygos**.

11. Pasirinkite **Įtraukti sąlygą**. Po **Kur** pasirinkite **Darbuotojo savitarnos įgūdžiai**, o tada – **Darbuotojo savitarnos įgūdžiai. Asmuo**. Po **yra** pasirinkite **laukas**, o tada – **Vartotojo ir asmens ryšys.Asmuo**.

    [![Sąlygos nurodymas.](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)

12. Pasirinkite **Priskyrimas** kairiojoje naršymo juostoje.

13. Skirtuke **Priskyrimo tipas** pasirinkite **Hierarchija**.

14. Skirtuko **Hierarchijos pasirinkimas** lauke **Hierarchijos tipas:** pasirinkite **Valdymo hierarchija**.

    [![Valdymo hierarchijos nurodymas.](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)

15. Pasirinkite **Uždaryti** ir **Darbo eiga** naršymo kelyje, o tada – **Įrašyti ir uždaryti**.

Daugiau informacijos apie darbo eigų kūrimą rasite [Darbo eigos sistemos apžvalga](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).

## <a name="enter-skills-for-a-worker"></a>Darbuotojo įgūdžių įvedimas

1. Pasirinkite darbuotoją.

2. **Darbuotojo** puslapio veiksmų juostoje pasirinkite **Asmuo**, o tada – **Įgūdžiai**.

3. Puslapyje **Įgūdžiai** užpildykite šiuos laukus kiekvienam įgūdžiui:

   - **Įgūdis**: Pasirinkite įgūdį.
   - **Lygio tipas**: Pasirinkite **Faktinis** jau turimam darbuotojo įgūdžiui arba **Tikslinis** – įgūdžiui, kurį darbuotojas siekią įgyti.
   - **Lygis**: Pasirinkite darbuotojo įgūdžio lygį.
   - **Lygio data**: Kalendoriaus įrankyje pasirinkite datą.
   - **Egzaminuotojas**: Jei reikia, iš sąrašo pasirinkite egzaminuotoją. Galite filtruoti savo iešką.
   - **Darbo patirties metai**: Įveskite darbo patirties metus.
   - **Patvirtinta**: Jei įgūdis yra patvirtintas, pažymėkite šį lauką.
   - **Patvirtino**: Įveskite patvirtinusio asmens vardą.

4. Įvedę įgūdžius, pasirinkite **Įrašyti**.

## <a name="see-also"></a>Taip pat žiūrėkite

[Įgūdžių konfigūravimas](hr-develop-skills.md)<br>
[Įgūdžių susiejimas](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
