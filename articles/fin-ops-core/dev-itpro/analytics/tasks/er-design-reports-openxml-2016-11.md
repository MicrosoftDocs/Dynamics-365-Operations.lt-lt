---
title: 'ER: konfigūracijos, skirtos generuoti ataskaitoms OPENXML formatu, kūrimas (2016 m. lapkričio mėn.)'
description: Šiame straipsnyje aprašoma, kaip sukurti naują elektroninės ataskaitos konfigūraciją, kurioje yra šablonas elektroniniams dokumentams generuoti OPENXML formatu.
author: kfend
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form:
- ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
- ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
ms.openlocfilehash: 49d56c545498a3f1aa01a455aaf7f5c65dd3eeaa
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291091"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a>ER: konfigūracijos, skirtos generuoti ataskaitoms OPENXML formatu, kūrimas (2016 m. lapkričio mėn.)

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmens vartotojas gali sukurti naują elektroninių ataskaitų (ER) konfigūraciją, kurioje būtų elektroninių dokumentų generavimo OPENXML formatu šablonas. Ši konfigūracija bus naudojama apdoroti tiekėjų mokėjimams.

Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją. Šiuos veiksmus galima atlikti GBSI įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu“. Taip pat reikia turėti „Excel‟ failą, kuris bus importuotas kuriant šabloną. Šį failą galima rasti srityje [Mokėjimo ataskaitos šablonas](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx).


## <a name="upload-the-payments-data-model-configuration"></a>Mokėjimų duomenų modelio konfigūracijos nusiuntimas
1. Naršymo srityje eikite į **Moduliai > Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos**.
2. Sąraše pažymėkite kaip pavyzdys pateiktos įmonės „Litware, Inc.“ konfigūracijų teikėją. Jei nematote konfigūracijų teikėjo, turite atlikti veiksmus, nurodytus [Konfigūracijų teikėjų kūrimas ir pažymėjimas kaip aktyvių](er-configuration-provider-mark-it-active-2016-11.md).
3. Pasirinkite **Nustatyti kaip aktyvų**.
4. Pasirinkite **Saugyklos**. Jei yra, pasirinkite tipo Operacijų ištekliai saugyklą. Jei tokia yra, praleiskite tolesnius naujos saugyklos kūrimo veiksmus.  
5. Pasirinkite **Įtraukti** ir atidarykite išplečiamąjį dialogo langą.
6. Lauke **Konfigūracijos saugyklos tipas** įveskite `Operations resourcesdd`.
7. Pasirinkite **Kurti saugyklą**.
8. Pasirinkite **Gerai**.
9. Pasirinkite **Atidaryti**.
10. Medyje pasirinkite **Mokėjimo modelis**.
11. Pasirinkite **Importuoti**. Importuokite šį duomenų modelį. Jis bus naudojamas kaip duomenų šaltinis naujoje formato konfigūracijoje. Jei ši konfigūracija jau importuota, šį veiksmą praleiskite.  
12. Pasirinkite **Taip**.
13. Uždarykite puslapius, kol grįšite atgal į elektroninių ataskaitų puslapį.

## <a name="create-a-new-format-configuration"></a>Kurti naują formato konfigūraciją
1. Pasirinkite **Ataskaitų konfigūracijos**.
2. Medyje pasirinkite **Mokėjimo modelis**.
3. Pasirinkite **Kurti konfigūraciją**, kad atidarytumėte tiesioginį dialogo langą.
4. Lauke **Naujas** įveskite `Format based on data model PaymentModel`. Sukurkite formatą, paremtą duomenų modeliu „PaymentModel‟.
5. Lauke **Pavadinimas** įveskite `Sample worksheet report`. Darbalapio ataskaitos pavyzdys  
6. Lauke **Aprašas** įveskite `Sample worksheet report for vendors' payments`. Darbalapio ataskaitos, skirtos tiekėjų mokėjimams, pavyzdys.  
7. Lauke **Duomenų modelio aprašas** įveskite arba pasirinkite reikšmę. Pasirinkite aprašą **CustomerCreditTransferInitiation**.  
8. Pasirinkite **Kurti konfigūraciją**.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>Naujo dokumento kūrimas OPENXML darbalapio formatu
1. Medyje pasirinkite **Mokėjimo modelis\Darbalapio ataskaitos pavyzdys**.
2. Pasirinkite **Dizaino įrankis**.
3. Veiksmų srityje pasirinkite **Importuoti**.
4. Pasirinkite **Importuoti iš „Excel“**.
5. Pasirinkite **Priedai**. Kaip šabloną pridėkite esamą „Excel‟ dokumentą.  
6. Pasirinkite **Naujas**.
7. Pasirinkite **Failas**. Nurodykite esamą „Excel“ failą.  
8. Uždarykite puslapį.
9. Lauke **Šablonas** įveskite arba pasirinkite reikšmę. Pasirinkite pridėtą „Excel‟ failą, kuris bus naudojamas kaip šablonas.  
10. Pasirinkite **Gerai**. Atkreipkite dėmesį, kad ER formato komponentai sukurti kūrimo formatu, paremtu susijusio „MS Excel‟ dokumento struktūra (įvardytaisiais diapazonais).  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Naujo duomenų šaltinio kūrimas, kad būtų galima skaičiuoti bendrąsias sumas pagal valiutos kodus
1. Pasirinkite skirtuką **Susiejimas**.
2. Pasirinkite **Įtraukti šakninį elementą**, kad atidarytumėte tiesioginį dialogo langą.
3. Medyje pasirinkite **Funkcijos / grupavimas pagal**.
4. Lauke **Pavadinimas** įveskite „`PaymentByCurrency`“.
5. Pasirinkite **Redaguoti grupavimą pagal**.
6. Medyje išplėskite **modelį**, o tada pasirinkite **modelis\Mokėjimai**.
7. Pasirinkite **Įtraukti lauką į**.
8. Pasirinkite **Ką grupuoti**.
9. Medyje išplėskite **model\Payments**, o tada pasirinkite **model\Payments\Currency**.
10. Pasirinkite **Įtraukti lauką į**.
11. Pasirinkite **Sugrupuoti laukai**.
12. Medyje pasirinkite **model\Payments\Instructed Amount(InstructedAmount)**.
13. Pasirinkite **Įtraukti lauką į**, o tada pasirinkite **Agregavimo laukai**.
14. Lauke **Būdas** pasirinkite parinktį. Pasirinkite funkciją **Sumos agregavimas**.  
15. Lauke **Pavadinimas** įveskite `TotalInstructuredAmount`.
16. Pasirinkite **Įrašyti**.
17. Uždarykite puslapį.
18. Pasirinkite **Gerai**.

