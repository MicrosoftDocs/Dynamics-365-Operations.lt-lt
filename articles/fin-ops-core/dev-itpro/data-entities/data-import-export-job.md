---
title: Duomenų importavimo ir eksportavimo užduočių apžvalga
description: Norėdami kurti ir valdyti duomenų importavimo bei eksportavimo užduotis, naudokite darbo sritį Duomenų valdymas.
author: peakerbl
ms.date: 10/21/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7e867b2815920a68e3cd79843ba7b15ed6bb635
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2022
ms.locfileid: "7981990"
---
# <a name="data-import-and-export-jobs-overview"></a>Duomenų importavimo ir eksportavimo užduočių apžvalga

[!include [banner](../includes/banner.md)]

Norint kurti ir valdyti duomenų importavimo bei eksportavimo užduotis, naudojama darbo sritis **Duomenų valdymas**. Pagal numatytuosius parametrus duomenų importavimo ir eksportavimo procesas kiekvienam paskirties duomenų bazės objektui sukuria išdėstymo lentelę. Naudodami išdėstymo lenteles, galite, prieš perkeldami duomenis, juos patikrinti, išvalyti ar konvertuoti.

> [!NOTE]
> Šioje temoje laikoma, kad esate susipažinę su [duomenų objektais](data-entities.md).

## <a name="data-importexport-process"></a>Duomenų importavimo / eksportavimo procesas
Toliau pateikti duomenų importavimo arba eksportavimo veiksmai.

1. Sukurkite importavimo arba eksportavimo užduotį, kurioje galite atlikti tolesnes užduotis.

    - Apibrėžkite projekto kategoriją.
    - Identifikuokite importuotinus arba eksportuotinus objektus.
    - Nustatykite užduoties duomenų formatą.
    - Nustatykite objektų seką, kad jie būtų apdorojami loginėmis grupėmis ir prasminga tvarka.
    - Nustatykite, ar reikia naudoti išdėstymo lenteles.

2. Patikrinkite, ar teisingai susieti šaltinio duomenys ir paskirties duomenys.
3. Patikrinkite importavimo arba eksportavimo užduoties saugą.
4. Importavimo arba eksportavimo užduotį vykdykite.
5. Peržiūrėdami užduočių retrospektyvą patikrinkite, ar užduotis buvo vykdyta taip, kaip tikėtasi.
6. Išvalykite išdėstymo lenteles.

Likusiuose šios temos skyriuose pateikiama daugiau informacijos apie kiekvieną proceso veiksmą.

> [!NOTE]
> Naudokite formos atnaujinimo piktogramą, kad atnaujintumėte duomenų importavimo / eksportavimo formą ir matytumėte naujausią eigą. Nerekomenduojama atnaujinti naršyklės lygio, nes ji nutrauks bet kokias importavimo / eksportavimo užduotis, kurios bys vykdomos ne bendrame pakete.

## <a name="create-an-import-or-export-job"></a>Importavimo arba eksportavimo užduoties kūrimas
Duomenų importavimo arba eksportavimo užduotį galima vykdyti vieną kartą arba daug kartų.

### <a name="define-the-project-category"></a>Projekto kategorijos apibrėžimas
Rekomenduojame atidžiai pasirinkti tinkamą importavimo arba eksportavimo užduoties projekto kategoriją. Projekto kategorijos gali padėti valdyti susijusias užduotis.

### <a name="identify-the-entities-to-import-or-export"></a>Importuotinų arba eksportuotinų objektų identifikavimas
Į importavimo arba eksportavimo užduotį galite įtraukti konkrečių objektų arba pasirinkti taikytiną šabloną. Naudojant šablonus užduotis užpildoma objektų sąrašu. Užduočiai suteikus pavadinimą ir ją įrašius, galima pasirinkti parinktį **Taikyti šabloną**.

