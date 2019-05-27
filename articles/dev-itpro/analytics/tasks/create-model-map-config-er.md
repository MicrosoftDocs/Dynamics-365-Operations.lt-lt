---
title: Elektroninės ataskaitos (ER) modelio susiejimo konfigūracijų kūrimas
description: Naudokite šią procedūrą norėdami sukurti naują elektroninių ataskaitų (ER) modelio susiejimo konfigūraciją ir, siekiant efektyviai sutelkti skaičiavimus, naudoti integruotas ER funkcijas.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 614ef06fcf5761f1cf2afb6e7655558d2858d763
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544961"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a>Elektroninės ataskaitos (ER) modelio susiejimo konfigūracijų kūrimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Naudokite šią procedūrą norėdami sukurti naują elektroninių ataskaitų (ER) modelio susiejimo konfigūraciją ir, siekiant efektyviai sutelkti skaičiavimus, naudoti integruotas ER funkcijas. Šioje procedūroje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją. 

Ši procedūra sukurta vartotojams, kuriems priskirtas vaidmuo Sistemos administratorius arba Elektroninių ataskaitų teikimo programuotojas.

Šiuos veiksmus galima atlikti naudojant bet kurį duomenų rinkinį. Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu“.

1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
    * Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip aktyvus. Jei nematote šio konfigūracijos teikėjo, atlikite procedūros „Kurkite konfigūracijos teikėją ir pažymėkite kaip aktyvų“ veiksmus.  
2. Spustelėkite Ataskaitų konfigūracijos.
3. Spustelėkite Rodyti filtrus.
4. Lauke „Pavadinimas“ įveskite filtro reikšmę „Intrastat” ir naudokite filtro operatorių „prasideda”.
    * Taikykite šį filtrą norėdami rasti „Intrastat“ duomenų modelio konfigūraciją. Šis modelis jau gali būti konfigūracijos medyje. Jei taip atsitiktų, praleiskite kitą antrinę užduotį.   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a>Gaukite „Microsoft“ teikiamas Intrastat modelio konfigūracijas
1. Uždarykite puslapį.
2. Uždarykite puslapį.
3. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
4. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite plytelę „Microsoft“ teikėjas.  
5. Spustelėkite Saugyklos.
    * Plytelėje „Microsoft“ teikėjas spustelėkite Saugyklos.  
6. Spustelėkite Rodyti filtrus.
7. Lauke „Įveskite pavadinimą“ įveskite filtro reikšmę „ištekliai” ir naudokite filtro operatorių „apima”. 
8. Spustelėkite Atidaryti.
9. Medyje pasirinkite „Intrastat model“ (Intrastat modelis).
10. Spustelėkite Importuoti.
11. Spustelėkite Taip.
    * Importavote ER modelio konfigūraciją, kurioje yra duomenų modelis, kurį naudosite norėdami ištirti, kaip gali būti naudojama nauja ER funkcija.  
12. Uždarykite puslapį.
13. Uždarykite puslapį.
14. Spustelėkite Ataskaitų konfigūracijos.

## <a name="add-a-new-model-mapping-configuration"></a>Pridėti naują modelio susiejimo konfigūraciją
1. Medyje pasirinkite „Intrastat model“ (Intrastat modelis).
2. Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.
3. Lauke Naujas įveskite „Modelio susiejimas pagal duomenų modelio Intrastat“.
4. Lauke Pavadinimas įveskite „Intrastat pavyzdžio susiejimas“.
    * „Intrastat“ pavyzdžio susiejimas  
5. Spustelėkite Sukurti konfigūraciją.

