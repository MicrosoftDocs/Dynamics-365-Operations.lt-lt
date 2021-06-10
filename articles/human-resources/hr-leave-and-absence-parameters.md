---
title: Atostogų ir neatvykimų parametrų konfigūravimas
description: Žmogiškųjų išteklių parametrų, skirtų atostogoms ir neatvykimams, nustatymas programoje „Dynamics 365 Human Resources“.
author: andreabichsel
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c3a3f4a8a1fa0b5dbc4869f81f091cc66437e978
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056857"
---
# <a name="configure-leave-and-absence-parameters"></a>Atostogų ir neatvykimų parametrų konfigūravimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Prieš nustatant atostogų ir neatvykimų planus „Dynamics 365 Human Resources“, naudinga patikrinti visus susijusius žmogiškųjų išteklių parametrų nustatymus, įskaitant:

- Atostogų užklausų numeraciją
- Nedarbingumo dėl ligos ar slaugymo akto (FMLA) parametrus
- Darbuotojo atostogų ir neatvykimų užklausų savitarnos parametrus
- Atostogų ir neatvykimų parametrai

## <a name="view-and-change-human-resources-parameters"></a>Peržiūrėti ir keisti žmogiškųjų išteklių parametrus

1. Puslapyje **Atostogos ir neatvykimai** pasirinkite skirtuką **Saitai**.

2. Dalyje **Sąranka** pasirinkite **Žmogiškųjų išteklių parametrai**.

3. Skirtuke **Numeracija** patikrinkite **numeracijos kodą**, skirtą **atostogų užklausos ID**, ir pakeiskite, jeigu reikia. Šiuo parametru nustatoma seka, naudojama automatiškai priskirti ID atostogų užklausoms.

4. Skirtuke **FMLA** patikrinkite FMLA parametrus ir pakeiskite, jei reikia.

5. Skirtuke **Darbuotojo savitarna** nurodykite, ar vadybininkai savo darbuotojų vardu gali įvesti atostogų ir neatvykimų užklausas.

7. Pasirinkite **Įrašyti**.

>[!IMPORTANT]
>Atostogų ir nebuvo darbe peržiūra visose įmonėse šiuo metu yra išankstinėje peržiūroje. Jums reikės įjungti jį savo **Smėlio dėžės** aplinkoje, kad matytumėte parinktį atostogoms ir nebuvimui darbe. Daugiau informacijos apie peržiūros versijos funkcijų įjungimą žr. [Funkcijų valdymas](hr-admin-manage-features.md).

## <a name="view-and-change-human-resources-shared-parameters"></a>Peržiūrėti ir keisti žmogiškųjų išteklių bendrintus parametrus

1. Puslapyje **Personalo valdymas** rinkitės **Nuorodų** skirtuką.

2. Skyriuje **Nustatymai**, Rinkitės **žmogiškųjų išteklių bendrinti parametrai**.

3. Skirtuke **Papildoma prieiga** rinkitės **Taip** norėdami **Įjungti kryžminę įmonės atostogų peržiūrą** tam, kad atostogos būtų matomos visose įmonėse.

4. Pasirinkite **Įrašyti**.

## <a name="view-and-change-leave-and-absence-parameters"></a>Peržiūrėti ir keisti atostogų ir neatvykimų parametrus

1. Puslapyje **Atostogos ir neatvykimai** pasirinkite skirtuką **Saitai**.

2. Dalyje **Sąranka** pasirinkite **Atostogų ir neatvykimų parametrai**.

3. Skirtuke **Bendra** nustatykite tolesnius parametrus.
 
    - Nustatykite **Atostogų ir neatvykimų vienetas** į valandas arba dienas. Jei nustatėte dienas, galite pasirinkti **Įjungti pusės dienos apibrėžtį**, kad darbuotojai galėtų pasirinkti pirmąją ar antrą dienos pusę prašymuose išleisti iš darbo. 

    - Pasirinkite **Paslaugos įsigaliojimo datos mėnesiai**, kad nustatytumėte, kada atostogų planų, naudojančių darbo mėnesius, kaupimo tarifai įsigalios.

    - Pasirinkite **Balanso skaičiavimas** rodyti balansams nuo šiandien arba nuo kaupimo laikotarpio. Jei pasirinksite **Šiandienos balansas**, balansas rodys visus šiandienos kaupimus, koregavimus ir užklausas. Jei pasirinksite **Kaupimo laikotarpio balansas**, balansas rodys visus kaupimo laikotarpio, nustatyto pagal atostogų plano dažnumą, kaupimus, koregavimus ir užklausas. 

    - Nustatykite pradžios laiką paketinės užduoties galiojimo pabaigai perkelti.  
    
    - Pasirinkite **Taip** dalyse **Leisti darbuotojams pirkti atostogas** ir **Leisti darbuotojams parduoti atostogas**. Jei pasirinksite **Taip** šioms parinktims, galite kurti atostogų pirkimo ir pardavimo strategijas ir įgalinti darbuotojus pateikti atostogų pirkimo ir pardavimo užklausas.

## <a name="configure-calendar-parameters"></a>Kalendoriaus parametrų konfigūravimas

1. Puslapyje **Atostogos ir neatvykimai** pasirinkite skirtuką **Saitai**.

2. Dalyje **Sąranka** pasirinkite **Atostogų ir neatvykimų parametrai**.

3. Skirtuke **Kalendorius** keiskite kalendoriaus parametrus, jei reikia.

4. Pasirinkite **Įrašyti**.

## <a name="see-also"></a>Taip pat žiūrėkite

- [Atostogų ir neatvykimų apžvalga](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]