---
title: Atributų ir atributų grupių tvarkymas
description: Šiame straipsnyje aprašoma, kaip valdyti atributus ir atributų grupes, siekiant aprašyti produktus ir jų charakteristikas Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.openlocfilehash: aad448ea733aabdff3dc4438dcb682d49e0665c0
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/31/2022
ms.locfileid: "9386978"
---
# <a name="manage-attributes-and-attribute-groups"></a>Atributų ir atributų grupių tvarkymas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip valdyti atributus ir atributų grupes, siekiant aprašyti produktus ir jų charakteristikas Microsoft Dynamics 365 Commerce.

*Atributai* pateikia produktų ir jų charakteristikų aprašą vartotojo apibrėžtuose laukuose. Pavyzdžiai yra atminties dydis, standusis disko pajėgumas ir energijos pagal "Energy" atitikimas.

Atributus galima susieti su įvairiais „Commerce“ objektais, pavyzdžiui, produkto kategorijomis ir kanalais, ir galima nustatyti jį numatytąsias reikšmes. Kai atributai siejami su produktų kategorijomis arba kanalais, produktai paveldi šiuos atributus ir jų numatytąsias vertes. Numatytųjų atributų verčių galima nepaisyti atskirų produktų lygyje, kanalo lygyje arba kataloge.

Pavyzdžiui, įprastas televizijos produktas gali turėti tolesnius atributus.

| Kategorija   | Atributas           | Leistinos reikšmės                        | Numatytoji vertė |
|------------|---------------------|-------------------------------------------|---------------|
| TV ir vaizdo įrašai | Rūšis               | Bet kuri tinkama prekės ženklo reikšmė                     | Jokia          |
| TV         | Ekrano dydis         | 20–85 colių                              | 55 colių     |
|            | Vertikali skiriamoji geba | 4K (2160p), Full HD (1080p) arba HD (720p) | 4K (2160p)    |
|            | Ekrano naujinimo dažnis | 60 hz, 120 hz arba 240 hz                     | 60 hz          |
|            | HDMI įvestys         | 0–10                                      | 3             |

## <a name="attributes-and-attribute-types"></a>Atributai ir atributų tipai

Atributai pagrįsti *atributų tipais*. Atributo tipas identifikuoja duomenų, kuriuos galima įvesti konkrečiam atributui, tipą. "Commerce" palaikomi šie atributų tipai:

- **Valiuta** – šis tipas palaiko valiutos reikšmę. Jis gali būti apribotas (t. y., jis gali palaikyti reikšmių intervalą) arba jis gali būti neapibrėžtas.
- **Data ir laikas** – šis tipas palaiko datos ir laiko reikšmę. Jį galima apibrėžti arba palikti neapibrėžtą.
- **Dešimtainis skaičius** – šis tipas palaiko skaitinę reikšmę su skaitmenimis po kablelio. Jis taip pat palaiko matavimo vienetą. Jį galima apibrėžti arba palikti neapibrėžtą.
- **Sveikasis skaičius** – šis tipas palaiko skaitinę reikšmę. Jis taip pat palaiko matavimo vienetą. Jį galima apibrėžti arba palikti neapibrėžtą.
- **Tekstas** – šis tipas palaiko teksto reikšmę. Jis taip pat palaiko iš anksto apibrėžtą galimų verčių rinkinį, kai **įgalintas fiksuoto** sąrašo nustatymas.
- **Bulio logika** – šis tipas palaiko dvejetainę reikšmę (**teisinga** arba **klaidinga**).
- **Nuoroda** – šis tipas nurodo į kitus atributus.

> [!NOTE]
> Dėl "[Azure" ieškos indekso apribojimų](/rest/api/searchservice/data-type-map-for-indexers-in-azure-search) dešimtainio **atributo** tipo nepalaikoma ieška debesyje. "Azure" nepavyko konvertuoti dešimtainių **atributų** **tipų į "Edm.Double"** paskirties indekso laukų tipus, nes šis konvertavimas turėtų sumažinti tikslumą.

### <a name="set-up-attribute-types"></a>Nustatyti atributų tipus

Norėdami nustatyti atributų tipus, atlikite šio pavyzdžio procedūros veiksmus.

