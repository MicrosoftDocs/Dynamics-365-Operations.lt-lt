---
title: Užduočių sąrašų priskyrimas parduotuvėms arba darbuotojams
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ priskirti užduočių sąrašus parduotuvėms arba darbuotojams.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ee924f5bf95d47814e7ca09b392a3d10b5e9b9dc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006265"
---
# <a name="assign-task-lists-to-stores-or-employees"></a>Užduočių sąrašų priskyrimas parduotuvėms arba darbuotojams

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ priskirti užduočių sąrašus parduotuvėms arba darbuotojams.

## <a name="overview"></a>Peržiūrėti

Užduočių valdymas „Dynamics 365 Commerce” leidžia priskirti užduočių sąrašą kelioms parduotuvėms ar darbuotojams arba parduotuvių ir darbuotojų kombinacijai. Pavyzdžiui, regioninis 20 parduotuvių vadybininkas gali norėti priskirti užduočių sąrašą **Pasiruošimas atostogų sezonui** visoms 20 parduotuvių.

## <a name="start-the-task-list-assignment-process"></a>Užduočių sąrašo priskyrimo proceso pradžia

Norėdami pradėti užduočių sąrašo priskyrimo procesą, atlikite šiuos veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Užduočių valdymas \> Užduočių valdymo administravimas**.
1. Pasirinkite užduočių sąrašą, kurį norite priskirti.
1. Pasirinkite **Pradėti procesą**.
1. Dialogo lange **Pradėti procesą** skirtuko **Bendra** lauke **Proceso pavadinimas** įveskite pavadinimą (pvz., **Rytų regiono parduotuvės**).
1. Lauke **Tikslinės datos** nurodykite datą.
1. Norėdami priskirti užduočių sąrašą parduotuvėms, skirtuke **Parduotuvės** naudokite filtrą **Organizacijos hierarchija**, kad rastumėte ir pasirinktumėte parduotuvių.

    Norėdami priskirti užduočių sąrašą darbuotojams, skirtuke **Darbuotojai** raskite ir pasirinkite darbuotojų.

1. Pasirinkite **Gerai**, kad pradėtumėte procesą. Užduočių sąrašas priskirtas pasirinktoms parduotuvėms arba darbuotojams.

Toliau pateiktame paveikslėlyje parodytas pavyzdys, kaip rasti ir pasirinkti parduotuves dialogo lange **Pradėti procesą**.

![Parduotuvių radimas ir pasirinkimas dialogo lange „Pradėti procesą”](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a>Reguliariai atliekamas užduočių sąrašo priskyrimas

Kartais mažmenininkai turi pasikartojančių užduočių, pvz., „Ketvirtadienio uždarymo kontrolinis sąrašas“ arba „Pirmosios mėnesio dienos kontrolinis sąrašas“. Todėl jie gali norėti reguliariai priskirti užduočių sąrašą.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Užduočių valdymas \> Užduočių valdymo administravimas**.
1. Pasirinkite užduočių sąrašą, kurį norite priskirti.
1. Pasirinkite **Pradėti procesą**.
1. Dialogo lange **Pradėti procesą** skirtuko **Bendra** lauke **Proceso pavadinimas** įveskite pavadinimą.
1. Nustatykite parinkties **Pasikartojimas** vertę **Taip**.
1. Lauke **Pasikartojančios tikslinės datos poslinkis dienomis**, įveskite dienų skaičių. Pavyzdžiui, jei įvesite **4**, tikslinė data bus pasikartojimo data pridėjus keturias dienas.
1. Skirtuke **Vykdyti fone** pasirinkite **Pasikartojimas**.
1. Dialogo lange **Nustatyti pasikartojimą** įveskite dažnumo kriterijus ir pasirinkite **Gerai**.

Toliau pateiktame paveikslėlyje parodytas pavyzdys, kaip įvesti dažnumo kriterijus dialogo lange **Nurodyti pasikartojimą**.

![Dažnumo kriterijų įvedimas dialogo lange „Nustatyti pasikartojimą“](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a>Sekti užduočių sąrašo būseną

Jei esate regioninis vadybininkas arba parduotuvės vadybininkas, galbūt norėsite sekti užduočių sąrašų, priskirtų kelioms parduotuvėms arba darbuotojams, būseną. Tada galite toliau dirbti su parduotuvėmis arba darbuotojais, kurie laiku neatliko jiems priskirtų užduočių. „Commerce“ tarnybinis biuras leidžia peržiūrėti užduočių sąrašų būseną, iš naujo priskirti užduotis arba pakeisti užduoties būseną.

Norėdami sekti visų užduočių sąrašo būseną, atlikite šiuos veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Užduočių valdymas \> Užduočių valdymo procesai**.
1. Pasirinkite skirtuką **Visi užduočių sąrašai**, kad peržiūrėtumėte visų užduočių sąrašų, priskirtų įvairioms parduotuvėms, būseną.

Norėdami sekti visų jums priskirtų užduočių sąrašo būseną, atlikite šiuos veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Užduočių valdymas \> Užduočių valdymo procesai**.
1. Norėdami peržiūrėti arba atnaujinti jums priskirtų užduočių būseną, pasirinkite skirtuką **Mano užduotys** arba **Visos užduotys**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Užduočių valdymo apžvalga](task-mgmt-overview.md)

[Užduočių valdymo konfigūravimas](task-mgmt-configure.md)

[Užduočių sąrašų kūrimas ir užduočių įtraukimas](task-mgmt-create-lists.md)

[Užduočių valdymas EKA programoje](task-mgmt-POS.md)
