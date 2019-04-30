---
title: Apibrėžti išmokų tinkamumo taisykles ir strategijas
description: Šis įrašas parodys, kaip sukurti išmokų tinkamumo taisykles ir strategijas, ir tada priskirti išmokoms taisykles.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0d35266c95cfbf3473a14fec47a1c748229dd25
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/19/2019
ms.locfileid: "859234"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Apibrėžti išmokų tinkamumo taisykles ir strategijas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šis įrašas parodys, kaip sukurti išmokų tinkamumo taisykles ir strategijas, ir tada priskirti išmokoms taisykles.  

Kuriant šį įrašą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="create-benefit-eligibility-policy-rule-type"></a>Sukurti išmokų tinkamumo strategijos taisyklių tipą
1. Eikite į Žmogiškieji ištekliai > Išmokos > Tinkamumas > Išmokų tinkamumo strategijos taisyklių tipai.
2. Spustelėkite Naujas.
3. Lauke Taisyklės pavadinimas surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Lauke Užklausos pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
7. Spustelėkite Įrašyti.
8. Uždarykite puslapį.

## <a name="benefit-eligibility-policy"></a>Išmokos tinkamumo strategija
1. Eikite į Žmogiškieji ištekliai > Išmokos >Tinkamumas > Išmokų tinkamumo strategijos.
2. Pasirinkite esamą išmokų strategiją.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Perjunkite dalies „Strategijos organizacijos“ išplėtimą.  Čia galite pridėti arba pašalinti organizacijas, kurias norite įtraukti į strategiją.
5. Išplėskite arba sutraukite dalį Strategijos taisyklės.
6. Sąraše raskite anksčiau sukurtą strategijos taisyklę.
7. Spustelėkite Kurti strategijos taisyklę.
8. Lauke „Įsigaliojimo data“ įveskite norimą strategijos įsigaliojimo datą.
    * Įsigaliojimo ir pabaigos datų nustatymas leidžia daryti ateityje įsigaliojančius strategijos taisyklių pakeitimus – jums nebereikės grįžti į strategiją, kad šie pakeitimai įsigaliotų.  
9. 
    * Pvz., jei norite, kad taisyklė būtų taikoma tik pardavimo vadybininkams, galite sukurti „Kai“ sąlygą: kai pareigų aprašas – pardavimo vadybininkas.  Kartu su „Kai“ sąlygomis taisyklėje galite naudoti keletą „Ir“ arba „Ar“.  
10. Spustelėkite GERAI.
11. Uždarykite puslapį.
12. Uždarykite puslapį.

## <a name="assign-rule-to-benefit"></a>Priskirti išmokai taisyklę
1. Pasirinkite Personalas > Išmokos > Išmokos.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Išplėskite arba sutraukite dalį Tinkamumo taisyklės.
5. Spustelėkite Redaguoti.
6. Lauke „Tinkamumas“ pasirinkite „Pagal taisyklę iš sąrašo“.
7. Lauke „Taisyklės tipas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
8. Sąraše raskite ir pasirinkite anksčiau sukurtą taisyklę.
9. Sąraše spustelėkite saitą pasirinktoje eilutėje.
10. Spustelėkite Įrašyti.
11. Uždarykite formą.

