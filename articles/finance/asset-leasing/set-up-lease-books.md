---
title: Nuomos knygų nustatymas
description: Šiame straipsnyje aprašoma informacija, tvarkoma nuomos knygose. Nuomos knygose yra apskaitos strategijos, apibrėžiančios, kaip sistemoje atsiskaitoma už nuomos sutartis.
author: moaamer
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseBookMaster
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ee8cb3c827d590a5eb91121fe4510fbc56c13d9a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903224"
---
# <a name="set-up-lease-books"></a>Nuomos knygų nustatymas

[!include [banner](../includes/banner.md)]

Nuomos knygose yra apskaitos strategijos, apibrėžiančios, kaip sistemoje atsiskaitoma už nuomos sutartis. Be grynųjų pinigų apskaitos, turto nuoma palaiko šiuos standartus.

- Jungtinėse Valstijose bendrai priimami apskaitos principai (US GAAP)
- Apskaitos standartų kodifikavimo tema Nr. 842 (ASC 842)
- ASC 840
- Tarptautinis finansinių ataskaitų standartas Nr. 16 (IFRS 16)
- Tarptautinis apskaitos standartas Nr. 17 (IAS 17)

Norėdami sukurti nuomos knygą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Turto nuoma \> Sąranka \> Nuomos knygos**.
2. Norėdami pridėti knygą, pasirinkite **Nauja**.
3. Užpildykite toliau nurodytus laukus.

    | Pavadinimas / vardas ir (arba) pavardė                                     | aprašymas |
    |------------------------------------------|-------------|
    | Registravimo sluoksnis                            | Pasirinkite naudotiną registravimo sluoksnį. Visos prie nuomos pridėtos knygos nustatytos tam tikram registravimo sluoksniui. Kiekvienas registravimo sluoksnis turi skirtingus registravimo tikslus. |
    | Nuomos tipas                               | Pasirinkite, ar nuomos sutartis turi būti klasifikuojama automatiškai, ar turi būti iš anksto nurodyta kaip finansai ar veiklos nuoma. |
    | Apskaitos sistema                     | Pasirinkite sistemą, kuri susieta su pagrindine knyga. |
    | Nuomos laikotarpio / naudingo naudojimo laiko nustatymas          | Sistema klasifikuos nuomą kaip finansinę, jei nustatytas **automatinis** nuomos tipas ir jei nuomos terminas per visą turto naudingo naudojimo laiką yra didesnis arba lygus šiame lauke apibrėžtai procentinei daliai.  |
    | Dabartinės vertės / turto tikrosios vertės nustatymas   | Įveskite sveikąjį skaičių, nurodantį ribinę vertę, kuri nustatys nuomos tipą. Jei dabartinė minimalių įmokų nuomos mokesčių vertė yra didesnė už vartotojo nustatytą vertę iš knygų nustatymo ir jei knygos nuomos klasifikacija nustatyta kaip automatinė, sistema suklasifikuos nuomos sutartį kaip finansinį nuomos sutartį. |
    | Trumpojo laikotarpio ribinė reikšmė                     | Įveskite dienų skaičių, kuris bus naudojamas kaip trumpalaikės nuomos ribos. Jei nuomos sąlygos vertė yra mažesnė arba lygi čia įvesto mėnesių skaičiui, sistema suklasifikuos nuomą kaip trumpalaikę nuomą ir bus taikomas atidėtas nuomos režimas. |
    | Mažos vertės ribinė reikšmė                      | Įveskite sumą, kuri bus naudojama kaip mažos vertės nuomos riba. Jei turto tikroji vertė yra mažesnė arba lygi čia įvestai vertei, sistema suklasifikuos nuomą kaip mažos vertės turto nuomą ir bus taikomas atidėtas nuomos režimas. |
    | Mokėti tiekėjui                            | Nustatyti šią parinktį į **Taip**, kad būtų leidžiama registruoti nuomos mokėjimus, kaip SF, į tiekėjo sąskaitą, nurodytą kiekvienoje nuomos sutartyje. Užregistravus nuomos apmokėjimą, tiekėjo sąskaita bus kredituota. Jei ši pasirinktis nustatyta į **Ne**, sąskaita, kuri yra nurodyta puslapio **Nuomos registravimo parametrai** registravimo tipe **Nuomos mokestis** bus kredituojama. |
    | Nuomos konvencija                       | Pasirinkite konvenciją nuomos pradžios datai:<ul><li><b>Jokios</b> – Naudokite nuomos pradžios datą kaip pradžios datą.</li><li><b>Visas mėnuo</b> – Naudokite pirmą mėnesio dieną, į kurį nuomos data patenka kaip pradžios data.</li></ul><p>Jei rinksitės <b>Jokios</b>, esama rizikos, kad atsakomybės amortizavimas ir turto nuvertėjimo grafikai bus apskaičiuojami ir publikuos išlaidas mėnesio viduryje, o ne jo gale. Pasirinkę <b>Visą mėnesį</b>, užtikrinsite, kad sistema pradės skaičiuoti nuomą pirmą mėnesio dieną ir visos mėnesio išlaidos bus skaičiuojamos ir publikuojamos paskutinę mėnesio dieną.</p><p><strong>Pastaba:</strong> Funkcija nuomos konvencijoms turi būti įjungta per funkcijų valdymą. Darbo srityje <b>Funkcijų valdymas</b> raskite ir pasirinkite funkciją pavadinimu <b>Lizingo sutartis turto nuomai</b> ir tada rinkitės <b>Įjungti dabar</b>.</p> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
