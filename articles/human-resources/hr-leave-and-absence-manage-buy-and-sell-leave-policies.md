---
title: Atostogų pirkimo ir pardavimo strategijų valdymas
description: Galite suteikti darbuotojams galimybę pirkti ir parduoti atostogas programoje „Dynamics 365 Human Resources“.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1fe7ce7eafdec175e3395a6ac37b33cb2bb8dbda
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066680"
---
# <a name="manage-buy-and-sell-leave-policies"></a>Atostogų pirkimo ir pardavimo strategijų valdymas


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Galite įgalinti darbuotojus pirkti ir parduoti atostogas, sukuriant atostogų pirkimo ir pardavimo strategiją. Galite konfigūruoti šias strategijas, kad galėtumėte naudotis darbo eiga patvirtinimams, nustatyti maksimalias sumas bei tarifus, ir nustatyti pirkimo ir pardavimo tarifus. 

## <a name="enable-employees-to-buy-and-sell-leave"></a>Suteikite darbuotojams galimybę pirkti ir parduoti atostogas

1. **Atostogų ir neatvykimų parametrų** puslapyje, **Leisti darbuotojams pirkti atostogas** ir **Leisti darbuotojams parduoti atostogas** dalyse, pasirinkite **Taip**.

## <a name="create-a-buy-and-sell-leave-policy"></a>Sukurkite atostogų pirkimo ir pardavimo strategiją

1. Puslapyje **Atostogos ir neatvykimai** pasirinkite skirtuką **Saitai**. 

2. Pasirinkite **Atostogų pirkimo ir pardavimo strategija**.

3. Pasirinkite **Naujas**.

4. Įveskite strategijos **Pavadinimą** ir **Aprašą** dalyje **Atostogų pirkimo ir pardavimo strategija**. 

5. Pasirinkite **Strategijos tipas**. 

   Galimi strategijos tipai yra **Kiekis** ir **Valandos per savaitę**. Pasirinkite **Kiekis**, kad įvestumėte **Fiksuotą kiekį** maksimaliam kiekiui, kurį gali pirkti ir parduoti darbuotojai. Jei pasirinksite **Valandos per savaitę**, darbo laikas, nurodytas darbuotojo priskirtame darbo laiko kalendoriuje, naudojamas nustatyti maksimaliam strategijos kiekiui. 

6. Pasirinkite strategijos **Pradžios datą** ir **Pabaigos datą**. Atostogų pirkimo ir pardavimo prašymus bus galima pateikti tik šiuo laikotarpiu. 

7. Parinkite **Darbo eigos ID** strategijai. Bet kurioms pirkimo ir pardavimo užklausoms bus naudojama ši darbo eiga peržiūrai ir patvirtinimui. 

8. Dalyje **Pirkimo strategija** pasirinkite **Visos darbo dienos ekvivalentiškumas** (FTE), norėdami proporcingai paskirstyti maksimalų kiekį pagal FTE, apibrėžtą darbuotojo pareigose. Jei strategijos tipas yra **Kiekis**, įveskite **Maksimalus fiksuotas kiekis**. 

9. Pasirinkite **Įtraukti**, kad įtrauktumėte darbuotojų atostogų tipus, kad būtų galima pirkti atostogas. Prie strategijos galite pridėti keletą atostogų tipų. 

10. Norėdami nustatyti maksimalų kiekį, kurį gali įsigyti darbuotojas, įveskite **Darbo mėnesiai**, kad būtų įjungti skirtingi paslaugų mėnesiai. 

11. Įveskite atostogų tipo **Maksimalų kiekį**. 

12. Įveskite **Įkainį**, kuriuo darbuotojas įsigys atostogų. 

13. Pasirinktinai įveskite **Uždarbio kodą,** kuris bus naudojamas perkant atostogas. 

14. Pasirinktinai nustatykite, ar naudoti FTE, kad būtų galima nustatyti maksimalų atostogų tipo kiekį. 

15. Tam, kad sukurtumėte ir parduotumėte strategiją, sekite 8–14 žingsnius, esančius po **Parduoti strategiją**. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>Atostogų pirkimo ir pardavimo strategijos įtraukimas į atostogų planą

1. Puslapyje **Atostogos** pasirinkite atostogų planą.

2. Dalyje **Taisyklės** pasirinkite **Atostogų pirkimo ir pardavimo strategija**.

## <a name="see-also"></a>Taip pat žiūrėkite

[Atostogų ir neatvykimų apžvalga](hr-leave-and-absence-overview.md)</br>
[Atostogų ir neatvykimų tipų konfigūravimas](hr-leave-and-absence-types.md)</br>
[Sukauptų atostogų ir neatvykimų planai](hr-leave-and-absence-accrue.md)</br>
[Atostogų pirkimas ir pardavimas](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
