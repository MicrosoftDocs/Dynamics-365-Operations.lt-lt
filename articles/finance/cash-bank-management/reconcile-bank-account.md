---
title: Banko sąskaitos derinimas
description: Šiame straipsnyje aprašoma, kaip suderinti banko sąskaitą.
author: angelad116
ms.date: 11/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: angelading
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 12de50f26127c54c2f82ace43487de10e7125aea
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804242"
---
# <a name="reconcile-a-bank-account"></a>Banko sąskaitos derinimas

[!include[banner](../includes/banner.md)]

Gavę banko išrašą, turėtumėte periodiškai suderinti juridinio subjekto banko operacijas su banko išrašo operacijomis.

Negalite suderinti banko išrašo su banko sąskaita, jei nors kurio nors čekio ar mokėjimo kvito mokėjimų, kurie išvardyti išraše **, būsena yra Laukiantis atšaukimas**. Kai redaktorius užregistruoja arba atmeta čekių atšaukimą arba mokėjimo kvitų mokėjimų atšaukimus, būsena nebėra **Laukiama atšaukimo**, ir jūs galite suderinti banko sąskaitą.

1. Eikite į **Grynųjų pinigų ir banko valdymas** \> **Banko sąskaitos** \> **Banko sąskaitos**. Pasirinkite banko sąskaitą, kurią norite suderinti su banko išrašu, ir pasirinkite **Suderinti** > **Sąskaitos suderinimas**.

2. Laukeliuose **Banko išrašo data** ir **Banko išrašas** įveskite informaciją. Lauke **Pabaigos likutis** įveskite banko sąskaitos balansą taip, kaip jis pateikiamas banko sąskaitos išraše.

3. Pasirinkite **Operacijos**, kad atidarytumėte puslapį **Sąskaitos suderinimas**.

4. Kiekvienos į banko išrašą įtrauktos operacijos žymės langelį Valyti pažymėkite, **jei** "Dynamics 365 Finance" suma atitinka banko išraše sumą. Taip pat galite įvesti arba keisti laukelio **Banko operacijos tipas** reikšmę. Tai svarbu jūsų banko operacijų statistikai ir kai kurioms ataskaitoms.
    

>[!NOTE]
>Nepažymėkite operacijų **, kurių nėra** banko išraše, žymės langelio Valyti. Šios operacijos ir toliau bus rodomos šioje formoje, kol nebus suderintos su kitu banko sąskaitos išrašu.
>Jei **operacijos** būsena yra Laukiantis atšaukimas, išvalytas žymės **langelis negalimas**. Operacijos gali turėti tokią būseną, jei „Finance“ nustatytas taip, kad prieš užregistruojant atšaukimus ar anuliavimus, jie būtų peržiūrimi. Kai redaktorius užregistruoja arba atmeta atšaukimą, būsena nebėra **Laukiama atšaukimo**, ir jūs galite suderinti banko sąskaitą su banko išrašu.


Norėdami pasirinkti žymės **langelį Valyti,** kad būtų rodomas visų banko išraše rodomų čekių intervalo žymės langelis Valyti, **pasirinkite Žymėti čekių intervalą**, tada nurodykite intervalą.

5.  Jei banko sąskaitos operacijos suma neatitinka operacijos sumos banko išraše, **koregavimo sumą įveskite lauke Koregavimo** suma.
    

> [!NOTE]
> Jei reikia tik pakoreguoti operacijos ataskaitinį laikotarpį, lauko **Koregavimo** suma naudoti negalima. Vietoj to sukurkite naują eilutę su operacijos data iš atvirojo ataskaitinio laikotarpio. Tokiu atveju turite pridėti atliekant pirminę operaciją naudotas finansines dimensijas ir korespondentinę pagrindinę sąskaitą.



6.  Sukurkite operacijas įrašams (pvz., mokesčiai ir palūkanos), kurie pateikti banko sąskaitos išraše, tačiau dar neužregistruoti „Finance“. Įveskite **Banko operacijos tipą** ir tinkamas finansines dimensijas.

7.  Kai banko sąskaitos išrašo operacijos pažymėtos kaip **Apmokėta**, lauke **Nesuderinta** esanti suma (kuri nuolat perskaičiuojama jums atliekant pakeitimus) artėja prie nulio. Kai ji pasiekia nulį, spustelėkite **Suderinti sąskaitą**, tokiu būdu užregistruosite suderinimą ir savo sukurtas operacijas bei koregavimus.
    
    Užregistrus suderinimą, įtrauktų operacijų negalima nei modifikuoti, nei pakoreguoti, jos nebus rodomos, kad būtų galima suderinti būsimą sąskaitą.

8.  Jei norite peržiūrėti dar nesuderintas banko operacijas, naudokite ataskaitą **Nesuderintos banko operacijos**. Jei norite peržiūrėti banko sąskaitos banko išrašą, naudokite ataskaitą **Banko išrašas**.

## <a name="cancel-bank-statement-reconciliation"></a>Banko išrašo sudarymo atšaukimas 

Banko **išrašo suderinimo atšaukimo** funkcija leidžia atšaukti banko išrašo suderinimą. Jei norite naudoti šią funkciją, aktyvuokite funkciją **Atšaukti banko išrašo suderinimą**, esančią darbo srityje **Funkcijų valdymas**. Taip pat turėsite aktyvuoti parametrą **Leisti redaguoti banko išrašą**. Kad tą atliktumėte, eikite į **Grynųjų pinigų ir banko valdymas > Sąranka > Grynųjų pinigų ir banko valdymo parametrai > Banko suderinimas**.
 
Banko išrašo suderinimus atšaukti galima tik chronologine tvarka pagal jų įvedimo laiką. Atšaukus banko išrašo suderinimą, naujos operacijos ir taisymai bus anuliuoti, o visos kitos operacijos bus pažymėtos kaip nesuderinamos.
 
Norėdami atšaukti banko išrašo suderinimą, pasirinkite banko išrašą ir pasirinkite **Banko išrašas > Atšaukti banko suderinimą**. Puslapyje **Atšaukti banko suderinimą** pateikite **Priežasties kodą**, **Priežasties komentarą** ir **Atšaukimo datą**. Spustelėkite **Gerai**, kad pradėtumėte atšaukimą. Atkreipkite dėmesį, kad banko išrašo atšaukimo data turi sutapti arba būti vėlesnė nei banko išrašo data. Atšaukus banko išrašo suderinimą, **banko** išrašo laukas Atšaukimo data bus atnaujintas naudojant pateiktą **atšaukimo** datą. Spustelėkite mygtuką **Operacijos**, kad peržiūrėtumėte operacijas, kurių suderinimas buvo atšauktas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
