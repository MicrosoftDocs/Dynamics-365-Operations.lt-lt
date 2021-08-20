---
title: Darbo laiko šablonų kūrimas
description: Darbo laiko šablonai nustato savaitės darbo valandas ir yra naudojami generuoti darbo laikus tam tikram laikotarpiui.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ef913777c8e2aa14af21e28ed56362e31b3d70a1a52e988a90ad94f59b77b70
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741266"
---
# <a name="create-working-time-templates"></a>Darbo laiko šablonų kūrimas

[!include [banner](../../includes/banner.md)]

Darbo laiko šablonai nustato savaitės darbo valandas ir yra naudojami generuoti darbo laikus tam tikram laikotarpiui. Ši procedūra nurodo, kaip nustatyti darbo laiko šabloną, naudojant darbo laiko planavimo ypatybes, skirtas darbo laiko intervalas skirstyti. Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.

1. Eikite į **Darbo sritys > Išteklių naudojimo ciklo valdymas**.
1. Rinkitės **Darbo laiko šablonai**.

## <a name="create-working-time-template"></a>Kurti darbo laiko šabloną

1. Pasirinkite **Naujas**.
1. Šablono lauke **Darbo laikas** įveskite.
1. Lauke **Pavadinimas** įveskite reikšmę.
1. Išplėskite skyrių **Pirmadienis**.
1. Pasirinkite **Įtraukti**.
1. Lauke **Nuo** įveskite laiką.
    * Nurodykite laiką, kada darbas prasideda ryte.  
1. Lauke **Iki** įveskite laiką.
    * Nurodykite laiką, kada būna darbuotojų pietų pertrauka.  
1. Pasirinkite **Įtraukti**.
1. Lauke **Nuo** įveskite laiką.
    * Nurodykite laiką, kada darbas tęsiamas po pietų.  
1. Lauke **Iki** įveskite laiką.
    * Nurodykite darbo dienos pabaigą.  

## <a name="replicate-working-times-to-all-week-days"></a>Dubliuoti visos savaitės dienų darbo laikus

1. Pasirinkite **Kopijuoti dieną**.
    * Kopijuokite darbo laiko apibrėžimus iš pirmadienio į antradienį.  
1. Pasirinkite **Gerai**.
1. Pasirinkite **Kopijuoti dieną**.
    * Kopijuokite darbo laiko apibrėžimus iš pirmadienio į trečiadienį.  
1. Lauke **Iki savaitės dienos** laukelyje rinkitės parinktį.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Kopijuoti dieną**.
    * Kopijuokite darbo laiko apibrėžimus iš pirmadienio į ketvirtadienį.  
1. Lauke **Iki savaitės dienos** laukelyje rinkitės parinktį.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Kopijuoti dieną**.
    * Kopijuokite darbo laiko apibrėžimus iš pirmadienio į penktadienį.  
1. Lauke **Iki savaitės dienos** laukelyje rinkitės parinktį.
1. Pasirinkite **Gerai**.

## <a name="define-time-slots-for-special-operations"></a>Nurodyti specialiųjų operacijų laiko atkarpas

1. Išplėskite skyrių **Penktadienis**.
1. Sąraše raskite ir pasirinkite norimą įrašą.
1. Lauke **Ypatybė** įveskite arba pasirinkite vertę.
1. Sąraše raskite ir pasirinkite norimą įrašą.
1. Lauke **Ypatybė** įveskite arba pasirinkite vertę.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Pažymėti savaitgalio dienas kaip uždarytas, kada negalima paimti

1. Išplėskite skyrių **Šeštadienis**.
1. Lauke *Taip* Uždaryta paimti pasirinkite **Taip**.
1. Išplėskite skyrių **Sekmadienis**.
1. Lauke *Taip* Uždaryta paimti pasirinkite **Taip**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]