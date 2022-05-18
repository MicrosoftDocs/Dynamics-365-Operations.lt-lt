---
title: Registravimo lapų tvarkymas
description: Ši tema aprašo, kaip dirbti su registravimo lapais. Registravimo lapas įprastai susideda iš vieno tiekėjo vienos siuntos prekių vienam objektui ar įmonei. Viename registracijos lape esančios prekės gali būti viename konteineryje arba gali būti paskirstytos keliuose konteineriuose.
author: Weijiesa
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMFolioTable, ITMFolioTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f908ae3c150a09af61bb0ee97469619744cd1079
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695308"
---
# <a name="manage-folios"></a>Registravimo lapų tvarkymas

[!include [banner](../../includes/banner.md)]

Registravimo lapai dažnai nustatomi pagal muitinės taisykles. Jie gali susidėti iš vieno tiekėjo vienos siuntos prekių vienam objektui ar įmonei. Prekės registracijose valdomos viename konteineryje.

Norėdami atidaryti puslapį **Visi registravimo lapai**, eikite į **Įkeltos išlaidos \> Registravimo lapai \> Visi registravimo lapai**. Šiame puslapyje rodomas visų dabartinių registravimo lapų sąrašas. Veiksmų srities mygtukus galite naudoti norėdami kurti, naikinti ir dirbti su registravimo lapais. Iš sąrašo pasirinkite bet kurį registravimo lapą peržiūrėti jo išsamiai informacijai **Registravimo lapų** puslapyje.

## <a name="action-pane"></a>Veiksmų sritis

Veiksmų srityje, esančioje puslapiuose **Visi registravimo lapai** ir **Registravimo lapai**, pateikiami mygtukai, leidžiantys dirbti su pasirinktu registravimo lapu. Kiekvienas mygtukas atlieka vieną veiksmą. Veiksmų srityje taip pat yra skirtukai, iš kurių kiekvienas pateikia susijusių mygtukų rinkinį. Išskyrus atvejus, kai pažymėta, visi toliau esančiuose poskyriuose aprašyti mygtukai yra pasiekiami tiek sąrašo rodinyje (tai yra, **Visų registravimo lapų** puslapyje), tiek išsamiame rodinyje (tai yra, **Registravimo lapų** puslapyje).

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Mygtukai, rodomi tiesiogiai veiksmų srityje

Toliau pateikta lentelė aprašo mygtukus, pasiekiamus tiesiogiai veiksmų srityje.

| Mygtukas | Aprašymas |
|---|---|
| Naujas | Sukuria registravimo lapą. |
| Panaikinti | Panaikina atidarytą arba pasirinktą registravimo lapą. |
| Reiso išlaidos | Atidarykite puslapį **Reiso išlaidos**, kuriame galite peržiūrėti ir pridėti registravimo lapo lygio išlaidas prie visų reiso prekių. Kai registravimo išlaidos į reisą įtraukiamos rankiniu būdu, jos automatiškai įtraukiamos į išlaidų užklausos puslapį ir priskiriamos kiekvienai prekei pagal metodą, nurodytą **Reiso išlaidų** puslapyje. |

### <a name="buttons-on-the-manage-tab"></a>Mygtukai, esantys skirtuke Valdymas

Toliau pateikta lentelė aprašo mygtukus, pasiekiamus veiksmų srities skirtuke **Valdyti**.

