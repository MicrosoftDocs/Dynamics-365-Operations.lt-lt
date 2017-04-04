---
title: "Kaip atšaukti tiekėjo mokėjimą"
description: "Šiame straipsnyje aprašomi mokėjimo atšaukimo, panaikinimo, anuliavimo ir atmetimo skirtumai. Be to, jame paaiškinami du tiekėjo tikrinimo atšaukimo metodai."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankChequeTable, LedgerJournalTransBankChequeReversal, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14361
ms.assetid: 9f0a1883-cbe0-4cc7-b9f3-dd12fb85ebe8
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 716134b2230683050b234297e475d9331fbc7dab
ms.lasthandoff: 03/31/2017


---

# <a name="reverse-a-vendor-payment"></a>Kaip atšaukti tiekėjo mokėjimą

Šiame straipsnyje aprašomi mokėjimo atšaukimo, panaikinimo, anuliavimo ir atmetimo skirtumai. Be to, jame paaiškinami du tiekėjo tikrinimo atšaukimo metodai. 

Kartais užregistravus tiekėjo mokėjimą jis turi būti atšauktas. Atšaukimas skiriasi nuo mokėjimo panaikinimo, anuliavimo ar atmetimo. Naikinti mokėjimą galite tik tada, kai jo būsena yra **Sukurta**. Ši būsena rodo, kad mokėjimas buvo sukurta, bet dar nebuvo buvo sukurtas. Taikomas šis apribojimas visada, nepriklausomai nuo mokėjimo būdo. Neužregistruotos čekius galite atšaukti po to, kai jos sukaupiamos, bet prieš jas užregistruojant. Jei sugeneruoti mokėjimo daroma kaip banko pervedimas (EFT), galite atmesti mokėjimo prieš užregistruojant. Norėdami atmesti mokėjimo, pakeisti į **mokėjimo būsena** vertę. Galima registruoti mokėjimą, kuris buvo anuliuotas arba atmestas po to **mokėjimo būsena** reikšmė bus pakeista į **nė vienas**. 

Užregistravus mokėjimo, naudojami posūkius kita linkme. Mokėjimai, kurie yra pagaminti elektroniniu būdu negali būti atšaukta, po to, kai jie buvo užregistruoti. Vietoj to, naują operaciją reikia sukurti sumos mokėjimo gauti atsakomybės atgal į tiekėjo sąskaitą. Yra du būdai atbulinės eigos paskelbtas patikrinimus. Taikant vieną būdą atšaukimai užregistruojami iškart spustelėjus **Mokėjimo atšaukimas** puslapyje **Čekis**. Kitas būdas: spustelėjus **Mokėjimo atšaukimas** puslapyje **Čekis** atšaukimas pirmiausia nusiunčiamas į grynųjų pinigų ir banko valdymo dalyje esantį čekių atšaukimo žurnalą, kuriame peržiūrintysis gali užregistruoti arba atmesti atšaukimą. 

Norėdami sužinoti, kurį būdą naudoja jūsų organizacija, žr. puslapį **Grynųjų pinigų ir banko valdymo parametrai**. Jei parinktis **Naudoti mokėjimų atšaukimų peržiūros procesą** nustatyta į **Taip**, atšaukimai nusiunčiami į peržiūrėti skirtą čekių atšaukimo žurnalą. Šioje lentelėje apžvelgiami čekių atšaukimo metodų skirtumai.

| Jei jūsų organizacija prieš registruodama neperžiūri čekių atšaukimų                                                                                                                                  | Jei jūsų organizacija prieš registruodama peržiūri čekių atšaukimus                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Čekis atšaukiamas iškart spustelėjus **Gerai** puslapyje **Čekis**.                                                                                                                      | Čekis ne iš karto atšaukiamas. Sukuriamas peržiūrėti skirtas čekio atšaukimo žurnalas. Sunaikinus čekio atšaukimo žurnalą čekis gali būti dar kartą atšaukiamas.                                                                                                                                                                                                                                                                |
| Bus atšaukti pradinio čekio apskaitos įrašai.                                                                                                                                         | DK sąskaita iš pradinio čekio apskaitos įrašo gali būti neužregistruota. Pradinio čekio žurnalo finansinės dimensijos naudojamos kaip numatytosios čekio atšaukimo žurnalo finansinės dimensijos. Šias numatytąsias vertes galite keisti. Kai užregistruojamas čekio atšaukimo žurnalas, pagrindinės Mokėtinų sumų sąskaitos įvedamos automatiškai iš registravimo šablonų, kurie galėjo pasikeisti. |
| Net jei buvo pakeista sąskaitos struktūra, čekiui atšaukti naudojamos tos apskaitos struktūros, kurios buvo naudotos užregistravus pradinį čekį. Sąskaitos derinys netikrinamas. | Jei užregistravus pradinį čekį buvo pakeista sąskaitos struktūra, atšaukiant čekį gali būti būtina nauja finansinė dimensija. Ši finansinė dimensija negali būti įvesta automatiškai iš pradinio mokėjimo žurnalo. Sąskaitos derinys tikrinamas užregistravus čekio atšaukimą.                                                                                                        |
| Atšaukimui netaikomos fiksuotosios dimensijos siekiant užtikrinti, kad atšaukiamos tos pačios DK sąskaitos.                                                                                      | Registruojant fiksuotosios dimensijos taikomos čekio atšaukimo žurnale. Pradinio čekio apskaitos įraše gali nebūti finansinės dimensijos reikšmės – tai priklauso nuo fiksuotosios dimensijos nustatymo laiko.                                                                                                                                                                                                     |

