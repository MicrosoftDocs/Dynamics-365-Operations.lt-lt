---
title: Daugiakalbių pranešimų Elektroninėse ataskaitose kūrimas
description: Šiame straipsnyje paaiškinama, kaip kurti ir generuoti ataskaitas keliomis kalbomis, naudojant elektroninių ataskaitų (ER) žymes.
author: kfend
ms.date: 05/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
ms.openlocfilehash: 5575ba3154521e3855ce6b97c5b37d3c4868e3e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285492"
---
# <a name="design-multilingual-reports-in-electronic-reporting"></a>Daugiakalbių pranešimų Elektroninėse ataskaitose kūrimas

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Peržiūra

Verslo vartotojai naudoja [Elektroninių ataskaitų (ER)](general-electronic-reporting.md) sistemą, kad konfigūruotų siunčiamų dokumentų formatus, kurie turi būti sugeneruoti pagal įvairių šalių ar regionų teisinius reikalavimus. Šiuos reikalavimuose nurodoma, kad siunčiami dokumentai būtų generuojami skirtingomis kalbomis skirtingoms šalims ar regionams, galite konfigūruoti vieną ar kelis ER formatus, kuriuose yra nuo kalbos priklausančių išteklių. Tokiu būdu galite pakartotinai naudoti formatą, kad sugeneruotumėte siunčiamus dokumentus įvairioms šalims ir regionams. Taip pat galite naudoti vieną ER formatą, kad sugeneruotumėte siunčiamą dokumentą skirtingomis kalbomis atitinkamiems klientams, tiekėjams, filialams ar kitoms šalims.

