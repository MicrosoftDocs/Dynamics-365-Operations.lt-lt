---
title: Atsargų registravimas
description: Šioje temoje paaiškinamas skirtukas Atsargų registravimas atsargų registravimo šablono puslapyje.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 464ffccd658003271b517038f430914fd5d8d50e
ms.sourcegitcommit: 6744cc2971047e3e568100eae338885104c38294
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/20/2022
ms.locfileid: "8783332"
---
# <a name="inventory-posting"></a>Atsargų registravimas

Atsargų **skirtukas**, kuris yra **atsargų registravimo šablonų** puslapyje, naudojamas atsargų operacijų registravimui DK valdyti. Atsargų operacijos yra operacijos, kurios nėra sukurtos iš pardavimo užsakymų, pirkimo užsakymų ar gamybos užsakymų. Jie automatiškai registruoja faktinius ir finansinius atsargų atnaujinimus vienu metu. Viena išimtis – perkėlimo užsakymai, kurie atskiria faktinius ir finansinius atnaujinimus jums siųsti ir gauti atsargas.

Toliau pateikiamoje lentelėje pateikiami kai kurie atsargų operacijų pavyzdžiai.

| Operacijos tipas | Gavimas arba išdavimas | Faktinis registravimas, finansinis registravimas arba abu | Aprašymas |
|---|---|---|---|
| Judėjimas | Abu | Abu | <p>Perkėlimo žurnalas yra atsargų žurnalas, kurį galite naudoti atsargai pridėti arba pašalinti. Tai veikia kaip atsargų koregavimo žurnalas. Tačiau vienas rakto skirtumas yra tas, kad nurodyta pagrindinė sąskaita, kuri kompensuoja įrašą.</p><p>Perkėlimo žurnalas įveda pradžios balansus ir vienų išjungimo koregavimus, į kuriuos reikia įrašyti išlaidas. Pavyzdžiui, jis naudojamas, kai pašalinamos pardavimo pavyzdžio atsargos.</p><p>Kai žurnalas užregistruojamas, faktiniai ir finansiniai atnaujinimai įvyksta vienu metu.</p><p>Teigiami kiekiai žurnalo eilutėse reiškia gavimus, o neigiami kiekiai reiškia gavimus.</p> |
| Atsargų koregavimas | Abu | Abu | Norint pridėti arba pašalinti atsargas, naudojamas atsargų koregavimo žurnalas. Tai neleidžia pasirinkti korespondentinės sąskaitos. DK įrašui atnaujinti naudojamos tik tos **sąskaitos**, kurios yra nurodytos atsargų registravimo šablono puslapyje. |
| Perkėlimas (žurnalas) | Abu | Abu | <p>Perkėlimo žurnalas naudojamas atsargoms perkelti iš vienos vietos į kitą (naudojant saugojimo dimensijas). Ji atnaujina atsargų operacijos produkto informaciją naujomis produkto arba sekimo dimensijomis.</p><p>Perkėlimo žurnalas sukuria vieną prekės judėjimo eilutę. Atsargų dimensijų laukuose Nuo ir Iki yra ši eilutė. Kiekviena perkėlimo žurnalo eilutė sukuria dvi atsargų operacijas. Sukuriama viena operacija atsargų dimensijoms Iš. Jis nurodo išdavimą ir turi neigiamą kiekį. Sukuriama kita atsargų dimensijų "Iki" operacija. Jis rodo gavimą ir turi teigiamą kiekį.</p><p>Perkėlimo žurnalai gali nesukurti kvito, jei atsargų judėjimas laikomas nefinansinis perkėlimas. Atsargų dimensijos, kurios skiriasi nuo ir **Iki** **·** **vertėmis, nepažymėtos pasirinktimi Finansinės atsargos saugojimo dimensijų grupėje arba Sekimo dimensijų grupės** puslapyje. Pavyzdžiui, jei **·** **pasirinktis** Finansinės atsargos nepažymėta vietos dimensijoje, o atsargas perkeliate iš vienos vietos į kitą, toje pačioje teritorijoje ir sandėlyje, kvitas nesukurtas.</p><p>Perkėlimo žurnalai skiriasi nuo perkėlimo užsakymų, nes nėra perkėlimo dokumentų. Atnaujinimas atliekamas vienoje operacijoje registruojant žurnalą. Priešingai, perkėlimo užsakymas gali generuoti paėmimo ir siuntimo dokumentus ir operacijai apdoroti reikalauja dviejų atnaujinimų.</p> |
| Perkėlimo užsakymo siuntimas | Problema | Abu | <p>Kai kuriate naują perkėlimo užsakymą, kiekvienas eilutės ir atsargų dimensijos derinys turi dvi atsargų operacijas: vieną perkėlimo užsakymo siuntai ir vieną perkėlimo užsakymo gavimui. Kai siuntimo užsakymą atnaujinate, atnaujinamos dvi atsargų operacijos ir sukuriamos dvi papildomos prekių tranzito atsargų operacijos, iš kurių iš viso yra keturios atsargų operacijos.</p><ol><li>Pirmoji atsargų operacija naudojama prekei pašalinti iš šaltinio sandėlio ir vietos. Šios operacijos išdavimo būsena yra **Parduota,** kad būtų galima nurodyti, jog prekė sandėlyje nebepalaikoma.</li><li>Antra atsargų operacija naudojama prekei įtraukti į tranzito sandėlį, pasirinktą sandėliui, iš kurios perkeliama prekė. Šios operacijos gavimo būsena yra **Nupirkta**.</li><li>Trečioji atsargų operacija yra skirta perkelti iš tranzito sandėlio į paskirties sandėlį. Šios operacijos išdavimo būsena yra Faktiškai **rezervuota**. Ši būsena užtikrina, kad kito proceso metu prekės negalima suvartoti, kol ji vis dar yra tranzito metu.</li><li>Ketvirta atsargų operacija yra skirta prekėms į paskirties sandėlį gauti. Šios operacijos gavimo būsena yra **Užsakyta**.</li></ol> |
| Perkėlimo užsakymo gavimas | Gavimas | Abu | Kai perkėlimo užsakymas gaunamas į paskirties sandėlį, atsargų operacijos, kuri yra tranzito sandėlyje, atsargų būsena (ankstesniame pavyzdyje pateiktas numeris 3) **atnaujinama** į Parduota, **o paskirties sandėlio atsargų būsena atnaujinama į Nupirkta**. |
| Komplektavimo specifikacijos | Abu | Abu | Galite naudoti komplektavimo specifikacijos (KS) žurnalą, norėdami produktą pranešti kaip baigtą ir naudoti žaliavas, suvartotas proceso metu, nenaudojant gamybos užsakymo. KS žurnale paprastai yra bent viena baigtos prekės teigiama eilutė ir viena ar daugiau suvartojamų žaliavų neigiamų eilučių. Baigtos prekės eilutė yra gavimas į atsargas, o neigiamos eilutės – žaliavų atsargų gavimas. Kuriant KS žurnalą, pirmoji eilutė yra KS antraštė, o kitos pridėtos eilutės yra KS eilutės. |
| Atsargų nuosavybės pakeitimas | Abu | Abu | Atsargų nuosavybės pakeitimų žurnalas naudojamas norint pakeisti tiekėjo į jūsų organizaciją siunčiamų atsargų nuosavybę. Atsargų nuosavybės keitimo žurnalai yra panašūs į atsargų perkėlimo žurnalus, nes dvi atsargų operacijos susijusios su kiekviena eilutės ir atsargų dimensijų kombinacija. Viena atsargų operacija pašalina atsargas iš tiekėjo **nuosavybės** dimensijoje, o kita įtraukia prekę į juridinio subjekto nuosavybės **dimensiją**. |
| Prekių gavimas | Gavimas | Faktinis | Prekių gavimo žurnalas naudojamas atsargų gavimo būsenai atnaujinti į **Užregistruota**. Paprastai naudojama prekių pirkimo užsakymo gavimui ir pardavimo užsakymų grąžinimams. |
| Gamybos įvestis | Gavimas | Faktinis | Gamybos įvesties žurnalas yra panašus į prekių gavimo žurnalą. Gamybos įvestis naudojama norint gauti baigtas prekes iš gamybos užsakymo sandėlyje. Užregistravę žurnalą, atsargų operacijos būsena atnaujinama į **Užregistruota**. |
| Inventorizacija | Abu | Abu | Inventorizacijos žurnalas naudojamas norint įrašyti prekių kiekį, kuris buvo inventorizacijos pagal tam tikrą atsargų dimensijų derinį. Atsargų operacijos sukuriamos, kai žurnalo eilutėje yra inventorizacijos skirtumas. Eilutė, kurios inventorizacijos kiekis didesnis, lemia atsargų gavimą. Eilutė, kurios inventorizacijos kiekis mažesnis, lemia atsargų išdavimą. Eilutės, kuriose inventorintas kiekis atitinka numatomą kiekį, neturi atsargų operacijų. |
| Skaičiavimas pagal žymę | Netaikoma | Netaikoma | Žymių inventorizacijos žurnalas naudojamas atsargų žymėms, kurios priskirtos ir naudojamos visu atsargų inventorizacija, sekti. Galite naudoti žurnalą žymės numeriui tam tikrai prekės ir atsargų dimensijos kombinacijai priskirti ir tos žymės būsenai visų atsargų metu sekti. Inventorizacijos pagal žymę žurnalai nesukuria atsargų operacijų. |
| Kokybės užsakymai | Problema | Faktinis | <p>Kokybės užsakymas naudojamas įrašyti tam pateiktos atsargų partijos bandymo rezultatus. Kiekvienas kokybės užsakymas yra susijęs su esama atsargų operacija arba atsargų operacijos dalimi.</p><p>Kokybės užsakymas generuos naują atsargų operaciją dviem situacijomis:</p><ul><li>Kokybės užsakymas pažymėtas kaip **Ardomasis tikrinimas** skirtuke **Bendra**.</li><li>Kokybės užsakymas pažymimas kaip Sulaikytas **, kai skirtuke** **Bendra nepavyksta patikrinti**, o tikrinimo rezultatai nepavyksta. Šiuo atveju sukuriamos dvi atsargų operacijos. Viena atsargų operacija pašalina prekę iš originalios atsargų dimensijų kombinacijos ir vietos, o kita įtraukia prekę į sulaikymo sandėlį.</li></ul> |
| Sulaikymo užsakymai | Abu | Abu | <p>Sulaikymo užsakymų atsargų operacijos yra panašios į perkėlimo užsakymą. Sulaikymo sandėlis naudojamas atsargai sekti. Yra dvi gavimo operacijos ir dvi išdavimo operacijos.</p><p>Kai pirmą kartą kuriate užsakymą, sukuriamos dvi operacijos. Gavimo operacijos būsena yra Užsakytas **sulaikymo** sandėliui, kuris susietas su sandėliu, kuriame yra prekė. Išdavimo operacijos būsena yra Užsakyta **sandėlyje**, kuriame saugoma prekė.</p><p>Paleidus sulaikymo užsakymą, sukuriamos dvi papildomos operacijos ir atnaujinamos esamos operacijos. Sulaikymo sandėlio gavimo operacijos **būsena atnaujinama į Gauta**, o saugojimo sandėlio išdavimo operacijos būsena atnaujinama į **Išskaičiuota**.</p><p>Dvi naujos operacijos naudojamos nurodyti įvykių perkėlimą atgal į saugojimo sandėlį. Gavimo operacijos būsena saugojimo sandėliui **yra** Užsakyta, **o išdavimo operacijos būsena sulaikymo sandėlyje yra** Faktiškai rezervuota.</p><p>Kai pranešate, kad sulaikymo užsakymas baigtas, ši operacija rodo fizinį sulaikymo užsakymo atnaujinimą. Gavimo būsena saugojimo sandėlyje atnaujinama į **Gauta**.</p><p>Kai pabaigiate sulaikymo užsakymą, ši operacija rodo finansinį sulaikymo užsakymo atnaujinimą. Išdavimo operacijų būsena atnaujinama į **Parduota**, o gavimo operacijų būsena atnaujinama į **Nupirkta**.</p><p>Taip pat galite nurašti sulaikymo užsakymą. Ši operacija pašalina prekę iš atsargų. Nurašant sulaikymo užsakymą, lieka tik trys operacijos. Saugojimo sandėlio gavimo operacija pašalinama, o likusios gavimo operacijos būsena atnaujinama į **Nupirkta**. Dviejų išdavimo operacijų būsena atnaujinama į **Parduota**. Ši operacija yra faktinis ir finansinis užsakymo atnaujinimas.</p> |

