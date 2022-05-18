---
title: Darbo su Turto nuoma pradžia
description: Šioje temoje aprašoma funkcija Turto nuoma ir nurodomi veiksmai, reikalingi norint sukurti turto nuomą ir peržiūrėti tos nuomos informaciją.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeasingWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom:
- "4464"
- intro-internal
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-09-24
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 991685f50a00e60026331bf573561be904c7f9ab
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710335"
---
# <a name="asset-leasing-get-started"></a>Darbo su Turto nuoma pradžia

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma funkcija Turto nuoma ir nurodomi veiksmai, reikalingi norint sukurti turto nuomą ir peržiūrėti tos nuomos informaciją. Temoje taip pat apibrėžiami terminai, naudojami vartotojo sąsajoje ir dokumentacijoje. Turto funkcija yra išplėstinė nuomojamo turto valdymo, sekimo ir automatinių Microsoft Dynamics finansinių operacijų galimybė 365 finansuose. Turto nuoma atitinka tarptautinius apskaitos standartus (IFRS 16) ir JAV GAAP standartus (ASC 842). Turto nuoma fiksuoja ir apdoroja nuomos informaciją ir padeda generuoti mėnesinius nuomos ciklo žurnalo įrašus – nuo pradinio pripažinimo iki nuomos pablogėjimo ir nutraukimo. Turto perteikite sklandžiai su kitais "Dynamics 365 Finance" komponentais, įskaitant ilgalaikį turtą, mokėtinas sumas ir DK.

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti **Funkcijos valdymas** darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Darbo srityje **Funkcijų valdymas** raskite ir pasirinkite funkciją, pavadinta **Turto nuoma** ir tada spustelėkite **Įjungti dabar** mygtuką.

Daugiau informacijos apie apskaitos standartus žr. standartinėje IFRS 16 ir JAV GAAP ASC 842 dokumentacijoje.

## <a name="asset-leasing-elements"></a>Turto nuomos elementai
Toliau pateiktoje diagramoje rodomi pagrindiniai nuomos verslo proceso elementai.

[![Turto nuomos elementai.](./media/overview-01.png)](./media/overview-01.png)

Nuomojame turte yra toliau pateikti pagrindiniai komponentai.

- **Nuomos sutartis** – nuomotojas valdo turtą ir sutinka išnuomoti jį nuomininkui konkrečiam laikotarpiui už periodinius nuomos mokesčius. Be teisinės nuomotojo ir nuomininko sutarties, nuomos sutartyje nurodomi valdymo sprendimai, pvz., tikimybė pasinaudoti pratęsimo galimybe ir nuosavybės perkėlimas.

- **Nuomos skaičiavimas ir klasifikavimas pagal apskaitos standartą** – nuomos skaičiavimas ir klasifikavimas nustato apskaitos standartą, kuris bus taikomas atliekant pradinį ir vėlesnį įvertinimą, ir klasifikavimo tikrinimą, nustatantį, koks bus nuomos tipas. Nuoma gali būti finansinė nuoma, veiklos nuoma, trumpalaikė nuoma arba mažos vertės turto nuoma. Sistema taip pat apskaičiuoja dabartinę būsimų minimalių grynąją nuomos mokesčių vertę siekiant atlikti vertinimą ir klasifikavimą.

