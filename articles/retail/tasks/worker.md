---
title: " Konfigūruoti darbininką"
description: Šioje procedūroje parodoma, kaip mažmeninės prekybos darbuotoją sukonfigūruoti kaip pardavimo atstovą, kuriam taikomi EKA pardavimo komisiniai.
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 797640b487884fc487582addea274007e4ba7a7d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "362538"
---
# <a name="configure-a-worker"></a> Konfigūruoti darbininką

[!include[task guide banner](../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip mažmeninės prekybos darbuotoją sukonfigūruoti kaip pardavimo atstovą, kuriam taikomi EKA pardavimo komisiniai. Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.


## <a name="create-a-commission-sales-group-for-the-worker"></a>Darbuotojo pardavimo komisinių grupės kūrimas
1. Pasirinkite Pardavimai ir rinkodara > Komisiniai > Pardavimo grupės.
    * Darbuotojus galima priskirti vienai arba kelioms pardavimo grupėms. EKA galite pasirinkti bet kurią pardavimo grupę, kurioje yra darbuotojų iš parduotuvės adresų knygelės.  
2. Spustelėkite Naujas.
3. Lauke Grupė įveskite reikšmę.
4. Lauke Pavadinimas surinkite reikšmę.
5. Spustelėkite Įrašyti.
6. Veiksmų srityje spustelėkite Bendra.
7. Spustelėkite Pardavimo atstovas.
    * Pardavimo grupėje gali būti daugiau nei vienas darbuotojas. Komisinius darbuotojams galima paskirstyti pagal nustatytą komisinių dalį.  
8. Lauke Pavadinimas įveskite arba pasirinkite reikšmę.
9. Lauke Komisinių dalis įveskite skaičių.
10. Spustelėkite Įrašyti.
11. Uždarykite puslapį.
12. Uždarykite puslapį.

## <a name="assign-the-workers-default-sales-group"></a>Darbuotojų priskyrimas prie numatytosios pardavimo grupės
1. Eikite į Mažmeninė prekyba ir prekyba > Darbuotojai > Darbuotojai.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Spustelėkite skirtuką Mažmeninė prekyba.
    * Darbuotoją galima priskirti numatytajai pardavimo grupei. Numatytoji pardavimo grupė bus automatiškai įtraukti į EKA pardavimo eilutes, jei ši parinktis įjungta parduotuvės funkcijų profilyje.  
5. Spustelėkite Redaguoti.
6. Lauke Numatytoji grupė įveskite arba pasirinkite reikšmę.
7. Spustelėkite Įrašyti.

