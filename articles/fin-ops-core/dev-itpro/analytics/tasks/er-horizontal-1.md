---
title: 'ER: horizontaliai išplečiamų diapazonų naudojimas norint dinamiškai įtraukti stulpelius į „Excel“ ataskaitas (1 dalis – Formato kūrimas)'
description: Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas ataskaitas generuoti kaip OPENXML darbalapių („Excel“) failus, kuriuose būtinus stulpelius galima dinamiškai kurti kaip horizontaliai išplečiamus diapazonus.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e36a2238ab4c67a2384d6da2a1e2c767414c21a1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684504"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a>ER: horizontaliai išplečiamų diapazonų naudojimas norint dinamiškai įtraukti stulpelius į „Excel“ ataskaitas (1 dalis – Formato kūrimas)

[!include [banner](../../includes/banner.md)]

Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas ataskaitas generuoti kaip OPENXML darbalapių („Excel“) failus, kuriuose būtinus stulpelius galima dinamiškai kurti kaip horizontaliai išplečiamus diapazonus. Šiuos veiksmus galima atlikti bet kurioje įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite baigti šiuos tris užduočių vadovus: 

„ER: konfigūracijos teikėjo kūrimas ir žymėjimas aktyviu“

„ER: finansinių dimensijų naudojimas kaip duomenų šaltinis (1 dalis. Duomenų modelio kūrimas)“

„ER: finansinių dimensijų naudojimas kaip duomenų šaltinis (2 dalis. Modelio susiejimas)“

