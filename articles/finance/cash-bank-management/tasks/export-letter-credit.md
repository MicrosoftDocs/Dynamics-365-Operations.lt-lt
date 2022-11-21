---
title: Eksportuoti akredityvą
description: Ši procedūra padeda eksportuoti akredityvą.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf06a73bf7665059658c7884a0b9f973929d647c
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779560"
---
# <a name="export-letter-of-credit"></a>Eksportuoti akredityvą

[!include [banner](../../includes/banner.md)]

Ši procedūra padeda eksportuoti akredityvą.

Akredityvas yra banko išduota sutartis, pagal kurią bankas sutinka užtikrinti mokėjimą pirkėjo vardu, jei sutarties tarp pirkėjo ir pardavėjo sąlygos yra patenkinamos.



Vykdykite **banko priemonių ir registravimo šablonų procedūrą** bei **rašto blanką Credit_Create prieš šią procedūrą atlikite** banko priemonės sutarties procedūrą. Reikia pasirinkti demonstracinę įmonę USMF, kad būtų galima sėkmingai atlikti šią procedūrą.


## <a name="create-sales-order-for-export-letter-of-credit"></a>Kurti eksporto akredityvo pardavimo užsakymą
1. Pereikite į Gautinų **sumų >, > visus pardavimo užsakymus**.
2. Spustelėkite **Naujas**.
3. Lauke **Kliento sąskaita** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Išplėskite arba sutraukite **skyrių** Bendra.
7. Lauke **Vieta** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Pasirinkite vietą **,** kurioje sandėliuojamas išduotinas elementas.  
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Lauke **Sandėlis** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Pasirinkite **sandėlį**, kuriame prekė, kuri turi būti išduota, yra sandėlio sandėlis.  
10. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Pastaba: turi būti **pasirinktas akredityvo** laukas Banko **dokumento tipas**.  
11. Lauke Banko **dokumento tipas pasirinkite** akredityvo **·**.
12. Išplėskite arba sutraukite **skyrių** Pristatymas.
    * Pasirinkite **Pristatymo data valdymo Nėra** = **·**.  
13. Į lauką **Pageidaujama** gavimo data įveskite datą.
14. Spustelėkite **Gerai**.
15. Lauke **Prekės numeris** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Pasirinkite prekę, kurią reikia išduoti / parduoti.  
16. Sąraše raskite ir pasirinkite norimą įrašą.
17. Sąraše spustelėkite saitą pasirinktoje eilutėje.
18. Lauke **Vieneto kaina** įveskite skaičių.
19. Išplėskite arba sutraukite dalį **Išsami eilučių informacija**.
20. Spustelėkite skirtuką **Pristatymas**.
21. Pageidaujamos **siuntimo datos** lauke įveskite datą.
22. Į lauką **Patvirtinta** siuntimo data įveskite datą.
23. Veiksmų srityje spustelėkite **Valdyti**.
24. Spustelėkite **akredityvo**.
25. Lauke Banko **dokumento numeris** įveskite vertę.
26. Lauke Galiojimo **data** įveskite datą ir laiką.
27. Išplėskite arba sutraukite **skyrių Banko** informacija.
28. Lauke Išduodantis **bankas** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
29. Sąraše spustelėkite saitą pasirinktoje eilutėje.
30. **Konsultavimo banko lauke** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
31. Sąraše raskite ir pasirinkite norimą įrašą.
32. Sąraše spustelėkite saitą pasirinktoje eilutėje.
33. Spustelėkite **Surasti pardavimo užsakymo siuntas**.
34. Spustelėkite išdavimo **banko dokumentą**.
35. Uždarykite puslapį.

## <a name="post-packing-slip"></a>Registruoti važtaraštį
1. Veiksmų srityje spustelėkite **Paimti ir pakuoti**.
2. Spustelėkite **Registruoti važtaraštį**.
3. Išplėskite arba sutraukite skyrių **Parametrai**.
4. Lauke **Kiekis** pasirinkite **Visi**.
5. Išplėskite arba sutraukite **sąrankos** skyrių.
6. **Važtaraščio datos** lauke įveskite datą.
7. Pasirinkite siuntos numerį.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Spustelėkite **Gerai**.
10. Spustelėkite **Gerai**.

## <a name="post-sales-invoice"></a>Registruoti pardavimo SF
1. Veiksmų srityje spustelėkite **Sąskaita faktūra**.
2. Spustelėkite **Sąskaita faktūra**.
3. Išplėskite arba sutraukite **skyrių** Peržiūra.
4. Pasirinkite siuntos **numerį**.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Išplėskite arba sutraukite **sąrankos** skyrių.
7. Lauke **SF data** įveskite datą.
8. Spustelėkite **Gerai**.
9. Spustelėkite **Gerai**.

## <a name="shipment-document-submitted-status"></a>Pateikto siuntos dokumento būsena
1. Veiksmų srityje spustelėkite **Valdyti**.
2. Spustelėkite **akredityvo**.
3. Išplėskite arba sutraukite **skyrių** Eilutės.
    * Pastaba: laukas **Dokumentas pateiktas** turi būti nustatytas kaip **Taip**.  

## <a name="verify-export-letter-of-credit"></a>Tikrinti eksporto akredityvą
1. Eikite į **mokėjimų grynaisiais pinigais ir > akredityvo > eksporto akredityvo ir importo rinkinį**.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Patikrinkite, ar eksporto **akredityvo** siuntos **būsena yra Išrašyta** **SF**.  

## <a name="customer-payment"></a>Kliento mokėjimas
1. Eikite **į gautinų sumų > ir > žurnalą**.
2. Spustelėkite **Naujas**.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Lauke **Pavadinimas** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Spustelėkite **Eilutės**.
7. Lauke **Data** įveskite datą.
8. Lauke **Sąskaita** nustatykite norimas reikšmes.
9. Spustelėkite **Sudengimas**.
10. Antraštėje Bendrosios sumos pažymėkite žymės langelį.
    * Pastaba: nustatykite lauką **Rodyti** kaip **akredityvo**.  
11. Sąraše raskite ir pasirinkite norimą įrašą.
12. Pažymėkite arba išvalykite žymės **langelį** Žymėti.
13. Spustelėkite **Gerai**.
14. Spustelėkite skirtuką **Mokėjimas**.
    * Patikrinti banko dokumento numerio ir siuntos numerio informaciją  
15. Spustelėkite **Registruoti**.

## <a name="verify-export-letter-of-credit-after-payment"></a>Tikrinti eksporto akredityvą po apmokėjimo
1. Eikite į **mokėjimų grynaisiais pinigais ir > akredityvo > eksporto akredityvo ir importo rinkinį**.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Patikrinkite, ar siuntos būsenos mokėjimas **gautas ir** = **balanso** suma **0,00** = **.**  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
