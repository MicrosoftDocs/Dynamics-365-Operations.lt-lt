---
title: KS versijos nustatymas
description: Jei nustatytas numatytasis prekės užsakymo tipas Gamyba, poreikio išskleidimo metu planavimo variklis pagal teritoriją suranda tinkamą KS versiją.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a90a257debe8f24e149ddca1738d8376b2124012
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966985"
---
# <a name="determine-the-bom-version"></a>KS versijos nustatymas

[!include [banner](../includes/banner.md)]

Jei nustatytas numatytasis prekės užsakymo tipas Gamyba, poreikio išskleidimo metu planavimo variklis pagal teritoriją suranda tinkamą KS versiją. 

Teritorijos dimensija visada žinoma ir yra nurodyta poreikio operacijoje. Tolesnis procesas naudojamas nustatyti, kokią KS versiją naudoti.

-   Jei poreikio teritorijoje yra nurodyta prekės KS versija, naudojama konkrečios teritorijos KS.
-   Jei poreikio teritorijoje konkrečios teritorijos KS versija nenustatyta, naudojama bendroji KS. Bendrajame KS teritorija nenurodoma, tad jis tinka kelioms teritorijoms. Jei yra bendroji KS, naudojama ji.
-   Jei nėra galimos naudoti bendrojo KS versijos, poreikio išskleidimas sustoja.

Tinkama KS versija, konkrečios teritorijos ar bendroji, turi atitikti nurodytus datos ir kiekio kriterijus.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]