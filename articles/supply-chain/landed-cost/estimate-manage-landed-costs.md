---
title: Iškrovimo kainų vertinimas ir valdymas
description: Sistema naudoja jūsų automatinės savikainos sąranką, kad nustatytų jūsų iškrovimo kainą. Šioje temoje paaiškinama, kaip galima nurodyti įvairius scenarijus, siekiant pateikti tikslesnį įvertinimą.
author: Weijiesa
ms.date: 01/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostTemplateTable, ITM CostEstimateDialog, ITMCostEstimateTable, SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-26
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 630fb9dc8e7954fcbc4f54941d81de1caa657676
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8696213"
---
# <a name="estimate-and-manage-landed-costs"></a>Iškrovimo kainų vertinimas ir valdymas

[!include [banner](../../includes/banner.md)]

Sistema naudoja jūsų [automatinį savikainos nustatymą](auto-cost-setup.md), kad apibrėžtų jūsų iškrovimo kainos vertinimą. Be to, taip pat galite nurodyti įvairius scenarijus, siekiant pateikti tikslesnį įvertinimą. Šie scenarijai saugomi. Todėl juos galėsite peržiūrėti vėliau ir palyginti su faktiniais, pateikiamais ataskaitoje. Taip pat galima atnaujinti prekės kainą.

## <a name="set-up-cost-estimates"></a>Savikainos vertinimų nustatymas

### <a name="set-up-cost-templates"></a>Nustatyti išlaidų šablonus

Savikainos šablonai nustato numatytuosius parametrus, kurių vertinimus gaunantys naudotojai gali nežinoti. Šablonai gali padėti sumažinti įvertinimo proceso sudėtingumą sumažinant naudotojų nurodomus pasirinkimus tiksliam įvertinimui gauti. Jei naudojate standartinį savikainos modelį, kai nustatote prekių savikainą, galite naudoti savikainos šablonus.

Kad gautumėte savikainos šablonus, pereikite į **Iškrovimo savikaina \> Įkainojimo nustatymas \> Savikainos šablonai**. Puslapio **Savikainos šablonai** kairėje esančioje sąrašo srityje rodomi visi dabartiniai savikainos šablonai. Veiksmų srityje esančius mygtukus galima naudoti šablonams kurti, trinti ir redaguoti.

Šioje lentelėje apibūdinami galimi kiekvieno šablono laukeliai.

| Laukas | aprašymas |
|---|---|
| Išlaidų šablonas | Įveskite unikalų savikainos šablono pavadinimą. Pavadinimas paprastai aprašo šablono koeficientą arba savikainos daugiklį. |
| aprašymas | Įveskite savikainos šablono aprašymą. |
| Gabenimo įmonė | Pasirinkite siuntimo įmonę, kurią reikėtų taikyti naudojant šabloną. |
| Pristatymo būdas | Pasirinkite pristatymo būdą, pvz., jūra arba oru, kuris turėtų būti taikomas, kai naudojamas šablonas. Šis laukelis padeda apibrėžti automatinę savikaina, siejamą su prekėmis savikainos vertinime. |
| Gabenimo konteinerio tipas | Pasirinkite siuntimo konteinerio tipą, kurį reikėtų taikyti naudojant šabloną. Šis laukelis padeda apibrėžti automatinę savikaina, siejamą su prekėmis savikainos vertinime. |
| Muitinės tarpininkas | Muitinės tarpininkas (tiekėjas), kurį reikėtų taikyti naudojant šabloną. Šis laukelis padeda apibrėžti automatinę savikaina, siejamą su savikainos vertinimu. |
| Koeficientas | Įveskite daugiklį (procentus), kuris turi būti automatiškai taikomas vertinant savikainą, kai naudojamas šablonas. Pavyzdžiui, norėdami prie apskaičiuotos įvertintos savikainos pridėti 10 procentų, įveskite *1,10*. |

### <a name="create-a-cost-estimate"></a>Savikainos vertinimo kūrimas

Naudodami dialogo langą **Savikainos vertinimas** generuokite naują savikainos vertinimą, kuris grindžiamas pasirinktu savikainos šablonu bei pasirinktu prekių rinkiniu bei kitais veiklos ciklo duomenimis. Tada nustatymai naudojami norint nustatyti numatomas prekių iškrovimo kainas. Šie išlaidų vertinimai pirmiausia naudojami dirbant su standartinės savikainos elementais. Įvertintas iškrovimo kainas sudėjus su standartine atsargų prekių savikaina, operacijų nuokrypis turėtų būti mažesnis, kai prekės pridedamos reisui, nes standartinė savikaina atspindės tokių iškrovimo kainų vertinimus.

