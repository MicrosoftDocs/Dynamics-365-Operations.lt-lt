---
title: Nustatyti priežasčių kodus
description: „Dynamics 365 Human Resources“ naudojami priežasčių kodus, siekiant paaiškinti, kodėl keičiasi darbuotojo išmokos.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5bcfa60349d6d362504184dd90cc97ea27e8ba43
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689528"
---
# <a name="set-up-reason-codes"></a>Nustatyti priežasčių kodus


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

„Dynamics 365 Human Resources“ naudojami priežasčių kodus, siekiant paaiškinti, kodėl keičiasi darbuotojo išmokos.

> [!NOTE]
> Nuo 2021 m. sausio mėnesio priežasties kodai yra perkelti į **Personalo valdymo** darbo sritį, o ne **Išmokų valdymo** darbo sritį. Dėl daugiau informacijos, žr. [Rankiniu būdu perkelti priežasties kodus į personalo valdymą](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).

## <a name="create-reason-codes"></a>Priežasčių kodų kūrimas

1. Darbo srityje **Personalo valdymas** (ar **Išmokų valdymas** darbo srityje, jei jūsų priežasties kodai nebuvo perkelti), rinkitės **Nuorodos** ir tada rinkitės **Priežasties kodai**.

2. Pasirinkite **Naujas**.

3. Nurodyti šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Tikslinės paskirties šifras** | Unikalus pavadinimas, skirtas nustatyti priežastį, dėl kurios darbuotojas galėtų keisti išmokų plano registraciją. |
   | **Aprašas** | Priežasties kodo aprašas. |

4. Skyriuje **Taikomi scenarijai**, nustatykite **Išmokų valdymas** į **Taip**. (Netaikoma, jei jūsų priežasties kodai dar nebuvo perkelti į **Personalo valdymo** darbo sritį.)

5. Pasirinkite **Įrašyti**.

## <a name="manually-migrate-reason-codes-to-personnel-management"></a>Rankiniu būdu perkelti priežasties kodus į personalo valdymą

Nuo 2021 m. sausio mėnesio priežasties kodai yra perkelti į **Personalo valdymo** darbo sritį, o ne **Išmokų valdymo** darbo sritį. Didžio dalis kodo duomenų buvo automatiniu būdu perkelti į jūsų aplinką. Kai kurie priežasties kodo duomenys gali būti neperkelti. Pavyzdžiui, priežasties kodai dabar turi daugiausiai 15 ženklų, dėl to, visi ilgesni nei 15 ženklų priežasties kodai nebus automatiniu būdu perkelti.

Matysite reklaminę juostą **Nuorodos** puslapyje **Išmokų valdymas** darbo srityje, kuri jus informuos apie perkelimą ir ar bet kurie priežasties kodai nepersikėlė.

1. Rinkitės **Priežasties kodai** dėl išsamios informacijos apie perkėlimo būseną.

   [![Priežasčių kodai.](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)

2. Rinkitės kodo priežastį, kuri nepersikėlė.

   [![Priežasties kodo perkėlimo būsena.](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)

3. Rinkitės **Perkelti priežasties kodą**.

   [![Perkelti priežasties kodą.](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)

4. Juostoje **išmokos priežasties kodo perkėlimas** turite dvi parinktis sudaryti žemėlapį personalo valdymo priežasties kodui:

   - Norėdami naudoti esantį priežasties kodą personalo valdyme, rinkitės vieną iš esančių **Naudoti esantį priežasties kodą** iškrentančiame meniu.
     > [!NOTE]
     > Galtie naudoti tik esantį priežasties kodą personalo valdyme, jei kitas išmokų valdymo priežasties kodas dar nebuvo į jį perkeltas.
   - Norėdami sukurti naują priežasties kodą personalo valdyme, įveskite naują **Naujas priežasties kodas** ir tada įveskite aprašą **Naujas aprašas**.

   [![Padarykite žemėlapį personalo valdymo priežasties kodo.](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)

Po to, kai priežasties kodai perkeliami į personalo valdymą, parinktis jų naudojimui išmokų valdyme yra automatiškai nustatomas į **Taip**.

[![Naudokite priežasties kodą išmokų valdyme.](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
