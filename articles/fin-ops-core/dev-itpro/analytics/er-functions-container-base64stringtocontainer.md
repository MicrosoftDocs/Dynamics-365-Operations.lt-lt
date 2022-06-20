---
title: „Base64StringToContainer” ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama Base64StringToContainer elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 12/14/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: bcbbead1155a7270a329c23055340492c73cdfda
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879926"
---
# <a name="base64stringtocontainer-er-function"></a>„Base64StringToContainer” ER funkcija

[!include [banner](../includes/banner.md)]

„`BASE64STRINGTOCONTAINER`” [funkcija](er-formula-language.md#Functions) konvertuoja nurodytą *Eilutės* tipo įvestį į *[Konteinerio](er-functions-category-container.md)* tipo duomenų elementą.

## <a name="syntax"></a>Sintaksė

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a>Argumentai

`input`: *Eilutė*

Tinkamas *Eilutės* tipo duomenų šaltinio maršrutas.

## <a name="return-values"></a>Grįžties vertės

*Konteineris*

Gauta dvejetainė vertė yra dvejetainio didelio objekto (BLOB) formatu.

## <a name="usage-notes"></a>Naudojimo pastabos

Išimtis „Parametras netinkamas” pateikiama, jei įvesties eilutėje nėra tinkamos dvejetainių teksto kodavimo schemų „Base64” grupės.

## <a name="example"></a>Pavyzdys

Apibrėžkite šiuos modelio susiejimo duomenų šaltinius:

- Šakninis *„Dynamics 365 for Operations” / Išvardijimas* tipo **„DocuTypeGroupEnum”** duomenų šaltinis nurodo **„DocuTypeGroup”** programos išvardijimą
- Šakninis *Dynamics 365 for Operations / Lentelės įrašai* tipo duomenų šaltinis **Klientas** nurodo **„CustTable”** programos lentelę
- Duomenų šaltinis **\#Laikmena,** kurio tipas yra *Apskaičiuotas laukas,* yra konfigūruojamas tokiu būdu:

    - Jis pridėtas kaip antrinis **Kliento** duomenų šaltinis.
    - Jame įtraukta išraiška `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.

- Duomenų šaltinis **\#„MediaAsBase64String”,** kurio tipas yra *Apskaičiuotas laukas,* yra konfigūruojamas tokiu būdu:

    - Jis pridėtas kaip antrinis **Kliento.'\#Laikmenos'** duomenų šaltinis.
    - Jame įtraukta išraiška `Customer.'#Media'.'getFileContentAsBase64String()'`.

- Duomenų šaltinis **\#„BlobFomBase64”,** kurio tipas yra *Apskaičiuotas laukas,* yra konfigūruojamas tokiu būdu:

    - Jis pridėtas kaip antrinis **Kliento.'\#Laikmenos'** duomenų šaltinis.
    - Jame įtraukta išraiška `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.

Šiame pavyzdyje duomenų šaltinis **\#„MediaAsBase64String”** užkoduoja dabartinio laikmenos priedo dvejetainį turinį kaip tekstą, kuris reiškia dvejetainių tekstų kodavimo schemų „Base64” grupę. Duomenų šaltinis **\#„BLOBFomBase64”** užkoduoja „Base64” eilutę ir grąžina dvejetainę vertę BLOB formatu.

![Pavyzdiniai duomenų šaltiniai ER modelio susiejimo dizaino įrankio puslapyje.](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Konteinerio funkcijos](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