- **Nuomos operacijos** – Turto nuoma palaiko pradinį naudojimo teise valdomo turto balanso nuomos pripažinimą, ir vėlesnį balanso nuomos arba ne balanso nuomos įvertinimą. Pradinio pripažinimo operacija apskaičiuoja dabartinę grynąją būsimų minimalių nuomos mokesčių vertę. Šie duomenys naudojami norint nustatyti pradinio naudojimo teise valdomo turto ir nuomos įsipareigojimo vertę, kuri turi įtakos organizacijos balansui. Vėlesnis mėnesinis nuomos operacijų įvertinimas apima nuomos įsipareigojimo palūkanų kaupimą, didinantį nuomos įsipareigojimą. Jis taip pat apskaičiuoja nuomos mokesčių, mažinančių nuomos įsipareigojimą, kaupimą, kuris vėliau bus sumokėtas nuomotojui. Įvertinimas taip pat apima naudojimo teise valdomo turto amortizaciją.

  Jei nuoma yra ne balanso, sistema apskaičiuoja tiesiogiai proporcingas nuomos išlaidas arba pagal turto ekonominį laiką, arba nuomos terminą, t. y. tą dydį, kuris mažesnis. Nuomos koregavimai matuoja sutarties keitimus, pvz., nuomos plėtinį arba išplėtimą ir nuvertėjimo operaciją, naudojančią naudojimo teise valdomą turtą išlaidoms, kurių negalima grąžinti.

  Turto nuoma integruojama su Didžioji knyga siekiant užtikrinti, kad visos užregistruotos nuomos operacijos atnaujins jūsų sąskaitų planą. Turto nuoma integruojama su Mokėtinos sumos siekiant sekti nuomotojo SF modulyje Mokėtinos sumos ir ateityje atlikti mokėjimus. Integravimas su Ilgalaikis turtas leidžia sekti nuomą ilgalaikio turto registre ir registruoti naudojimo teise valdomo turto operacijas, įskaitant pradinį turto pripažinimą, nusidėvėjimą ir nuvertėjimą, modulyje Ilgalaikis turtas.   

## <a name="asset-leasing-components"></a>Turto nuomos komponentai 
Turto nuoma susieja nuomos informaciją, mokėjimo grafikus, pradžios ir pabaigos datas bei mokėjimo dažnumą. Ji taip pat automatizuoja esamos grynosios vertės, mėnesinių nuomos mokesčių, palūkanų ir nuomos amortizacijos skaičiavimus. Sistema vykdo nuomos klasifikacijos testus atsižvelgdama į konfigūraciją. Sistema taip pat sukuria ir registruoja atitinkamas nuomos operacijas, paremtas sistema, kurią apibrėžia apskaitos standartas, kurio laikotės.

Toliau pateiktoje diagramoje vaizduojama nuomos knyga, nuoma, apskaičiuotas mokėjimo grafikas, nuomos ir nuomos knygų klasifikacijos testai bei atitinkamos apskaitos operacijos.

[![Nuoma, nuomos knyga ir mokėjimo grafikas.](./media/overview-02.png)](./media/overview-02.png)

- **Nuomos knyga** – nuomos knyga apima visą nuomos sutarties informaciją, pvz., nuomos sąlygas, tikrąją vertę ir nuomos mokesčius. Joje taip pat yra apskaitos standartas, kurio laikotės, nuomos tipas ir ribinės vertės, į kurias atsižvelgiama nuomos klasifikacijos teste. Nuomos knygoje taip pat yra nuomos operacijos, užregistravusios didžiojoje knygoje. 
  
- **Nuoma** – nuomos metu yra turto nuomos informacija, kuri atspindi turto pagrindą, nuomos informacijos šaltinis yra nuomos sutartis ir valdymo sprendimas, kurie abu jie atliekami ne "Dynamics 365 Finance". Turto tikroji vertė yra kaina, kuri būtų sumokėta už turtą operacijos metu įvertinimo dieną. Ši vertė gali priklausyti nuo turto tipo, rinkos sąlygų ir kitų kriterijų, į kuriuos galima atsižvelgti vertinant. Į turto tikrąją vertę bus atsižvelgiama klasifikacijos testo lygtyje.

- **Turto naudingo naudojimo laikas** – tai yra likę turto naudingo naudojimo laikotarpiai nuo nuomos pradžios datos. Į turto naudingo naudojimo laiką bus atsižvelgiama klasifikacijos testo lygtyje. Jis skiriasi nuo naudingo naudojimo laiko, kaip nurodyta Ilgalaikis turtas.

