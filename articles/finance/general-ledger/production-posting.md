---
title: Gamybos užsakymo registravimas
description: Šioje temoje pateikiama informacija apie skirtingus gamybos užsakymų registravimo tipus.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, ProjCategory, CostSheetDesigner
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: cd1b6c49e59f9480fd831ad5ff143033ca09792c
ms.sourcegitcommit: 5b55f2913e736d12e40c227bf3ce3a9abec815bd
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/24/2022
ms.locfileid: "8803051"
---
# <a name="production-postings"></a>Gamybos registravimas

Šioje temoje pateikiama informacija apie skirtingus registravimo gamybos užsakymo proceso tipus.


## <a name="material-consumption"></a>Medžiagų suvartojimas

Vykdant gamybos procesą ir užregistravus gamybos išrinkimo dokumento žurnalą, medžiagos užregistruojamos suvartotomis. Taip sukuriamos operacijos, kurios atima turimos atsargas. Gamybos parametruose **galite** nurodyti, ar nebaigtų žaliavų vertė (vadinama NG) turėtų būti registruojama DK.

Nebaigtų žaliavų vertė užregistruojama **įvertintose** **suvartotų medžiagų išlaidose ir įvertintai suvartotų medžiagų savikainai, NG sąskaitoms**. Gamybos užsakymo išrinkimo dokumentų procesas yra faktinis atsargų operacijų, susijusių su gamybos užsakymu, atnaujinimas. Kai gamybos užsakymas registruojamas kaip baigtas, faktinės operacijos atšaukiamos ir susijusios atsargų operacijos finansiškai atnaujinamos. Kai registruojamas pabaigos žurnalas, naudojamos **suvartotos medžiagų išlaidos** ir **suvartotų medžiagų išlaidos, naudojami** NG registravimo tipai.

Atsargų **registravimo** šablonų puslapio **skirtukas Gamyba kontroliuoja**, kaip gamybos užsakymai užregistruojami DK. Tai naudojama, kai gamybos **valdymo parametrų** puslapyje laukas DK **registravimas** nustatytas kaip Prekė **ir** ištekliai arba Prekė ir **kategorija.** 

Norint, kad išrinkimo dokumentų žurnalas būtų užregistruojamas gamybos užsakymo DK, turi būti įvykdytos šios sąlygos:

-   Gamybos **valdymo parametrų puslapyje turi** būti pažymėtas žymės langelis Registruoti **DK modulyje išrinkimo** sąrašą. Konkrečios gamybos valdymo parametrų dalies parametrų pagal vietą **puslapyje nustatymas gali būti nepaisomas**.
-   Prekės **, pasirinktos pirkimo užsakymo** eilutėje, prekių **modelių grupių** puslapyje turi būti pažymėtas žymės langelis Registruoti faktines atsargas.
-   Šių registravimo tipų pagrindinės sąskaitos **turi būti nurodytos atsargų** registravimo šablono puslapyje:
    -   **Įvertinta suvartotų medžiagų savikaina**
    -   **Įvertinta suvartotų medžiagų savikaina, NG**

## <a name="time-consumption"></a>Laiko suvartojimas

Laikas, kurį darbuotojai praleidžia gamybos užduotims atlikti, įrašomas Maršruto **kortelės žurnale** arba užduoties **kortelės žurnale**. Kai šie žurnalai užregistruojami, apdorojamas DK registravimas paskirtoje nebaigtų išteklių (NG) sąskaitoje. Ją užregistravus nurodoma laiko, skirto gamybos užsakymui atlikti, vertė. Gamybos užsakymą užregistravus baigtu, sudengiamos NG sąskaitos.

Yra trys galimi būdai laiko suvartojimui registruoti, priklausomai nuo pasirinkties, **pasirinktos** DK registravimo lauke **, gamybos kontrolės parametrų** puslapyje.

## <a name="reporting-finished-goods-and-error-quantities"></a>Paskelbimas apie pagamintų prekių ir klaidų kiekius

Kai gamybos užsakymas yra **paskelbtas baigtu**, **baigtos prekės atsargose atnaujinamos žurnale Paskelbta, kad** užbaigta. Jei naudojate NG apskaitą, registruojamas DK žurnalas, skirtas NG sąskaitoms sumažinti ir baigtų prekių atsargoms padidinti. Žurnale naudojamos standartinės išlaidos, nustatytos produktui. Jei gamybos **valdymo parametrų** puslapyje pasirinkta pasirinktis **Naudoti įvertintą savikainą**, bus naudojamos įvertintos gamybos užsakymo išlaidos.

