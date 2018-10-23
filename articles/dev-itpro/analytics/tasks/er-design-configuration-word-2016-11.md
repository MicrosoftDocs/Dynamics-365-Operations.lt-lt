--- 
title: "ER konfigūracijų kūrimas siekiant generuoti ataskaitas „Word“ formatu"
description: "Toliau nurodytuose veiksmuose paaiškinta, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmens vartotojas gali konfigūruoti elektroninių ataskaitų formatus, norėdamas ataskaitas generuoti kaip „Microsoft Word” failus."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: dc47d44285af4c720d2f450d11fb1004ef461d0f
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a>ER konfigūracijų kūrimas siekiant generuoti ataskaitas „Word“ formatu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Toliau nurodytuose veiksmuose paaiškinta, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmens vartotojas gali konfigūruoti elektroninių ataskaitų (ER) formatus, norėdamas ataskaitas generuoti kaip „Microsoft Word” failus. Šiuos veiksmus galima atlikti GBSI įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite užbaigti užduočių vadovo „ER konfigūracijos, skirtos generuoti ataskaitoms OPENXML formatu, kūrimas“ veiksmus. Iš anksto taip pat turite atsisiųsti ir įrašyti šiuos šablonus vietoje ataskaitos pavyzdžiui:

- [Mokėjimo ataskaitos šablonas](https://go.microsoft.com/fwlink/?linkid=862266)
- [Susietas mokėjimo ataskaitos šablonas](https://go.microsoft.com/fwlink/?linkid=862266)


Ši procedūra yra skirta funkcijai, įtrauktai į „Microsoft Dynamics 365 for Operations“ 1611 versiją.


## <a name="select-the-existing-er-report-configuration"></a>Pasirinkite esamą ER ataskaitos konfigūraciją
1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
    * Įsitikinkite, kad konfigūracijos teikėjas „Litware, Inc.“. pasirinktas kaip aktyvus.  
2. Spustelėkite Ataskaitų konfigūracijos.
    * Pakartotinai naudosime esamą ER konfigūraciją, kuri iš pradžių buvo skirta ataskaitos išvesčiai OPENXML formatu generuoti.  
3. Medyje išplėskite „Mokėjimo modelis‟.
4. Medyje pasirinkite Mokėjimo modelis\Darbalapio ataskaitos pavyzdys.
5. Spustelėkite Konstruktorius.

## <a name="replace-the-excel-template-with-the-word-template"></a>„Excel” šabloną pakeiskite „Word“ šablonu
    * Šiuo metu „Excel” dokumentas naudojamas kaip šablonas OPENXML formato išvesčiai generuoti. Importuosime ataskaitos šabloną „Word“ formatu.  
1. Spustelėkite Priedai.
    * Esamą „Excel” šabloną pakeiskite „Word“ šablonu SampleVendPaymDocReport.docx, kurį atsisiuntėte anksčiau. Atkreipkite dėmesį, kad šiame šablone yra tik dokumento maketas, kurį norime sugeneruoti kaip ER išvestį.  
2. Spustelėkite Naikinti.
3. Spustelėkite Taip.
4. Spustelėkite Naujas.
5. Spustelėkite Failas.
6. Spustelėkite Naršyti. Suraskite ir pasirinkite anksčiau atsisiųstą failą SampleVendPaymDocReport.docx. Spustelėkite GERAI.
    * Pasirinkite šabloną, kurį atsisiuntėte vykdydami ankstesnį veiksmą.  
7. Lauke Šablonas įveskite arba pasirinkite reikšmę.

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a>Išplėskite „Word“ šabloną įtraukdami pasirinktinę XML dalį
1. Spustelėkite Įrašyti.
    * Be to, norėdami išsaugoti konfigūracijos pakeitimus, atlikite veiksmą Įrašyti, kuriuo taip pat atnaujinamas pridėtas „Word” šablonas. Sukurto formato struktūra perkeliama į pridėtą „Word” dokumentą kaip nauja pasirinktinė XML dalis, kurios pavadinimas „Ataskaita“. Atminkite, kad pridėtame „Word” šablone yra ne tik dokumento maketas, kurį norime sugeneruoti kaip ER išvestį, bet ir duomenų struktūra, kuri apdorojimo metu ER perkels į šį šabloną.  
2. Spustelėkite Priedai.
    * Dabar turite susieti pasirinktinės XML dalies „Ataskaita“ elementus su „Word” dokumento dalimis.  
    * Jei esate susipažinę su „Word“ dokumentais, kurie gali būti sukurti kaip formos, turinčios su pasirinktinių XML dalių elementais susietų turinio valdiklių, paleiskite visus kitos papildomos užduoties veiksmus, kad sukurtumėte tokį dokumentą. Norėdami gauti daugiau informacijos, žr. šią nuorodą https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US. Priešingu atveju praleiskite visus kitos papildomos užduoties veiksmus.  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a>Norėdami gauti „Word“ dokumentą su pasirinktine XML dalimi, susiekite duomenis
    * Atidarykite šį dokumentą programa „Word“ ir atlikite tokius veiksmus: - atidarykite skirtuką „Word“ kūrėjas (pritaikykite juostelę, jei dar neįjungta);  - pasirinkite XML susiejimo sritį;  - peržvalgos sąraše pasirinkite pasirinktinę XML dalį „Ataskaita“;  - pasirinktos pasirinktinės XML dalies elementus susiekite su „Word“ dokumento turinio valdikliais;  - atnaujintą „Word” dokumentą įrašykite į vietinį diską.  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a>Įkelkite „Word“ šabloną su turinio valdikliais susieta pasirinktine XML dalimi
1. Spustelėkite Naikinti.
2. Spustelėkite Taip.
    * Įtraukite naują šabloną. Jei atlikote ankstesnės papildomos užduoties veiksmus, pasirinkite paruoštą ir įrašytą vietoje „Word“ dokumentą. Priešingu atveju pasirinkite „MS Word” šabloną SampleVendPaymDocReportBounded.docx, kurį atsisiuntėte anksčiau.  
3. Spustelėkite Naujas.
4. Spustelėkite Failas.
5. Spustelėkite Naršyti. Suraskite ir pasirinkite anksčiau atsisiųstą failą SampleVendPaymDocReportBounded.docx. Spustelėkite Gerai.
6. Lauke Šablonas pasirinkite dokumentą, kurį atsisiuntėte vykdydami ankstesnį veiksmą.
7. Spustelėkite Įrašyti.
8. Uždarykite puslapį.

## <a name="execute-the-format-to-create-word-output"></a>Formato paleidimas norint kurti „Word“ išvestį
1. Veiksmų srityje spustelėkite Konfigūracijos.
2. Spustelėkite Vartotojo parametrai.
3. Lauke Paleisti parametrus pasirinkite Taip.
4. Spustelėkite GERAI.
5. Spustelėkite Redaguoti.
6. Lauke Paleisti juodraštį pasirinkite Taip.
7. Spustelėkite Įrašyti.
8. Uždarykite puslapį.
9. Uždarykite puslapį.
10. Pasirinkite Mokėtinos sumos > Mokėjimai > Mokėjimų žurnalas.
11. Spustelėkite Eilutės.
12. Pažymėkite arba atžymėkite visas sąrašo eilutes.
13. Spustelėkite mokėjimo būsena.
14. Spustelėkite Nėra.
15. Spustelėkite Generuoti mokėjimus.
16. Spustelėkite GERAI.
17. Spustelėkite GERAI.
    * Analizuokite sugeneruotą išvestį. Įsidėmėkite, kad sukurta išvestis pateikiama „Word” formatu kartu su informacija apie apdorotus mokėjimus.  


