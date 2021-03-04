---
title: „Human Resources“ parametrų konfigūravimas
description: Kai kurie žmogiškųjų išteklių parametrai naudojami keliose įmonėse, o kiti – konkrečioje įmonėje. Šiame straipsnyje paaiškinama, kaip nustatyti konkrečios įmonės HR parametrus.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bac50c5f302797e28df2bc792893c8a682899a93
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419663"
---
# <a name="configure-human-resources-parameters"></a>„Human Resources“ parametrų konfigūravimas

Kai kurie modulio Personalas (HR) parametrai naudojami keliose įmonėse, o kiti – konkrečioje įmonėje. Šiame straipsnyje paaiškinama, kaip nustatyti konkrečios įmonės HR parametrus.

Personalo parametrams nustatyti naudojami du puslapiai. Jei parametrai yra bendrai naudojami keliose įmonėse, galite naudoti puslapį **Bendrai naudojami žmogiškųjų išteklių parametrai**. Jei parametrai skirti konkrečiai įmonei (kitaip tariant, parametrai taikomi prie vienai įmonei), naudokite puslapį **Personalo parametrai**. Puslapyje **Personalo parametrai** parametrai suskirstyti į šešis toliau pateiktus skirtukus.

-   Bendri
-   Įdarbinimas – sprendime „Dynamics 365 Human Resources“ jo nėra
-   Kompensacija
-   Numeracijos
-   Nedarbingumo dėl ligos ar slaugymo aktas (FMLA)
-   Darbuotojų savitarna

Kiekviename skirtuke yra informacijos, susijusios su viena įmone. Skirtuko **Bendra** parametrai apibrėžia informacijos apie neatvykimą, sužalojimus ir ligas bei naujus darbuotojus, rodymą. Šio skirtuko parametrai taip pat nustato kai kuriuos numatytuosius įrašus, rodomus, kai dirbate. Tiksliau sakant, šiame skirtuke galite pasirinkti spalvą, kurią norite taikyti atviroms neatvykimų operacijoms, nurodyti stiliaus aprašą, naudojamą ataskaitoms, aktyvinti integravimą tarp mokymosi kursų ir neatvykimų registravimo bei pasirinkti neatvykimo kodą, naudojamą šiam integravimui valdyti. Taip pat galite nurodyti, kiek laiko sužeidimo ir ligos atvejų incidentai turėtų būti laikomi bei nurodyti numatytąjį identifikavimo numerį, rodomą, kai pasamdomas naujas darbuotojas. 

Skirtuko **Įdarbinimas** parametrai apibrėžia dokumentų tipus, kurie naudojami korespondencijoje, automatiškai siunčiamoje pretendentams, ir įdarbinimo projektą, kuris naudojamas neprašytiems prašymams (nesusijusiems su konkrečiu įdarbinimo projektu). Nurodytas skirstymo pagal terminus laikotarpis nustato įdarbinimo projektus, įtrauktus į išklotinę **Suskirstyti pagal terminus projektai**, esančią darbo srityje **Įdarbinimo valdymas**. Nurodytas prašymo pateikimo termino įspėjimo laikotarpis yra naudojamas įdarbinimo projektams, kurių prašymo pateikimo terminas artėja, rodyti išklotinėje **Prašymo pateikimo terminas artėja**, esančioje darbo srityje **Įdarbinimas**. 

Skirtuko **Kompensacija** nustatymai apibrėžia, ar vartotojai turi patvirtinti, kad nori išsaugoti informaciją fiksuotosios arba kintamosios atlyginimo dalies planą. Jei pažymėsite žymės langelį **Įgalinti tikrinimo įrašymą**, uždarydami su kompensacija susijusį puslapį vartotojai gaus pranešimą, kuriame klausiama, ar jie nori įrašyti įrašą. Kai kuriuose kompensacijos valdymo puslapiuose vartotojai informacijos naikinti negali. Todėl, reikalaudami, kad vartotojai patvirtintų, jog jie nori įrašyti informaciją, galėsite riboti informaciją, kuri įrašoma, bet kurios vėliau negalima panaikinti. Jei žymės langelis **Aktyvinti įrašymo tvirtinimą** nepažymėtas, įrašai visada įrašomi iš karto, galimai anksčiau nei tai padaro vartotojas. Jei naudojate našumo valdymą, skirtuke **Kompensacija** taip pat galite pasirinkti vertinimo modelį, kuris bus naudojamas vietoje modelio, našumo vertinimo metu priskirto kompensavimo planams. 

### <a name="previously-released-functionality"></a>Anksčiau išleistos funkcijos

Skirtuko **Numeracija** parametrai nurodo sekas, naudojamas ID automatiškai priskirti elementams personalo srityje, pvz., prašymams, neatvykimo registracijoms, kompensavimo proceso rezultatams, atvejų numeriams, kursams ir kursų darbotvarkei. Norėdami prižiūrėti numeracijų nuorodas ir kodus, naudokite **Numeracijos** sąrašo puslapį (spustelėkite **Organizacijos administravimas** &gt; **Numeracijos** &gt; **Numeracijos**).

> [!NOTE]
> Išdirbtų valandų skaičius negali viršyti 1 250, o įdarbinimo trukmė negali viršyti 12 mėnesių. Šios didžiausios galimos reikšmės atitinka Jungtinių Amerikos Valstijų federalinę teisę. Galiausiai skirtuko **Darbuotojų savitarna** parametrai apibrėžia informaciją, kurią vadybininkai gali įvesti savo darbuotojų vardu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]