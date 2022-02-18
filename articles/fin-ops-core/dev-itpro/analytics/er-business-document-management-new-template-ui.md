---
title: Microsoft Office- verslo dokumentų valdymo stiliaus vartotojo sąsaja (yra vaizdo įrašas)
description: Šioje temoje paaiškinama, kaip naudoti naują vartotojo sąsają Elektroninių ataskaitų (ER) sistemos funkcijoje Verslo dokumentų valdymas.
author: v-anamir
ms.date: 01/05/2022
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
ms.openlocfilehash: e33830e2147d92ad5ee53ad11da55a50613b8ef9
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8074746"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>„Microsoft Office” stiliaus vartotojo sąsaja Verslo dokumentų valdyme

[!include [banner](../includes/banner.md)]

Verslo dokumentų valdymas leidžia verslo vartotojams redaguoti verslo dokumentų šablonus naudojant „Microsoft Office 365“ paslaugą arba atitinkamą „Microsoft Office“ darbalaukio programą. Redagavimas gali būti dizaino keitimai arba nauji diegimai arba vartotojai gali įtraukti vietos rezervavimo ženklų, kad galėtų įtraukti papildomų duomenų, nekeisdami šaltinio kodo. Norėdami gauti daugiau informacijos apie tai, kaip naudotis funkcija Verslo dokumentų valdymas, žr. [Funkcijos Verslo dokumentų valdymas apžvalga](er-business-document-management.md).

