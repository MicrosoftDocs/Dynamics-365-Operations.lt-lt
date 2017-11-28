---
title: "DUK apie adresų knygeles"
description: "Šioje temoje pateikiami atsakymai į dažnai užduodamus klausimus, susijusius su „Microsoft Dynamics 365 for Finance and Operations“ „Enterprise“ leidimo adresų knygelėmis."
author: kfend
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartyCheckDuplicate, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23601
ms.assetid: b177fa0f-ac9a-415e-9498-15438e132f60
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2af6c89879300d8d1a510fd7d65b11f281997cd3
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="address-books-faq"></a>DUK apie adresų knygeles

[!include[banner](../includes/banner.md)]




<a name="how-do-i-check-for-duplicate-records"></a>Kaip patikrinti, ar nėra besidubliuojančių įrašų?
-------------------------------------

Tikrinti, ar nėra besidubliuojančių įrašų, galite tiesiai iš **Visuotinės adresų knygelės** sąrašo puslapio. Veiksmų srityje, skirtuke **Šalis**, grupėje **Prižiūrėti** spustelėkite **Tikrinti, ar nėra dublikatų**. Tada pasirinkite reikšmes, kurias norite įtraukti tikrindami, ar nėra dublikatų.

## <a name="can-i-bulk-add-or-delete-party-records-from-an-address-book"></a>Ar galima adresų knygelėje įrašus pridėti ar naikinti masiškai?
Taip, į adresų knygelę galite pridėti kelis šalių įrašus ir taip pat pašalinti kelis įrašus.

-   Norėdami į adresų knygelę pridėti kelis šalių įrašus, **Visuotinės adresų knygelės** sąrašo puslapyje sąraše pasirinkite šalis. Tada veiksmų srityje, skirtuke **Šalis**, grupėje **Prižiūrėti** spustelėkite **Priskirti šalis**. Pasirinkite adresų knygeles, į kurias turi būti pridėti šalių įrašai, ir spustelėkite **Gerai**. Visi pasirinkti šalių įrašai pridedami į jūsų pasirinktas adresų knygeles.
-   Norėdami iš adresų knygelę pašalinti kelis šalių įrašus, **Visuotinės adresų knygelės** sąrašo puslapyje sąraše pasirinkite šalis. Tada veiksmų srityje, skirtuke **Šalis**, grupėje **Prižiūrėti** spustelėkite **Šalinti šalis**. Pasirinkite adresų knygeles, iš kurių reikia pašalinti šalis, ir spustelėkite **Gerai**. Visi pasirinkti šalių įrašai pašalinami iš jūsų pasirinktų adresų knygelių.

## <a name="can-i-change-the-party-type-of-a-record-or-do-i-have-to-delete-the-old-record-and-create-a-new-one"></a>Ar galiu keisti įrašo šalies tipą, ar reikia panaikinti senąjį įrašą ir sukurti naują?
Kartais gali tekti pakeisti įrašo šalies tipą iš asmens į organizacijos arba iš organizacijos į asmens. Pavyzdžiui, Nancy yra „Fabrikam U.K.‟ pardavimo komandos narė. Prekybos parodoje Londone ji sutinka šešis naujus potencialius klientus. Nancy kiekvienam potencialiam klientui sukuria potencialaus kliento šalies įrašą. Nancy įrašant įrašus, kiekvienas įrašas taip pat sukuriamas visuotinėje adresų knygelėje. „Fabrikam‟ numatytąjį šalies tipą nustatė į organizacijos, tačiau dviejų naujų potencialių klientų įrašo tipas turėtų būti asmens. Todėl, kai Nancy grįžta iš prekybos parodos, ji turi pakeisti šių dviejų potencialių klientų šalies tipą. Norėdami šalies įrašą pakeisti iš vieno šalies tipo į kitą, pirmiausia visuotinėje adresų knygelėje turite sukurti naują tinkamo tipo šalies įrašą. Tada senąjį šalies įrašą susiejate su šiuo nauju įrašu. Susieję naująją šalį, panaikinkite pradinį šalies įrašą, kurio įrašo tipas netinkamas.

## <a name="how-do-i-change-the-name-or-address-of-a-party-record"></a>Kaip pakeisti šalies įrašo pavadinimą ar adresą?
Atnaujinti šalies įrašo pavadinimą ir adresus, susietus su tuo įrašu, galite bet kuriuo metu.

-   Norėdami atnaujinti šalies įrašo pavadinimą, atidarykite tą šalies įrašą ir veiksmų srityje spustelėkite **Redaguoti**. „FastTab‟ **Bendra** įveskite naująjį šalies pavadinimą ir įrašykite įrašą.
-   Norėdami atnaujinti šalies įrašo adresą, atidarykite tą šalies įrašą, tada „FastTab‟ **Adresai** pasirinkite norimą atnaujinti adresą. Spustelėkite **Redaguoti**, tada puslapyje **Redaguoti adresą** atlikite reikiamus adreso ar adreso parametrų keitimus.

