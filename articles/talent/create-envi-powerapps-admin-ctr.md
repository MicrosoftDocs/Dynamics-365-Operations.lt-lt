---
title: Nepavyksta sukurti aplinkos „PowerApps“ administravimo centre
description: Šioje temoje paaiškinama, ką daryti, jei administratorius negali sukurti aplinkos „Microsoft PowerApps“ administravimo centre.
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
ms.openlocfilehash: 97d44dc034cb8097fc0ecf9ac4e485425f097102
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518609"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a>Nepavyksta sukurti aplinkos „PowerApps“ administravimo centre

[!include [banner](includes/banner.md)]

**Problema**

- Nuomotojo arba aplinkos administratorius negali sukurti aplinkos „Microsoft PowerApps“ administravimo centre.
- Licencija, suteikianti vartotojams teisę atlikti aplinkos kūrimo veiksmą, nėra tiesiogiai priskirta vartotojui, kuris atlieka šį veiksmą.

**Sprendimas**

Įsitikinkite, kad nuomotojo administratorius tiesiogiai priskyrė tinkamą „PowerApps“ P2 licenciją vartotojui, kuris atliks aplinkos kūrimo veiksmą. Štai „Microsoft Dynamics“ paslaugų teikimo planai, kurie suteikia tokią teisę.

| Viso produkto sandėliavimo vienetas (SKU)       | „PowerApps“ P2 paslaugų teikimo planas  |
|------------------------------------------------|----------------------------|
| „Microsoft Dynamics 365 for Operations“          | „PowerApps“, skirtos „Dynamics 365“ |
| „Microsoft Dynamics 365“ planas „Enterprise Edition“ | „PowerApps“, skirtos „Dynamics 365“ |

Atkreipkite dėmesį, kad įvairūs „Microsoft Office“ SKU taip pat suteikia teisę kartu naudoti atskiro „PowerApps“ 2 plano SKU. Svarbiausia tai, kad turi būti vienas iš šių SKU.

1. Eikite į [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Kurkite aplinkas vykdydami instrukcijas, pateiktas [„Talent“ parengimas](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).