| Mygtukas | Aprašymas |
|---|---|
| Užregistruoti gavimo kvitų sąrašą | Registruoja visų pirkimo užsakymo eilučių gavimo kvitų sąrašą registravimo lape. Jei vykdomos kelių įmonių siuntos, kiekvienai įmonei atidaromas naujas gavimo kvitų sąrašo registravimo dialogo langas. |
| Registruoti produkto gavimo kvitą | Registruoja visų pirkimo užsakymo eilučių produktų gavimo kvitus registravimo lape. Jei vykdomi kelių įmonių reisai, kiekvienai įmonei atidaromas naujas produktų gavimo kvitų registravimo dialogo langas. |
| Registruoti SF | Registruoja visų pirkimo užsakymo eilučių sąskaitą faktūrą registravimo lape. Jei vykdomi kelių įmonių reisai, kiekvienai įmonei atidaromas naujas sąskaitos faktūros registravimo dialogo langas. |
| Siuntimo perkėlimo užsakymas | Registruoja perkėlimo užsakymą visoms perkėlimo užsakymo eilutėms, kurios yra susijusios su dabartiniu susijusios siuntos registravimo lapu. |
| Gauti perkėlimo užsakymą | Registruoja perkėlimo užsakymo gavimo kvitą visoms perkėlimo užsakymo eilutėms, kurios yra susijusios su dabartiniu susijusios siuntos registravimo lapu. |
| Gauti tranzito prekes | Gauna visas tranzite esančias užsakymo eilutes registravimo lape. |
| Gauti dokumentai | Atnaujinkite parametro **Gauti dokumentai** parinktį į *Taip*. Galite naudoti šį mygtuką, norėdami užrakinti prekę ir (arba) pirkimo eilutę, kad jos nebūtų galima atnaujinti. |
| Rasti automatines išlaidas | Suranda aktualias reiso išlaidas. Jei šios išlaidos jau buvo surastos arba atnaujintos, gausite šį pranešimą: „Yra išlaidų eilučių, kurių SF neišrašytos. Ar norite perrašyti?” Atkreipkite dėmesį, kad reiso išlaidos, kurios pridėtos prie registravimo lapo, ir kurioms išrašytos sąskaitos faktūros, nebus perrašytos. |
| Kurti pristatymo žurnalą | Generuoja gavimo žurnalą organizacijoms, naudojant išplėstines sandėlio funkcijas. Galite pasirinkti **Inicijuoti kiekį** (rekomenduojama), **Kurti iš tranzito prekių** ir (arba) **Kurti iš pirkimo užsakymų**. Paskutiniai du pasirinkimai priklauso nuo to, ar naudojamas tranzito prekių apdorojimas. |
| Kaupti išlaidas | Kaupia išlaidas, kai nurodyta išlaidų tipo debeto didžiosios knygos sąskaita. Šis mygtukas paprastai naudojamas, kai atsargos gabenamos tranzitu arba kai prekės yra gautos ir išrašytos jų SF. |

### <a name="buttons-on-the-general-tab"></a>Mygtukai, esantys skirtuke Bendra

Toliau pateikta lentelė aprašo mygtukus, pasiekiamus veiksmų srities skirtuke **Bendra**.

| Mygtukas | Aprašymas |
|---|---|
| Gavimo kvitų sąrašas | Registruoja visų pirkimo užsakymo eilučių gavimo kvitų sąrašą registravimo lape. Jei vykdomi kelių įmonių reisai, kiekvienai įmonei atidaromas naujas gavimo kvitų sąrašo registravimo dialogo langas. |
| Produkto gavimo kvitas | Peržiūrėkite produkto gavimo kvito įrašą, jeigu jis panaudotas. |
| Prekių gavimas | Peržiūrėkite prekių gavimo žurnalą, jei jis naudojamas. |
| Išlaidų užklausa | Atidarykite išlaidų užklausos puslapį, jei norite peržiūrėti visas reiso išlaidas, įskaitant gabenimo konteinerį, registravimo lapą ir pirkimo užsakymą. Galite koreguoti tikslų puslapio rodinį naudodami veiksmą Peržiūrėti. Išlaidų užklausos puslapyje galite peržiūrėti bet kurią iš sričių, taip pat prekės ir išlaidų tipo kodus. Pašalinę šias prekes, galite koreguoti puslapį sugrupuodami kartu išlaidas. Ši galimybė gali būti naudinga, jei naudojate dydžius ir spalvas. Galite pakeisti puslapyje rodomas dimensijas. Puslapyje **Išlaidos** rodomi tik tie išlaidų tipo kodai, kurių įrašas **„Dr”**, esantis **Registravimo** skirtuke, nustatytas kaip *Prekė*. |

## <a name="header-view"></a>Antraštės rodinys

Norėdami atidaryti rodinį **Antraštė**, atidarykite registravimo lapą ir jo antraštės viršutinėje dešinėje pusėje pasirinkite skirtuką **Antraštė**.