## <a name="fixed-receipt-price-posting"></a>Fiksuotos gavimo kainos registravimas

Fiksuota gavimo kaina leidžia produktui naudoti standartinę savikainą. Tai yra standartinės savikainos **pasirinktis** prekių **modelių grupės** puslapyje. Pagrindinis skirtumas, kai naudojate fiksuotą gavimo kainą, yra tas, kad dabar sukonfigūruota savikaina bus naudojama prekei, užregistrėjus gavimą į atsargas. Fiksuotos gavimo kainos išlaidų perkainojimo proceso nėra. Kai užregistruojamas finansinis atnaujinimas, registravimo metu naudojama esama savikaina. Jei gavimo metu naudojama savikaina ir SF skiriasi, nuokrypis bus registruojamas fiksuotos gavimo kainos pelno ir nuostolio sąskaitose.

Norėdami pasirinktinai naudoti produkto fiksuotą gavimo kainą, turite atlikti šią konfigūraciją:

- Prekių modelių **grupės puslapyje pažymėkite** žymės **langelį Registruoti** faktines atsargas prekei, kuri pasirinkta atsargų operacijos eilutėje.
- Prekių modelių **grupės puslapyje pažymėkite** žymės langelį Fiksuota **gavimo** kaina.
- Atsargų registravimo šablono puslapyje nurodykite šių registravimo **tipų pagrindines** sąskaitas:

    - Fiksuotos gavimo kainos pelnas
    - Fiksuotos gavimo kainos nuostolis

