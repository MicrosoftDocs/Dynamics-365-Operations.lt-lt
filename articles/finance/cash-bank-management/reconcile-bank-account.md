---
title: Banko sąskaitos suderinimas
description: Šioje temoje aprašoma, kaip suderinti banko sąskaitą.
author: panolte
manager: AnnBe
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: panolte
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c77d08d5877ab27f9b6549a5b2a666150938fc08
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446066"
---
# <a name="reconcile-a-bank-account"></a>Banko sąskaitos suderinimas

[!include[banner](../includes/banner.md)]

Gavę banko išrašą, turėtumėte periodiškai suderinti juridinio subjekto banko operacijas su banko išrašo operacijomis.

Negalite suderinti banko sąskaitos išrašo su banko sąskaita, jei nors vieno iš čekių ar mokėjimo kvitų, kurie išvardinti išraše, būsena yra **Laukiama atšaukimo**. Kai redaktorius užregistruoja arba atmeta čekių atšaukimą arba mokėjimo kvitų mokėjimų atšaukimus, būsena nebėra **Laukiama atšaukimo**, ir jūs galite suderinti banko sąskaitą.

1.  Eikite į  **Grynųjų pinigų ir banko valdymas** \> **Banko sąskaitos** \> **Banko sąskaitos**. Pasirinkite banko sąskaitą, kurią norite suderinti su banko išrašu, ir pasirinkite **Suderinti** > **Sąskaitos suderinimas**.

2.  Laukeliuose **Banko išrašo data** ir **Banko išrašas** įveskite informaciją. Lauke **Pabaigos likutis** įveskite banko sąskaitos balansą taip, kaip jis pateikiamas banko sąskaitos išraše.

3.  Pasirinkite **Operacijos**, kad atidarytumėte puslapį **Sąskaitos suderinimas**.

4.  Kiekvienos operacijos, kuri įtraukta į banko sąskaitos išrašą, metu – jei  suma atitinka banko sąskaitos išraše nurodytą sumą Dynamics 365 Finance – pažymėkite žymės langelį **Išvalyta**. Taip pat galite įvesti arba keisti laukelio **Banko operacijos tipas** reikšmę. Tai svarbu jūsų banko operacijų statistikai ir kai kurioms ataskaitoms.
    

    > [!NOTE]
    > <P>Tų operacijų, kurių nėra banko sąskaitos išraše, žymės langelis <STRONG>Išvalyta</STRONG> turi likti nepažymėtas. Šios operacijos ir toliau bus rodomos šioje formoje, kol nebus suderintos su kitu banko sąskaitos išrašu.</P>
    > <P>Žymės langelis <STRONG>Išvalyta</STRONG> neaktyvus, jei operacijos būsena yra <STRONG>Laukiama atšaukimo</STRONG>. Operacijos gali turėti tokią būseną, jei „Finance“ nustatytas taip, kad prieš užregistruojant atšaukimus ar anuliavimus, jie būtų peržiūrimi. Kai redaktorius užregistruoja arba atmeta atšaukimą, būsena nebėra <STRONG>Laukiama atšaukimo</STRONG>, ir jūs galite suderinti banko sąskaitą su banko išrašu.</P>

    
    Norėdami pasirinkti žymės langelį **Ištrinta** visų banko išraše rodomų čekių intervalui, pasirinkite žymės langelį **Pažymėti čekių intervalą** ir nurodykite intervalą.

5.  Jei banko sąskaitos operacijos suma neatitinka banko išraše nurodytos operacijos sumos, lauke **Koregavimo suma** įveskite pakoreguotą sumą.
    

    > [!NOTE]
    > <P>Jei koreguotinos operacijos ataskaitinis laikotarpis yra uždarytas, lauko <STRONG>Koregavimo suma</STRONG> naudoti negalima. Vietoj to sukurkite naują eilutę su operacijos data iš atvirojo ataskaitinio laikotarpio. Tokiu atveju turite pridėti atliekant pirminę operaciją naudotas finansines dimensijas ir korespondentinę pagrindinę sąskaitą.</P>



6.  Sukurkite operacijas įrašams (pvz., mokesčiai ir palūkanos), kurie pateikti banko sąskaitos išraše, tačiau dar neužregistruoti „Finance“. Įveskite **Banko operacijos tipą** ir tinkamas finansines dimensijas.

7.  Kai banko sąskaitos išrašo operacijos pažymėtos kaip **Apmokėta**, lauke **Nesuderinta** esanti suma (kuri nuolat perskaičiuojama jums atliekant pakeitimus) artėja prie nulio. Kai ji pasiekia nulį, spustelėkite **Suderinti sąskaitą**, tokiu būdu užregistruosite suderinimą ir savo sukurtas operacijas bei koregavimus.
    
    Suderinimą užregistravus, įtrauktų operacijų nebegalima nei peržiūrėti, nei taisyti, ir jos daugiau neberodomos kitų sąskaitos suderinimų metu.

8.  Jei norite peržiūrėti dar nesuderintas banko operacijas, naudokite ataskaitą **Nesuderintos banko operacijos**. Jei norite peržiūrėti banko sąskaitos banko išrašą, naudokite ataskaitą **Banko išrašas**.

## <a name="cancel-bank-statement-reconciliation"></a>Banko išrašo sudarymo atšaukimas 

Naudodami banko išrašo sudarymo atšaukimo funkciją galėsite atšaukti banko išrašo sudarymą. Jei norite naudoti šią funkciją, aktyvuokite funkciją **Atšaukti banko išrašo suderinimą**, esančią darbo srityje **Funkcijų valdymas**. Taip pat turėsite aktyvuoti parametrą **Leisti redaguoti banko išrašą**. Kad tą atliktumėte, eikite į **Grynųjų pinigų ir banko valdymas > Sąranka > Grynųjų pinigų ir banko valdymo parametrai > Banko suderinimas**.
 
Banko išrašo suderinimus atšaukti galima tik chronologine tvarka pagal jų įvedimo laiką. Atšaukus banko išrašo suderinimą, naujos operacijos ir taisymai bus anuliuoti, o visos kitos operacijos bus pažymėtos kaip nesuderinamos.
 
Norėdami atšaukti banko išrašo suderinimą, pasirinkite banko išrašą ir pasirinkite **Banko išrašas > Atšaukti banko suderinimą**. Puslapyje **Atšaukti banko suderinimą** pateikite **Priežasties kodą**, **Priežasties komentarą** ir **Atšaukimo datą**. Spustelėkite **Gerai**, kad pradėtumėte atšaukimą. Atkreipkite dėmesį, kad banko išrašo atšaukimo data turi sutapti arba būti vėlesnė nei banko išrašo data. Atšaukus banko išrašo suderinimą, banko išrašo laukas **Atšaukimo data** bus atnaujintas pateikta **Atšaukimo data**. Spustelėkite mygtuką **Operacijos**, kad peržiūrėtumėte operacijas, kurių suderinimas buvo atšauktas.
