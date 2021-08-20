---
title: DUK apie finansines ataskaitas
description: Šioje temoje pateikiami atsakymai į kai kuriuos dažnai užduodamus klausimus apie finansines ataskaitas.
author: jiwo
ms.date: 07/07/2021
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
ms.openlocfilehash: dd493e855e45362c1681dc9cdfbbcb71f7627d64624cd093eadab32fd966c174
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733616"
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

## <a name="how-does-the-selection-of-historical-rate-translation-affect-report-performance"></a>Kokį poveikį ataskaitos efektyvumui turi retrospektyvinio kurso perskaičiavimo pasirinkimas?

Retrospektyvinis kursas paprastai naudojamas su nepaskirstyto pelno, turto, įrangos ir įrengimų bei kapitalo sąskaitomis. Retrospektyvinis kursas gali būti reikalingas, remiantis Finansinės atskaitomybės standartų valdybos (FASB) rekomendacijomis arba visuotiniais buhalterinės apskaitos principais (GAAP). Norėdami gauti daugiau informacijos žr. [Valiutos galimybės finansinėse ataskaitose](financial-reporting-currency-capability.md).

## <a name="how-many-types-of-currency-rate-are-there"></a>Kiek valiutos kurso tipų yra?

Yra trys tipai:

- **Dabartinis kursas** – šis tipas paprastai naudojamas su balanso sąskaitomis. Jis paprastai žinomas kaip *vietos valiutos kursas* ir gali būti kursas paskutinę mėnesio dieną arba kitą iš anksto nustatytą datą.
- **Vidutinis kursas** – šis tipas paprastai naudojamas su pajamų išrašo (pelnas / nuostoliai) sąskaitomis. Galite nustatyti vidutinį kursą, kad apskaičiuotumėte arba paprastą vidurkį, arba svertinį vidurkį.
- **Retrospektyvinis kursas** – šis tipas paprastai naudojamas su nepaskirstyto pelno, turto, įrangos ir įrengimų bei kapitalo sąskaitomis. Šių sąskaitų gali reikėti remiantis FASB arba GAAP rekomendacijomis.

## <a name="how-does-historical-currency-translation-work"></a>Kaip veikia retrospektyvinės valiutos perskaičiavimas?

Kursai yra būdingi operacijos datai. Todėl kiekviena operacija perskaičiuojama atskirai, atsižvelgiant į artimiausią valiutos kursą.

Retrospektyvinio valiutos perskaičiavimo atveju iš anksto apskaičiuoti laikotarpio balansai gali būti naudojami vietoje išsamios atskiros operacijos informacijos. Šis veikimo būdas skiriasi nuo dabartinio tarifo perskaičiavimo veikimo būdo.

## <a name="how-does-historical-currency-translation-affect-performance"></a>Kokį poveikį našumui turi retrospektyvinis valiutos perskaičiavimas?

Kai atnaujinami ataskaitose pateikti duomenys, galima delsa, nes sumos turi būti perskaičiuotos tikrinant išsamią operacijos informaciją. Ši delsa suaktyvinama kaskart, kai atnaujinami tarifai arba užregistruojama daugiau operacijų. Pavyzdžiui, jei retrospektyviniam perskaičiavimui nustatomos tūkstančiai sąskaitų kelis kartus per dieną, galima iki valandos trunkanti delsa prieš tai, kai bus atnaujinti ataskaitos duomenis. Kita vertus, jei yra mažesnis konkrečių sąskaitų skaičius, ataskaitos duomenų atnaujinimų apdorojimo laikas gali būti sutrumpintas iki minutės arba mažiau.

Be to, kai ataskaitos generuojamos naudojant retrospektyvinio tipo sąskaitų valiutos perskaičiavimą, bus papildomų operacijos skaičiavimų. Atsižvelgiant į sąskaitų skaičių, ataskaitos generavimo laikas gali būti dvigubai ilgesnis.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
