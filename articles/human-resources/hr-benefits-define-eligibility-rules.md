---
title: Teisės į išmoką taisyklių ir strategijų nustatymas
description: Šiame straipsnyje sužinosite, kaip sukurti išmokų tinkamumo taisykles bei strategijas ir priskirti išmokoms taisykles.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: f46437fef342ab1a4e368063d8b74205ca8e8c05
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430882"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Teisės į išmoką taisyklių ir strategijų nustatymas

Šiame straipsnyje sužinosite, kaip sukurti išmokų tinkamumo taisykles bei strategijas ir priskirti išmokoms taisykles.  

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

