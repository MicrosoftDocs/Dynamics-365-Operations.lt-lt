---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent Core HR“ (2019 m. sausio 11 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 for Talent Core HR“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6a89ba455acbed9724da6826ac4d41c6a481490
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/19/2019
ms.locfileid: "856143"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-11-2019"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent Core HR“ (2019 m. sausio 11 d.)

[!include [banner](includes/banner.md)]

**8.1.2100 versija**

Šioje temoje aprašomos naujos ir pakeistos „Core HR“ funkcijos.

## <a name="changes"></a>Pakeitimai

### <a name="validate-leave-requests-by-forecasting-available-balance"></a>Atostogų užklausų tikrinimas prognozuojant turimą balansą
Šiame leidime atlikti pakeitimai suteikia galimybę darbuotojams teikti ateities atostogų užklausas nesumažinus savo esamo balanso. Ateityje pateikus užklausas bus naudojamos standartinės darbo eigos. Daugiau informacijos žr. [Nedarbo laiko kaupimas pagal pradirbtas valandas](leave-accrue-hours-worked.md).

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a>Prognozuojamo atostogų balanso peržiūra darbo srityse ESS ir Žmonės
Ši funkcija personalo skyriui, vadovams ir darbuotojams leidžia peržiūrėti būsimų atostogų laikotarpių balansus. Darbuotojai ateities balansus gali peržiūrėti darbo srityje **Darbuotojų savitarna**, o personalo skyrius gali pasiekti tą pačią informaciją naudodamas darbo sritį **Žmonės**.

### <a name="notifications-for-changing-leave-balances"></a>Atostogų balansų keitimo pranešimai
Atostogų balansai rodys esamą darbuotojų balansą. Ateities balansai pateikiami darbo srityse **Darbuotojų savitarna** ir **Žmonės** įvedus datą, kad būtų apskaičiuotas prognozuojamas balansas.

Patobulintas naršymas – prognozuojamus balansus galima peržiūrėti toliau nurodytose srityse.
  - Kortelėje **Atostogos**, darbo srityje **Aarbuotojų savitarna**.
  - Kortelėje **Atostogos ir neatvykimas**, darbo srityje **Vadovų savitarna**.
  - Puslapyje **Atostogos ir neatvykimas**, darbo srityje **Žmonės**.

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a>Leisti dešimtaines dalis kintamųjų atlyginimo dalių planuose (grynųjų pinigų planai)
Dabar kintamosios grynųjų pinigų premijoms ir planams priskirta papildoma sumų funkcija, kuri perrašo reikšmes naudodama dešimtainius skaitmenis.

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a>Negalima pakeisti datų kintamosios atlyginimo dalies registracijose įrašius planą
Šis pakeitimas leidžia atnaujinti plano pabaigos datą (pratęstą arba praėjusią) įrašius planą. Vis dar galite aktyvinti arba išjungti planus nepriklausomai nuo pradžios ir pabaigos datų.

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a>Algalapio informacija pasiekiama priskyrus atlyginimų administratoriaus saugos vaidmenį
Algalapio administratoriaus vaidmuo atnaujintas ir dabar jam priskirta prieiga prie algalapio informacijos užklausos kūrimo metu.

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Darbuotojų savitarnos, pareigų hierarchijos išklotinės detalizavimui nepavyksta gauti pirminio mazgo
Atlikti pakeitimai siekiant pašalinti klaidą, kuri kildavo įtraukiant pareigų hierarchiją į naujas darbo sritis ir naršant organizacijos struktūroje.

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a>Naujas tikrinimo pranešimas, kai naudojama personalo numeracija
Atliktas pakeitimas siekiant paaiškinti, kokia problema kyla, kai jūs pasamdote darbuotoją ir naudojamas kitas personalo numeris.

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a>Darbuotojų savitarnos darbo sritis pasirenkama kaip pradinis pradžios puslapis
Kai darbo sritis **Darbuotojų savitarna** pasirenkama kaip vartotojo pradinis pradžios puslapis ir tam vartotojui nėra priskirtas darbuotojo vaidmuo, sistema nukreips į numatytąją ataskaitų sritį.

### <a name="termination-reason-code-updates-position-assignment-record"></a>Atleidimo priežasties kodas atnaujina pareigų priskyrimo įrašą
Atleidimo priežasties kodas dabar atnaujins pareigų priskyrimą, kaidarbuotojas atleidžiamas ir pareigos nutraukiamos. 
