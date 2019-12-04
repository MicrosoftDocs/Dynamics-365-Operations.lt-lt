---
title: Nepavyksta sukurti aplinkos „Power Apps“ administravimo centre
description: Šioje temoje paaiškinama, ką daryti, jei administratorius negali sukurti aplinkos „Microsoft Power Apps“ administravimo centre.
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
ms.openlocfilehash: 5923c59ab5dde13fed0483972e76634031404fd8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773224"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Nepavyksta sukurti aplinkos „Power Apps“ administravimo centre

[!include [banner](includes/banner.md)]

**Išduoti**

- Nuomotojo arba aplinkos administratorius negali sukurti aplinkos „Microsoft Power Apps“ administravimo centre.
- Licencija, suteikianti vartotojams teisę atlikti aplinkos kūrimo veiksmą, nėra tiesiogiai priskirta vartotojui, kuris atlieka šį veiksmą.

**Sprendimas**

Įsitikinkite, kad nuomotojo administratorius tiesiogiai priskyrė tinkamą Power Apps P2 licenciją vartotojui, kuris atliks aplinkos kūrimo veiksmą. Štai „Microsoft Dynamics“ paslaugų teikimo planai, kurie suteikia tokią teisę.

| Viso produkto sandėliavimo vienetas (SKU)       | Power Apps P2 paslaugos planas  |
|------------------------------------------------|----------------------------|
| „Microsoft Dynamics 365 for Operations“          | Power Apps, skirta „Dynamics 365“ |
| „Microsoft Dynamics 365“ planas „Enterprise Edition“ | Power Apps, skirta „Dynamics 365“ |

Atkreipkite dėmesį, kad įvairūs Microsoft Office SKU taip pat suteikia teisę kartu naudoti atskiro Power Apps 2 plano SKU. Svarbiausia tai, kad turi būti vienas iš šių SKU.

1. Eikite į [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Kurkite aplinkas vykdydami instrukcijas, pateiktas [„Talent“ parengimas](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).
