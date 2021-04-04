---
title: Darbas su vietos nurodymais
description: Ši tema aprašo, kaip dirbti su vietos nurodymais. Vietos nurodymai yra vartotojui draugiškos taisyklės padedančios identifikuoti paėmimo ir padėjimo vietas inventoriaus judėjime.
author: Mirzaab
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSLocDirHint, WHSLocDirTableUOM, WHSLocDirFailure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-11-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 84821fe4e7c5054b2121dbd7f9e536c80080b978
ms.sourcegitcommit: 1f23adbc6c7e6f9ffe8c48c10659b9fae2155aeb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470524"
---
# <a name="work-with-location-directives"></a>Darbas su vietos nurodymais

[!include [banner](../includes/banner.md)]

Vietos nurodymai yra taisyklės, kurios padeda identifikuoti atsargų judėjimo paėmimo ir padėjimo vietas. Pvz., pardavimo užsakymo operacijoje vietos nurodymas nustato, kur prekės bus paimtos ir kur bus padėtos. Vietos nurodymus sudaro antraštė ir susietos eilutės. Jos sukuriamos konkretiems *darbo užsakymo tipams*.

> [!NOTE]
> Ši tema taikoma **Sandėlio valdymo** modulio funkcijoms. Ji netaikoma funkcijoms [Atsargų valdymo](../inventory/inventory-home-page.md) moduliui.

Galite naudoti vietos nurodymus tam, kad atliktumėte šias užduotis:

- Ateinančių prekių atidėjimas.
- Prekių paėmimas ir stadijos išorės perlaidoms.
- Žaliavų gamybai paėmimas ir atidėjimas.
- Vietų papildymas.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš tai, kai galite sukurti vietos nurodymus, privalote atlikti šiuos žingsnius tam, kad įsitikintumėte, kad išankstinės sąlygos yra sukurtos.

