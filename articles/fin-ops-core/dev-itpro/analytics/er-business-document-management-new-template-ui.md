---
title: Microsoft Office-stiliaus vartotojo sąsaja verslo dokumentų valdymas (yra vaizdo įrašas)
description: Šiame straipsnyje paaiškinama, kaip naudoti naują vartotojo sąsają elektroninių ataskaitų (ER) sistemos verslo dokumentų valdymo priemonėje.
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
ms.openlocfilehash: 208cfc91f11d4893785538ce4874e85a5725e993
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109267"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>„Microsoft Office” stiliaus vartotojo sąsaja Verslo dokumentų valdyme

[!include [banner](../includes/banner.md)]

Verslo dokumentų valdymas leidžia verslo vartotojams redaguoti verslo dokumentų šablonus naudojant „Microsoft Office 365“ paslaugą arba atitinkamą „Microsoft Office“ darbalaukio programą. Redagavimas gali būti dizaino keitimai arba nauji diegimai arba vartotojai gali įtraukti vietos rezervavimo ženklų, kad galėtų įtraukti papildomų duomenų, nekeisdami šaltinio kodo. Norėdami gauti daugiau informacijos apie tai, kaip naudotis funkcija Verslo dokumentų valdymas, žr. [Funkcijos Verslo dokumentų valdymas apžvalga](er-business-document-management.md).

