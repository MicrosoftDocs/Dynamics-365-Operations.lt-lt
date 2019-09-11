---
title: ER konfigūracijų kūrimas siekiant generuoti ataskaitas „Word“ formatu
description: Toliau nurodytuose veiksmuose paaiškinta, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmens vartotojas gali konfigūruoti elektroninių ataskaitų formatus, norėdamas ataskaitas generuoti kaip „Microsoft Word“ failus.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 327f03435ab55551953fd998dd89c831c76c4c26
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916027"
---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a>ER konfigūracijų kūrimas siekiant generuoti ataskaitas „Word“ formatu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Toliau nurodytuose veiksmuose paaiškinta, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmens vartotojas gali konfigūruoti elektroninių ataskaitų (ER) formatus, norėdamas ataskaitas generuoti kaip „Microsoft Word“ failus. Šiuos veiksmus galima atlikti GBSI įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite užbaigti užduočių vadovo „ER konfigūracijos, skirtos generuoti ataskaitoms OPENXML formatu, kūrimas“ veiksmus. Iš anksto taip pat turite atsisiųsti ir įrašyti šiuos šablonus vietoje ataskaitos pavyzdžiui:

- [Mokėjimo ataskaitos šablonas](https://go.microsoft.com/fwlink/?linkid=862266)
- [Susietas mokėjimo ataskaitos šablonas](https://go.microsoft.com/fwlink/?linkid=862266)


Ši procedūra yra skirta į 1611 „Microsoft Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.


## <a name="select-the-existing-er-report-configuration"></a>Pasirinkite esamą ER ataskaitos konfigūraciją
1. **Naršymo srityje eikite į Moduliai > Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos**. Įsitikinkite, kad konfigūracijos teikėjas „Litware, Inc.“. pasirinktas kaip aktyvus.  
2. Spustelėkite **Ataskaitų konfigūracijos**. Pakartotinai naudosime esamą ER konfigūraciją, kuri iš pradžių buvo skirta ataskaitos išvesčiai OPENXML formatu generuoti.  
3. Medyje išplėskite „Mokėjimo modelis‟.
4. Medyje pasirinkite Mokėjimo modelis\Darbalapio ataskaitos pavyzdys.
5. Spustelėkite Konstruktorius.

## <a name="replace-the-excel-template-with-the-word-template"></a>„Excel” šabloną pakeiskite „Word“ šablonu

Šiuo metu „Excel” dokumentas naudojamas kaip šablonas OPENXML formato išvesčiai generuoti. Importuosime ataskaitos šabloną „Word“ formatu.

1. Spustelėkite **Priedai**. Esamą „Excel” šabloną pakeiskite „Word“ šablonu SampleVendPaymDocReport.docx, kurį atsisiuntėte anksčiau. Atkreipkite dėmesį, kad šiame šablone yra tik dokumento maketas, kurį norime sugeneruoti kaip ER išvestį.  
2. Spustelėkite **Naikinti**.
3. Spustelėkite **Taip**.
4. Spustelėkite **Naujas**.
5. Spustelėkite **Failas**.
6. Spustelėkite **Naršyti**. Suraskite ir pasirinkite anksčiau atsisiųstą failą SampleVendPaymDocReport.docx. Spustelėkite **Gerai**. Pasirinkite šabloną, kurį atsisiuntėte vykdydami ankstesnį veiksmą.  
7. Lauke **Šablonas** įveskite arba pasirinkite reikšmę.

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a>Išplėskite „Word“ šabloną įtraukdami pasirinktinę XML dalį
1. Spustelėkite **Įrašyti**. Be to, norėdami išsaugoti konfigūracijos pakeitimus, atlikite veiksmą Įrašyti, kuriuo taip pat atnaujinamas pridėtas „Word” šablonas. Sukurto formato struktūra perkeliama į pridėtą „Word” dokumentą kaip nauja pasirinktinė XML dalis, kurios pavadinimas „Ataskaita“. Atminkite, kad pridėtame „Word” šablone yra ne tik dokumento maketas, kurį norime sugeneruoti kaip ER išvestį, bet ir duomenų struktūra, kuri apdorojimo metu ER perkels į šį šabloną.  
2. Spustelėkite **Priedai**.
    + Dabar turite susieti pasirinktinės XML dalies „Ataskaita“ elementus su „Word” dokumento dalimis.  
    + Jei esate susipažinę su „Word“ dokumentais, kurie gali būti sukurti kaip formos, turinčios su pasirinktinių XML dalių elementais susietų turinio valdiklių, paleiskite visus kitos papildomos užduoties veiksmus, kad sukurtumėte tokį dokumentą. Daugiau informacijos ieškokite temoje [Formų, kurias vartotojai užbaigia ar spausdina programoje „Word“, kūrimas](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US). Priešingu atveju praleiskite visus kitos papildomos užduoties veiksmus.  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a>Norėdami gauti „Word“ dokumentą su pasirinktine XML dalimi, susiekite duomenis

Atidarykite šį dokumentą programoje „Word“ ir atlikite toliau nurodytus veiksmus:  
1. Atidarykite skirtuką „Word“ programų kūrėjas (tinkinkite juostelę, jei ji dar neįjungta).
2. Pasirinkite XML susiejimo sritį.
3. Peržvalgoje pažymėkite pasirinktinę XML dalį Ataskaita.
4. Susiekite pažymėtos pasirinktinės XML dalies ir „Word“ dokumento turinio valdiklio elementus.  5. Įrašykite atnaujintą „Word“ dokumentą vietiniame diske.  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a>Įkelkite „Word“ šabloną su turinio valdikliais susieta pasirinktine XML dalimi
1. Spustelėkite **Naikinti**.
2. Spustelėkite **Taip**. Įtraukite naują šabloną. Jei atlikote ankstesnės papildomos užduoties veiksmus, pasirinkite paruoštą ir įrašytą vietoje „Word“ dokumentą. Priešingu atveju pasirinkite „MS Word” šabloną SampleVendPaymDocReportBounded.docx, kurį atsisiuntėte anksčiau.  
3. Spustelėkite **Naujas**.
4. Spustelėkite **Failas**.
5. Spustelėkite **Naršyti**. Suraskite ir pasirinkite anksčiau atsisiųstą failą SampleVendPaymDocReportBounded.docx. Spustelėkite **Gerai**.
6. Lauke **Šablonas** pasirinkite ankstesniame žingsnyje atsisiųstą dokumentą.
7. Spustelėkite **Įrašyti**.
8. Uždarykite puslapį.

## <a name="execute-the-format-to-create-word-output"></a>Formato paleidimas norint kurti „Word“ išvestį
1. **Veiksmų srityje** spustelėkite **Konfigūracijos**.
2. Spustelėkite **Vartotojo parametrai**.
3. Pažymėkite Taip lauke **Paleisti parametrus**.
4. Spustelėkite **Gerai**.
5. Spustelėkite **Redaguoti**.
6. Pažymėkite Taip lauke **Paleisti juodraštį**.
7. Spustelėkite **Įrašyti**.
8. Uždarykite puslapį.
9. Uždarykite puslapį.
10. **Naršymo srityje** eikite į **Moduliai > Mokėtinos sumos > Mokėjimai > Mokėjimo žurnalas**.
11. Spustelėkite **Eilutės**.
12. Pažymėkite arba atžymėkite visas sąrašo eilutes.
13. Spustelėkite **Mokėjimo būsena**.
14. Spustelėkite **Nėra**.
15. Spustelėkite **Generuoti mokėjimus**.
16. Spustelėkite **Gerai**.
17. Spustelėkite **Gerai**. Analizuokite sugeneruotą išvestį. Įsidėmėkite, kad sukurta išvestis pateikiama „Word” formatu kartu su informacija apie apdorotus mokėjimus.  