Galite konfigūruoti ER duomenų modelius ir modelio susiejimus kaip konfigūruotų ER formatų duomenų šaltinius, kad apibrėžtume duomenų srautą, nurodantį, kokie programos duomenys įdedami į generuojamus dokumentus. Kaip ER konfigūravimo paslaugų [teikėjas galite](general-electronic-reporting.md#Provider)[skelbti sukonfigūruotus duomenų modelius, modelio išdėstymus ir formatus kaip ER](tasks/er-upload-configuration-into-lifecycle-services.md#upload-a-configuration-into-lcs) sprendimo komponentus, norėdami sugeneruoti konkrečius siunčiamus dokumentus. Taip pat galite leisti klientams [įkelti](general-electronic-reporting-manage-configuration-lifecycle.md) publikuotą ER sprendimą, kad jį būtų galima naudoti ir tinkinti. Jei tikitės, kad klientai kalba kitomis kalbomis, galite sukonfigūruoti ER komponentus, kad juose būtų nuo kalbos priklausantys ištekliai. Tokiu būdu redaguojamo ER komponento turinys gali būti pateiktas kliento vartotojo pageidaujama kalba projektavimo metu.

Galite konfigūruoti nuo kalbos priklausančius išteklius kaip ER žymas. Tada galite naudoti šias žymas, kad sukonfigūruotumėte ER komponentus šiais tikslais:

- Projektavimo metu:

    - Pateikite konfigūruojamų ER komponentų turinį vartotojo pageidaujama kalba.

- Apdorojimo metu:

    - Sugeneruokite siunčiamų dokumentų nuo kalbos priklausantį turinį.
    - Pateikite įspėjimų ir klaidos pranešimus vartotojo pageidaujama kalba.
    - Paraginkite užpildyti privalomus laukus vartotojo pageidaujama kalba.

Galite konfigūruoti ER žymas kiekvienai ER [konfigūracijai](general-electronic-reporting.md#Configuration), kurioje yra skirtingi komponentai. Žymos gali būti tvarkomos neatsižvelgiant į sukonfigūruotą ER duomenų modelių, ER modelių susiejimų ir ER formatų komponentų logiką.

Kiekviena ER žyma identifikuojama pagal ID unikaliu ER konfigūracijos, kuriai priklauso ta žyma, aprėptyje. Kiekvienoje žymėje gali būti kiekvienos kalbos, kurią palaiko dabartinis 365 finansų Microsoft Dynamics egzempliorius, žymės tekstas. Į šias palaikomas kalbas įeina įdiegtų organizacijų kalbos.

## <a name="entry"></a>Įrašas

Kai kuriate ER duomenų modelį, ER modelių susiejimą ar ER formatą, **Išversti** parinktis rodoma kiekvieną kartą jums pasirinkus lauką, kuriame yra verstinas tekstas. Jums pasirinkus šią pasirinktį, galite susieti pasirinktą lauką su ER žyma **Teksto vertimas** <a name="TextTranslationPane">srityje </a>. Galite pasirinkti esamą ER žymą arba pridėti naują ER žymą, jei jos dar nėra. Jums pasirinkus ar pridėjus ER žymą, galite pridėti susijusį tekstą bet kuriai kalbai, palaikomai dabartinėje „Finance” programoje.

Toliau pateiktoje iliustracijoje parodyta, kaip šis vertimas atliekamas redaguotame ER duomenų modelyje. Šiame pavyzdyje **Aprašas** atributas **PirkimoUžsakymas** lauko, skirtas redaguotam **Sąskaitos faktūros šablonas**, išverčiamas į austrų vokiečių (de-at) ir japonų (ja) kalbas.

![ER žymos vertimo ER duomenų modelio kūrimo įrankyje pateikimas.](./media/er-multilingual-labels-refer.png)

Gali būti išverstas tik žymų, kurios yra redaguojamame ER komponente, tekstas. Pavyzdžiui, jei pasirinksite **Išversti**, skirtą ER modelio susiejimo duomenų šaltinio žymės atributui, ir pasirinksite ER žymą, esančią pirminiame ER duomenų modelyje, pamatysite žymos turinį, bet negalėsite jo pakeisti. Tokiais atvejais **Išverstas tekstas** lauko negalėsite naudoti kaip parodyta šioje iliustracijoje.

![ER žymos pateikto vertimo ER modelio susiejimų kūrimo įrankyje peržiūra.](./media/er-multilingual-labels-refer-mapping.png)

> [!NOTE]
> Negalite naudoti kūrimo įrankių, kad panaikintumėte žymą, įvestą redaguojamame ER komponente.

## <a name="scope"></a>Apimtis

ER žymas galima nurodyti keliuose verstiniuose ER komponentų atributuose.

### <a name="data-model-component"></a>Duomenų modelio komponentas

Konfigūruodami ER duomenų modelį, galite jam pridėti ER žymas. **Žyma** ir **Aprašas** modelio prekės atributai, kiekvienas modelio laukas ir kiekvienas <a id="LinkModelEnum"></a>modelio išvardijimo vertė gali būti susiejami su ER žyma, pridėta į ER duomenų modelį.

![Atributo aprašo vertimo pateikimas ER duomenų modelio kūrimo įrankyje.](./media/er-multilingual-labels-refer.png)

Kai taip sukonfigūruojate ER duomenų modelį, jo turinys bus pateiktas ER duomenų modelio kūrimo įrankio vartotojams kiekviena vartotoja pageidaujama kalba. Todėl modelio priežiūra supaprastinta. Toliau pateiktose iliustracijose rodoma, kaip ši funkcija veikia vartotojams, besinaudojantiems DE-AT ir JA rinkiniu jų pageidaujama kalba.

![ER duomenų modelio kūrimo įrankio maketas vartotojui, besinaudojančiam DE-AT rinkiniu kaip jo pageidaujama kalba.](./media/er-multilingual-labels-refer-de.png)

![ER duomenų modelio kūrimo įrankio maketas vartotojui, besinaudojančiam JA rinkiniu kaip jo pageidaujama kalba.](./media/er-multilingual-labels-refer-ja.png)

### <a name="model-mapping-component"></a>Modelio susiejimo komponentas

Kadangi ER modelio susiejimas yra pagrįstas ER duomenų modeliu, nurodytų duomenų modelio elementų žymės vartotojo pageidaujama kalba bus rodomos modelių susiejimo konstruktoriuje. Toliau pateiktoje iliustracijoje rodoma, kaip **PirkimoUžsakymas** lauko vertė yra paaiškinta redaguotame modelio susiejime naudojant **Aprašas** atributą, pridėtą konfigūruotame duomenų modelyje. Atkreipkite dėmesį, kad ši žyma pateikiama vartotojo pageidaujama kalba (šiuo atveju, DE-AT).

![ER modelio susiejimų kūrimo įrankio maketas vartotojui, besinaudojančiam DE-AT rinkiniu jo pageidaujama kalba.](./media/er-multilingual-labels-show-mapping.png)

Kai **Žyma** atributas **Vartotojo įvesties parametras** duomenų šaltinio yra susietas su ER žyma, parametro laukas, atitinkantis šį duomenų šaltinį, pateikiamas vartotojo dialogo lange apdorojimo metu vartotojams jų pageidaujama kalba.

### <a name="format-component"></a>Formato komponentas

Kai konfigūruojate ER formatą, galite jam pridėti ER žymas. Kiekvieno sukonfigūruoto duomenų šaltinio **Žyma** ir **Pagalbos tekstas** atributai gali būti susieti su ER žyma, pridėta prie ER formato. Kiekvieno **formato** išvardijimo **·**<a id="LinkFormatEnum"></a> vertės žymos ir aprašymo atributus taip pat galima susieti su ER žyme, kuri pasiekiama iš redaguojamo ER formato.

> [!NOTE]
> Taip pat galite susieti šiuos atributus su pirminio ER duomenų modelio ER žyma, kuri iš naujo panaudoja modelio žymas kiekviename ER formate, sukonfigūruotame šiame ER duomenų modeliui.

Kai taip sukonfigūruojate ER formatą, jo formato turinys bus pateiktas „ER Operation” kūrimo įrankio vartotojams kiekviena vartotoja pageidaujama kalba. Todėl konfigūruojamos logikos formato priežiūra ir analizė yra supaprastintos.

Dėl to, kad ER formatas pagrįstas ER duomenų modeliu, nurodytos žymos duomenų modelio elementuose pateikiamos ER formato kūrimo įrankyje vartotojo pageidaujama kalba.

Kai **Žyma** atributas **Vartotojo įvesties parametras** duomenų šaltinio yra susietas su ER žyma, laukas, atitinkantis parametrą vartotojo dialogo lange apdorojimo metu, pateikiamas vartotojui kaip paraginimas. Toliau pateiktoje iliustracijose rodoma, kaip galima susieti **Žyma** atributą **Vartotojo įvesties parametras** duomenų šaltinį kūrimo metu su ER žyma, kad vartotojai būtų raginami įvesti parametrą skirtingose vartotojo pageidaujamose kalbose rodoma anglų (Jungtinių Valstijų (EN-ES) ir DE-AT kalbomis) vykdymo metu.

![Vartotojo įvesties parametro atributų vertimo pateikimas „ER Operation” kūrimo įrankyje.](./media/er-multilingual-labels-refer-format.png)

![ER teikėjo mokėjimo apdorojimas apdorojimo metu EN-US vartotojo pageidaujama kalba.](./media/er-multilingual-labels-show-runtime-en.png)

![ER teikėjo mokėjimo apdorojimas apdorojimo metu DE-AT vartotojo pageidaujama kalba.](./media/er-multilingual-labels-show-runtime-de.png)

### <a name="expressions"></a>Išraiškos

Norėdami panaudoti žymą ER [išraiškoje](er-formula-language.md), turite naudoti sintaksę **@„GER\_ŽYMA: X”**, kurioje prefiksas **@** nurodo, kad operandas nurodo žymą, **GER\_ŽYMA** nurodo, kad ER žyma yra, o **X** yra ER žymos ID.

![ER išraiškos, kurioje yra nuoroda į ER žymą, konfigūravimas ER formulės kūrimo įrankyje.](./media/er-multilingual-labels-expression1.png)

Norėdami nurodyti sistemos (programos) žymą, naudokite sintaksę **@„X”**, kurioje prefiksas nurodo, **@**, kad operandas nurodo žymę, o **X** yra sistemos žymos ID.

![ER išraiškos, kurioje yra nuoroda į programos žymą, konfigūravimas ER formulės kūrimo įrankyje.](./media/er-multilingual-labels-expression2.png)

#### <a name="model-mapping"></a>Modelio susiejimas

Naudojant žymą, galite sukonfigūruoti ER modelio susiejimo išraišką. Kai šį susiejimą iškviečia ER formatas, paleistas generuoti siunčiamą dokumentą, vykdymo kontekste yra kalbos kodas. Sukonfigūruota išraiškos žyma bus užpildyta žymos tekstu, sukonfigūruotu pagal to konteksto kalbą.

Jeigu nurodyta žyma neturi formato vykdymo konteksto, iškviečiančio modelio susiejimą, kalbos vertimo, vietoj to, naudojamas žymos tekstas EN-US kalba.

#### <a name="format"></a>Formatuoti

Naudojant žymas, galite sukonfigūruoti ER formato ER išraišką. Kai šis formatas paleidžiamas sugeneruoti siunčiamą dokumentą, vykdymo kontekste yra kalbos kodas. Sukonfigūruota išraiškos žyma bus užpildyta žymos tekstu, sukonfigūruotu pagal to konteksto kalbą.

![Redaguojamos ER išraiškos ER žymos vertimo pateikimas ER formulės kūrimo įrankyje.](./media/er-multilingual-labels-refer-in-expression.png)

![Duomenų susiejimo, nurodančio ER žymą, pavyzdys „ER Operation” kūrimo įrankyje.](./media/er-multilingual-labels-refer-in-binding.png)

Galite sukonfigūruoti ER formato **FAILAS** komponentą, kad sugeneruotumėte ataskaitą vartotojo pageidaujama kalba.

![Nustatykite FAILO komponentą „ER Operation” kūrimo įrankyje, kad sugeneruotumėte ataskaitą vartotojo pageidaujama kalba.](./media/er-multilingual-labels-language-context-user.png)

Jei taip sukonfigūruosite ER formatą, ataskaita bus sugeneruota naudojant atitinkamą ER žymų tekstą. Toliau pateiktose iliustracijose pateikiami EN-US ir DE-AT vartotojų kalbų ataskaitų pavyzdžiai.

![Ataskaitos, sugeneruotos EN-US vartotojo pageidaujama kalba, peržiūra.](./media/er-multilingual-labels-report-preview-en.png)

![Ataskaitos, sugeneruotos DE-AT vartotojo pageidaujama kalba, peržiūra.](./media/er-multilingual-labels-report-preview-de.png)

Jeigu nurodyta žyma neturi formato vykdymo konteksto kalbos vertimo, vietoj to, naudojamas žymos tekstas EN-US kalba.

> [!TIP]
> Galite naudoti aplanką ir **atskirų** tipų RINKMENos komponentus **redaguojamu** ER formatu, norėdami nurodyti, kaip sugeneruotas siunčiamas failas. Norėdami pavadinti sugeneruotą failą, sukonfigūruokite [komponento parametro](er-formula-language.md) Failo vardas **ER** išraišką. Žymės gali būti naudojamas sukonfigūruotoje išraiškoje. Kadangi failo **vardo** parametras pagal numatytuosius nustatymus yra agnostinis, visų šioje išraiškoje nurodomų žymių tekstas rodomas numatytąja EN-US kalba vykdyklėje. Tačiau versijoje 10.0.28 **ir vėlesnėje versijoje galite įgalinti parametrą Kalbos nuostatos taikyti išraiškos funkcijai** Failo vardas. Tada **atliekant** nustatymą failo vardo **išraiška** atsižvelgiama į kalbos nuostatų parametrą.

## <a name="language"></a>Kalba

ER palaiko skirtingus būdus nurodyti generuotos ataskaitos kalbą. **Kalbos prioritetai** lauke **Formatas** skirtuke galite pasirinkti šias vertes:

- **Įmonės prioritetas** – sugeneruokite ataskaitą įmonėje nurodyta kalba.

    ![Nurodykite „ER Operation” kūrimo įrankyje įmonės pageidaujamą kalbą kaip sugeneruotos ataskaitos kalbą.](./media/er-multilingual-labels-language-context-company.png)

- **Vartotojo prioritetas** – sugeneruokite ataskaitą vartotojo pageidaujama kalba.
- **Išsamiai apibrėžta** – sugeneruokite ataskaitą kalba, nurodyta kūrimo metu.

    ![Nurodykite „ER Operation” kūrimo įrankyje kūrimo laiku nurodytą kalbą kaip sugeneruotos ataskaitos kalbą.](./media/er-multilingual-labels-language-context-fixed.png)

- **Apibrėžta apdorojimo metu** – sugeneruokite ataskaitą kalba, nurodyta apdorojimo metu. Jei pasirinksite šią vertę lauke **Kalba**, sukonfigūruokite ER išraišką, gražinančią kalbos kodą kalbai, pavyzdžiui, atitinkamo kliento kalbą.

    ![Nurodykite „ER Operation” kūrimo įrankyje apdorojimo metu nurodytą kalbą kaip sugeneruotos ataskaitos kalbą.](./media/er-multilingual-labels-language-context-runtime.png)

## <a name="culture-specific-formatting"></a>Nuo kultūris priklausantis formatavimas

ER palaiko skirtingus būdus nurodyti nuo kultūros priklausomą sugeneruotą ataskaitą. Todėl tinkamas formatavimas kultūrai gali būti naudojamas datos, laiko ir skaitinių verčių atveju. Jums kuriant ER formatą, **Formato** skirtuke **Kultūros ypatybės** laukelyje galite pasirinkti vieną iš tolesnių verčių kiekvienam formato komponentui **Bendras\\Failas**, **„Excel“\\Failas**, **PDF\\Failas**, ar **PDF\\Suliejimo** tipas:

- **Vartotojo nuostatos** – formatuoti vertes pagal vartotojo pageidaujamą kultūras. Šis kultūra apibrėžiama vartotojo pasirinkčių puslapio nuostatų skirtuko lauke **Data** **laikas** ir **skaičiaus** formatas.

    ![Vartotojo pageidaujamo kultūros, kaip sugeneruotos ataskaitos principas ER operacijų konstruktoriuje, apibrėžimas.](./media/er-multilingual-labels-culture-context-user-preferred.png)

- **Tiesiogiai apibrėžta** – formatuoti vertes pagal dizaino metu nurodytą reikšmę.

    ![Kultūros nustatymas yra konkretus numatytu laiku kaip pagal kultūrą sukurta ataskaita ER operacijų kūrimo įrankyje.](./media/er-multilingual-labels-culture-context-fixed.png)

- **Nustatyta vykdymo metu** – formatuoti vertes pagal dizaino metu nurodytą reikšmę vykdymo metu. Jei pasirinksite šią vertę, skirtuko Susiejimas lauke Data, laikas ir skaičiaus formatas  **sukonfigūruokite** išraišką **ER, kuri grąžina kultūros, pvz., atitinkamo kliento kultūros kodą,** kodą.

    ![Kultūros nustatymas yra nustatytas vykdymo metu pagal kultūros sukurtą ataskaitą ER operacijų kūrimo įrankyje.](./media/er-multilingual-labels-culture-context-runtime.png)

> [!NOTE]
> ER komponente, kurį apibrėžiate kaip konkretų į reikšmę įrašyti teksto reikšmę sukonfigūruotų antrinių ER komponentų, gali būti antrinių ER komponentų. Pagal numatytuosius nustatymus šių komponentų vertėms formatuoti naudojama pirminio komponento kultūra. Norėdami konfigūruoti šių komponentų susiejimus ir taikyti alternatyvų vertės formatavimo reikšmę, galite naudoti šias įtaisytąsias ER funkcijas:
>
> - [DATOS FORMATAS](er-functions-datetime-dateformat.md#syntax-2)
> - [DATOSLAIKOFORMATAS](er-functions-datetime-datetimeformat.md#syntax-2)
> - [FORMATO SKAIČIUS](er-functions-text-numberformat.md#syntax-2)
>
> 10.0.20 versijoje ir vėlesnėje, vietinio formato komponentai **Bendri\\Failas** ir **„Excel“\\Failo** tipai naudojami siekiant suformatuoti vertes per [PDF keitimą](electronic-reporting-destinations.md#OutputConversionToPDF) pagal sukurtą dokumentą.

## <a name="translation"></a>Perkėlimas

Galite pridėti reikiamas ER žymas prie redaguojamo ER komponento. Kai ER žyma pridedama, ji gali būti išversta dviem būdais: įprastiniu būdu ir automatiškai.

### <a name="manual-translation"></a>Įprastinis vertimas

Kai pridedate ER žymą **Teksto vertimas** [srityje](#TextTranslationPane), galite įprastiniu būdu išversti ją į visas dabartinės „Finance” programos versijos palaikomas kalbas. Galite pasirinkti pageidaujamą kalbą, esančią **Kalba** lauke **Sistemos kalba** arba **Vartotojo kalba** dalyje, įveskite atitinkamą tekstą į atitinkamą **Išverstas tekstas** lauką ir pasirinkite **Išversti**. Šis procesas turi būti kartojamas kiekvienai reikiamai kalbai ir kiekvienai jūsų pridėtai žymai.

### <a name="automatic-translation"></a>Automatinis vertimas

ER komponento konfigūracija baigiama ER konfigūracijos juodraštinėje versijoje, kurioje yra redaguojamas ER komponentas.

![ERA konfigūracijos puslapis, siūlantis prieigą prie konfigūracijos versijos juodraščio būsenoje.](./media/er-multilingual-labels-configurations.png)

Kaip aprašyta anksčiau šiame straipsnyje, reikalaujamas ER žymes galite pridėti prie redaguojamo ER komponento. Tokiu būdu galite nurodyti ER žymų tekstą EN-US kalba. Tada galite eksportuoti ER komponento žymas naudodami įtaisytąją ER funkciją. Pasirinkite ER konfigūracijos juodraštinę versiją, kurioje yra redaguojamas ER komponentas, ir pasirinkite **Sukeisti \>Eksporto žymos**.

![ER konfigūracijos puslapis, leidžiantis eksportuoti ER žymas iš pasirinktos konfigūracijos versijos.](./media/er-multilingual-labels-export.png)

Galite eksportuoti arba visas žymas arba vienos kalbos žymas, kurias nurodote eksporto pradžioje. Žymos eksportuojamos kaip suarchyvuotas failas, kuriame yra XML failų. Kiekviename XML faile yra vienos kalbos žymos.

![Eksportuoto failo, kuriame yra ER žymų, skirtų DE-AT kalbai, pavyzdys.](./media/er-multilingual-labels-in-xml.png)

Šį formatą naudoja išorinės vertimo paslaugos žymų automatiniam vertimui, pvz., [„Dynamics 365 Translation Service”](../lifecycle-services/translation-service-overview.md). Gavę išverstas žymas, jas galima importuoti atgal į ER konfigūracijos juodraštinę versiją, kurioje yra ER komponentų, kuriems priklauso šios žymos. Pasirinkite ER konfigūracijos juodraštinę versiją, kurioje yra redaguojamas ER komponentas, ir pasirinkite **Sukeisti \>Įkelti žymas**.

![ER konfigūracijos puslapis, leidžiantis importuoti ER žymas į pasirinktą konfigūracijos versiją.](./media/er-multilingual-labels-load.png)

Išverstos žymos bus importuojamos į pasirinktą ER konfigūraciją. ER konfigūracijoje esančios išverstos žymos yra pakeičiamos. Jei trūksta išverstos žymos ER konfigūracijoje, ji pridedama.

## <a name="lifecycle"></a>Gyvavimo ciklas

ER komponento žymos, kurios gali būti keičiamos, yra išsaugomos kartu su komponento turiniu atitinkamoje ER konfigūracijos versijoje.

Pagrindinio ER komponento žymas galima susieti su jūsų sukurta ER komponento išvestine versija, kad pritaikytumėte savo keitimus.

> [!TIP]
> Kurdami ER sprendimą, galite iš jo gauti savo ER [duomenų](er-overview-components.md#data-model-component) modelio komponentą. Šiame išvestiniuose duomenų modelyje galite pristatyti savo ER žymes ir naudoti jas visais ER formatais, kurie naudos duomenų modelį kaip duomenų šaltinį. Tada galite išvesti savo ER [formato komponentą](er-overview-components.md#format-component) iš to, kuris pateikiamas pasirinkus išvestinį ER duomenų modelį, o ne pateiktą. Versijoje 10.0.28 ir vėliau galite įgalinti išplėstinę prieigą prie didėjančios ER duomenų modelio funkcijos žymių, **kad būtų galima pasiekti didėjančios ER duomenų modelio žymes išvestiniuose ER formato komponentuose, net jei jūsų pasirinktas išvestinio ER** komponento ER duomenų modelis skiriasi nuo to, kuris buvo naudojamas pagrindinio ER komponento.
>
> Kai jūsų išvestuose komponentuose naudojamas tas pats žymės pavadinimas ir didėjimo tvarka esantys komponentai, tos žymės vertimas naudojamas kaip tinkamiausiiausias.

ER versijų valdymo žymos priskyrimas ER komponento atributui. Žymos priskyrimo pokyčiai įrašomi redaguojamo ER komponento, sukurto kaip pateikto ER komponento išvestinė versija, pokyčių (delta) sąraše. Šie pakeitimai bus patikrinti, kai išvestinė versija yra iš naujo pagrįsta nauja bazine versija.

## <a name="functions"></a>Funkcijos

Įdėtoji [LAUKŲSĄRAŠAS](er-functions-list-listoffields.md) ER funkcija gali pasinaudoti ER žymomis, sukonfigūruotomis pagal kai kurias ER komponentų prekes.

Kaip aprašyta anksčiau šiame straipsnyje, kiekvieno modelio ar formato ER išvardijimo vertės žymos ir aprašymo atributai gali būti susieti su ER žyme, **·** **·**[...](#LinkModelEnum)[kuri](#LinkFormatEnum) pasiekiama tam tikrą ER komponentą. Galite konfigūruoti ER išraišką, kurioje iškviečiate **LAUKŲSĄRAŠAS** funkciją, naudodami ER išvardijimą kaip argumentą. Ši išraiška grąžina sąrašą, kuriame yra ER išvardijimo, apibūdinto kaip šios funkcijos argumentas, kiekvienos vertės įrašas. Kiekviename įraše yra ER žymos vertė, susieta su ER išvardijimo verte:

- ER žymos vertė, susieta su **Žyma** atributais, saugoma grąžinto įrašo **Žyma** lauke.
- ER žymos vertė, susieta su **Aprašas** atributais, saugoma grąžinto įrašo **Aprašas** lauke.

## <a name="performance"></a><a name=performance></a>Našumas

Konfigūruodami ER formato komponentą, kad būtų galima generuoti ataskaitą pageidaujama [kalba](#language), arba importuoti gaunamąjį dokumentą, kai turinys išanalizuotas jūsų pageidaujama kalba, rekomenduojame įgalinti **talpyklą kaip pageidaujamą dabartinio vartotojo kalbą, kuri skirta ER, veikia** funkcijų [funkcijų valdymo](../../fin-ops/get-started/feature-management/feature-management-overview.md) darbo srityje. Ši funkcija padeda pagerinti našumą, ypač ER formato komponentams, kurie turi kelias nuorodas į žymes ER formulėse ir susiejimus bei daug tikrinimo taisyklių, kad sugeneruotų vartotojo pranešimus [pageidaujama](general-electronic-reporting-formula-designer.md#TestFormula) kalba.

Kai pakeičiate **ER** **konfigūracijos** versijos būseną iš Juodraštis į Baigta, jei konfigūracijos versijoje yra ER žymės, šios žymės saugomos programos duomenų bazėje. Saugojimo schema priklauso nuo ER žymių **saugojimo funkcijos pagreitinti būsenos**:

- Jei priemonė neįgalinta, visos **žymės saugomos lentelės ERSOLUTIONVERSIONTABLE** lauke LABELXML **kaip** vienas XML fragmentas.
- Jei priemonė įgalinta, lentelėje **ERSOLUTIONVERSIONLABELSTABLE** kiekvienai kalbai sukuriamas atskiras įrašas. Šios **lentelės** turinio lauke žymės pagal kalbą saugomos kaip suglaudintas XML fragmentas.

Funkcijų valdymo darbo srityje **patariame įgalinti ER žymų** saugojimo funkciją **pagreitinti**. Ši funkcija padeda pagerinti tinklo pralaidumo naudojimą ir visos sistemos našumą, nes dažniausiai, naudojant vieną ER konfigūraciją, naudojamos vienos kalbos ER žymės.

Norėdami taikyti pasirinktą saugojimo schemą visų ER konfigūracijų žymoms dabartiniame finansų egzemplioriuje saugoti, atlikite šiuos veiksmus.

1. Eikite į **Organizacijos administravimas** > **·** > **Periodinis taikykite pasirinktas žymes, saugant schemą visoms ER konfigūracijų.**
2. Pasirinkite **Gerai**.


## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)
- [Elektroninių ataskaitų funkcijos](er-formula-language.md#Functions)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