Nebaigtų žaliavų vertė užregistruojama apskaičiuotose **pagamintose išlaidose ir Įvertintos pagamintos** **išlaidos, NG sąskaitose**. Gamybos **užsakymo skelbimo** baigtu procesas yra faktinis atsargų operacijų, susijusių su gamybos užsakymu, atnaujinimas. Kai gamybos užsakymas baigiamas, faktinės operacijos atšaukiamos ir susijusios atsargų operacijos finansiškai atnaujinamos. Kai registruojamas pabaigos žurnalas, naudojamos pagamintos **išlaidos ir** **pagamintos išlaidos, NG** registravimo tipai.

Atsargų **registravimo** šablonų **puslapio skirtukas** Gamyba naudojamas valdyti, kaip gamybos užsakymai bus užregistruojami DK. Tai naudojama, kai gamybos **valdymo parametrų** puslapyje laukas DK **registravimas** nustatytas kaip Prekė **ir** ištekliai arba Prekė ir **kategorija.** DK **prekių "** FastTab", kuris **yra** gamybos grupių puslapyje, taip pat gali būti naudojamas gamybos užsakymų registravimui kontroliuoti, kai laukas nustatytas kaip **Gamybos grupės**.

Kad paskelbimo **baigtu žurnalas** būtų užregistruojamas GAMYBOS užsakymo DK, turi būti įvykdytos šios sąlygos:
-   Gamybos **valdymo parametrų puslapyje turi būti** pasirinktas žymės langelis DK **užregistruoti ataskaitą kaip baigtą**. Konkrečios gamybos valdymo parametrų dalies parametrų pagal vietą **puslapyje nustatymas gali būti nepaisomas**.
-   Prekės **, pasirinktos pirkimo užsakymo** eilutėje, prekių **modelių grupių** puslapyje turi būti pažymėtas žymės langelis Registruoti faktines atsargas.
-   Šių registravimo tipų pagrindinės sąskaitos turi **būti nurodytos** atsargų registravimo šablono puslapyje:
    -   **Įvertinta gamybos savikaina**
    -   **Įvertinta gamybos savikaina, NG**

## <a name="ending-the-production-order"></a>Gamybos užsakymo baigimas

Prieš gamybos užsakymo pabaigos, apskaičiuojamos faktinės pagaminto kiekio išlaidos. Visos numatytosios medžiagų, darbo ir papildomos išlaidos yra anuliuojamos ir pakeičiamos faktinėmis išlaidomis. Bendros baigtos prekės išlaidos nurašomos nuo pagamintų **išlaidų** sąskaitos ir kredituodamos į **pagamintų išlaidų, NG** sąskaitą. Medžiagos, suvartotos gamybos užsakymo metu, **·** **kredituotos į suvartotų medžiagų išlaidas ir debetuotos į medžiagų savikainą, NG** sąskaitą.

Jei pasirenkate žymės **langelį** Baigti užduotį paleisdami išlaidų skaičiavimą, gamybos užsakymo būsena pakeičiama į **Baigta**. Ši būsena neleidžia registruoti jokių netyčinių papildomų išlaidų užbaigtam gamybos užsakymui. Galite nurodyti, kad klaidų kiekių, kurie yra pranešti kaip baigti, vertė turėtų būti priskirta prie gerų kiekių, kurie yra pranešami kaip baigti. Taip pat galite nurodyti, kad klaidų kiekių vertė būtų registruojama paskirtoje atliekų sąskaitoje. 

Norėdami nurodyti konkrečią nurašymo sąskaitą, atlikite šiuos veiksmus:
1.  Eikite į **Gamybos kontrolės** > **nustatymo** > **gamybos kontrolės parametrus**.
2.  Pasirinkite skirtuką **Standartinis** atnaujinimas.
3.  Lauke Nurašymo **metodas** pasirinkite Atliekų **sąskaita**.
4.  Lauke Atliekų **sąskaita pasirinkite** pagrindinę sąskaitą, kurioje pasibaigus gamybos užsakymui reikia registruoti klaidų kiekio nurašyme. Pavyzdžiui, pasirinkite išlaidų sąskaitą, pvz., 510380: Gamybos atliekos.

Kad pabaigos žurnalas būtų registruojamas gamybos užsakymo DK, reikia įvykdyti šias sąlygas:
-   Šių registravimo tipų pagrindinės sąskaitos turi **būti nurodytos atsargų** **registravimo šablone** arba gamybos grupių puslapyje:
    -   **Suvartotų medžiagų savikaina**
    -   **Suvartotų medžiagų savikaina, NG**
    -   **Pagaminto kiekio savikaina**
    -   **Pagaminto kiekio savikaina, NG**
