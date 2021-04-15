---
title: Nepavyksta sukurti aplinkos „Power Apps“ administravimo centre
description: Šiame straipsnyje paaiškinama, ką daryti, jei administratorius negali sukurti aplinkos „Microsoft Power Apps“ administravimo centre.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f1a086f1b710de9bad898abc740286c174ae3be7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797990"
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
2. Kurkite aplinkas vykdydami instrukcijas, pateiktas [„Human Resources“ parengimas](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).


[!INCLUDE[footer-include](../includes/footer-banner.md)]