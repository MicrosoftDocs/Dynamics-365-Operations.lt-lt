---
title: "„Retail“ laikas ir buvimas darbe"
description: "Šioje temoje aprašoma scenarijai, kuriuos palaiko Microsoft Dynamics 365 operacijų - mažmeninės prekybos laiką ir lankomumą valdymo."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: eac0b85a17df33c860333c5c19d4fb58f160930f
ms.lasthandoff: 03/31/2017


---

# <a name="retail-time-and-attendance"></a>„Retail“ laikas ir buvimas darbe

Šioje temoje aprašoma scenarijai, kuriuos palaiko Microsoft Dynamics 365 operacijų - mažmeninės prekybos laiką ir lankomumą valdymo. 

<a name="manage-worker-setup-and-scheduling"></a>Valdyti darbuotojo nustatymas ir planavimas
----------------------------------

### <a name="initial-configuration"></a> pradinė konfigūracija

-   Paleiskite konfigūracijos vedlį.
-   Registruokite darbuotojus kaip laiko registracijos darbuotojus.

### <a name="plan-worker-schedules"></a>Planuokite darbuotojų grafikus

-   Taikykite šablonus naudodami darbo planuotoją. Daugiau informacijos žr. <https://technet.microsoft.com/en-us/library/aa551234.aspx>.

Informacijos apie konfigūravimo veiksmus žr. <https://technet.microsoft.com/en-us/library/aa496971.aspx>.

### <a name="retail-specific-configuration"></a>Konkretus mažmeninės prekybos konfigūravimas

-   Įjunkite laikrodžio funkcijų šabloną darbuotojams, kuriems norite leisti laiko registravimus. Spustelėkite **POS funkcijų šablonų**&gt;**funkcijos**&gt;**POS laiko registracijos**&gt;**leisti laiką registracijos**.
-   Sukonfigūruokite elektroninio kasos aparato (EKA) teisių grupes, kad leistumėte teisę Peržiūrėti laikrodžio įrašus. Naudodamas šią teisę vartotojas gali peržiūrėti kitų parduotuvės (ir bet kurios kitos parduotuvės, su kuria vartotojas susietas per adresų knygelę) darbuotojų laikrodžio registravimus. Galite įjungti šią teisę vadovo vaidmeniui, bet ne kasininko vaidmeniui. Spustelėkite **POS teisių grupėms**&gt;**tikr± laiko laikrodis**.

## <a name="register-time"></a>Registracijos laikas
### <a name="cashier-and-non-cashier-time-registrations"></a>Kasininko ir ne kasininko laiko registravimai

-   EKA
    -   Atėjimo į darbą operacijos
        -   Prisijunkite naudodami ne stalčiaus operaciją arba naują pamainą.
        -   Pasirinkite laikrodžio operaciją.
        -   Pasirinkite norimą operaciją.
            -   Atėjimas į darbą
            -   Darbo pertrauka
            -   Pietų pertrauka
            -   Išėjimas iš darbo

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Dabartinė būsena</th>
    <th>Galimos operacijos</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Atėjimas į darbą</td>
    <td><ul>
    <li>Darbo pertrauka</li>
    <li>Pietų pertrauka</li>
    <li>Išėjimas iš darbo</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Darbo pertrauka</td>
    <td>Atėjimas į darbą</td>
    </tr>
    <tr class="odd">
    <td>Pietų pertrauka</td>
    <td>Atėjimas į darbą</td>
    </tr>
    <tr class="even">
    <td>Išėjimas iš darbo</td>
    <td>Atėjimas į darbą</td>
    </tr>
    </tbody>
    </table>

    [![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)
-   Peržiūrėkite patvirtinimo pranešimą ir patikrinkite, ar dabartinis veiklos laikas yra teisingas.
-   Registracijos žurnalas
    -   Spustelėkite **Registracijos žurnalas** laikrodžio veiklai peržiūrėti.
    -   Naudokite laiko filtrus, norėdami pasirinkti skirtingus laiko langus.
    -   Jei dirbate keliose parduotuvių vietose, matysite savo laiko registravimus visose parduotuvėse, kuriose įrašėte laiką. Galite naudoti parduotuvių filtrą, norėdami peržiūrėti pasirinktos parduotuvės laiko registravimus.

<!-- -->

-   Skirtingos laiko juostos
    -   Jei peržiūrite kitos vietos laiką (naudodami kasininko registracijos žurnalą arba vadovo vaidmens scenarijaus parinktį **Peržiūrėti laiko įrašus**) ir ta vieta yra kitoje laiko juostoje, rodomi laiko įrašai yra konvertuojami į jūsų vietos laiko juostą. Pavyzdžiui, jūs esate už dvi parduotuvės vadybininkas, Arizona ir Nevada. Kasininkas registrai yra laikrodis-9:00 am Arizona. Tuo metu Nevadoje yra 8:00. Todėl, jei esate Nevados parduotuvėje ir pažiūrite laiko registravimo įrašus, laiko registravimas pažymėtas 8:00.

## <a name="view-worker-time-registrations"></a>Peržiūrėti darbuotojo laiko registracija
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Darbuotojų laiko registravimų peržiūra ir filtravimas pagal parduotuvę arba veiklos tipą

EKA

-   Pasirinkite **Peržiūrėti laikrodžio įrašus**.
-   Galite matyti visų darbuotojų, kurie priskirti toms pačioms parduotuvėms, kaip ir jūs, laikrodžio registravimus.
-   Galite naudoti veiklos tipo ir parduotuvės filtrus laiko registravimams filtruoti.

## <a name="process-and-manage-time-registrations"></a>Tvarkyti ir valdyti registracijos metu
Dynamics 365 operacijų - mažmeninės vartotojas toliau skaičiuoti, tvirtinti ir perkelti laiko registracijas į darbo užmokesčio darbo eigą.

### <a name="primary-operations"></a>Pirminės operacijos

-   Skaičiuoti
-   Patvirtinti
-   Pateikti į algalapį

### <a name="other-common-operations"></a>Kitos įprastos operacijos

-   Masinis išėjimas iš darbo
-   Registruoti neatvykimą

Daugiau informacijos apie tai, kaip apdoroti laiko ir lankomumo registravimus, žr. <https://technet.microsoft.com/en-us/library/aa573180.aspx>.


