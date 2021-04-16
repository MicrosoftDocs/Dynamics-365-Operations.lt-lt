---
title: Užduočių sąrašų kūrimas ir užduočių įtraukimas
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ kurti užduočių sąrašus ir įtraukti į juos užduotis.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: a0e49d1eced3bb62e78c630b137a5b86121682f3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795242"
---
# <a name="create-task-lists-and-add-tasks"></a>Užduočių sąrašų kūrimas ir užduočių įtraukimas

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ kurti užduočių sąrašus ir įtraukti į juos užduotis.

*Užduotis* apibrėžia konkretų darbą arba veiksmą, kurį reikia atlikti iki nurodyto termino. Programoje „Dynamics 365 Commerce” į užduotį galima įtraukti išsamių instrukcijų ir informacijos apie kontaktinį asmenį. Į ją taip pat galima įtraukti tarnybinio biuro operacijų, elektroninio kasos aparato (EKA) operacijų arba svetainių puslapių saitų, siekiant patobulinti našumą ir suteikti kontekstą, reikalingą užduoties savininkui efektyviai atlikti užduotį.

*Užduočių sąrašas* yra užduočių, kurios turi būti atliktos vykdant verslo procesą, rinkinys. Pavyzdžiui, gali būti užduočių sąrašas, skirtas naujam darbuotojui įvykdyti supažindinimo metu, užduočių sąrašas, skirtas kasininkams, dirbantiems vakarinėmis pamainomis, arba užduočių sąrašas, kurį reikia įvykdyti, siekiant paruošti parduotuvę būsimam švenčių laikotarpiui. „Commerce“ kiekvienas užduočių sąrašas, kuriame yra tikslinė data, gali būti priskirtas neribotam parduotuvių ar darbuotojų skaičiui, be to, jį galima konfigūruoti, kad pasikartotų.

Ir vadybininkai, ir darbuotojai gali kurti užduočių sąrašus „Commerce“ tarnybiniame biure ir priskirti juos parduotuvių grupei.

## <a name="create-a-task-list"></a>Užduočių sąrašo kūrimas

Norėdami sukurti užduočių sąrašą, atlikite tolesnius veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Užduočių valdymas \> Užduočių valdymo administravimas**.
1. Pasirinkite **Naujas**, tada laukuose **Pavadinimas**, **Aprašas** ir **Savininkas** įveskite vertes.
1. Pasirinkite **Įrašyti**.

## <a name="add-tasks-to-a-task-list"></a>Užduočių įtraukimas į užduočių sąrašą

Norėdami įtraukti užduočių į užduočių sąrašą, atlikite tolesnius veiksmus.
 
1. Esamo užduočių sąrašo „FastTab“ skirtuke **Užduotys** pasirinkite **Nauja**.
1. Dialogo lango **Kurti naują užduotį** lauke **Pavadinimas** įveskite užduoties pavadinimą.
1. Lauke **Termino poslinkis nuo tikslinės datos** įveskite teigiamą arba neigiamą sveikąją vertę. Pavyzdžiui, įveskite **-2**, jei užduotis turi būti užbaigta likus dviem dienoms iki užduočių sąrašo termino datos.
1. Lauke **Pastabos** įveskite išsamias instrukcijas.
1. Lauke **Kontaktinis asmuo** įveskite srities eksperto, į kurį užduoties savininkas, prireikus, gali kreiptis pagalbos, vardą ir pavardę.
1. Lauke **Užduoties saitas** įveskite saitą, pagrįstą užduoties pobūdžiu.

> [!TIP]
> Nors kurdami užduočių sąrašą galite naudoti lauką **Priskirta**, kad kam nors priskirtumėte užduočių, rekomenduojame vengti priskirti užduotis, kai kuriamas užduočių sąrašas. Vietoj to priskirkite užduotis, sukūrę atskiroms parduotuvėms skirtų sąrašo egzempliorių.

## <a name="use-task-links-to-help-improve-worker-productivity"></a>Užduočių saitų naudojimas, siekiant tobulinti darbuotojų efektyvumą

„Commerce“ leidžiama susieti užduotis su konkrečiomis EKA operacijomis, pvz., su pardavimo ataskaitos vykdymu, mokomojo vaizdo įrašo, skirto naujiems darbuotojams orientuoti, peržiūra arba tarnybinio biuro operacijos atlikimu. Ši funkcija padeda užduočių savininkams gauti informacijos, kurios reikia norint efektyviai atlikti užduotį.

Norėdami įtraukti užduočių saitų kurdami užduotį, atlikite tolesnius veiksmus.

1. Esamo užduočių sąrašo „FastTab“ skirtuke **Užduotys** pasirinkite **Redaguoti**.
1. Dialogo lango **Redaguoti užduotį** lauke **Užduoties saitas** pasirinkite vieną ar daugiau toliau pateikiamų parinkčių.

    - Pasirinkite **Meniu elementas**, kad konfigūruotumėte tarnybinio biuro operaciją, pvz., „Produkto rinkiniai“.
    - Pasirinkite **EKA operacija**, kad konfigūruotumėte EKA operaciją, pvz., „Pardavimo ataskaitos”.
    - Pasirinkite **URL**, kad konfigūruotumėte absoliučią URL.

Toliau pateiktame paveikslėlyje parodytas užduočių saitų žymėjimas dialogo lange **Redaguoti užduotį**.

![Užduočių saitų žymėjimas dialogo lange „Redaguoti užduotį“](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a>EKA operacijos konfigūravimas, kad ją būtų galima susieti su užduotimi

Norėdami konfigūruoti EKA operaciją, kad ją būtų galima susieti su užduotimi, atlikite tolesnius veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA \> EKA operacijos**.
1. Pasirinkite **Redaguoti**, raskite EKA operaciją, tada pažymėkite jos žymės langelį **Įgalinti užduočių valdymą**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Užduočių valdymo apžvalga](task-mgmt-overview.md)

[Užduočių valdymo konfigūravimas](task-mgmt-configure.md)

[Užduočių sąrašų priskyrimas parduotuvėms arba darbuotojams](task-mgmt-assign-lists.md)

[Užduočių valdymas EKA programoje](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