1. Prisiregistruokite prie "Commerce Headquarters" kaip prekybos vadybininko.
1. Eikite į **produkto informacijos valdymo nustatymo \> kategorijas \> ir atributų atributų \> tipus**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Atributo **tipo pavadinimo lauke** įveskite Maišelio **tipą**.
1. Lauke **Tipas** pasirinkite **Tekstas**.
1. Nustatykite sąrašo **parinktis** Fiksuota kaip **Taip**.
1. Skirtuke **Vertės** FastTab pasirinkite **Įtraukti**.
1. Naujoje eilutėje vertės lauke **įveskite** **Satijus**.
1. Pridėti dar penkias eilutes. Kiekvieno vertės **lauke** įveskite skirtingą vertę: **Ckarpa**, Purse **,** Backpack, **Pasiuntinys** **arba** Tts **·**.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Atributo **tipo pavadinimo lauke** įrašykite Pagal vartotojo **prekės ženklą**.
1. Lauke **Tipas** pasirinkite **Tekstas**.
1. Nustatykite sąrašo **parinktis** Fiksuota kaip **Taip**.
1. Skirtuke **Vertės** FastTab pasirinkite **Įtraukti**.
1. Naujoje eilutėje, vertės **lauke**, įveskite **Skirtuko banką**.
1. Pridėti dar dvi eilutes. Kiekvieno vertės **lauke** įveskite kitą vertę: **Aviatorius arba** **Javs**.
1. Veiksmų srityje pasirinkite **Įrašyti**.

![Atributų tipų puslapis.](media/AttributeType_2022Series.png)

### <a name="set-up-an-attribute"></a>Nustatyti atributą

Norėdami nustatyti atributą, atlikite šio pavyzdžio procedūros veiksmus.

1. Prisiregistruokite prie "Commerce Headquarters" kaip prekybos vadybininko.
1. Eikite į **produkto informacijos valdymo nustatymo \> kategorijas \> ir atributų atributus \>**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Lauke Pavadinimas **įveskite** Maišelio **tipą**.
1. Atributo **tipo lauke** pasirinkite Maišelio **tipas**.
1. Veiksmų srityje pasirinkite **Įrašyti**.

![Atributų puslapis.](media/Attribute_2022Series.png)

## <a name="attribute-metadata"></a>Atributo metaduomenys

*Atributų metaduomenys* leidžia pasirinkti parinktis, kad galėtumėte nurodyti, kaip turėtų veikti kiekvieno produkto atributai. Pavyzdžiui, galite nurodyti, ar atributai reikalingi, ar juos galima naudoti ieškant ir ar juos galima naudoti kaip filtrą.

Produktų atributų metaduomenų parametrų galima nepaisyti kanalo lygiu.

Atributo atributų puslapyje **yra** kelios pasirinktys, susijusios su atributo metaduomenimis. Pvz., **·** **·** **jei "Commerce**" kanalams nustatėte parinktį Galima patikslinti kaip Taip, atributo metaduomenys bus rodomas patikslinus arba filtruojant produktus paieškos rezultatuose ir kategorijų naršymo puslapiuose. Norėdami konfigūruoti atributą kaip tikslinam, pirmiausia veiksmų **srityje** turite pasirinkti Filtro parametrus ir patvirtinti atributo filtro parametrus.

## <a name="filter-settings-for-attributes"></a>Atributų filtrų parametrai

Atributų filtravimo parametrai leidžia nustatyti, kaip atributų filtrai rodomi point sale (EKA). Norėdami pasiekti atributo filtro parametrus, atributo atributų **puslapyje**, veiksmų srityje, pasirinkite **Filtro parametrai**.

Filtro **parametrų** puslapyje yra šie laukai:

- **Pavadinimas** – pagal numatytuosius parametrus šis laukas yra nustatytas kaip atributo pavadinimas. Tačiau reikšmę galite keisti.
- **Rodymo parinktis** – galimos tolesnės parinktys.

    - **Viena reikšmė** – šią parinktį galima naudoti su šių tipų atributais: **Bulio logika**, **Valiuta**, **Dešimtainis skaičius**, **Sveikasis skaičius** ir **Tekstas**. Galima pasirinkti tik vieną produktų sąrašo puslapių patikslintojų vertę, pvz., naršymą po kategorijas ir produktų ieškos rezultatų puslapius.
    - **Kelios reikšmės** – šią parinktį galima naudoti su šių tipų atributais: **Valiuta**, **Dešimtainis skaičius**, **Sveikasis skaičius** ir **Tekstas**. Tai leidžia pasirinkti kelias kliento atributo vertes patikslinti.

- **Rodymo valdiklis** – galimos tolesnės parinktys.

    - **Sąrašas** – ši pasirinktis galima visiems atributų tipams.
    - **Intervalas** – šią parinktį galima naudoti su šių tipų atributais: **Valiuta**, **Dešimtainis skaičius** ir **Sveikasis skaičius**.
    - **Slankiklis** – šią parinktį galima naudoti su šių tipų atributais: **Valiuta**, **Dešimtainis skaičius** ir **Sveikasis skaičius**.
    - **Slankiklis su juostomis** – šią parinktį galima naudoti su šių tipų atributais: **Valiuta**, **Dešimtainis skaičius** ir **Sveikasis skaičius**.

- **Ribinė reikšmė** – šis parametras reikalingas, jei kaip rodymo valdiklio tipą pasirinkote **Intervalas**. Apibrėžti reikšmes galite kaip skyriklį naudodami kabliataškį (;).

    Pavyzdžiui, **·** **maišelio tūrio atributui, kuris turi atributo tipą "Integer**", **ribinė vertė gali būti 10; 20; 50; 100; 200; 500; 1000; 5000**. Tokiu atveju el. kasos aparate bus rodomi tolesni intervalai. Diapazonai, kurių rezultatų rinkinys neturi jokių produktų, bus rodomi blankūs.

    - Mažiau nei 10
    - 10–20
    - 20–50
    - 50–100
    - 100–200
    - 200–500
    - 500 ar daugiau

Atributų filtravimo parametrai taikomi tik produkto atributams ir gali būti naudojami produktų ieškos ir kategorijų naršymo rezultatams patikslinti. Jos netaikomos klientų paieškai ar užsakymų paieškai, nors tie patys atributai gali būti naudojami kliento arba užsakymo informacijai papildyti.

Numatytuosiuuose "Commerce" moduliuose, "Display" valdiklio filtro parametrams, **·** **pvz**., Intervalas, **Diapazonas** ir Parinktys su juostomis, **negalima naudoti** jokio numatytojo palaikymo. Diapazono **·** **ir Esamų** nustatymai toliau palaikomi EKA sprendimais, **o Parametras Už el su juostomis taikomas senesniems interneto parduotuvės kiekims, jis išlieka galimas** SharePoint trečiosios šalies integravimui ir pasirinktiniams scenarijams.

Patariame **·** **patikslinti** atributus kaip Teksto tipo atributą, kai įgalinta pasirinktis Fiksuotas sąrašas, ir kad sąrašas būtų valdomas (iki 100–200 unikaliųjų verčių). Jei patikslintojas turės 1000 ar daugiau unikalių verčių, labiau tinka naudoti teksto tipo atributą, kai išjungta **parinktis** **Fiksuotas** sąrašas.

Vertimai yra svarbūs atributų pavadinimams ir jų vertėms. Atributams, kurių **teksto** tipo parinktis **Fiksuotas** sąrašas įgalinta, galite nurodyti atributo verčių vertimus po atributo **tipu**. Puslapyje, kuriame apibrėžiate atributo vertes, galite nurodyti kiekvieno kito atributo tipo vertimus. Pvz., teksto tipo **atributui** galite apibrėžti numatytosios vertės vertimus atributo atributų **puslapyje**. Tačiau, jei nepaisote numatytosios vertės produkto lygyje, galite nurodyti atributo vertimus produkto atributų **puslapyje**.

Po to, kai atributas yra pažymėtas kaip tikslinimas kanalui, atributo tipo atnaujinti nereikia. Priešingu atveju, tai turės įtakos produkto duomenų publikavimui ieškos indekse. Todėl rekomenduojame sukurti naują atributą naujam tikslinimo tipui ir panaikinti ankstesnį atributą pašalinant jį iš kitų atributų grupių.