- **Apskaičiuota skolinimosi palūkanų norma** – tai palūkanų norma, kuri bus naudojama dabartinei grynajai vertei apskaičiuoti. Sistema naudos numanomą normą, jei ji apibrėžiama nuomos duomenyse, kad apskaičiuotų dabartinę grynąją nuomos mokesčių vertę. Jei numanoma norma nenurodyta, sistema naudos apskaičiuotą skolinimosi palūkanų normą.

- **Anuiteto tipas** – tai nuomos mokestis, kurį reikia sumokėti arba mokėjimo laikotarpio pradžioje, arba laikotarpio pabaigoje. Tai gali būti išankstinis mokėjimas ar laikotarpio pradžios anuitetas (nuomos mokėjimo laikotarpio pradžioje) arba įprastas anuitetas (nuomos mokėjimo laikotarpio pabaigoje).

  Pirmasis mėnuo bus laikomas nuliniu išankstinio mokėjimo laikotarpiu; pirmasis mėnuo bus laikomas pirmuoju mokėjimo skolų laikotarpiu.

- **Sudėjimo intervalas** – jis nurodo laikotarpių, kurių metu skaičiuojamos palūkanos, skaičių per metus. Jis gali būti mėnesinis (12 laikotarpių per metus), ketvirtinis (4 laikotarpiai per metus), pusmetinis (2 laikotarpiai per metus) arba metinis (1 laikotarpis per metus). Į laikotarpių skaičių bus atsižvelgiama dabartinės grynosios vertės skaičiavime.

- **Pradžios data** – tai data, kai nuomotojas leidžia nuomininkui naudoti turtą. Visi nuomos skaičiavimai ir operacijos bus pagrįsti pradžios data. Pradžios data turi būti laikotarpio pradžioje (pirmą mėnesio dieną), siekiant užtikrinti vėlesnių skaičiavimų tikslumą. Galite naudoti lauką **Sutarties pasirašymo data**, norėdami įvesti faktinę datą, kai sutartis buvo pasirašyta.

- **Nuomos terminas** – tai nuomos laikotarpio trukmė mėnesiais.

> [!NOTE] 
> Nuomos termino apibrėžimas paremtas laikotarpių skaičiumi arba intervalais, esančiais mokėjimo grafiko eilutėse. Apibrėžtas intervalų skaičius bus konvertuojamas į mėnesius.

- **Mokėjimo grafiko eilutė** – ji užfiksuoja nuomos mokesčius per laikotarpį. Be to, ji nurodo, ar bus vykdomas atnaujinimo laikotarpis ir ar jis bus įtrauktas į pradinį naudojimo teise valdomo turto ir nuomos įsipareigojimo įvertinimą. Galite nurodyti nuomos mokėjimo termino pradžios datą ir laikotarpių intervalus, nurodančius nuomos trukmę (tai gali būti dienos, mėnesiai ar metai).

- **Mokėjimo dažnumas** – nurodo, ar mokama kas mėnesį, kas ketvirtį, kas pusmetį, ar kas metus. Pabaigos data apskaičiuojama automatiškai, remiantis pradžios data ir įvestų laikotarpių skaičiumi.

- **Mokėjimo grafikas** – tai apskaičiuota dabartinė grynoji vertė, paremta nuomos mokesčių mokėjimo trukme, mokesčių suma, sudėjimo laikotarpiais ir anuiteto tipu.

- **Laikotarpiai** – tai nuomos laikotarpiai, nurodantys sudėjimo intervalą ir anuiteto tipą. Sudėjimo intervalas nustato, kaip laikotarpiai bus suskirstyti. Galite nustatyti toliau nurodytus sudėjimo intervalus.

  - Mėnesinis, 12 laikotarpių per metus
  - Ketvirtinis, 4 laikotarpiai per metus
  - Pusmetinis, 2 laikotarpiai per metus
  - Metinis, 1 laikotarpis per metus

