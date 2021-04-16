---
title: Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius
description: Šioje temoje paaiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigoms priskirtas naudotojas gali sukurti konfigūracijos teikėją.
author: NickSelin
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27e1275199d098fffb56db61ed6bfd2fc3cdb790
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755135"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius

[!include [banner](../../includes/banner.md)]

Šioje temoje paaiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigoms priskirtas naudotojas gali sukurti elektroninių ataskaitų (ER) konfigūracijos teikėją. Kiekviena ER konfigūracija į teikėją nurodys kaip į konfigūracijos autorių. Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūracijų teikėją. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijų teikėjų paslaugas visos įmonės naudoja bendrai.

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

![Elektroninių ataskaitų darbo srities puslapis](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]