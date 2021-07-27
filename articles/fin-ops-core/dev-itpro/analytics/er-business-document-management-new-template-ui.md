---
title: „Microsoft Office” stiliaus vartotojo sąsaja Verslo dokumentų valdyme
description: Šioje temoje paaiškinama, kaip naudoti naują vartotojo sąsają Elektroninių ataskaitų (ER) sistemos funkcijoje Verslo dokumentų valdymas.
author: v-anamir
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e8a3782e5beb7d16accc0a56447d5db1f1376dd8
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350189"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>„Microsoft Office” stiliaus vartotojo sąsaja Verslo dokumentų valdyme

[!include [banner](../includes/banner.md)]

Verslo dokumentų valdymas leidžia verslo vartotojams redaguoti verslo dokumentų šablonus naudojant „Microsoft 365 service“ paslaugą arba atitinkamą „Microsoft Office“ darbalaukio programą. Redagavimas gali būti dizaino keitimai arba nauji diegimai arba vartotojai gali įtraukti vietos rezervavimo ženklų, kad galėtų įtraukti papildomų duomenų, nekeisdami šaltinio kodo. Norėdami gauti daugiau informacijos apie tai, kaip naudotis funkcija Verslo dokumentų valdymas, žr. [Funkcijos Verslo dokumentų valdymas apžvalga](er-business-document-management.md).

Naujo vartotojo sąsaja (UI) yra aiškesnė ir patogesnė naudoti. Srityje **Verslo dokumentas** rodomi tik tie šablonai, kurie yra pasiekiami dabartiniam tiekėjui. Ankstesnėje vartotojo sąsajoje, skirtuke **Šablonas** buvo išvardyti visi šablonai, galimi bet kuriam teikėjui. Taip pat joje buvo rodomi visi šablonai, kuriuos sukūrė ir redagavo bet kuris vartotojas, turintis tokį patį vaidmenį.

Galite naudoti mygtuką **Naujas dokumentas** kurti ir redaguoti šabloną Elektroninių ataskaitų (ER) formato konfigūracijoje, kurią pateikia kitas teikėjas. Šioje temoje pateikiamame pavyzdyje teikėjas yra „Microsoft“. Taip pat galite sukurti šabloną įkeldami savo šabloną „Excel” formatu.


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