### <a name="set-the-data-format-for-the-job"></a>Užduoties duomenų formato nustatymas
Pasirinkę objektą, turite pasirinkti duomenų, kurie bus eksportuojami arba importuojami, formatą. Formatai apibrėžiami naudojant plytelę **Duomenų šaltinių nustatymas**. Šaltinio duomenų formatas – tai **tipo**, **failo formato**, **eilutės skyriklio** ir **stulpelio skyriklio** kombinacija. Taip pat yra ir kitų atributų, bet apie šiuos žinoti yra būtina. Šioje lentelėje išvardijamos leistinos kombinacijos.

| Failo formatas            | Eilutės / stulpelio skyriklis                       | XML stilius                 |
|------------------------|--------------------------------------------|---------------------------|
| Excel                  | Excel                                      | \-NA–                     |
| XML                    | \-NA–                                      | XML elementas XML atributas |
| Atskirtas, fiksuotas plotis | Kablelis, kabliataškis, skirtukas, vertikali juosta, dvitaškis | \-NA–                     |

> [!NOTE]
> Svarbu pasirinkti tinkamą eilučių skyriklio **stulpelio skyriklio**, **teksto kvalifikatoriaus**, ir **Eilutės skyriklio**, jei **Failo formatas** parinktis yra nustatyta **Atribota**. Įsitikinkite, kad jūsų duomenyse nėra simbolio, kuris naudojamas kaip skyriklis arba kvalifikatorius, nes dėl to gali kilti klaidų importuojant ir eksportuojant.

### <a name="sequence-the-entities"></a>Objektų sekos nustatymas
Objektų seka gali būti nustatyta duomenų šablone arba importavimo ir eksportavimo užduotyse. Vykdydami užduotį, kurioje yra daugiau nei vienas duomenų objektas, turite įsitikinti, kad nustatyta teisinga duomenų objektų seka. Objektų seka pirmiausia nustatoma todėl, kad galėtumėte valdyti tarp objektų esančias funkcines priklausomybes. Jei objektai funkcinių priklausomybių neturi, galima suplanuoti juos importuoti arba eksportuoti lygiagrečiai.

#### <a name="execution-units-levels-and-sequences"></a>Vykdymo vienetai, lygiai ir sekos
Vykdymo vienetas, jo lygis ir objekto seka padeda valdyti, kokia tvarka duomenys eksportuojami ar importuojami.

- Skirtingų vykdymo vienetų objektai apdorojami lygiagrečiai.
- Jei objektų vykdymo vieneto lygis toks pats, jie apdorojami lygiagrečiai.
- Kiekviename lygyje objektai apdorojami pagal jų sekos numerį tame lygyje.
- Apdorojus vieną lygį apdorojamas kitas lygis.

#### <a name="resequencing"></a>Pakartotinis sekos nustatymas
Tolesnėse situacijose galbūt norėsite iš naujo nustatyti objektų seką.

- Jei visiems keitimams naudojama tik viena duomenų užduotis, naudodami pakartotinio sekos nustatymo parinktis galite optimizuoti visos užduoties vykdymo laiką. Tokiais atvejais vykdymo vienetas gali atstoti modulį, lygis – modulio funkcijų sritį, o seka – objektą. Naudodami šį metodą, galite lygiagrečiai dirbti su keliais moduliais, tačiau konkrečiame modulyje vis tiek dirbti laikydamiesi sekos. Norėdami užtikrinti, kad lygiagrečios operacijos bus įvykdytos sėkmingai, turite atsižvelgti į visas priklausomybes.
- Jei naudojamos kelios duomenų užduotys (pavyzdžiui, viena užduotis kiekvienam moduliui), nustatydami seką galite nurodyti objektų lygį ir seką, kad užduotys būtų vykdomos optimaliai.
- Jei priklausomybių visai nėra, objektų seką gali nustatyti naudodami skirtingus vykdymo vienetus – taip pasieksite didžiausią optimizaciją.

