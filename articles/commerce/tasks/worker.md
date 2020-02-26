---
title: " Konfigūruoti darbininką"
description: Šioje procedūroje parodoma, kaip darbininką sukonfigūruoti kaip pardavimo atstovą, kuriam taikomi EKA pardavimo komisiniai.
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
ms.openlocfilehash: aee84f2dc39d2225985992fac0f9c20985ed9804
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023391"
---
# <a name="configure-a-worker"></a> Konfigūruoti darbininką

[!include[task guide banner](../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip darbininką sukonfigūruoti kaip pardavimo atstovą, kuriam taikomi EKA pardavimo komisiniai. Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.


## <a name="create-a-commission-sales-group-for-the-worker"></a>Darbininko pardavimo komisinių grupės kūrimas
1. Pasirinkite Pardavimai ir rinkodara > Komisiniai > Pardavimo grupės.
    * Darbininkus galima priskirti vienai arba kelioms pardavimo grupėms. EKA galite pasirinkti bet kurią pardavimo grupę, kurioje yra darbininkų iš parduotuvės adresų knygelės.  
2. Spustelėkite Naujas.
3. Lauke Grupė įveskite reikšmę.
4. Lauke Pavadinimas surinkite reikšmę.
5. Spustelėkite Įrašyti.
6. Veiksmų srityje spustelėkite Bendra.
7. Spustelėkite Pardavimo atstovas.
    * Pardavimo grupėje gali būti daugiau nei vienas darbininkas. Komisinius darbininkams galima paskirstyti pagal nustatytą komisinių dalį.  
8. Lauke Pavadinimas įveskite arba pasirinkite reikšmę.
9. Lauke Komisinių dalis įveskite skaičių.
10. Spustelėkite Įrašyti.
11. Uždarykite puslapį.
12. Uždarykite puslapį.

## <a name="assign-the-workers-default-sales-group"></a>Darbininkų priskyrimas prie numatytosios pardavimo grupės
1. Eikite į Mažmeninė prekyba ir prekyba > Darbuotojai > Darbininkai.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Spustelėkite skirtuką Prekyba.
    * Darbininką galima priskirti numatytajai pardavimo grupei. Numatytoji pardavimo grupė bus automatiškai įtraukti į EKA pardavimo eilutes, jei ši parinktis įjungta parduotuvės funkcijų profilyje.  
5. Spustelėkite Redaguoti.
6. Lauke Numatytoji grupė įveskite arba pasirinkite reikšmę.
7. Spustelėkite Įrašyti.