Video (parodytas aukščiau) apie tai, kaip [Kurti naują verslo dokumentą naudojant Verslo dokumentų valdymą](https://youtu.be/gAIYl-mM_pw) yra įtrauktas į [„Finance and Operations” grojaraštį](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), prieinamą „YouTube”.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Naujo dokumento vartotojo sąsajos įjungimas funkcijoje Verslo dokumentų valdymas

Norėdami pradėti naudoti naujo dokumento vartotojo sąsają funkcijoje Verslo dokumentų valdymas, turite įjungti funkciją **Į „Office“ panaši vartotojo sąsaja funkcijoje Verslo dokumentų valdymas** darbo srityje **Funkcijų valdymas**.

Atlikite tolesnius veiksmus, norėdami įjungti šią funkciją visiems juridiniams subjektams.

1. Iš darbo srities **Funkcijų valdymas** skirtuko **Visi** sąrašo pasirinkite funkciją **Į „Office“ panaši vartotojo sąsajos patirtis Verslo dokumentų valdymui**.
2. Pasirinkite **Įjungti dabar**, kad įjungtumėte pasirinktą funkciją.
3. Norėdami pasiekti naują funkciją, atnaujinkite puslapį.

## <a name="edit-templates-that-are-owned-by-other-providers"></a>Šablonų, priklausančių kitiems teikėjams, redagavimas

1. Darbo srityje **Verslo dokumentų valdymas** pasirinkite **Naujas dokumentas**.

    ![Darbo sritis Verslo dokumentų valdymas.](./media/BDM_overview_new_template1.png)

2. Skirtuke **Pasirinkti** pasirinkite dokumentą, kurį norite naudoti kaip šabloną, o tada pasirinkite **Kurti dokumentą**.

    ![Verslo dokumentų dialogo langas.](./media/BDM_overview_new_template2.png)

3. Naujo dialogo lango lauke **Pavadinimas** pakeiskite pavadinimą į norimą pavadinimą. Pavadinimo tekstas naudojamas automatiškai sukurtai naujai ER formato konfigūracijai pavadinti. Šios konfigūracijos (**Kliento laisvos formos sąskaitos-faktūros ataskaitos (GER) kopija**) juodraščio versijoje bus suredaguotas šablonas ir ji bus naudojama vykdant šį ER formatą, skirtą dabartiniam vartotojui. Originalus šablonas iš pagrindinio ER formato konfigūracijos bus naudojamas visiems kitiems vartotojams skirtam ER formatui vykdyti.
4. Lauke **Pavadinimas** pakeiskite redaguojamo šablono, kuris bus automatiškai sukurtas, pirmo pataisymo pavadinimą.
5. Lauke **Komentaras** atnaujinkite redaguojamo šablono, kuris bus automatiškai sukurtas, pataisymo pastabas.
6. Pasirinkite **Gerai**, kad patvirtintumėte redagavimo proceso pradžią.

    ![Dokumento kūrimo dialogo langas.](./media/BDM_overview_new_template3.png)

Paspaudus mygtuką **Naujas dokumentas**, sukuriamas ir redaguojamas šablonas ER formato konfigūracijoje, kurią pateikia kitas teikėjas. Šiame pavyzdyje teikėjas yra „Microsoft“. Pasirinkę **Naujas dokumentas**, peržiūrėsite visus šablonus, priklausančius dabartiniam ir kitiems teikėjams. Pasirinktas šablonas atidaromas ir jį galima redaguoti. Redaguotas šablonas bus išsaugotas naujoje automatiškai sugeneruotoje ER formato konfigūracijoje.

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a>Esamą „Excel” formatą naudojančio šablono įkėlimas
Norėdami pateikti reikiamą informaciją prieš šablono įkėlimą, atlikite šiuos veiksmus.

1. Darbo srityje **Verslo dokumentų valdymas** pasirinkite **Naujas dokumentas**.

    ![Darbo sritis Verslo dokumentų valdymas.](./media/BDM_overview_new_template1.png)
    
2. Puslapio **Kurti naują šabloną** skirtuko **Įkelti** skirtuke **Šablonas** pasirinkite **Naršyti**, kad surastumėte ir pasirinktumėte „Excel” failą, kurį norite naudoti kaip šabloną. Skyriaus **Šablono** laukai **Pavadinimas** ir **Aprašas** yra užpildomi automatiškai. Jie nurodo naujos, automatiškai kuriamos, ER formato konfigūracijos pavadinimą ir aprašą. Prireikus galite redaguoti šiuos laukus.
3. Skyriaus **Dokumento tipas** lauke **Pavadinimas** nurodykite verslo dokumento tipą. Ši reikšmė bus naudojama ieškoti tinkamam duomenų šaltiniui (tai yra, ER modelio konfigūracijai).

    ![Šablono skirtukas.](./media/BDM_overview_new_UI_import_21.jpg)

4. Skirtuko **Duomenų šaltinis** „FastTab” **Filtras** pasirinkite **Taikyti filtrą**. Skyriaus **Duomenų šaltinio** laukas **Pavadinimas** yra užpildomas automatiškai arba galite jo reikšmę pasirinkti rankiniu būdu. Galite naudoti filtrą atitinkamam duomenų šaltinio vardui ieškoti pagal vardą, aprašą, šalies/regiono kodą ir verslo dokumento tipą.

    ![Duomenų šaltinio skirtukas.](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > „FastTab” **Filtruoti** yra naudojamas ieškoti tinkamam duomenų šaltiniui (tai yra, ER modelio konfigūracijai). Galite redaguoti visus filtro laukus, kad rastumėte tinkamiausią duomenų šaltinį įkeliamam dokumentui.
    > 
    > „FastTab” **Filtruoti** esančios sąlygos yra naudojamos kaip **ARBA** sąlygos.
    
5. Skirtuke **Susiejimas** pasirinkite **Automatiškai aptikti**. Laukas **Šakninis aprašas** yra užpildomas automatiškai arba galite jo reikšmę pasirinkti rankiniu būdu. Šiame skirtuke rodomas galutinis šablono ir modelio elementų susiejimas.

    ![Susiejimo skirtukas.](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > Susiejimas skyriuje **Šablono struktūra** naudoja duomenų šaltinio žymų arba aprašų vartotojo kalba, esančių langelio pavadinime šablone, visišką atitiktį.

6. Pasirinkite **Kurti dokumentą**, kad patvirtintumėte, jog norite sukurti šabloną ir pradėti redagavimo procesą.

Daugiau informacijos žr. [Verslo dokumentų valdymo apžvalga](er-business-document-management.md).

Jeigu nėra tiekėjo Elektroninėse ataskaitose, jį galite sukurti. Jeigu nėra aktyvaus teikėjo, galite pasirinkti jį aktyvavimui.

- Norėdami sukurti teikėją, pakeiskite teikėjo pavadinimą lauke **Pavadinimas**, atnaujinkite naujo teikėjo internetinį adresą lauke **Internetinis adresas** ir pasirinkite **Gerai** patvirtinimui.

    ![Naujo BDM teikėjo kūrimas.](./media/bdm_create_provider.png)
    
- Norėdami aktyvuoti esamą teikėją, pasirinkite teikėjo pavadinimą lauke **Konfigūracijos teikėjas** ir pasirinkite **Gerai**, kad nustatytumėte teikėją aktyviu.

    ![BDM teikėjo aktyvavimas.](./media/bdm_choose_provider.png)

> [!NOTE]
> Kiekvienas BDM šablonas kreipiasi į teikėją kaip į konfigūracijos autorių. Štai todėl šablonui reikia aktyvaus teikėjo.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