Meniu **Pakartotinis sekos nustatymas** galima naudoti pasirinkus kelis objektus. Iš naujo nustatyti seką galite pagal vykdymo vieneto, lygio arba sekos parinktis. Galite nustatyti pakartotinės pasirinktų objektų sekos reikšmių pokytį. Pagal nurodytą pokytį atnaujinamas pasirinktas kiekvieno objekto vienetas, lygis ir (arba) sekos numeris.

#### <a name="sorting"></a>Rikiavimas
Naudodami parinktį **Rikiuoti pagal**, objektų sąrašą galite peržiūrėti nuosekliai.

### <a name="truncating"></a>Trumpinimas
Dirbdami su importo projektais galite prieš importuodami sutrumpinti objektų įrašus. Tai naudinga, kai įrašus reikia importuoti į švarų lentelių rinkinį. Pagal numatytuosius nustatymus šis parametras išjungtas.

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a>Patikrinimas, ar teisingai susieti šaltinio duomenys ir paskirties duomenys
Susiejimo funkcija taikoma tiek importavimo, tiek eksportavimo užduotims.

- Importavimo užduoties kontekste susiejimo funkcija nurodo, kurie šaltinio failo stulpeliai tampa išdėstymo lentelės stulpeliais. Taip sistema gali nustatyti, kuriuos šaltinio failo stulpelių duomenis reikia nukopijuoti į kurį išdėstymo lentelės stulpelį.
- Eksportavimo užduoties kontekste susiejimo funkcija nurodo, kurie išdėstymo lentelės (tai yra, šaltinio) stulpeliai tampa paskirties failo stulpeliais.

Jei išdėstymo lentelės ir failo stulpelių pavadinimai sutampa, sistema pagal juos automatiškai nustato susiejimą. Tačiau, jei pavadinimai skiriasi, stulpeliai automatiškai nesusiejami. Tokiais atvejais atlikti susiejimą turite prie duomenų užduoties objekto pasirinkdami parinktį **Peržiūrėti schemą**.

Yra du susiejimo rodiniai: **Susiejimo vizualizacija** (numatytasis rodinys) ir **Susiejimo informacija**. Raudona žvaigždute (\*) nurodomi būtinieji objekto laukai. Kad galėtumėte dirbti su objektu, šiuos laukus reikia susieti. Dirbdami su objektu pagal poreikį galite atsieti kitus laukus. Norėdami atsieti lauką, jį pasirinkite stulpelyje **Objektas** arba stulpelyje **Šaltinis**, o tada pasirinkite **Naikinti pasirinktį**. Pasirinkite **Įrašyti**, kad įrašytumėte keitimus, ir uždarykite puslapį, kad grįžtumėte į projektą. Naudodami tą patį procesą, po importavimo galite redaguoti lauko susiejimą (iš šaltinio į išdėstymą).

Puslapyje susiejimą galite sugeneruoti pasirinkdami **Generuoti šaltinio susiejimą**. Sugeneruotas susiejimas veikia taip, kaip automatinis susiejimas. Todėl turite rankiniu būdu susieti visus nesusietus laukus.

