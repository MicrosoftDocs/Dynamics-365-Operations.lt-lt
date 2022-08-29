---
title: Vaizdų ir figūrų įterpimas generuojamuose dokumentuose naudojant ER
description: Šiame straipsnyje paaiškinama, kaip naudoti elektroninį ataskaitų įrankį, norint sugeneruoti verslo dokumentus, kuriuose yra įdėtųjų vaizdų ir figūrų.
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.custom: 27621
ms.assetid: ''
ms.search.form: EROperationDesigner, ERParameters
ms.openlocfilehash: 0bb652f245db93424aeadcaadf2ad393945e616b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280995"
---
# <a name="embed-images-and-shapes-in-documents-that-you-generate-by-using-er"></a>Vaizdų ir figūrų įterpimas generuojamuose dokumentuose naudojant ER

[!include [banner](../includes/banner.md)]

Galite naudoti Elektroninių ataskaitų (ER) įrankį kurti ataskaitoms, kurias galite vykdyti reikalingų elektroninių dokumentų generavimui. Galite naudoti „Microsoft Excel” ar „Microsoft Word” dokumentus ataskaitos maketui nurodyti. ER operacijų kūrimo priemonė suteikia galimybę pridėti „Excel” arba „Word” dokumentą kaip šabloną ataskaitai. Pavadinti elementai pridėtame šablone yra susieti su ER ataskaitos formato elementais: Ataskaitos formato elementai yra susieti su duomenų šaltiniais. Šie elementai nurodo duomenis, kurie bus įtraukti į apdorojimo metu generuojamus dokumentus.

Ši nauja funkcija viršija esamas ER dokumentų „Microsoft Office” formatais kūrimo galimybes. Daugiau informacijos rasite toliau pateiktuose užduočių vedliuose. Šiuos užduočių vadovus galite rasti 7.5.4.3 Aptarnavimo/Kūrimo IT/sprendimo komponentų (10677) verslo procesų skyriuose.

- ER: konfigūracijos, skirtos generuoti ataskaitoms OPENXML formatu, kūrimas
- ER konfigūracijos, skirtos ataskaitoms „Microsoft WORD” formatu generuoti, kūrimas

## <a name="embed-an-image-in-an-excel-document"></a>Vaizdo įdėjimas į „Excel” dokumentą

### <a name="embed-an-image-in-an-excel-worksheet"></a>Vaizdo įdėjimas į „Excel” darbalapį

Visų pirma, „Excel” dokumente turite pridėti vaizdo vietos rezervavimo ženklą. Atidarykite „Excel” darbaknygę ir pridėkite paveikslėlį kaip vietos rezervavimo ženklą vaizdui, kurį įtrauksite vėliau. Tada naudodami ER įrankį įtraukite naują ER formato konfigūraciją, į kurią įtrauksite jūsų kuriamą ataskaitą. Pridėkite „Excel” darbaknygę kaip ataskaitos formato šabloną, o tada importuokite darbaknygės turinį į ER formatą. Formato apibrėžimas bus sukurtas automatiškai. Jūsų pridėtas vaizdo vietos rezervavimo ženklas bus įtrauktas į ER formato apibrėžimą kaip **LANGELIO** elementas.

> [!NOTE]
> Užuot importuodami formato apibrėžimą, galite rankiniu būdu jį nurodyti. Įrašius pakeitimus, formatas bus patikrintas.

