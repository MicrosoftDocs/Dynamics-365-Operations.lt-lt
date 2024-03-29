---
title: Palaikomi elektroninių ataskaitų formulių sudėtiniai duomenų tipai
description: Šiame straipsnyje pateikta informacija apie sudėtinius duomenų tipus, kurie palaikomi elektroninės ataskaitos (ER) formulėse.
author: kfend
ms.date: 06/02/2021
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: ea6f8ab1f0cd26fd2414a17be559aa60fc52e7d3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272719"
---
# <a name="supported-composite-data-types-for-electronic-reporting-formulas"></a>Palaikomi elektroninių ataskaitų formulių sudėtiniai duomenų tipai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikta informacija apie sudėtinius duomenų tipus, kurie palaikomi elektroninės [ataskaitos (ER)](general-electronic-reporting.md) išraiškose. Sudėtiniai duomenų tipai yra [klasė](#class), [talpykla](#container), [įrašas](#record), [įrašų sąrašas](#record-list), ir [objektas](#object).

## <a name="class"></a><a name="class"></a>Klasė

Duomenų tipas *klasė* nurodo viešą programos klasė. ER jis pateikiamas kaip [*įrašas*](#record) kuriame yra atskiras kiekvieno viešo nuorodos klasės metodo laukas. Kai metodo iškvietimas yra parametras, taip pat turite nurodyti reikalingus atitinkamų tipų argumentus ER išraiškoje, kuri sukonfigūruota iškviesti metodą.

ER susiejime ir formato komponentuje galite įtraukti klasės duomenų šaltinį, **kuris** pateikiamas kaip duomenų šaltinis ir pateikia klasės tipo *vertę*. Šis duomenų šaltinis parodo viešąjį klasės, kuri gali būti iškviesta apdorojimo metu, metodus.

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

Numatytoji vertė *įrašo sąrašo* yra **tuščia**. Galite naudoti [ISEMPTY](er-functions-list-isempty.md) funkciją norėdami įvertinti, ar *įrašo sąrašas* yra tuščias.

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
