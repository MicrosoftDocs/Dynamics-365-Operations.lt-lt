--- 
title: "Formato modifikavimas ir vykdymas, kad dokumentų valdymo failai galėtų būti naudojami formato išvestyse elektroninėse ataskaitose (ER)"
description: "Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: 5d4f57ae2a309d9e15c1afe60c3e91d7d7eb3870
ms.openlocfilehash: e145c4c7a1f3fd88481ad32d0af05511437e21dc
ms.contentlocale: lt-lt
ms.lasthandoff: 11/02/2017

---
# <a name="modify-and-run-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a>Formato modifikavimas ir vykdymas, kad dokumentų valdymo failai galėtų būti naudojami formato išvestyse elektroninėse ataskaitose (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje. Šiuos veiksmus galima atlikti DEMF įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: dokumentų valdymo failų naudojimas formato išvestyse (4 dalis): formato paleidimas“.

Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a>Keiskite formatą, jei norite priedus įvesti į generuojamus pranešimus dvejetainiu formatu
1. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.
2. Medyje išplėskite Kliento SF modelis.
3. Medyje išplėskite dalį Kliento SF modelis / kliento SF modelis (pasirinktinis).
4. Medyje pasirinkite Kliento SF modelis / kliento SF modelis (pasirinktinis) / elektroninės SF pranešimo pavyzdys.
5. Spustelėkite Konstruktorius.
    * SF pranešimas bus automatiškai įvedamas generuojamoje išvestyje kaip XML failas naudojant UNICODE kodavimą.  
6. Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.
7. Medyje pasirinkite „Bendra \ Failas“.
8. Lauke Pavadinimas įveskite XML pranešimas.
    * XML pranešimas  
9. Lauke „Kodavimas“ įveskite „UTF-8“.
    * UTF-8  
10. Spustelėkite GERAI.
    * Sukonfigūruokite generuojamą išvestį kaip suglaudintą failą.  
11. Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.
12. Medyje pasirinkite Bendra / aplankas.
13. Lauke Pavadinimas įveskite ZIP išvestis.
    * ZIP išvestis  
14. Spustelėkite GERAI.
15. Medyje pasirinkite ZIP išvestis.
    * Pridėkite priedų prie generuojamo suglaudinto failo kaip failus su pradiniais pavadinimais ir plėtiniais.  
16. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
17. Medyje pasirinkite „Bendra \ Failas“.
18. Lauke Pavadinimas įveskite Pridėtas failas.
    * Pridėtas failas  
19. Spustelėkite GERAI.
20. Medyje pasirinkite ZIP išvestis / pridėtas failas.
21. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
22. Medyje pasirinkite Text\Base64.
23. Spustelėkite GERAI.

## <a name="map-new-format-elements-to-data-model"></a>Susiekite naujo formato elementus su duomenų modeliu
1. Spustelėkite skirtuką „Susiejimas“.
2. Medyje išplėskite „modelis‟.
3. Medyje išplėskite model\Invoice attachments.
4. Medyje pasirinkite ZIP išvestis / pridėtas failas / Base64.
5. Medyje pasirinkite model\Invoice attachments\File content.
6. Spustelėkite Susieti.
7. Medyje pasirinkite ZIP išvestis / pridėtas failas.
8. Spustelėkite Redaguoti failo vardą.
9. Medyje išplėskite „modelis‟.
10. Medyje išplėskite model\Invoice attachments.
11. Medyje pasirinkite model\Invoice attachments\File name.
12. Spustelėkite „Įtraukti duomenų šaltinį“.
13. Spustelėkite Įrašyti.
14. Uždarykite puslapį.
15. Medyje pasirinkite model\Invoice attachments.
16. Spustelėkite Susieti.
17. Spustelėkite Įrašyti.
18. Uždarykite puslapį.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Paleiskite sukurtą pasirinktos SF ataskaitą
1. Spustelėkite Vykdyti.
2. Išplėskite dalį Įtrauktini įrašai ().
3. Spustelėkite Filtras.
4. Pasirinkite kliento SF žurnalo eilutę ir lauką Pardavimo užsakymas.
5. Lauko Kriterijai kriterijų lauke Pardavimo užsakymas įveskite užsakymo numerį 000148.
    * 000148  
6. Spustelėkite GERAI.
7. Spustelėkite GERAI.
    * Peržiūrėkite sugeneruotą išvestį. Atkreipkite dėmesį – be SF pranešimo XML formatu sukuriamas vienas failas kiekvienam priedui. Priedų failai yra užpildomi įvedant suglaudintos išvesties duomenis dvejetainiu formatu.  


