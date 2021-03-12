---
title: „Base64StringToContainer” ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) „Base64StringToContainer” funkcija.
author: NickSelin
manager: kfend
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 0e92ae41a3e0f03cb14d4791ab768f096f2a0523
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739098"
---
# <a name="base64stringtocontainer-er-function"></a><span data-ttu-id="b75e4-103">„Base64StringToContainer” ER funkcija</span><span class="sxs-lookup"><span data-stu-id="b75e4-103">Base64StringToContainer ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b75e4-104">„`BASE64STRINGTOCONTAINER`” [funkcija](er-formula-language.md#functions) konvertuoja nurodytą *Eilutės* tipo įvestį į *[Konteinerio](er-functions-category-container.md)* tipo duomenų elementą.</span><span class="sxs-lookup"><span data-stu-id="b75e4-104">The `BASE64STRINGTOCONTAINER` [function](er-formula-language.md#functions) converts the specified input of the *String* type to a data item of the *[Container](er-functions-category-container.md)* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="b75e4-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="b75e4-105">Syntax</span></span>

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a><span data-ttu-id="b75e4-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="b75e4-106">Arguments</span></span>

<span data-ttu-id="b75e4-107">`input`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="b75e4-107">`input`: *String*</span></span>

<span data-ttu-id="b75e4-108">Tinkamas *Eilutės* tipo duomenų šaltinio maršrutas.</span><span class="sxs-lookup"><span data-stu-id="b75e4-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="b75e4-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="b75e4-109">Return values</span></span>

<span data-ttu-id="b75e4-110">*Konteineris*</span><span class="sxs-lookup"><span data-stu-id="b75e4-110">*Container*</span></span>

<span data-ttu-id="b75e4-111">Gauta dvejetainė vertė yra dvejetainio didelio objekto (BLOB) formatu.</span><span class="sxs-lookup"><span data-stu-id="b75e4-111">The resulting binary value in binary large object (BLOB) format.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b75e4-112">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="b75e4-112">Usage notes</span></span>

<span data-ttu-id="b75e4-113">Išimtis „Parametras netinkamas” pateikiama, jei įvesties eilutėje nėra tinkamos dvejetainių teksto kodavimo schemų „Base64” grupės.</span><span class="sxs-lookup"><span data-stu-id="b75e4-113">The "Parameter is not valid" exception is thrown if the input string doesn't provide a correct Base64 group of binary-to-text encoding schemes.</span></span>

## <a name="example"></a><span data-ttu-id="b75e4-114">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="b75e4-114">Example</span></span>

<span data-ttu-id="b75e4-115">Apibrėžkite šiuos modelio susiejimo duomenų šaltinius:</span><span class="sxs-lookup"><span data-stu-id="b75e4-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="b75e4-116">Šakninis *„Dynamics 365 for Operations” / Išvardijimas* tipo **„DocuTypeGroupEnum”** duomenų šaltinis nurodo **„DocuTypeGroup”** programos išvardijimą</span><span class="sxs-lookup"><span data-stu-id="b75e4-116">The root **DocuTypeGroupEnum** data source of the *Dynamics 365 for Operations / Enumeration* type that refers to the **DocuTypeGroup** application enumeration</span></span>
- <span data-ttu-id="b75e4-117">Šakninis *Dynamics 365 for Operations / Lentelės įrašai* tipo duomenų šaltinis **Klientas** nurodo **„CustTable”** programos lentelę</span><span class="sxs-lookup"><span data-stu-id="b75e4-117">The root **Customer** data source of the *Dynamics 365 for Operations / Table records* type that refers to the **CustTable** application table</span></span>
- <span data-ttu-id="b75e4-118">Duomenų šaltinis **\#Laikmena,** kurio tipas yra *Apskaičiuotas laukas,* yra konfigūruojamas tokiu būdu:</span><span class="sxs-lookup"><span data-stu-id="b75e4-118">The **\#Media** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="b75e4-119">Jis pridėtas kaip antrinis **Kliento** duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="b75e4-119">It's added as a child data source of the **Customer** data source.</span></span>
    - <span data-ttu-id="b75e4-120">Jame įtraukta išraiška `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span><span class="sxs-lookup"><span data-stu-id="b75e4-120">It contains the expression `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span></span>

- <span data-ttu-id="b75e4-121">Duomenų šaltinis **\#„MediaAsBase64String”,** kurio tipas yra *Apskaičiuotas laukas,* yra konfigūruojamas tokiu būdu:</span><span class="sxs-lookup"><span data-stu-id="b75e4-121">The **\#MediaAsBase64String** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="b75e4-122">Jis pridėtas kaip antrinis **Kliento.'\#Laikmenos'** duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="b75e4-122">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="b75e4-123">Jame įtraukta išraiška `Customer.'#Media'.'getFileContentAsBase64String()'`.</span><span class="sxs-lookup"><span data-stu-id="b75e4-123">It contains the expression `Customer.'#Media'.'getFileContentAsBase64String()'`.</span></span>

- <span data-ttu-id="b75e4-124">Duomenų šaltinis **\#„BlobFomBase64”,** kurio tipas yra *Apskaičiuotas laukas,* yra konfigūruojamas tokiu būdu:</span><span class="sxs-lookup"><span data-stu-id="b75e4-124">The **\#BlobFomBase64** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="b75e4-125">Jis pridėtas kaip antrinis **Kliento.'\#Laikmenos'** duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="b75e4-125">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="b75e4-126">Jame įtraukta išraiška `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span><span class="sxs-lookup"><span data-stu-id="b75e4-126">It contains the expression `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span></span>

<span data-ttu-id="b75e4-127">Šiame pavyzdyje duomenų šaltinis **\#„MediaAsBase64String”** užkoduoja dabartinio laikmenos priedo dvejetainį turinį kaip tekstą, kuris reiškia dvejetainių tekstų kodavimo schemų „Base64” grupę.</span><span class="sxs-lookup"><span data-stu-id="b75e4-127">In this example, the **\#MediaAsBase64String** data source encodes the binary content of the current media attachment as text that represents a Base64 group of binary-to-text encoding schemes.</span></span> <span data-ttu-id="b75e4-128">Duomenų šaltinis **\#„BLOBFomBase64”** užkoduoja „Base64” eilutę ir grąžina dvejetainę vertę BLOB formatu.</span><span class="sxs-lookup"><span data-stu-id="b75e4-128">The **\#BlobFomBase64** data source decodes the Base64 string and returns a binary value in BLOB format.</span></span>

![Pavyzdiniai duomenų šaltiniai ER modelio susiejimo dizaino įrankio puslapyje](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a><span data-ttu-id="b75e4-130">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b75e4-130">Additional resources</span></span>

[<span data-ttu-id="b75e4-131">Konteinerio funkcijos</span><span class="sxs-lookup"><span data-stu-id="b75e4-131">Container functions</span></span>](er-functions-category-container.md)
