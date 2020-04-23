---
title: Numerio lentelės etikečių dokumentų maršrutų planavimo maketas
description: Šioje temoje aprašoma, kaip naudoti formatavimo metodus spausdinti reikšmėms etiketėse.
author: perlynne
manager: tfehr
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 62d4301f9dbe301c2a2573102d911a8d0ec58eb0
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261355"
---
# <a name="document-routing-layout-for-license-plate-labels"></a>Numerio lentelės etikečių dokumentų maršrutų planavimo maketas

[!include [banner](../includes/banner.md)]

Dokumento maršruto planavimo maketas apibrėžia numerio lentelės etikečių maketą ir ant etikečių išspausdintus duomenis. Spausdinimo aktyvinimo taškus galite konfigūruoti, kai nustatote mobiliojo įrenginio meniu elementus ir darbo šablonus.

Paprastai sandėlio gavimo klerkai spausdina numerio lentelės etiketes iš karto po to, kai įrašo padėklų, kurie pristatomi į gavimo sritį, turinį. Fizinės etiketės pritaikomos padėklams. Jos gali būti naudojamos tolesnei atidėjimo proceso tikrinimo daliai ir būsimoms siuntimo paėmimo operacijoms.

Galite spausdinti itin sudėtingas etiketes, jei spausdinimo įrenginys gali suprasti jam siunčiamą tekstą. Pavyzdžiui, „Zebra” programavimo kalbos (ZPL) maketas, kuriame yra brūkšninis kodas, gali būti panašus į toliau pateiktą pavyzdį.

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

Etikečių spausdinimo proceso metu tekstas, , šiame pavyzdyje – `$LicensePlateId$`, bus pakeistas į duomenų reikšmę.

Norėdami pamatyti reikšmes, kurios bus išspausdintos, eikite į **Sandėlio valdymas \> Užklausos ir ataskaitos \> Numerio lentelės etiketės**.

Keletas plačiai prieinamų etikečių generavimo įrankių gali padėti formatuoti etiketės maketo tekstą. Dauguma šių įrankių palaiko `$FieldName$` formatą. Be to, „Microsoft Dynamics 365 Supply Chain Management” naudoja specialią formatavimo logiką, kuri yra dokumento maršruto planavimo maketo laukų susiejimo dalis.

## <a name="custom-number-formats"></a>Pasirinktiniai numerių formatai

Galite tinkinti skaitinių lauko reikšmių, kurios spausdinamos naudojant kodus, turinčius toliau pateikiamą formatą, formatavimą.

```dos
$FieldName:FormatString$
```

Toliau pateikiamas šio formato paaiškinimas.

- `FieldName` yra duomenų lauko pavadinimas (pvz., **Kiekis**).
- `FormatString` nurodo, kaip turi būti spausdinami duomenys.

Toliau pateikti pavyzdžiai rodo, kaip galima tinkinti darbo kiekio (**Kiekis**) lauką.

- Naudokite `$Qty:0000$`, norėdami visada matyti keturis skaitmenis (nuliai naudojami kaip vietos rezervavimo ženklai). Pavyzdžiui, jei kiekis yra 10, etiketėje bus rodoma „0010”.
- Naudokite `$Qty:0.00$`, norėdami visada matyti du skaičius po kablelio. Pavyzdžiui, jei kiekis yra 10, etiketėje bus rodoma „10.00”.

Norėdami peržiūrėti visą galimų numerių formato eilučių sąrašą, žr. [Pasirinktinės skaitinės formato eilutės](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).

## <a name="custom-string-formats"></a>Pasirinktiniai eilučių formatai

Galite pašalinti pirmuosius eilutės simbolius naudodami toliau pateiktą lauką ir formato kodą.

```dos
$FieldName:#..$
```

`#` nurodo praleidžiamų simbolių skaičių. Pavyzdžiui, norėdami išspausdinti gabenimo konteinerio serijos kodo (SSCC) numerio lentelės numerį, kuris neapima pirmų dviejų simbolių, naudokite `$LicensePlateId:2..$`. Šiuo atveju numerio lentelės numeris „0011111111111222221” bus išspausdintas kaip „11111111111222221”.

## <a name="custom-datetime-formats"></a>Pasirinktiniai datos / laiko formatai

Toliau pateiktame pavyzdyje parodyta, kaip galima kontroliuoti formatą, kuris naudojamas datoms spausdinti.

```dos
$PrintedDate:dd-MM-yyyy$
```

Šiame pavyzdyje data 2020 m. balandžio 30 d. bus spausdinama kaip „30-04-2020”.

Norėdami peržiūrėti visą galimų datos / laiko formatų sąrašą, žr. [Pasirinktinės datos ir laiko formato eilutės](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).

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

Šį formatą galite derinti su kitais šioje temoje aprašytais tipais. Pavyzdžiui, turite rodymo būdą, kurio pavadinimas `DisplayListOfItemsNumbers()`, ir norite spausdinti pirmą šio būdo prekės numerį. Tokiu atveju galite naudoti toliau pateiktą kodą.

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a>Daugiau informacijos apie tai, kaip spausdinti etiketes

Daugiau informacijos apie tai, kaip nustatyti ir spausdinti etiketes, žr. [Numerio lentelės etiketės spausdinimo įgalinimas](tasks/license-plate-label-printing.md).
