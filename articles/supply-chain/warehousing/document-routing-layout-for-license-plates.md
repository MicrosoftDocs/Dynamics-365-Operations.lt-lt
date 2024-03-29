---
title: Dokumento maršruto žymos maketai
description: Šiame straipsnyje aprašoma, kaip naudoti formatavimo metodus vertėms ant etikečių spausdinti.
author: perlynne
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: a4e0c16b71c257cae832870ca58679884047ea16
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708651"
---
# <a name="document-routing-label-layout"></a>Dokumento maršruto žymos maketas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip sukurti numerio lentelės, konteinerio ir bangos etikečių maketus. Joje taip pat pateikiamos gairės, kaip kurti maketus naudojant Apimabra programavimo kalbą (ZPL).

Dokumentų maršruto žymos maketai nurodo, kokiu būdu išdėstyti žymės ir ant jų spausdinami duomenys. Spausdinimo aktyvinimo taškus galite konfigūruoti, kai nustatote mobiliojo įrenginio meniu elementus ir darbo šablonus.

Šiame straipsnyje pateikiama informacija taikoma visiems dokumentų maršruto žymos maketams, [įskaitant](tasks/license-plate-label-printing.md) numerio lentelės žymų, [konteinerių žymių ir bangos žymių](print-container-labels.md)[maketus](configure-wave-label-printing.md).

Galite spausdinti itin sudėtingas etiketes, jei spausdinimo įrenginys gali suprasti jam siunčiamą tekstą. Pavyzdžiui, ZPL maketas, kuriame yra brūkšninis kodas, gali būti panašus į šį pavyzdį.

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

Etikečių spausdinimo proceso metu tekstas, , šiame pavyzdyje – `$LicensePlateId$`, bus pakeistas į duomenų reikšmę. Keletas plačiai prieinamų etikečių generavimo įrankių gali padėti formatuoti etiketės maketo tekstą. Dauguma šių įrankių palaiko `$FieldName$` formatą. Be to, „Microsoft Dynamics 365 Supply Chain Management” naudoja specialią formatavimo logiką, kuri yra dokumento maršruto planavimo maketo laukų susiejimo dalis.

Norėdami pamatyti reikšmes, kurios bus išspausdintos, eikite į **Sandėlio valdymas \> Užklausos ir ataskaitos \> Numerio lentelės etiketės**.

## <a name="turn-on-this-feature-for-your-system"></a>Šios funkcijos įjungimas sistemoje

Jei jūsų sistemoje dar nėra šiame straipsnyje aprašytų funkcijų, [eikite](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) į funkcijų valdymą ir įjunkite funkciją Išplėstiniai *numerio lentelės žymų maketai*. (Kaip ir tiekimo grandinės valdymo versija 10.0.21, ši funkcija įjungiama pagal numatytąjį nustatymą. Kadangi tiekimo grandinės valdymas yra 10.0.25, ši funkcija yra privaloma ir jos išjungti negalima.)

## <a name="custom-number-formats"></a>Pasirinktiniai numerių formatai

Galite tinkinti skaitinių lauko reikšmių, kurios spausdinamos naudojant kodus, turinčius toliau pateikiamą formatą, formatavimą.

```dos
$FieldName:FormatString$
```

Toliau pateikiamas šio formato paaiškinimas.

- `FieldName` yra duomenų lauko pavadinimas (pvz., **Kiekis**).
- `FormatString` nurodo, kaip turi būti spausdinami duomenys.

Toliau pateikti pavyzdžiai rodo, kaip galima tinkinti darbo kiekio (**Kiekis**) lauką.

- Naudokite `$Qty:0000$`, norėdami visada matyti keturis skaitmenis (nuliai naudojami kaip vietos rezervavimo ženklai). Pavyzdžiui, jei kiekis yra 10, etiketėje bus rodoma „0010.”
- Naudokite `$Qty:0.00$`, norėdami visada matyti du skaičius po kablelio. Pavyzdžiui, jei kiekis yra 10, etiketėje bus rodoma „10,00”.

Norėdami peržiūrėti visą galimų numerių formato eilučių sąrašą, žr. [Pasirinktinės skaitinės formato eilutės](/dotnet/standard/base-types/custom-numeric-format-strings).

## <a name="custom-string-formats"></a>Pasirinktiniai eilučių formatai

Galite pašalinti pirmuosius eilutės simbolius naudodami toliau pateiktą lauką ir formato kodą.

```dos
$FieldName:#..$
```

`#` nurodo praleidžiamų simbolių skaičių. Pavyzdžiui, norėdami išspausdinti gabenimo konteinerio serijos kodo (SSCC) numerio lentelės numerį, kuris neapima pirmų dviejų simbolių, naudokite `$LicensePlateId:2..$`. Šiuo atveju numerio lentelės numeris „0011111111111222221” bus išspausdintas kaip „11111111111222221.”

## <a name="custom-datetime-formats"></a>Pasirinktiniai datos / laiko formatai

Toliau pateiktame pavyzdyje parodyta, kaip galima kontroliuoti formatą, kuris naudojamas datoms spausdinti.

```dos
$PrintedDate:dd-MM-yyyy$
```

Šiame pavyzdyje data 2020 m. balandžio 30 d. bus spausdinama kaip „30-04-2020.”

Norėdami peržiūrėti visą galimų datos / laiko formatų sąrašą, žr. [Pasirinktinės datos ir laiko formato eilutės](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="print-individual-lines-from-multiline-data"></a>Kelių eilučių duomenų atskirų eilučių spausdinimas

Jei duomenų lauke yra kelios eilutės (t. y. eilutės, kurios yra atskirtos eilučių lūžiais), galite spausdinti atskirą eilutę naudodami toliau pateiktą formatą.

```dos
$FieldName[#]$
```

`#` yra eilutės numeris, kurį norite spausdinti. (Pirmai eilutei naudokite 1.)

Pavyzdžiui, jūsų sistemoje yra `AdditionalAddress` laukas, kuriame saugomas toliau pateiktas kelių eilučių adresas.

„Contoso Inc.”  
Gatvės pavadinimas 123  
Miestas, Valstija

Galite spausdinti šį adresą po vieną eilutę, naudodami toliau pateiktus kodus.

| Kodas | Išspausdintas tekstas |
|---|---|
| `$AdditionalAddress[1]$` | „Contoso Inc.” |
| `$AdditionalAddress[2]$` | Gatvės pavadinimas 123 |
| `$AdditionalAddress[3]$` | Miestas, Valstija |

## <a name="print-and-format-from-a-display-method"></a>Spausdinimas ir formatavimas naudojant rodymo būdą

Galite spausdinti iš rodymo būdo naudodami toliau pateiktą formatą.

```dos
$DisplayMethod()$
```

Šį formatą galima derinti su kitais tipais, kurie anksčiau aprašyti šiame straipsnyje. Pavyzdžiui, turite rodymo būdą, kurio pavadinimas `DisplayListOfItemsNumbers()`, ir norite spausdinti pirmą šio būdo prekės numerį. Tokiu atveju galite naudoti toliau pateiktą kodą.

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a>Daugiau informacijos apie tai, kaip spausdinti etiketes

Daugiau informacijos apie tai, kaip nustatyti ir išspausdinti etiketes, ieškokite toliau pateikiamame straipsnyje:

- [Numerio lentelės žymės spausdinimas](tasks/license-plate-label-printing.md)
- [Spausdinti konteinerių etiketes](print-container-labels.md)
- [Bangos žymos spausdinimas](configure-wave-label-printing.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
