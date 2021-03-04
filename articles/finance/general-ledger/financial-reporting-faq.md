---
title: DUK apie finansines ataskaitas
description: Šioje temoje pateikiami klausimai, susiję su finansinėmis ataskaitomis, kurias turėjo kiti vartotojai.
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3f9381f5b656d0cc0b46c8828b2ef9d024e296b0
ms.sourcegitcommit: 14785208d84b2c1efd30f140c52df35a2ccd1577
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/27/2021
ms.locfileid: "5070222"
---
# <a name="financial-reporting-faq"></a>DUK apie finansines ataskaitas 

Šioje temoje pateikiami klausimai, susiję su finansinėmis ataskaitomis, kurias turėjo kiti vartotojai. 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Kaip apriboti prieigą prie ataskaitos naudojant medžio saugą?

Scenarijus: USMF demonstracinė įmonė turi balanso ataskaitą ir nenori, kad visi finansinių ataskaitų vartotojai galėtų peržiūrėti naudodami D365. Sprendimas: galite naudoti medžio saugą, kad apribotumėte prieigą prie vienos ataskaitos, kad tik tam tikri vartotojai galėtų pasiekti ataskaitą. 

1.  Prisijunkite prie finansinių ataskaitų rengėjų ataskaitų dizaino įrankio

2.  Sukurkite naują medžio apibrėžimą (Failas | Naujas | Medžio aprašas) a.    Dukart spustelėkite eilutę **Suvestinė** stulpelyje **Vieneto sauga**.
  i.    Spustelėkite Vartotojai ir grupės.  
          1. Pasirinkite vartotojus ar grupę, kuri galės pasiekti šią ataskaitą. 
          
[![vartotojo ekranas](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)

[![saugos ekranas](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)

  b.    Spustelėkite **Įrašyti**.
  
[![įrašymo mygtukas](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)

3.  Savo ataskaitos apraše įtraukite naują medžio aprašą

[![medžio aprašo forma](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)

A.  Medžio apraše spustelėkite Parametras ir dalyje Ataskaitos vieneto pasirinkimas pažymėkite Įtraukti visus vienetus

[![ataskaitos vieneto pasirinkimo forma](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)

**Prieš:** [![ekrano nuotrauka](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)

**Po:** [![ekrano nuotrauka](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)

Pastaba: pirmiau pateikto pranešimo priežastis ta, kad mano vartotojas neturi prieigos prie šios ataskaitos pritaikius vieneto saugą



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a>Kaip nustatyti, kurios sąskaitos neatitinka mano balansų D365?

Kai turite ataskaitą, kuri neatitinka to, ko tikitės iš D365, štai keli veiksmai, kuriuos galite atlikti norėdami nustatyti šias sąskaitas ir nukrypimus. 

### <a name="in-financial-reporter-report-designer"></a>Naudodami finansinių ataskaitų rengėjų ataskaitų dizaino įrankį

1.  Sukurkite naują eilutės aprašą a.    Spustelėkite Redaguoti | Įterpti eilutes iš dimensijų i.  Pasirinkite MainAccount [![Pasirinkite Pagrindinis ekranas_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)
    
    ii. Spustelėkite Gerai b.    Eilutės aprašo įrašymas

2.  Naujo stulpelio aprašo kūrimas [![Naujo stulpelio aprašo kūrimas](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)

3.  Sukurkite naują ataskaitos aprašą a.    Spustelėkite Parametrai ir atžymėkite [![formą Parametrai](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)
   
4.  Generuokite ataskaitą. 

5.  Eksportuokite ataskaitą į „Excel“.

### <a name="in-d365"></a>Naudodami D365: 
1.  Spustelėkite DK | Užklausos ir ataskaitos | Bandomasis balansas a.    Parametrai i.  Pradžios data: finansinių metų pradžia ii. Pabaigos data: data, kuriai sugeneravote ataskaitą iii.    Finansinių dimensijų rinkinys „Pagrindinės sąskaitos rinkinys“ [![Pagrindinės sąskaitos forma](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)
      
  b.    Spustelėkite Skaičiuoti

2.  Ataskaitos eksportavimas į „Excel“

Dabar turėtų būti galima kopijuoti duomenis iš FR „Excel“ ataskaitos į D365 bandomojo balanso ataskaitą ir palyginti uždarymo balanso stulpelius.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]