--- 
title: "Modelių susiejimas, kad finansinės dimensijos galėtų būti naudojamos kaip duomenų šaltinis elektroninėse ataskaitose (ER)"
description: "Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: bbc7401284146c2ab4fdfe325cfefb95d1eefb81
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="map-models--to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a>Modelių susiejimas, kad finansinės dimensijos galėtų būti naudojamos kaip duomenų šaltinis elektroninėse ataskaitose (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį. Šiuos veiksmus galima atlikti bet kurioje įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite užbaigti atlikti veiksmus, nurodytus procedūroje „ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (1 dalis: duomenų modelio kūrimas)“.


## <a name="add-required-data-sources-to-model-mapping"></a>Būtinų duomenų šaltinių įtraukimas į modelio susiejimą
1. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.
2. Medyje pasirinkite Finansinių dimensijų modelio pavyzdys.
3. Spustelėkite Konstruktorius.
4. Spustelėkite „Susieti modelį su duomenų šaltiniu“.
5. Spustelėkite Naujas.
6. Lauke Apibrėžimas pasirinkite Įrašas.
7. Lauke Pavadinimas įveskite Dimensijų duomenų susiejimas.
8. Lauke Aprašas įveskite Dimensijų duomenų susiejimas.
9. Spustelėkite Įrašyti.
10. Spustelėkite Konstruktorius.
11. Medyje pasirinkite „Dynamics 365 for Operations\Table“.
12. Spustelėkite „Įtraukti šaknį“.
13. Lauke „Pavadinimas“ įveskite „Įmonė“.
14. Lauke „Lentelė“, įveskite „CompanyInfo“.
15. Spustelėkite Gerai.
16. Medyje pasirinkite Functions\Financial dimensions details.
17. Spustelėkite „Įtraukti šaknį“.
    * Šis duomenų šaltinis nurodo, kaip bus apibrėžta kiekvienos ataskaitos, kurioje šis modelis bus naudojamas kaip duomenų šaltinis, finansinių dimensijų apimtis.  
18. Lauke Pavadinimas surinkite reikšmę.
19. Lauke Prašyti dimensijų pasirinkite Taip.
    * Pasirinkite Taip, jei norite leisti vartotojui vykdymo metu pasirinkti dimensijas formoje Vartotojo dialogo langas. Jei pasirinksite NE, visos šio egzemplioriaus finansinės dimensijos bus naudojamas kaip numatytosios.  
20. Lauke Finansinių dimensijų pasirinkimas pasirinkite Juridinis subjektas.
    * Pasirinkite Visos, jei norite leisti vartotojui pasirinkti norimas dabartinio egzemplioriaus dimensijas lauke Peržvalga.  Pasirinkite Juridinis subjektas, jei norite leisti vartotojui pasirinkti įmonės dimensijas lauke Peržvalga.  Pasirinkite Dimensija, jei norite leisti vartotojui pasirinkti dimensijas naudojant vieną dimensijų rinkinį.  
21. Lauke Prašyti pagrindinės sąskaitos pasirinkite Taip.
    * Nustatykite parinktį Prašyti pagrindinės sąskaitos į Taip, kad jei norite leisti vartotojams pasirinkti pagrindinę sąskaitą kaip dimensijų sąrašo dalį.   Jei pasirinksite Ne, pagrindinė sąskaita nebus įtraukta į dimensijų sąrašą ir parinktis Pagrindinė sąskaita yra privaloma bus įjungta. Jei parinktį Pagrindinė sąskaita yra privaloma nustatysite į Taip, įtraukite pagrindinę sąskaitą į dimensijų sąrašą neatsižvelgdami į vartotojo pasirinkimą.  
22. Spustelėkite GERAI.
23. Medyje pasirinkite „Dynamics 365 for Operations\Table records“.
24. Spustelėkite „Įtraukti šaknį“.
25. Lauke Pavadinimas įveskite LedgerJournal.
26. Lauke „Prašyti užklausos“ pasirinkite „Taip“.
27. Lauke Lentelė įveskite LedgerJournalTable.
28. Spustelėkite GERAI.