1. Įsitikinkite, kad būtinas licencijos raktas įjungtas. Eikite į **Sistemos administravimas \> Nustatymai \> Licensijos konfigūravimas**, plėskite **Prekyba** licensijos raktą ir tada rinkitės **Sandėlio ir gabenimo valdymo** konfigūravimo raktą. Atminkite, kad administravimo prieiga būtina šiam žingsniui.
1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlis \> Sandėliai**.
1. Sandėlio sukūrimas.
1. „FastTab“ **Sandėlis** įsitikinkite nustatykite **Sandėlio valdymo procesų naudojimo** parinktį į *Taip*.
1. Sukurkite vietas, vietos tipus, vietos profilius ir vietos formatus. Dėl isamesnės informacijos, žr. [Konfigūruokite vietas WMS įjungtame sandėlyje](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).
1. Sukurkite vietas, sritis ir srities grupes. Dėl isamesnės informacijos, žr. [Sandėlio nustatymas](https://docs.microsoft.com/dynamics365/commerce/channels-setup-warehouse) ir [Konfigūruokite vietas WMS sandėlio įjungime](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).

## <a name="work-order-types-for-location-directives"></a>Darbo užsakymai tipai vietos nurodymams

Daugelis laukelių, kurie gali būti nustatyti vietos nurodymams yra bendri visiems darbo užsakymo tipams. Nepaisant to, kiti laukeliai yra konkretūs konkretiems darbo užsakymo tipams.

![Vietos nurodymų darbo užsakymo tipai](media/Location_Directives_Work_Order_Types.png "Vietos nurodymų darbo užsakymo tipai")

> [!NOTE]
> Du darbo tipai, *Atšauktas darbas* ir *Ciklo skaičiavimas* yra naudojami tik sistemos. Vietos nurodymai negali būti sukurti šiems darbo užsakymo tipams.

Lentelės tolesniuose poskyrių sąraše bendrina ir darbo užsakymo tipo konkretūs laukeliai prieinami jums nustatant vietos nurodymą.

### <a name="fields-that-are-common-to-all-work-order-types"></a>Laukeliai bendri visiems darbo užsakumo tipams

Tolesnėje lentelėje pateikti laukeliai bendri visiems darbo užsakymo tipams.

| FastTab | Laukas |
|---|---|
| Vietos nurodymai | Darbo tipas |
| Vietos nurodymai | Vieta |
| Vietos nurodymai | Sandėlis |
| Vietos nurodymai | Krypties kodas |
| Vietos nurodymai | Keli SKU |
| Eilutės | Sekos numeris |
| Eilutės | Pradinis kiekis |
| Eilutės | Kiekis Iki |
| Eilutės | Vienetas |
| Eilutės | Sandėliavimo kiekis |
| Eilutės | Riboti pagal vienetą |
| Eilutės | Apvalinti iki vieneto |
| Eilutės | Sandėliavimo pakavimo kiekis |
| Eilutės | Leisti skaidyti |
| Vietos nurodymo veiksmai | Sekos numeris |
| Vietos nurodymo veiksmai | Pavadinimas / vardas ir (arba) pavardė |
| Vietos nurodymo veiksmai | Fiksuotos vietos naudojimas |
| Vietos nurodymo veiksmai | Leisti neigiamas atsargas |
| Vietos nurodymo veiksmai | Paketas įjungtas |
| Vietos nurodymo veiksmai | Strategija |

### <a name="fields-that-are-specific-to-work-order-types"></a><a name="fields-specific-types"></a>Laukeliai konkretūs visiems darbo užsakumo tipams

Tolesnėje lentelėje pateikti laukeliai konkretūs konkretiems darbo užsakymo tipams.

| FastTab | Laukas | Darbo užsakymo tipas |
|---|---|---|
| Vietos nurodymai | Rasti pagal | Pirkimo užsakymai |
| Vietos nurodymai | Taikomas perdavimo kodas | Pirkimo užsakymai |
| Vietos nurodymai | Perdavimo kodas | Pirkimo užsakymai |
| Vietos nurodymai | Taikomas perdavimo kodas | Baigtos prekės atidėtos |
| Vietos nurodymai | Perdavimo kodas | Baigtos prekės atidėtos |
| Vietos nurodymai | Taikomas perdavimo kodas | Grąžinimo užsakymai |
| Vietos nurodymai | Perdavimo kodas | Grąžinimo užsakymai |
| Vietos nurodymai | Taikomas perdavimo kodas | „Kanban“ atidėtas |
| Vietos nurodymai | Taikomas perdavimo kodas | „Kanban“ paėmimas |
| Eilutės | Skubaus papildymo šablonas | Pardavimo užsakymai |
| Eilutės | Skubaus papildymo šablonas | Žaliavų paėmimas |
| Eilutės | Skubaus papildymo šablonas | Perkėlimo išdavimas |
| Eilutės | Skubaus papildymo šablonas | „Kanban“ paėmimas |

## <a name="open-the-location-directives-page"></a>Atverkite vietos nurodymų puslapį

Norėdami atverti **Vietos nurodymų** puslapį eikite į **Sandėlio valdymas \> Nustatymai \> Vietos nurodymai**.

Iš ten galite peržiūrėti, kurti ar redaguoti savo vietos kryptis naudodami komandas veiksmų juostoje. Žr. tolesnius šios temos skyrius dėl informacijos, kaip naudoti visus laukelius prieinamus puslapyje.

## <a name="action-pane"></a>Veiksmų sritis

Veiksmų juostos **VIETOS NURODYMŲ** puslapyje yra mygtukai, kuriuos galite naudoti siekiant sukurti, redaguoti ir naikinti kryptus (**redaguoti**, **naujas**, ir **naikinti**). Jame taip pat yra tolesni mygtukai, kurie leidžia keisti seką vietos direktyvai tvarkomai ir konfigūruoti užklausą, kuri nustato taikymo kriterijus vietos direktyvai:

- **Eiti aukštyn** – Eikite pasirinkta vietos nurodymo kryptimi aukštyn seka. Pavyzdžiui, galite perkelti jį iš skaičių sekos 4 į seką skaičiaus 3.
- **Eiti žemyn** – Eikite pasirinkta vietos nurodymo kryptimi žemyn seka. Pavyzdžiui, galite perkelti jį iš skaičių sekos 4 į seką skaičiaus 5.
- **Redaguoti užklausą** – Atidarykite teksto laukelį, kai nustatote sąlygas, kurios pasirinktos vietos direktyva turi būti tvarkoma pagal jas. Pavyzdžiui, jums gali reikėti ją taikyti tik konkrečiam sandėliui.

## <a name="location-directives-header"></a>Vietos direktyvų antraštė

Vietos direktyvos antraštė apima tolesnius laukelius dėl sekos skaičiaus ir aprašo vardą vietos direktyvai:

- **Sekos skaičius** – Šis laukelis nurodo, kad seka, kurią sistema bando taikyti kiekvienai vietos direktyvai pasirinktam darbo užsakymo tipui. Pirmiausia taikomi žemi skaičiai. Galite keisti seką naudodami **Judėti aukštyn** ir **Judėti žemyn** mygtukus veiksmų juostoje.
- **Pavadinimas** – Įveskite kainų profilį vietos direktyvos pavadinimą. Šis pavadinimas turi padėti nustatyti bendrą direktyvos tikslą. Pavyzdžiui, įveskite *Prekybos užsakymo atsiėmimas sandėlyje 24*.

## <a name="location-directives-fasttab"></a>Vietos direktyvų „FastTab“

Laukeliai **Vietos direktyvų** „FastTab“ yra konkretūs siekiant dirbti su užsakymo tipu pasirinktu **Darbo užsakymo tipo** laukelyje sąrašo juostoje.

- **Darbo tipas** – Pasirinkite darbo tipą, kurį reikia atlikti. Esamos vertės priklauso nuo inventoriaus perlaidos tipo, kurį pasirinkote **Darbo užsakymo tipo** laukelyje. Pasirinkite vieną iš šių reikšmių:

    - **Padėjimas** – Vietos direktyva bandys rasti ideliausią vietą siekiant padėti ir nustatyti inventorių, kuris patenka į sistemą iš gavimo, gamybos ar inventoriaus keitimų. Jis taip pat gali būti naudojamas siekiant nustatyti padėjimo į platformą vietą arba galutinę bay door siuntimo vietą.
    - **Paėmimas** – Vietos direktyva bandys rasti idealiausias vietas tam, kad fiziškai rezervuotų inventorių iš (kūrimo darbo). Paėmimas gali būti baigtas (tai yra, paėmimo darbo eilutė gali būti uždaryta) net jei darbas nėra baigtas. Vartotojas gali užbaigti fizinį paėmimą. Sistemoje, šis veiksmas yra paėmimo žingsnis. Darbuotojas gali tuomet atšaukti iš mobilaus įrenginio ir užbaigti darbą vėliau. Nepaisant to, darbo antraštė yra uždaroma pirmiausiai, kai galutinis padėjimas yra baigtas.

    > [!IMPORTANT]
    > Kitos vertės **Darbo tipo** laukelyje nėra svarbios vietos krypčiai. Jos pasirodo, nes laukelis nėra filtruojamas, kad atitiktų pasirinktam darbo užsakymo tipui.

- **Saitas** – Laukelis yra būtinas, nes vietos kryptis turi galėti nustatyti saitą ir jam galiojantį sandėlį.
- **Sandėlis** – Laukelis yra būtinas, nes vietos kryptis turi galėti nustatyti saitą ir jam galiojantį sandėlį.
- **Krypties kodas** – Pasirinkite krypties kodą, kad susietumėte su darbo šablonu ar papildymo šablonu. Puslapyje **Krypties kodas** galite sukurti naujus kodus, kurie gali būti naudojami siekiant sujungti darbo šablonus ar papildymo šablonus su vietos kryptimis. Direktybos kodai gali būti naudojami norint sukurti ryšį tarp bet kurio darbo šablono eilutės ir vietos direktyva (tokia kaip bay door ar platformos vieta).

    > [!TIP]
    > Jei direktyvos kodas nustatytas, sistema neieškos vietos direktyvų pagal sekos numerį, tuomet darbas bus sukurtas. Vietoje to, ji ieškos pagal direktyvos kodą. Tokiu būdu, galite būti konkretesni dėl vietos šablono, kuris naudojamas konkrečiame žingsnyje darbo šablone, tokiame kaip žingsnis medžiagų padėjimui į etapus.

- **Keli SKU** – Nustatykite šią parinktį į *Taip* tam, kad įjungtumėte keletą atsargų laikymo vienetų (SKU) naudojamų vietoje. Pavyzdžiui, keli SKU turi būti įjungti bay door vietoje. Jei įjungiate kelis SKU, jūsų padėjimo vieta bus nurodyta darbe, kaip tikimasi. Nepaisant to, padėjimo vieta galės tvarkyti tik kelių prekių padėjimą (jei darbas apima skirtingus SKU, kurie turi būti paimti ir padėti). Jis negalės sutvarkyti vieno SKU padėjimo. Jei parinktis nustatyta į *Ne*, jūsų padėjimo vieta bus nurodyta tik, jei jūsų padėjimas turi kitą SKU tipą.

    > [!IMPORTANT]
    > Norėdami galėti atlikti kelių prekių padėjimą ir vieno SKU padėjimą, turite nurodyti dvi eilutes su ta pačia struktūra ir nustatymais, tačiau turite nustatyti **Kelių SKU** parinktį į *Taip* vienai eilutei ir *Ne* kitai. Dėl to, vietos veiksmams turite du identiškas vietos direktyvas, net jei neturite atskirti atskirų SKU ir kelių SKU darbo ID. Dažnai, jei nenusatote abiejų šių vietos direktyvų, netikėtas verslo proceso vietos bus taikomos vietos direktyvai. Privalote naudoti panašius nustatymus vietos direktyvoms, kurios turi **Darbo tipą** esantį *paėmimo* jei neturite tvarkyti užsakymų su keliais SKU.

    Naudokite **Kelių SKU** parinktį darbo eilutės, kurios tvarko daugiau nei vieną prekės numerį. (Prekės numeris bus tuščias darbo išsamioje informacijoje ir bus rodomas kaip **Keli** tvarkymo puslapiuose sandėlio programoje.)

    Dažniausiuo pavyzdžio scenarijuje, darbo šablonas nustatytas taip, kad turėtų daugiau nei vieną paėmimo ar padėjimo porą. Tokiu atveju, jums gali reikėti ieškoti konkrečių platformos vietos norint naudoti eilutes su **Darbo tipu** iš *Padėjimo*.

    > [!NOTE]
    > Jei **Kelių SKU** parinktis yra nustatyta į *Taip*, negalite rinktis **Redaguoti užklausos** veiksmų juostoje, nes užklausa negali įvertinti prekės lygmeniu, kai yra kelios prekės. Siekiant užtikrinti, kad norima vietos direktyva yra pasirinkta, naudokite **Direktyvos kodo** laukelį, kad vykdytumėte pasirinkimą vietos direktyvos, kuri susijusi su padėjimo eilutėmis, kuriose vietos kodas yra priskirtas darbo šablonui.

    Išskyrus atvejus, kai visada dirbate su viena preke ar maišytų prekių veiksmais, svarbu, kad nustatytumėte dviejų vietų direktyvas *padėjimo* darbo tipo: kuriame **Keli SKU** parinktis nustatyta į *Taip* ir vieną nustatytą į *Ne*.

- **Taikomo talpinimo kodas** – Nurodykite, ar vietos talpinimo kodas direktyvos turi atitikti su talpinimo kodu taikomu, kai prekė gaunama ar vietos direktyvą galima pasirinkti pagal bet kurį talpinimo kodą. Jei renkatės *Tiksli atitiktis* ir **Talpinimo kodas** laukelis yra tuščias, tik tuščias talpinimo kodas bus laikomas šiai vietos direktyvai.

    > [!NOTE]
    > Šis laukelis prieinamas tik pasirinktiems darbo užsakymo tipams, kai papildymas leidžiamas. Dėl viso sąrašo, žr. [Laukeliai, kurie yra konkretūs darbo užsakymo tipams](#fields-specific-types) skyriuje anksčiau šioje temoje.

- **Nustatyta** – Nurodykite, ar atidėjimo kiekis turi būti visas kiekis licencijos ženkle ar jis turi būti pagal prekę. Naudokite šį laukelį, kad padėtumėte užtikrinti, jog visi turiniai licencijos ženkle padedami į vieną vietą ir kad sistema nesiūlo jums atskirti turinių į keletą vietų **ASN** (licencijos numerio gavimas), **Maišytas licencijos numeris** gaunamas ir **Klasterio** gavimo procesai. (Gavimo procesas **Klasterio** reikalauja, kad *Klasterio atidėjimo funkcija* būtų įjungta.) Toks vietos direktyvos eilės elgesys, eilučių ir vietos direktyvos veiksmai skirsis priklausomai nuo jūsų pasirinktos vertės. „FastTab“ **Eilutės** naudojamos tik, kai **Nustatyta** nustatyta į *Prekė*.

    > [!NOTE]
    > Šis laukelis prieinamas tik pasirinktiems darbo užsakymo tipams, kai papildymas leidžiamas. Dėl viso sąrašo, žr. [Laukeliai, kurie yra konkretūs darbo užsakymo tipams](#fields-specific-types) skyriuje.

- **Patalpinimo kodas** – Šis laukelis naudojamas vietos nurodymams, kurie turi darbo užsakymo tipą *Pirkimo užsakymai*, *Baigtų prekių atidėjimas* ar *Grąžinimo užsakymai* ir darbo tipą, kuris yra *Padėjimas*. Naudokite jį, kad nukreiptumėte eigą ir ji naudotų konkretų vietos nukreipimą priklausomai nuo talpinimo kodo, kurį darbuotojas pasirinko sandėlio programoje. Pavyzdžiui, galite nukreipti grąžintas prekes į apžiūros vietą prieš tai, kai jos grąžinamos į turimas. Talpinimo kodas gali būti susietas su inventoriaus būsena. Tokiu būdu, jis gali būti naudojamas siekiant pakeisti inventoriaus būseną kaip gavimo proceso dalis. Pavyzdžiui, turite talpinimo kodą, *QA*, kuris nustato inventoriaus būseną į *QA*. Galite tada turėti atskirą vietos nukreipimą tam, kad perkeltumėte inventorių į karantino vietą.

    > [!NOTE]
    > Šis laukelis prieinamas tik pasirinktiems darbo užsakymo tipams, kai papildymas leidžiamas. Dėl viso sąrašo, žr. [Laukeliai, kurie yra konkretūs darbo užsakymo tipams](#fields-specific-types) skyriuje.

## <a name="lines-fasttab"></a>Eilučių „FastTab“

Naudokite **Eilučių** „FastTab“ tam, kad įsteigtumėte sąlygas taikyti susijusius veiksmus, kurie nurodyti **Vietos nurodymo veiksmuose** „FastTab“. Kiekvienai eilutei galitte nurodyti konkretų minimalų kiekį ir maksimalų kiekį, kuriems turi būti taikomi veiksmai. Galite taip pat nurodyti, kad veiksmai būtų taikomi tik konkrečiai inventoriaus prekei.

- **Sekos skaičius** – Įveskite seką, kurioje kiekvienos vietos nurodymo eilutė turi būti tvarkoma pasirinktam vietos tipui. Galite keisti seką kaip norite su **Judėti aukštyn** ir **Judėti žemyn** mygtukais įrankių juostoje.
- **Iš kiekio** – Nurodykite kiekio intervalo pradžią, kuriai taikoma eilutė. Nurodykite matavimo vieneto kiekį, kuris yra pasirinktas **Vieneto** laukelyje.
- **Į kiekį** – Nurodykite kiekio intervalo pabaigą, kuriai taikoma eilutė. Nurodykite matavimo vieneto kiekį, kuris yra pasirinktas **Vieneto** laukelyje.
- **Vienetas** – Rinkitės matavimo vienetą prekėms. Galite nurodyti mažiausią ir didžiausią kiekius, kuriems nurodymas būtų taikomas, taip pat galite nurodyti, kad nurodymas yra skirtas konkrečiam atsargų vienetui. Laukelis **Vienetas** naudojamas *tik* kiekio vertinimui. Norėdami nustatyti, ar vietos nurodymo eilutė tiakoma, sistema naudoja kiekį vienete, kuris nurodytas toje eilutėje. Kas kartą, kai ji pasiekia vietos krypties eilutę, sistema bando pakeisti paklausos vienetą į vienetą nurodytą toje eilutėje. Jei vieneto matmens keitimas neegzistuoja, sistema pereina prie kitos eilutės.
- **Nustatyti kiekį** – Šis laukelis naudojamas tik bandymų metu siekiant padėti ar nustatyti prekes sandėlyje. (Dėl to, jis taikomas tik kai **Darbo tipo** laukelis nustatytas į *Padėjimą*.) Pasirinkite vieną tolesnių verčių, kad nurodytumėte kiekį, kuris naudojamas siekiant įvertinti, ar kiekis yra **Iš kiekio** į **Į kiekį** intervale:

    - **Licencijos numerio kiekis** – Naudokite kiekį licencijos numeryje, kuris yra gaunamas.
    - **Sujungtas kiekis** – Naudokite kiekį, kuris yra naudojamas perlaidos metu. Pavyzdžiui, gaunate kiekį 1 000 sandėlyje ir išskaidote jį į 10 licencijos numerių, kurių kiekvieno kiekis yra 100. Tokiu atveju, galite naudoti 1 000 prekių kiekį, o ne licencijos numerio kiekį 100.
    - **Likęs kiekis** – Naudokite kiekį, kuris vis dar turi būti gautas tvarkomoje prikimo užsakymo eilutėje.
    - **Tikėtinas kiekis** – Naudokite bendrą pirkimo užsakymo eilutės kiekį nepriklausomai nuo to, ar jis jau buvo gautas.

- **Apribojimas pagal vienetus** – Šis žymimas laukelis leidžia vietos nurodymo eilutę padaryti konkrečia pagal matavimo vienetą ar keletą matavimo vienetų. Pasirinkite ją tam, kad apribotumėte matavimo vienetus, kurie yra laikomi galiojančiais pasirinkimo kriterijais vietos nurodymo eilutėse. Ši funkcija veikia tik vietos kryptyse, kuriose **Darbo tipo** laukelis yra nustatytas į *Paimti*.

    Pavyzdžiui, jums rezervuojants kiekius, norite rezervuoti padėklus tik iš konkretaus vietų rinkinio. Tokiu atveju, eilutės apribos tą seką padėklams taip, kad bet kuris kiekis mažesnis nei padėklas nebus pasirinktas vietos nurodymui.

    Atsiminkite, kad **Apriboti vienetu** žymimas laukelis nevaldo vieneto ar vienetų, kurie taikomi darbo eilutėms. Vieneto apribojimas taikomas tik vienetams, kurie yra prieinami per vieneto sekos grupę. Pavyzdžiui, prekė yra susieta su vieneto sekos grupe, kuri apima tiek *padėklų*, tiek vienetus *vnt*. Matavimo vienetas buvo nustatytas, kai 1 padėklas = 100 vnt. ir vietos nurodymas naudoja **Apriboti pagal vienetą** funkciją tik padėklams. Taip pat, buvo nustatytas darbo šablonas, kuris apriboja darbo antraštės kūrimą iki 50 vnt. Šiuo atveju, bus sukurtos 50 vnt. darbo eilutės. Norėdami nustatyti matavimo vieneto apribojimą, atlikite šiuos žingsnius:

    1. „FastTab“ **Eilutės** rinkitės **Apriboti pagal eilutę** įrankių juostoje. (Šis mygtukas yra prieinamas tik po to, kai pasirenkate **Apriboti pagal vienetą** žymimą laukelį eilutėje ir tuomet pasirinkite **Įrašyti**.)
    1. Puslapyje **Apriboti pagal vienetus** laukelyje, **Vienetaas** pasirinkite matavimo vienetą, kurį norite apriboti pagal paėmimo ir padėjimo procesus.

- **Apribojimas pagal vienetą** – Šis laukelis veikia kartu su **Apribota pagal vienetą** žymimą laukelį. Pavyzdžiui, jei  **Apribokite pagal vienetą** ir **Apribokite pagal vienetą** yra pasirenkami vietos krypties eilutėje, darbas yra sukuriamas iš nurodymo žaliavų paėmimui turi būti apvalintas iki kelių tvarkymo vienetų **Apriboji pagal vienetą** puslapį.

    > [!NOTE]
    > Šie **Apvalinti iki vieneto** nustatymai veikia tik *Žalaivos paėmimo* darbo užsakymo tipe tik kai vietos nurodymai, kai **Darbo tipo** laukelis nustatytas į *Paimti*.

- **Nustatyti pakavimo kiekį** – Jei nurodėte pakavimo kiekį pardavimo užsakyme, perdavimo užsakyme ar gamybos užsakyme, šis žymimas laukelis leidžia jums apriboti sistemą taip, kad ji galėtų parinkti tik vietas, kurios turėjo mažiausią pakavimo kiekį.

    > [!NOTE]
    > Ši funkcija veikia tik su vietos nurodymais *Paėmimo* tipe.

- **Leisti dalijimą** – Nurodykite, ar vietos nurodymas gali padalyti kiekį, kuris yra gautas ar rezervuotas keliuose sandėlio vietose ar visas kiekis turi būti apdėtas vienoje vietoje ar rezervuotas iš vienos vietos siekiant sukurti darbą.
- **Nedelstinas papildymo šablonas** – Naudokite šį laukelį, kad sukurtumėte jungtį su papildymo šablonu taip, kad papildymas būtų nedelsiant paskelbtas, jei prekės nėra priskirtos. Jei paliekate šį laukelį tuščią, prekės papildymas neprasidės, kol visos vietos nurodymo eilutės nebus apdorotos.

    > [!NOTE]
    > Šis laukelis prieinamas tik pasirinktiems darbo užsakymo tipams, kai papildymas leidžiamas. Dėl viso sąrašo, žr. [Laukeliai, kurie yra konkretūs darbo užsakymo tipams](#fields-specific-types) skyriuje.

## <a name="location-directive-actions-fasttab"></a>Vietos nurodymo veiksmai „FastTab“

Galite nurodyti kelis kiekvienos eilutės vietos nurodymo veiksmus. Primename, kad sekos numeris yra naudojamas veiksmų vertinimo tvarkai nustatyti. Šiame lygyje, galite nustatyti užklausą, kad nustatytumėte, kaip geriausia vieta sandėlyje randama. Galite taip pat naudoti iš anksto nustatytas **Strategijos** vertes, kad rastumėte optimalią vietą.

- **Sekos skaičius** – Šis laukelis rodo seką, kurioje veiksmai yra tvarkomi pasirinktame darbo tipe. Galite keisti seką naudodami **Judėti aukštyn** ir **Judėti žemyn** mygtukus įrankių juostoje.
- **Pavadinimas** – Įveskite vietos nurodymo veiksmo pavadinimą. Būkite konkretūs taip, kad atliekamas veiksmas būtų aiškus iš pavadinimo.
- **Fiksuotos vietos naudojimas** – Nurodykite, kurios vietos vietos nurodyme turi būti vertinamos. Pasirinkite vieną iš šių reikšmių:

    - **Fiksuotos ir nefiksuotos vietos** – Bus atsižvelgta į vietos nurodymą visose vietose.
    - **Tik fiksuotos vietos produktui** – Vietos nurodymas atsižvelgs tik į fiksuotas vietas produktams.
    - **Tik fiksuotos vietos produkto variantui** – Vietos nurodymas atsižvelgs tik į fiksuotas vietas produkto variantams.

- **Leisti neigiamą inventorių** – Pasirinkite šį žymimą laukelį ir leiskite neigiamą inventorių konkrečiame sandėlio nurodyme vietos nurodymuose.
- **Bendri įjungti** – RInkitės šį žymimą laukelį, kad naudotumėte bendrų strategiją prekėms, kurios yra įjungtos kaip bendros. Svarbu, kad pasirinktumėte šį žymimą laukelį tvarkymui, kuris naudoja vietos nurodymus, kad rastumėte vietas paėmimo darbui skaičiaus sekimo prekėms. Tokiu būdu, ieškokite vietų, kurios laiko bendrų skaičių sekimo prekes. Jei šis žymimas laukelis yra pasirinkitas ir **Strategijos** laukelis yra nustatytas į *Jokio*, sistema judės prie kito veiksmo eilutės.
- **Strategija** – Norėdami paprasčiau ir greičiau nustatyti veiksmus susietus su kiekvienos vietos nurodymo eilute galite pasirinkti vieną iš parengtų strategijų:

    - **Jokia** – Bus nenaudojama jokia strategija.
    - **Atitikimo paketo kiekis** – Strategija patikrina, ar paėmimo vieta turi konkretų pakavimo kiekį. Ši strategija galioja tik, jei **Darbo tipo** laukelis yra nustatytas į *Paimti*.
    - **Konsoliduoti** – Ši strategija konsoliduoja prekes konkrečioje vietoje, kai panašios prekės jau yra prieinamos. Ši strategija galioja tik, jei **Darbo tipo** laukelis yra nustatytas į *Padėti*. Įprasti nustatymai atidėjimo bandymams siekia konsoliduoti pirmojo veiksmo eilutę ir tada antrają eilutę, bando padėti be konsolidavimo. Prekių konsolidavimas paverčia pastarąjį paėmimą efektyvesniu.
    - **FEFO bendrų rezervavimas** – Ši strategija naudoja pirmojo pasibaigimo, pirmojo išvesties (FEFO) bendrus rezervavimus. Naudokite ją, kai inventorius aptinkamas naudojant bendrą pabaigos datą ir paskyrimą bendrų rezervavimui. Galite naudoti šią strategiją tik pakete įjungtoms prekėms. Jis galioja tik tada, kai **Darbo tipo** laukelis nustatytas į *Paėmimą*.
    - **Apvalinkite iki viso LP ir FEFO bendrų** – Ši strategija suderina elementus *FEFO bendros rezervacijos* ir *Apvalinimo iki viso LP* strategijas. Ji galio ja tik bendrų įjungtoms prekėms ir vietų kryptims, kurių darbo tipas yra *Paimti*. Eilutę turi būti įjungta bendriems siekiant naudoti *FEFO bendrų rezervavimo* strategiją ir *Apvalinimo iki viso LP* strategiją, kuri gali būti naudojama tik papildymui. Jei ši strategija konfigūruojama kartu su vietos talpos apribojimu, ji gali sukelti pasirinktimo padėjimo darbo vietos perpildymą ir atsargų apribojimus, kurie ignoruojami.
    - **Apvalinti iki pilno LP** – Ši strategija naudojama siekiant suapvalinti inventoriaus kiekį taip, kad jis atitiktų licencijos numerio kiekį priskirtą prekėms, kurias reikia paimti. Galite naudoti šią strategiją tik papildymo vietos nurodymams *Paėmimo* tipe. Jei ši strategija konfigūruojama kartu su vietos talpos apribojimu, ji gali sukelti pasirinktimo padėjimo darbo vietos perpildymą ir atsargų apribojimus, kurie ignoruojami.
    - **Licencijos numerio vedlys** – Naudokite šią strategiją išleisdami užsakymą į sandėlį siekiant sukurti paėmimo ir padėjimo darbą. Galite naudoti šią prieigą keliems licencijų numeriams. Ši strategija bandys rezervuoti ir kurti paėmimo darbą lyginant su vietomis, kurios paima būtinus licencijos numerius, susietus su perdavimo užsakymo eilutėmis. Nepaisant to, jei šie veiksmai negali būti užbaigti, bet vis dar norite sukurti paėmimo darbą, turėtumėte eiti į kitą strategiją vietos nurodymų veiksmams. Priklausomai nuo jūsų verslo proceso reikalavimų, jums gali reikėti ieškoti inventoriaus kitoje sandėlio srityje.
    - **Tuščia vieta be jokio ateinančio darbo** – Naudokite šią strategiją, kad nustatytumėte tuščias vietas. Vieta laikoma tuščia, jei ji neturi jokių fizinių atsargų ir jokio tikimosi ateinančio darbo. Galite naudoti šią strategiją tik papildymo vietos nurodymams, kurių darbo tipas yra *Padėti*.
    - **Pasenusio FIFO nustatymas** – Naudokite pirmojo įeinančiojo, pirmojo išeinančio (FIFO) strategiją norėdami siųsti tiek bendrai sekamas prekes, tiek ir nesekamas prekes pagal datą, kai inventorius pateko į sandėlį. Ši galimybė gali būti ypatingai naudinga nebendram sekamam inventoriaus, kai nėra jokios galiojimo datos prieinamos siekiant naudoti rūšiavimą. FIFO strategija suranda vietą, kurioje yra seniausia pasenusi data ir tuomet nustato paėmimą pagal tą pasenusią datą.
    - **Pasenusio LIFO nustatymas** – Naudokite paskutinio įeinančiojo, paskutinio išeinančio (LIFO) strategiją norėdami siųsti tiek bendrai sekamas prekes, tiek ir nesekamas prekes pagal datą, kai inventorius pateko į sandėlį. Ši galimybė gali būti ypatingai naudinga nebendram sekamam inventoriaus, kai nėra jokios galiojimo datos prieinamos siekiant naudoti rūšiavimą. LIFO strategija suranda vietą, kurioje yra naujausia pasenusi data ir tuomet nustato paėmimą pagal tą pasenusią datą.

## <a name="example-using-location-directives"></a>Pavyzdys: Vietos nurodymų naudojimas

Šiame pavyzdyje svarstomas pirkimo užsakymo procesas, kai vietos nurodymas turi sandėlyje rasti laisvos vietos atsargų prekėms, kurios buvo ką tik užregistruotos gavimo rampoje. Pirmiausia reikia sandėlyje rasti laisvos vietos, konsoliduojant esamas atsargas. Jei konsoliduoti negalima, tada reikia rasti tuščią vietą.

Pagal šį scenarijų turite nustatyti du vietos nurodymo veiksmus. Pirmasis sekos veiksmas turi naudoti strategiją *Konsoliduoti*, o antrasis – strategiją *Tuščia vieta, kurioje negaunama darbo*. Jei nenustatysite trečio veiksmo, skirto perpildos scenarijui tvarkyti, kai sandėlyje nėra vietos, galimi du rezultatai: darbą galima kurti net jei nėra nurodytų vietų arba darbo kūrimo procesas gali nepavykti. Išdava yra nustatoma pagal nustatymus **Vietos nurodymo nesėkmės** puslapyje, kuriame galite pasirinkti, ar pasirinkti **Baigti darbą su vietos nurodymo nesėkmės** parinktimi kiekvienam darbo tipui.

## <a name="next-step"></a>Kitas veiksmas

Kai sukūrėte vietos nurodymus, galite susieti visus nurodymo kodus su darbo šablono kodu darbo sukūrimui. Dėl išsamesnės informacijos, žr. [Sandėlio darbo kontroliavimas naudojant darbo šablonus ir vietos nurodymus](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/control-warehouse-location-directives).

## <a name="additional-resources"></a>Papildomi ištekliai

- Vaizdo įrašas: [Sandėlio valdymo konfigūravimo gili analizė](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Pagalbos tema: [Valdyti sandėlio darbą naudojant darbo šablonus ir vietos nurodymus](control-warehouse-location-directives.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
