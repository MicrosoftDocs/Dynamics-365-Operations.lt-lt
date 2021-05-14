---
title: DUK apie finansines ataskaitas
description: Šioje temoje pateikiami klausimai, susiję su finansinėmis ataskaitomis, kurias turėjo kiti vartotojai.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923030"
---
# <a name="financial-reporting-faq"></a>DUK apie finansines ataskaitas 

Šioje temoje pateikiami atsakymai į dažnai užduodamus klausimus apie finansines ataskaitas. 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Kaip apriboti prieigą prie ataskaitos naudojant medžio saugą?

Toliau pateikiamu pavyzdžiu nurodoma, kaip apriboti prieigą prie ataskaitos naudojant medžio saugą.

Demonstracinė įmonė USMF turi balanso ataskaitą, prie kurios ne visi finansinių ataskaitų vartotojai turi turėti prieigą. Norėdami apriboti prieigą galite naudoti medžio saugą, kad apribotumėte prieigą prie vienos ataskaitos ir tik tam tikri vartotojai galėtų pasiekti ataskaitą. Norėdami apriboti prieigą, atlikite šiuos veiksmus: 

1. Prisijunkite prie „Financial Reporter Report Designer“.
2. Sukurkite naują medžio aprašą. Eikite į **Failas > Naujas > Medžio aprašas**.
3. Dukart spustelėkite eilutę **Suvestinė** stulpelyje **Vieneto sauga**.
4. Pasirinkite **Vartotojai ir grupės**.  
5. Pasirinkite vartotojus ar grupes, kuriems reikalinga prieiga prie ataskaitos. 
6. Pasirinkite **Įrašyti**.
7. Į ataskaitos aprašą įtraukite naują medžio aprašą.
8. Medžio apraše pasirinkite **Parametras**. Dalyje **Ataskaitos vieneto pasirinkimas** pasirinkite **Įtraukti visus vienetus**.

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a>Kaip nustatyti, kurios sąskaitos neatitinka mano balansų?

Jei turite ataskaitą, kurioje nėra atitinkančių balansų, štai keli veiksmai, kuriuos galite atlikti norėdami nustatyti kiekvieną sąskaitą ir nukrypimą. 

**„Financial Reporter Report Designer“**
1. Naudodami „Financial Reporter Report Designer“, sukurkite naują eilutės aprašą. 
2. Pasirinkite **Redaguoti > Įterpti eilutes iš dimensijų**.
3. Pasirinkite **Pagrindinė sąskaita**.  
4. Pasirinkite **Gerai**.
5. Įrašykite eilutės aprašą.
6. Sukurkite naują eilutės aprašą
7. Sukurkite naują ataskaitos aprašą.
8. Pasirinkite **Parametrai** ir atžymėkite šią parinktį.  
9. Generuokite ataskaitą. 
10. Eksportuokite ataskaitą į „Microsoft Excel“.

**„Dynamics 365 Finance“** 
1. „Dynamics 365 Finance“ eikite į **Didžioji knyga > Užklausos ir ataskaitos > Bandomasis balansas**.
2. Nustatykite šiuos parametrus:
   - **Pradžios data** – įveskite finansinių metų pradžią.
   - **Pabaigos data** – įveskite datą, kuriai generuojate ataskaitą.
   - **Finansinė dimensija** – nustatykite šį lauką kaip **Pagrindinė sąskaita nustatyta**.
 3. Pasirinkite **Skaičiuoti**.
 4. Eksportuokite ataskaitą į „Microsoft Excel“.

Dabar turėtų būti galima kopijuoti duomenis iš finansinių ataskaitų rengėjų „Excel“ ataskaitos į bandomojo balanso ataskaitą, kad galėtumėte palyginti **uždarymo balanso** stulpelius.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]