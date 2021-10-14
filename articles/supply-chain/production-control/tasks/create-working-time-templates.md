---
title: Darbo laiko šablonų kūrimas
description: Darbo laiko šablonai nustato savaitės darbo valandas ir yra naudojami generuoti darbo laikus tam tikram laikotarpiui.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 130a21d08e4e720f8bf803a5d4b03d315cefc26f
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580677"
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