Ieška pagal atributus palaikoma, bet ieškoma rezultatų tik tikslaus ieškos žodžių atitikmens. Pavyzdžiui, medžiagos atributo **vertė** yra **Cashmere objekto** vertė. Jei klientas ieškos "Grynieji pinigai", nebus **nuskaityta nė dalis produktų, kurie turi kasininko jausinį**. Tačiau jei klientas ieško "Cashmere", "Kuriama", "Kuriama" arba "Cashmere Automatiškai", produktų, **kurių** kasininko klaida yra pasisiųsta kaip medžiaga, bus nuskaityta.

### <a name="additional-attribute-metadata-options"></a>Papildomos atributo metaduomenų parinktys

> [!NOTE]
> Šios atributo metaduomenų parinktys taikomos tik senesniems interneto parduotuvėse SharePoint iš anksto ir išoriniams integrauojant. Daugiau informacijos apie šias atributo metaduomenų pasirinktis [ieškokite ieškos schemos serveryje SharePoint 2013 peržiūra](/SharePoint/search/search-schema-overview).

Atributų puslapyje taip pat galimos šios papildomos atributų metaduomenų **pasirinktys**:

- Galimas ieškoti
- Atgaunamas
- Galima užklausti
- Galimas rikiuoti
- Nepaisyti atvejo ir formato
- Visiška atitiktis

Šios pasirinktys iš pradžių buvo skirtos patobulintos senesnių internetinės SharePoint parduotuvės parduotuvių ieškos funkcijų. Jie nebūtinai taikomi "Commerce e-commerce" svetainėms arba EKA terminalams. Kadangi ir toliau palaikoma besidūmių integravimas, šios pasirinktys galimos atributų metaduomenims eksportuoti naudojant "Commerce" programinės įrangos kūrimo rinkinį (SDK). Galite naudoti "Commerce SDK" produktams į pasirinktinį optimizuotą išorinės ieškos indeksą įtraukti. Tokiu būdu galite užtikrinti, kad indeksuojami tik indeksuojami atributai.

## <a name="attribute-groups"></a>Atributų grupės

Atributų *grupė* naudojama produkto konfigūracijos modelyje norint sugrupuoti atskirus komponento arba subkomponento atributus. Atributą galima įtraukti į daugiau nei vieną atributų grupę. Atributų grupės vartotojams gali padėti konfigūruoti produktus, nes įvairios pasirinktys išdėstomos konkrečiame kontekste. Atributų grupes galima priskirti kategorijoms arba kanalams. Taip pat galite nustatyti atributų grupės numatytąsias vertes.

![Atributų grupių puslapis.](media/AttributeGroup_2022Series.png)

### <a name="create-an-attribute-group"></a>Atributų grupės kūrimas

Norėdami sukurti atributų grupę, atlikite šio pavyzdžio procedūros veiksmus.

1. Prisiregistruokite prie "Commerce Headquarters" kaip prekybos vadybininko.
1. Eikite į **produkto informacijos valdymo nustatymo \> kategorijas \> ir atributų atributų \> grupes**.
1. Sukurti atributų grupę, pavadintą **Tamsūs marškinėliai**.
1. Įtraukite šiuos atributus: CleaningMethod **,** Pagalrūšis **,** Rinkinys **ir** Dizainas **.**

> [!NOTE]
> Rodomos atributų grupės užsakymų vertės neturi įtakos arba taikomos patikslintojų tvarkai ieškos ir kategorijos naršymo rezultatuose. Jos taikomos tik užsakymo atributų scenarijui.

### <a name="assign-attribute-groups-to-categories"></a>Atributų grupių priskyrimas kategorijoms

Viena ar daugiau atributų grupių gali būti susietos su kategorijų mazgais šių tipų kategorijų hierarchijuose:

- „Commerce“ produktų hierarchija
- Kanalo naršymo kategorijų hierarchija
- Papildoma produktų kategorijų hierarchija

Kai produktai skirstomi į kategorijas, kurios susietos su atributų grupėmis, jie paveldi atributus, įtrauktus į tas atributų grupes.

