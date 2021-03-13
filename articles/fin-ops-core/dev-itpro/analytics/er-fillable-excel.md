---
title: Konfigūracijų kūrimas dokumentams „Excel“ formatu generuoti
description: Šioje temoje apibūdinama, kaip kurti Elektroninės ataskaitos (ER) formatą, kad būtų galima pildyti „Excel“ šabloną, o tada generuoti siunčiamus „Excel“ formato dokumentus.
author: NickSelin
manager: AnnBe
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c8d6a18741d57829d1929fb8362dc4ba8e03a1bd
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094034"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Konfigūracijos, skirtos dokumentams „Excel“ formatu generuoti, kūrimas

[!include[banner](../includes/banner.md)]

Galite sukurti [Elektroninės ataskaitos (ER)](general-electronic-reporting.md) formato konfigūraciją, kurios ER [formato komponentą](general-electronic-reporting.md#FormatComponentOutbound) galite sukonfigūruoti taip, kad siunčiamas dokumentas būtų sugeneruotas „Microsoft Excel“ darbaknygės formatu. Šiam tikslui reikia naudoti konkrečius ER formato komponentus.

Norėdami daugiau sužinoti apie šią funkciją, atlikite veiksmus, aprašytus temoje [Konfigūracijos, skirtos ataskaitoms OPENXML formatu generuoti, kūrimas](tasks/er-design-reports-openxml-2016-11.md).

## <a name="add-a-new-er-format"></a>Naujo ER formato įtraukimas

Kai įtraukiate naują ER formato konfigūraciją, kad siunčiami dokumentai būtų generuojami „Excel“ darbaknygės formatu, turite pasirinkti formato atributo **Formato tipas** reikšmę **Excel** arba atributą **Formato tipas** palikti tuščią.

- Jei pasirinksite **Excel**, galėsite konfigūruoti formatą, kad siunčiamas dokumentas būtų generuojami tik „Excel“ formatu.
- Jei atributą paliksite tuščią, galėsite konfigūruoti formatą, kad siunčiamas dokumentas būtų generuojamas bet kokiu ER sistemos palaikomu formatu.

Norėdami sukonfigūruoti konfigūracijos ER formato komponentą, veiksmų srityje pasirinkite **Dizaino įrankis** ir ER operacijų kūrimo įrankyje atidarykite ER formato komponentą, kurį norite redaguoti.

![Konfigūracijų puslapis](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>„Excel“ failo komponentas

### <a name="manual-entry"></a>Neautomatinis įrašas

Jei siunčiamą dokumentą norite generuoti „Excel“ formatu, į sukonfigūruotą ER formatą turite įtraukti komponentą **Excel\\Failas**.

![Komponentas „Excel\Failas“](./media/er-excel-format-add-file-component.png)

Norėdami nurodyti siunčiamo dokumento maketą, prie komponento **Excel\\Failas** kaip siunčiamų dokumentų šabloną pridėkite „Excel“ darbaknygę, kurios plėtinys – .xlsx.

> [!NOTE]
> Kai šabloną pridedate neautomatiniu būdu, turite naudoti [dokumento tipą](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types), kuris buvo sukonfigūruotas tam tikslui [ER parametruose](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

![Priedo pridėjimas prie komponento „Excel\Failas“](./media/er-excel-format-add-file-component2.png)

Jei norite nurodyti, kaip pridėtas šablonas bus pildomas vykdant sukonfigūruotą ER formatą, į komponentą **Excel\\Failas** turite įtraukti įterptuosius komponentus **Lapas**, **Diapazonas** ir **Langelis**. Kiekvienas įterptasis komponentas turi būti susietas su „Excel“ įvardytuoju elementu.

### <a name="template-import"></a>Šablono importavimas

Norėdami į tuščią ER formatą importuoti naują šabloną, veiksmų srities skirtuke **Importavimas** galite pasirinkti **Importuoti iš „Excel“**. Šiame pavyzdyje komponentas **Excel\\Failas** bus sukurtas automatiškai, o importuotas šablonas bus pridėtas prie jo. Visi būtinieji ER komponentai taip pat bus sukurti automatiškai, remiantis aptiktu „Excel“ įvardytųjų elementų sąrašu.

![Importavimo pasirinkimas iš „Excel“](./media/er-excel-format-import-template.png)

> [!NOTE]
> Jei redaguojamame ER formate norite sukurti pasirinktinį elementą **Lapas**, parinkties **Kurti „Excel“ lapo formato elementą** reikšmę nustatykite kaip **Taip**.

## <a name="sheet-component"></a>Lapo komponentas

Komponentas **Lapas** nurodo pridėtos „Excel“ darbaknygės darbalapį, kurį reikia užpildyti. „Excel“ šablone esančio darbalapio pavadinimas yra apbirėžtas šio komponento ypatybėje **Lapas**.

> [!NOTE]
> „Excel“ darbaknygėse, kuriose yra vienas darbalapis, šis komponentas yra pasirinktinis.

ER operacijų kūrimo įrankio skirtuke **Susiejimas** galite konfigūruoti komponento **Lapas** ypatybę **Įgalinta**, kad nustatytumėte, ar komponentas turi būti įtrauktas į sugeneruotą dokumentą.

- Jei ypatybės **Įgalinta** išraiška sukonfigūruota vykdymo laiku grąžinti reikšmę **Teisinga** arba jei nesukonfigūruota jokia išraiška, į sugeneruotą dokumentą bus įtrauktas atitinkamas darbalapis.
- Jei ypatybės **Įgalinta** išraiška sukonfigūruota vykdymo laiku grąžinti reikšmę **Klaidinga**, sugeneruotame dokumente darbalapio nebus.

![Lapo komponento pavyzdys](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Diapazono komponentas

Komponentas **Diapazonas** nurodo „Excel“ diapazoną, kurį turi kontroliuoti šis ER komponentas. Diapazono pavadinimas yra apbirėžtas šio komponento ypatybėje **„Excel“ diapazonas**.

Ypatybė **Dubliavimo kryptis** nurodo, ar diapazonas bus kartojamas sugeneruotame dokumente, ir kaip.

- Jei ypatybės **Dubliavimo kryptis** reikšmė nustatyta kaip **Dubliavimo nėra**, atitinkamas „Excel“ diapazonas nebus kartojamas sugeneruotame dokumente.
- Jei ypatybės **Dubliavimo kryptis** reikšmė nustatyta kaip **Vertikali**, atitinkamas „Excel“ diapazonas bus kartojamas sugeneruotame dokumente. Kiekvienas dubliuojamas diapazonas „Excel“ šablone yra pateikiamas po pradiniu diapazonu. Pasikartojimų skaičius apibrėžiamas duomenų šaltinio, kurio tipas – **Įrašų sąrašas** ir kuris yra susietas su šiuo ER komponentu, įrašų skaičiumi.
- Jei ypatybės **Dubliavimo kryptis** reikšmė nustatyta kaip **Horizontali**, atitinkamas „Excel“ diapazonas bus kartojamas sugeneruotame dokumente. Kiekvienas dubliuojamas diapazonas „Excel“ šablone yra pateikiamas pradinio diapazono dešinėje. Pasikartojimų skaičius apibrėžiamas duomenų šaltinio, kurio tipas – **Įrašų sąrašas** ir kuris yra susietas su šiuo ER komponentu, įrašų skaičiumi.

Norėdami daugiau sužinoti apie horizontalų dubliavimą, atlikite veiksmus, aprašytus skyriuje [Horizontaliai išplečiamų diapazonų naudojimas norint dinamiškai įtraukti stulpelius į „Excel“ ataskaitas](tasks/er-horizontal-1.md).

Komponente **Diapazonas** gali būti kitų įterptųjų ER komponentų, kurie naudojami norint įvesti reikšmes atitinkamuose „Excel“ įvardytuose diapazonuose.

- Jei reikšmėms įvesti naudojamas bet kuris grupės **Tekstas** komponentas, reikšmė „Excel“ diapazone įvedama kaip tekstinė reikšmė.

    > [!NOTE]
    > Naudokite šį šabloną, kai norite formatuoti įvestas reikšmes pagal programoje apirbrėžtą lokalę.

- Jei reikšmėms įvesti naudojamas grupės **Excel** komponentas **Langelis**, „Excel“ diapazone įvedama reikšmė yra duomenų tipo, kuris apibrėžiamas to komponento **Langelis** susiejimu (pavyzdžiui, **Eilutė**, **Realusis skaičius** arba **Sveikasis skaičius**).

    > [!NOTE]
    > Naudokite šį modelį, kad „Excel“ programa formatuotų įvestas reikšmes pagal vietinio kompiuterio, kuriame atidaromas siunčiamas dokumentas, lokalę.

ER operacijų kūrimo įrankio skirtuke **Susiejimas** galite konfigūruoti komponento **Diapazonas** ypatybę **Įgalinta**, kad nustatytumėte, ar komponentas turi būti įtrauktas į sugeneruotą dokumentą.

- Jei ypatybės **Įgalinta** išraiška sukonfigūruota vykdymo laiku grąžinti reikšmę **Teisinga** arba jei nesukonfigūruota jokia išraiška, sugeneruotame dokumente bus užpildytas atitinkamas diapazonas.
- Jei ypatybės **Įgalinta** išraiška sukonfigūruota vykdymo laiku grąžinti reikšmę **Klaidinga**, arba jei šis diapazonas neatitinka visų eilučių ar stulpelių, sugeneruotame dokumente atitinkamas diapazonas nebus užpildytas.
- Jei ypatybės **Įgalinta** išraiška sukonfigūruota vykdymo laiku grąžinti reikšmę **Klaidinga**, ir šis diapazonas atitinka visas eilutes ar stulpelius, sugeneruotame dokumente tos eilutės ir stulpeliai bus kaip paslėptos eilutės ir stulpeliai.

## <a name="cell-component"></a>Langelio komponentas

Komponentas **Langelis** naudojamas įvardytiems „Excel“ langeliams, figūroms ir paveikslėliams užpildyti. Jei norite nurodyti „Excel“ įvardytąjį objektą, kurį turi užpildyti ER komponentas **Langelis**, komponento **Langelis** ypatybėje **„Excel“ diapazonas** turite nurodyti to objekto pavadinimą.

ER operacijų kūrimo įrankio skirtuke **Susiejimas** galite konfigūruoti komponento **Langelis** ypatybę **Įgalinta**, kad nustatytumėte, ar objektas turi būti užpildytas sugeneruotame dokumente.

- Jei ypatybės **Įgalinta** išraiška sukonfigūruota vykdymo laiku grąžinti reikšmę **Teisinga** arba jei nesukonfigūruota jokia išraiška, sugeneruotame dokumente bus užpildytas atitinkamas objektas. Šio komponento **Langelis** susiejimas nurodo reikšmę, kuri įvedama atitinkamam objektui.
- Jei ypatybės **Įgalinta** išraiška sukonfigūruota vykdymo laiku grąžinti reikšmę **Klaidinga**, sugeneruotame dokumente atitinkamas objektas nebus užpildytas.

Kai komponentas **Langelis** yra sukonfigūruojamas taip, kad reikšmė būtų įvedama langelyje, jis gali būti susietas su duomenų šaltiniu, kuris grąžina primityviojo duomenų tipo reikšmę (pavyzdžiui, **Eilutė**, **Realusis skaičius** arba **Sveikasis skaičius**). Šiuo atveju langelyje reikšmė įvedama kaip to paties duomenų tipo reikšmė.

Kai komponentas **Langelis** yra sukonfigūruojamas taip, kad reikšmė būtų įvedama „Excel“ figūroje, jis gali būti susietas su duomenų šaltiniu, kuris grąžina primityviojo duomenų tipo reikšmę (pavyzdžiui, **Eilutė**, **Realusis skaičius** arba **Sveikasis skaičius**). Šiuo atveju „Excel“ figūroje reikšmė įvedama kaip tos figūros tekstas. Reikšmių, kurių duomenų tipai nėra **Eilutė**, konvertavimas į tekstą atliekamas automatiškai.

> [!NOTE]
> Galite konfigūruoti komponentą **Langelis**, kad figūra būtų užpildoma tik tais atvejais, kai palaikoma figūros teksto ypatybė.

Kai komponentas **Langelis** yra sukonfigūruojamas taip, kad reikšmė būtų įvedama „Excel“ paveikslėlyje, jis gali būti susietas su duomenų šaltiniu, kuris grąžina duomenų tipo **Konteineris**, atitinkančio dvejetainio formato vaizdą, reikšmę. Šiuo atveju reikšmė įvedama „Excel“ paveikslėlyje kaip vaizdas.

> [!NOTE]
> Laikoma, kad kiekvieno „Excel“ paveikslėlio ir figūros viršutinis kairysis kampas fiksuojamas prie konkretaus „Excel“ langelio arba diapazono. Jei norite dubliuoti „Excel“ paveikslėlį arba figūrą, turite sukonfigūruoti langelį arba diapazoną, prie kurio jis fiksuojamas, kaip dubliuojamą langelį arba diapazoną.

Norėdami sužinoti daugiau, kaip įterpti paveikslėlius ir figūras, žr. [Vaizdų ir figūrų įterpimas generuojamuose dokumentuose naudojant ER](electronic-reporting-embed-images-shapes.md).

## <a name="page-break-component"></a>Puslapio lūžio komponentas

Komponentas **Puslapio lūžis** priverčia programą „Excel“ pradėti naują puslapį. Šis komponentas nerekalingas, kai norite naudoti numatytąją „Excel“ puslapių kaitą, bet turite jį naudoti, jei norite, kad programa „Excel“ puslapių kaitai taikytų jūsų ER formatą.

## <a name="edit-an-added-er-format"></a>Pridėto ER formato redagavimas

### <a name="update-a-template"></a>Šablono naujinimas

Norėdami į redaguojamą ER formatą importuoti atnaujintą šabloną, veiksmų srities skirtuke **Importavimas** galite pasirinkti **Naujinti iš „Excel‟**. Šio proceso metu pasirinkto komponento **Excel\\Failas** šablonas bus pakeistas nauju šablonu. Redaguojamo ER formato turinys bus sinchronizuojamas su atnaujinto ER šablono turiniu.

- Jei redaguojamo formato ER formato komponentas nerandamas, kiekvienam „Excel“ pavadinimui bus automatiškai sukurtas naujas ER formato komponentas.
- Neradus atitinkamo „Excel“ pavadinimo, iš redaguojamo ER formato bus panaikinti visi ER formato komponentai.

> [!NOTE]
> Jei redaguojamame ER formate norite sukurti pasirinktinį elementą **Lapas**, parinkties **Kurti „Excel“ lapo formato elementą** reikšmę nustatykite kaip **Taip**.
>
> Jei redaguojamame ER formate iš pradžių buvo elementai **Lapas**, rekomenduojame importuojant atnaujintą šabloną parinkties **Kurti „Excel“ lapo formato elementą** reikšmę nustatyti kaip **Taip**. Priešingu atveju, visi įterptieji originalaus elemento **Lapas** elementai bus sukurti iš naujo. Todėl atnaujintame ER formate visi iš naujo sukurtų formato elementų susiejimai bus prarasti.

![„Excel“ lapo formato elemento parinkties kūrimas dialogo lange „Naujinti iš „Excel‟](./media/er-excel-format-update-template.png)

Norėdami sužinoti daugiau apie šią funkciją, atlikite veiksmus, aprašytus skyriuje [Elektroninių ataskaitų formatų modifikavimas iš naujo pritaikant „Excel“ šablonus](modify-electronic-reporting-format-reapply-excel-template.md).

## <a name="validate-an-er-format"></a>ER formato tikrinimas

Kai tikrinate redaguojamą ER formatą, atliekama vientisumo patikra, siekiant įsitikinti, ar šiuo metu naudojamame „Excel“ šablone yra „Excel“ pavadinimas. Jums bus pranešta apie neatitikimus. Kai kurių neatitikimų atveju bus pasiūlyta galimybė automatiškai ištaisyti problemas.

![Tikrinimo klaidos pranešimas](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>„Excel“ formulių skaičiavimo valdymas

Kai sugeneruojamas siunčiamas dokumentas „Microsoft Excel“ darbaknygės formatu, kai kuriuose šio dokumento langeliuose gali būti „Excel“ formulių. Įjungę funkciją **Įjungti EPPlus biblioteką Elektroninėje ataskaitų sistemoje**, galite kontroliuoti, kada formulės apskaičiuojamos, keisdami [parametro](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) **Skaičiavimo parinktys** reikšmę „Excel“ šablone, kuris naudojamas.

- Pasirinkite **Automatiškai**, jei norite perskaičiuoti visas priklausomąsias formules kiekvieną kartą, kai sugeneruotas dokumentas papildomas naujais diapazonais, langelių ir pan.
    >[!NOTE]
    > Dėl to gali kilti „Excel“ šablonų, kuriuose yra kelios susijusios formulės, našumo problema.
- Pasirinkite **Neautomatiškai**, kad formulės nebūtų perskaičiuojamos, kai generuojamas dokumentas.
    >[!NOTE]
    > Formulių perskaičiavimas neautomatiškai vykdomas, kai sugeneruotas dokumentas atidaromas peržiūrėti naudojant „Excel“.
    > Nenaudokite šios pasirinkties, jei konfigūruosite ER paskirties vietą, kuri naudoja sugeneruotą dokumentą jo neperžiūrėdama programoje „Excel“ (PDF konvertavimas, siuntimas el. paštu ir t.t.), kadangi sugeneruoto dokumento langeliuose, kuriuose yra formulių, gali nebūti reikšmių.

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

[Konfigūracijos, skirtos ataskaitoms OPENXML formatu generuoti, kūrimas](tasks\er-design-reports-openxml-2016-11.md)

[Elektroninių ataskaitų formatų modifikavimas iš naujo pritaikant „Excel“ šablonus](modify-electronic-reporting-format-reapply-excel-template.md)

[Horizontaliai išplečiamų diapazonų naudojimas norint dinamiškai įtraukti stulpelius į „Excel“ ataskaitas](tasks/er-horizontal-1.md)

[Vaizdų ir figūrų įterpimas generuojamuose dokumentuose naudojant ER](electronic-reporting-embed-images-shapes.md)

[Elektroninių ataskaitų (ER) konfigūravimas duomenims perkelti į „Power BI“](general-electronic-reporting-report-configuration-get-data-powerbi.md)