## <a name="map-format-components-to-data-sources"></a>Formato komponentų susiejimas su duomenų šaltiniais
1. Medyje pasirinkite **model\Payments\Initiating Party(InitiatingParty)\Name** ir **Excel\ReportHeader\CompanyName**.
2. Pasirinkite **Susieti**.
3. Medyje pasirinkite **model\Payments\Creditor\Identification\Source ID(SourceID)** ir **Excel\PaymLines\VendAccountName**.
4. Pasirinkite **Susieti**.
5. Medyje pasirinkite **model\Payments\Creditor\Name** ir **Excel\PaymLines\VendName**.
6. Pasirinkite **Susieti**.
7. Medyje pasirinkite **model\Payments\Creditor Agent(CreditorAgent)\Name** ir **Excel\PaymLines\Bank**.
8. Pasirinkite **Susieti**.
9. Medyje pasirinkite **model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)** ir **Excel\PaymLines\RoutingNumber**.
10. Pasirinkite **Susieti**.
11. Medyje pasirinkite **model\Payments\Creditor Account(CreditorAccount)\Identification\Number** ir **Excel\PaymLines\AccountNumber**.
12. Pasirinkite **Susieti**.
13. Medyje pasirinkite **model\Payments\Instructed Amount(InstructedAmount)** ir **Excel\PaymLines\Debit**.
14. Pasirinkite **Susieti**.
15. Medyje pasirinkite **model\Payments\Currency** ir **Excel\PaymLines\Currency**.
16. Pasirinkite **Susieti**.
17. Medyje pasirinkite **PaymentByCurrency\grouped\Currency** ir **Excel\SummaryLines\SummaryCurrency**.
18. Pasirinkite **Susieti**.
19. Medyje pasirinkite **PaymentByCurrency\aggregated\TotalInstructuredAmount** ir **Excel\SummaryLines\SummaryAmount**.
20. Pasirinkite **Susieti**.
21. Medyje pasirinkite **PaymentByCurrency** ir **Excel\SummaryLines**.
22. Pasirinkite **Susieti**.
23. Medyje pasirinkite **model\Payments** ir **Excel\PaymLines**.
24. Pasirinkite **Susieti**.
25. Pasirinkite **Įrašyti**, o tada uždarykite puslapį.

## <a name="use-the-created-configuration-for-payments-processing"></a>Naudokite sukurtą konfigūraciją mokėjimams apdoroti
1. Pasirinkti **Keisti būseną**.
2. Pasirinkite **Baigti**.
3. Pasirinkite **Gerai**.
4. Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Mokėjimo sąranką > Mokėjimo būdai**.
5. Naudokite spartųjį filtrą lauke **Mokėjimo būdas** su reikšme **Elektroninis**.
6. Pasirinkite **Redaguoti**.
7. Išplėskite skyrių **Failo formatai**.
8. Lauke **Bendrosios elektroninės ataskaitos** pasirinkite **Taip**.
9. Lauke **Eksportuoti formato konfigūraciją** įveskite arba pasirinkite reikšmę. Pasirinkite konfigūraciją **Pavyzdinio darbalapio ataskaita**.  
10. Pasirinkite **Įrašyti**.
11. Uždarykite puslapį.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>Sukurtosios konfigūracijos naudojimas tikrinant mokėjimo žurnalų apdorojimą
1. Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Mokėjimai > Mokėjimo žurnalas**.
2. Norėdami sukurti naują mokėjimo žurnalą, pasirinkite **Naujas**.
3. Lauke **Pavadinimas** įveskite **VendPay**.
4. Pasirinkite **Eilutės**.
5. Lauke **Sąskaita** nurodykite reikšmės „`GB_SI_000001`“.
6. Nustatykite **Debetas** į `1000`.
7. Pasirinkite **Naujas**.
8. Lauke **Sąskaita** nurodykite reikšmės `GB_SI_000005`.
9. Nustatykite **Debetas** į `2000`.
10. Lauke **Valiuta** įveskite `EUR`.
11. Lauke **Korespondentinė sąskaita** nurodykite reikšmės `GBSI OPER`.
12. Lauke **Mokėjimo būdas** įveskite `Electronic`.
13. Pasirinkite **Įrašyti**.
14. Pasirinkite **Generuoti mokėjimus**.
15. Lauke **Mokėjimo būdas** įveskite `Electronic`.
16. Lauke **Failo pavadinimas** įveskite `Payments`.
17. Lauke **Banko sąskaita** įveskite `GBSI OPER`.
18. Pasirinkite **Gerai**, tada dar kartą – **Gerai**. Peržiūrėkite sukurtąjį darbalapį – išsamią mokėjimo eilučių informaciją bei kiekvieno šiame mokėjimo pranešime naudojamo valiutos kodo bendrąsias sumas.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