Naujo vartotojo sąsaja (UI) yra aiškesnė ir patogesnė naudoti. Verslo **dokumentų sritis** rodo tik šablonus, [...](tasks/er-configuration-provider-mark-it-active-2016-11.md)[kurie](general-electronic-reporting.md#Provider) priklauso dabartiniam aktyviam tiekėjui ir yra dabartiniame "Dynamics 365 Finance" egzemplioriuje. Ankstesniame vartotojo sąsajose skirtuke **Šablonas** išvardyti visi šablonai, galimi bet kuriam tiekėjui. Taip pat joje buvo rodomi visi šablonai, kuriuos sukūrė ir redagavo bet kuris vartotojas, turintis tokį patį vaidmenį.

**·** **·**[Galite naudoti verslo dokumentų valdymo darbo srityje esantį dokumento mygtuką, kad kurtumėte ir redaguotumėte šabloną elektroninės ataskaitos (ER)](general-electronic-reporting.md) formato [konfigūracijoje](general-electronic-reporting.md#Configuration), kurią teikia kitas teikėjas ir kuris yra dabartiniame finansų egzemplioriuje, arba norėdami įkelti naują šabloną iš Excel darbaknygės. Be to, 10.0.25 ir vėlesnės versijos metu galite naudoti mygtuką Naujas dokumentas, norėdami sukurti ir redaguoti šabloną ER formato konfigūracija, **kuri** saugoma visuotinėje saugykloje [.](general-electronic-reporting.md#Repository)

Šiame straipsnyje pateiktiuose pavyzdžiuose aktyvus tiekėjas yra "Contoso", o jūs naudojate jį norėdami sukurti šabloną, pagrįstą šablonu, kurį teikia "Microsoft". Taip pat galite sukurti šabloną įkeldami savo šabloną „Excel” formatu.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWAVQg]

Naujas [verslo dokumentas sukurtas naudojant verslo dokumentų valdymo vaizdo įrašą](https://youtu.be/gAIYl-mM_pw) (parodyta aukščiau) yra įtrauktas [į finansų ir operacijų sąrašą](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), kuris pasiekiamas YouTube.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Naujo dokumento vartotojo sąsajos įjungimas funkcijoje Verslo dokumentų valdymas

Norėdami pradėti naudoti naujo dokumento vartotojo sąsają funkcijoje Verslo dokumentų valdymas, turite įjungti funkciją **Į „Office“ panaši vartotojo sąsaja funkcijoje Verslo dokumentų valdymas** darbo srityje **Funkcijų valdymas**.

Atlikite tolesnius veiksmus, norėdami įjungti šią funkciją visiems juridiniams subjektams.

1. Iš darbo srities **Funkcijų valdymas** skirtuko **Visi** sąrašo pasirinkite funkciją **Į „Office“ panaši vartotojo sąsajos patirtis Verslo dokumentų valdymui**.
2. Pasirinkite **Įjungti dabar**, kad įjungtumėte pasirinktą funkciją.
3. Norėdami pasiekti naują funkciją, atnaujinkite puslapį.

## <a name="add-or-activate-a-provider"></a>Įtraukti arba aktyvinti teikėją

Kiekvienas verslo dokumento šablonas saugomas ER formato konfigūracijoje, kuri pažymėta kaip priklauso konkrečiam konfigūracijos tiekėjui. Kuriant naują šabloną sukuriama nauja ER formato konfigūracija, pagal kurią jis bus sulaikytas. Todėl reikia nustatyti tos konfigūracijos teikėją. Šiuo tikslu naudojamas aktyvus ER sistemos teikėjas. Jei ER teikėjo nėra, jį galite sukurti. Jei nėra aktyvaus *teikėjo*, galite suaktyvinti vieną iš esamų teikėjų. Kai reikia, o jūs pradedate pridėti naują šabloną, atidaromas teikėjo pridėjimo arba aktyvinimo dialogo langas.

### <a name="add-a-new-provider"></a>Įtraukti naują teikėją

Norėdami sukurti naują teikėją, konfigūracijos teikėjo dialogo lange **atlikite šiuos** veiksmus:

1.  **Skirtuko Pasirinkti konfigūracijos** teikėją lauke **Pavadinimas** įveskite naujo teikėjo pavadinimą.
2.  **Interneto adreso** lauke įveskite naujo teikėjo interneto adresą (URL). 
3.  Pasirinkite **Gerai**.

    ![Verslo dokumentų valdymo teikėjas kuriamas.](./media/bdm_create_provider.png)

Įtrauktas teikėjas bus suaktyvintas automatiškai.

### <a name="activate-a-provider"></a>Teikėjo aktyvinimas

Norėdami aktyvinti teikėją, konfigūracijos teikėjo dialogo lange **atlikite šiuos** veiksmus:

1.  Skirtuko Pasirinkti **konfigūracijos teikėją** lauke Konfigūracijos **teikėjas** pasirinkite teikėją.
2.  Pasirinkite **Gerai**.

    ![Verslo dokumentų valdymo teikėjo suaktyvinimas.](./media/bdm_choose_provider.png)

Pasirinktas teikėjas bus suaktyvintas.

> [!NOTE]
> Kiekvienas verslo dokumentų valdymo šablonas yra ER formato konfigūracijoje, kuri nurodo tiekėją kaip konfigūracijos autorių. Todėl kiekvienam šablonui reikia aktyvaus teikėjo.

## <a name="edit-a-template-that-is-owned-by-another-provider"></a>Redaguoti šabloną, priklauso kitam tiekėjui

Šis pavyzdys **rodo** **·**, kaip naudoti mygtuką Naujas dokumento verslo dokumentų valdymo darbo srityje, norint sukurti ir redaguoti šabloną ER formato konfigūracija, kurią teikia kitas teikėjas ir kuris yra dabartiniame finansų egzemplioriuje. Šiame pavyzdyje aktyvus tiekėjas yra "Contoso", kuris naudoja "Microsoft" teikia ER formato konfigūraciją. Kai pasirenkate **naują** dokumentą, skirtuko Pasirinkti puslapyje Kurti naują šabloną rodomi visi dabartinio finansų egzemplioriaus šablonai, **·** **priklauso** dabartiniam tiekėjui ir kitiems teikėjai. Pasirinkite šabloną, kurį jį atidarysite. Tada galėsite kurti naują redaguojamą šablono kopiją. Redaguotas šablonas saugomas naujoje ER formato konfigūracijoje, kuri sugeneruojama automatiškai.

1. Darbo srityje **Verslo dokumentų valdymas** pasirinkite **Naujas dokumentas**.

    ![Darbo sritis Verslo dokumentų valdymas.](./media/BDM_overview_new_template1.png)

2. Skirtuko Pasirinkti **puslapyje Kurti** **naują** šabloną pasirinkite dokumentą, kurį norite naudoti kaip šabloną, tada pasirinkite Kurti **dokumentą.**

    ![Verslo dokumentų dialogo langas.](./media/BDM_overview_new_template2.png)

3. Naujo dialogo lango lauke **Pavadinimas** pakeiskite pavadinimą į norimą pavadinimą. Pavadinimo tekstas naudojamas automatiškai sukurtai naujai ER formato konfigūracijai pavadinti. Šios konfigūracijos (**Kliento laisvos formos sąskaitos-faktūros ataskaitos (GER) kopija**) juodraščio versijoje bus suredaguotas šablonas ir ji bus naudojama vykdant šį ER formatą, skirtą dabartiniam vartotojui. Originalus šablonas iš pagrindinio ER formato konfigūracijos bus naudojamas visiems kitiems vartotojams skirtam ER formatui vykdyti.
4. Lauke **Pavadinimas** pakeiskite redaguojamo šablono, kuris bus automatiškai sukurtas, pirmo pataisymo pavadinimą.
5. Lauke **Komentaras** atnaujinkite redaguojamo šablono, kuris bus automatiškai sukurtas, pataisymo pastabas.
6. Pasirinkite **Gerai**, kad patvirtintumėte redagavimo proceso pradžią.

    ![Dokumento kūrimo dialogo langas.](./media/BDM_overview_new_template3.png)

## <a name="upload-a-template-that-uses-an-existing-excel-workbook"></a>Nusiųsti šabloną, kuris naudoja esamą "Excel" darbaknygę

Šis pavyzdys rodo, **·** **kaip** naudoti mygtuką Naujas dokumento verslo dokumentų valdymo darbo srityje, norint sukurti ir redaguoti šabloną ER formato konfigūracija, remiantis galima Excel darbaknyge. Šiame pavyzdyje aktyvus teikėjas yra "Contoso", o jūs naudojate "Microsoft" pateikiamas ER [duomenų](er-overview-components.md#data-model-component) modelio ir ER [modelio](er-overview-components.md#model-mapping-component) susiejimo konfigūracijas. Kai pasirenkate **naują dokumentą**, pasirinkite skirtuką **Įkelti**, kurį rasite **puslapyje Kurti naują šabloną**. Ten galite nurodyti "Excel" darbaknygės nusiuntimo informaciją. Įkėlus Excel darbaknygę, ji transformuojama į redaguoti atidarytą verslo dokumento šabloną. Redaguotas šablonas bus saugomas naujoje ER formato konfigūracijoje, kuri sukuriama automatiškai.

Norėdami pateikti reikiamą informaciją prieš šablono įkėlimą, atlikite šiuos veiksmus.

1. Darbo srityje **Verslo dokumentų valdymas** pasirinkite **Naujas dokumentas**.
2. Puslapio **Kurti naują šabloną** skirtuko **Įkelti** skirtuke **Šablonas** pasirinkite **Naršyti**, kad surastumėte ir pasirinktumėte „Excel” failą, kurį norite naudoti kaip šabloną. Skyriaus **Šablono** laukai **Pavadinimas** ir **Aprašas** yra užpildomi automatiškai. Jie nurodo naujos, automatiškai kuriamos, ER formato konfigūracijos pavadinimą ir aprašą. Prireikus galite redaguoti šiuos laukus.
3. Skyriaus **Dokumento tipas** lauke **Pavadinimas** nurodykite verslo dokumento tipą. Ši reikšmė bus naudojama ieškoti tinkamam duomenų šaltiniui (tai yra, ER modelio konfigūracijai).

    ![Šablono skirtukas, esantis skirtuko Kurti naują šabloną puslapyje skirtuke Siuntimas.](./media/BDM_overview_new_UI_import_21.jpg)

4. Skirtuko **Duomenų šaltinis** „FastTab” **Filtras** pasirinkite **Taikyti filtrą**. Skyriaus **Duomenų šaltinio** laukas **Pavadinimas** yra užpildomas automatiškai arba galite jo reikšmę pasirinkti rankiniu būdu. Galite naudoti filtrą atitinkamam duomenų šaltinio vardui ieškoti pagal vardą, aprašą, šalies/regiono kodą ir verslo dokumento tipą.

    ![Duomenų šaltinio skirtukas nusiuntimo skirtuke, kuris yra puslapio Kurti naują šabloną.](./media/BDM_overview_new_UI_import_31.jpg)

    > [!NOTE]
    > „FastTab” **Filtruoti** yra naudojamas ieškoti tinkamam duomenų šaltiniui (tai yra, ER modelio konfigūracijai). Galite redaguoti visus filtro laukus, kad rastumėte tinkamiausią duomenų šaltinį įkeliamam dokumentui.
    > 
    > „FastTab” **Filtruoti** esančios sąlygos yra naudojamos kaip **ARBA** sąlygos.

5. Skirtuke **Susiejimas** pasirinkite **Automatiškai aptikti**. Laukas **Šakninis aprašas** yra užpildomas automatiškai arba galite jo reikšmę pasirinkti rankiniu būdu. Šiame skirtuke rodomas galutinis šablono ir modelio elementų susiejimas.

    ![Susiejimo skirtukas, esantis naujo šablono puslapio kūrimo skirtuke Siuntimas.](./media/BDM_overview_new_UI_import_41.jpg)

    > [!NOTE]
    > Susiejimas skyriuje **Šablono struktūra** naudoja duomenų šaltinio žymų arba aprašų vartotojo kalba, esančių langelio pavadinime šablone, visišką atitiktį.

6. Pasirinkite **Kurti dokumentą**, kad patvirtintumėte, jog norite sukurti šabloną ir pradėti redagavimo procesą.

Daugiau informacijos žr. [Verslo dokumentų valdymo apžvalga](er-business-document-management.md).

## <a name="upload-a-template-from-the-global-repository"></a>Įkelti šabloną iš visuotinės saugyklos

Šis pavyzdys **rodo** **·**, kaip naudoti mygtuką Naujas dokumento verslo dokumentų valdymo darbo srityje, norint sukurti ir redaguoti šabloną ER formato konfigūracija, kurią teikia Microsoft ir yra visuotinoje saugykloje. Šiame pavyzdyje aktyvus tiekėjas yra "Contoso", kuris naudoja "Microsoft" teikia ER formato konfigūraciją. Kai pasirenkate **Naują** dokumentą, skirtuko Importuoti iš visuotinės saugyklos puslapyje Kurti naują šabloną rodomi visi verslo dokumentų šablonai, saugomi visuotiniame saugykloje, **·** **tačiau** nėra dabartiniame finansų egzemplioriuje. Kai pasirenkate šabloną, jis importuojamas iš visuotinės saugyklos į dabartinį finansų egzempliorių, kad būtų sukurta nauja redaguojama kopija. Redaguotas šablonas saugomas naujoje ER formato konfigūracijoje, kuri sugeneruojama automatiškai.

1. Darbo srityje **Verslo dokumentų valdymas** pasirinkite **Naujas dokumentas**.
2. Skirtuko Importuoti **iš visuotinės** saugyklos **puslapyje Kurti naują šabloną** pasirinkite dokumentą, kurį norite naudoti kaip šabloną, tada pasirinkite **Kurti dokumentą**.

    ![Importuoti iš skirtuko Visuotinis saugyklos šablonas, kuris yra Puslapio Šablono kūrimas.](./media/BDM_overview_new_template22.png)

3. Pranešimų lauke pasirinkite Taip, jei **norite** patvirtinti, kad norite importuoti pasirinktą dokumentą iš visuotinės saugyklos į dabartinį finansų egzempliorių. Jei būsite paraginti autorizuoti, laikykitės ekrane pateikiamų instrukcijų.
4. Naujo dialogo lango lauke **Pavadinimas** pakeiskite pavadinimą į norimą pavadinimą. Pavadinimo tekstas naudojamas automatiškai sukurtai naujai ER formato konfigūracijai pavadinti. Šios konfigūracijos juodraščio versijoje (**priminimo laiško pastabos (Excel) kopija)** bus redaguotas šablonas ir jis bus naudojamas šiam vartotojui paleisti šį ER formatą. Originalus šablonas iš pagrindinio ER formato konfigūracijos bus naudojamas visiems kitiems vartotojams skirtam ER formatui vykdyti.
5. Lauke **Pavadinimas** pakeiskite redaguojamo šablono, kuris bus automatiškai sukurtas, pirmo pataisymo pavadinimą.
6. Lauke **Komentaras** atnaujinkite redaguojamo šablono, kuris bus automatiškai sukurtas, pataisymo pastabas.
7. Pasirinkite **Gerai**, kad patvirtintumėte redagavimo proceso pradžią.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