Daugiau informacijos ieškokite Fiksuota [gavimo kaina](/supply-chain/cost-management/fixed-receipt-price.md).

## <a name="catch-weight-posting"></a>Esamo svorio registravimas

Esamo svorio produktai dažnai naudojami pramonės šakose, pvz., maisto pramonėje, kur produktai gali šiek tiek skirtis pagal svorį, dydį arba abu. Produktai su esamu svoriu naudoja du matavimo vienetus: atsargų vienetą ir esamo svorio vienetą. Sandėliui patenkant į atsargas naudojamas atsargų svoris gali skirtis nuo svorio, kai atsargos išrašomos iš sandėlio. Esamo svorio produkto apdorojimas koreguoja atsargas.

Jei esamo svorio nuokrypis yra, skirtumai registruojami sąskaitose, **·** **·** **kurios nurodytos laukuose Esamo svorio nuostolis ir Esamo svorio pelnas, atsargų registravimo šablono** puslapyje. Paprastai ta pati pagrindinė sąskaita nurodoma abiejuose laukuose.

Toliau pateikiamoje lentelėje pateikiami numatytųjų registravimo tipų pavyzdžiai, įtraukti pagrindinių sąskaitų pavyzdžiai ir aprašymai.

- Ar rodyti debetą/kreditą? Stulpelis nurodo, ar operacija paprastai yra debeto, ar kreditas. Kai kuriais atvejais operacija gali registruoti debetus arba kreditus.
- Stulpelyje Kliringo sąskaita nurodoma, kad registravimo tipas yra tarpuskaitos sąskaita. Kitaip tariant, šioje sąskaitoje užregistruota suma automatiškai atšaukiama, kai užregistruojama vėlesnė operacija.
- Stulpelis P/F nurodo registravimo tipą. "P" rodo faktiškai užregistravimą, o "F" reiškia finansinį registravimą.
- Stulpelyje Sekti nurodoma, ar registravimo tipo pagrindinė sąskaita paprastai yra ta pati, kaip ir kito registravimo tipo pagrindinė sąskaita. Tiksliau nurodo registravimo tipą, kuris paprastai naudojamas registruojant.