Pirmas laikotarpis prasidės nuliniu laikotarpiu, jei anuiteto tipas yra laikotarpio pradžios anuitetas. Kitu atveju pirmas laikotarpis prasidės pirmuoju, jei anuiteto tipas yra mokėjimo skolos.

- **Mėnesiai** – nurodo kalendorinių mėnesių skaičių nuomos trukmės laikotarpiu. Mokėjimo suma yra mokėtina suma, nurodyta pagal mokėjimo dažnumą. Apskaičiuotą dabartinę grynąją vertę sudaro dabartinis grynąja verte paremtas nuomos mokestis per laikotarpį, sudėjimo intervalai ir apskaičiuota skolinimosi palūkanų norma.

> [!NOTE] 
> Dabartinė grynoji vertė apskaičiuojama pagal diskontuoto pinigų srauto lygtį.

- **Knygos** – tai iš anksto sukonfigūruota sąranka, kuris bus susieta su kiekviena nuoma. Knyga apibrėžia taikomą apskaitos standartą, nuomos tipus ir ribines vertes, naudojamas kaip klasifikacijos testų pagrindą. Klasifikacijos testai naudojami norint nurodyti nuomos tipą automatiškai.

- **Apskaitos sistema** – nurodo pasirinktą apskaitos standartą, kurį palaikote – IFRS 16 arba ASC 842. Apskaitos standartas pažymėtas knygoje, kuri susijusi su nuoma. Apskaitos standartas nustatys DK sąskaitas, nurodytas registravimo šablone.

- **Nuomos tipai** – nurodo, kuris iš dviejų nuomos tipų bus naudojamas – finansinė nuoma ar veiklos nuoma. Jei nuoma finansinė, nuomininkui pateikiama rizika ir nauda, susijusios su nuomojamu turtu. Jei nuoma yra veiklos, rizika ir nauda, susijusios su nuomojamu turtu, nepateikiamos nuomininkui. Trečia parinktis yra automatizuota nuomos tipo (finansinė arba veiklos) identifikacija pagal knygoje nurodytas ribines vertes. Ši automatiška identifikacija atliekama nuomos perklasifikavimo testo metu.

- **Ribinės vertės** – jos naudojamos nuomos klasifikacijos testų metu siekiant nustatyti, ar turtas klasifikuojamas kaip vienas iš toliau pateiktų:

  - **Nuomos terminas** – tai naudingo naudojimo laiko, kuris bus naudojamas klasifikacijos teste, procentinė dalis. Sistema klasifikuos nuomą kaip finansinę, jei nustatytas automatinis nuomos tipas ir jei nuomos terminas per visą turto naudingo naudojimo laiką yra didesnis arba lygus čia apibrėžtai procentinei daliai.

  - **Dabartinė grynoji vertė** – tai turto tikrosios vertės, kuri bus naudojama klasifikacijos teste, procentinė dalis. Sistema klasifikuos nuomą kaip finansinę, jei nustatytas automatinis nuomos tipas ir jei būsimų nuomos mokesčių dabartinė grynoji vertė kartu su turto tikrąja verte yra didesnė arba lygi čia apibrėžtai procentinei daliai.

  - **Trumpalaikė nuoma** – jei nuomos terminas yra mažesnis arba lygus apibrėžtai vertei, nuoma bus klasifikuojama kaip trumpalaikė nuoma.

  - **Mažos vertės turto nuoma** – jei turto tikroji vertė yra mažesnė arba lygi apibrėžtai vertei, nuoma bus klasifikuojama kaip mažos vertės turto nuoma.

  - **Nuomos klasifikacija ir operacijos** – nuomos klasifikacija yra automatizuotas procesas, skirtas nuomai klasifikuoti pagal nustatytas knygų ribines vertes ir kitus klasifikacijos testo kriterijus, siekiant nustatyti, ar nuoma yra finansinė nuoma, veiklos nuoma, trumpalaikė nuoma ar mažos vertės turto nuoma. Jis taip pat naudojamas norint nustatyti, ar laikomasi atidėtojo nuomos mokėjimo proceso.

