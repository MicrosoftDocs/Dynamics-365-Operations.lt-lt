---
title: NUMSEQVALUE ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama NUMSEQVALUE elektroninių ataskaitų (ER) funkcija.
author: kfend
ms.date: 12/17/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 62255f0a47d3c67468cf2cf3922a1886c29c03d6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271560"
---
# <a name="numseqvalue-er-function"></a>NUMSEQVALUE ER funkcija

[!include [banner](../includes/banner.md)]

`NUMSEQVALUE` funkcija grąžina *Eilutės* reikšmę, reiškiančią naują sugeneruotą numeracijos reikšmę pagal nurodytą numeraciją, aprėptį ir aprėpties ID. Aprėpties ID yra lygus įmonės kodui pagal kontekstą, kuriame paleistas elektroninių ataskaitų (ER) formatas.

## <a name="syntax-1"></a>Sintaksė 1

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a>Sintaksė 2

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a>Sintaksė 3

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a>Argumentai

`number sequence code`: *Eilutė*

Tekstinė reikšmė, reiškianti numeracijos kodą, kurio reikia naujajai reikšmei.

`number sequence record ID`: *Int64*

*Int64* reikšmė, nurodanti įrašo ID, kurio NumberSequenceTable lentelėje yra numeracijos apibrėžtis, kurios reikia naujajai reikšmei.

`scope type`: *Išvard. reikšmė*

Išvardijimo **ERExpressionNumberSequenceScopeType** išvardijimo reikšmė, nurodanti numeracijos, kuriai reikia naujos reikšmės, aprėptį. Galimi aprėpties tipai yra **Bendrasis**, **Juridinis subjektas** ir **Įmonė**.

`scope ID`: *Eilutė*

*Eilutės* reikšmė, identifikuojanti aprėptį pagal nurodytą aprėpties tipą.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Aprėpties tipui **Bendrasis** nurodykite tuščią eilutę kaip aprėpties ID.

Aprėpties tipams **Įmonė** ir **Juridinis subjektas** nurodykite įmonės kodą kaip aprėpties ID. Jei šiems aprėpties tipams nurodote tuščią eilutę kaip aprėpties ID, naudojamas dabartinės įmonės kodas.

Naudojant sintaksę 1, reikalaujama numeracija aprėpties tipui **Įmonė**, o įmonės kodas pateikiamas pagal kontekstą, kuriuo vykdomas ER formatas.

## <a name="example-1"></a>1 pavyzdys

JSavo ER formatu galite nustatyti duomenų šaltinį **AskNumSeq**, kurio tipas – *Vartotojo įvesties parametras*. Šis duomenų šaltinis nurodo išplėstąjį duomenų tipą **Aprašas**. Toliau, apibrėžiate tipo *Apskaičiuotasis laukas* duomenų šaltinį **NumSeq**. Šiame duomenų šaltinyje yra išraiška `NUMSEQVALUE (AskNumSeq)`. Kai duomenų šaltinis **NumSeq** yra iškviečiamas, jis grąžina naują sugeneruotą numeraciją, kuri buvo nurodyta vykdymo metu įvedant jo kodą į dialogo langą. Prašoma numeracija aprėpties tipui **Įmonė**. Įmonės kodas pateikiamas atsižvelgiant į kontekstą, pagal kurį ER formatas yra vykdomas.

## <a name="example-2"></a>2 pavyzdys

Šie duomenų šaltiniai apibrėžti jūsų modelių susiejime:

- Duomenų šaltinis **LedgerParms**, priklausantis tipui *Lentelės įrašai*. Šis duomenų šaltinis nurodo lentelę „LedgerParameters“.
- Tipo *Apskaičiuotasis laukas* duomenų šaltinis **NumSeq**. Šiame duomenų šaltinyje yra išraiška `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.

Kai iškviečiamas duomenų šaltinis **NumSeq**, pateikiama nauja sukurta numeracijos, pagal DK parametrus sukonfigūruotos taip, kad būtų pritaikyta kontekstą, pagal kurį vykdomas ER formatas, teikiančiai įmonei, vertė. Ši numeracija unikaliai identifikuoja žurnalus ir naudojama kaip operacijas siejantis paketo numeris.

## <a name="example-3"></a>3 pavyzdys

Šie duomenų šaltiniai apibrėžti jūsų modelių susiejime:

- **365 finansų išvardijimo** tipo Microsoft Dynamics *enum Yra* duomenų šaltinis. Šis duomenų šaltinis nurodo **ERExpressionNumberSequenceScopeType** išvardijimą.
- Tipo *Apskaičiuotasis laukas* duomenų šaltinis **NumSeq**. Šiame duomenų šaltinyje yra išraiška `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.

Kai iškviečiamas duomenų šaltinis **NumSeq**, pateikiama nauja sukurta numeracijos **Gene\_1**, sukonfigūruotos taip, kad būtų pritaikyta kontekstą, pagal kurį vykdomas ER formatas, teikiančiai įmonei, vertė.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kitos (konkrečios verslo srities) funkcijos](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
