---
title: Atostogų užklausos darbo eigos kūrimas
description: Atostogų ir neatvykimų užklausų darbo eigos kūrimas, siekiant nuosekliai tvarkyti atostogų užklausas „Dynamics 365 Human Resources“.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a97cbec20d57c47e021582a0b9a1a4d7110c936a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688014"
---
# <a name="create-a-leave-request-workflow"></a>Atostogų užklausos darbo eigos kūrimas

> [!Important]
> Šioje temoje parodytas funkcionalumas šiuo metu prieinamas autonominiams „Dynamics 365 Human Resources“ klientams. Kai kurios arba visos funkcijos bus prieinamos kaip būsimo „Finance“ infrastruktūros leidimo dalis po to, kai bus išleistas „Finance“ leidimas 10.0.26.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Galite sukurti darbo eigą „Dynamics 365 Human Resources“, kad galėtumėte nuosekliai tvarkyti atostogų ir neatvykimų užklausas. **Atostogų ir neatvykimų** darbo eiga leidžia:

- Nustatyti užduotis
- Nustatyti, kas turi atlikti užduotis
- Nurodyti, kas gali patvirtinti arba atmesti užklausas

## <a name="create-a-leave-and-absence-request-workflow"></a>Atostogų ir neatvykimų darbo eigos kūrimas

1. Puslapyje **Atostogos ir neatvykimai** pasirinkite skirtuką **Saitai**.

2. Dalyje **Sąranka** pasirinkite **Žmogiškųjų išteklių darbo eigos**.

3. Pasirinkite **Nauja**, tada pasirinkite **Atostogų ir neatvykimų užklausa**. 

4. Kai pasirodys pranešimo langelis **Atidaryti šį failą?**, pasirinkite **Atidaryti** ir prisijunkite, naudodami įmonės kredencialus.

5. Naudokite darbo eigos doroklį, kad sukurtumėte savo atostogų užklausų darbo eigą. Daugiau informacijos apie darbą su darbo eigomis žr. skyriuje [Darbo eigų apžvalgos kūrimas](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Atostogų ir neatvykimų darbo eigos duomenų elementai

Galite naudoti tolesnius duomenų elementus, norėdami sukurti sąlyginius arba automatinius patvirtinimus atostogų ir neatvykimų užklausų darbo eigose.

- **Suma**
- **Komentuoti**
- **Įmonė**
- **Sukūrė**
- **Sukūrimo data ir laikas**
- **Pabaigos data**
- **Atostogų tipas**
- **Modifikavo**
- **Pakeitimo data ir laikas**
- **Tikslinės paskirties šifras**
- **Užklausos ID**
- **Pradžios data**
- **Būsena** 
- **Pateikimo data**
- **Pateikė**
- **Pateikė personalas**
- **Pateikė vadovas**
- **Pateikė kito vardu**
- **Darbininkas**
- **Darbininko tipas**

Šie pavyzdžiai rodo, kaip galima sukurti skirtingus darbo eigos sąlygų tipus naudojant tolesnius duomenų elementus.

- Sąlyginiame išraše naudokite **Priežasties kodas**, kad nukreiptumėte nedarbingumo atostogų užklausas su priežasties kodu **Operacija** personalui patvirtinti, o visus kitus priežasties kodus – vadovui. Daugiau informacijos apie sąlyginius išrašus žr. [Sąlyginių darbo eigos sprendimų konfigūravimas](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md). 

- Automatiniame veiksme naudokite **Pateikė personalas** ir **Pateikė vadovas**, norėdami automatiškai patvirtinti atostogų užklausas, kurias šie vaidmenys pateikia darbuotojų vardu. Daugiau informacijos apie automatinius veiksmus žr. [Darbo eigos patvirtinimo procesų konfigūravimas](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- Sąlyginiame išraše arba automatiniame veiksme naudokite **Atostogų tipas**, norėdami valdyti, kaip darbo eiga nukreipia tam tikrų atostogų tipų užklausas.

## <a name="see-also"></a>Taip pat žiūrėkite

- [Atostogų ir neatvykimų apžvalga](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