Klasifikacijos testai apima nuosavybės perkėlimą, pirkimo galimybę, nuomos terminą, dabartinę grynąją vertę ir unikalų turtą. Toliau pateiktoje diagramoje pateikiami nuomos klasifikacijos testai.

[![Nuomos klasifikacijos testai.](./media/overview-03.png)](./media/overview-03.png)

Kiekvieno nuomos tipo skirtingų nuomos operacijų apskaita vykdoma skirtingai. Operacijos apima pradinį pripažinimą, palūkanų sąnaudas, nuomos mokėjimo terminą bei nuomos nusidėvėjimą ir jos pagrįstos apskaitos standartais, kurių laikotės (IFRS 16 arba ASC 842). DK sąskaitos nurodomos kiekvieno operacijos tipo ir apskaitos sistemos nuomos registravimo šablone.

## <a name="asset-leasing-transactions"></a>Turto nuomos operacijos

#### <a name="initial-recognition"></a>Pradinis pripažinimas 
Pradinis nuomojamo turto pripažinimas naudoja apskaičiuotą dabartinę grynąją vertę, kad ją būtų galima nurodyti balanse. Apskaitos įrašas sugeneruojamas automatiškai. Ši operacija debetuoja naudojimo teise valdomo turto sąskaitą ir kredituoja veiklos nuomos įsipareigojimo sąskaitą, kaip nurodyta toliau. Jei ilgalaikis turtas susietas su nuoma, pradinio pripažinimo įrašas nurodys ilgalaikio turto įsigijimą. Šiame scenarijuje turite nustatyti ilgalaikio turto registravimo šabloną, kad būtų galima registruoti į naudojimo teise valdomo turto sąskaitą. 

> [!NOTE]
> Veiklos nuomą palaiko tik JAV GAAP ASC 842.

|     Tipas                                          |     Debetas                     |     Kreditas                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Veiklos nuoma pagal JAV GAAP            |     Naudojimo teise valdomas turtas        |     Veiklos nuomos įsipareigojimas     |
|     Finansinė nuoma pagal IFRS ir JAV GAAP      |     Naudojimo teise valdomas turtas        |     Finansinės nuomos įsipareigojimas       |

#### <a name="lease-liability-amortization-interest-expense"></a>Nuomos įsipareigojimo amortizacija (palūkanų sąnaudos) 
Nuomos palūkanos pripažįstamos skaičiuojant nuomos pradžios balanso palūkanas, laikotarpio nuomos mokesčius, skolinimosi palūkanų normą ir sudėjimo intervalų laikotarpius per metus. Palūkanų suma didina veiklos nuomos įsipareigojimo sąskaitą ją kredituodama, o tai bus nurodyta organizacijos balanse. Operacija taip pat įtraukia debeto įrašą į palūkanų sąnaudų sąskaitą (tai nurodoma finansinės nuomos pelno ir nuostolio išraše) ir į veiklos nuomos išlaidų sąskaitą.

|     Tipas                                          |     Debetas                     |     Kreditas                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Veiklos nuomos įsipareigojimo įrašas pagal JAV GAAP ASC 842    |     Nuomos išlaidos         |     Veiklos nuomos įsipareigojimas         |
|     Finansinės nuomos įsipareigojimo įrašas pagal IFRS ir JAV GAAP      |     Palūkanų išlaidos          |     Finansinės nuomos įsipareigojimas           |

