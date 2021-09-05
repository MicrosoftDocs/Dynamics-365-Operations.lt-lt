---
title: Nepavyksta sukurti aplinkos „Power Apps“ administravimo centre
description: Šioje temoje paaiškinama, ką daryti, jei administratorius negali sukurti aplinkos „Microsoft Power Apps“ administravimo centre.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 50a5aac71ec8ed850cfad32bdb1b8d589eb2885a
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413566"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Nepavyksta sukurti aplinkos „Power Apps“ administravimo centre

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Išduoti**

- Nuomotojo arba aplinkos administratorius negali sukurti aplinkos „Microsoft Power Apps“ administravimo centre.
- Vartotojas neturi licencijos suteikiančios teisę kurti aplinkas.

**Sprendimas**

Įsitikinkite, kad nuomotojo administratorius turi teisę įgyvendinti „Power Apps“ P2 teises vartotojui kuriančiam aplinką. Tolesni „Microsoft Dynamics“ paslaugų planai suteikia teises kurti aplinkas:

| Bendras produkto atsargų laikymo padalinys (SKU)       | Power Apps P2 paslaugos planas  |
|------------------------------------------------|----------------------------|
| „Microsoft Dynamics 365 for Operations“          | Power Apps, skirta „Dynamics 365“ |
| „Microsoft Dynamics 365“ planas „Enterprise Edition“ | Power Apps, skirta „Dynamics 365“ |

Atkreipkite dėmesį, kad įvairūs Microsoft Office SKU taip pat suteikia teisę kartu naudoti atskiro Power Apps 2 plano SKU. Svarbiausia tai, kad turi būti vienas iš šių SKU.

1. Eikite į [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Kurkite aplinkas vykdydami instrukcijas, pateiktas [„Human Resources“ parengimas](/dynamics365/unified-operations/talent/provisioning-talent).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
