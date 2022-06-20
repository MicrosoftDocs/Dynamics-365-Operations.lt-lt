---
title: Laiko ir lankomumo valdymo planavimas dalyje Mažmeninė prekyba
description: Šiame straipsnyje aprašomi scenarijai, kuriuos palaiko laiko ir lankomumo valdymas dalyje Dynamics 365 Commerce.
author: aamirallaqaband
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 75c09d9e98a08bec0697b0b522ba6e647d35b140
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855733"
---
# <a name="time-and-attendance-management-in-retail"></a>Laiko ir lankomumo valdymo planavimas dalyje Mažmeninė prekyba

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomi scenarijai, kuriuos palaiko laiko ir lankomumo valdymas dalyje Dynamics 365 Commerce.

## <a name="manage-worker-setup-and-scheduling"></a>Valdyti darbininko nustatymą ir planavimą

### <a name="initial-configuration"></a>Pradinė konfigūracija

- Paleiskite konfigūracijos vedlį.
- Registruokite darbuotojus kaip laiko registracijos darbuotojus.

### <a name="plan-worker-schedules"></a>Planuokite darbuotojų grafikus

- Taikykite šablonus naudodami darbo planuotoją. Daugiau informacijos žr. [Šablonų taikymas naudojant darbo planuotoją](/dynamicsax-2012/appuser-itpro/apply-profiles-using-work-planner).

Informacijos apie konfigūravimo veiksmus žr. [Laiko ir buvimo darbe nustatymas](/dynamicsax-2012/appuser-itpro/setting-up-time-and-attendance).

### <a name="commerce-specific-configuration"></a>Konkrečios „Commerce“ konfigūracija

- Įjunkite laikrodžio funkcijų šabloną darbuotojams, kuriems norite leisti laiko registravimus. Spustelėkite **EKA funkcijų šablonai** &gt; **Funkcijos** &gt; **EKA laiko registravimai** &gt; **Įjungti laiko registravimus**.
- Sukonfigūruokite elektroninio kasos aparato (EKA) teisių grupes, kad leistumėte teisę Peržiūrėti laikrodžio įrašus. Naudodamas šią teisę vartotojas gali peržiūrėti kitų parduotuvės (ir bet kurios kitos parduotuvės, su kuria vartotojas susietas per adresų knygelę) darbuotojų laikrodžio registravimus. Galite įjungti šią teisę vadovo vaidmeniui, bet ne kasininko vaidmeniui. Spustelėkite **EKA teisių grupės** &gt; **Peržiūrėti laikrodžio įrašus**.

## <a name="register-time"></a>Registracijos laikas

### <a name="cashier-and-non-cashier-time-registrations"></a>Kasininko ir ne kasininko laiko registravimai

- EKA

    - Atėjimo į darbą operacijos

        - Prisijunkite naudodami ne stalčiaus operaciją arba naują pamainą.
        - Pasirinkite laikrodžio operaciją.
        - Pasirinkite norimą operaciją.

            - Atėjimas į darbą
            - Darbo pertrauka
            - Pietų pertrauka
            - Išėjimas iš darbo

        <table>
        <thead>
        <tr>
        <th>Dabartinė būsena</th>
        <th>Galimos operacijos</th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td>Atėjimas į darbą</td>
        <td>
        <ul>
        <li>Darbo pertrauka</li>
        <li>Pietų pertrauka</li>
        <li>Išėjimas iš darbo</li>
        </ul>
        </td>
        </tr>
        <tr>
        <td>Darbo pertrauka</td>
        <td>Atėjimas į darbą</td>
        </tr>
        <tr>
        <td>Pietų pertrauka</td>
        <td>Atėjimas į darbą</td>
        </tr>
        <tr>
        <td>Išėjimas iš darbo</td>
        <td>Atėjimas į darbą</td>
        </tr>
        </tbody>
        </table>

        [![Laikrodžio būsenos.](./media/timeclockstates.png)](./media/timeclockstates.png)

- Peržiūrėkite patvirtinimo pranešimą ir patikrinkite, ar dabartinis veiklos laikas yra teisingas.
- Registracijos žurnalas

    - Spustelėkite **Registracijos žurnalas** laikrodžio veiklai peržiūrėti.
    - Naudokite laiko filtrus, norėdami pasirinkti skirtingus laiko langus.
    - Jei dirbate keliose parduotuvių vietose, matysite savo laiko registravimus visose parduotuvėse, kuriose įrašėte laiką. Galite naudoti parduotuvių filtrą, norėdami peržiūrėti pasirinktos parduotuvės laiko registravimus.

- Skirtingos laiko juostos

    - Jei peržiūrite kitos vietos laiką (naudodami kasininko registracijos žurnalą arba vadovo vaidmens scenarijaus parinktį **Peržiūrėti laiko įrašus**) ir ta vieta yra kitoje laiko juostoje, rodomi laiko įrašai yra konvertuojami į jūsų vietos laiko juostą. Pvz., jūs esate dviejų parduotuvių (Arizonoje ir Nevadoje) vadovas. Kasininkas registruoja atėjimą į darbą 9:00 Arizonos laiku. Tuo metu Nevadoje yra 8:00. Todėl, jei esate Nevados parduotuvėje ir pažiūrite laiko registravimo įrašus, laiko registravimas pažymėtas 8:00.

## <a name="view-worker-time-registrations"></a>Peržiūrėti darbuotojų laiko registravimą

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Darbuotojų laiko registravimų peržiūra ir filtravimas pagal parduotuvę arba veiklos tipą

EKA

- Pasirinkite **Peržiūrėti laikrodžio įrašus**.
- Galite matyti visų darbuotojų, kurie priskirti toms pačioms parduotuvėms, kaip ir jūs, laikrodžio registravimus.
- Galite naudoti veiklos tipo ir parduotuvės filtrus laiko registravimams filtruoti.

## <a name="process-and-manage-time-registrations"></a>Apdoroti ir valdyti darbuotojų laiko registravimą

„Commerce“ vartotojas seka darbo eigą, kad apskaičiuotų, patvirtintų ir perkeltų laiko registravimą į algalapį.

### <a name="primary-operations"></a>Pirminės operacijos

- Skaičiuoti
- Patvirtinti
- Pateikti į algalapį

### <a name="other-common-operations"></a>Kitos įprastos operacijos

- Masinis išėjimas iš darbo
- Registruoti neatvykimą

Daugiau informacijos apie tai, kaip apdoroti laiko ir buvimo darbe registravimus, žr. [Laiko ir buvimo darbe registravimų apdorojimas](/dynamicsax-2012/appuser-itpro/process-time-and-attendance-registrations).


[!INCLUDE[footer-include](../includes/footer-banner.md)]