## <a name="reverse-posted-checks-without-reviewing-them"></a>Kaip atšaukti užregistruotus čekius jų neperžiūrėjus
Jei jūsų organizacija nori registruoti čekių atšaukimus iš karto, kai spustelima **Mokėjimo atšaukimas** puslapyje **Čekis**. Puslapyje **Grynųjų pinigų ir banko valdymo parametrai** nustatykite parinktį **Naudoti mokėjimų atšaukimų peržiūros procesą** į **Ne**. Puslapyje **Čekiai** galite pasirinkti norimą atšaukti čekį ir pasirinkite **Mokėjimo atšaukimas**. Tada galite įvesti datą ir pasirinkti atšaukimo datą.

## <a name="reverse-posted-checks-after-they-are-reviewed-in-the-check-reversal-journal"></a>Kaip atšaukti užregistruotus čekius juos peržiūrėjus čekio atšaukimo žurnale
Jei jūsų organizacija nori peržiūrėti čekių atšaukimus prieš juos užregistruojant, sukurkite peržiūrėti skirtą čekio atšaukimo žurnalą puslapyje **Grynųjų pinigų ir banko valdymo parametrai** ir nustatykite parinktį **Naudoti mokėjimų atšaukimų peržiūros procesą** į **Taip**. Puslapyje **Čekiai** galite pasirinkti norimą atšaukti čekį ir pasirinkite **Mokėjimo atšaukimas**. Tada galite įvesti datą ir pasirinkti atšaukimo datą. Norėdami sukurti žurnalą čekio atšaukimo žurnale turite pasirinkti žurnalo pavadinimą.

### <a name="review-a-reversal"></a>Peržiūrėti atšaukimą

Jei esate vartotojas, kuris turi peržiūrėti atšaukimus, galite patvirtinti ir užregistruoti žurnalą arba atmesti atšaukimą panaikindami žurnalą. Puslapyje **Čekio atšaukimų žurnalas** galite pasirinkti norimą peržiūrėti atšaukimo žurnalą, tada spustelėkite **Eilutės**. Galite peržiūrėti atšauktą čekį ir pasirinkti vieną iš šių patvirtinimo parinkčių:

-   Norėdami patvirtinti ir užregistruoti atšaukimo žurnalą, spustelėkite **Užregistruoti** arba **Registruoti ir perkelti**.
-   Norint atmesti atšaukimą reikia panaikinti čekių atšaukimo žurnalą.

> [!NOTE]
> Jei panaikinsite žurnalą, atstatymas yra pašalinamas iš sistemos, bet originalus žymės lieka su **patikrinti** puslapis. Čekio būsena nebebus **Laukia atšaukimo**.

## <a name="results-of-posting-a-reversal"></a>Atšaukimo užregistravimo rezultatai
Užregistravus čekio atšaukimą, įvyksta tai:

-   Čekio būsena atnaujinama į **Atšaukimas**.
-   Jei atšaukimo metu atšaukimo puslapyje buvo pasirinkta parinktis **Suderinti**, čekis suderinamas (pasirenkama parinktis **Suderinta**) ir nerodomas puslapyje **Sąskaitos suderinimas**.
-   Atšaukimo kvitas užregistruojamas pagal banko sąskaitą, iš kurios čekis buvo išduotas, kad būtų padidintas banko sąskaitos balansas.
-   Kvitas užregistruotas į Didžiąją knygą.
-   Pakeitimo informacija atnaujinama laukų grupėje **Retrospektyva**, puslapyje **Čekis**.

> [!NOTE] 
> Kai atšaukiate čekį, kuris buvo išduotas vidinės įmonės prekybos operacijai, korespondavimo įrašai yra iš vidinės įmonės prekybos apskaitos nustatymo, ne iš pradinės operacijos. Jeigu atšauktas čekis buvo išduotas tiekėjo mokėjimui, taip pat atsiranda:

-   Pradinis mokėjimas iš SF, pagal kurią mokėjimas buvo sudengtas, nėra taikomas (sudengimas atšaukiamas).
-   Operacija užregistruojama pagal tiekėjo mokėjimo atšaukimo sąskaitą, atšauktas mokėjimas sudengiamas pagal pradinį mokėjimą. Laukas **Paskutinio sudengimo kvitas** puslapyje **Tiekėjų operacijos**, skirtas pradiniam tiekėjui išmokėti, atnaujinamas, kad būtų atspindimas atšauktos operacijos tiekėjo numeris.

Jeigu atšauktas čekis buvo išduotas klientui grąžinamų pinigų mokėjimui, taip pat atsiranda:

-   Operacija užregistruojama pagal kliento mokėjimo atšaukimo sąskaitą, sudengimas tarp pradinio mokėjimo ir dokumento, pagal kurį mokėjimas iš pradžių buvo sudengtas, atšaukiamas (sukuriamas neigiamas mokėjimas).
-   Mokėjimo atšaukimas taikomas pradiniam mokėjimui. Laukas **Paskutinio sudengimo kvitas** puslapyje **Kliento operacijos**, skirtas pradiniam kliento mokėjimui, atnaujinamas, kad būtų atspindimas atšauktos operacijos tiekėjo numeris.



