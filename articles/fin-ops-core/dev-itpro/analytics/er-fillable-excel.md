---
title: Konfigūracijų kūrimas dokumentams „Excel“ formatu generuoti
description: Šioje temoje apibūdinama, kaip kurti Elektroninės ataskaitos (ER) formatą, kad būtų galima pildyti „Excel“ šabloną, o tada generuoti siunčiamus „Excel“ formato dokumentus.
author: NickSelin
ms.date: 03/25/2022
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ec25065f2e3cc3b5dd3c9004d5330447f7b2ac61
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645141"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Konfigūracijos, skirtos dokumentams „Excel“ formatu generuoti, kūrimas

[!include[banner](../includes/banner.md)]

Galite sukurti elektroninės ataskaitos [(ER)](general-electronic-reporting.md) formato konfigūraciją, kuri turi ER formato komponentą, kurį galite konfigūruoti, kad sugeneruotų siunčiamą dokumentą darbaknygės Microsoft Excel formatu. Šiam tikslui reikia naudoti konkrečius ER formato komponentus.

Norėdami daugiau sužinoti apie šią funkciją, atlikite veiksmus, aprašytus temoje [Konfigūracijos, skirtos ataskaitoms OPENXML formatu generuoti, kūrimas](tasks/er-design-reports-openxml-2016-11.md).

## <a name="add-a-new-er-format"></a>Naujo ER formato įtraukimas

Kai įtraukiate naują ER formato konfigūraciją, kad siunčiami dokumentai būtų generuojami „Excel“ darbaknygės formatu, turite pasirinkti formato atributo **Formato tipas** reikšmę **Excel** arba atributą **Formato tipas** palikti tuščią.

- Jei pasirinksite **Excel**, galėsite konfigūruoti formatą, kad siunčiamas dokumentas būtų generuojami tik „Excel“ formatu.
- Jei atributą paliksite tuščią, galėsite konfigūruoti formatą, kad siunčiamas dokumentas būtų generuojamas bet kokiu ER sistemos palaikomu formatu.

Norėdami sukonfigūruoti konfigūracijos ER formato komponentą, veiksmų srityje pasirinkite **Dizaino įrankis** ir ER operacijų kūrimo įrankyje atidarykite ER formato komponentą, kurį norite redaguoti.