-   Šių tipų pagrindinės sąskaitos turi būti nurodytos **išlaidų** kategorijų **,** **išteklių** arba išteklių grupių puslapyje:
    -   **Pagamintų išlaidųoje**
    -   **Suvartotos gamybos savikaina, NG**

## <a name="indirect-costs-for-production-orders"></a>Netiesioginės gamybos užsakymų išlaidos

Apdorodami gamybos užsakymo operacijas, galite konfigūruoti netiesiogines išlaidas pridėtinėms išlaidoms arba papildomiems mokesčiams jūsų DK fiksuoti. Faktinės netiesioginių išlaidų operacijos atpažįstamos atsargose, kai registruojate išrinkimo dokumento žurnalą arba pranešate, kad užbaigtas žurnalas. Finansinės netiesioginių išlaidų operacijos atpažįstamos atsargose, kai registruojate pabaigos žurnalą.

Galite atpažinti netiesiogines išlaidas laiko suvartojimui, susijusiam **su maršruto** kortelių žurnalais arba **užduočių kortelių** žurnalais. Šios operacijos yra atšaukiamos ir registruojamos finansinėse sąskaitose, kai gamybos užsakymas baigiasi. Norėdami gauti daugiau informacijos, eikite į įkainojimo [lapus](/supply-chain/cost-management/costing-sheets.md).

## <a name="controlling-the-level-of-ledger-posting"></a>DK registravimo lygio valdymas

Norėdami nustatyti **gamybos procesų DK** registravimo **lygį**, puslapyje Gamybos valdymo parametrai galite naudoti lauką DK registravimas. 

Galimi šie laukai:

### <a name="item-and-resource"></a>Prekė ir ištekliai

Kai DK registravimo lauke **pasirenkate** **pasirinktį** Prekė ir ištekliai, registravimo sąskaitos maršruto operacijos ištekliaus arba išteklių grupės. Konkrečių išteklių sąskaitos bus pirmoji registravimo pasirinktis. Jei sąskaita nenurodyta, bus naudojamos išteklių grupėje nurodytos sąskaitos. Kiekvienoje maršruto operacijos eilutėje gali būti vienas išteklius, nurodytas kaip įkainojimo **išteklius**. Šie ištekliai naudojami norint nustatyti naudotią sąskaitą. Ši pasirinktis dažniausiai naudojama, kai organizacija ištekliams priskiria valdymo išlaidas. Išlaidos ištekliams dažnai yra didesnės ir naudojamos norint daryti sprendimus "palyginti su pirkdami". Tai yra išsamiausia registravimo konfigūracija, kuri leidžia išsamiausią registravimo kontrolę ir labai išsamią gamybos proceso analizę.

### <a name="item-and-category"></a>Prekė ir kategorija

Dk registravimo lauke **pasirinkus pasirinktį** **Prekė** ir kategorija, registravimo sąskaitos bus siunčiamos iš išlaidų kategorijos **puslapio,** susijusio su kiekviena maršruto eilute. Kiekviena maršruto operacijos eilutė gali turėti tris išlaidų kategorijas: **nustatymo** laiką, **vykdymo** laiką ir **kiekį**. Ši pasirinktis dažniausiai naudojama, kai jūsų organizacijos pagrindinis dėmesys skiriamas proceso efektyvumui ir veiklos trukmei. Ši pasirinktis yra suvestines registravimo būdas ir vis tiek suteikia būdą sugrupuoti išlaidas į kategorijas.

### <a name="production-group"></a>Gamybos grupė

Kai lauke DK **registravimas pasirenkate** pasirinktį **Gamybos grupės**, registravimo sąskaitos siunčiamos iš **gamybos grupių** puslapio. **Gamybos grupės** paprastai naudojamos, kai daugiau nei viena gamybos eilutė vykdo panašius produktus arba turi panašią įrangą. Galite naudoti šią pasirinktį išlaidoms tarp dviejų skirtingų gamybos grupių palyginti.  
  
> [!NOTE]
> Jei naudojamas standartinis baigtos prekės išlaidų skaičiavimo metodas, tai atspindės galutinės operacijos. Jei faktinės išlaidos ir išlaidos, apskaičiuotos naudojant standartinį metodą, skiriasi, skirtumai registruojami sąskaitoje, kurioje rodomas pelnas ir nuostolis.

### <a name="route-groups-and-ledger-posting"></a>Maršrutų grupės ir DK registravimas