Kad atidarytumėte dialogo langą **Savikainos vertinimas**, eikite į **Iškrovimo kaina \> Periodinės užduotys \> Savikainos vertinimas**. Tada nustatykite laukelius, kurie aprašomi tolesniuose papildomuose skyriuose. Galiausiai pasirinkite **Gerai** ir sukurkite vertinimą. Tada pasirodo puslapis **Savikainos vertinimas** (**Iškrovimo kaina \> Užklausos \> Savikainos vertinimas**) ir jame rodomas naujasis vertinimas, kaip aprašoma toliau šioje temoje.

### <a name="settings-on-the-parameters-tab"></a>Nustatymai parametrų skirtuke

Šioje lentelėje aprašomi laukeliai, esantys skirtuke **Parametrai**, dialogo lange **Savikainos vertinimas**.


| Laukas | aprašymas |
|---|---|
| Išlaidų šablonas | Pasirinkite savikainos šabloną. Su pasirinktu šablonu siejami nustatymai bus naudojami taikomai automatinei savikainai nustatyti. |
| Įvertinti datą | Numatyta, kad šiame laukelyje nustatoma šios dienos data, tačiau vertę galima keisti. Nurodyta data bus naudojama atitinkamoms pardavimo kainoms, pirkimo kainoms, automatinei savikainai ir valiutų kursui pasirinkti, jei naudojamas siuntimo tarifas. |
| Matas | Savikaina gali priklausyti nuo matavimo vieneto. Pvz., jei naudojamas oro transportas, gali būti taikomas tūrinis įkainojimas. Jei savikaina priklauso nuo matavimo vieneto, įveskite to matavimo vieneto vertę. Priešingu atveju rekomenduojame šį laukelį nustatyti kaip *1*, jei naudojant matavimo vienetą neatliekama jokia paslauga. Įveskite dešimtainę reikšmę. Vienetas yra apibrėžiamas atitinkamame automatinės savikainos įraše. |
| Kelionės šablonas | Pasirinkite [veiklos ciklo šabloną](multi-leg-journey-setup.md). Šis laukelis naudojamas teisingam automatinės savikainos, kurią reikėtų taikyti, nustatyti. |
| Kilmės uostas | Uostas, iš kurio bus siunčiamos prekės. Šis laukelis nustatomas pagal pasirinktą veiklos ciklo šabloną. |
| Paskirties uostas | Uostas, į kurį bus siunčiamos prekės. Šis laukelis nustatomas pagal pasirinktą veiklos ciklo šabloną. |
| Valiuta | Pasirinkite valiutą, kuria bus perkamos prekės. |
| Konteineriai | Jei paprastai naudojami keli konteineriai, nurodykite konteinerių skaičių. Įvertinusi savikainą, sistema naudos kelių konteinerių savikainas. |
| Sąskaitos lapai | Jei paprastai naudojami keli lapai, nurodykite kiekį. (Kiekis paprastai yra *1*.) |
| Vieta | Nurodykite vietą, kurioje bus pristatomos prekės. |

### <a name="settings-on-the-items-tab"></a>Nustatymai prekių skirtuke

Skirtuke **Prekės** galite pridėti tiek vertinimo prekių, kiek jums reikia. Naudodami įrankių juostą prie tinklelio pridėkite prekių arba jas pašalinkite. Įrankių juostoje pasirinkite **Atsargos \> Rodyti dimensijas**, kad atidarytumėte dialogo langą, kuriame prie tinklelio galėsite pridėti dimensijų stulpelius arba juos pašalinti.

Šioje lentelėje apibūdinami galimi kiekvienos prekės laukeliai.

| Laukas | aprašymas |
|---|---|
| Prekės numeris | Pasirinkite prekę, kurios kainą norite nustatyti. (Jei prekės sistemoje dar nėra, sukurkite fiktyvią prekę, pasirinktinai ją pridėkite prie reiso prekių išlaidų grupės, o tada kainą palikite tuščią arba ją sukurkite arba pakeiskite). |
| Tiekėjo kodas | Pasirinkite tiekėją, kuris bus naudojamas šios prekės vertinimui. Jei prekei priskirtas numatytasis tiekėjas, šis laukelis nustatomas automatiškai. |
| Kiekis | Pasirinkite kiekį, kurį pirksite. |
| Savikaina | Pradinei kainai rasti sistema naudoja įkainojimo taisykles, tačiau prireikus tos kainos galima nepaisyti. |
| Pardavimo kaina | Įveskite numatomą prekių pardavimo kainą. |
| Matas | Įveskite prekių matavimo vieneto dešimtainę vertę. Vienetas nustatomas taikomam išleistam produktui. |
| Atnaujinti prekės svorį/tūrį | Pažymėkite šį žymės langelį, jei norite atnaujinti išleisto produkto svorio ar tūrio matavimo vienetą, kad jis sutaptų tai eilutei įvesta verte **Matavimas**. |
| (Kitos dimensijos) | Atsižvelgiant į dimensijas, kurias pasirinkote rodyti, galite matyti papildomus kiekvienos prekės informacijos stulpelius. |