## <a name="map-data-model-elements-to-added-data-sources"></a>Duomenų modelio elementų susiejimas su įtrauktais duomenų šaltiniais
1. Medyje išplėskite dalį Žurnalas.
2. Medyje išplėskite dalį Journal\Transaction.
3. Medyje išplėskite Journal\Transaction\Dimensions data.
4. Medyje išplėskite dalį Dimensijų parametras.
5. Medyje išplėskite dalį LedgerJournal.
6. Medyje išplėskite LedgerJournal\<Relations.
7. Medyje išplėskite dalį LedgerJournal\<Relations\LedgerJournalTrans.
8. Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Voucher.
9. Medyje pasirinkite Journal\Transaction\Voucher.
10. Spustelėkite Susieti.
11. Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension).
    * Atminkite, kad su bet kokia nuoroda į finansines dimensijas, nustatyta į, pavyzdžiui, LedgerDimension, galima naudoti atitinkamą duomenų šaltinio elementą (LedgerDimension.Dimension). Šis duomenų šaltinio elementas pateikia finansines dimensijas, kurios nustatytos kaip įrašo sąrašas.  
12. Medyje išplėskite dalį LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension).
13. Medyje išplėskite dalį LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions.
14. Medyje išplėskite dalį LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value.
15. Medyje išplėskite dalį LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition.
16. Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name.
17. Medyje pasirinkite Journal\Transaction\Dimensions data\Name.
18. Spustelėkite Susieti.
19. Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description.
20. Medyje pasirinkite Journal\Transaction\Dimensions data\Description.
21. Spustelėkite Susieti.
22. Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code.
23. Medyje pasirinkite Journal\Transaction\Dimensions data\Code.
24. Spustelėkite Susieti.
25. Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions.
26. Medyje pasirinkite Journal\Transaction\Dimensions data.
27. Spustelėkite Susieti.
28. Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit).
29. Medyje pasirinkite Journal\Transaction\Debit.
30. Spustelėkite Susieti.
31. Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate).
32. Medyje pasirinkite Journal\Transaction\Date.
33. Spustelėkite Susieti.
34. Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode).
35. Medyje pasirinkite Journal\Transaction\Currency.
36. Spustelėkite Susieti.
37. Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit).
38. Medyje pasirinkite Journal\Transaction\Credit.
39. Spustelėkite Susieti.
40. Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans.
41. Medyje pasirinkite Journal\Transaction.
42. Spustelėkite Susieti.
43. Medyje pasirinkite LedgerJournal\Journal batch number(JournalNum).
44. Medyje pasirinkite Journal\Batch.
45. Spustelėkite Susieti.
46. Medyje pasirinkite LedgerJournal.
47. Medyje pasirinkite Žurnalas.
48. Spustelėkite Susieti.
49. Medyje išplėskite dalį Dimensijos.
50. Medyje išplėskite dalį Dimensions\Main account and dimensions.
51. Medyje išplėskite dalį Dimensions\Main account and dimensions\Definition.
52. Medyje pasirinkite Dimensions\Main account and dimensions\Definition\Name.
53. Medyje pasirinkite Dimensions setting\Code.
54. Spustelėkite Susieti.
55. Medyje pasirinkite Dimensions\Main account and dimensions\Definition\Report column name.
56. Medyje pasirinkite Dimensions setting\Name.
57. Spustelėkite Susieti.
58. Medyje pasirinkite Dimensions\Main account and dimensions.
59. Medyje pasirinkite Dimensijų parametras.
60. Spustelėkite Susieti.
61. Medyje pasirinkite Įmonė.
62. Spustelėkite Redaguoti.
63. Lauke expressionAsStringText įveskite Company.'find()'.'name()'.
    * Company.'find()'.'name()'  
64. Spustelėkite Įrašyti.
65. Uždarykite puslapį.
66. Spustelėkite Įrašyti.
67. Uždarykite puslapį.

## <a name="complete-this-draft-models-version"></a>Šio modelio versijos juodraščio užbaigimas
1. Uždarykite puslapį.
2. Uždarykite puslapį.
3. Spustelėkite keisti būseną.
4. Spustelėkite Baigti.
5. Spustelėkite GERAI.