Nurodyta kiekvienos maršruto operacijos eilutės maršruto **grupė**. Įvertinimo **ir įkainojimo grupės Maršruto grupės nustatymo laikas,** **·** **·** **·** **·** **·** **Vykdymo laikas ir Kiekis naudojami kontroliuoti, ar laikas bus naudojamas įkainoti gamybos užsakyme registruojant užduoties kortelę arba maršruto kortelės žurnalą.** Jei pasirinktys uždraustos, laiko suvartojimo kvitas DK nebus sukurtas.

Norint, **kad maršruto** **kortelė ar užduoties** kortelių žurnalas būtų užregistruojamas gamybos užsakymo DK, turi būti įvykdytos šios sąlygos:

-   Maršruto **grupės** puslapio įvertinimo **ir** įkainojimo **grupėje** **turi būti pasirinktas laukas Nustatymo laikas,** Vykdymo **laikas arba** Kiekis.
-   Šių registravimo tipų pagrindinės sąskaitos turi būti **nurodytos išlaidų kategorijos,** **·** **maršruto,** maršruto **grupės arba gamybos grupių puslapyje:**
    -   Įvertinta suvartota gamybos savikaina
    -   Įvertinta suvartotos gamybos savikaina, NG

Šioje diagramoje parodomas maršruto grupės ryšys su kiekvienos operacijos (maršruto eilutės) bendrųjų išlaidų apskaičiavimu d pateiktame maršrute. Kiekviena maršruto eilutė turi vieną maršruto grupę. Maršruto grupė valdo nustatymo laiko, vykdymo laiko ir kiekio parametrus. Išlaidų **kategorijos skirtuke** yra trys nustatymo **, vykdymo** **ir** kiekio pasirinktys, **įgalintos** pagal maršruto grupių parametrą. Laiko **FastTab** yra trys laukai, pagrįsti maršruto grupe.

Naudojama formulė priklauso nuo to, ar pasirinktis įgalinta maršruto grupėje. Pasirinktos išlaidų kategorijos išlaidos padauginamos iš laiko metu įvesto kiekio, kad būtų galima apskaičiuoti visas išlaidas.

:::image type="complex" source="media/RouteGroupRelationship.png" alt-text="Maršrutų grupių ryšys su bendromis apskaičiuotomis išlaidomis.":::
Maršrutų grupių ryšys su bendromis apskaičiuotomis išlaidomis. Kiekviena maršruto eilutė turi vieną maršruto grupę. Maršrutų grupė valdo nustatymo laiko, vykdymo laiko ir kiekio parametrus. Išlaidų kategorijos skirtuke yra trys nustatymo, vykdymo ir kiekio pasirinktys, įgalintos remiantis maršruto grupių parametru. Laiko "FastTab" yra trys laukai, kurie įgalinti ir įkainoti remiantis maršruto grupe. Naudojama formulė priklauso nuo to, ar pasirinktis įgalinta maršruto grupėje. Pasirinktos išlaidų kategorijos išlaidos padauginamos iš laiko metu įvesto kiekio, kad būtų galima apskaičiuoti visas išlaidas.
:::image-end:::

## <a name="sample-posting-profile-configuration"></a>Registravimo šablono konfigūracijos pavyzdys

Toliau pateikiamoje lentelėje pateikiami numatytųjų registravimo tipų, kurių pagrindinės sąskaitos ir aprašymai yra pavyzdiniai, pavyzdžiai. 

 - Stulpelis **Debetas** /kreditas nurodo, ar operacija paprastai yra debetas, ar kreditas, ar kai kuriais atvejais ji gali registruoti arba debetą. 
 - Kliringo **sąskaitos** stulpelis nurodo, ar registravimo tipas yra tarpuskaitos sąskaita. Šioje sąskaitoje užregistruota suma automatiškai atšaukiama, kai užregistruojama vėlesnė operacija. 
 - Stulpelyje **P/F** nurodomas **finansinio** registravimo faktinio registravimo **P ir F**. 
 - Stulpelyje **Sekti** nurodoma, ar konkretaus registravimo tipo pagrindinė sąskaita paprastai yra ta pati, kaip ir kito registravimo tipo. Stulpelio vertė nurodo registravimo tipą, kurio paprastai laikomasi.

> [!NOTE]
> Siūlomos pagrindinės sąskaitos ir pagrindinės sąskaitos pavadinimai yra pasiūlymai. Rekomenduojame dirbti su savo buhalteriu, kad nustatytumėte geriausią konfigūraciją savo verslo poreikiams.