Naujo vartotojo sąsaja (UI) yra aiškesnė ir patogesnė naudoti. The **Verslo dokumentas** srityje rodomi tik šablonai, kurie priklauso dabartinei [aktyvus](tasks/er-configuration-provider-mark-it-active-2016-11.md)[teikėjas](general-electronic-reporting.md#Provider) ir yra dabartiniame egzemplioriuje Dynamics 365 Finance. Ankstesnėje vartotojo sąsajoje **Šablonas** skirtuke išvardyti visi šablonai, kurie buvo prieinami bet kuriam teikėjui. Taip pat joje buvo rodomi visi šablonai, kuriuos sukūrė ir redagavo bet kuris vartotojas, turintis tokį patį vaidmenį.

Galite naudoti **Naujas dokumentas** mygtuką **Verslo dokumentų tvarkymas** darbo sritis, skirta šablonui kurti ir redaguoti [Elektroninis ataskaitų teikimas (ER)](general-electronic-reporting.md) formatu [konfigūracija](general-electronic-reporting.md#Configuration) kurį teikia kitas teikėjas ir yra dabartiniame „Finance“ egzemplioriuje, arba įkelti naują šabloną iš „Excel“ darbaknygės. Be to, 10.0.25 ir naujesnėse versijose galite naudoti **Naujas dokumentas** mygtuką, norėdami sukurti ir redaguoti ER formato konfigūracijos šabloną, kuris saugomas [Pasaulinė saugykla](general-electronic-reporting.md#Repository).

Šios temos pavyzdžiuose aktyvus teikėjas yra „Contoso“, kurį naudojate kurdami šabloną, pagrįstą „Microsoft“ pateiktu šablonu. Taip pat galite sukurti šabloną įkeldami savo šabloną „Excel” formatu.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWAVQg]

The [Sukurkite naują verslo dokumentą naudodami verslo dokumentų valdymą](https://youtu.be/gAIYl-mM_pw) vaizdo įrašas (parodytas aukščiau) yra įtrauktas į [„Finance and Operations“ grojaraštis](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) galima YouTube.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Naujo dokumento vartotojo sąsajos įjungimas funkcijoje Verslo dokumentų valdymas

Norėdami pradėti naudoti naujo dokumento vartotojo sąsają funkcijoje Verslo dokumentų valdymas, turite įjungti funkciją **Į „Office“ panaši vartotojo sąsaja funkcijoje Verslo dokumentų valdymas** darbo srityje **Funkcijų valdymas**.

Atlikite tolesnius veiksmus, norėdami įjungti šią funkciją visiems juridiniams subjektams.

1. Iš darbo srities **Funkcijų valdymas** skirtuko **Visi** sąrašo pasirinkite funkciją **Į „Office“ panaši vartotojo sąsajos patirtis Verslo dokumentų valdymui**.
2. Pasirinkite **Įjungti dabar**, kad įjungtumėte pasirinktą funkciją.
3. Norėdami pasiekti naują funkciją, atnaujinkite puslapį.

## <a name="add-or-activate-a-provider"></a>Pridėkite arba suaktyvinkite teikėją

Kiekvienas verslo dokumento šablonas saugomas ER formato konfigūracijoje, kuri pažymėta kaip priklausanti konkrečiam konfigūracijos teikėjui. Kai kuriate naują šabloną, sukuriama nauja ER formato konfigūracija, skirta jam laikyti. Todėl tos konfigūracijos teikėjas turi būti nustatytas. Šiuo tikslu naudojamas aktyvus ER sistemos teikėjas. Jei ER nėra teikėjo, galite jį sukurti. Jei nėra *aktyvus* teikėją, galite suaktyvinti vieną iš esamų teikėjų. Kai reikia, atidaromas tiekėjo įtraukimo arba aktyvinimo dialogo langas, o pradedate pridėti naują šabloną.

### <a name="add-a-new-provider"></a>Įtraukti naują teikėją

Norėdami sukurti naują teikėją, atlikite šiuos veiksmus **Konfigūracijos teikėjas** dialogas:

1.  Ant **Pasirinkite konfigūracijos teikėją** skirtuke **vardas** lauke įveskite naujo teikėjo pavadinimą.
2.  Viduje konors **Interneto adresas** laukelyje įveskite naujo teikėjo interneto adresą (URL). 
3.  Pasirinkite **Gerai**.

    ![Naujo verslo dokumentų valdymo teikėjo kūrimas.](./media/bdm_create_provider.png)

Pridėtas teikėjas bus automatiškai suaktyvintas.

### <a name="activate-a-provider"></a>Suaktyvinkite tiekėją

Norėdami suaktyvinti teikėją, atlikite šiuos veiksmus **Konfigūracijos teikėjas** dialogas:

1.  Ant **Pasirinkite konfigūracijos teikėją** skirtuke **Konfigūracijos teikėjas** lauke, pasirinkite teikėją.
2.  Pasirinkite **Gerai**.

    ![Verslo dokumentų valdymo paslaugų teikėjo aktyvinimas.](./media/bdm_choose_provider.png)

Pasirinktas teikėjas bus suaktyvintas.

> [!NOTE]
> Kiekvienas verslo dokumentų valdymo šablonas yra ER formato konfigūracijoje, kuri nurodo teikėją kaip konfigūracijos autorių. Todėl kiekvienam šablonui reikalingas aktyvus teikėjas.

## <a name="edit-a-template-that-is-owned-by-another-provider"></a>Redaguokite šabloną, kuris priklauso kitam teikėjui

Šiame pavyzdyje parodyta, kaip naudoti **Naujas dokumentas** mygtuką **Verslo dokumentų tvarkymas** darbo sritis, skirta sukurti ir redaguoti šabloną ER formato konfigūracija, kurią teikia kitas teikėjas ir yra dabartiniame „Finance“ egzemplioriuje. Šiame pavyzdyje aktyvus teikėjas yra „Contoso“, kuris naudoja „Microsoft“ pateiktą ER formato konfigūraciją. Po to, kai pasirinksite **Naujas dokumentas**, **skirtuką** ant **Sukurkite naują šabloną** puslapyje rodomi visi dabartinio finansų egzemplioriaus šablonai, priklausantys dabartiniam teikėjui ir kitiems teikėjams. Pasirinkite šabloną, kad jį atidarytumėte. Tada galite sukurti naują redaguojamą šablono kopiją. Redaguotas šablonas saugomas naujoje ER formato konfigūracijoje, kuri generuojama automatiškai.

1. Darbo srityje **Verslo dokumentų valdymas** pasirinkite **Naujas dokumentas**.

    ![Darbo sritis Verslo dokumentų valdymas.](./media/BDM_overview_new_template1.png)

2. Ant **Sukurkite naują šabloną** puslapyje, esančiame **Pasirinkite** skirtuke pasirinkite dokumentą, kurį norite naudoti kaip šabloną, tada pasirinkite **Sukurti dokumentą**.

    ![Verslo dokumentų dialogo langas.](./media/BDM_overview_new_template2.png)

3. Naujo dialogo lango lauke **Pavadinimas** pakeiskite pavadinimą į norimą pavadinimą. Pavadinimo tekstas naudojamas automatiškai sukurtai naujai ER formato konfigūracijai pavadinti. Šios konfigūracijos (**Kliento laisvos formos sąskaitos-faktūros ataskaitos (GER) kopija**) juodraščio versijoje bus suredaguotas šablonas ir ji bus naudojama vykdant šį ER formatą, skirtą dabartiniam vartotojui. Originalus šablonas iš pagrindinio ER formato konfigūracijos bus naudojamas visiems kitiems vartotojams skirtam ER formatui vykdyti.
4. Lauke **Pavadinimas** pakeiskite redaguojamo šablono, kuris bus automatiškai sukurtas, pirmo pataisymo pavadinimą.
5. Lauke **Komentaras** atnaujinkite redaguojamo šablono, kuris bus automatiškai sukurtas, pataisymo pastabas.
6. Pasirinkite **Gerai**, kad patvirtintumėte redagavimo proceso pradžią.

    ![Dokumento kūrimo dialogo langas.](./media/BDM_overview_new_template3.png)

## <a name="upload-a-template-that-uses-an-existing-excel-workbook"></a>Įkelkite šabloną, kuriame naudojama esama „Excel“ darbaknygė

Šiame pavyzdyje parodyta, kaip naudoti **Naujas dokumentas** mygtuką **Verslo dokumentų tvarkymas** darbo sritis, skirta sukurti ir redaguoti ER formato konfigūracijos šabloną pagal turimą „Excel“ darbaknygę. Šiame pavyzdyje aktyvus teikėjas yra „Contoso“, o jūs naudojate ER [duomenų modelis](er-overview-components.md#data-model-component) ir ER [modelio kartografavimas](er-overview-components.md#model-mapping-component) konfigūracijos, kurias teikia Microsoft. Po to, kai pasirinksite **Naujas dokumentas**, pasirinkite **Įkelti** skirtuką ant **Sukurkite naują šabloną** puslapį. Čia galite nurodyti išsamią „Excel“ darbaknygės įkėlimo informaciją. Įkėlus „Excel“ darbaknygę, ji paverčiama verslo dokumento šablonu, kuris atidaromas redaguoti. Redaguotas šablonas bus saugomas naujoje ER formato konfigūracijoje, kuri sugeneruojama automatiškai.

Norėdami pateikti reikiamą informaciją prieš šablono įkėlimą, atlikite šiuos veiksmus.

1. Darbo srityje **Verslo dokumentų valdymas** pasirinkite **Naujas dokumentas**.
2. Puslapio **Kurti naują šabloną** skirtuko **Įkelti** skirtuke **Šablonas** pasirinkite **Naršyti**, kad surastumėte ir pasirinktumėte „Excel” failą, kurį norite naudoti kaip šabloną. Skyriaus **Šablono** laukai **Pavadinimas** ir **Aprašas** yra užpildomi automatiškai. Jie nurodo naujos, automatiškai kuriamos, ER formato konfigūracijos pavadinimą ir aprašą. Prireikus galite redaguoti šiuos laukus.
3. Skyriaus **Dokumento tipas** lauke **Pavadinimas** nurodykite verslo dokumento tipą. Ši reikšmė bus naudojama ieškoti tinkamam duomenų šaltiniui (tai yra, ER modelio konfigūracijai).

    ![Skirtukas Šablonas, esantis puslapio Sukurti naują šabloną skirtuke Įkėlimas.](./media/BDM_overview_new_UI_import_21.jpg)

4. Skirtuko **Duomenų šaltinis** „FastTab” **Filtras** pasirinkite **Taikyti filtrą**. Skyriaus **Duomenų šaltinio** laukas **Pavadinimas** yra užpildomas automatiškai arba galite jo reikšmę pasirinkti rankiniu būdu. Galite naudoti filtrą atitinkamam duomenų šaltinio vardui ieškoti pagal vardą, aprašą, šalies/regiono kodą ir verslo dokumento tipą.

    ![Duomenų šaltinio skirtukas, esantis puslapio Kurti naują šabloną skirtuke Įkėlimas.](./media/BDM_overview_new_UI_import_31.jpg)

    > [!NOTE]
    > „FastTab” **Filtruoti** yra naudojamas ieškoti tinkamam duomenų šaltiniui (tai yra, ER modelio konfigūracijai). Galite redaguoti visus filtro laukus, kad rastumėte tinkamiausią duomenų šaltinį įkeliamam dokumentui.
    > 
    > „FastTab” **Filtruoti** esančios sąlygos yra naudojamos kaip **ARBA** sąlygos.

5. Skirtuke **Susiejimas** pasirinkite **Automatiškai aptikti**. Laukas **Šakninis aprašas** yra užpildomas automatiškai arba galite jo reikšmę pasirinkti rankiniu būdu. Šiame skirtuke rodomas galutinis šablono ir modelio elementų susiejimas.

    ![Puslapio Sukurti naują šabloną skirtuke Įkėlimas esantis skirtukas Susiejimas.](./media/BDM_overview_new_UI_import_41.jpg)

    > [!NOTE]
    > Susiejimas skyriuje **Šablono struktūra** naudoja duomenų šaltinio žymų arba aprašų vartotojo kalba, esančių langelio pavadinime šablone, visišką atitiktį.

6. Pasirinkite **Kurti dokumentą**, kad patvirtintumėte, jog norite sukurti šabloną ir pradėti redagavimo procesą.

Daugiau informacijos žr. [Verslo dokumentų valdymo apžvalga](er-business-document-management.md).

## <a name="upload-a-template-from-the-global-repository"></a>Įkelkite šabloną iš pasaulinės saugyklos

Šiame pavyzdyje parodyta, kaip naudoti **Naujas dokumentas** mygtuką **Verslo dokumentų tvarkymas** darbo sritis, skirta sukurti ir redaguoti šabloną ER formato konfigūracija, kurią teikia Microsoft ir kuri yra visuotinėje saugykloje. Šiame pavyzdyje aktyvus teikėjas yra „Contoso“, kuris naudoja „Microsoft“ pateiktą ER formato konfigūraciją. Po to, kai pasirinksite **Naujas dokumentas**, **iš pasaulinės saugyklos** skirtuką ant **Sukurkite naują šabloną** puslapyje rodomi visi verslo dokumentų šablonai, kurie yra saugomi visuotinėje saugykloje, bet kurių trūksta dabartiniame finansų egzemplioriuje. Pasirinkus šabloną, jis importuojamas iš visuotinės saugyklos į dabartinį finansų egzempliorių, kad būtų sukurta nauja redaguojama kopija. Redaguotas šablonas saugomas naujoje ER formato konfigūracijoje, kuri generuojama automatiškai.

1. Darbo srityje **Verslo dokumentų valdymas** pasirinkite **Naujas dokumentas**.
2. Ant **Sukurkite naują šabloną** puslapyje, esančiame **Importuoti iš pasaulinės saugyklos** skirtuke pasirinkite dokumentą, kurį norite naudoti kaip šabloną, tada pasirinkite **Sukurti dokumentą**.

    ![Importuoti iš pasaulinės saugyklos skirtuko puslapyje Sukurti naują šabloną.](./media/BDM_overview_new_template22.png)

3. Pranešimo laukelyje pasirinkite **Taip** patvirtinti, kad norite importuoti pasirinktą dokumentą iš visuotinės saugyklos į dabartinį finansų egzempliorių. Jei būsite paraginti suteikti įgaliojimą, vykdykite ekrane pateikiamas instrukcijas.
4. Naujo dialogo lango lauke **Pavadinimas** pakeiskite pavadinimą į norimą pavadinimą. Pavadinimo tekstas naudojamas automatiškai sukurtai naujai ER formato konfigūracijai pavadinti. Šios konfigūracijos juodraštis (**Surinkimo laiško raštelis (Excel) Kopija**) bus redaguotas šablonas ir bus naudojamas paleisti šį ER formatą dabartiniam vartotojui. Originalus šablonas iš pagrindinio ER formato konfigūracijos bus naudojamas visiems kitiems vartotojams skirtam ER formatui vykdyti.
5. Lauke **Pavadinimas** pakeiskite redaguojamo šablono, kuris bus automatiškai sukurtas, pirmo pataisymo pavadinimą.
6. Lauke **Komentaras** atnaujinkite redaguojamo šablono, kuris bus automatiškai sukurtas, pataisymo pastabas.
7. Pasirinkite **Gerai**, kad patvirtintumėte redagavimo proceso pradžią.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
