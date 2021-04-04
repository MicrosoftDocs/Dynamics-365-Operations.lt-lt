---
title: Datos ir laiko sinchronizavimas importavimo užduotyse
description: Naudokite UTC laiko juostas importavimo užduotyse tam, kad išvengtumėte problemų, susijusių su laiko juostų konvertavimu.
author: Sunil-Garg
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ce3bf39e8342d3fe19a253f6d17684b2bd0aec0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570486"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>Datos ir laiko sinchronizavimas importavimo užduotyse

[!include [banner](../includes/banner.md)]

Svarbu nustatyti jūsų importavimo užduoties laiko juostą kaip Universaliojo laiko (UTC). Jei naudojate kitą parametrą, jūsų importuotuose duomenyse galite matyti netikėtas datas ir laikus. Be tinkamo parametro, importavimo procese UTC formato data konvertuojama į vietinį formatą, o tada sistemos parametrai konvertuoja ją dar kartą.

Dėl šio dvigubo konvertavimo, datos gali pasikeisti tarp programų. Pavyzdžiui, dėl dvigubo konvertavimo darbuotojo darbo pradžios data gali skirtis tarp „Dynamics 365 Human Resources” ir „Dynamics 365 Finance”, kadangi egzistuoja skirtumai tarp vietinio laiko zonų. Importavimo užduoties nustatymas į UTC laiko zoną išsprendžia šią problemą.

1. „Dynamics 365 Finance and Operations” pasirinkit **Duomenų valdymas**.

2. Pasirinkite **Importuoti projektus**, o tada pasirinkite projektą.

3. Dalyje **Šaltinio datos formatas** pasirinkite **„CSV-Unicode”**.

   [![Šaltinio datos formatą pakeitimas į UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. Pakeiskite **Laiko zoną** į **Universaliojo laiko zoną** ir pakeiskite **Kalbą** į **„En-US”**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]