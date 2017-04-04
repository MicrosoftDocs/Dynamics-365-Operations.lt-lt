---
title: Naudokite darbo eigas tvarkoma darbuoto informacija
description: "Šioje temoje paaiškinama, kaip galite naudoti eigos pajėgumas žmogiškųjų išteklių darbuotojo informacijai tvarkyti. Pavyzdžiui, galite susieti darbo eigos padėtį ir konfigūruoti patvirtinimo darbo eigą, kuri yra prasidėjo, kai darbuotojams pakeisti jų įrašą."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: a76ec0cd86bcc810b42ae3cd8efd8a584e6c4da3
ms.openlocfilehash: f286436aa4833babaeb3de875ee393d18e5f8eea
ms.lasthandoff: 03/31/2017


---

# <a name="use-workflows-to-manage-employee-information"></a>Naudokite darbo eigas tvarkoma darbuoto informacija

Šioje temoje paaiškinama, kaip galite naudoti eigos pajėgumas žmogiškųjų išteklių darbuotojo informacijai tvarkyti. Pavyzdžiui, galite susieti darbo eigos padėtį ir konfigūruoti patvirtinimo darbo eigą, kuri yra prasidėjo, kai darbuotojams pakeisti jų įrašą.

Eigos pajėgumas žmogiškųjų išteklių suteikia daug darbo eigų valdyti žmogiškuosius išteklius veiklai. Be to, daugybę variantų yra prieinami, kad jūs keisti konkrečius darbo eigos ir susieti juos su ataskaitų hierarchijoje. Darbo eigos, gali padėti valdyti keletą standartinių tipų darbuotojo informacijos pakeitimus. Darbo eigą, galite susieti su poziciją. Tada, jei darbuotojams pakeisti savo darbuotojo įrašo, yra darbo eiga bus pradėta, turi patvirtinti prieš įrašoma nauja informacija. Darbo eigos yra iš anksto už šių tipų informaciją norėdama padėti jums efektyviai valdyti pokyčius ir išlaikyti savo darbuotojų duomenis tiksliai:

-   Identifikavimo numeriai
-   Kursai
-   Išsilavinimas
-   Vaizdas
-   Panaudos prekės
-   Profesinė patirtis
-   Darbo projektuose patirtis
-   Įgūdžiai
-   Atsakingos pareigos
-   Žmogiškųjų išteklių veiksmų
-   Modulio registracija

Kai darbuotojai samdomi, perduodant arba nutraukta, darbo eigos gali būti peržiūros procesą. Tokiu būdu galima peržiūrėti dokumentą arba ieškinį terminai gali būti apibrėžiamas kaip dalis, darbo eiga. Atlikus peržiūrą, dokumentą ar veiksmas bus baigtas, ir darbo eiga pereina prie galutinio patvirtinimo žingsnis.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Susieti darbo eigos padėtį hierarchijoje
Darbo eigą, galite susieti su bet hierarchijos, kuriuos galite konfigūruoti. Pavyzdžiui, jei pozicija yra susijusi su matricos ataskaitų hierarchijoje, galite konfigūruoti darbo eigą, kuri nukreipia konkretaus projekto išlaidas, projekto švino vietoj valdytojo darbuotojas, kuris yra susijęs su šios pozicijos. Norėdami sukurti naują darbo eigą arba keisti esamas darbo eigą, į **žmogiškųjų išteklių darbo eigos** spustelėkite **naujas**. Pasirinkite darbo eigos paleisti darbo eigos dizaino įrankis sąraše. Galite naudoti dizainerio sukurti naują darbo eigą arba keisti esamas darbo eigos veiksmus. Kai keičiate esamą darbo eigos, jūsų keitimai įrašomi kaip naują versiją. Todėl, jūs galite visada grįžti prie ankstesnės versijos jei turite.

## <a name="configure-a-human-resources-workflow"></a>Konfigūruoti darbo eigos žmogiškųjų išteklių
Konfigūruoti pagrindinius darbo eigą, kuri yra prasidėjo, kai darbuotojai reikalauti keisti jų asmens tapatybės, atlikite šiuos veiksmus.

1.  Dėl į **žmogiškųjų išteklių darbo eigų** spustelėkite **naujas**.
2.  Pasirinkite iš sąrašo galimos darbo eigos, **identifikacijos numerius**.
3.  Spustelėkite **paleisti** paleisti darbo eigos dizaino įrankis, ir tada įveskite savo vartotojo vardą ir slaptažodį, kai būsite paraginti.
4.  Vilkite į **patvirtinti identifikavimo numerį** elemento darbo eigos elementų sąraše dizaineris drobė.
5.  Prijunkite patvirtinimo elemento **pradėti** ir **apdailos**.
6.  Dukart spustelėkite **tvirtinti elementas**, ir tada dešiniuoju pelės mygtuku spustelėkite ir pasirinkite **ypatybės**.
7.  Atlikite šiuos veiksmus ir pridėkite darbo elementą instrukcijas:
    1.  Pasirinkite **priskyrimas**, ir tada pasirinkite **hierarchijos** pagal užduoties tipas.
    2.  Pagal į **hierarchijos** pasirinkimas, pasirinkite **konfigūruojama hierarchijos**.
    3.  Pridėkite stabdymo sąlyga ir uždaryti puslapį.

8.  Užbaigti papildomomis instrukcijomis (jokių papildomų įspėjimų turėtų būti).
9.  Spustelėkite **Įrašyti ir uždaryti**. Aktyvinti naują darbo eigą, kai dialogo lange atsidarys, ir pasirinkite **aktyvus**.
10. Eikite į **žmogiškųjų išteklių**&gt;**pozicijos**&gt;**pozicija hierarchijoje tipų**.
11. Pasirinkite **matricos**.
12. Pridėti į **darbuotojo identifikavimo numerį** darbo eigą į sąrašą.



