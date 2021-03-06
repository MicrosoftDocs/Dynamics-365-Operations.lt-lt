---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2019 m. kovo 5 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
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
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 115d7cd3d71eaddce2434cb1939c503d36bccdf8
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527295"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-5-2019"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2019 m. kovo 5 d.)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje aprašomos naujos ir pakeistos „Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai

### <a name="extending-option-sets-in-attract"></a>„Attract“ parinkčių rinkinių išplėtimas

„Attract“ yra daug laukų, kurie yra „Common Data Service“ parinkčių rinkiniai. Pristatytos naujos galimybės išplėsti parinkčių rinkinius, pradedant nuo laukų **Atmetimo priežastis**, **Įdarbinimo tipas** ir **Stažo tipas**.

> [!IMPORTANT]
> Norint naudoti darbo registravimo „LinkedIn“ funkciją, reikalingi puslapio **Darbo informacija** laukai **Įdarbinimo tipas** ir **Stažo tipas**. Numatytąsias šių laukų reikšmes palaiko „LinkedIn“ ir jos rodomos, kai darbas registruojamas. Jei registruojate darbus „LinkedIn“ ir modifikuojate esamas tų laukų parinkčių rinkinių reikšmes, darbas bus užregistruotas, bet „LinkedIn“ nerodys pasirinktinių laukų **Įdarbinimo tipas** ir **Stažo tipas** reikšmių.

## <a name="changes-in-onboarding"></a>Supažindinimo pakeitimai

### <a name="private-preview-for-onboard-teams"></a>Supažindinimo komandų privati peržiūra
Dabar galite lengvai bendrinti ir bendrai tvarkyti šablonus visoje savo organizacijoje. Daugiau informacijos žr. [Geriausios praktikos bendrinimas savo organizacijoje naudojant supažindinimo komandas](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).

### <a name="private-preview-for-assignee-placeholders"></a>Priėmėjų rezervavimo ženklų privati peržiūra
Savo šablonus galite išplėsti priskirdami veiklas vaidmenims, o ne asmenims. Tada vaidmenys priskiriami asmenims vadovo kūrimo metu. Daugiau informacijos žr. [Vadovo administravimo supaprastinimas priskiriant veiklas vaidmenims](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai
**8.1.2178 versija**

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a>Sukonfigūruokite darbo eigą, kad automatiškai patvirtintumėte, arba atlikite darbo eigą, kai yra personalo arba eilutės vadovas pateikia ar atnaujina nedarbo laiko užklausas
Įtrauktos naujos darbo eigų sąlygos, kad nedarbo laiko užklausos būtų automatiškai patvirtinamos, jei jas pateikė darbuotojo vadovas arba personalo darbuotojas. Vienas būdas, kaip naudoti šią automatinio patvirtinimo darbo eigoje funkciją, yra įjungti automatinį veiksmą darbo eigos patvirtinime.

Toliau pateiktos įtrauktos sąlygos.

- Pateikė – naudojama siekiant patikrinti vartotojo, kuris pateikė užklausą į darbo eigą, sistemos vartotojo ID.
- Kieno vardu pateikta – naudojama siekiant patikrinti, ar nedarbo laiko užklausa buvo pateikta darbininko, susieto su užklausa, vardu.
- Pateikė personalas – naudojama siekiant patikrinti, ar sistemos vartotojo, kuris pateikė užklausą į darbo eigą, vaidmuo yra Personalo darbuotojas.
- Pateikė vadovas – naudojama siekiant patikrinti, ar vartotojas, kuris pateikė nedarbo laiko užklausą į darbo eigą, yra su užklausa susieto darbininko eilutės hierarchijos vadovas.

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a>Būsimų pareigų priskyrimų darbuotojų pastoviosios atlyginimo dalies įjungimas
Darbuotojai įprastai prisijungia prie organizacijos nustatant pradžios datą ateityje. Šis pakeitimas suteikia galimybę nustatyti darbuotojų, kuriems priskirtos pareigos ateityje, pastoviąją atlyginimo dalį.

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a>Redaguojant pareigas pareigų algalapio laukai yra nenurodyti
Atlikus šį pakeitimą, kai teikiama esamų pareigų pakeitimų užklausa, algalapio laukuose bus nustatomos esamos reikšmės.

### <a name="other-miscellaneous-bug-fixes"></a>Kiti įvairūs klaidų ištaisymai
Kiti smulkūs klaidų ištaisymai yra įtraukti į šį leidimą.

### <a name="upgrade-to-common-data-service"></a>Naujovinimas į „Common Data Service“
Terminas, iki kurio galima naujovinti į „Common Data Service“, sparčiai artėja. Prisijunkite prie „Power Apps“ administravimo centro ir nustatykite, ar reikia naujinti duomenų bazę. Daugiau informacijos apie galutinius terminus ir reikiamus naujovinimo veiksmus žr. [Naujovinimas į „Common Data Service“](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="coming-soon"></a>Jau greitai

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Išplėstinės kompensacijos sauga (fiksuota ir kintama)
Daugelyje organizacijų kompensacijų ir išmokų vadovai gali pasiekti tik tam tikrus kompensacijų įrašus, pvz., vadovams arba tam tikrų regionų darbuotojams skirtus įrašus. Atlikus šį pakeitimą, galite valdyti ir tvarkyti kompensacijų planus, skirtus skirtingoms darbuotojų grupėms jūsų organizacijoje. Fiksuotam ir kintamam planams galima priskirti saugos vaidmenis – tokiu būdu nustatysite prieigą prie planų ir darbuotojų duomenų, susijusių su planais, pvz., pajamų arba premijų įrašai. Tik asmenys, kuriems priskirti reikiami vaidmenys, galės apdoroti tų darbuotojų kompensaciją.

###  <a name="platform-update-24-for-finance-and-operations"></a>„Finance and Operations” platformos 24 naujinimas
Dėl papildomos išsamios informacijos apie „Platform“ naujinimą 24 „Finance and Operations“, žr. [Kas yra nauja ar pakeista „Finance and Operations“ platformos naujinime 24 (2019 m. kovo mėnesį)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).


[!INCLUDE[footer-include](../includes/footer-banner.md)]