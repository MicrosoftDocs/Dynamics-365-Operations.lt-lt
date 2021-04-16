---
title: Pardavimo pasiūlymų trikčių diagnostika
description: Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti kol dirbate su pardavimo pasiūlymais.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 09529ba729170be7281e2ae04008d3ba4a58e060
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824755"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="3e6b6-103">Pardavimo pasiūlymų trikčių diagnostika</span><span class="sxs-lookup"><span data-stu-id="3e6b6-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="3e6b6-104">Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti kol dirbate su pardavimo pasiūlymais.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="3e6b6-105">Negaliu pakeisti pardavimo pasiūlymo pardavimų kiekio aptarnavimo prekei.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3e6b6-106">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="3e6b6-106">Issue description</span></span>

<span data-ttu-id="3e6b6-107">Jei pardavimo pasiūlymo eilutėje bandysite nustatyti prekės, kurios tipas yra *Paslauga*, pardavimų kiekį (**SalesQty** laukas), jūs gausite tokį pranešimą: „Atnaujinimas neleidžiamas kiekio laukui.“</span><span class="sxs-lookup"><span data-stu-id="3e6b6-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3e6b6-108">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="3e6b6-108">Issue resolution</span></span>

<span data-ttu-id="3e6b6-109">Negalite nustatyti produktų, kurie yra aptarnavimo prekės, pardavimų kiekio.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="3e6b6-110">Pavyzdžiui, jei jūs siūlote paslaugą prekei įdiegti, nėra prasminga įrašyti kiekį, nes nėra faktinių prekių.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="3e6b6-111">Yra tik paslauga.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-111">There is only a service.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]