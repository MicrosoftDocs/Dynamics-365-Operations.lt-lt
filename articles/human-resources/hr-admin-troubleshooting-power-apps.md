---
title: Nepavyksta sukurti aplinkos „Power Apps“ administravimo centre
description: Šioje temoje paaiškinama, ką daryti, jei administratorius negali sukurti aplinkos „Microsoft Power Apps“ administravimo centre.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e50348515f14b543c392c5f9c8637cec5fa037f2
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689612"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Nepavyksta sukurti aplinkos „Power Apps“ administravimo centre


[!INCLUDE [PEAP](../includes/peap-2.md)]

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
