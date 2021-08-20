---
title: Palaikomi elektroninių ataskaitų formulių sudėtiniai duomenų tipai
description: Šioje temoje pateikiama informacijos apie sudedamųjų duoemnų tipo funkcijas, palaikomas modulyje Elektroninės ataskaitos (ER) formulėse.
author: NickSelin
ms.date: 06/02/2021
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72b97b2f7091883e445b2e8474ca140217bda004b0c4d8988411b9ed4209e254
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758269"
---
# <a name="supported-composite-data-types-for-electronic-reporting-formulas"></a>Palaikomi elektroninių ataskaitų formulių sudėtiniai duomenų tipai

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacijos apie sudedamųjų duoemnų tipo funkcijas, palaikomas modulyje [Elektroninės ataskaitos (ER)](general-electronic-reporting.md) formulėse. Sudėtiniai duomenų tipai yra [klasė](#class), [talpykla](#container), [įrašas](#record), [įrašų sąrašas](#record-list), ir [objektas](#object).

## <a name="class"></a><a name="class"></a>Klasė

Duomenų tipas *klasė* nurodo viešą programos klasė. ER jis pateikiamas kaip [*įrašas*](#record) kuriame yra atskiras kiekvieno viešo nuorodos klasės metodo laukas. Kai metodo iškvietimas yra parametras, taip pat turite nurodyti reikalingus atitinkamų tipų argumentus ER išraiškoje, kuri sukonfigūruota iškviesti metodą.

ER [žemėlapyje](general-electronic-reporting.md#data-model-and-model-mapping-components) ir [formatė](general-electronic-reporting.md#FormatComponentOutbound) sudedamosios dalys, kurias galite įtraukti į **Klasės** duomenų šaltinius, kurie pristatomi kaip duomenų šaltinis ir grąžina *klasės* tipo vertę. Šis duomenų šaltinis parodo viešąjį klasės, kuri gali būti iškviesta apdorojimo metu, metodus.

> [!NOTE]
> Tik vertės grąžinimo metodai gali būti iškviesti iš ER išraiškų.
>
> Iš ER išraiškų galima iškviesti tik metodus, kurių diapazonas nuo nulio iki aštuonių argumentų.

Numatytoji klasės vertė *yra* ne **neapibrėžta**.

Ši iliustracija parodo, kaip pridėtas klasės tipo **Sistemos informacija(xInfo)** duomenų šaltinį **Klasės** tipas, kuris yra įtraukiamas į elementą **xInfo** programos klasę ir iškviečia **produkto pavadinimo()** metodą, kad jis gautų esamos programos pavadinimą. Dabartinės programos pavadinimas surenkamas vykdymo metu vykdant ER duomenų modelio programinės įrangos pavadinimo `xInfo.productName` laukui **Software name(SoftwareName)** sukonfigūruotą susiejimą. Susiejimas iškviečia `productName()` metodą **xInfo** progrmaos klasę, kuri rodoma esamo modelio žemėlapyje kaip **Sistemos informacijos (xInfo)** duomenų šaltinis.

[![Klasės šaltinio konfigūravimas puslapyje ER modelio susiejimo kūrimo įrankis.](./media/er-formula-supported-data-types-composite-class1.gif)](./media/er-formula-supported-data-types-composite-class1.gif)

Šioje iliustracijoje parodyta, kaip ER formatas sukonfigūruotas pateikti programos pavadinimą sugeneruotuose dokumentuose. Laukelis **Software name(SoftwareName)** naudotų duomenų modelio buvo susietas su **eilutės** komponentu, kuris įdėtas pagal ER formato **softwareUsed** XML elementą ER formatu. Taigi, dabartinės programos pavadinimas pateikiamas vykdyklėje į **naudota programinė įranga** XML elementtą sukurtą dokumento XML formatu.

[![Elektroninio siunčiamo dokumento struktūros konfigūravimas ER formato konstruktoriuje.](./media/er-formula-supported-data-types-composite-class2.png)](./media/er-formula-supported-data-types-composite-class2.png)

## <a name="container"></a><a name="container"></a>Konteineris

Duomenų tipas *talpykla* turi susiejimo turinį. Konteinerio *vertė* gali būti naudojama perduoti tam tikrą informaciją iš saugyklos į sugeneruotą dokumentą. ER sistemoje šis duomenų tipas dažnai naudojamas norint sugeneruotuose dokumentuose pateikti laikmenos turinį, pvz., įmonės logotipą.

> [!NOTE]
> Nors kiekviena laikmenos prekė gali būti vaizduojama kaip *konteinerio* vertė, ne kiekviena *konteinerio* vertė nurodo laikmenos prekę. Todėl jei konfigūruojate ER formatą taip, kad jis naudoja *konteinerį* sugeneruotiems dokumentams padėti, bet nurodytas *konteineris* negrąžina laikmenos turinio, gali būti pateikta išimtis, panaši į toliau pateiktą pavyzdį: "Klaida vykdant kodą: Dvejetainis (objektas), metodas constructFromContainer iškviestas su netinkamais parametrais."

Numatytoji klasės vertė *konteineris* ne **neapibrėžta**.

Tolesnis paveikslėlis rodo, kaip **Bitmap(Image)** laukas tipe *konteinerio* yra susietas su duomenų modelio **Logotipo** laukeliu **Kontenerio** tipo **Pardavimo sąskaitos** duomenų modelyje. Dėl šio susiejimo įmonės logotipas tampa bet kokiu ER formatu, kuris yra skirtas **Pardavimo SF** akniniam apibrėžimui ir kuris naudoja šį modelio susiejimą vykdyklėje.

[![Konteinerio tipo, kuris yra ER modelio susiejimo konstruktorius, lauko susiejimas.](./media/er-formula-supported-data-types-composite-container.png)](./media/er-formula-supported-data-types-composite-container.png)

## <a name="record"></a><a name="record"></a>Įrašyti

Įrašas yra įvardytųjų laukų rinkinys, kiekvienas iš jų susietas su nesueitų duomenų *tipo* arba [sudėtinio duomenų tipo verte](er-formula-supported-data-types-primitive.md). Paprastai *įrašas* naudojamas vienam įrašų sąrašo įrašui pateikti. Šiuo atveju kiekviena prekė rodo atskirus laukus, metodus ir ryšius.

Numatytoji vertė *įrašo sąrašo* yra **tuščia**.

> [!NOTE]
> Kai gaunate tuščio įrašo lauko *vertę*, grąžinama numatytoji atitinkamo duomenų tipo vertė.

*Įrašas* gali būti gautas naudojant šias funkcijas:

- [FIRST](er-functions-list-first.md)
- [FIRSTORNULL](er-functions-list-firstornull.md)
- [EMPTYRECORD](er-functions-record-emptyrecord.md)
- [NULLCONTAINER](er-functions-record-nullcontainer.md)

Daugiau informacijos apie datos verčių *įraųas* ieškokite [datos ir laiko kategorijos ER kategorijų sąraše](er-functions-category-list.md).

## <a name="record-list"></a><a name="record-list"></a>Įrašų sąrašas

Įrašų *sąrašas* yra įrašų tipo elementų *sąrašas*. Paprastai įrašų *sąrašas* naudojamas įrašų, išrinktų iš duomenų bazės lentelės, sąrašui pateikti.

Numatyta, kad įrašų *sąrašo įrašai* bus pasiekti iš eilės. Norėdami pasiekti konkretų įrašą, galite naudoti funkciją [INDEX](er-functions-list-index.md) ir nurodyti *integer* indeksą.

Numatytoji vertė *įrašo sąrašo* yra **tuščia**. Galite naudoti [ISEMPTY](/er-functions-list-isempty.md) funkciją norėdami įvertinti, ar *įrašo sąrašas* yra tuščias.

> [!NOTE]
> Jei *įrašų sąrašas* tuščias, bet koks bandymas gauti lauko vertę jame sukelia *išimtį* apdorojimo metu. Norėdami sužinoti, kaip galite padėti išvengti šio tipo vykdyklės išimčių, [žr. Tuščias sąrašo atvejų svarstymas](er-components-inspections.md#i9).

*Įrašų sąrašas* gali būti pradėtas naudojant šias funkcijas:

- [ALLITEMS](er-functions-list-allitems.md)
- [ALLITEMSQUERY](er-functions-list-allitemsquery.md)
- [EMPTYLIST](er-functions-list-emptylist.md)
- [LIST](er-functions-list-list.md)
- [LISTDISTINCT](er-functions-list-listdistinct.md)

Daugiau informacijos apie datos verčių *įrašų sąrašas* ieškokite [datos ir laiko kategorijos ER kategorijų sąraše](er-functions-category-list.md). Norėdami sužinoti, kaip pristatyti *įrašų list* sąrašo, elementus, užpildykite juos programos duomenis, o tada naudokite duomenis norėdami generuoti verslo dokumentus, žr. [Sukurkite naują ER sprendimą, norėdami išspausdint](er-quick-start1-new-solution.md).

## <a name="object"></a><a name="object"></a>Objektas

Objektas *nurodo* valstybinį klasės *egzempliorių*. Paprastai *objektas* inicijuojamas šaltinio kodu. Tada jis perduotas į ER modelio susiejimą ir pateikia vykdymo konteksto informaciją.

Numatytoji klasės vertė *objektas* ne **neapibrėžta**.

Toliau esanti iliustracija rodo, kaip pridedamas objekto tipo **ReportDataContract** duomenų šaltinis *Objekto* tad informacija apie sugeneruotą SF būtų pereina iš šaltinio kodo į **Projekto sf** modelio susiejimą. Pvz., SF egzemplioriaus tekstas perduotas kaip vykdymo konteksto dalis. Šis tekstas imamas iš šaltinio kodo apdorojimo metu vykdant `ReportDataContract.parmInvoiceInstanceText` ER duomenų modelio pastabos lauke **sukonfigūruotą** susiejimą. Susiejimas iškviečia `parmInvoiceInstanceText()` metodą **PSAProjInvoiceContract** progrmaos klasę, kuri rodoma esamo modelio žemėlapyje kaip **ReportDataContract** duomenų šaltinis.

[![Objekto šaltinio konfigūravimas puslapyje ER modelio susiejimo kūrimo įrankis.](./media/er-formula-supported-data-types-composite-object.gif)](./media/er-formula-supported-data-types-composite-object.gif)

Norėdami sužinoti, kaip perkelti išsamią vykdymo konteksto informaciją iš šaltinio kodo į paleisto ER sprendimą, žr. [Kurti programos artefaktus, norėdami iškviesti sukurtą ataskaitą](er-quick-start1-new-solution.md#DevelopCustomCode).

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)
- [Elektroninių ataskaitų formulių kalba](er-formula-language.md)
- [Palaikomų primityvių duomenų tipai](er-formula-supported-data-types-primitive.md)