> [!NOTE]
> Lentelėje pagrindinės sąskaitos ir pagrindinės sąskaitos pavadinimai yra pasiūlymai. Rekomenduojame dirbti su savo buhalteriu, kad nustatytumėte geriausią konfigūraciją savo verslo poreikiams.

| Registravimo tipas | Pagrindinės sąskaitos pavyzdys | Pagrindinės sąskaitos pavadinimo pavyzdys | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | P / F | Atlikite | Aprašymas |
|---|---|---|---|---|---|---|---|---|
| Svėrimo nuostolių sąskaita | 510520 | Atsargų koregavimas | Išlaidos | | Ne | Abu | Svėrimo pelno sąskaita | Ši sąskaita naudojama, kai registruojate atsargų operaciją, kurios esamo svorio suma yra mažesnė. |
| Svėrimo pelno sąskaita | 510520 | Atsargų koregavimas | Išlaidos | | Ne | Abu | Svėrimo nuostolių sąskaita | Ši sąskaita naudojama, kai registruojate atsargų operaciją, kurios esamo svorio suma didesnė. |

Daugiau informacijos apie esamo svorio produktus ieškokite informacijos apie esamo [svorio prekes ir esamo](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.md)[svorio produkto apdorojimą naudojant sandėlio valdymą](/supply-chain/warehousing/catch-weight-processing.md).

