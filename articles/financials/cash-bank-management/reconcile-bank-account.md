---
title: Banko sąskaitos suderinimas
description: Šioje temoje aprašoma, kaip suderinti banko sąskaitą.
author: ShivamPandey-msft
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
ms.author: shpandey
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e9a9d1c53a4b9e764c1592cca898cd6f3293594
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863637"
---
# <a name="reconcile-a-bank-account"></a>Banko sąskaitos suderinimas

[!include[banner](../includes/banner.md)]

Gavę banko išrašą, turėtumėte periodiškai suderinti juridinio subjekto banko operacijas su banko išrašo operacijomis.

Negalite suderinti banko sąskaitos išrašo su banko sąskaita, jei nors vieno iš čekių ar mokėjimo kvitų, kurie išvardinti išraše, būsena yra **Pending cancellation**. Kai redaktorius užregistruoja arba atmeta čekių atšaukimą arba mokėjimo kvitų mokėjimų atšaukimus, būsena nebėra **Pending cancellation **, ir jūs galite suderinti banko sąskaitą.

1.  Eikite į „ **Grynųjų pinigų ir banko valdymas“** \> **Banko sąskaitos** \> **Banko sąskaitos**. Pasirinkite banko sąskaitą, kurią norite suderinti su banko išrašu, ir pasirinkite**Reconcile** > **Account reconciliation**.

2.  Laukeliuose **Banko išrašo data** ir **Banko išrašas** įveskite informaciją. Lauke **Ending balance** įveskite banko sąskaitos balansą taip, kaip jis pateikiamas banko sąskaitos išraše.

3.  Pasirinkite **Transactions**, kad atidarytumėte puslapį **Account reconciliation**.

4.  Kiekvienos operacijos, kuri įtraukta į banko sąskaitos išrašą, metu – jei  suma atitinka banko sąskaitos išraše nurodytą sumą Microsoft Dynamics 365 for Finance and Operations – pažymėkite žymės langelį **Cleared **. Taip pat galite įvesti arba keisti laukelio **Banko operacijos tipas** reikšmę. Tai svarbu jūsų banko operacijų statistikai ir kai kurioms ataskaitoms.
    

    > [!NOTE]
    > <P>Tų operacijų, kurių nėra banko sąskaitos išraše, žymės langelis <STRONG>Išvalyta</STRONG> turi likti nepažymėtas. Šios operacijos ir toliau bus rodomos šioje formoje, kol nebus suderintos su kitu banko sąskaitos išrašu.</P>
    > <P>Žymės langelis <STRONG>Cleared</STRONG> neaktyvus, jei operacijos būsena yra <STRONG>Pending cancellation</STRONG>. Operacijos gali turėti tokią būseną, jei „Finance and Operations“ nustatytas taip, kad prieš užregistruojant atšaukimus ar anuliavimus, jie būtų peržiūrimi. Kai redaktorius užregistruoja arba atmeta atšaukimą, būsena nebėra <STRONG>Laukiama atšaukimo</STRONG>, ir jūs galite suderinti banko sąskaitą su banko išrašu.</P>

    
    Norėdami pasirinkti žymės langelį **Ištrinta** visų banko išraše rodomų čekių intervalui, pasirinkite žymės langelį **Pažymėti čekių intervalą** ir nurodykite intervalą.

5.  Jei banko sąskaitos operacijos suma neatitinka banko išraše nurodytos operacijos sumos, lauke **Koregavimo suma** įveskite pakoreguotą sumą.
    

    > [!NOTE]
    > <P>Jei koreguotinos operacijos ataskaitinis laikotarpis yra uždarytas, lauko <STRONG>Koregavimo suma</STRONG> naudoti negalima. Vietoj to sukurkite naują eilutę su operacijos data iš atvirojo ataskaitinio laikotarpio. Tokiu atveju turite pridėti atliekant pirminę operaciją naudotas finansines dimensijas ir korespondentinę pagrindinę sąskaitą.</P>



6.  Sukurkite operacijas įrašams (pvz., mokesčiai ir palūkanos), kurie pateikti banko sąskaitos išraše, tačiau dar neužregistruoti Finance and Operations. Įveskite **Banko operacijos tipą** ir tinkamas finansines dimensijas.

7.  Kai banko sąskaitos išrašo operacijos pažymėtos kaip įtrauktos **Cleared **, lauke **Unreconciled** esanti suma (kuri nuolat perskaičiuojama jums atliekant pakeitimus) artėja prie nulio. Kai ji pasiekia nulį, spustelėkite **Reconcile account**, tokiu būdu užregistruosite suderinimą ir savo sukurtas operacijas bei koregavimus.
    
    Suderinimą užregistravus, įtrauktų operacijų nebegalima nei peržiūrėti, nei taisyti, ir jos daugiau neberodomos kitų sąskaitos suderinimų metu.

8.  Jei norite peržiūrėti dar nesuderintas banko operacijas, naudokite ataskaitą **Unreconciled bank transactions**. Jei norite peržiūrėti banko sąskaitos banko išrašą, naudokite ataskaitą **Bank statement**.

# <a name="cancel-bank-statement-reconciliation"></a>Banko išrašo sudarymo atšaukimas 

Naudodami banko išrašo sudarymo atšaukimo funkciją galėsite atšaukti banko išrašo sudarymą. Jei norite naudoti šią funkciją, aktyvuokite funkciją **Cancel bank statement reconciliation**, esančią darbo srityje **Feature management**. Taip pat turėsite aktyvuoti parametrą **Allow bank statement edit**. Kad tą atliktumėte, eikite į **Grynųjų pinigų ir banko valdymas > Sąranka > Grynųjų pinigų ir banko valdymo parametrai > Banko suderinimas**.
 
Banko išrašo suderinimus atšaukti galima tik chronologine tvarka pagal jų įvedimo laiką. Atšaukus banko išrašo suderinimą, naujos operacijos ir taisymai bus anuliuoti, o visos kitos operacijos bus pažymėtos kaip nesuderinamos.
 
Norėdami atšaukti banko išrašo suderinimą, pasirinkite banko išrašą ir pasirinkite **Banko išrašas > Atšaukti banko suderinimą**. Puslapyje **Atšaukti banko suderinimą** pateikite **Priežasties kodą**, **Priežasties komentarą** ir **Atšaukimo datą**. Spustelėkite **OK**, kad pradėtumėte atšaukimą. Atkreipkite dėmesį, kad banko išrašo atšaukimo data turi sutapti arba būti vėlesnė nei banko išrašo data. Atšaukus banko išrašo suderinimą, banko išrašo laukas **Atšaukimo data** bus atnaujintas pateikta **Atšaukimo data**. Spustelėkite mygtuką **Transactions**, kad peržiūrėtumėte operacijas, kurių suderinimas buvo atšauktas.
