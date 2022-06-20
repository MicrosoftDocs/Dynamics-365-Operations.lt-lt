---
title: 'ER: dokumentų valdymo failų naudojimas formato išvestyse (1 dalis – Duomenų modelio ruošimas)'
description: Šiame straipsnyje aprašoma, kaip sukonfigūruoti elektroninių ataskaitų (ER) formatą, kad būtų galima naudoti dokumentų valdymo failus (priedus) ER išvestyje. (1 dalis)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7818b4916de7f3afbead0da39aa471f690d8f5e7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908390"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a>ER: dokumentų valdymo failų naudojimas formato išvestyse (1 dalis – Duomenų modelio ruošimas)

[!include [banner](../../includes/banner.md)]

Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje. Šiuos veiksmus galima atlikti bet kurioje įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu“.

Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Gaukite prieigą prie „Microsoft“ teikiamų konfigūracijų sąrašo
1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.

    Įsitikinkite, kad teikėjas „Litware, Inc.“ yra pasiekiamas ir pažymėtas kaip aktyvus.  

2. Pasirinkite „Litware, Inc.“ „Litware, Inc.“.
3. Spustelėkite Saugyklos.

    Jei tipo Operacijų ištekliai saugykla jau yra, praleiskite likusius dabartinės antrinės užduoties veiksmus.  

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

    Pasirinkite modelio konfigūraciją Kliento SF modelis, kad ją importuotumėte.  

6. Spustelėkite Importuoti.

    Spustelėkite Importuoti 1 pasirinktos konfigūracijos versiją.  

7. Spustelėkite Taip.
8. Uždarykite puslapį.
9. Uždarykite puslapį.
10. Spustelėkite Ataskaitų konfigūracijos.
11. Medyje pasirinkite Kliento SF modelis.

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a>Kurkite išvestinį modelį, norėdami palaikyti prieigą prie dokumentų valdymo failų.
Savo kliento SF modelio konfigūraciją sukursite pagal „Microsoft“ pateiktą konfigūraciją. Šią konfigūraciją galima naudoti norint suteikti prieigą prie dokumentų valdymo failų ir nustatyti, kad juos būtų galima naudoti elektroniniuose dokumentuose, kuriuos sukursite pagal šį modelį.  
1. Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.
2. Lauke Naujas įveskite Kildinti iš pavadinimo: kliento SF modelis, „Microsoft“.
3. Lauke Pavadinimas įveskite Kliento SF modelis (pasirinktinis).
4. Spustelėkite Sukurti konfigūraciją.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]