## <a name="inventory-to-fixed-asset-transfer-posting"></a>Atsargų perkėlimo į ilgalaikį turtą registravimas

Atsargos į ilgalaikio turto žurnalą (**ilgalaikio turto** \> **žurnalai Atsargos į ilgalaikio turto žurnalą) naudojamos prekėms** \> **iš** atsargų perkelti ir konvertuoti į ilgalaikį turtą. Norėdami daugiau informacijos žr. [Ilgalaikio turto integravimas](/fixed-assets/fixed-asset-integration.md).

Toliau pateikiamoje lentelėje pateikiami numatytųjų registravimo tipų pavyzdžiai, įtraukti pagrindinių sąskaitų pavyzdžiai ir aprašymai.

- Ar rodyti debetą/kreditą? Stulpelis nurodo, ar operacija paprastai yra debeto, ar kreditas. Kai kuriais atvejais operacija gali registruoti debetus arba kreditus.
- Stulpelyje Kliringo sąskaita nurodoma, kad registravimo tipas yra tarpuskaitos sąskaita. Kitaip tariant, šioje sąskaitoje užregistruota suma automatiškai atšaukiama, kai užregistruojama vėlesnė operacija.
- Stulpelis P/F nurodo registravimo tipą. "P" rodo faktiškai užregistravimą, o "F" reiškia finansinį registravimą.
- Stulpelyje Sekti nurodoma, ar registravimo tipo pagrindinė sąskaita paprastai yra ta pati, kaip ir kito registravimo tipo pagrindinė sąskaita. Tiksliau nurodo registravimo tipą, kuris paprastai naudojamas registruojant.

> [!NOTE]
> Lentelėje pagrindinės sąskaitos ir pagrindinės sąskaitos pavadinimai yra pasiūlymai. Rekomenduojame dirbti su savo buhalteriu, kad nustatytumėte geriausią konfigūraciją savo verslo poreikiams.

| Registravimo tipas | Pagrindinės sąskaitos pavyzdys | Pagrindinės sąskaitos pavadinimo pavyzdys | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | P / F | Atlikite | Aprašymas |
|---|---|---|---|---|---|---|---|---|
| Ilgalaikio turto išdavimas | 180100 | Materialusis ilgalaikis turtas | Turtas | Kreditas | Ne | Abu | Netaikoma | Ši sąskaita naudojama, kai registruojate atsargas ilgalaikio turto žurnale, norėdami pašalinti prekę iš atsargų ir konvertuoti ją į ilgalaikį turtą. |

## <a name="moving-average-posting"></a>Slankusis vidurkio registravimas

Slankusis vidurkis yra nuolatinis įkainojimo metodas, pagrįstas vidurkio principu. Atsargų problemų išlaidos nesikeičia kai pirkimo išlaidos. Skirtumas kapitalizuojamas ir pagrindžiamas proporcingu skaičiavimu. Likusi suma įtraukiama į išlaidų sąskaitą.

Toliau pateikiamoje lentelėje pateikiami numatytųjų registravimo tipų, kurių pagrindinės sąskaitos ir aprašymai yra pavyzdiniai, pavyzdžiai.

- Ar rodyti debetą/kreditą? Stulpelis nurodo, ar operacija paprastai yra debeto, ar kreditas. Kai kuriais atvejais operacija gali registruoti debetus arba kreditus.
- Stulpelyje Kliringo sąskaita nurodoma, kad registravimo tipas yra tarpuskaitos sąskaita. Kitaip tariant, šioje sąskaitoje užregistruota suma automatiškai atšaukiama, kai užregistruojama vėlesnė operacija.
- Stulpelis P/F nurodo registravimo tipą. "P" rodo faktiškai užregistravimą, o "F" reiškia finansinį registravimą.
- Stulpelyje Sekti nurodoma, ar registravimo tipo pagrindinė sąskaita paprastai yra ta pati, kaip ir kito registravimo tipo pagrindinė sąskaita. Tiksliau nurodo registravimo tipą, kuris paprastai naudojamas registruojant.

