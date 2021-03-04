---
title: Pasirinktinių laukų kūrimas ir naudojimas
description: Šioje temoje parodoma, kaip vartotojo sąsajoje kurti pasirinktinius laukus ir programą pritaikyti savo verslui.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 5f74397bcdd59a1fe24f5b6046081cbd2bed461b
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693550"
---
# <a name="create-and-work-with-custom-fields"></a>Pasirinktinių laukų kūrimas ir naudojimas

[!include [banner](../includes/banner.md)]

Nors yra platus parengtų naudoti laukų rinkinys, skirtas valdyti įvairius verslo procesus, kartais įmonei sistemoje reikia sekti papildomą informaciją. Nors programuotojai gali įtraukti šiuos laukus kaip plėtinius į programavimo įrankius, pasirinktinių laukų funkcija leidžia įtraukti laukus tiesiai iš vartotojo sąsajos, todėl galite pritaikyti programą prie savo įmonės per žiniatinklio naršyklę.

Galimybė pridėti pasirinktinius laukus pasiekiama 13-ame ir vėlesniuose platformos naujinimuose. Tik vartotojai, turintis specialias teises, turi prieigą prie šios funkcijos.

Šiame vaizdo įraše rodoma, kaip lengva į puslapį įtraukti pasirinktinį lauką: [Pasirinktinių laukų įtraukimas](https://www.youtube.com/watch?v=gWSGZI9Vtnc).

## <a name="creating-custom-fields"></a>Pasirinktinių laukų kūrimas

Nustatę papildomą informaciją, kurią norėtumėte sekti programoje, atitinkamoje lentelėje galite sukurti pasirinktinį lauką ir jį rodyti puslapyje.

Tolesniais veiksmais aprašomas pasirinktinio lauko kūrimo ir įtraukimo į formą procesas.

1. Pereikite į formą, kurioje reikia naujo lauko.
2. Kadangi galutinis tikslas yra pasirinktinį lauką rodyti formoje, pasirinktinių laukų kūrimo įvesties taškas yra personalizavimo srityje. Atidarykite personalizavimo įrankių juostą pasirinkdami **Parinktys**, tada – **Personalizuoti šią formą**.
3. Spustelėkite **Įterpti**, tada – **Laukas**.
4. Pasirinkite formos sritį, kurioje norite rodyti naująjį lauką. Ją pasirinkus, dialogo lange **Įterpti laukų** bus rodomas esamų laukų, kuriuos galima įtraukti į pasirinktą formos sritį, sąrašas.
5. Įsitikinkite, kad jus dominančio lauko sąraše dar nėra. Jei jis yra, galite tiesiog pasirinkti tą lauką sąraše ir spustelėti **Įterpti**.
6. Spustelėkite virš sąrašo esantį mygtuką **Kurti naują lauką**, kad pradėtumėte pasirinktinio lauko kūrimo procesą. Taip atidarysite dialogo langą **Kurti naują lauką**.

    Jei mygtuko **Kurti naują lauką** nematote, neturite reikiamų teisių naudoti šią funkciją.

7. Dialogo lange **Kurti naują lauką** įveskite tolesnę informaciją.

    1. Pasirinkite duomenų bazės lentelę, į kurią šis laukas turėtų būti įtrauktas. Atkreipkite dėmesį, kad išplečiamajame sąraše bus rodomos tik pasirinktinius laukus palaikančios lentelės. Techninės informacijos apie palaikomas lenteles rasite žemiau esančiame skyriuje.
    2. Pasirinkite naujojo lauko duomenų tipą. Galimi duomenų tipai yra žymės langelis, data, data ir laikas, dešimtainis skaičius, skaičius, išrinkimo sąrašas ir tekstas.

        - Jei pasirenkate teksto duomenų tipą, taip pat galite nurodyti didžiausią teksto, kurį galima įvesti šiame lauke, ilgį.
        - Jei pasirenkate išrinkimo sąrašo duomenų tipą, taip pat galite pasirinkti tinkamas lauko reikšmes.

    3. Nurodykite lauko pavadinimą, žymą ir žinyno tekstą. Pavadinimas atitinka fizinį lauko pavadinimą duomenų bazėje, o žyma ir žinyno tekstas yra tekstas, naudojamas šį lauką pateikti vartotojo sąsajoje.

8. Jei šioje formoje reikia sukurti tik šį lauką, spustelėkite **Įrašyti**. Jei reikia sukurti papildomų laukų, spustelėkite **Įrašyti ir kurti naują** bei grįžkite prie 7 veiksmo. Atkreipkite dėmesį, kad šiuo metu laukų limitas yra **20 pasirinktinių laukų vienoje lentelėje**.
9. Išėję iš dialogo lango **Kurti naują lauką**, grįšite į dialogo langą **Įterpti laukų**. Visi ką tik įtraukti pasirinktiniai laukai laukų sąraše bus automatiškai pažymėti, kad juos reikia įterpti į formą.
10. Spustelėkite **Įterpti**, kad pažymėtus laukus įterptumėte į pasirinktą formos sritį.
11. **Pasirenkama.** Personalizavimo įrankių juostoje įjunkite režimą **Perkelti**, kad naujuosius laukus perkeltumėte į norimą pasirinktos srities vietą. Norėdami gauti daugiau informacijos apie tai, kaip, naudojant įvairias personalizavimo galimybes, optimizuoti formą asmeniniam naudojimui, žr. [Vartotojo patirties personalizavimas](personalize-user-experience.md).

## <a name="sharing-custom-fields-with-other-users"></a>Pasirinktinių laukų bendrinimas su kitais vartotojais

Sukūrę pasirinktinį lauką ir jį įtraukę į formą, galbūt norėsite šį atnaujintą puslapio rodinį su naujuoju lauku bendrinti su kitais sistemos vartotojais. Tai galima atlikti toliau nurodytais dviem skirtingais būdais, naudojant produkto personalizavimo galimybes.

- Rekomenduojamas kelias – kreiptis į sistemos administratorių, kuris personalizuotą elementą gali perduoti visiems vartotojams arba vartotojų subrinkiniui. Norėdami gauti daugiau informacijos, žr. [Vartotojo patirties personalizavimas](personalize-user-experience.md).
- Arba savo keitimus (vadinamus *personalizavimais*) galite eksportuoti, nusiųsti vienam ar keliems vartotojams, kad kiekvienas iš jų jūsų keitimus importuotų. Eksportuoti ir importuoti personalizavimus galite pasirinkę personalizavimo įrankių juostos parinktį **Valdyti**.

## <a name="managing-custom-fields"></a>Pasirinktinių laukų valdymas

Visus pasirinktinius sistemos laukus galima valdyti modulio Sistemos administravimas puslapyje **Pasirinktiniai laukai**. Šiame puslapyje vartotojai gali pasiekti daug galimybių, įskaitant tolesnes.

- Visų pasirinktinių sistemos laukų sąrašo peržiūra.
- Esamų pasirinktinių laukų riboto redagavimo funkcija.
- Pasirinktinių laukų naikinimas.
- Pasirinktinių laukų rodymas duomenų objektuose.
- Pasirinktinių laukų žymų ir žinyno teksto vertimas.

### <a name="viewing-all-custom-fields"></a>Visų pasirinktinių laukų peržiūra

Puslapyje **Pasirinktiniai laukai** galima matyti visus sistemoje nustatytus pasirinktinius laukus. Tiesiog pasirinkite jus dominančią lentelę ir puslapis atsinaujins bei bus rodomas su ta lentele susietų pasirinktinių laukų sąrašas. Sąraše pasirinkę kokį nors pasirinktinį lauką, galėsite peržiūrėti visą informaciją apie jį.

### <a name="editing-custom-fields"></a>Pasirinktinių laukų redagavimas

Sukūrus pasirinktinį lauką, puslapyje **Pasirinktiniai laukai** galima modifikuoti tik tam tikrą pasirinktinio lauko informaciją.

*Galite* modifikuoti tolesnius atributus.

- Etiketė
- Žinyno tekstas
- Ilgis, teksto laukų

*Negalite* redaguoti tolesnių atributų.

- Lauko pavadinimas
- Duomenų tipas

Be to, jei laukų tipas yra išrinkimo sąrašas, galima pertvarkyti tinkamas pasirinktinio lauko reikšmes ir įtraukti naujų reikšmių; tačiau esamų išrinkimo sąrašo lauko reikšmių pašalinti negalima. Baigę redaguoti konkrečios lentelės laukus, nepamirškite spustelėti **Taikyti keitimus**, kad keitimai būtų įrašyti.

### <a name="exposing-custom-fields-on-data-entities"></a>Pasirinktinių laukų rodymas duomenų objektuose

Taip pat gali būti svarbu leisti, kad pasirinktiniai laukai būtų matomi duomenų objektuose. Duomenų objektai yra naudojami funkcijoje [„Office“ integravimo apžvalga](../../dev-itpro/office-integration/office-integration.md), taip pat duomenų importavimo / eksportavimo scenarijuose.

Norėdami pasirinktinį lauką rodyti duomenų objekte, atlikite tolesnius veiksmus.

1. Formoje **Pasirinktiniai laukai** pasirinkite pasirinktinį lauką.
2. Išplėskite skyrių **Objektai**, kad galėtumėte peržiūrėti aktualius objektus.
3. Spustelėkite mygtuką **Redaguoti**.
4. Modifikuokite lauką **Įjungta**, kad jį reikėtų pasirinkti prie kiekvieno objekto, kuriame turėtų būti rodomas šis laukas.
5. Spustelėkite **Taikyti keitimus**, kad įrašytumėte pasirinktis.

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a>Leidimas pasirinktinius laukus rodyti kitomis kalbomis

Kadangi pasirinktinius laukus vartotojams gali reikėti pasiekti įvairiomis kalbomis, puslapyje **Pasirinktiniai laukai** pateikiamas mechanizmas, leidžiantis pasirinktinio lauko žymos ir žinyno tekstą išversti į kitas kalbas.

Tolesniais veiksmais aprašomas pasirinktinių laukų vertimo į kitas kalbas procesas.

1. Puslapyje **Pasirinktiniai laukai** pasirinkite pasirinktinį lauką.
2. Veiksmų srityje pasirinkite mygtuką **Vertimai**. Taip atidarysite išplečiamąjį meniu su esamais šio lauko vertimais.
3. Išplečiamajame meniu **Kalba** rodoma, į kurias kalbas tekstas jau išverstas.

    Jei norite redaguoti esamą vertimą, meniu pasirinkite norimą kalbą ir modifikuokite žymos bei žinyno teksto reikšmes.

    Kitu atveju spustelėkite mygtuką **Įtraukti kalbą**, meniu pasirinkite norimą kalbą ir nurodykite išverstas žymos bei žinyno teksto reikšmes.

4. Baigę spustelėkite **Gerai**.

### <a name="deleting-custom-fields"></a>Pasirinktinių laukų naikinimas

Retais atvejais galite nuspręsti, kad koks nors pasirinktinis laukas yra nebereikalingas. Tokiu atveju sistemos administratorius gali pasirinkti tokį lauką panaikinti puslapyje **Pasirinktiniai laukai**. Norėdami tai padaryti, įsitikinkite, kad pasirinktas teisingas laukas, spustelėkite **Panaikinti**, tada – **Taip**, kad patvirtintumėte naikinimą, ir galiausiai spustelėkite **Taikyti keitimus**.

> [!NOTE]
> Šio veiksmo anuliuoti negalima ir juo duomenų bazėje bus visam laikui panaikinti su lauku susieti duomenys.

## <a name="appendix"></a>Priedas

### <a name="who-can-create-custom-fields"></a>Kas gali kurti pasirinktinius laukus?

Siekiant apsaugoti sistemą, pagal numatytuosius nustatymus kurti pasirinktinius laukus gali tik sistemos administratoriai. Tačiau, jei organizacija nusprendžia, kad to reikia, sistemos administratorius patyrusiems vartotojams gali suteikti teises kurti pasirinktinius laukus, naudodamas saugos vaidmenį **Patyręs vykdymo aplinkos tinkinimo vartotojas**. Šio saugos vaidmens neturintys vartotojai pasirinktinių laukų kurti negalės, tačiau vis tiek galės matyti ir interaktyviai naudoti kitų sistemos vartotojų įtrauktus pasirinktinius laukus.

### <a name="what-tables-support-custom-fields"></a>Kokios lentelės palaiko pasirinktinius laukus?

Dėl našumo ir techninių priežasčių pasirinktinių laukų galima įtraukti tik į tas lenteles, kurios atitinka tolesnes sąlygas.

- Lentelė turi būti pažymėta priklausanti vienai iš tolesnių grupių.

    - Grupuoti
    - WorksheetHeader
    - Pagrindinis
    - Įvairios
    - Parametras
    - Nuoroda
    - TransactionHeader

- Kitos lentelės naudojant šią lentelę išplėsti negalima.
- Lentelės negalima pažymėti sistemos lentele.
- Lentelė negali būti laikina.

### <a name="can-i-reference-custom-fields-from-the-developer-tools"></a>Ar galiu nurodyti pasirinktinius laukus iš programavimo įrankių?  

Pasirinktinius laukus galima valdyti tik vartotojo sąsajoje ir jų negalima nurodyti pagal kodą. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]