![Produktų atributų grupių "FastTab" "Commerce" produktų hierarchijos puslapyje.](media/AGRetailProdHierarchy_2022Series.png)

Norėdami priskirti atributų grupes kategorijoms "Commerce" produktų hierarchijoje, atlikite šio pavyzdžio procedūros veiksmus.

1. Prisiregistruokite prie "Commerce Headquarters" kaip prekybos vadybininko.
1. Eikite į **Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Prekybos produktų hierarchija**.
1. Pasirinkite madingų **madingų** prekės naršymo hierarchiją.
1. Skirtuke Mens **įvardijami, pasirinkite Kategoriją**,**tada** į produktų atributų grupes "FastTab **" įtraukite atributų grupę,** kuri vadinama Vyrais **.**
1. Pasirinkite kategoriją **Madingi akiniai nuo saulės** ir patikrinkite naujus atributų grupės **Madingi akiniai nuo saulės** atributus pasirinkdami **Peržiūrėti atributus**. Atributų grupėje turi būti rodomi nauji atributai **Lęšio forma** ir **Akinių nuo saulės prekės ženklas**.
1. Pasirinkite kategoriją **Arbas** ir, pasirinkdami **Peržiūrėti atributus, patikrinkite Vyriškos atributų** grupės **atributus**. Atributų grupėje turi būti rodomi atributai **Vyriško diržo prekės ženklas**, **Diržo medžiaga** ir **Diržo dydis**.

Ta pati pagrindinė procedūra taip pat gali būti naudojama atributų grupėms priskirti kategorijoms kanalo naršymo kategorijų hierarchijoje ir papildomoje produktų kategorijų hierarchijoje. Tačiau 2 veiksme naudokite vieną iš toliau nurodytų maršrutų, atsižvelgdami į hierarchiją, prie kurios norite priskirti atributų grupes:

- **Kanalo naršymo kategorijų hierarchija:** eikite į mažmeninės **prekybos ir "Commerce" \> kategorijų ir produktų valdymo kanalo \> naršymo kategorijas**.
- **Papildoma produktų kategorijų hierarchija:** eikite į " **Retail" ir "Commerce \> " kategoriją ir produktų valdymo \> papildomas produktų kategorijas**.

> [!NOTE]
> Įsitikinkite, kad susiejate tik atributų grupes kategorijų **hierarchijoje**, "FastTab", o ne **kategorijos atributų vertėse "** FastTab". Jei atributai rodomi kategorijos **atributų vertėse "** FastTab", veiksmų **srityje pasirinkite** Redaguoti kategorijų hierarchiją. Tada kategorijos atributų **grupėse** "FastTab" pasirinkite kategorijos mazgus ir pasirinkite **Pašalinti**. Nepalaikoma atributų pagal kategoriją naudojant komercijos skalės vienetą.

## <a name="identify-viewable-and-refinable-attributes-for-commerce-channels-for-the-default-product-collection"></a>Nustatyti "Commerce" kanalų peržiūrėtimus ir tikslinamus atributus, siekiant nustatyti numatytąjį produktų rinkinį

Susieę įvairias atributų grupes su kategorijomis įvairiose hierarchijose ("Commerce" produktų hierarchijos arba kanalo naršymo kategorijos) ir pagal kategorijos susiejimą apibrėžę atributų vertes turite įgalinti atributą Rodyti **kanalo vėliavėlėje,** kad šiuos atributus būtų galima peržiūrėti konkrečiame kanale.

1. Pasirinkite **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Kanalo kategorijos ir produkto atributai**.
1. Pasirinkite **Nustatyti atributo metaduomenis**, tada kairiojoje naršymo srityje pasirinkite atributą.
1. Kanalo produkto **atributų "** FastTab" (ne **kategorijos** atributų "FastTab") **nustatykite atributo Rodyti** **kanalo pasirinktyje kaip Taip**, kad atributą būtų galima peržiūrėti.
1. Jei norite, kad atributas būtų per daug tikslinimas, nustatykite **pasirinktį Galima patikslinti** kaip **Taip**.

### <a name="control-visibility-of-dimension-based-refiners-such-as-size-style-and-color"></a>Valdyti dimensijomis pagrįstų tikslinimų matomumą, pvz., dydį, stilių ir spalvą