### <a name="settings-on-the-general-fasttab"></a>Parametrai, esantys Bendra „FastTab”

Toliau pateikiamoje lentelėje aprašomi laukai, galimi registravimo lapo rodinio **Antraštė** „FastTab” **Bendra**.

| Laukas | Aprašymas |
|---|---|
| Registravimo lapas | Registravimo lapo pavadinimas. Šis pavadinimas sugeneruojamas automatiškai, kai sukuriamas registravimo lapas.|
| Reisas | Reisas, susietas su registravimo lapu. |
| Muitinės tarpininkas | Registravimo lapui pasirenkamas muitinės tarpininkas. Muitinės tarpininkai apibrėžiami tiekėjo parametre. Jie įgalina automatiškai nustatyti sukurtas išlaidas. |
| Namų oro transporto važtaraštis / važtaraštis | Nurodykite registravimo lapui taikomą namų oro transporto važtaraštį arba važtaraštį. |
| Įmonė | Su registravimo lapu susietas juridinis subjektas (įmonė). |
| Krovinio kontrolinis numeris | Šis laukas naudojamas kai kurių šalių arba regionų muitinės padalinių. |
| Matavimas | Šis laukas įgalina patikslinti matavimus **Įkeltų išlaidų** modulyje. Matavimo vienetus dažnai naudoja organizacijos, kurios nežino atskirų prekių tūrio ar svorio, tačiau reikalauja tikslesnio paskirstymo, nei pateikia suma ar kiekis. Krovinių ekspeditorius pateiks svorį arba kubinį matavimo vienetą, o jūs galėsite pateikti jį prekės arba pirkimo užsakymo lygiu. Jį galima atnaujinti automatiškai, jei parametras yra pasirinktas arba įvestas rankiniu būdu. |
| Matavimo vienetas | Nurodytam matavimui taikomas vienetas. |
| Kartoninių dėžių skaičius | Kartoninių dėžių skaičius registravimo lape. Šis laukas gali būti atnaujinamas automatiškai, priklausomai nuo parametrų pasirinkimo. |
| Tiekėjo paskyra | Pasirinkite tiekėją, susijusį su registravimo lapu. Šis laukas naudojamas tik informaciniais tikslais. Jis neturi įtakos jokiai funkcijai. |
| Pavadinimas | Pasirinktos tiekėjo paskyros pavadinimas. |
| Pastabos | Įvesti bet kokią papildomą informaciją, susijusią su registravimo lapu. |
| Prekių aprašas | Pasirinkite prekių aprašą, kad padėtumėte identifikuoti registravimo lapą. Daugiau informacijos rasite [Prekių aprašas](shipping-information-setup.md#description-of-goods). |
| Vertinimo data | Šis laukas yra susijęs su muito mokesčio įrašo puslapiu. Modulis **Įkeltos išlaidos** naudos muitų valiutos kursą datai, kurią nustatote čia. Numatytoji reikšmė yra data, įvesta muito mokesčio įrašo puslapyje. |
| Muitinės ID | Įveskite muitinės ID. Šį ID pateikia šalių ar regionų muitinės padaliniai. |
| Tarifo kodas | Įveskite tarifo kodą, kuris bus susietas su registravimo lapu. Šio kodo paprastai reikalauja (ir jį nustato) šalis arba regionas, į kurį siunčiate. |

### <a name="settings-on-the-delivery-fasttab"></a>„FastTab” Pristatymas parametrai

Toliau pateikiamoje lentelėje aprašomi parametrai, galimi registravimo lapo rodinio **Antraštė** „FastTab” **Pristatymas**.

| Laukas | Aprašymas |
|---|---|
| Registravimo lapo data | Pasirinkite datą, kurią norite susieti su registravimo lapu. Numatytoji reikšmė yra reiso sukūrimo data. |
| ETA siuntimo uoste | Numatyta atvykimo laiko (ETA) į paskirties uostą („iki” uosto) data. |
| Numatoma pristatymo data | Įprastai, tai yra data, kada numatomas prekių atvykimas į sandėlį. Šis laukas nėra naudojamas, kai apskaičiuojama numatoma pristatymo data. (Vietoj jo naudojama sekimo kontrolės numatoma pristatymo data.) Norėdami nustatyti šį lauką, kad vertė atitiktų sekimo kontrolės numatomą pristatymo datą, naudokite [Sekimo kontrolės centrą](delivery-information-setup.md#tracking-control-center). |
| Gauti originalūs dokumentai | Originalių dokumentų gavimo data. |
| Patarė tarpininkas | Data, kada tarpininkui patarta. |
| Išsiųstas originalus važtaraštis | Pradinio važtaraščio išsiuntimo data. |
| Išleistos prekės | Prekių išleidimo data. |
| Kliento paskyrimas | Kliento paskyrimo data. |
| Pristatymas į sandėlį | Prekių pristatymo į sandėlį data. |
| Patikrinimo data | Patikrinimo data. |
| Pristatymo instrukcijos | Pristatymo instrukcijų gavimo data. |
| Kilmės uostas | Uostas, iš kurio išvyksta reisas. |
| Paskirties uostas | Uostas, į kurį atvyksta reisas. Gabenimo konteinerių paskirties uostai gali skirtis, nes laivas gali stoti keliuose uostuose. |

### <a name="settings-on-the-export-fasttab"></a>Parametrai, esantys Eksportavimo „FastTab”

Toliau pateikiamoje lentelėje aprašomi parametrai, galimi registravimo lapo rodinio **Antraštė** „FastTab” **Eksportavimas**.

| Laukas | Aprašymas |
|---|---|
| Eksportuotojas | Eksportuotoją galima saugoti registravimo lapuose. Tarptautinės prekybos atveju, jūs galite siųsti pirkimo užsakymą vienai įmonei, tačiau gauti prekes iš kitos įmonės. Muitinė reikalauja sekimo ir dokumentacijos. Eksportuotojo pavadinimas ir adresas gali būti saugomi čia. |
| Pavadinimas | Pasirinkto eksportuotojo pavadinimas. |

## <a name="lines-view"></a>Rodinys Eilutės

Norėdami atidaryti rodinį **Eilutės**, atidarykite registravimo lapą ir jo viršutinėje dešinėje pusėje pasirinkite skirtuką **Eilutės**.

### <a name="information-on-the-folio-fasttab"></a>Informacijos apie registravimo lapą „FastTab”

„FastTab” **Registravimo lapas**, esančiame rodinyje **Eilutės**, rodoma informaciją apie registracijos lapą. Didžioji dalis šios informacijos taip pat rodoma **Antraštės** rodinyje, kaip aprašyta anksčiau šioje temoje.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Informacija ir mygtukai, esantys „FastTab” Eilutės

„FastTab” **Eilutės**, esančiame rodinyje **Eilutės** rodoma išsami informacija apie kiekvieną pilną arba dalinę pirkimo užsakymo eilutę, įtrauktą į dabartinį registravimo lapą.

Toliau pateikta lentelė aprašo mygtukus, pasiekiamus „FastTab” **Eilutės**, esančiame **Eilučių** rodinyje.

| Mygtukas | Aprašymas |
|---|---|
| Šalinti | Pašalinti pasirinktą pirkimo užsakymo eilutę iš reiso. |
| Atsargos \> Operacijos | Peržiūrėkite pasirinktos pirkimo užsakymo eilutės atsargų operacijas. Atkreipkite dėmesį, kad jei naudojate tranzito prekes, rodomas tiek pradinis užsakymas, tiek tranzito prekių užsakymai. |
| Atsargos \> Rodyti dimensijas | Atidarykite dialogo langą, kuriame galite pasirinkti atsargų dimensijas, kurios pasirodo jūsų peržiūrimoms operacijoms. |
| Atnaujinti | Atnaujinkite informaciją, susijusią su pasirinktos pirkimo užsakymo eilutės suma, svoriu ar tūriu. |

### <a name="information-on-the-lines-details-fasttab"></a>Informacija, esanti „FastTab” Eilučių informacija

„FastTab” **Eilučių informacija**, esančiame **Eilučių** rodinyje, rodoma išsami informaciją apie šiuo metu pasirinktą pirkimo užsakymą „FastTab” skirtuke **Eilutės**.