Tada susiekite ER formato **LANGELIO** elementą su lauku iš formato duomenų šaltinio, kuris teikia paveikslėlio duomenis dvejetainiu formatu vykdymo metu. Kai ER duomenų modelis yra naudojamas kaip formato duomenų šaltinis, lauko duomenų tipas turi būti [Konteineris](er-formula-supported-data-types-composite.md#container). Šiuo metu ER duomenų modelio laukas, kuriame yra [Konteinerio](er-formula-supported-data-types-composite.md#container) duomenų tipas, gali būti susietas su keliais duomenų šaltinių tipais, kurie grąžina vaizdus dvejetainiu formatu. Naudodami Dokumentų valdymo sistemą galite pasiekti duomenų lentelės lauką ir prie duomenų lentelės įrašo pridėtą failą.

> [!IMPORTANT]
> - Jei norite užpildyti vaizdo vietos rezervavimo ženklą kuriamame dokumente naudodami „Excel” šabloną, ER formate turi būti **LANGELIO** elementas, nurodantis pavadintą paveikslėlį „Excel” šablone. Kitu atveju ataskaitos išeigoje nebus rodomas vaizdo vietos rezervavimo ženklas. Jei **LANGELIO** elemento susiejimas negrąžina jokių duomenų apdorojimo metu, sugeneruotame dokumente bus rodomas vaizdo vietos rezervavimo ženklas iš šablono. Norėdami paslėpti vaizdą generuojamame dokumente, nustatykite **LANGELIO** elementą ir nurodykite, kad **Įgalinimo** išraiška turėtų grąžinti reikšmę **KLAIDINGA**.
> - „Excel” šablone naudokite unikalų pavadinimą kiekvienam elementui. Šie elementai apima paveikslėlius ir langelius. Jei dubliuojate elemento pavadinimą, sugeneruotos ataskaitos turinys bus dviprasmiškas ir painus.

### <a name="embed-images-in-the-header-and-footer-of-an-excel-worksheet"></a>Į „Excel” darbalapio antraštę ir poraštę įdėti vaizdai

Norėdami nurodyti ataskaitos maketą, naudokite „Excel” darbaknygės dokumentą kaip šabloną. Darbaknygėje gali būti keletas darbalapių, iš kurių kiekvienas gali būti sukurtas taip, kad jame būtų antraštė ir poraštė. „Excel” palaiko iki trijų kiekvieno darbalapio antraštės ir poraštės vaizdų. Vaizdus galima lygiuoti kairėn, dešinėn arba centre.

10.0.21 „Finance” leidime galite valdyti antraštės ir poraštės vaizdus, sugeneruotus ER sprendimo, kuris turi „Excel” šabloną.

Jeigu norite, kad sugeneruoto dokumento antraštėje arba poraštėje būtų rodomas numatytasis paveikslėlis, prie ER šablono darbalapio antraštės ar poraštės galite pridėti paveikslėlį. Norėdami šį vaizdą pasiekti savo ER formatu, turite įtraukti **Paveikslėlio** komponentą formato [Antraštės](er-fillable-excel.md#header-component) arba [Poraštės](er-fillable-excel.md#footer-component) komponente. Konfigūruokite **Paveikslėlio** komponento lygiuotę, kaip reikalinga. 

Taip pat galite naudoti **Paveikslėlio** komponentą, kad į sugeneruoto dokumento antraštę arba poraštę būtų galima įtraukti vaizdą apdorojimo metu, net jei šablone nėra numatytojo vaizdo. Norėdami nurodyti laikmenos turinį, kuris turėtų būti įdėtas į sugeneruoto dokumento antraštę arba poraštę kaip naujas vaizdas arba numatytojo vaizdo pakaitalas, turite susieti **Paveikslėlio** komponentą su [Konteinerio](er-formula-supported-data-types-composite.md#container) tipo duomenų šaltiniu, kuris reiškia vaizdą dvejetainiu formatu.

Kiekviename **Antraštės** arba **Poraštės** komponente gali būti vienas **Paveikslėlio** komponentas kiekvienai palaikomai lygiuotei: **Kairės**, **Centro** ir **Dešinės**.

**Paveikslėlio** komponento ypatybė **Aukščio keitimas** leidžia jums naudoti sukonfigūruotą susiejimą, kad būtų galima valdyti paveikslėlio dydį:

- Pasirinkite **Pradinis**, jei norite išlaikyti pradinį vaizdo dydį.
- Pasirinkite **Santykinis** vaizdo aukščio dydžiui proporcingai su tą paveikslėlį laikančios antraštės arba poraštės aukščiu.

    - Šiuo atveju vaizdo aukštis turi būti apibrėžtas kaip pirminės antraštės arba poraštės procentinė dalis.
    - Jei dydžio keitimo vertė viršija 100 procentų, vaizdas gali persidengti su atitinkamo darbalapio duomenų sritimi.
    - Jei vaizdo aukštis keičiamas, kai taikomas dydžio keitimas, plotis taip pat pakeičiamas, kad būtų išlaikoma pradinė vaizdo proporcija.

- Pasirinkite **Absoliutusis**, jei norite pakeisti vaizdo dydį, atsižvelgiant į dizaino metu pateikiamas aukščio ir pločio vertes (pikseliais).

    - Jei nurodytas aukštis viršija pirminės antraštės arba poraštės aukštį, vaizdas gali persidengti su atitinkamo darbalapio duomenų sritimi.

Taip pat galite naudoti **Paveikslėlio** komponento ypatybę **Įgalinta**, kad valdytumėte vaizdo, įdėto į sugeneruotą dokumentą naudojant šį komponentą, matomumą.

> [!NOTE]
> Turite naudoti ER formato kūrimo įrankį, kad pridėtumėte **Paveikslėlio** komponentą į redaguotiną ER formatą. Negalite įtraukti komponento, kai naudojate [Verslo dokumentų valdymo](er-business-document-management.md) darbo sritį verslo dokumento šablono redagavimui.

Norėdami sužinoti daugiau apie šią funkciją, atlikite veiksmus skyriuje [ER formato kūrimas generuoti ataskaitai „Excel” formatu su įdėtaisiais paveikslėliais puslapių antraštėse arba poraštėse](er-embed-images-header-footer-excel-reports.md).

## <a name="embed-a-shape-in-an-excel-document"></a>Formos įdėjimas į „Excel” dokumentą

Visų pirma, „Excel” dokumente turite pridėti formos vietos rezervavimo ženklą. Atidarykite „Excel” darbaknygę ir pasirinkite **Forma**, **Teksto langas** ar **„WordArt”** kaip formos vietos rezervavimo ženklą. Tada naudodami ER įrankį įtraukite naują ER formato konfigūraciją, į kurią įtrauksite jūsų kuriamą ataskaitą. Pridėkite „Excel” darbaknygę kaip ataskaitos formato šabloną, o tada importuokite darbaknygės turinį į ER formatą. Formato apibrėžimas bus sukurtas automatiškai. Įtrauktas formos vietos rezervavimo ženklas bus įtrauktas į ER formato apibrėžimą kaip **LANGELIO** elementas, nurodantis pavadintą „Excel” formos elementą.

> [!NOTE]
> Užuot importuodami formato apibrėžimą, galite rankiniu būdu jį nurodyti. Įrašius pakeitimus, formatas bus patikrintas.

Tada susiekite **LANGELIO** elementą ER formate su lauku iš formato duomenų šaltinio, kuris teikia duomenis vykdymo metu. Šie duomenys gali būti sukonvertuoti į teksto eilutę. Kai ER formato **LANGELIO** elementas nurodo tekstą palaikantį„Excel” šablono formos elementą, tekstas, pateiktas šiuo susiejimu, vykdymo metu bus rodomas sugeneruoto dokumento formoje.

> [!IMPORTANT]
> - Jei norite naudoti „Excel” šabloną, kuriame yra formos vietos rezervavimo ženklas naujam dokumentui generuoti, ER formate turi būti **LANGELIO** elementas, nurodantis „Excel” formos elementą. Kitu atveju ataskaitos išeigoje nebus rodomas formos vietos rezervavimo ženklas. Jei **LANGELIO** elemento, kuris nurodo įvardytąjį „Excel” formos elementą, susiejimas negrąžina jokių duomenų apdorojimo metu, sugeneruotame dokumente bus rodomas formos vietos rezervavimo ženklo tekstas iš „Excel” šablono. Norėdami paslėpti formą generuojamame dokumente, nustatykite **LANGELIO** elementą, nurodantį įvardytąjį „Excel” formos elementą ir nurodykite, kad **Įgalinimo** išraiška turėtų grąžinti reikšmę **KLAIDINGA**.
> - „Excel” šablone naudokite unikalų pavadinimą kiekvienam elementui. Šie elementai apima formas ir langelius. Jei dubliuojate elemento pavadinimą, sugeneruotos ataskaitos turinys bus dviprasmiškas ir painus.

## <a name="embed-an-image-in-a-word-document"></a>Vaizdo įdėjimas į „Word” dokumentą
> [!IMPORTANT]
> Galite pakartotinai naudoti ER formatą, kuris naudoja „Excel” šabloną kurti dokumentams, kuriuose yra įdėtųjų vaizdų. ER formate įsitikinkite, kad **LANGELIO** elementui, kuris nurodo įvardytą paveikslėlio elementą „Excel” programoje, nurodytas pavadinimas ir tai, kad jis susietas su duomenų šaltiniu, vykdymo metu grąžinančiu paveikslėlį.

Pirmiausia turite sukonfigūruoti „Word” dokumento maketą. Naudokite **Paveikslėlio turinio** valdiklį, kad sukurtumėte įdėtojo vaizdo vietos rezervavimo ženklą. Norėdami pasiekti šį valdiklį, pirmiausia padarykite **Programuotojo** skirtuką matomą „Word” juostoje.

Po to panaikinkite „Excel” šabloną iš ER formato ir pridėkite „Word” šablono dokumentą. Atnaujinkite nuorodą į šabloną ir įrašykite pakeitimus. Dabartinio ER formato struktūra įrašoma „Word” šabloną kaip nauja pasirinktinė XML dalis, pavadinta **Ataskaita**.

Po to įrašykite dabartinio ER formato „Word” šabloną savo vietiniame kompiuteryje. Atidarykite šabloną ir **XML susiejimo** sritį. Raskite pasirinktinę XML dalį, pavadintą **Ataskaita**, ir tada pažymėkite ER ataskaitos **LANGELIO** elementą, kuris yra susietas su duomenų šaltiniu, pateikiančiu vaizdą dvejetainiu formatu. Susiekite šį XML dalies elementą su pasirinktu **Paveikslėlio turinio** valdikliu ir įrašykite pakeitimus.

[![įdėtieji vaizdai.](./media/embed-images-shapes-01.png)](./media/embed-images-shapes-01.png)

Galiausiai, panaikinkite „Word” šabloną iš ER formato ir pridėkite „Word” dokumentą, kuriame yra susietos pasirinktinės XML dalys. Atnaujinkite formato nuorodą į šabloną ir įrašykite atliktus šio ER formato keitimus.

## <a name="more-information"></a>Daugiau informacijos
Norėdami susipažinti su šios funkcijos informacija, skaitykite užduočių vadovų rinkinį, **ER Kurti ataskaitas „MS Office” formatais su įdėtais vaizdais**. Šie užduočių vedliai parodo, kaip galite įdėti įmonės logotipo vaizdus ir autorizuotus asmenų parašus į mokėjimo čekius, kurie generuojami naudojant ER įrankį „Excel” ir „Word” dokumentuose.

Šioje lentelėje pateikiami failai, reikalingi norint užbaigti **ER Kurti ataskaitas „MS Office” formatais su įdėtais vaizdais** užduočių vedlius. Atsisiųskite ir įrašykite failus savo vietiniame kompiuteryje.

| Aprašas                                          | Failo vardas                   |
|------------------------------------------------------|-----------------------------|
| ER duomenų modelio konfigūracija                          | [cheques.xml šablonas](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| ER formato konfigūracija                              | [Čekių spausdinimas formatas.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| Įmonės logotipo vaizdas                                   | [Įmonės logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| Parašo vaizdas                                      | [Parašo vaizdas.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| Alternatyvus parašo vaizdas                          | [Signature image 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| „Microsoft Word“ mokėjimo čekių spausdinimo šablonas  | [Cheque template Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |
| „Microsoft Excel“ mokėjimo čekių spausdinimo šablonas | [„Čekio šablonas.xlsx”](https://download.microsoft.com/download/1/f/6/1f671963-73aa-48d5-ae69-45f21fe7dfb4/Cheque%20template.xlsx)        |

Šiame grafike pateikiamas mokėjimo čekio, sugeneruoto iš „Excel” šablono, bandomojo spaudinio pavyzdys.

[![Mokėjimo čekio bandomasis spaudinys.](./media/embed-images-shapes-02.png)](./media/embed-images-shapes-02.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