![Puslapis Konfigūracijos.](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>„Excel“ failo komponentas

### <a name="manual-entry"></a>Neautomatinis įrašas

Jei siunčiamą dokumentą norite generuoti „Excel“ formatu, į sukonfigūruotą ER formatą turite įtraukti komponentą **Excel\\Failas**.

![Komponentas „Excel\Failas“.](./media/er-excel-format-add-file-component.png)

Norėdami nurodyti siunčiamo dokumento maketą, prie komponento **Excel\\Failas** kaip siunčiamų dokumentų šabloną pridėkite „Excel“ darbaknygę, kurios plėtinys – .xlsx.

> [!NOTE]
> Kai šabloną pridedate neautomatiniu būdu, turite naudoti [dokumento tipą](../../../fin-ops-core/fin-ops/organization-administration/configure-document-management.md#configure-document-types), kuris buvo sukonfigūruotas tam tikslui [ER parametruose](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

![Priedo pridėjimas prie komponento „Excel\Failas“.](./media/er-excel-format-add-file-component2.png)

Jei norite nurodyti, kaip pridėtas šablonas bus pildomas vykdant sukonfigūruotą ER formatą, į komponentą **Excel\\Failas** turite įtraukti įterptuosius komponentus **Lapas**, **Diapazonas** ir **Langelis**. Kiekvienas įterptasis komponentas turi būti susietas su „Excel“ įvardytuoju elementu.

### <a name="template-import"></a>Šablono importavimas

Norėdami į tuščią ER formatą importuoti naują šabloną, veiksmų srities skirtuke **Importavimas** galite pasirinkti **Importuoti iš „Excel“**. Šiame pavyzdyje komponentas **Excel\\Failas** bus sukurtas automatiškai, o importuotas šablonas bus pridėtas prie jo. Visi būtinieji ER komponentai taip pat bus sukurti automatiškai, remiantis aptiktu „Excel“ įvardytųjų elementų sąrašu.

![Importavimo pasirinkimas iš „Excel“.](./media/er-excel-format-import-template.png)

> [!NOTE]
> Jei redaguojamame ER formate norite sukurti pasirinktinį elementą **Lapas**, parinkties **Kurti „Excel“ lapo formato elementą** reikšmę nustatykite kaip **Taip**.

## <a name="sheet-component"></a>Lapo komponentas

Komponentas **Lapas** nurodo pridėtos „Excel“ darbaknygės darbalapį, kurį reikia užpildyti. „Excel“ šablone esančio darbalapio pavadinimas yra apibrėžtas šio komponento ypatybėje **Lapas**.

> [!NOTE]
> „Excel“ darbaknygėse, kuriose yra vienas darbalapis, šis komponentas yra pasirinktinis.

ER operacijų kūrimo įrankio skirtuke **Susiejimas** galite konfigūruoti komponento **Lapas** ypatybę **Įgalinta**, kad nustatytumėte, ar komponentas turi būti įtrauktas į sugeneruotą dokumentą.

- Jei ypatybės **Įgalinta** išraiška sukonfigūruota vykdymo laiku grąžinti reikšmę **Teisinga** arba jei nesukonfigūruota jokia išraiška, į sugeneruotą dokumentą bus įtrauktas atitinkamas darbalapis.
- Jei ypatybės **Įgalinta** išraiška sukonfigūruota vykdymo laiku grąžinti reikšmę **Klaidinga**, sugeneruotame dokumente darbalapio nebus.

![Lapo komponento pavyzdys.](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Diapazono komponentas

### <a name="nested-components"></a>Įdėtųjų komponentų

#### <a name="data-typing"></a>Duomenų įvedimas

Diapazono **komponente** gali būti kitų įdėtųjų ER komponentų, naudojamų norint įvesti vertes į atitinkamus diapazonus.

- Jei reikšmėms įvesti naudojamas bet kuris grupės **Tekstas** komponentas, reikšmė „Excel“ diapazone įvedama kaip tekstinė reikšmė.

    > [!NOTE]
    > Naudokite šį šabloną, kai norite formatuoti įvestas reikšmes pagal programoje apibrėžtą lokalę.

- **Jei vertėms** **įvesti naudojamas Excel** grupės langelio komponentas, vertė įvedama į Excel **diapazoną kaip duomenų tipo vertė, kurią apibrėžia to langelio komponento susiejimas**. Pvz., duomenų tipas gali būti **Eilutė**, **Real** arba **Integer**.

    > [!NOTE]
    > Naudokite šį modelį, kad „Excel“ programa formatuotų įvestas reikšmes pagal vietinio kompiuterio, kuriame atidaromas siunčiamas dokumentas, lokalę.

#### <a name="row-handling"></a>Eilučių tvarkymas

Diapazono **komponentas** gali būti konfigūruojamas kaip vertikaliai dubliuotas, kad Excel darbalapyje būtų sugeneruotos kelios eilutės. Eilutes gali generuoti pirminis diapazono **komponentas** arba jo įdėtieji diapazono **komponentai**.

Versijoje 10.0.26 ir vėliau galite priversti sugeneruotą darbalapį, kad sugeneruotos eilutės būtų tame pačiame puslapyje. ER formato konstruktoriuje **pirminį** **·** **diapazono** komponentą redaguojamu ER formatu nustatykite pasirinktį Išlaikyti eilutes kartu kaip Taip. Tada ER bandys saugoti visą turinį, sugeneruotą to paties puslapio diapazono. Jei turinio aukštis viršija likusį dabartinio puslapio tarpą, bus įtrauktas puslapio lūžis, o turinys bus rodomas kito naujo puslapio viršuje.

> [!NOTE]
> Rekomenduojame konfigūruoti pasirinktį Išlaikyti **eilutes kartu tik** diapazonams, kurie apima visą sugeneruoto dokumento plotį.
>
> Parinktis **Išlaikyti eilutes kartu** taikoma tik "Excel" **failo \> komponentams**, kurie sukonfigūruoti naudoti "Excel" darbaknygės šabloną.
>
> Parinktis **Išlaikyti eilutes** kartu gali būti naudojama tik tada, kai **įgalinta parinktis Įgalinti EP² bibliotekos naudojimą elektroninės** ataskaitų sistemos priemonėje.
>
> Šią funkciją galima naudoti diapazono **komponentams**, kurie yra puslapio **komponente**. Tačiau nėra garantijos, kad puslapio poraštės [bendrosios sumos bus teisingai apskaičiuotos](er-paginate-excel-reports.md#add-data-sources-to-calculate-page-footer-totals) naudojant duomenų [rinkinio duomenų](er-data-collection-data-sources.md) šaltinius.

Norėdami sužinoti, kaip naudoti šią pasirinktį, [atlikite pavyzdinį veiksmus dalyje ER formato kūrimas, kad eilutės būtų išlaikytos tame pačiame Excel puslapyje](er-keep-excel-rows-together.md).

### <a name="replication"></a>Dubliavimas

Dublikato **krypties** ypatybė nurodo, ar diapazonas bus kartojamas sugeneruotame dokumente:

- **Nėra dubliavimo** – atitinkamas "Excel" diapazonas nebus kartojamas sugeneruotame dokumente.
- **Vertikalus** – atitinkamas Excel diapazonas sugeneruotame dokumente bus pakartotas vertikaliai. Kiekvienas dubliuotas diapazonas Excel šablone bus žemiau pradinio diapazono. Pasikartojimų skaičius apibrėžiamas duomenų šaltinio, kurio tipas – **Įrašų sąrašas** ir kuris yra susietas su šiuo ER komponentu, įrašų skaičiumi.
- **Horizontalus** – sugeneruotame dokumente atitinkamas Excel diapazonas bus pakartotas horizontaliai. Kiekvienas dubliuotas diapazonas excel šablone bus naudojamas į dešinę nuo pradinio diapazono. Pasikartojimų skaičius apibrėžiamas duomenų šaltinio, kurio tipas – **Įrašų sąrašas** ir kuris yra susietas su šiuo ER komponentu, įrašų skaičiumi.

    Norėdami daugiau sužinoti apie horizontalų dubliavimą, atlikite veiksmus, aprašytus skyriuje [Horizontaliai išplečiamų diapazonų naudojimas norint dinamiškai įtraukti stulpelius į „Excel“ ataskaitas](tasks/er-horizontal-1.md).

### <a name="enabling"></a>Įjungiama

ER operacijų kūrimo įrankio skirtuke **Susiejimas** galite konfigūruoti komponento **Diapazonas** ypatybę **Įgalinta**, kad nustatytumėte, ar komponentas turi būti įtrauktas į sugeneruotą dokumentą.

- Jei ypatybės **Įgalinta** išraiška sukonfigūruota vykdymo laiku grąžinti reikšmę **Teisinga** arba jei nesukonfigūruota jokia išraiška, sugeneruotame dokumente bus užpildytas atitinkamas diapazonas.
- Jei ypatybės **Įgalinta** išraiška sukonfigūruota vykdymo laiku grąžinti reikšmę **Klaidinga**, arba jei šis diapazonas neatitinka visų eilučių ar stulpelių, sugeneruotame dokumente atitinkamas diapazonas nebus užpildytas.
- Jei ypatybės **Įgalinta** išraiška sukonfigūruota vykdymo laiku grąžinti reikšmę **Klaidinga**, ir šis diapazonas atitinka visas eilutes ar stulpelius, sugeneruotame dokumente tos eilutės ir stulpeliai bus kaip paslėptos eilutės ir stulpeliai.

### <a name="resizing"></a>Dydžio keitimas

Galite konfigūruoti savo Excel šabloną, kad jis galėtų naudoti langelius tekstiniams duomenims pateikti. Norėdami užtikrinti, kad sugeneruotame dokumente būtų matomas visas langelio tekstas, galite sukonfigūruoti, kad langelis automatiškai nulaužti tekstą jame. Taip pat galite konfigūruoti eilutę, kurioje yra šis langelis, kad automatiškai būtų koreguojamas jo aukštis, jei viršelio tekstas nematomas. Norėdami gauti daugiau informacijos, žr. skyrių "Sulaužyti tekstą langelyje" [, kuris yra išjungtas langeliuose](https://support.microsoft.com/office/fix-data-that-is-cut-off-in-cells-e996e213-6514-49d8-b82a-2721cef6144e).

> [!NOTE]
> [Dėl žinomo Excel](https://support.microsoft.com/topic/you-cannot-use-the-autofit-feature-for-rows-or-columns-that-contain-merged-cells-in-excel-34b54dd7-9bfc-6c8f-5ee3-2715d7db4353) apribojimo, net jei konfigūruojate langelius, kad įsilaužtų tekstas, ir konfigūruojate eilutes, kuriose yra tų langelių, kad automatiškai pakoreguotų jų aukštį, kad tilptų tekstas, gali būti taip, kad sulietiems langeliams ir eilutėms, kuriose yra tų langelių, **gali būti, kad negalėsite naudoti funkcijos AutoFit** **ir Tikrinimo** teksto Excel. 

Kaip ir "Dynamics 365" finansų versija 10.0.23, kai dirbate su sugeneruotu dokumentu, galite priversti ER apskaičiuoti kiekvienos eilutės aukštį, kuris buvo sukonfigūruotas taip, kad automatiškai atitiktų įdėtųjų langelių turinį, kai vienoje eilutėje yra bent vienas sulietas langelis, kuris buvo sukonfigūruotas uždengti tekstą jame. Apskaičiuotas aukštis naudojamas eilutei pakeisti, kad sugeneruotame dokumente būtų matomi visi eilutės langeliai.

> [!NOTE]
> Žinokite, kad ši funkcija gali neveikti kaip tikėtasi, kai pasirinktinis šriftas naudojamas sulietai langeliui formatuoti. Kadangi "Excel" neįterpa pasirinktinių šriftų, ji teikia ne informaciją apie pasirinktinį šrifto dydį. Todėl gali būti netinkamai įvertintas susieto langelio dydis.

Jei norite pradėti naudoti šią funkciją, paleisdami bet kuriuos ER formatus, sukonfigūruotus naudoti Excel šablonus siunčiamams dokumentams generuoti, atlikite šiuos veiksmus.

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Susiję saitai** pasirinkite **Elektroninių ataskaitų parametrai**.
3. Elektroninių ataskaitų **parametrų puslapyje**, skirtuke **Runtime**, nustatykite pasirinktį **Automatiškai įtraukti eilutės aukštį** kaip **Taip**.

Norėdami pakeisti šią taisyklę vienam ER formatui, atnaujinkite to formato juodraščio versiją, atlikite šiuos veiksmus.

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos** dalyje pasirinkite plytelę **Konfigūracijų ataskaitos**.
3. Konfigūracijos **puslapio**, konfigūracijos medžio kairiojoje srityje, pasirinkite ER konfigūraciją, skirtą naudoti Excel šabloną siunčiamams dokumentams generuoti.
4. **Versijos** „FastTab“, pasirinkite konfigūravimo versiją, kuri turi statusą **Juodraštis**.
5. Veiksmų srityje pasirinkite **Dizaino įrankis**.
6. Skirtuko Formatų **konstruktorius** puslapyje, kairiojoje srityje esančioje formato medyje, pasirinkite "Excel" komponentą, kuris susietas su Excel šablonu.
7. **Skirtuko Formatas** **lauke** Koreguoti eilutės aukštį pasirinkite vertę, norėdami nurodyti, ar ER turėtų būti naudojamas vykdymo metu, norint pakeisti siunčiamo dokumento, sugeneruoto redaguojamo ER formato, eilučių aukštį:

    - **Numatyta** – naudokite bendrąjį parametrą, kuris sukonfigūruotas **lauke Automatiškai taikyti eilutės aukštį** elektroninių **ataskaitų parametrų** puslapyje.
    - **Taip** – nepaisyti bendrojo parametro ir pakeisti eilutės aukštį vykdyklėje.
    - **Ne** – nepaisyti bendrojo parametro ir vykdymo metu nekeiskite eilutės aukščio.

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

Komponentas **Puslapio lūžis** priverčia programą „Excel“ pradėti naują puslapį. Šis komponentas nereikalingas, kai norite naudoti numatytąją „Excel“ puslapių kaitą, bet turite jį naudoti, jei norite, kad programa „Excel“ puslapių kaitai taikytų jūsų ER formatą.

## <a name="page-component"></a><a name="page-component"></a>Puslapio komponentas

### <a name="overview"></a>Peržiūra

Galite naudoti **Puslapio** komponentą, kai norite, kad „Excel” vadovautųsi jūsų ER formatu ir struktūros išdėstymu puslapiuose sugeneruotame gaunamame dokumente. Kai ER formatas vykdo komponentus, kurie yra po **Puslapio** komponentu, būtini puslapių lūžiai įtraukiami automatiškai. Šio proceso metu atsižvelgiama į sugeneruoto turinio dydį, „Excel” šablono puslapio nustatymą ir „Excel” šablone pasirinktą popieriaus dydį.

Jei turite suskaidyti sugeneruotą dokumentą į skirtingus skyrius, kurių kiekvienas jų turi skirtingą puslapių numeraciją, galite sukonfigūruoti kelis **Puslapio** komponentus kiekviename [lapo](er-fillable-excel.md#sheet-component) komponente.

### <a name="structure"></a><a name="page-component-structure"></a>Struktūra

Jei pirmasis komponentas po **Puslapio** komponentu yra [Diapazono](er-fillable-excel.md#range-component) komponentas, kurio **Replikavimo krypties** ypatybė nustatyta į **Jokio replikavimo**, šis diapazonas yra laikomas puslapių numeracijos puslapio antraštė, pagrįsta dabartinio **Puslapio** komponento parametrais. Su šiuo formato komponentu susietas „Excel” diapazonas yra kartojamas kiekvieno puslapio, sugeneruoto naudojant dabartinio **Puslapio** komponento parametrus, viršuje.

> [!NOTE]
> Tam, kad puslapių numeracija būtų teisinga, diapazonas [Viršuje kartotinos eilutės](https://support.microsoft.com/office/repeat-specific-rows-or-columns-on-every-printed-page-0d6dac43-7ee7-4f34-8b08-ffcc8b022409) yra konfigūruojamas jūsų „Excel” šablone, šio „Excel” diapazono adresas turi būti toks pat, kaip ir „Excel” diapazono, susieto su anksčiau aprašytu **Diapazono** komponentu.

Jei paskutinis komponentas po **Puslapio** komponentu yra **Diapazono** komponentas, kurio **Replikavimo krypties** ypatybė nustatyta į **Jokio replikavimo**, šis diapazonas yra laikomas puslapių numeracijos puslapio poraštė, pagrįsta dabartinio **Puslapio** komponento parametrais. Su šiuo formato komponentu susietas „Excel” diapazonas yra kartojamas kiekvieno puslapio, sugeneruoto naudojant dabartinio **Puslapio** komponento parametrus, pabaigoje.

> [!NOTE]
> Tam, kad puslapių numeracija būtų teisinga, su **Diapazono** komponentais susietų „Excel” diapazonų dydis neturėtų būti pakeistas vykdymo metu. Mes nerekomenduojame formatuoti šio diapazono langelių naudojant **Laužti tekstą langelyje** ir **Automatinis eilutės aukščio taikymas** „Excel” [parinkčių](https://support.microsoft.com/office/wrap-text-in-a-cell-2a18cff5-ccc1-4bce-95e4-f0d4f3ff4e84).

Galite įtraukti kitus **Diapazono** komponentus tarp pasirinktinių **Diapazono komponentų**, kad nurodytumėte, kaip sugeneruoti dokumentai yra užpildomi.

Jei įdėtųjų **Diapazono** komponentų rinkinys, esantis po **Puslapio** komponentu neatitinka su anksčiau aprašyta struktūra, įvyksta tikrinimo [klaida](er-components-inspections.md#i17) kūrimo metu ER formatų rengyklėje. Klaidos pranešimas informuos jus, kad triktis gali sukelti problemų vykdymo metu.

> [!NOTE]
> Norėdami sugeneruoti tinkamą išvestį, nenurodykite susiejimo jokiam **Diapazono** komponentui, esančiam po **Puslapio** komponentu, jei **Replikavimo krypties** ypatybė tam **Diapazono** komponentui yra nustatyta į **Jokio replikavimo**, o diapazonas yra sukonfigūruotas generuoti puslapio antraštes arba poraštes.

Jei norite, kad su puslapių numeracija susijęs sumavimas ir skaičiavimas skaičiuotų puslapio vykdomas sumas ir sumas, rekomenduojame konfigūruoti reikiamus [Duomenų rinkimo](er-data-collection-data-sources.md) duomenų šaltinius. Norėdami sužinoti, kaip naudoti **Puslapio** komponentą sugeneruoto „Excel” dokumento puslapių išdėstymui, atlikite procedūras, aprašytas [ER formato kūrimas sugeneruoto dokumento „Excel” formatu puslapių išdėstymui](er-paginate-excel-reports.md).

### <a name="limitations"></a><a name="page-component-limitations"></a>Apribojimai

Kai naudojate **Puslapio** komponentą „Excel” puslapių išdėstymui, jūs nežinosite galutinio sugeneruoto dokumento puslapio skaičiaus tol, kol puslapių išdėstymas nebus užbaigtas. Todėl negalite apskaičiuoti bendro puslapių skaičiaus naudodami ER formules ir atspausdinti teisingo sugeneruoto dokumento puslapių skaičiaus bet kuriame puslapyje prieš paskutinį puslapį.

> [!TIP]
> Norėdami pasiekti šį rezultatą „Excel” antraštėje arba poraštėje, naudokite specialų „Excel” [formatavimą](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) antraštėms ir poraštėms.

Sukonfigūruotų puslapio **komponentų** neį atsižvelgiama, kai atnaujinate "Excel" šabloną redaguojamu formatu "Dynamics 365" finansų versijoje 10.0.22. Ši funkcija yra svarstoma būsimiems „Finance” leidimams.

Jei konfigūruojate savo „Excel” šabloną, kad būtų naudojamas [sąlyginis formatavimas](/office/dev/add-ins/excel/excel-add-ins-conditional-formatting), jis tam tikrais atvejais gali neveikti taip, kaip tikėjotės.

### <a name="applicability"></a>Taikymas

**Puslapio** komponentas veikia [„Excel” failo](er-fillable-excel.md#excel-file-component) formato komponentui tik tada, kai komponentas sukonfigūruotas naudoti „Excel” šabloną. Jei [pakeisite](tasks/er-design-configuration-word-2016-11.md) „Excel” šabloną „Word” šablonu ir tada paleisite redaguojamą ER formatą, **Puslapio** komponento bus nepaisoma.

**Puslapio** komponentas veikia tik tada, kai **Įgalinti „EPPlus” bibliotekos naudojimą elektroninių ataskaitų sistemoje** funkcija yra įjungta. Išimtis pateikiama apdorojimo metu, jei ER bando apdoroti **Puslapio** komponentą, kai ši funkcija išjungta.

> [!NOTE]
> Išimtis pateikiama apdorojimo metu, jei ER formatas apdoroja **Puslapio** komponentą „Excel” šablonui, kuriame yra bent viena formulė, nurodanti netinkamą langelį. Norėdami išvengti vykdymo klaidų, ištaisykite „Excel” šabloną, kaip aprašyta skyriuje [Kaip ištaisyti #REF! klaidą](https://support.microsoft.com/office/how-to-correct-a-ref-error-822c8e46-e610-4d02-bf29-ec4b8c5ff4be).

## <a name="footer-component"></a>Poraštės komponentas

**Poraštė** komponentas naudojamas norint užpildyti poraštes sugeneruoto darbalapio „Excel” darbaknygėje apačioje.

> [!NOTE]
> Šį komponentą galite įtraukti į kiekvieną **Lapas** komponentą, kad sugeneruotoje „Excel” darbaknygėje būtų galima nurodyti skirtingas skirtingų darbalapių poraštes.

Konfigūruodami atskirą **Poraštė** komponentą, galite naudoti **Antraštės / poraštės išvaizda** ypatybę, kad nurodytumėte puslapius, kuriuose poraštė naudojama. Galimos šios vertės:

- **Bet kokia** – paleiskite sukonfigūruotą **Poraštė** komponentą, kuris skirtas bet kuriam pirminio „Excel” darbalapio puslapiui.
- **Pirma** – paleiskite sukonfigūruotą **Poraštė** komponentą, kuris skirtas tik pirmam pirminio „Excel” darbalapio puslapiui.
- **Lyginis** – paleiskite sukonfigūruotą **Poraštė** komponentą, kuris skirtas lyginiams pirminio „Excel” darbalapio puslapiams.
- **Nelyginis** – paleiskite sukonfigūruotą **Poraštė** komponentą, kuris skirtas nelyginiams pirminio „Excel” darbalapio puslapiams.

Vienam **Lapas** komponentui, galite pridėti kelis **Poraštė** komponentus, kurio kiekvieno **Antraštės / poraštės išvaizda** ypatybė turi skirtingą vertę. Tokiu būdu „Excel” darbalapyje galite sugeneruoti skirtingas skirtingo tipo puslapių poraštes.

> [!NOTE]
> Įsitikinkite, kad kiekvienas jūsų pridėtas **Poraštė** komponentas vienam **Lapas** komponentui turi skirtingą **Antraštės / poraštės išvaizda** ypatybės vertę. Priešingu atveju įvyksta [tikrinimo klaida](er-components-inspections.md#i16). Klaidos pranešimas, kurį gaunate, praneša apie nesutapimą.

Po pridėto **Poraštė** komponentu pridėkite **Tekstas\\Eilutė**, **Tekstas\\Datos laikas** arba kito tipo būtinus įdėtus komponentus. Norėdami nurodyti, kaip užpildoma jūsų puslapio poraštė, sukonfigūruokite tų komponentų susiejimus.

Taip pat galite naudoti specialius [formatavimo kodus](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) norėdami teisingai suformuoti sugeneruotos poraštės turinį. Norėdami sužinoti, kaip naudoti šį būdą, atlikite [1 pavyzdyje](#example-1) žemiau šioje temoje aprašytus veiksmus.

> [!NOTE]
> Konfigūruodami ER formatus, nepamirškite atsižvelgti į „Excel” [limitą](https://support.microsoft.com/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3) ir didžiausią vienos antraštės ar poraštės simbolių skaičių.

## <a name="header-component"></a>Antraštės komponentas

**Antraštė** komponentas naudojamas norint užpildyti antraštes sugeneruoto darbalapio „Excel” darbaknygėje viršuje. Jis naudojamas kaip **Poraštė** komponentas.

## <a name="edit-an-added-er-format"></a>Pridėto ER formato redagavimas

### <a name="update-a-template"></a>Šablono naujinimas

Norėdami į redaguojamą ER formatą importuoti atnaujintą šabloną, veiksmų srities skirtuke **Importavimas** galite pasirinkti **Naujinti iš „Excel‟**. Šio proceso metu pasirinkto komponento **Excel\\Failas** šablonas bus pakeistas nauju šablonu. Redaguojamo ER formato turinys bus sinchronizuojamas su atnaujinto ER šablono turiniu.

- Jei redaguojamo formato ER formato komponentas nerandamas, kiekvienam „Excel“ pavadinimui bus automatiškai sukurtas naujas ER formato komponentas.
- Neradus atitinkamo „Excel“ pavadinimo, iš redaguojamo ER formato bus panaikinti visi ER formato komponentai.

> [!NOTE]
> Jei redaguojamame ER formate norite sukurti pasirinktinį elementą **Lapas**, parinkties **Kurti „Excel“ lapo formato elementą** reikšmę nustatykite kaip **Taip**.
>
> Jei redaguojamame ER formate iš pradžių buvo elementai **Lapas**, rekomenduojame importuojant atnaujintą šabloną parinkties **Kurti „Excel“ lapo formato elementą** reikšmę nustatyti kaip **Taip**. Priešingu atveju, visi įterptieji originalaus elemento **Lapas** elementai bus sukurti iš naujo. Todėl atnaujintame ER formate visi iš naujo sukurtų formato elementų susiejimai bus prarasti.

![„Excel“ lapo formato elemento parinkties kūrimas dialogo lange Naujinti iš „Excel”.](./media/er-excel-format-update-template.png)

Norėdami sužinoti daugiau apie šią funkciją, atlikite veiksmus, aprašytus skyriuje [Elektroninių ataskaitų formatų modifikavimas iš naujo pritaikant „Excel“ šablonus](modify-electronic-reporting-format-reapply-excel-template.md).

## <a name="validate-an-er-format"></a>ER formato tikrinimas

Kai tikrinate redaguojamą ER formatą, atliekama vientisumo patikra, siekiant įsitikinti, ar šiuo metu naudojamame „Excel“ šablone yra „Excel“ pavadinimas. Jums bus pranešta apie neatitikimus. Kai kurių neatitikimų atveju bus pasiūlyta galimybė automatiškai ištaisyti problemas.

![Tikrinimo klaidos pranešimas.](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>„Excel“ formulių skaičiavimo valdymas

Kai sugeneruojamas siunčiamas dokumentas „Microsoft Excel“ darbaknygės formatu, kai kuriuose šio dokumento langeliuose gali būti „Excel“ formulių. Įjungę funkciją **Įjungti EPPlus biblioteką Elektroninėje ataskaitų sistemoje**, galite kontroliuoti, kada formulės apskaičiuojamos, keisdami [parametro](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) **Skaičiavimo parinktys** reikšmę „Excel“ šablone, kuris naudojamas.

- Pasirinkite **Automatiškai**, jei norite perskaičiuoti visas priklausomąsias formules kiekvieną kartą, kai sugeneruotas dokumentas papildomas naujais diapazonais, langelių ir pan.

    > [!NOTE]
    > Dėl to gali kilti „Excel“ šablonų, kuriuose yra kelios susijusios formulės, našumo problema.

- Pasirinkite **Neautomatiškai**, kad formulės nebūtų perskaičiuojamos, kai generuojamas dokumentas.

    > [!NOTE]
    > Formulių perskaičiavimas neautomatiškai vykdomas, kai sugeneruotas dokumentas atidaromas peržiūrėti naudojant „Excel“.
    > Nenaudokite šios pasirinkties, jei konfigūruosite ER paskirties vietą, kuri naudoja sugeneruotą dokumentą jo neperžiūrėdama programoje „Excel“ (PDF konvertavimas, siuntimas el. paštu ir t.t.), kadangi sugeneruoto dokumento langeliuose, kuriuose yra formulių, gali nebūti reikšmių.

## <a name="example-1-format-footer-content"></a><a name="example-1"></a>1 pavyzdys – formato poraštės turinys

1. Naudokite pateiktas ER konfigūracijas [sugeneruoti](er-generate-printable-fti-forms.md) spausdintiną laisvos formos SF (FTI) dokumentą.
2. Peržiūrėkite sugeneruoto dokumento poraštę. Atkreipkite dėmesį, kad joje yra informacijos apie dabartinio puslapio numerį ir bendrą dokumento puslapių skaičių.

    ![Peržiūrėti sugeneruoto dokumento poraštę „Excel” formatu.](./media/er-fillable-excel-footer-1.gif)

3. ER formato kūrimo įrankyje, [atidarykite](er-generate-printable-fti-forms.md#features-that-are-implemented-in-the-sample-er-format) ER formato pavyzdį jį peržiūrėti.

    **Sąskaita faktūra** darbalapio poraštė sugeneruota pagal dviejų **Eilutė** komponentų, priklausančių **Poraštė** komponentui, nustatymus:

    - Pirmasis **Eilutė** komponentas užpildo šiuos specialius formatavimo kodus, dėl to „Excel” pritaikys specialų formatavimą:

        - **&C** – lygiuoti poraštės tekstą centre.
        - **& "Segoe UI,Reguliarus"&8** – pateikti poraštės tekstą "Segoe UI Regular"8 taškų šriftu.

    - Antrasis **Eilutė** komponentas užpildo tekstą, kuriame yra dabartinis puslapio numeris ir bendras puslapių skaičius dabartiniame dokumente.

    ![Peržiūrėkite ER formato komponento poraštę Formato kūrimo įrankio puslapyje.](./media/er-fillable-excel-footer-2.png)

4. Pritaikykite ER formato pavyzdį, kad modifikuotumėte dabartinę puslapio poraštę:

    1. [Kurkite](er-quick-start2-customize-report.md#DeriveProvidedFormat) išvestinį **Laisvos formos teksto pasirinktinė SF (Excel)** ER formatą, pagrįstą ER formato pavyzdžiu.
    2. Pridėkite primą naują **Eilutė** komponentų porą, skirtą **Poraštė** **Sąskaita faktūra** darbalapio komponentui:

        1. Pridėkite **Eilutė** komponentą, sulygiuojantį įmonės pavadinimą kairėje ir pateikiantį "Segoe UI Regular" 8 dydžio šriftu (**"&L&"Segoe UI,Regular"&8"**).
        2. Pridėkite **Eilutė** komponentą, užpildančią įmonės pavadinimą (**model.InvoiceBase.CompanyInfo.Name**).

    3. Pridėkite antrą naują **Eilutė** komponentų porą, skirtą **Poraštė** **Sąskaita faktūra** darbalapio komponentui:

        1. Pridėkite **Eilutė** komponentą, sulygiuojantį apdorojimo datą dešinėje ir pateikiantį "Segoe UI Regular" 8 dydžio šriftu (**"&R&"Segoe UI,Regular"&8"**).
        2. Pridėkite **Eilutė** komponentą, užpildantį apdorojimo datą pasirinktame formate (**"&nbsp;„&DATEFORMAT(SESSIONTODAY(), „metai-mėnuo-diena”)**).

        ![ER formato komponento poraštės Formato kūrimo įrankio puslapyje peržiūra.](./media/er-fillable-excel-footer-3.png)

    4. [Užpildykite](er-quick-start2-customize-report.md#CompleteDerivedFormat) išvestinę **Laisvos formos teksto pasirinktinė SF (Excel)** ER formato juodraščio versiją.

5. [Sukonfigūruokite](er-generate-printable-fti-forms.md#configure-print-management) spausdinimo tvarkymą, kad pasinaudotumėte išvestine **Laisvos formos teksto pasirinktinė SF (Excel)** ER formato versija, o ne ER formato pavyzdžiu.
6. Sugeneruokite spausdintiną FTI dokumentą ir peržiūrėkite sugeneruoto dokumento poraštę.

    ![Sugeneruoto dokumento poraštę „Excel” formatu poraštės peržiūra.](./media/er-fillable-excel-footer-4.gif)

## <a name="example-2-fixing-the-merged-cells-epplus-issue"></a><a name="example-2"></a> 2 pavyzdys: Sulietų langelių EP Tarpo išdavimo nustatymas

Norėdami generuoti siunčiamą dokumentą Excel darbaknygės formatu, galite paleisti ER formatą. Kai funkcijų **valdymo darbo srityje įgalintas** **EP** Pagal elektroninių ataskaitų sistemos funkciją įgalintas EP Pagal bibliotekos naudojimo įgalinimas, ["EPVz"biblioteka](https://www.nuget.org/packages/epplus/4.5.2.1) naudojama Excel išvestims atlikti. Tačiau dėl žinomo [Excel](https://answers.microsoft.com/msoffice/forum/all/deleting-a-range-of-cells-that-includes-merged/8601462c-4e2c-48e0-bd23-848eecb872a9) veikimo būdo ir EPVz., bibliotekos apribojimo galite susidurti su šia išimtimi: "Negalima panaikinti / perrašyti sulietų langelių. Diapazonas iš dalies sulietas su kitu susieuotu diapazonu. Norėdami sužinoti, kokio tipo "Excel" šablonai gali sukelti šią išimtį ir kaip galite išspręsti problemą, atlikite toliau nurodytą pavyzdį.

1. Excel kompiuterio programoje sukurkite naują Excel darbaknygę.
2. Darbalapio **Sheet1** pridėkite **langelio A2 ReportTitle** **pavadinimą**.
3. Sulieti **langelius A1** ir **A2**.

    ![Peržiūrėkite langelių A1 ir A2 suliejimo rezultatus "Excel" kompiuterio programos sukurta "Excel" darbaknygėje.](./media/er-fillable-excel-example2-1.png)

3. Konfigūracijos puslapyje **pridėkite** naują [ER formatą, kad](er-fillable-excel.md#add-a-new-er-format) sugeneruotumėte siunčiamą dokumentą Excel darbaknygės formatu.
4. Formato kūrimo **puslapyje,** importuokite [sukurtą](er-fillable-excel.md#template-import) Excel darbaknygę į pridėtą ER formatą kaip naują siunčiamų dokumentų šabloną.
5. Skirtuke **Susiejimas** sukonfigūruokite langelio **tipo ReportTitle** komponento [susiejimą](er-fillable-excel.md#cell-component).
6. Paleiskite sukonfigūruotą ER formatą. Atkreipkite dėmesį, kad pateikta ši išimtis: "Negalima panaikinti / perrašyti sulietų langelių. Diapazonas iš dalies sulietas su kitu susieuotu diapazonu.

    ![Konfigūruojamo ER formato darbo formato peržiūra formato konstruktoriaus puslapyje.](./media/er-fillable-excel-example2-2.png)

Galite išspręsti problemą vienu iš šių būdų:

- **Lengviau, bet nerekomenduojama:** funkcijų valdymo darbo **srityje išjunkite** bibliotekos Įgalinti EP Workspace naudojimą elektroninės ataskaitų sistemos **priemonėje**. Nors šis būdas yra paprastesnis, jei jį naudojate, gali kilti kitų problemų, nes kai kurios ER **funkcijos palaikomos tik tada, kai elektroninių ataskaitų sistemos priemonėje įgalinta bibliotekos Įgalinti EP Yra** naudojimas.
- **Rekomenduojama: atlikite** šiuos veiksmus:

    1. Excel kompiuterio programoje modifikuokite Excel darbaknygę vienu iš šių būdų:

        - Darbalapio **Sheet1 atsieti** **A1 ir** **A2 langelius**.
        - **Pakeiskite ReportTitle** **pavadinimo nuorodą iš =Sheet1!$A$2** į **=Sheet1!$A$1**.

        ![Peržiūrėkite nuorodos keitimo rezultatus excel kompiuterio programos sukurtame Excel darbaknygėje.](./media/er-fillable-excel-example2-3.png)

    2. Puslapyje Formatų **konstruktorius** importuokite modifikuotą [Excel darbaknygę į redaguojamą ER formatą,](er-fillable-excel.md#template-import) kad atnaujinkite esamą šabloną.
    3. Paleisti modifikuotą ER formatą.

        ![Peržiūrėkite sugeneruotą dokumentą "Excel" darbalaukio programoje.](./media/er-fillable-excel-example2-4.png)

## <a name="limitations"></a>Apribojimai

### <a name="known-epplus-library-limitations"></a>Žinomos EP Yra bibliotekos apribojimai

#### <a name="external-data-sources"></a>Išorinių duomenų šaltiniai

Jei viename iš jūsų šablonų yra PivotTable PowerPivot [...](https://support.microsoft.com/office/create-a-pivottable-with-an-external-data-source-db50d01d-2e1c-43bd-bfb5-b76a818a927b), pagrįstą modeliu, kuris susijęs su išoriniu duomenų šaltiniu, **ir įgalintas EPIklis** bibliotekos naudojimas elektroninės ataskaitų sistemos priemonėje, jūs gaunate tokį klaidos pranešimą, kai paleidžiate ER formatą, kuris naudoja tą šabloną siunčiamam dokumentui Excel formatu generuoti: "Talpyklos šaltinis nėra darbalapis". Norėdami išspręsti šią problemą, turite šias pasirinktis:

- **Rekomenduojama:** perprojektuoti jūsų naudojate "Excel" sprendimą:

    1. Išsąskite dalį, kurioje yra suvestinės, atskiroje Excel darbaknygėje (A darbaknygėje). 
    2. Naudokite ER, norėdami sugeneruoti antrą Excel darbaknygę (B darbaknygę) iš finansų, kuri turi reikiamą informaciją. 
    3. Iš karto sugeneravote B darbaknygę, žr. darbaknygę B.

- Išjunkite funkciją, įgalinti **EP Tarpinės bibliotekos naudojimą elektroninėje** ataskaitų sistemoje, kad būtų galima naudoti kitą pasirinktį, nei EP². 

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

[Konfigūracijos, skirtos ataskaitoms OPENXML formatu generuoti, kūrimas](tasks\er-design-reports-openxml-2016-11.md)

[Elektroninių ataskaitų formatų modifikavimas iš naujo pritaikant „Excel“ šablonus](modify-electronic-reporting-format-reapply-excel-template.md)

[Horizontaliai išplečiamų diapazonų naudojimas norint dinamiškai įtraukti stulpelius į „Excel“ ataskaitas](tasks/er-horizontal-1.md)

[Vaizdų ir figūrų įterpimas generuojamuose dokumentuose naudojant ER](electronic-reporting-embed-images-shapes.md)

[Elektroninių ataskaitų (ER) konfigūravimas duomenims perkelti į „Power BI“](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