## <a name="can-i-merge-two-or-more-party-records-into-one-record"></a>Ar galima du arba kelis šalių įrašus sulieti į vieną įrašą?
Kartais galbūt norėsite du arba kelis šalių įrašus sulieti į vieną įrašą. Taip gali nutikti, jei sąmoningai ar netyčia sukuriate vieną ar kelis besidubliuojančius šalių įrašus. Suliedami šalių įrašus, vieną įrašą pasirenkate išsaugoti. Į šį įrašą tada suliejama informacija iš kitų įrašų. Pavyzdžiui, pastebite, kad informacija apie „Fabrikam‟ saugoma trijuose šalių įrašuose: A, B ir C. Nusprendžiate palikti šalies įrašą A. Todėl informacija, saugoma šalių įrašuose B ir C, bus sulieta į šalies įrašą A. Toliau nurodytos kelios situacijos, kai sulieti šalių įrašų negalima.

-   Negalima sulieti šalių įrašų, tame pačiame juridiniame subjekte susietų su tuo pačiu šalies vaidmeniu, pvz., kliento ar tiekėjo. Pavyzdžiui, šalis B susieta su tiekėju 123 juridiniame subjekte, o šalis B 123 juridiniame subjekte susieta su kitu klientu. Šių šalių įrašų negalima sulieti, nes juos suliejus sulietas šalies įrašas būtų susietas su keliais to paties juridinio subjekto klientais, o tai neleidžiama. Tačiau įrašai gali būti sulieti, jei šalis B susieta su tiekėju 123 juridiniame subjekte arba su klientu kitame juridiniame subjekte.
-   Negalima sulieti vidinių šalies organizacijos įrašų tame pačiame juridiniame subjekte, komandoje ar valdymo vienete.

## <a name="should-i-create-a-party-record-in-the-global-address-book-or-in-another-place-such-as-the-customer-or-vendor-page"></a>Ar šalies įrašą turėčiau sukurti visuotinėje adresų knygelėje, ar kitoje vietoje, pvz., Kliento ar Tiekėjo puslapyje?
Šalių įrašus galite įvesti arba visuotinėje adresų knygelėje, arba atitinkamame objekto puslapyje. Kai įrašą pridedate vienoje vietoje, tas pats įrašas visada pridedamas kitoje vietoje. Pvz., jei kliento šalies įrašą pridedate visuotinėje adresų knygelėje, tas įrašas taip pat pridedamas **Kliento** puslapyje. Panašiai, jei kliento šalies įrašą pridedate **Kliento** puslapyje, tas įrašas taip pat pridedamas visuotinėje adresų knygelėje. Spręsdami, kur reikėtų įvesti naujus šalių įrašus, vadovaukitės toliau pateiktomis gairėmis.

-   **Šalies įrašo kūrimas nežinant objekto tipo** – jei turite sukurti įrašą, bet nežinote jo objekto tipo (pvz., nežinote, ar objektas yra klientas, ar galimybė), įrašą sukurkite visuotinėje adresų knygelėje. Pasirinkti objekto tipą galite vėliau.
-   **Šalies įrašo kūrimas žinant objekto tipą** – jei žinote šalies objekto tipą, įrašą galite kurti atitinkamame to tipo puslapyje. Pvz., kliento įrašą sukurkite **Kliento** puslapyje. Kai įrašą sukuriate ir įrašote naudodami atitinkamą objekto puslapį, tas įrašas automatiškai sukuriamas visuotinėje adresų knygelėje.

## <a name="can-i-translate-address-information-for-party-records"></a>Ar galima išversti šalių įrašų adreso informaciją?
Galite nustatyti adreso informacijos vertimus, kad sprendime „Microsoft Dynamics 365 for Finance and Operations‟ informacija būtų rodoma jūsų vartotojo kalba (sistemos kalba), tačiau dokumentuose, pvz., pardavimo užsakymuose, – kita kalba. Galite įvesti šalių / regionų pavadinimų, adresų ir vardų sekų vertimus. Pavyzdžiui, jūsų sistemos kalba yra danų, ir pardavimo užsakymą sukuriate klientui Prancūzijoje. Šiuo atveju programoje kliento įrašą galite peržiūrėti danų kalba, tačiau išspausdintame pardavimo užsakyme adreso informaciją rodyti prancūzų kalba. Nustatydami vertimus, turėtumėte įvesti kiekvienos sąrašo prekės vertimą. Visos prekės, kurioms neįvesite vertimo, bus rodomos sistemos kalba. Pavyzdžiui, jūsų sistemos kalba yra danų, ir dokumentą siunčiate klientui Ispanijoje. Jei neįvedėte adreso informacijos vertimų į ispanų (ESP) kalbą, ta informacija danų kalba bus rodoma ir programoje, ir išspausdintame dokumente.




