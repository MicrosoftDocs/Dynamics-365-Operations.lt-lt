---
title: Atostogų pirkimo ir pardavimo strategijų valdymas
description: Galite suteikti darbuotojams galimybę pirkti ir parduoti atostogas programoje „Dynamics 365 Human Resources“.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429018"
---
# <a name="manage-buy-and-sell-leave-policies"></a>Atostogų pirkimo ir pardavimo strategijų valdymas

[!include [banner](includes/preview-feature.md)]

Galite suteikti darbuotojams galimybę pirkti atostogas, kurdami pirkimo atostogų strategiją.  

## <a name="enable-employees-to-buy-and-sell-leave"></a>Suteikite darbuotojams galimybę pirkti ir parduoti atostogas

1. Puslapyje **Atostogų parametrai** pasirinkite **Taip**, jei norite **Leisti darbuotojams pirkti atostogas**. 

## <a name="create-a-buy-leave-policy"></a>Atostogų pirkimo strategijos kūrimas

1. Puslapyje **Atostogos ir neatvykimai** pasirinkite skirtuką **Saitai**. 

2. Pasirinkite **Atostogų pirkimo ir pardavimo strategija**.

3. Pasirinkite **Naujas**.

4. Įveskite strategijos **Pavadinimą** ir **Aprašą** dalyje **Atostogų pirkimo ir pardavimo strategija**. 

5. Pasirinkite **Strategijos tipas**. 

   Galimi strategijos tipai yra **Kiekis** ir **Valandos per savaitę**. Pasirinkite **Kiekis**, kad įvestumėte **Fiksuotą kiekį** maksimaliam kiekiui, kurį gali pirkti ir parduoti darbuotojai. Jei pasirinksite **Valandos per savaitę**, darbo laikas, nurodytas darbuotojo priskirtame darbo laiko kalendoriuje, naudojamas nustatyti maksimaliam strategijos kiekiui. 

6. Pasirinkite strategijos **Pradžios datą** ir **Pabaigos datą**. Atostogų pirkimo ir pardavimo prašymus bus galima pateikti tik šiuo laikotarpiu. 

7. Dalyje **Pirkimo strategija** pasirinkite **Visos darbo dienos ekvivalentiškumas** (FTE), norėdami proporcingai paskirstyti maksimalų kiekį pagal FTE, apibrėžtą darbuotojo pareigose. Jei strategijos tipas yra **Kiekis**, įveskite **Maksimalus fiksuotas kiekis**. 

8. Pasirinkite **Įtraukti**, kad įtrauktumėte darbuotojų atostogų tipus, kad būtų galima pirkti atostogas. Prie strategijos galite pridėti keletą atostogų tipų. 

9. Norėdami nustatyti maksimalų kiekį, kurį gali įsigyti darbuotojas, įveskite **Darbo mėnesiai**, kad būtų įjungti skirtingi paslaugų mėnesiai. 

10. Įveskite atostogų tipo **Maksimalų kiekį**. 

11. Įveskite **Įkainį**, kuriuo darbuotojas įsigys atostogų. 

12. Pasirinktinai įveskite **Uždarbio kodą,** kuris bus naudojamas perkant atostogas. 

13. Pasirinktinai nustatykite, ar naudoti FTE, kad būtų galima nustatyti maksimalų atostogų tipo kiekį. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>Atostogų pirkimo ir pardavimo strategijos įtraukimas į atostogų planą

1. Puslapyje **Atostogos** pasirinkite atostogų planą.

2. Dalyje **Taisyklės** pasirinkite **Atostogų pirkimo ir pardavimo strategija**.

## <a name="see-also"></a>Taip pat žiūrėkite

[Atostogų ir neatvykimų apžvalga](hr-leave-and-absence-overview.md)</br>
[Atostogų ir neatvykimų tipų konfigūravimas](hr-leave-and-absence-types.md)</br>
[Sukauptų atostogų ir neatvykimų planai](hr-leave-and-absence-accrue.md)</br>
[Atostogų pirkimas ir pardavimas](hr-employee-self-service-buy-sell-leave.md)

