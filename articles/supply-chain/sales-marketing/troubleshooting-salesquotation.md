---
title: Pardavimo pasiūlymų trikčių diagnostika
description: Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti kol dirbate su pardavimo pasiūlymais.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 67610a833be132399b2d47ae8c6b27119be9ce95
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834397"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="84ab9-103">Pardavimo pasiūlymų trikčių diagnostika</span><span class="sxs-lookup"><span data-stu-id="84ab9-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="84ab9-104">Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti kol dirbate su pardavimo pasiūlymais.</span><span class="sxs-lookup"><span data-stu-id="84ab9-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="84ab9-105">Negaliu pakeisti pardavimo pasiūlymo pardavimų kiekio aptarnavimo prekei.</span><span class="sxs-lookup"><span data-stu-id="84ab9-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="84ab9-106">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="84ab9-106">Issue description</span></span>

<span data-ttu-id="84ab9-107">Jei pardavimo pasiūlymo eilutėje bandysite nustatyti prekės, kurios tipas yra *Paslauga*, pardavimų kiekį (**SalesQty** laukas), jūs gausite tokį pranešimą: „Atnaujinimas neleidžiamas kiekio laukui.“</span><span class="sxs-lookup"><span data-stu-id="84ab9-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="84ab9-108">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="84ab9-108">Issue resolution</span></span>

<span data-ttu-id="84ab9-109">Negalite nustatyti produktų, kurie yra aptarnavimo prekės, pardavimų kiekio.</span><span class="sxs-lookup"><span data-stu-id="84ab9-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="84ab9-110">Pavyzdžiui, jei jūs siūlote paslaugą prekei įdiegti, nėra prasminga įrašyti kiekį, nes nėra faktinių prekių.</span><span class="sxs-lookup"><span data-stu-id="84ab9-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="84ab9-111">Yra tik paslauga.</span><span class="sxs-lookup"><span data-stu-id="84ab9-111">There is only a service.</span></span>

