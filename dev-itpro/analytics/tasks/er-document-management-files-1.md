--- 
title: "Duomenų modelio rengimas, kad dokumentų valdymo failai galėtų būti naudojami formato išvestyse elektroninėse ataskaitose (ER)"
description: "Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: cc0909f99be9aad1b6bec22d4ed10381e0484a41
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="prepare-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a>Duomenų modelio rengimas, kad dokumentų valdymo failai galėtų būti naudojami formato išvestyse elektroninėse ataskaitose (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje. Šiuos veiksmus galima atlikti bet kurioje įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite juos užbaigti procedūroje „Sukurti konfigūracijos teikėją ir pažymėti jį kaip aktyvų“.

Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Gaukite prieigą prie „Microsoft“ teikiamų konfigūracijų sąrašo
1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
    * Įsitikinkite, kad teikėjas „Litware, Inc.“ yra pasiekiamas ir pažymėtas kaip aktyvus.  
2. Pasirinkite „Litware, Inc.“ „Litware, Inc.“.
3. Spustelėkite Saugyklos.
    * Jei tipo Operacijų ištekliai saugykla jau yra, praleiskite likusius dabartinės antrinės užduoties veiksmus.  
4. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
5. Lauke Konfigūracijų saugyklos tipas įveskite Operacijų ištekliai.
6. Spustelėkite Kurti saugyklą.
7. Spustelėkite GERAI.

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a>Gaukite Kliento SF modelio konfigūracijas, kurias teikia „Microsoft“
1. Spustelėkite Rodyti filtrus.
2. Taikykite toliau nurodytus filtrus: lauke Pavadinimas įveskite filtro reikšmę Operacijų ištekliai, naudodami filtro operatorių Prasideda; lauke Aprašas įveskite filtro reikšmę "", naudodami filtro operatorių Prasideda
3. Spustelėkite Rodyti filtrus.
4. Spustelėkite Atidaryti.
5. Medyje pasirinkite Kliento SF modelis.
    * Pasirinkite modelio konfigūraciją Kliento SF modelis, kad ją importuotumėte.  
6. Spustelėkite Importuoti.
    * Spustelėkite Importuoti 1 pasirinktos konfigūracijos versiją.  
7. Spustelėkite Taip.
8. Uždarykite puslapį.
9. Uždarykite puslapį.
10. Spustelėkite Ataskaitų konfigūracijos.
11. Medyje pasirinkite Kliento SF modelis.

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a>Kurkite išvestinį modelį, norėdami palaikyti prieigą prie dokumentų valdymo failų.
    * Savo kliento SF modelio konfigūraciją sukursite pagal „Microsoft“ pateiktą konfigūraciją. Šią konfigūraciją galima naudoti norint suteikti prieigą prie dokumentų valdymo failų ir nustatyti, kad juos būtų galima naudoti elektroniniuose dokumentuose, kuriuos sukursite pagal šį modelį.  
1. Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.
2. Lauke Naujas įveskite Kildinti iš pavadinimo: kliento SF modelis, „Microsoft“.
3. Lauke Pavadinimas įveskite Kliento SF modelis (pasirinktinis).
    * Kliento SF modelis (pasirinktinis)  
4. Spustelėkite Sukurti konfigūraciją.