Produktų dimensijos, pvz., dydis, stilius ir spalva, yra dažniausiai naudojami tikslinimo priemonės. Norėdami, kad šios produkto dimensijos būtų galimos kaip tikslinimo priemonės, turite susieti atributų grupę kanalo lygiu, kuriame yra nuoroda į atributo tipą, kuris automatiškai perima vertes iš produkto dimensijų reikšmių.

Galite nurodyti, kad produkto dimensijos yra peržiūrėtinos ir tikslinamos, atnaujindami vėliavėles kanalo **kategorijų ir produktų atributų** puslapyje. Naršymo srityje pasirinkite šakninį mazgą, **tada dalyje Kanalo produkto atributai "FastTab**" nustatykite atributo Rodyti **kanalo** pasirinktį **Taip** **, jei atributai Dydis,** **·** **Stilius ir Spalva.** Jei norite, kad šie atributai būtų per patikslinti, nustatykite **kiekvieno iš jų pasirinktį** Galima **patikslinti** kaip Taip.

![Nustatoma dimensijų tikslinimo priemonių atributo metaduomenys.](./media/ProductDimensionRefinersMetadataSetup_2022Series.png)

Norėdami įgalinti atributus, kad jie būtų galimi demonstracinių duomenų kanale Pagal Jav, atlikite šioje pavyzdyje nurodytus veiksmus.

1. Pasirinkite **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Kanalo kategorijos ir produkto atributai**.
1. Pasirinkite kanalą **„Houston“**.
1. Veiksmų srityje pasirinkite **Nustatyti atributų metaduomenis**.
1. Pasirinkite kategorijos mazgą **Madingos prekės**, tada „FastTab“ skirtuke **Kanalo produktų atributai** kiekvienam atributui parinkite **Įtraukti atributą**.
1. Pasirinkite kategorijos mazgą **Madingi priedai**, pasirinkite kategoriją **Madingi akiniai nuo saulės**, tada „FastTab“ skirtuke **Kanalo produktų atributai** kiekvienam atributui parinkite **Įtraukti atributą**.
1. Pasirinkite kategorijos mazgą **Vyriški drabužiai**, pasirinkite kategoriją **Kelnės**, tada „FastTab“ skirtuke **Kanalo produktų atributai** kiekvienam atributui parinkite **Įtraukti atributą**.
1. Atnaujinę savo skirtų atributų ir tikslinimo priemonių atributų metaduomenis, įsitikinkite, kad įrašysite keitimus ir užduotį Publikuoti **kanalo naujinimus**. Publikuoę naujinimus turite vykdyti šias užduotis: **1070** (**kanalo** konfigūracija), 1040 **(** **produktai)** **ir 1150** (**katalogas).**

> [!NOTE]
> - Jei jūsų verslui reikia dažnai įtraukti ar šalinti produktus naršymo hierarchijoje arba atlikti pakeitimus, pvz., atnaujinti rodymo užsakymo vertes, įtraukti naujas kategorijas ir į kategorijas įtraukti naujų atributų grupių, **rekomenduojame** sukonfigūruoti kanalo naujinimų publikavimo užduotį, kad ji būtų vykdoma kaip dažna paketinė užduotis. **Arba rankiniu būdu suaktyvinkite kanalo atnaujinimo užduotį Publikuoti**, Commerce Data Exchange tada šias (CDX) užduotis: **1070** (**kanalo** konfigūracija), **1040** (**produktai**) **ir 1150** (**katalogas**).
> - Paveldėjimo **parinktis** leidžia nurodyti, kad kanalas turėtų paveldėti atributų grupes iš jos pagrindinio kanalo hierarchijoje. Jei parinktį **Paveldėti** nustatote kaip **Taip**, antrinis kanalo mazgas paveldi visas atributų grupes ir visus tų atributų grupių atributus.
> - Jei veiksmų **srities mygtuko** Nustatyti atributą metaduomenys nėra, įsitikinkite, **kad** naršymo hierarchija susieta su jūsų kanalu **bendrajame** "FastTab".
> - Turite susieti jokių atributų grupių, išskyrus dimensija paremtas atributų grupes kanalo lygyje (pvz., **·** **dalies Atributų grupės puslapyje Kanalo kategorijos ir Produkto atributai**).
> - Po to, kai "Commerce" versijoje 10.0.27 buvo įdiegtas klientų aptarnavimo įmonių (B2B) katalogų palaikymas, tikimasi, kad kiekvienam B2B katalogui patikslinsite ir atributų nustatymus taip pat, kaip aprašyta šiame straipsnyje.