| Registravimo tipas  | Pagrindinės sąskaitos pavyzdys | Pagrindinės sąskaitos pavadinimo pavyzdys| Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | Faktinis arba finansinis | Atlikite | Aprašymas |
|---------------|----------------------|--------------------------|--------------|----------------|------------------|-----------------------|--------|------------|
| Įvertinta suvartotų medžiagų savikaina      | 140100               | Medžiagų atsargos        | Turtas        | Kreditas         | Y                | P                     | Suvartotų medžiagų savikaina                | Ši sąskaita naudojama, kai gamybos užsakymui registruojate išrinkimo dokumento žurnalą. Šios sąskaitos korespondentinė sąskaita yra įvertinta medžiagų savikaina, NG. Suma šioje sąskaitoje automatiškai atšaukiama, kai baigiamas gamybos užsakymas. Ši sąskaita rodo atsargų sąskaitą balanse.       |
| Įvertinta suvartotų medžiagų savikaina, NG | 150150               | Gamybos NG – medžiagos | Turtas        | Debetas          | Y                | P                     | Įvertinta gamybos savikaina, NG          | Ši sąskaita naudojama, kai gamybos užsakymui registruojate išrinkimo dokumento žurnalą. Šios sąskaitos korespondentinė sąskaita yra įvertinta suvartotų medžiagų savikaina. Suma šioje sąskaitoje automatiškai atšaukiama, kai baigiamas gamybos užsakymas. Ši sąskaita rodo NG savo balanse.                  |
| Įvertinta gamybos savikaina               | 140200               | Baigtų prekių atsargos   | Turtas        | Debetas          | Y                | P                     | Pagaminto kiekio savikaina                         | Ši sąskaita naudojama, kai gamybos užsakymui registruojate skelbimo baigtu žurnalą. Šios sąskaitos korespondentinė sąskaita yra įvertinta pagaminta savikaina, NG. Suma šioje sąskaitoje automatiškai atšaukiama, kai baigiamas gamybos užsakymas. Ši sąskaita rodo atsargų sąskaitą balanse. |
| Įvertinta gamybos savikaina, NG          | 150150               | Gamybos NG – medžiagos | Turtas        | Kreditas         | Y                | P                     | Pagaminto kiekio savikaina, NG                    | Ši sąskaita naudojama, kai gamybos užsakymui registruojate skelbimo baigtu žurnalą. Šios sąskaitos korespondentinė sąskaita yra įvertinta pagaminta savikaina. Suma šioje sąskaitoje automatiškai atšaukiama, kai baigiamas gamybos užsakymas. Ši sąskaita rodo NG savo balanse.                     |
| Suvartotų medžiagų savikaina                | 140100               | Medžiagų atsargos        | Turtas        | Kreditas         | N                 | Pn.                     | Įvertinta suvartotų medžiagų savikaina      | Ši sąskaita naudojama atpažinti medžiagas, kurios yra suvartojamos gamybos užsakyme pabaigos proceso metu. Korespondentinė sąskaita yra suvartotų medžiagų savikaina, NG.                                                                                                    |
| Suvartotų medžiagų savikaina, NG           | 150150               | Gamybos NG – medžiagos | Turtas        | Debetas          | N                 | Pn.                     | Įvertinta suvartotų medžiagų savikaina, NG | Ši sąskaita naudojama norint atpažinti NG medžiagas, kurios suvartojamos gamybos užsakyme pabaigos proceso metu. Šios sąskaitos korespondentinė sąskaita yra suvartotų medžiagų savikaina.                                                |
| Pagaminto kiekio savikaina                         | 140200               | Baigtų prekių atsargos   | Turtas        | Debetas          | N                 | Pn.                     | Įvertinta gamybos savikaina               | Ši sąskaita naudojama norint atpažinti baigtos prekės, gaminamos gamybos užsakymo, kai baigiate gamybos užsakymą, išlaidas. Šios sąskaitos korespondentinė sąskaita yra pagaminta savikaina, NG sąskaita.                                                                  |
| Pagaminto kiekio savikaina, NG                    | 150150               | Gamybos NG – medžiagos | Turtas        | Kreditas         | N                 | Pn.                     | Įvertinta gamybos savikaina, NG          | Ši sąskaita naudojama norint atpažinti baigtos prekės, gaminamos gamybos užsakymo, kai baigiate gamybos užsakymą, išlaidas. Šios sąskaitos korespondentinė sąskaita yra pagamintų išlaidų sąskaita.                                     |

> [!NOTE]
> " **Lean" paslaugos NG gavimo** ir " **Lean" paslaugos NG tarpuskaitos** sąskaita naudojama su "lean manufacturing" įkainojimo atvirkštine tvarka metu. Norėdami gauti daugiau informacijos, eikite į įkainojimo [atvirkštine tvarka eikite įkainojimo atvirkštine tvarka](/supply-chain/cost-management/backflush-costing.md).

