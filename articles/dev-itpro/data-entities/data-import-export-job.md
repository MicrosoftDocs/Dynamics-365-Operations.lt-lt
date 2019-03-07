---
title: Duomenų importavimo ir eksportavimo užduotys
description: Norėdami kurti ir valdyti duomenų importavimo bei eksportavimo užduotis, naudokite darbo sritį Duomenų valdymas.
author: Sunil-Garg
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68cafc167c178e2feeb0a5af764a491ea6b3c60b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "360215"
---
# <a name="data-import-and-export-jobs"></a>Duomenų importavimo ir eksportavimo užduotys

[!include [banner](../includes/banner.md)]

Norint sprendime „Microsoft Dynamics 365 for Finance and Operations“ kurti ir valdyti duomenų importavimo bei eksportavimo užduotis, naudojama darbo sritis **Duomenų valdymas**. Pagal numatytuosius parametrus duomenų importavimo ir eksportavimo procesas kiekvienam paskirties duomenų bazės objektui sukuria išdėstymo lentelę. Naudodami išdėstymo lenteles, galite, prieš perkeldami duomenis, juos patikrinti, išvalyti ar konvertuoti.

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

![Duomenų susiejimas](./media/dixf-map.png)

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

## <a name="validate-that-the-job-ran-as-expected"></a>Tikrinimas, ar užduotis įvykdyta taip, kaip tikėtasi
Norint nustatyti ir ištirti importavimo bei eksportavimo užduočių triktis, galima naudoti jų retrospektyvą. Retrospektyviniai užduoties vykdymai sisteminami pagal laiko intervalus.

![Užduoties retrospektyvos intervalai](./media/dixf-job-history.md.png)

Kiekvieną kartą vykdant užduotį pateikiama tolesnė informacija.

- Vykdymo informacija
- Vykdymo žurnalas

Vykdymo informacijoje rodoma kiekvieno duomenų objekto, kurį užduotis apdorojo, būsena. Todėl galite greitai rasti tolesnę informaciją.

- Kurie objektai buvo apdoroti
- Kiek objekto įrašų buvo sėkmingai apdoroti ir kiek apdoroti nepavyko
- Kiekvieno objekto išdėstymo įrašai

Išdėstymo duomenis galite atsisiųsti kaip eksportavimo užduočių failą arba kaip importavimo ir eksportavimo užduočių paketą.

Vykdymo informacijos srityje taip pat galite atidaryti vykdymo žurnalą.

## <a name="clean-up-the-staging-tables"></a>Išdėstymo lentelių valymas
Išvalyti išdėstymo lenteles galite naudodami darbo srities **Duomenų valdymas** funkciją **Išdėstymo valymas**. Norėdami pasirinkti, kurioje išdėstymo lentelėje reikia panaikinti kuriuos įrašus, galite naudoti tolesnes parinktis.

- **Objektas** – jei pateiktas tik objektas, panaikinami visi to objekto išdėstymo lentelės įrašai. Pasirinkite šią parinktį, kad visus objekto duomenis išvalytumėte visuose duomenų projektuose ir visose užduotyse.
- **Užduoties ID** – jei pateikta tik užduoties ID, visi visų pasirinktos užduoties objektų įrašai panaikinami atitinkamose išdėstymo lentelėse.
- **Duomenų projektai** – jei pasirinktas tik duomenų projektas, panaikinami visi visų objektų ir visų pasirinktų duomenų užduočių įrašai.

Parinktis taip pat galite jungti ir taip dar labiau apriboti naikintinų įrašų rinkinį.