## <a name="override-attribute-values"></a>Nepaisyti atributo verčių

Atskirų produktų atributų numatytųjų reikšmių galima nepaisyti produkto lygiu. Be to, atskirų produktų, skirtų konkretiems kanalams, jų galima nepaisyti.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Atskiro produkto atributų reikšmių nepaisymas

Norėdami nepaisyti atskiro produkto atributų verčių, atlikite šio pavyzdžio procedūros veiksmus.

1. Prisiregistruokite prie "Commerce Headquarters" kaip prekybos vadybininko.
1. Eikite į " **Retail" ir "Commerce \> Category" ir "Produktų valdymas \> " Išleistus produktus pagal kategoriją**.
1. Pasirinkite madingų **\> madingų \> madingų objektų madingų objektų priedai**.
1. Tinklelyje pasirinkite reikiamą produktą. Tada veiksmų srities skirtuko **Produktas** grupėje **Nustatyti** pasirinkite **Produktų atributai**.
1. Pasirinkite atributą kairiojoje srityje, tada atnaujinkite jo reikšmę dešiniojoje srityje.

![Produkto atributo reikšmių puslapis.](media/ProdDetailsProdAttrValues_2022Series.png)

### <a name="override-the-attribute-values-of-all-products-in-a-catalog"></a>Nepaisyti visų katalogo produktų atributų verčių

Norėdami nepaisyti visų katalogo produktų atributų verčių, atlikite šios pavyzdinės procedūros veiksmus.

1. Prisiregistruokite prie "Commerce Headquarters" kaip prekybos vadybininko.
1. Eikite į **"Retail" ir "Commerce \> Catalog Management \> All" katalogus**.
1. Pasirinkite katalogą **„Fabrikam“ pagrindinis katalogas**.
1. Pasirinkite madingų **\> madingų \> madingų objektų madingų objektų priedai**.
1. „FastTab“ skirtuke **Produktai** pasirinkite reikiamą produktą, tada virš produktų tinklelio pasirinkite **Atributai**.
1. Tolesniuose „FastTab“ atnaujinkite reikiamų atributų reikšmes.

    - Bendrinami produktų publikavimo kanalai
    - Bendrai naudojami produkto atributai
    - Publikavimo kanalas
    - Kanalo produkto atributai

### <a name="override-the-attribute-values-of-all-products-in-a-channel"></a>Nepaisyti visų kanalo produktų atributų verčių

Norėdami nepaisyti visų kanalo produktų atributų verčių, atlikite šios pavyzdinės procedūros veiksmus.

1. Prisiregistruokite prie "Commerce Headquarters" kaip prekybos vadybininko.
1. Pasirinkite **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Kanalo kategorijos ir produkto atributai**.
1. Pasirinkite kanalą **„Houston“**.
1. „FastTab“ skirtuke **Produktai** pasirinkite reikiamą produktą, tada virš produktų tinklelio pasirinkite **Atributai**.
1. Jei produktų nėra, pasirinkite **Įtraukti į** produktų **"** FastTab", tada dialogo lange Įtraukti **produktus pasirinkite reikiamus** produktus.
1. Tolesniuose „FastTab“ atnaujinkite reikiamų atributų reikšmes.

    - Bendrinami produktų publikavimo kanalai
    - Bendrai naudojami produkto atributai
    - Publikavimo kanalas
    - Kanalo produkto atributai

### <a name="define-variant-specific-attribute-values-and-define-multiple-values-for-product-attributes"></a>Apibrėžti variantui basias atributų vertes ir apibrėžti kelias produkto atributų vertes

Norėdami apibrėžti variantui b kelias produkto atributų vertes ir apibrėžti kelias vertes, atlikite šio pavyzdžio procedūros veiksmus.