#### <a name="accrued-lease-payment"></a>Sukauptas nuomos mokestis
Sukauptas nuomos mokestis pripažįstamas kaip būsimas nuomos mokestis, kuris bus apdorotas kaip banko ar grynųjų pinigų sąskaitų mokėjimo operacija. Nuomos mokesčio terminas mažina nuomos įsipareigojimą debetuodamas nuomos įsipareigojimo sąskaitą pagal tai, ar nuomotojo tiekėjo papildoma knyga yra nurodyta kaip tiekėjas, arba registruodamas kredito pusę į mokėtinų pažymų DK sąskaitą, tokiu atveju mokestis bus vykdomas pagal tiekėją arba mokėtinas pažymas.

|     Tipas                                          |     Debetas                     |     Kreditas                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Veiklos nuoma pagal JAV GAAP              |  Veiklos nuomos įsipareigojimas    |   Tiekėjo įsipareigojimas (papildoma knyga) / mokėtinos pažymos  |
|     Finansinė nuoma pagal IFRS ir JAV GAAP        |  Finansinės nuomos įsipareigojimas      |   Tiekėjo įsipareigojimas (papildoma knyga) / mokėtinos pažymos  |

#### <a name="asset-depreciation"></a>Turto nusidėvėjimas
Naudojimo teise valdomas turtas nusidėvi per turto naudingo naudojimo laiką arba nuomos terminą, t. y. per tą, kuris trumpesnis. JAV GAAP (ASC 842) veiklos nuomos nusidėvėjimo skaičiavimo būdas yra paremtas skirtumu tarp tiesiogiai proporcingų nuomos išlaidų ir palūkanų sumos. Finansinės nuomos nusidėvėjimas apskaičiuojamos naudojant standartinį tiesioginio proporcingumo būdą. Nuomos nusidėvėjimas turi įtakos pelno ir nuostolio išrašui, debetuodamas palūkanų sąnaudas. Sukauptos finansinės nuomos naudojimo teise valdomo turto sąskaitos kreditavimas turi įtakos balansui. Jei nuoma yra susieta su ilgalaikiu turtu, nusidėvėjimo operacijos bus vykdomos tik pagal ilgalaikio turto modulį. 

|     Tipas                                          |     Debetas                     |     Kreditas                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Veiklos nuoma pagal JAV GAAP              |  Nuomos išlaidos                |   Sukauptas naudojimo teise valdomo turto nusidėvėjimas     |
|     Finansinė nuoma pagal IFRS ir JAV GAAP        |   Naudojimo teise valdomo išlaidų nusidėvėjimas   |   Sukauptas naudojimo teise valdomo turto nusidėvėjimas    |

#### <a name="short-term-lease"></a>Trumpalaikė nuoma
Trumpalaikė nuoma pripažįstama kaip sąnaudos, o tai turės įtakos organizacijos pajamų išrašui. Sugeneruotas nuomos mokesčio terminas debetuos nuomos išlaidų sąskaitą ir kredituos mokėtinų pažymų arba tiekėjo papildomos knygos sąskaitą.

|     Tipas                                          |     Debetas                     |     Kreditas                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Trumpalaikės nuomos įrašas pagal IFRS ir JAV GAAP     |  Nuomos išlaidos                |   Tiekėjo įsipareigojimas (papildoma knyga) / mokėtinos pažymos  |

#### <a name="low-value-lease"></a>Mažos vertės turto nuoma
Mažos vertės turto nuoma pripažįstama kaip sąnaudos, turinčios įtakos jūsų organizacijos pajamų išrašui. Sugeneruotas nuomos mokesčio terminas debetuos nuomos išlaidas ir kredituos mokėtinas pažymas arba tiekėjo papildomą knygą.

|     Tipas                                          |     Debetas                     |     Kreditas                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Mažos vertės turto nuomos įrašas pagal IFRS ir JAV GAAP      |  Nuomos išlaidos                |   Tiekėjo įsipareigojimas (papildoma knyga) / mokėtinos pažymos  |


