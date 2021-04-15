---
title: Datos ir laiko sinchronizavimas importavimo užduotyse
description: Naudokite UTC laiko juostas importavimo užduotyse tam, kad išvengtumėte problemų, susijusių su laiko juostų konvertavimu.
author: Sunil-Garg
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
ms.openlocfilehash: 41c0ec805a20a525989e0133e5dffb29ce3fed39
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748674"
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