![Duomenų susiejimas.](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a>Importavimo arba eksportavimo užduoties saugos tikrinimas
Prieigą prie darbo srities **Duomenų valdymas** galima apriboti, kad administratoriaus teisių neturintys vartotojai galėtų pasiekti tik konkrečias duomenų užduotis. Prieiga prie duomenų užduoties reiškia visišką prieigą prie tos užduoties vykdymo retrospektyvos ir prieigą prie išdėstymo lentelių. Todėl turite įsitikinti, kad kuriant duomenų užduotį nustatomi tinkami prieigos valdikliai.

### <a name="secure-a-job-by-roles-and-users"></a>Užduoties apsauga pagal vaidmenis ir vartotojus
Naudodami meniu **Taikytini vaidmenys**, užduotį galite apriboti taip, kad ją galėtų pasiekti tik vienas ar keli saugos vaidmenys. Prieigą prie užduoties turės tik tuos vaidmenis turintys vartotojai.

Užduotį taip pat galite apriboti taip, kad ją galėtų pasiekti tik konkretūs vartotojai. Užduotį apsaugojus ne pagal vaidmenis, o pagal vartotojus, turite daugiau valdymo galimybių, jei vaidmeniui priskiriami keli vartotojai.

### <a name="secure-a-job-by-legal-entity"></a>Užduoties apsauga pagal juridinį subjektą
Duomenų užduotys yra visuotinio pobūdžio. Todėl, jei duomenų užduotis buvo sukurta ir naudojama kokiame nors juridiniame subjekte, ji bus matoma kituose sistemos juridiniuose subjektuose. Toks numatytasis veikimas gali būti pageidaujamas kai kuriose taikymo situacijose. Pavyzdžiui, organizacija, sąskaitas faktūras importuojanti naudodama duomenų objektus, gali sudaryti centralizuotą sąskaitų faktūrų apdorojimo komandą, atsakingą už visuose organizacijos padaliniuose įvykstančių sąskaitų faktūrų klaidų valdymą. Tokioje situacijoje centralizuotai sąskaitų faktūrų apdorojimo komandai naudinga turėti prieigą prie sąskaitų faktūrų importavimo užduočių, gaunamų iš visų juridinių subjektų. Todėl numatytasis veikimas atitinka juridinio subjekto poreikį.

Tačiau organizacija gali norėti sąskaitų faktūrų apdorojimo komandas sudaryti kiekvienam juridiniam subjektui. Tokiu atveju konkretaus juridinio subjekto komanda turi turėti prieigą tik prie savo juridinio subjekto sąskaitų faktūrų importavimo užduočių. Norėdami patenkinti šį reikalavimą, galite sukonfigūruoti prieigos prie duomenų užduočių valdymą pagal juridinius subjektus – naudokite duomenų užduoties meniu **Taikytini juridiniai subjektai**. Tai sukonfigūravus, vartotojai gali matyti tik to juridinio subjekto, prie kurio jie šiuo metu yra prisijungę, užduotis. Norėdami matyti kito juridinio subjekto užduotis, vartotojai turi pereiti į tą juridinį subjektą.

Užduotį tuo pačiu metu galima apsaugoti pagal vaidmenis, vartotojus ir juridinį subjektą.

## <a name="run-the-import-or-export-job"></a>Importavimo arba eksportavimo užduoties vykdymas
Apibrėžę užduotį, ją galite vieną kartą vykdyti pasirinkdami mygtuką **Importuoti** arba **Eksportuoti**. Norėdami nustatyti pasikartojančią užduotį, pasirinkite **Kurti pasikartojančią duomenų užduotį**.

> [!NOTE]
> Importavimo arba eksportavimo užduotį galima vykdyti pasirinkus mygtuką **Importuoti** arba **Eksportuoti**. Tada paketinė užduotis bus suplanuota vykdyti tik vieną kartą. Užduotis gali nebūti vykdoma iš karto, jei paketinio vykdymo tarnyba ribojama dėl jos apkrovos. Užduotis taip pat galima vykdyti sinchroniškai pasirinkus **Importuoti dabar** arba **Eksportuoti dabar**. Tokiu būdu užduotis pradedama iš karto ir tai naudinga, jei paketinė užduotis nepradedama dėl ribojimo. Užduotys taip pat gali būti planuojamos vykdyti vėliau. Tai galima padaryti pasirenkant parinktį **Paketinis vykdymas**. Paketo ištekliuose gali būti vykdomas užklausų buferizavimas, todėl paketinė užduotis gali būti pradėta ne iš karto. Rekomenduojama naudoti paketą, nes jis taip pat padės dirbti su dideliais duomenų kiekiais, kuriuos reikia importuoti arba eksportuoti. Paketines užduotis galima suplanuoti vykdyti konkrečioje paketinėje grupėje, todėl turėsite daugiau valdymo funkcijų, susijusių su apkrovų paskirstymu.

## <a name="validate-that-the-job-ran-as-expected"></a>Tikrinimas, ar užduotis įvykdyta taip, kaip tikėtasi
Norint nustatyti ir ištirti importavimo bei eksportavimo užduočių triktis, galima naudoti jų retrospektyvą. Retrospektyviniai užduoties vykdymai sisteminami pagal laiko intervalus.

![Užduoties retrospektyvos intervalai.](./media/dixf-job-history.md.png)

Kiekvieną kartą vykdant užduotį pateikiama tolesnė informacija.

- Vykdymo informacija
- Vykdymo žurnalas

Vykdymo informacijoje rodoma kiekvieno duomenų objekto, kurį užduotis apdorojo, būsena. Todėl galite greitai rasti tolesnę informaciją.

- Kurie objektai buvo apdoroti
- Kiek objekto įrašų buvo sėkmingai apdoroti ir kiek apdoroti nepavyko
- Kiekvieno objekto išdėstymo įrašai

Išdėstymo duomenis galite atsisiųsti kaip eksportavimo užduočių failą arba kaip importavimo ir eksportavimo užduočių paketą.

Vykdymo informacijos srityje taip pat galite atidaryti vykdymo žurnalą.

## <a name="parallel-imports"></a>Lygiagretus importavimas
Norint pagreitinti duomenų importavimą, galima įjungti lygiagretų failo importavimo apdorojimą, jei objektas palaiko lygiagretų importavimą. Norėdami sukonfigūruoti objekto lygiagretų importavimą, atlikite toliau pateiktus veiksmus.

1. Eikite į **Sistemos administravimas \> Darbo sritys \> Duomenų valdymas**.
2. Skyriuje **Importavimas / eksportavimas** pasirinkite plytelę **Sistemos parametrai**, kad atidarytumėte puslapį **Duomenų importavimo / eksportavimo sistemos parametrai**.
3. Skirtuke **Objekto parametrai** pasirinkite **Konfigūruoti objekto vykdymo parametrus**, kad atidarytumėte puslapį **Objekto importavimo vykdymo parametrai**.
4. Nustatyti toliau pateiktus laukus, kad sukonfigūruotumėte objekto lygiagretų importavimą.

    - Lauke **Objektas** pasirinkite objektą.
    - Lauke **Importavimo įrašų ribinė reikšmė** įveskite importavimo įrašų ribinę reikšmę. Ji nurodo įrašų, kuriuos reikia apdoroti naudojant giją, skaičių. Jei faile yra 10 000 įrašų, o 2 500 įrašų yra 4 užduotys, kiekviena gija apdoros 2 500 įrašų.
    - Lauke **Importavimo užduočių skaičius** įveskite importavimo užduočių skaičių. Jis neturi viršyti maksimalaus paketo apdorojimui priskirto paketinių gijų skaičiaus dalyje **Sistemos administravimas \>Serverio konfigūravimas**.

## <a name="job-history-clean-up"></a>Darbo istorijos valymas 
Užduočių retrospektyvos valymo funkcija duomenų valdyme turi būti naudojama periodiniui vykdymo retrospektyvos valymui planuoti. Ši funkcija pakeičia ankstesnę išdėstymo lentelės valymo funkciją, kuri dabar nebenaudojama. Šios lentelės bus išvalytos pagal valymo procesą.

-   Visos išdėstymo lentelės

-   DMF išdėstymo tikrinimo žurnalas

-   DMF išdėstymo vykdymo klaidos

-   DMF išdėstymo žurnalo išsami informacija

-   DMF išdėstymo žurnalas

-   DMF aprašo grupės vykdymo retrospektyva

-   DMF vykdymas

-   DMF aprašo grupės vykdymas

Turite įjungti funkciją **Vykdymo retrospektyvos valymas** funkcijų valdymo srityje ir tada galite ją pasiekti nuėję į **Duomenų valdymas \> Užduoties retrospektyvos valymas**.

### <a name="scheduling-parameters"></a>Planavimo parametrai

Planuodami valymo procesą, turite nurodyti šiuos parametrus, kad apibrėžtumėte valymo kriterijus.

-   **„Dienų, kiek saugoma retrospektyva, skaičius“** – šis parametras naudojamas kontroliuoti vykdymo retrospektyvos saugomą kiekį. – Lauke nurodytas dienų skaičius. Kai valymo užduotis suplanuota kaip pasikartojanti paketinė užduotis, šis parametras veiks kaip nuolat judantis langas, tokiu būdu visada palikdamas retrospektyvą nepaliestą tam tikram nurodytam dienų skaičiui, naikindamas likusią dalį. Numatytoji vertė yra 7.

-   **„Valandų skaičius, reikalingas užduočiai įvykdyti“** – priklausomai nuo retrospektyvos, kurią reikia išvalyti, kiekio, bendras valymo užduoties vykdymo laikas gali svyruoti nuo kelių minučių iki kelių valandų. Šis parametras turi būti nustatytas kaip valandų, kurias bus vykdoma užduotis, skaičius. Po to, kai nurodytą valandų skaičių vykdoma išvalymo užduotis, ji bus išjungta ir vėl bus tęsiama pagal pasikartojimo grafiką.

    Maksimalų įvykdymo laiką galima nurodyti nustatant maksimalią valandų skaičiaus ribą, per kurią užduotis turi būti vykdoma naudojant šį parametrą. Valymo logika vienu metu remiasi vienos užduoties vykdymo ID chronologine tvarka išdėstyta seka, kur seniausia užduotis yra pirmoji susijusios vykdymo retrospektyvos valymui. Ji nustos rinkti naujo vykdymo ID valymui, kai likusi vykdymo trukmė yra nurodytos trukmės paskutiniuose 10 %. Kai kuriais atvejais tikimasi, kad valymo užduotis tęsis ilgiau nei nurodytas maksimalus laikas. Tai daugiausia priklausys nuo dabartinio vykdymo ID, kuris buvo pradėtas prieš 10% slenkstį, įrašų, kuriuos reikia panaikinti, skaičiaus. Pradėtas išvalymas turi būti užbaigtas siekiant užtikrinti duomenų vientisumą, o tai reiškia, kad išvalymas tęsis nepaisant nurodyto limito viršijimo. Kai valymas bus baigtas, naujas vykdymo ID neįtraukiamas ir valymo užduotis yra baigiama. Likusi vykdymo istorija, kuri nebuvo išvalyta dėl pakankamo vykdymo laiko trūkumo, bus įtraukta į kitą valymo užduoties planuojamą kartą. Numatytoji ir minimali šio parametro reikšmė nustatyta kaip 2 valandos.

-   **„Pasikartojantis paketas“** – valymo užduotį galima vykdyti vieną kartą rankiniu būdu, arba ji taip pat gali būti suplanuota pasikartojančiam vykdymui pakete. Paketas gali būti planuojamas naudojant **Vykdyti fone** parametrus, tai yra standartinis paketo nustatymas.

> [!NOTE]
> Jei įrašai išdėstymo lentelėse iki galo nėra išvalyti, įsitikinkite, kad valymo užduotis yra suplanuota vykdyti pasikartojančiu grafiku. Kaip paaiškinta pirmiau, bet kuriuo valymo vykdymo metu užduotis išvalys tik tiek vykdymo ID, kiek galės per nustatytą maksimalų valandų skaičių. Kad būtų galima tęsti visų likusių išdėstymo įrašų valymą, užduotis turi būti suplanuota vykdyti periodiškai.

## <a name="job-history-clean-up-and-archival"></a>Užduočių retrospektyvos valymas ir archyvavimas 
Užduoties retrospektyvos valymo ir archyvavimo funkcija pakeičia ankstesnes valymo funkcijos versijas. Šiame skyriuje bus paaiškintos naujos galimybės.

Vienas iš pagrindinių valymo funkcijos pakeitimų yra sistemos paketinės užduoties naudojimas retrospektyvai valyti. Naudojant sistemos paketinę užduotį, finansų ir operacijų programėlės gali automatiškai suplanuoti ir paleisti valymo paketinę užduotį, kai tik sistema bus parengta. Nebereikia paketinės užduoties planuoti neautomatiniu būdu. Šiuo numatytuoju vykdymo režimu paketinė užduotis bus vykdoma kiekvieną valandą nuo vidurnakčio ir išlaikys vykdymo retrospektyvą artimiausioms 7 dienoms. Išvalyta retrospektyva archyvuojama, kad ją būtų galima gauti ateityje. Pradedant 10.0.20 versija, ši funkcija visada įjungta.

Antrasis valymo proceso pakeitimas yra išvalytos vykdymo retrospektyvos archyvavimas. Išvalymo užduotis archyvuoja panaikintus įrašus didelių dvejetainių objektų saugykloje, kurią DIXF naudoja įprastai integracijai. Suarchyvuotas failas bus DIXF paketo formatu ir bus pasiekiamas 7 dienas didelių dvejetainių objektų saugykloje – tada jį bus galima atsisiųsti. Numatytąją 7 dienų suarchyvuoto failo laikymą parametruose galima pakeisti į ne daugiau nei 90 dienų.

### <a name="changing-the-default-settings"></a>Numatytųjų parametrų keitimas
Ši funkcija šiuo metu yra kaip peržiūros versija ir ji turi būti atskirai įjungta, įjungiant testą DMFEnableExecutionHistoryCleanupSystemJob. Išdėstymo valymo funkcija taip pat turi būti įjungta funkcijų valdymo srityje.

Norėdami pakeisti numatytąjį suarchyvuoto failo laikymo parametrą, eikite į duomenų valdymo darbo sritį ir pasirinkite **Užduoties retrospektyvos valymas**. Parinktį **Kiek dienų paketą laikyti didelių dvejetainių objektų saugykloje** nustatykite kaip reikšmę nuo 7 iki 90 (imtinai). Tai įsigalios archyvuose, sukurtame po šio pakeitimo.

### <a name="downloading-the-archived-package"></a>Suarchyvuoto paketo atsisiuntimas
Ši funkcija šiuo metu yra kaip peržiūros versija ir ji turi būti atskirai įjungta, įjungiant testą DMFEnableExecutionHistoryCleanupSystemJob. Išdėstymo valymo funkcija taip pat turi būti įjungta funkcijų valdymo srityje.

Norėdami atsisiųsti suarchyvuotą vykdymo retrospektyvą, eikite į duomenų tvarkymo darbo sritį ir pasirinkite **Užduoties retrospektyvos valymas**. Norėdami atidaryti retrospektyvos formą, pasirinkite **Paketų atsarginių kopijų retrospektyva**. Šioje formoje pateikiamas visų archyvuotų paketų sąrašas. Archyvą galima pasirinkti ir atsisiųsti pasirenkant **Atsisiųsti paketą**. Atsisiųstas paketas bus DIXF paketo formato ir jame bus tolesni failai.

-   Objektų išdėstymo lentelės failas
-   DMF aprašo grupės vykdymas
-   DMF aprašo grupės vykdymo retrospektyva
-   DMF vykdymas
-   DMF išdėstymo vykdymo klaidos
-   DMF išdėstymo žurnalas
-   DMFSTAGINGLOGDETAILS
-   DMF išdėstymo tikrinimo žurnalas



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