> [!NOTE]
> Lentelėje pagrindinės sąskaitos ir pagrindinės sąskaitos pavadinimai yra pasiūlymai. Rekomenduojame dirbti su savo buhalteriu, kad nustatytumėte geriausią konfigūraciją savo verslo poreikiams.

| Registravimo tipas | Pagrindinės sąskaitos pavyzdys | Pagrindinės sąskaitos pavadinimo pavyzdys | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | P / F | Atlikite | Aprašymas |
|---|---|---|---|---|---|---|---|---|
| Slankiojo vidurkio kainų skirtumas | 510600 | Slankusis vidutinės kainos skirtumas | Išlaidos | Abu | Ne | Abu | Netaikoma | Ši sąskaita naudojama, kai yra skirtumas tarp gavimo ir SF išlaidų. |
| Slankiojo vidurkio pakartotinis įvertinimas | 510610 | Perkeliamas vidutinis perkainojimas | Išlaidos | Abu | Ne | Abu | Netaikoma | Ši sąskaita naudojama koreguojant produkto slankusį vidurkį |

## <a name="sample-posting-profile-configuration"></a>Registravimo šablono konfigūracijos pavyzdys

Toliau pateikiamoje lentelėje pateikiami numatytųjų registravimo tipų, kurių pagrindinės sąskaitos ir aprašymai yra pavyzdiniai, pavyzdžiai.

| Registravimo tipas | Pagrindinės sąskaitos pavyzdys | Pagrindinės sąskaitos pavadinimo pavyzdys | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | P / F | Atlikite | Aprašymas |
|---|---|---|---|---|---|---|---|---|
| Atsargų išdavimas | 140100 | Medžiagų atsargos | Turtas | Kreditas | Ne | Abu | Atsargų gavimas | Ši sąskaita naudojama, kai užregistruota atsargų operacija yra išdavimas (neigiamas kiekis) ir nėra susijęs su pardavimu, pirkimu ar gamyba. Šios sąskaitos korespondentinė sąskaita yra atsargų išlaidos, nuostolių sąskaita. Ši sąskaita paprastai pateikia atsargas balanse. |
| Atsargų išlaidos, nuostoliai | 510100 | Atsargų pelnas ir nuostoliai | Išlaidos | Debetas | Ne | Abu | Atsargų išlaidos, pelnas | Ši sąskaita naudojama, kai užregistruota atsargų operacija yra išdavimas (neigiamas kiekis) ir nėra susijęs su pardavimu, pirkimu ar gamyba. Šios sąskaitos korespondentinė sąskaita yra atsargų išdavimo sąskaita. |
| Atsargų gavimas | 140100 | Medžiagų atsargos | Turtas | Debetas | Ne | Abu | Atsargų išdavimas | Ši sąskaita naudojama, kai užregistruota atsargų operacija yra gavimas (teigiamas kiekis) ir nėra susijęs su pardavimu, pirkimu ar gamyba. Šios sąskaitos korespondentinė sąskaita yra atsargų išlaidos, pelno sąskaita. Ši sąskaita paprastai pateikia atsargas balanse. |
| Atsargų išlaidos, pelnas | 510100 | Atsargų pelnas ir nuostoliai | Išlaidos | Kreditas | Ne | Abu | Atsargų išlaidos, nuostoliai | Ši sąskaita naudojama, kai užregistruota atsargų operacija yra gavimas (teigiamas kiekis) ir nėra susijęs su pardavimu, pirkimu ar gamyba. Šios sąskaitos korespondentinė sąskaita yra atsargų gavimo sąskaita. |
| Mokėtinos sumos tarp susijusių vienetų | 231500 | Susiję susiję su mokėtina suma | Įsipareigojimai | Debetas | Ne | Abu | | Ši sąskaita naudojama, kai atsargos perkeliamos iš vienos atsargų dimensijos į kitą, pvz., teritorijose, o prekių išlaidos svetainėse skiriasi. |
| Gautinos sumos tarp susijusių vienetų | 131500 | Gautinos sumos tarp susiję vienetų | Turtas | Kreditas | Ne | Abu | | Ši sąskaita naudojama, kai atsargos perkeliamos iš vienos atsargų dimensijos į kitą, pvz., teritorijose, o prekių išlaidos svetainėse skiriasi. |