Norėdami peržiūrėti arba koreguoti prekės tūrio ir (arba) svorio informaciją, tinklelyje pasirinkite prekę ir tada naudokite puslapio apačioje esančius laukelius.

## <a name="manage-estimated-costs"></a>Įvertintos savikainos valdymas

Norėdami peržiūrėti ir redaguoti sukurtus savikainos vertinimus, eikite į **Iškrovimo kaina \> Užklausos \> Savikainos vertinimas**. Puslapio **Savikainos vertinimas** kairėje esančioje sąrašo srityje rodomi visi dabartiniai savikainos šablonai. Veiksmų srities mygtukus galite naudoti norėdami dirbti su pasirinktu vertinimu. Atminkite, kad puslapyje **Savikainos vertinimas** negalėsite kurti naujo savikainos vertinimo. Geriau naudokite dialogo langą **Savikainos vertinimas** (**Iškrovimo kaina \> Periodinės užduotys \> Savikainos vertinimas**), kaip aprašyta šioje temoje aukščiau.

Puslapyje **Savikainos vertinimas** rodoma, kaip išvedama kiekviena įvertinta savikaina. Jame taip pat rodoma kiekvienos prekės įvertinta iškrovimo savikaina. Savikainos vertinimą galima modifikuoti keičiant savikainos kainą ir (arba) valiutą, kuri siejama su įvairiomis prekėmis. Taip pat galima modifikuoti susijusias reiso išlaidas ir reiso lygyje, ir konteinerio lygyje. Kai naudojate šį puslapį išlaidoms modifikuoti, esate raginami perskaičiuoti įvertintas prekių, esančių savikainos įvertinime, savikainas. Kai būsite pasirengę, vertinimus galite naudoti prekių savikainos kainai atnaujinti savikainos šablone.

### <a name="information-on-the-header"></a>Informacija antraštėje

Puslapio **Savikainos vertinimas** viršuje rodomi nustatymai, kurie buvo naudojami pasirinktos savikainos vertinimui generuoti, kaip aprašyta ankstesniame skyriuje. 

### <a name="settings-and-buttons-on-the-lines-fasttab"></a>Nustatymai ir mygtukai, esantys eilučių „FastTab” skirtuke

„FastTab“ skirtuke **Eilutės** nurodoma kiekviena prekė, kuri yra įtraukta į dabartinį vertinimą. Šioje lentelėje apibūdinami galimas kiekvienos prekės laukelis.

| Laukas | aprašymas |
|---|---|
| Tiekėjo kodas | Su preke susijusi tiekėjo paskyra. |
| Prekės numeris | Prekės numeris. |
| Kiekis | Prekių, naudojamų savikainai nustatyti, skaičius. |
| Savikaina | Savikainos kaina pagal prekybos sutartį. Ši vertė rodoma vietos valiuta. |
| Matas | Atskiras matavimo vienetas. Vienetas apibrėžiamas taikomam išleistam produktui. |
| Įvertintos pristatymo išlaidos | Viso kiekio įvertinta iškrovimo kaina. |
| Vienetui | Iš kiekio padalinta įvertinta iškrovimo kaina. |
| (Kitos dimensijos) | Atsižvelgiant į dimensijas, kurias pasirinkote rodyti, galite matyti papildomus kiekvienos prekės informacijos stulpelius. |

Šioje lentelėje aprašomi mygtukai, esantys „FastTab“ skirtuko **Eilutės** įrankių juostoje.

| Mygtukas | aprašymas |
|---|---|
| Pridėti | Pridėkite prekes prie savikainos vertinimo. Pridėję prekių veiksmų srityje turite pasirinkti **Perskaičiuoti**. |
| Šalinti | Iš savikainos vertinimo pašalinkite prekes. Pašalinę prekes veiksmų srityje turite pasirinkti **Perskaičiuoti**. |
| Reiso išlaidos | Atidarykite puslapį, kuriame galima peržiūrėti ir redaguoti įvairių tipų prekės reiso savikainas. |
| Atsargos \> Rodyti dimensijas | Atidarykite dialogo langą, kuriame galima dimensijos stulpelius galima pridėti prie tinklelio arba pašalinti stulpelius. |

### <a name="settings-on-the-general-fasttab"></a>Parametrai, esantys Bendra „FastTab”

