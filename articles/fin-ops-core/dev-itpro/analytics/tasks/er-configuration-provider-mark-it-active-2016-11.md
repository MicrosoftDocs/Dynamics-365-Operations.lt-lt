---
title: Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius
description: Šiame straipsnyje paaiškinama, kaip vartotojas, priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmeniui, gali sukurti konfigūracijos teikėją.
author: kfend
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
ms.openlocfilehash: db5226720a4e0c0f167921a972429c0a5ecdd2e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267820"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip vartotojas, priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmeniui, gali sukurti elektroninių ataskaitų (ER) konfigūracijos teikėją. Kiekviena ER konfigūracija į teikėją nurodys kaip į konfigūracijos autorių. Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūracijų teikėją. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijų teikėjų paslaugas visos įmonės naudoja bendrai.

## <a name="create-a-provider"></a>Kurti teikėją
1. Viršutiniame kairiajame kampe eikite į **naršymo sritį** ir pasirinkite **Organizacijos administravimas**.
2. Eikite į **Darbo sritis > Elektroninės ataskaitos**.
3. Eikite į **Susiję saitai > Konfigūracijos teikėjai**.
4. Pasirinkite **Naujas**.
    - Teikėjo įrašas turi unikalų pavadinimą ir URL. Peržiūrėkite šio puslapio turinį ir praleiskite šią procedūrą, jei „Litware, Inc.“ (https://www.litware.com) įrašas jau egzistuoja.  
5. Lauke Pavadinimas įveskite `Litware, Inc.`.
6. Lauke Interneto adresas įveskite `https://www.litware.com`.
7. Pasirinkite **Įrašyti**.
8. Uždarykite puslapį.

## <a name="select-as-an-active-provider"></a>Pasirinkti kaip aktyvų teikėją
1. Pasirinkite teikėją „Litware, Inc.“.
2. Pasirinkite **Nustatyti kaip aktyvų**.

![Elektroninių ataskaitų darbo srities puslapis.](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
