---
title: Konfigūruoti darbininką
description: Šioje procedūroje parodoma, kaip darbininką sukonfigūruoti kaip pardavimo atstovą, kuriam taikomi EKA pardavimo komisiniai.
author: jblucher
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a21d5f2d5963db2a92b653e8e520f96f11ba1bf6acbb238812211154d5b39fc0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726388"
---
# <a name="configure-a-worker"></a>Konfigūruoti darbininką

[!include [banner](../includes/banner.md)]

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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]