„FastTab“ skirtuke **Bendra** rodoma prekės, kuri šiuo metu pažymėta „FastTab“ skirtuke **Eilutės**, informacija. Daug šios informacijos yra kartojama „FastTab“ skirtuke **Eilutės** ir ją galima redaguoti bet kurioje vietoje. Tačiau čia taip pat galima gauti papildomos informacijos. Papildomų laukelių vertės grindžiamos taikomo išleisto produkto nustatymu.

### <a name="settings-on-the-dimension-fasttab"></a>Parametrai, esantys matmenų „FastTab” skirtuke

„FastTab“ skirtuke **Dimensija** rodomos visų turimų atsargų dimensijų vertės prekei, kuri yra pasirinkta „FastTab“ skirtuke **Eilutės**, nepriklausomai nuo dimensijų, kurias pasirinkote rodyti čia. Visos vertės, kurios rodomos čia, gaunamos iš taikomos savikainos vertinimo šablono. Jos yra laisvai pasirenkamos savikainos vertinimo šablone.

### <a name="buttons-on-the-action-pane"></a>Veiksmų srities mygtukai

Puslapio **Savikainos vertinimas** veiksmų srityje galite naudoti mygtukus, dirbdami su pasirinktu savikainos vertinimu. Šioje lentelėje aprašomi galimi mygtukai.

| Operacija | aprašymas |
|---|---|
| Savikainos užklausa | Peržiūrėkite visas reiso savikainas. Prireikus galite peržiūrėti kiekvienos prekės savikainą. |
| Atnaujinti standartines išlaidas | <p>Standartinę savikainą atnaujinkite naudodami numatytąją įkainojimo versiją, kuri apibrėžiama puslapyje **Iškrovimo kainos parametrai**. Šios versijos galima nepaisyti.</p><p>**Pastaba.** Jei prekėje yra kelios prekės dimensijos (pvz., keli dydžiai, spalvos ir konfigūracijos), tačiau šios dimensijos nebuvo pasirinktos vertinimui, sistema kiekvienam deriniui sukurs laukiančią kainą.</p><p>**Svarbu.** Sukuriamas kainos paskirstymas ir naudojamas iškrovimo kainos standartinės savikainos nuokrypiui nustatyti.</p> |
| Reiso išlaidos | Peržiūrėkite ir redaguokite visų siuntos prekių reiso savikainas. |
| Perskaičiuoti | Įvertintas iškrovimo kainas atnaujinkite po to, kai atnaujinsite, pridėsite arba pašalinsite reiso savikainas. |
| Blokuoti | Užrakinkite savikainos vertinimo įrašą, kad nebebūtų galima daryti pakeitimų. |

## <a name="item-cost-price-update"></a>Prekės išlaidų kainos atnaujinimas

**Prekės savikainos kainos naujinimas** atnaujina visus periodinės užduoties savikainos vertinimus, kurie sutampa su filtrais, nustatomais paleidus užduotį. Poveikis panašus į poveikį, kai vienam vertinimui veiksmų srityje pasirenkama funkcija **Atnaujinti standartinę savikainą**. Tačiau šiuo atveju atnaujinimas taikomas visiems atitinkantiems vertinimams.

Kad paleistumėte periodinę užduotį, atlikite nurodytus veiksmus.

1. Eikite į **Iškrovimo kaina \> Periodinės užduotys \> Prekės savikainos kainos naujinimas**.
1. Dialogo lange **Atnaujinti savikainos kainą pagal vertinimą** atitinkamai nustatykite šiuos laukelius, kad apribotumėte atnaujinimo aprėptį:

    - **Versija** – atnaujinkite tik tuos vertinimus, kurie naudoja nurodytą įkainojimo versiją.
    - **Svetainė** – atnaujinkite tik tuos vertinimus, kurie naudoja nurodytą svetainę.
    - **Savikainos šablonas** – atnaujinkite tik tuos vertinimus, kurie naudoja nurodytą šabloną.
    - **Atvykimo uostas** – atnaujinkite tik tuos vertinimus, kurie naudoja nurodytą atvykimo uostą.
    - **Vertinimo data** – atnaujinkite tik vertinimus su nurodyta data.

1. Nustatykite parinktis „FastTab“ skirtuke **Įtraukiami įrašai** ir **Paleisti fone**, kaip atliekama su periodinėmis užduotimis.
1. Norėdami paleisti užduotį, pasirinkite **Gerai**.

> [!NOTE]
> Ši periodinė užduotis sėkmingai bus vykdoma tik tada, kai bus prieinama ši informacija:
>
> - Kiekvienam atitinkamam produktui reikia nustatyti šiuos parametrus: **Bendrą gylį**, **Bendrą plotį** ir **Bendrą aukštį**.
> - Kiekvienas atitinkamas tiekėjas turi apibrėžti **Išvykimo uostą**.