Taip pat turite atsisiųsti ir įrašyti vietinę šablono kopiją su ataskaitos pavyzdžiu, esančią čia [Finansinių ataskaitų pavyzdžių žiniatinklio tarnybos ataskaita](https://go.microsoft.com/fwlink/?linkid=862266).

Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.


## <a name="create-a-new-report-configuration"></a>Naujos ataskaitos konfigūracijos kūrimas
1. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.
2. Medyje pasirinkite Finansinių dimensijų modelio pavyzdys.
3. Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.
4. Lauke Naujas įveskite Formatas, pagrįstas duomenų modeliu Finansinių dimensijų modelio pavyzdys.
    * Naudokite iš anksto sukurtą modelį kaip naujos ataskaitos duomenų šaltinį.  
5. Lauke Pavadinimas įveskite Ataskaitos su horizontaliai išplečiamais diapazonais pavyzdys.
    * Ataskaitos su horizontaliai išplečiamais diapazonais pavyzdys  
6. Lauke Aprašas įveskite „Excel“ išvesties su dinamiškai įtraukiamais stulpeliais kūrimas.
    * „Excel“ išvesties su dinamiškai įtraukiamais stulpeliais kūrimas  
7. Lauke Duomenų modelio aprašas pasirinkite Įrašas.
8. Spustelėkite Sukurti konfigūraciją.

## <a name="design-the-report-format"></a>Ataskaitos formato kūrimas
1. Spustelėkite Konstruktorius.
2. Įjunkite perjungimo mygtuką „Rodyti išsamią informaciją“.
3. Veiksmų srityje spustelėkite Importuoti.
4. Spustelėkite Importuoti iš „Excel‟.
5. Spustelėkite Priedai.
    * Importuokite ataskaitos šabloną. Naudokite „Excel“ failą, kurį šiuo tikslu atsisiuntėte.  
6. Spustelėkite Naujas.
7. Spustelėkite Failas.
8. Uždarykite puslapį.
9. Lauke Šablonas įveskite arba pasirinkite reikšmę.
    * Pasirinkite atsisiųstą šabloną.  
10. Spustelėkite GERAI.
    * Įtraukite naują diapazoną, norėdami dinamiškai kurti „Excel“ išvestį su tiek finansinių dimensijų stulpelių, kiek pasirinkote (vartotojo dialogo formoje). Kiekvienas kiekvieno stulpelio langelis nurodys vienos finansinės dimensijos pavadinimą.  
11. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
12. Medyje pasirinkite Excel\Range.
13. Lauke „Excel“ diapazonas įveskite DimNames.
    * DimNames  
14. Lauke Dubliavimo kryptis pasirinkite Horizontali.
15. Spustelėkite Gerai.
16. Medyje pasirinkite Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal.
17. Spustelėkite Perkelti aukštyn.
18. Medyje pasirinkite Excel = "SampleFinDimWsReport"\Cell<DimNames>.
19. Spustelėkite Iškirpti.
20. Medyje pasirinkite Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal.
21. Spustelėkite Įklijuoti.
22. Medyje išplėskite Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal.
23. Medyje išplėskite Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical.
24. Medyje išplėskite Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical.
25. Medyje pasirinkite Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical.
    * Įtraukite naują diapazoną, norėdami dinamiškai kurti „Excel“ išvestį su tiek finansinių dimensijų stulpelių, kiek pasirinkote (vartotojo dialogo formoje). Kiekvienas kiekvieno stulpelio langelis nurodys vienos finansinės dimensijos reikšmę, skirtą kiekvienai ataskaitų operacijai.  
26. Spustelėkite Įtraukti diapazoną.
27. Lauke „Excel“ diapazonas įveskite DimValues.
    * DimValues  
28. Lauke Dubliavimo kryptis pasirinkite Horizontali.
29. Spustelėkite Gerai.
30. Medyje pasirinkite Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>.
31. Spustelėkite Iškirpti.
32. Medyje pasirinkite Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal.
33. Spustelėkite Įklijuoti.
34. Medyje išplėskite Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal.

## <a name="map-format-elements-to-data-sources"></a>Formato elementų susiejimas su duomenų šaltiniais
1. Spustelėkite skirtuką „Susiejimas“.
2. Medyje išplėskite dalį model: Data model Financial dimensions sample model.
3. Medyje išplėskite dalį model: Data model Financial dimensions sample model\Journal: Record list.
4. Medyje išplėskite dalį model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list.
5. Medyje išplėskite dalį model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list.
6. Medyje pasirinkite Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>.
7. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String.
8. Spustelėkite Susieti.
9. Medyje pasirinkite Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal.
10. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list.
11. Spustelėkite Susieti.
12. Medyje pasirinkite Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>.
13. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real.
14. Spustelėkite Susieti.
15. Medyje pasirinkite Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>.
16. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real.
17. Spustelėkite Susieti.
18. Medyje pasirinkite Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>.
19. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String.
20. Spustelėkite Susieti.
21. Medyje pasirinkite Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>.
22. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date.
23. Spustelėkite Susieti.
24. Medyje pasirinkite Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>.
25. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String.
26. Spustelėkite Susieti.
27. Medyje pasirinkite Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>.
28. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Batch: String.
29. Spustelėkite Susieti.
30. Medyje pasirinkite Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical.
31. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list.
32. Spustelėkite Susieti.
33. Medyje pasirinkite Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>.
34. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Batch: String.
35. Spustelėkite Susieti.
36. Medyje pasirinkite Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical.
37. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list.
38. Spustelėkite Susieti.
39. Medyje išplėskite dalį model: Data model Financial dimensions sample model\Dimensions setting: Record list.
40. Medyje pasirinkite dalį model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String.
41. Medyje pasirinkite Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'.
42. Spustelėkite Susieti.
43. Medyje pasirinkite dalį model: Data model Financial dimensions sample model\Dimensions setting: Record list.
44. Medyje pasirinkite Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal.
45. Spustelėkite Susieti.
46. Medyje pasirinkite Excel = "SampleFinDimWsReport"\Cell<CompanyName>.
47. Medyje pasirinkite model: Data model Financial dimensions sample model\Company: String.
48. Spustelėkite Susieti.
49. Spustelėkite Įrašyti.
50. Uždarykite puslapį.

