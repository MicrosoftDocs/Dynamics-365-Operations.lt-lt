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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 98011dbf22ff55b7651ce63557fa4a360130b6af
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974765"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="ce787-103">Pardavimo pasiūlymų trikčių diagnostika</span><span class="sxs-lookup"><span data-stu-id="ce787-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="ce787-104">Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti kol dirbate su pardavimo pasiūlymais.</span><span class="sxs-lookup"><span data-stu-id="ce787-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="ce787-105">Negaliu pakeisti pardavimo pasiūlymo pardavimų kiekio aptarnavimo prekei.</span><span class="sxs-lookup"><span data-stu-id="ce787-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ce787-106">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="ce787-106">Issue description</span></span>

<span data-ttu-id="ce787-107">Jei pardavimo pasiūlymo eilutėje bandysite nustatyti prekės, kurios tipas yra *Paslauga*, pardavimų kiekį (**SalesQty** laukas), jūs gausite tokį pranešimą: „Atnaujinimas neleidžiamas kiekio laukui.“</span><span class="sxs-lookup"><span data-stu-id="ce787-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ce787-108">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="ce787-108">Issue resolution</span></span>

<span data-ttu-id="ce787-109">Negalite nustatyti produktų, kurie yra aptarnavimo prekės, pardavimų kiekio.</span><span class="sxs-lookup"><span data-stu-id="ce787-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="ce787-110">Pavyzdžiui, jei jūs siūlote paslaugą prekei įdiegti, nėra prasminga įrašyti kiekį, nes nėra faktinių prekių.</span><span class="sxs-lookup"><span data-stu-id="ce787-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="ce787-111">Yra tik paslauga.</span><span class="sxs-lookup"><span data-stu-id="ce787-111">There is only a service.</span></span>