1. Prisiregistruokite prie "Commerce Headquarters" kaip prekybos vadybininko.
1. Pasirinkite **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Kanalo kategorijos ir produkto atributai**.
1. Pasirinkite kanalą **„Houston“**.
1. Produktų "**FastTab**" pasirinkite reikiamą produkto variantą, tada virš produkto tinklelio **pasirinkite** Atributai.
1. Jei produktų nėra, produktų "**·** **FastTab**" pasirinkite Įtraukti, **tada dialogo lange Įtraukti produktų pasirinkite reikiamus produktų** variantus.
1. Tolesniuose „FastTab“ atnaujinkite reikiamų atributų reikšmes.

    - Bendrinami produktų publikavimo kanalai
    - Bendrai naudojami produkto atributai
    - Publikavimo kanalas
    - Kanalo produkto atributai

#### <a name="example-of-variant-specific-attribute-configuration"></a>Variantui brinkto atributo konfigūracijos pavyzdys
        
Šiame pavyzdyje P001-Bendrasis **produktas yra daugkartinės veiklos išeijimas,** kuris turi tris variantus **:** **Vykdoma,** Programos **ir** Klintys. Kiekvienam variantui norite unikaliai nurodyti veiklos atributo **vertę**. Kanalo kanalo **produktų** "FastTab" produktų "FastTab **·**" ir produkto atributų puslapyje turite nustatyti variantų veiklos atributo vertę, **kaip** parodyta pateiktoje lentelėje.

| Variantas     | Veiklos atributo vertė |
|-------------|--------------------------|
| P001 –pagrindinis | Sporto                   |
| P001–1      | Vykdoma                  |
| P001–2      | Vaikščiojimas                  |
| P001–3      | Trekas                 |

Jei vartotojas ieško "šiuo metu", ieškos **rezultatuose bus rodomas** P001 bendrasis produktas. Jei sukonfigūravote **atributą** Veikla kaip tikslinam, **·** **veiklos tikslinimo priemonė sąrašys tik sporto** šaką kaip tikslina vertę, **·** **nes ji buvo nurodyta atributui Veikla P001-bendrojo** produkto lygiu.

Pagal numatytuosius nustatymus varianto lygio atributai skirti naudoti tik produkto informacijos puslapiuose (PDPs). Kai PDP pasirenkate konkretų produkto variantą, PDP produktų specifikacijos atnaujinamos pagal tą konkretų variantą.

Norėdami, kad tikslinimo priemonės išrinktų atributų vertes, nustatytas produkto varianto lygiu, turite nurodyti atributą bendrojo produkto lygiu, **·** **pažymėti žymės langelį Leisti kelias vertes ir nustatyti atributo tipą Tekstas.**

Po to turite nustatyti visas galimas produkto variantų vertes. Šiame pavyzdyje naudojamam veiklos **atributui galimos vertės gali būti Running**, Senis, **·** **Pagalbinė**, **Kliupsingas**, Rajono,Ports **·** **·** **, Ir Tuonsports.** **·**

Nustačius, kokios turi būti varianto atributų vertės, galima nustatyti jas bendrojo produkto lygyje, naudojant nuo darbo grupės atskirtas vertes. Galite nustatyti **atributo** vertę veiklos pagrindiniame produkte kaip **Vykdoma| Į| Per | Ėjimas| Arba | Sąjiniai| Į šį prievadą.**

Tada kiekvienam variantui galite apibrėžti atributų vertes, įvesdami arba kanalus, atskirtas vertes, arba atskiras vertes. Veiklos atributui **galima** sukonfigūruoti atskirą produkto variantą kaip Vykdoma **| Į| Pasisoo**, **vykdoma**, **vykdoma| Per | Prievadai** ir t. t.

Nustačius varianto atributų vertes, **veiksmų** srities kanalo kategorijų ir produkto atributų puslapyje pasirinkite Publikuoti **kanalo naujinimus,** **tada paleiskite 1150**, **1040** **ir 1070** užduotis.

Kai užduotys baigiamos ir atnaujinamas ieškos indeksas, ieškos rezultatuose ir kategorijų naršymo rezultatuose turėtų būti rodomos visos numatomos vertės.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
