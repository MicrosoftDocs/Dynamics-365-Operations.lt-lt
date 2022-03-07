---
title: „Base64StringToContainer” ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) „Base64StringToContainer” funkcija.
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
ms.openlocfilehash: 3e813c628bfe783fb8e93fc5d7e8b275405245c42710f9ea691d4c06afff0d84
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772037"
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
