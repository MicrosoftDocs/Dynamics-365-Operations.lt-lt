---
title: Sukurkite darbo eigą atostogų pirkimo ir pardavimo užklausai
description: Sukurkite darbo eigą atostogų pirkimo ir pardavimo užklausai, tam, kad galėtumėte nuosekliai tvarkyti atostogų pirkimo ir pardavimo užklausas Dynamics 365 Human Resources platformoje.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5bc31740218e3f171d89debace339dee0177d826
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053976"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a>Sukurkite darbo eigą atostogų pirkimo ir pardavimo užklausai

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Galite sukurti darbo eigą Dynamics 365 Human Resources platformoje, tam, kad nuosekliai tvarkytumėte savo atostogų pirkimo ir pardavimo užklausas. **Atostogų pirkimo ir pardavimo** darbo eiga jums leidžia:

- Nustatyti užduotis
- Nustatyti, kas turi atlikti užduotis
- Nurodyti, kas gali patvirtinti arba atmesti užklausas

## <a name="create-a-buy-and-sell-leave-request-workflow"></a>Sukurkite darbo eigą atostogų pirkimo ir pardavimo užklausai

1. Puslapyje **Atostogos ir neatvykimai** pasirinkite skirtuką **Saitai**.

2. Dalyje **Sąranka** pasirinkite **Žmogiškųjų išteklių darbo eigos**.

3. Pasirinkite **Naujas**, o tada pasirinkite **Atostogų pirkimo ir pardavimo užklausa**. 

4. Kai pasirodys pranešimo langelis **Atidaryti šį failą?**, pasirinkite **Atidaryti** ir prisijunkite, naudodami įmonės kredencialus.

5. Naudokite darbo eigos doroklį, kad sukurtumėte savo atostogų užklausų darbo eigą. Daugiau informacijos apie darbą su darbo eigomis žr. skyriuje [Darbo eigų apžvalgos kūrimas](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Atostogų ir neatvykimų darbo eigos duomenų elementai

Galite naudotis šiais informacijos elementais, kad sukurtumėte sąlyginius ir automatinius patvirtinimus atostogų pirkimo ir pardavimo užklausoms darbo eigose:

- **Suma**
- **Atostogų pirkimo ir pardavimo strategija**
- **Įmonė**
- **Sukūrė**
- **Sukūrimo data ir laikas**
- **Pabaigos data**
- **Atostogų tipas**
- **Modifikavo**
- **Pakeitimo data ir laikas**
- **Užklausos ID**
- **Pradžios data**
- **Būsena** 
- **Pateikimo data**
- **Pateikė**
- **Pateikė personalas**
- **Pateikė vadovas**
- **Pateikė kito vardu**
- **Darbuotojas**

## <a name="workflow-examples"></a>Darbo eigos pavyzdžiai

Šie pavyzdžiai rodo, kaip galima sukurti skirtingus darbo eigos sąlygų tipus naudojant tolesnius duomenų elementus.

- Naudokite **Pateikė personalas** ir **Pateikė vadovas** automatiniame veiksme, tam, kad automatiškai būtų patvirtintos atostogų pirkimo ir pardavimo užklausos, ir kad šie vaidmenys būtų pateikti darbuotojų vardu. Daugiau informacijos apie automatinius veiksmus žr. [Darbo eigos patvirtinimo procesų konfigūravimas](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- Sąlyginiame išraše arba automatiniame veiksme naudokite **Atostogų tipas**, norėdami valdyti, kaip darbo eiga nukreipia tam tikrų atostogų tipų užklausas.

## <a name="see-also"></a>Taip pat žiūrėkite

[Atostogų ir neatvykimų apžvalga](hr-leave-and-absence-overview.md)<br>
[Atostogų pirkimo ir pardavimo strategijų valdymas](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]