#### <a name="index-revaluation"></a>Indeksuojamos palūkanų normos perkainojimas
Tai kintamų nuomos mokesčių, vertinamų pagal indeksuojamą palūkanų normą, turto nuomos sąskaita. Nuomos mokesčių pasikeitimai, kuriuos sukėlė indeksuojamos palūkanų normos svyravimai, sudaro nuomos koregavimą pagal IFRS 16. Nuomos įsipareigojimas ir naudojimo teise valdomas turtas bus pakoreguoti taip, kad būtų atsižvelgta į naujus mokesčius. 

|     Tipas                                          |     Debetas                             |     Kreditas                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Indeksuojamos palūkanų normos perkainojimo įrašas pagal IFRS esant padidėjimui  |  Naudojimo teise valdomas turtas       |   Veiklos nuomos įsipareigojimas |
|   Indeksuojamos palūkanų normos perkainojimo įrašas pagal IFRS esant sumažėjimui  |  Veiklos nuomos įsipareigojimas  |   Naudojimo teise valdomas turtas      |

Kai mokesčiai pasikeičia dėl indeksuojamos palūkanų normos pasikeitimo, tik kintami mokesčiai pasikeičia, išskyrus atvejus, kai yra papildomų grynųjų pinigų srautų pakeitimų, pvz., nuomos sąlygų pakeitimas, susijęs su palūkanų normomis, pagal JAV GAAP ASC 842.

#### <a name="lease-adjustment"></a>Nuomos koregavimas
Turto nuoma leidžia koreguoti nuomą, jei modifikuojamos nuomos sąlygos, nuoma pratęsiama arba jei yra papildomų aplinkybių, dėl kurių nuomą reikia koreguoti. Nuomos koregavimai registruojami siekiant padidinti arba sumažinti naudojimo teise valdomą turtą ir nuomos įsipareigojimą. Koregavimo procesas taiko įsipareigojimo amortizacijos ir turto balanso perkėlimo pabaigos balansus koregavimo dieną. Kai nuoma susieta su ilgalaikiu turtu, naudojimo teise valdomo turto koregavimas bus užregistruotas naudojant ID, priskirtą modulyje Ilgalaikis turtas. 

|     Tipas                                          |     Debetas                             |     Kreditas                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   IFRS ir JAV GAAP nuomos koregavimo įrašas esant padidėjimui     |  Naudojimo teise valdomas turtas       |   Veiklos nuomos įsipareigojimas |
|   IFRS ir JAV GAAP nuomos koregavimo įrašas esant sumažėjimui     |  Veiklos nuomos įsipareigojimas  |   Naudojimo teise valdomas turtas      |


#### <a name="lease-impairment"></a>Nuomos nuvertėjimas
Nurodo naudojimo teise valdomo turto perkėlimo balanso sumažinimą. Nustatykite nuvertėjimo sumą, operacijos datą ir likusius laikotarpius. Likęs naudojimo teise valdomas turtas bus amortizuotas tiesioginio proporcingumo pagrindu. Nuomos nuvertėjimo logika atsižvelgia į turto perkėlimo vertę, kuri yra turto nusidėvėjimo grafike.  

|     Tipas                                          |     Debetas                             |     Kreditas                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   IFRS ir JAV GAAP nuvertėjimo įrašas           |  Nuvertėjimo išlaidos                   |    Naudojimo teise valdomas turtas     |

>[!NOTE]
> Jei nuoma yra susieta su ilgalaikiu turtu, nuomos nuvertėjimas turi būti užregistruotas naudojant Ilgalaikis turtas, nes turto nusidėvėjimas vykdomas modulyje Ilgalaikis turtas.

