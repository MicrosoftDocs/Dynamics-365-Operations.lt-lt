---
title: Palaikomi primityvių duomenų ataskaitų formulių sudėtiniai duomenų tipai
description: Šioje temoje pateikiama informacijos apie primityvių duoemnų tipo funkcijas, palaikomas modulyje Elektroninės ataskaitos (ER) formulėse.
author: NickSelin
ms.date: 06/02/2021
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 96fdf33f4cc5f22015c00c57858bd438e6465764
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323645"
---
# <a name="supported-primitive-data-types-for-electronic-reporting-formulas"></a>Palaikomi primityvių duomenų ataskaitų formulių sudėtiniai duomenų tipai

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacijos apie primityvių duoemnų tipo funkcijas, palaikomas modulyje [Elektroninės ataskaitos (ER) formulėse](general-electronic-reporting.md). Čia pateikiamas naujų primityvių duomenų tipai:

- [Bulio logikos](#boolean)
- [data](#date)
- [data ir laikas](#datetime)
- [numeravimas](#enumeration)
- [vadovas](#guid)
- [sveikasis skaičius](#integer)
- [Int64](#int64)
- [tikrasis](#real)
- [Eilutė](#string)

## <a name="boolean"></a><a name="boolean"></a>Bulio logika

*Boolean* logikos primityvių duomenų tipe yra vertė, kuri įvertinta kaip *teisinga* arba *klaidinga*. Galite naudoti rezervuotus literalo raktinius žodžius **Teisinga** ir **Klaidinga,** kai tik tikimasi *Bulio logikos* išraiškos. Numatytoji reikšmė yra *klaidinga*.

Vidinis Bulio *logikos vaizdas* yra *sveikasis skaičius*. Vertė 0 (nulis) įvertinta kaip klaidinga, o *visos* kitos *įvertintos* yra *kaip* teisingos *skaičius*. Kai Jūs [patvirtinate](general-electronic-reporting-formula-designer.md#TestFormula) sukonfigūruotą išraišką, kuri grąžina *boolean* logiką [ER formulės kūrimo įrankyje](er-advanced-formula-editor.md), testo rezultatu juosta rodo *0* (nulį) ir išraiška grąžina *neteisinga*. Kitu atveju tikrinimo rezultatų srityje bus *1*.

*Bulio* logikoje nėra netiesiogiai konvertavimų. Tačiau galite naudoti [TEXT](er-functions-text-text.md) funkciją, kad Bulio logikos *aiškiai* konvertuojama į *eilutę*:

- Klaidinga *vertė* konvertuojama į teksto eilutę **Klaidinga**.
- Klaidinga *teisinga* konvertuojama į teksto eilutę **Teisinga**.

> [!NOTE]
> Šis konvertavimas nepriklauso nuo pateiktos kalbos ir kultūros [konteksto](er-design-multilingual-reports.md).

Palyginimo [operatoriai](er-formula-language.md#Operators) yra vienintelis operatoriaus tipas, kurį galima naudoti su *Bulio* logikos duomenų tipu. Šie operatoriai gali būti naudojami norint palyginti dvi *Bulio* logikos vertes: \<\> ir =.

## <a name="date"></a><a name="date"></a>Data

*Datos* primityvių duomenų tipe yra diena, mėnuo ir metai. Datos gali būti inicijuojamos naudojant šias funkcijas:

- [DATEVALUE](er-functions-datetime-datevalue.md)
- [NULLDATE](er-functions-datetime-nulldate.md)
- [SESSIONTODAY](er-functions-datetime-sessiontoday.md)
- [TODAY](er-functions-datetime-today.md)

Duomenų *tipe* gali būti nurodytos datos nuo 1900 m. sausio 1 d. iki 2154 m. gruodžio 31 d. Numatytoji vertė yra **neapibrėžta**, o vidinio pristatymo data yra 1900 m. sausio 1 d.

*Datos* logikoje nėra netiesiogiai konvertavimų. Tačiau galite naudoti šias tikslias konvertavimo funkcijas:

- [DATOS FORMATAS](er-functions-datetime-dateformat.md)
- [DATETODATETIME](er-functions-datetime-datetodatetime.md)
- [TEXT](er-functions-text-text.md)

Funkcija [ADDDAYS](er-functions-datetime-adddays.md) jums leidžia įtraukti ir išreikšti dienas iš duomenų. Tokiu būdu galite perkelti tam tikrą dienų skaičių į ateitį ir praeitį. Funkcija [DAYS](er-functions-datetime-days.md) leidžia atimti datas viena nuo kitos ir apskaičiuoti dienų skirtumą. Daugiau informacijos apie datos verčių *pasikeitimą* ieškokite [datos ir laiko kategorijos ER funkcijų sąraše](er-functions-category-datetime.md).

Palyginimo [operatoriai](er-formula-language.md#Operators) yra vienintelis operatoriaus tipas, kurį galima naudoti su *datos* logikos duomenų tipu. Šie operatoriai gali būti naudojami norint palyginti dvi *datos* vertes: \<\>, \<, \<=, =, \>, ir \>=.

## <a name="datetime"></a><a name="datetime"></a>Datetime

Primityvių duomenų *datos ir laiko* nesumityvių duomenų tipas sujungia *datos* tipą ir vertę, kuri rodo laiką, kuris praėjo nuo vidurnakčio. Laikas išreiškiamas valandomis, minutėmis, sekundėmis ir sekundėmis. Be to, *datos ir laiko* vertėje yra informacijos apie laiko juostą.

Datos ir laiko duomenų tipas gali turėti datas *nuo* sausio 1 d., 1900 (1900-01-01T00:00:00.0000000+00:00 kelionės formatu iki [gruodžio](/dotnet/standard/base-types/standard-date-and-time-format-strings)) 31 d., 2154 (2154/12/31T11:59:59.9999999+00:00 apvalinimo formatu). Mažiausias datetime laiko vienetas *yra* viena dešimt milijono antro.

> [!NOTE]
> Kai **hh** [specifier naudojamas valandoms, laiko reikšmių](/dotnet/standard/base-types/standard-date-and-time-format-strings) 12:59:59:9999999 negalima interpretuoti kaip galiojimo laiko.
>
> Kai **HH** naudojamas valandoms, laiko reikšmių 23:59:59:9999999 negalima interpretuoti kaip galiojimo laiko.

Numatytoji vertė yra **neapibrėžta** o vidinio pristatymo data yra sausio 1 d., 1900 (1900-01-01T00:00:00.0000000+00:00 kelionės atgal formatu).

Datos ir laikai gali būti inicijuojamos naudojant šias funkcijas:

- [DATETIMEVALUE](er-functions-datetime-datetimevalue.md)
- [NULNULLDATETIMELDATE](er-functions-datetime-nulldatetime.md)
- [SESSIONNOW](er-functions-datetime-sessionnow.md)
- [NOW](er-functions-datetime-now.md)

*Datos ir laiko* logikoje nėra netiesiogiai konvertavimų. Tačiau galite naudoti šias tikslias konvertavimo funkcijas:

- [DATOSLAIKOFORMATAS](er-functions-datetime-datetimeformat.md)
- [TEXT](er-functions-text-text.md)

Daugiau informacijos apie datos verčių *pasikeitimą* ieškokite [datos ir laiko verčių ER funkcijų sąraše](er-functions-category-datetime.md).

Palyginimo [operatoriai](er-formula-language.md#Operators) yra vienintelis operatoriaus tipas, kurį galima naudoti su *datos ir laiko* logikos duomenų tipu. Šie operatoriai gali būti naudojami norint palyginti dvi *datos ir laiko* vertes: \<\>, \<, \<=, =, \>, ir \>=.

## <a name="enumeration"></a><a name="enumeration"></a>Išvardijimas

*Išvardijimo* nesudėtingų duomenų tipas yra literalų sąrašas. Galite naudoti išvardijimo, apibrėžto programos šaltinio [kode, išvardijimas](../dev-ref/xpp-data-primitive.md#enum). Taip pat galite pristatyti savo išvardijimas ER duomenų modelio ir ER formato komponentams.

Programos *išvardijimas* gali būti naudojamas kaip bet kurio ER modelio susiejimo ir ER formato išraiškos.

Toliau pateikta iliustracija rodo, kaip įtraukti **CustVendCorrectiveReasonCode** modelio išvardijimo į redaguojamą ER duomenų modelį.

[![Konfigūruotas modelio numeravimas ER duomenų modelio kūrimo įrankyje.](./media/er-formula-supported-data-types-primitive-enum1.gif)](./media/er-formula-supported-data-types-primitive-enum1.gif)

Modelio *išvardijimas* gali būti naudojamas bet kurio ER modelio susiejimo ir ER formato išraiškoms, sukurtoms pagal duomenų modelį, kuriame buvo *įvestas* išvardijimas.

Šioje iliustracijoje parodyta, kaip į redaguojamą ER formatą galima įtraukti Atšauktų išlaidų subkategorijų sąrašo **formatą** Išvardijimas.

[![Konfigūruotas formato numeravimas ER foramto kūrimo įrankyje.](./media/er-formula-supported-data-types-primitive-enum2.gif)](./media/er-formula-supported-data-types-primitive-enum2.gif)

Formato *išvardijimas* ali būti naudojamas tik ER formato, kuriame buvo įvestas *išvardijimas* išraiškomis.

Turite naudoti atitinkamą ER duomenų šaltinių tipą, kad būtų rodomas konkretus išvardijimas sukonfigūruotam ER komponentui kaip konstanta arba kaip vertė, kurią vartotojas, vykdantis ER sprendimą, nurodytą dialogo lange apdorojimo metu.

- Programos išvardijimas gali būti pasiekti naudojant **Dynamics 365 for Operations \ Išvardijimas** ir **Bendrieji \ Vartotojo įvesties** parametrų duomenų šaltiniai. Šioje iliustracijoje parodyta, kaip galima pridėti prie redaguojamo ER formato **appenumNoYes** ir **uipNoYes** duomenų šaltinius, kurie nurodo **NoYes** programos išvardijimą.

    [![Programos išvardijimo duomenų šaltinių įtraukimas į ER formato konstruktorių.](./media/er-formula-supported-data-types-primitive-enum3a.gif)](./media/er-formula-supported-data-types-primitive-enum3a.gif)

- Duomenų modelių išvardijimas gali būti pasiekti naudojant **duomenų modelį \ Išvardijimas** ir **duomenų modelis \ Išvardijimo vartotojo įvesties parametrų** duomenų šaltiniai. Šioje iliustracijoje parodyta, kaip galima pridėti prie redaguojamo ER formato **CustVendCorrectiveReasonCode** duomenų šaltinis, kuris rodo į **CustVendCorrectiveReasonCode** duomenų modelio išvardijimą.

    [![Programos išvardijimo duomenų išvardijimo įtraukimas į ER formato konstruktorių.](./media/er-formula-supported-data-types-primitive-enum3b.gif)](./media/er-formula-supported-data-types-primitive-enum3b.gif)

- Formato modelių išvardijimas gali būti pasiekti naudojant **duomenų modelį \ Formato** ir **Formato modelis \ Išvardijimo vartotojo įvesties parametrų** duomenų šaltiniai. Šioje iliustracijoje parodyta, kaip galima pridėti prie redaguojamo ER formato **NaturaReverseCharge** duomenų šaltinis, kuris rodo į **Natura atvirkštinio apmokestinimo papildomos kategorijos** duomenų formato išvardijimą.

    [![Formato išvardijimo duomenų išvardijimo įtraukimas į ER formato konstruktorių.](./media/er-formula-supported-data-types-primitive-enum3c.gif)](./media/er-formula-supported-data-types-primitive-enum3c.gif)

*Išvardijimo* logikoje nėra netiesiogiai konvertavimų. Tačiau galite naudoti [TEXT](er-functions-text-text.md) konvertavimo funkciją norėdami *išvardijimo* konvertavimą į teksto eilutę. Šis konvertavimas nepriklauso nuo kalbos. Norėdami sužinoti, kaip galite susieti *išvardijimo* vertę su tam tikros kalbos žymomis, žr [LISTOFFIELDS](er-functions-list-listoffields.md) ir [GETENUMVALUEBYNAME](er-functions-text-getenumvaluebyname.md) pavyzdžius.

Palyginimo [operatoriai](er-formula-language.md#Operators) yra vienintelis operatoriaus tipas, kurį galima naudoti su *išvardijimo* logikos duomenų tipu. Šie operatoriai gali būti naudojami norint palyginti dvi *išvardijimo* logikos vertes: \<\> ir =.

## <a name="guid"></a><a name="guid"></a>Vadovas

*vadovas* nesumifikuotų duomenų tipas turi visuotinai unikalią identifikatoriaus (GUID) reikšmę. GUID yra vertė, kurią galima naudoti tarp visų kompiuterių ir tinklų, kai reikalingas unikalus identifikatorius. Neįmanoma, kad numeris dubliuotųsi. Tinkamas GUID atitinka visas šias specifikacijas:

- Turi būti 32 šešioliktainiai skaičiai.
- Be to, turi būti keturi brūkšnių simboliai, įdėti į šias vietas: 8-4-4-4-12.
- Be to, eilutės pradžioje \{\} ir pabaigoje galima įtraukti papildomus riestinius skliaustus. Pvz., abu **\{2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212\}** ir **2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212** yra tinkamos GUID eilutės.
- Todėl bendra suma turi būti 36 ar 38 simbolių; tai priklauso nuo to, ar pridėti riestiniai skliaustai.
- Raidės, kurios naudojamos kaip šešioliktainiai skaitmenys, gali būti didžioji (A–F), didžioji raidė (a–f) arba mišrus.

Tačiau galite naudoti šias tikslias konvertavimo funkcijas:

- [GUIDVALUE](er-functions-text-guidvalue.md)
- [TEXT](er-functions-text-text.md)

Palyginimo [operatoriai](er-formula-language.md#Operators) yra vienintelis operatoriaus tipas, kurį galima naudoti su *guid* logikos duomenų tipu. Šie operatoriai gali būti naudojami norint palyginti dvi *guid* logikos vertes: \<\> ir =.

## <a name="integer"></a><a name="integer"></a>Sveikasis skaičius

Sveikojo *skaičiaus* primityvių duomenų tipas nurodo skaičių, neturintį skaitmenų po kablelio. Skaičių skaičiai naudojami kaip kontrolės kintamieji pasikartojančiuose išrašuose arba kaip indeksai įrašų sąrašuose.

Literatas *sveikasis skaičius* yra visas skaičius, kaip jis tiesiogiai įvestas ER išraiškoje (formulė) [pvz.](general-electronic-reporting-formula-designer.md#formula-designer-overview) tokia kaip **12345**. *Integeris* yra 32 bitų pločio. Numatytoji vertė yra **0**, o vidinis vaizdas – ilgas skaičius. Konvertuoti *svertą* į *realų* skaičių automatiškai.

Taip pat, galite naudoti šias tikslias konvertavimo funkcijas:

- [INTVALUE](er-functions-conversion-intvalue.md)
- [FORMATO SKAIČIUS](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

Ats. *skaičius* yra \[ -2,147,483,647: 2,147,483,647\]. Visi šio diapazono skaitmenys gali būti naudojami kaip literalai.

Visi palyginimo ir matematiniai [operatoriai](er-formula-language.md#Operators) gali būti naudojami su skaičiaus duomenų *tipu*.

## <a name="int64"></a><a name="int64"></a>Int64

Sveikojo *int64* primityvių duomenų tipas nurodo skaičių, neturintį skaitmenų po kablelio. *Int64* verėts yra naudojamos kaip kontrolės kintamieji pasikartojančiuose išrašuose arba kaip indeksai įrašų sąrašuose.

*int64* yra 64 bitų pločio. Numatytoji vertė yra **0**, o vidinis vaizdas – ilgas skaičius. Konvertuoti *int64* į *realų* skaičių automatiškai.

Taip pat, galite naudoti šias tikslias konvertavimo funkcijas:

- [INT64VALUE](er-functions-conversion-int64value.md)
- [FORMATO SKAIČIUS](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

Ats. *int64* yra \[ -9,223,372,036,854,775,807: 9,223,372,036,854,775,807\].

Visi palyginimo ir matematiniai [operatoriai](er-formula-language.md#Operators) gali būti naudojami su skaičiaus duomenų *int64*.

## <a name="real"></a><a name="real"></a>Tikrasis

Primityviųjų *realiųjų* duomenų tipe, be sveikojo skaičiaus, gali būti nurodyti ir dešimtainės trupmenos skaitmenys. Galite naudoti dešimtainius literalus bet kurioje vietoje, *kur* tikisi realusis skaičius. Dešimtainis literalas yra dešimtainis, kaip jis įvedamas tiesiogiai kode, pvz. **2.19**.

> [!NOTE]
> ER išraiškose laikotarpis (.) visada naudojamas kaip dešimtainis skyriklis.

Reals galima naudoti visose išraiškose ir juos galima naudoti su palyginimu ir aritmetiniais operatoriais. *realusis* turi 16 skaitmeninių ženklų tikslumą. Numatytoji vertė *realių* skaičių yra **0,0**, o vidinis vaizdas yra dvejetainis skaitmeninis (BCD) numeris. BCD kodavimas leidžia tiksliai pateikti vertes, kurios yra 0.1 kartotiniai. Kintamųjų intervalas *realiųjų* yra -(10)<sup>127</sup> per (10)<sup>127</sup>. Visos šio diapazono realinės išraiškos gali būti naudojamos kaip literalai ER išraiškose.

*Realiųjų* logikoje nėra netiesiogiai konvertavimų. Tačiau galite naudoti šias funkcijas, norėdami tiesiogiai konvertuoti realų į kitus *duomenų* tipus ir kitus duomenų tipus į *realų*:

- [INTVALUE](er-functions-conversion-intvalue.md)
- [INT64VALUE](er-functions-conversion-int64value.md)
- [FORMATO SKAIČIUS](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)
- [VALUE](er-functions-conversion-value.md)

Visi palyginimo ir matematiniai [operatoriai](er-formula-language.md#Operators) gali būti naudojami su skaičiaus duomenų *realiųjų*.

## <a name="string"></a><a name="string"></a>Eilutė

Primityviųjų *eilutės* duomenų tipai nurodo simbolių seką, kuri naudojama kaip tekstai, sąskaitų numeriai, adresai ir telefonų numeriai.

*Eilutės* literalai yra simboliai, rašiniai kabutėse (""). *Eilutės* literalai gali būti naudojami ten, kur *ER* išraiškose turi būti tikėtasi eilučių verčių. Galite naudoti eilutes loginėse išraiškose, pvz., palyginimuose. Taip pat galite suaktyvint *eilutės* vertes naudodami **\&** operatorių ar [CONCATENATE](er-functions-text-concatenate.md) funkciją.

> [!NOTE]
> Jei suliejate *dviejų* eilučių vertes, ir norite, kad gauta eilutė truktų daugiau nei vieną eilutę, *naudokite* eilučių lūžio skyriklį tarp verčių. TEXT išeigai šis skyriklis gali būti simbolis, generuojamas naudojant išraišką [CHAR](er-functions-text-char.md)(10) ar CHAR(13) išraišką. HTML gali būt **\<br\>** žymė.

Numatytoji vertė *eilutės* yra tuščia teksto eilutė, neturi turinti simbolių, o vidinis vaizdas yra simbolių sąrašas.

Nėra automatinių eilučių konvertavimų. Tačiau galite naudoti šias tikslias konvertavimo funkcijas:

- [CHAR](er-functions-text-char.md)
- [FORMAT](er-functions-text-format.md)
- [LEFT](er-functions-text-left.md)
- [LEN](er-functions-text-len.md)
- [MID](er-functions-text-mid.md)
- [PADLEFT](er-functions-text-padleft.md)
- [REPLACE](er-functions-text-replace.md)
- [RIGHT](er-functions-text-right.md)
- [TEXT](er-functions-text-text.md)
- [TRANSLATE](er-functions-text-translate.md)
- [TRIM](er-functions-text-trim.md)
- [UPPER](er-functions-text-upper.md)

Daugiau informacijos apie datos verčių *eilučių* ieškokite [teksto kategorijos ER funkcijų sąraše](er-functions-category-text.md).

Gali *eilutė* turėti neribotą simbolių skaičių.

Visi palyginimo ir matematiniai [operatoriai](er-formula-language.md#Operators) gali būti naudojami su skaičiaus duomenų *eilutė*.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)
- [Elektroninių ataskaitų formulių kalba](er-formula-language.md)
- [Palaikomi sudedamųjų duomenų tipai](er-formula-supported-data-types-composite.md)
