---
title: Duomenų modelio aprašo pasirinkimas, kuriant formatus
description: Norėdami baigti šios procedūros veiksmus, pirmiausia turite atlikti procedūrą „ER sukurti konfigūracijos teikėją“ ir pažymėti jį kaip aktyvų.
author: kfend
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65b3a74f98282f01940c5d17f8aa893d174883da
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290131"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a>Duomenų modelio aprašo pasirinkimas, kuriant formatus

[!include [banner](../../includes/banner.md)]

Norėdami baigti šios procedūros veiksmus, pirmiausia turite atlikti procedūrą „ER sukurti konfigūracijos teikėją“ ir pažymėti jį kaip aktyvų. 

Ši procedūra nurodo, kaip modelio šakninis elementas gali būti pasirinktas kaip duomenų modelio aprašas norint įterpti elektroninių ataskaitų (ER) formato konfigūraciją, skirtą generuoti elektroninius dokumentus. Atlikdami šią procedūrą sukursite pavyzdinės įmonės „Litware, Inc.“ naują ER formato konfigūraciją. 

Ši procedūra skirta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo. Šiuos veiksmus galima atlikti naudojant bet kurį duomenų rinkinį.

1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
    * Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip aktyvus. Jei nematote šio konfigūracijos teikėjo, atlikite procedūros Kurkite konfigūracijos teikėją ir pažymėkite kaip aktyvų veiksmus.  
2. Spustelėkite Ataskaitų konfigūracijos.

## <a name="add-a-new-er-data-model-configuration"></a>Pridėkite naują ER duomenų modelio konfigūraciją
1. Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.
    * Mes pridėjome naują ER modelio konfigūraciją, kurioje yra duomenų modelis, skirtas naudoti kaip duomenų šaltinis Intrastat ataskaitoms generuoti.  
2. Lauke „Pavadinimas“ įrašykite „Mokėjimo modelis (fiktyvus)“.
    * Mokėjimo modelis (fiktyvus)  
3. Spustelėkite Sukurti konfigūraciją.
4. Spustelėkite Konstruktorius.
    * Atidarykite ER kūrimo priemonę, norėdami nurodyti šios konfigūracijos duomenų modelio struktūrą.  
    * Tarkime, kad mes kuriame duomenų modelį mokėjimų verslo domenui, kad palaikytų 2 mokėjimo būdus – kredito pervedimo ir tiesioginio debeto.  
5. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
6. Lauke Pavadinimas įrašykite „Mokėjimai – kredito pervedimas“.
    * Mokėjimai – kredito pervedimas  
7. Spustelėkite Pridėti.
8. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
9. Lauke „Naujas mazgas kaip” įveskite „Modelio šaknis”.
10. Lauke Pavadinimas įrašykite „Mokėjimai – tiesioginis debetas“.
    * Mokėjimai – tiesioginis debetas  
11. Spustelėkite Pridėti.
12. Spustelėkite Įrašyti.
13. Uždarykite puslapį.
14. Spustelėkite keisti būseną.
    * Užbaikite modelio juodraščio versiją, kad jis būtų prieinamas naujo modelio susiejimams ir formatams.  
15. Spustelėkite Baigti.
16. Spustelėkite GERAI.

## <a name="start-to-enter-a-new-er-format-configuration"></a>Pradėkite įvesti naują ER formato konfigūraciją
1. Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.
2. Lauke Naujas įveskite „Formatas, pagrįstas duomenų modeliu „Mokėjimo modelis (fiktyvus)“.
3. Lauke Duomenų modelio aprašas įveskite arba pasirinkite reikšmę.
    * Žinokite, kad visi pasirinkto duomenų modelio šakniniai elementai dabar prieinami pasirinkimui kaip duomenų modelio apibrėžtis. Jūs galite ir toliau kurti savo formatą, naudodami bet kokius reikiamus šakninius duomenų modelio elementus. Trūkstamas modelio susiejimas pasirinktam šakniniam elementui neužkerta jums kelio tęsti.  
4. Uždarykite puslapį.

## <a name="add-a-new-er-model-mapping-configuration"></a>Pridėkite naują ER modelio susiejimo konfigūraciją
1. Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.
2. Lauke Naujas įveskite „Modelio susiejimas, pagrįstas duomenų modeliu „Mokėjimo modelis (fiktyvus)“.
3. Lauke „Pavadinimas“ įrašykite „Mokėjimo modelio susiejimai (fiktyvūs)“.
    * Mokėjimo modelio susiejimai (fiktyvūs)  
4. Lauke Duomenų modelio aprašas įveskite arba pasirinkite reikšmę.
5. Spustelėkite Sukurti konfigūraciją.

## <a name="design-er-model-mappings"></a>Sukurkite ER modelio susiejimus
1. Spustelėkite Konstruktorius.
    * Naudokite ER kūrimo priemonę nurodyti modelio susiejimus reikalingiems šakniniams elementams.  
2. Spustelėkite Konstruktorius.
    * Modeliuokite pasirinkto modelio susiejimo nustatymą pasirinkto modelio šakniniam elementui.  
3. Medyje pasirinkite Dynamics 365 for Operations\Table records.
4. Spustelėkite „Įtraukti šaknį“.
5. Lauke Pavadinimas įveskite „Didžioji knyga“.
6. Lauke „Lentelė“, įveskite „LedgerJournalTrans“.
    * LedgerJournalTable  
7. Spustelėkite GERAI.
8. Spustelėkite Įrašyti.
9. Uždarykite puslapį.
10. Uždarykite puslapį.

## <a name="start-to-enter-another-new-er-format-configuration"></a>Pradėkite įvesti kitą naują ER formato konfigūraciją
1. Medyje pasirinkite „Payment model (fictitious)“.
2. Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.
3. Lauke Naujas įveskite „Formatas, pagrįstas duomenų modeliu „Mokėjimo modelis (fiktyvus)“.
4. Lauke Duomenų modelio aprašas įveskite arba pasirinkite reikšmę.
    * Žinokite, kad dabar tik vieną šakninį elementą galima susieti su programos duomenų šaltiniais. Kai bent vienas modelio susiejimas yra įvestas, tik modelio šakniniai elementai, susieti su programos duomenų šaltiniais, gali būti pasirinkti kaip modelio apibrėžtis, kai pridėtas ER formatas.   
5. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
