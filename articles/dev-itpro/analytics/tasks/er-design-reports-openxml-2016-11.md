--- 
title: "ER konfigūracijų kūrimas siekiant generuoti ataskaitas „OpenXML“ formatu"
description: "Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti naują elektroninių ataskaitų (ER) konfigūraciją, apimančią elektroninių dokumentų generavimo OPENXML formatu šabloną."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: b42cfe36c57a9526e585bbad0fcd31ff60b90397
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---
# <a name="design-er-configurations-to-generate-reports-in-openxml-format"></a>ER konfigūracijų kūrimas siekiant generuoti ataskaitas „OpenXML“ formatu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti naują elektroninių ataskaitų (ER) konfigūraciją, apimančią elektroninių dokumentų generavimo OPENXML formatu šabloną. Ši konfigūracija bus naudojama apdoroti tiekėjų mokėjimams.



Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją. Šiuos veiksmus galima atlikti GBSI įmonėje.



Norėdami atlikti šiuos veiksmus, pirmiausia turite juos užbaigti procedūroje „Sukurti konfigūracijos teikėją ir pažymėti jį kaip aktyvų“. Taip pat turite atsisiųsti ir įrašyti „Microsoft Excel“ failą [Mokėjimo ataskaitos šablonas](https://go.microsoft.com/fwlink/?linkid=862266). 

## <a name="upload-the-payments-data-model-configuration"></a>Mokėjimų duomenų modelio konfigūracijos nusiuntimas
1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
2. Sąraše pažymėkite pasirinktą eilutę.
    * Pasirinkite pavyzdinės įmonės „Litware, Inc“ konfigūracijos teikėją. Jei nematote šio konfigūracijos teikėjo, pirmiausia turite užbaigti procedūros „Sukurti konfigūracijos teikėją ir pažymėti jį kaip aktyvų" veiksmus.  
3. Spustelėkite Nustatyti kaip aktyvų.
4. Spustelėkite Saugyklos.
    * Jei yra, pasirinkite tipo Operacijų ištekliai saugyklą. Jei tokia yra, praleiskite tolesnius naujos saugyklos kūrimo veiksmus.  
5. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
6. Lauke Konfigūracijų saugyklos tipas įveskite Operacijų ištekliai.
7. Spustelėkite Kurti saugyklą.
8. Spustelėkite GERAI.
9. Spustelėkite Atidaryti.
10. Medyje pasirinkite Mokėjimo modelis.
11. Spustelėkite Importuoti.
    * Importuokite šį duomenų modelį. Jis bus naudojamas kaip duomenų šaltinis naujoje formato konfigūracijoje. Jei ši konfigūracija jau importuota, šį veiksmą praleiskite.  
12. Spustelėkite Taip.
13. Uždarykite puslapį.
14. Uždarykite puslapį.

## <a name="create-a-new-format-configuration"></a>Kurti naują formato konfigūraciją
1. Spustelėkite Ataskaitų konfigūracijos.
2. Medyje pasirinkite Mokėjimo modelis.
3. Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.
4. Lauke „Naujas“ įveskite „Formatas pagal duomenų modelį PaymentModel“.
    * Sukurkite formatą, paremtą duomenų modeliu „PaymentModel‟.  
5. Lauke Pavadinimas įveskite „Darbalapio ataskaitos pavyzdys‟.
    * Darbalapio ataskaitos pavyzdys  
6. Lauke Aprašas įveskite „Darbalapio ataskaitos, skirtos tiekėjų mokėjimams, pavyzdys‟.
    * Darbalapio ataskaitos, skirtos tiekėjų mokėjimams, pavyzdys.  
7. Lauke Duomenų modelio aprašas įveskite arba pasirinkite reikšmę.
    * Pasirinkite apibrėžtį „CustomerCreditTransferInitiation‟.  
8. Spustelėkite Sukurti konfigūraciją.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>Naujo dokumento kūrimas OPENXML darbalapio formatu
1. Medyje pasirinkite Mokėjimo modelis\Darbalapio ataskaitos pavyzdys.
2. Spustelėkite Konstruktorius.
3. Veiksmų srityje spustelėkite Importuoti.
4. Spustelėkite Importuoti iš „Excel‟.
5. Spustelėkite Priedai.
    * Kaip šabloną pridėkite esamą „Excel‟ dokumentą.  
6. Spustelėkite Naujas.
7. Spustelėkite Failas.
    * Nurodykite esamą „Excel“ failą.  
8. Uždarykite puslapį.
9. Lauke Šablonas įveskite arba pasirinkite reikšmę.
    * Pasirinkite pridėtą „Excel‟ failą, kuris bus naudojamas kaip šablonas.  
10. Spustelėkite GERAI.
    * Atkreipkite dėmesį, kad ER formato komponentai sukurti kūrimo formatu, paremtu susijusio „MS Excel‟ dokumento struktūra (įvardytaisiais diapazonais).  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Naujo duomenų šaltinio kūrimas, kad būtų galima skaičiuoti bendrąsias sumas pagal valiutos kodus
1. Spustelėkite skirtuką „Susiejimas“.
2. Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.
3. Medyje pasirinkite Funkcijos\Grupuoti pagal.
4. Lauke Pavadinimas įveskite „PaymentByCurrency‟.
    * PaymentByCurrency  
5. Spustelėkite Redaguoti grupę pagal.
6. Medyje išplėskite „modelis‟.
7. Medyje pasirinkite „modelis \ Mokėjimai“.
8. Spustelėkite Įtraukti lauką į.
9. Spustelėkite Ką grupuoti.
10. Medyje išplėskite „modelis \ Mokėjimai‟.
11. Medyje pasirinkite „modelis \ Mokėjimai \ Valiuta“.
12. Spustelėkite Įtraukti lauką į.
13. Spustelėkite Sugrupuoti laukai.
14. Medyje pasirinkite „modelis \ Mokėjimai \ Nurodyta suma (InstructedAmount)“.
15. Spustelėkite Įtraukti lauką į.
16. Spustelėkite Telkimo laukai.
17. Lauke Metodas pasirinkite parinktį.
    * Pasirinkite telkimo funkciją SUM.  
18. Lauke Pavadinimas įveskite „TotalInstructuredAmount‟.
    * TotalInstructuredAmount  
19. Spustelėkite Įrašyti.
20. Uždarykite puslapį.
21. Spustelėkite GERAI.

## <a name="map-format-components-to-data-sources"></a>Formato komponentų susiejimas su duomenų šaltiniais
1. Medyje išplėskite „modelis‟.
2. Medyje išplėskite „modelis \ Mokėjimai‟.
3. Medyje išplėskite „modelis \ Mokėjimai \ Inicijuojanti šalis(InitiatingParty)‟.
4. Medyje pasirinkite „modelis \ Mokėjimai \ Inicijuojanti šalis(InitiatingParty) \ Pavadinimas‟.
5. Medyje išplėskite „Excel \ ReportHeader”.
6. Medyje pasirinkite „Excel \ ReportHeader \ CompanyName”.
7. Spustelėkite Susieti.
8. Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius‟.
9. Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius \ Identifikacija‟.
10. Medyje pasirinkite „modelis \ Mokėjimai \ Kreditorius \ Identifikacija \ Šaltinio ID(SourceID)‟.
11. Medyje išplėskite „Excel \ PaymLines”.
12. Medyje pasirinkite „Excel \ PaymLines \ VendAccountName”.
13. Spustelėkite Susieti.
14. Medyje pasirinkite „modelis \ Mokėjimai \ Kreditorius \ Pavadinimas“.
15. Medyje pasirinkite „Excel \ PaymLines \ VendName”.
16. Spustelėkite Susieti.
17. Medyje išplėskite „modelis \ Mokėjimai \ Kreditoriaus agentas(CreditorAgent)‟.
18. Medyje pasirinkite „modelis \ Mokėjimai \ Kreditoriaus agentas(CreditorAgent) \ Pavadinimas‟.
19. Medyje pasirinkite „Excel \ PaymLines \ Bankas”.
20. Spustelėkite Susieti.
21. Medyje pasirinkite „modelis \ Mokėjimai \ Kreditoriaus agentas(CreditorAgent) \ Banko numeris(RoutingNumber)“.
22. Medyje pasirinkite „Excel \ PaymLines \ RoutingNumber”.
23. Spustelėkite Susieti.
24. Medyje išplėskite „modelis\Mokėjimai\Kreditoriaus sąskaita(Kreditoriaussąskaita)‟.
25. Medyje išplėskite „modelis\Mokėjimai\Kreditoriaus sąskaita(Kreditoriaussąskaita)\Identifikacija‟.
26. Medyje pasirinkite „modelis \ Mokėjimai \ Kreditoriaus sąskaita(CreditorAccount) \ Identifikacija \ Numeris‟.
27. Medyje pasirinkite „Excel \ PaymLines \ AccountNumber”.
28. Spustelėkite Susieti.
29. Medyje pasirinkite „modelis \ Mokėjimai \ Nurodyta suma (InstructedAmount)“.
30. Medyje pasirinkite „Excel \ PaymLines \ Debetas”.
31. Spustelėkite Susieti.
32. Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius‟.
33. Medyje išplėskite „modelis\Mokėjimai\Kreditoriaus sąskaita(Kreditoriaussąskaita)‟.
34. Medyje išplėskite „modelis \ Mokėjimai \ Kreditoriaus agentas(CreditorAgent)‟.
35. Medyje pasirinkite „modelis \ Mokėjimai \ Valiuta“.
36. Medyje pasirinkite „Excel \ PaymLines \ Valiuta”.
37. Spustelėkite Susieti.
38. Medyje išplėskite „PaymentByCurrency‟.
39. Medyje išplėskite „PaymentByCurrency \ sugrupuota‟.
40. Medyje pasirinkite „PaymentByCurrency \ sugrupuota \ Valiuta‟.
41. Medyje išplėskite „Excel \ SummaryLines”.
42. Medyje pasirinkite „Excel \ SummaryLines \ SummaryCurrency”.
43. Spustelėkite Susieti.
44. Medyje išplėskite „PaymentByCurrency \ sutelkta‟.
45. Medyje pasirinkite „PaymentByCurrency \ sutelkta \ TotalInstructuredAmount‟.
46. Medyje pasirinkite „Excel \ SummaryLines \ SummaryAmount”.
47. Spustelėkite Susieti.
48. Medyje pasirinkite „PaymentByCurrency‟.
49. Medyje pasirinkite „Excel \ SummaryLines”.
50. Spustelėkite Susieti.
51. Medyje pasirinkite „modelis \ Mokėjimai“.
52. Medyje pasirinkite „Excel \ PaymLines”.
53. Spustelėkite Susieti.
54. Spustelėkite Įrašyti.
55. Uždarykite puslapį.

## <a name="use-the-created-configuration-for-payments-processing"></a>Naudokite sukurtą konfigūraciją mokėjimams apdoroti
1. Spustelėkite keisti būseną.
2. Spustelėkite Baigti.
3. Spustelėkite GERAI.
4. Uždarykite puslapį.
5. Uždarykite puslapį.
6. Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo būdai.
7. Norėdami filtruoti lauką Mokėjimo būdas pagal reikšmę „Elektroninis“, naudokite spartųjį filtrą.
    * Elektroninis  
8. Spustelėkite Redaguoti.
9. Išplėskite dalį Failo formatai.
10. Lauke Bendrosios elektroninės ataskaitos pasirinkite Taip.
11. Lauke Eksportuoti formato konfigūraciją įveskite arba pasirinkite reikšmę.
    * Pasirinkite konfigūraciją „Darbalapio ataskaitos pavyzdys‟.  
12. Spustelėkite Įrašyti.
13. Uždarykite puslapį.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>Sukurtosios konfigūracijos naudojimas tikrinant mokėjimo žurnalų apdorojimą
1. Pasirinkite Mokėtinos sumos > Mokėjimai > Mokėjimų žurnalas.
2. Spustelėkite Naujas.
    * Sukurkite naują mokėjimų žurnalą.  
3. Lauke Pavadinimas įveskite „VendPay“.
    * VendPay  
4. Spustelėkite Eilutės.
5. Lauke Sąskaita nurodykite reikšmes „GB_SI_000001“.
    * GB_SI_000001  
6. Debetas nustatykite į „1000‟.
7. Spustelėkite Naujas.
8. Lauke Sąskaita nurodykite reikšmes „GB_SI_000005“.
    * GB_SI_000005  
9. Debetas nustatykite į „2000‟.
10. Lauke Valiuta įveskite „EUR‟.
    * EUR  
11. Lauke Korespondentinė sąskaita nurodykite reikšmes „GBSI OPER“.
    * GBSI OPER  
12. Lauke Mokėjimo būdas įveskite „Elektroninis‟.
    * Elektroninis  
13. Spustelėkite Įrašyti.
14. Spustelėkite Generuoti mokėjimus.
15. Lauke Mokėjimo būdas įveskite „Elektroninis‟.
    * Elektroninis  
16. Lauke Failo vardas, įveskite „Mokėjimai”.
    * Pvz., įveskite „Mokėjimai‟.  
17. Lauke Banko sąskaita įveskite „GBSI OPER‟.
    * GBSI OPER  
18. Spustelėkite GERAI.
19. Spustelėkite GERAI.
    * Peržiūrėkite sukurtąjį darbalapį – išsamią mokėjimo eilučių informaciją bei kiekvieno šiame mokėjimo pranešime naudojamo valiutos kodo bendrąsias sumas.  


