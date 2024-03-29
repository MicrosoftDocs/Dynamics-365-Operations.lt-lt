---
title: 'ER: dokumentų valdymo failų naudojimas formato išvestyse (5 dalis – Formato modifikavimas ir paleidimas)'
description: Šiame straipsnyje aprašoma, kaip sukonfigūruoti elektroninių ataskaitų (ER) formatą, kad būtų galima naudoti dokumentų valdymo failus (priedus) ER išvestyje. (5 dalis)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
ms.openlocfilehash: 093bf93ef747279ee8213a3e3f16f140c6ba2426
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290911"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a>ER: dokumentų valdymo failų naudojimas formato išvestyse (5 dalis – Formato modifikavimas ir paleidimas)

[!include [banner](../../includes/banner.md)]

Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje. Šiuos veiksmus galima atlikti DEMF įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: dokumentų valdymo failų naudojimas formato išvestyse (4 dalis. Formato paleidimas)“.

Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.


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
5. Lauko Kriterijai kriterijų lauke „Pardavimo užsakymas“ įveskite užsakymo numerį 000148.
    * 000148  
6. Spustelėkite Gerai.
7. Spustelėkite Gerai.
    * Peržiūrėkite sugeneruotą išvestį. Atkreipkite dėmesį, kad be SF pranešimo XML formatu sukuriamas vienas failas kiekvienam priedui. Priedų failai yra užpildomi įvedant suglaudintos išvesties duomenis dvejetainiu formatu.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
