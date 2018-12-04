--- 
title: "ER: mokėjimų elektroninių dokumentų generavimas naudojant formato konfigūraciją"
description: "Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali naudodamas naują elektroninių ataskaitų (ER) formato konfigūraciją generuoti elektroninius mokėjimų apdorojimo dokumentus."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: cf2ae8fb451eba1054bb94edbce009dcfa8c872c
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a>ER: mokėjimų elektroninių dokumentų generavimas naudojant formato konfigūraciją

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali naudodamas naują elektroninių ataskaitų (ER) formato konfigūraciją generuoti elektroninius mokėjimų apdorojimo dokumentus. Šiuos veiksmus galima atlikti pavyzdinėje įmonėje GBSI.

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti procedūros „Mokėjimo dokumento formato konfigūracijos kūrimas“ veiksmus.


## <a name="change-the-configuration-of-the-electronic-payment-method"></a>Elektroninio mokėjimo būdo konfigūracijos keitimas
1. Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo būdai.
2. Jei reikia, dalį Failo formatas išskleisite ją perjungdami.
3. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką Mokėjimo būdas reikšme „Elektroninis“.
4. Spustelėkite Redaguoti.
5. Lauką Bendrosios elektroninės ataskaitos nustatykite į Taip.
    * Pasirinkite Taip, kad generuoti mokėjimo failams naudotumėte šabloną Bendrosios elektroninės ataskaitos.  
6. Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
7. Pasirinkite BACS (JK fiktyvus) formato konfigūraciją.
8. Spustelėkite Įrašyti.
9. Uždarykite puslapį.

## <a name="test-the-format-of-generated-payment-files"></a>Sugeneruotų mokėjimo failų formato tikrinimas
1. Pasirinkite Mokėtinos sumos > Mokėjimai > Mokėjimų žurnalas.
2. Spustelėkite Naujas.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Pasirinkite „VendPay‟.  
6. Spustelėkite Įrašyti.
7. Spustelėkite Eilutės.
8. Lauke Įmonė įveskite„DEMF‟.
    * DEMF  
9. Lauke „Sąskaita“ nustatykite reikšmes „DE-01001“.
    * DE – 01001  
10. Lauke Aprašas įveskite „Mokėjimas‟.
    * Mokėjimas  
11. Lauke Debetas įveskite skaičių.
    * 1000  
12. Spustelėkite skirtuką Mokėjimas.
13. Lauke Mokėjimo būdas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
14. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite reikšmę Elektroninis.  
15. Sąraše spustelėkite saitą pasirinktoje eilutėje.
16. Spustelėkite Įrašyti.
17. Spustelėkite Generuoti mokėjimus.
18. Lauke Mokėjimo būdas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
19. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite reikšmę Elektroninis.  
20. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Pasirinkite reikšmę Elektroninis.  
21. Lauke „Failo pavadinimas“ suveskite reikšmę.
    * Pavyzdžiui, įveskite „mokėjimai‟.  
22. Lauke Banko sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
23. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Pasirinkite reikšmę GBSI OPER.  
24. Spustelėkite GERAI.
25. Spustelėkite GERAI.
    * Sukurtą mokėjimo failą analizuokite XML formatu. Jį palyginkite su sukurtu dokumento maketu ir apibrėžtais mokėjimo operacijų atributais.  


