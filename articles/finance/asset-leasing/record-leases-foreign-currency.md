---
title: Nuomų įrašymas užsienio valiutomis
description: Šioje temoje paaiškinama, kaip įrašyti nuomą kitomis valiutomis nei apskaitos ar ataskaitų valiuta.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 92177d4f808bfec88dabe9277c3d584ed02e401e
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446187"
---
# <a name="record-leases-in-foreign-currencies"></a>Nuomų įrašymas užsienio valiutomis

[!include [banner](../includes/banner.md)]

Puslapyje **DK sąranka** yra nustatytos nuomos, kuri yra kita nei apskaitos valiuta arba ataskaitų valiuta, turto nuomos sąskaitos. Visas nuomos sutartis turi būti įvesta į savo operacijų valiutą. Kitaip tariant, jie turėtų būti įvedami į nuomos sutartyje nurodytą valiutą. Šioje temoje paaiškinama, kaip įrašyti nuomą kitomis valiutomis nei apskaitos ar ataskaitų valiuta.

Jei įvesite nuomos užsienio valiuta, naudojimo teise valdomas turtas yra nuvertėja ir apskaitos valiuta, ir ataskaitų valiuta. Šios valiutos sukonfigūruotos puslapyje **DK sąranka**. Taip pat naudojama ilgalaikiam turtui. Kai kuriate nuomą užsienio valiuta, lauke **valiuta** pasirinkite operacijos valiutą.

Apskaitos valiutos kursas yra numatytoji vertė lauke **Apskaitos valiutos keitimo kursas**. Ataskaitų valiutos kursas yra numatytoji vertė lauke **Ataskaitų valiutos keitimo kursas**. Šie valiutos kursai buvo veiksmingi nuomos pradžios dieną. Laukai **Apskaitos valiutos kursas** ir **Ataskaitų valiutos kursas** yra puslapio **Nuomos informacija** „FastTab“ **Finansinių ir ataskaitų valiutos keitimo informacija**.

1. Pasirinkite žymės langelį **Fiksuotą tarifas**, kad būtų nepaisoma automatiškai įvesto valiutos kurso, o tada įveskite naują tarifą.
2. Kituose laukuose įveskite reikiamą nuomos informaciją ir pasirinkite **Kurti grafikus**.
3. Puslapyje **Nuomos informacija** pasirinkite **Knygos**.
4. Puslapio **Nuomos knyga** skirtuke **Finansinės ir ataskaitų valiutos keitimo informacija** patikrinkite laukų **Apskaitos valiutos pradinis naudojimo teise valdomas turtas** ir **Ataskaitų valiutos pradinis naudojimo teise valdomas turtas** vertes. Kiekvienas iš šių laukų nurodo, kaip išverstas ROU turto balansas atitinkama valiuta. Šie laukai atnaujinami kaskart, kai pakeičiate finansinę informaciją. Prieš patvirtindami apmokėjimo grafiką pasirinkite **Kurti grafikus**.

    Pradinis pripažinimo žurnalo įrašas įrašo naudojimo teise valdomą turtą, kuris naudoja valiutų kursus, kurie išvardyti nuomos sutartyje. Be to, į žurnalo įrašą įtraukiamos laukų **Apskaitos valiutos pradinis naudojimo teise valdomas turtas** ir **Ataskaitų valiutos pradinis naudojimo teise valdomas turtas** vertės.

## <a name="subsequent-measurement-for-foreign-currency-leases"></a>Vėlesnis užsienio valiutos nuomos matavimas

Nusidėvėjimo grafikas parodo numatomas nusidėvėjimo išlaidų sumas ataskaitų valiuta, apskaitos valiuta ir operacijos valiuta.

Norėdami peržiūrėti naudojimo teise valdomo turto balansus ir nusidėvėjimo sumas ataskaitų valiuta arba apskaitos valiuta, atsidarykite puslapį **Turto nusidėvėjimo grafikas** ir pasirinkite žymės langelį **Rodyti apskaitos valiutos sumas** arba **Rodyti ataskaitų valiutos sumas**.

Kai sukuriate nusidėvėjimo išlaidų žurnalo įrašus su nuoma, išreikšta užsienio valiuta, įrašas naudoja valiutos kursus, kurie išvardyti nuomos sutartyje. Be to, jis naudoja laukų **Apskaitos valiutos pradinis naudojimo teise valdomas turtas** ir **Ataskaitų valiutos pradinis naudojimo teise valdomas turtas** vertes.

Galutinę nusidėvėjimo išlaidų sumą galima apskaičiuoti naudojant šiek tiek kitokį valiutos kursą, kad naudojimo teise valdomas turtas būtų visiškai nusidėvėjęs tiek apskaitos valiuta, tiek ataskaitų valiuta.

Jei nuoma buvo perklasifikuota kaip **Atidėtasis nuomos mokėjimas**, sistema automatiškai panaikina apskaitos ir ataskaitų valiutų kursus, jei jie jau nustatyti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]