**Dvi valiutos** – nuomos operacijas galima registruoti kita valiuta nei apskaitos ir ataskaitų valiuta. Valiutos keitimo kursas apibrėžiamas modulyje Didžioji knyga pradžios dieną. Galite keisti valiutos kursus, nustatydami lauką **Fiksuotas kursas** į **Taip**, kai kuriate nuomą. Įvedus nuomos operacijas, pradinio pripažinimo ir vėlesnės nusidėvėjimo operacijos naudos valiutos kursą nuo pradžios datos. Vėlesnės mokėjimo ir palūkanų operacijos naudos dabartinį aktyvų valiutos kursą. 

## <a name="create-an-asset-lease"></a>Turto nuomos kūrimas
Norėdami sukurti naują nuomą, atlikite toliau nurodytus veiksmus. 

1. Norėdami naudoti funkciją **Turto nuoma**, turite įjungti ją darbo srityje **Funkcijų valdymas**. Darbo srityje **Funkcijų valdymas** pasirinkite **Visi**, kad visos funkcijos būtų pateiktos puslapyje. Pasirinkite **Turto nuoma** ir tada pasirinkite **Įjungti dabar**.
2. Eikite į **Turto nuoma > Bendra > Nuomos suvestinė**. „FastTab“ **Bendra** užpildykite reikiamus laukus. 
   - **Nuomos informacija**
   - **Turto naudingo naudojimo laikas (mėnesiais)**
   - **Nuomos grupė**
   - **Apskaičiuota skolinimosi palūkanų norma (%)**
   - **Sujungimo intervalas**
   - **Anuiteto tipas**
   - **Valiuta**
   - **Pradžios data**

3. Pereikite prie „FastTab” **Mokėjimo grafiko eilutės** ir įveskite mokėjimo eilutę, tada pasirinkite **Kurti grafikus**.

4. Pasirinkite **Knygos**. 

5. Pereikite prie „FastTab” **Bendra**. Apskaičiuojamas **pradinis naudojimo teise valdomas turtas** ir **nuomos įsipareigojimas**. 

6. Pereikite į „FastTab” **Nuomos klasifikacijos testas**, kad patikrintumėte vertę, esančią lauke **Nuomos tipas**. 

   Automatinis **nuomos tipas** klasifikuojamas pagal kriterijus, kurie apibrėžti puslapyje **Knygos**.

7.  Eikite į **Mokėjimo grafikas** dalyje **Funkcija**.  

   Puslapyje **Mokėjimo grafikas** pateikiami būsimi nuomos ID mokesčių grafikai. Pasirinkite **Patvirtinti grafiką**, kad būtų galima registruoti **pradinio pripažinimo** operacijas. 

[![Pradinio pripažinimo funkcija.](./media/overview-13.png)](./media/overview-13.png)

8. Pasirinkite **Pradinis pripažinimas**, norėdami sukurti pradinio pripažinimo žurnalą. 

9. Pasirinkite **Turto nuomos žurnalai**, norėdami užregistruoti pradinio pripažinimo operaciją. 

   Iš mokėjimo grafiko galite atidaryti išsamų puslapį, kuriame pateikiamos naudojimo teise valdomo turto operacijos. 
 
   **Nuomos įsipareigojimo amortizacijos grafike** nurodoma apskaičiuota kiekvieno laikotarpio palūkanų suma.
   
10. Sukurkite žurnalą ir eikite į **Turto nuomos žurnalai**. **Nuomos įsipareigojimo amortizacijos grafikas** taip pat nurodomas palūkanų operacijose.

   Puslapyje **Turto nusidėvėjimo grafikas** nurodomos pasirinkto nuomos ID nusidėvėjimo operacijos. 

   [![Puslapis Naudojimo teise valdomo turto operacijos.](./media/overview-20.png)](./media/overview-20.png)

   Puslapis **Naudojimo teise valdomo turto operacijos** pateikia pradinį pripažinimą, sukauptą nusidėvėjimą ir turto balansą. 

   Puslapis **Nuomos įsipareigojimo operacijos** nurodo pradinį pripažinimą, nuomos palūkanų mokesčius, nuomos mokesčius ir nuomos įsipareigojimo balansą. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
