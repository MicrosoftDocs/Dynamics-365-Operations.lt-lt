---
title: DUK apie finansines ataskaitas
description: Šioje temoje pateikiami atsakymai į kai kuriuos dažnai užduodamus klausimus apie finansines ataskaitas.
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
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266638"
---
# <a name="financial-reporting-faq"></a>DUK apie finansines ataskaitas

Šioje temoje pateikiami atsakymai į dažnai užduodamus klausimus apie finansines ataskaitas.

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a>Kaip apriboti prieigą prie ataskaitos naudojant medžio saugą?

Toliau pateikiamu pavyzdžiu nurodoma, kaip apriboti prieigą prie ataskaitos naudojant medžio saugą.

Demonstracinė įmonė USMF turi **balanso ataskaitą** , prie kurios ne visi finansinių ataskaitų vartotojai turi turėti prieigą. Galite naudoti medžio saugą, kad apribotumėte prieigą prie vienos ataskaitos, kad tik tam tikri vartotojai galėtų ją pasiekti.

1. Prisijungti prie „Financial Reporter Report Designer”.
2. Pasirinkite **Failas \> Naujas \> Medžio aprašas**, kad sukurtumėte naują medžio aprašą.
3. Dukart bakstelėkite (arba dukart spustelėkite) eilutę **Suvestinė** stulpelyje **Vieneto sauga**.
4. Pasirinkite **Vartotojai ir grupės**.
5. Pasirinkite vartotojus ar grupes, kuriems reikalinga prieiga prie ataskaitos.
6. Pasirinkite **Įrašyti**.
7. Į ataskaitos aprašą įtraukite naują medžio aprašą.
8. Medžio apraše pasirinkite **Parametras**. Tada dalyje **Ataskaitos vieneto pasirinkimas** pasirinkite **Įtraukti visus vienetus**.

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a>Kaip nustatyti, kurios sąskaitos neatitinka mano balansų?

Jei turite ataskaitą, kurioje nėra atitinkančių balansų, naudokite toliau pateikiamas procedūras norėdami nustatyti kiekvieną paskyrą ir nukrypimą.

### <a name="in-financial-reporter-report-designer"></a>„Financial Reporter Report Designer“

1. Sukurkite naują eilutės aprašą.
2. Pasirinkite **Redaguoti \> Įterpti eilutes iš dimensijų**.
3. Pasirinkite **MainAccount**.
4. Pasirinkite **Gerai**.
5. Įrašykite eilutės aprašą.
6. Sukurkite naują stulpelio aprašą.
7. Sukurkite naują ataskaitos aprašą.
8. Pasirinkite **Parametrai** ir atžymėkite šią parinktį.
9. Generuokite ataskaitą. 
10. Eksportuokite ataskaitą į „Microsoft Excel“.

### <a name="in-dynamics-365-finance"></a>„Dynamics 365 Finance“

1. Eikite į **Didžioji knyga \> Užklausos ir ataskaitos \> Bandomasis balansas**.
2. Užpildykite toliau nurodytus laukus:

    - **Pradžios data** – įveskite finansinių metų pradžios datą.
    - **Pabaigos data** – įveskite datą, kuriai generuojate ataskaitą.
    - **Finansinė dimensija** – nustatykite šį lauką kaip **Pagrindinė sąskaita nustatyta**.

3. Pasirinkite **Skaičiuoti**.
4. Eksportuokite ataskaitą į „Excel“.

Dabar turėtų būti galima kopijuoti duomenis iš „Financial Reporter“ „Excel“ ataskaitos į **bandomojo balanso** ataskaitą, kad galėtumėte palyginti **uždarymo balanso** stulpelius.

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a>Kai kuriu ataskaitą „Report Designer“ arba generuoju finansinę ataskaitą, gaunu šį pranešimą: „Operacijos nepavyko užbaigti dėl duomenų teikėjo sistemos problemos“. Kaip turėčiau atsakyti?

Pranešimas nurodo, kad problema įvyko, kai sistema bandė nuskaityti finansinius metaduomenis iš duomenų srities, kol naudojote finansines ataskaitas. Yra du būdai atsakyti į šią problemą:

- Peržiūrėkite duomenų integravimo būseną „Report Designer“ eidami į **Įrankiai \> Integravimo būsena**. Jei integravimas neužbaigtas, palaukite, kol jis bus baigtas. Tada, kartokite tai, ką darėte, kai gavote pranešimą.
- Norėdami nustatyti ir išspręsti problemą, susisiekite su palaikymo tarnyba. Sistemoje gali būti pateikti nenuoseklūs duomenys. Palaikymo inžinieriai gali padėti nustatyti problemą serveryje ir rasti konkrečius duomenis, kuriuos gali reikėti atnaujinti.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
