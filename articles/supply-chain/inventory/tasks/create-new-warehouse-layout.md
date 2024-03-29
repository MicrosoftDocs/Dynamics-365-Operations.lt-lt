---
title: Naujo sandėlio maketo kūrimas
description: Šiame straipsnyje aprašoma, kaip nustatyti informaciją apie sandėlio vietas.
author: yufeihuang
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 143648e5317e6dce1b1a76a96d6069abe5d0e351
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859320"
---
# <a name="create-a-new-warehouse-layout"></a>Naujo sandėlio maketo kūrimas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip nustatyti informaciją apie sandėlio vietas. Tai taikoma tik tiems sandėliams, kurie sukurti naudojant funkciją „pagrindinis sandėliavimas‟, esančią modulyje Atsargų valdymas, o ne tiems, kurie sukurti modulyje Sandėlio valdymas. Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis.


## <a name="set-the-default-location-capacity"></a>Nustatyti numatytuosius vietos pajėgumus
1. Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Sąranka > Atsargų ir sandėlio valdymo parametrai**.
2. Pažymėkite skirtuką **Vietos**.
3. Lauke **Standartinis plotis** įveskite skaičių.
4. Lauke **Standartinis gylis** įveskite skaičių.
5. Lauke **Standartinis aukštis** įveskite skaičių.
6. Pasirinkite **Įrašyti**.
7. Uždarykite puslapį.

## <a name="define-the-location-name-format"></a>Nustatyti vietos pavadinimo formatą
1. Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Sąranka > Atsargų paskirstymas > Sandėliai**.
2. Pasirinkite **Naujas**.
3. Lauke **Sandėlis** įveskite reikšmę.
4. Lauke **Pavadinimas** įveskite reikšmę.
5. Lauke **Vieta** peržvalgoje pažymėkite pageidaujamą įrašą.
6. Perjunkite skyriaus **Vietos pavadinimai** išplėtimą. Parinktys šiame skyriuje nurodo numatytąjį vietos pavadinimų formatą. Savo pavyzdyje įtrauksime perėjimo numerį, stelažo numerį ir lentynos numerį.  
7. Pažymėkite parinktį **Įtraukti perėjimą** kaip **Taip**.
8. Pažymėkite parinktį **Įtraukti stelažą** kaip **Taip**. 
9. Lauke **Formatas** įveskite stelažo reikšmę.
10. Pažymėkite parinktį **Įtraukti lentyną** kaip **Taip**.
11. Lauke **Formatas** įveskite lentynos reikšmę.

## <a name="define-warehouse-locations"></a>Nustatyti sandėlio vietas
1. Veiksmų srityje pažymėkite **Sandėlis**.
2. Pažymėkite **Vietos vedlys**.
3. Pasirinkite **Toliau**.
4. Atžymėkite parinktį **Pakrovimo rampos**
5. Atžymėkite parinktį **Palaidų krovinių vietos**
6. Spauskite **Toliau**, kol galėsite pažymėti **Baigti**.
7. Uždarykite puslapį.
8. Atnaujinkite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]