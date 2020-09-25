---
title: Pusmečio nusidėvėjimo konvencijos metodika
description: Šioje temoje aprašomas metodas, kurį ilgalaikis turtas naudoja nusidėvėjimui apskaičiuoti pagal pusmečio konvenciją, apskaičiuojančią šešių mėnesių nusidėvėjimą per pirmuosius ir paskutiniuosius metus, kai turtas eksploatuojamas.
author: moaamer
manager: Ann Beebe
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 578f812a0426566c6bc2b943a6b2b7b6c01b94de
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761448"
---
# <a name="half-year-depreciation-convention-methodology"></a><span data-ttu-id="cf0db-103">Pusmečio nusidėvėjimo konvencijos metodika</span><span class="sxs-lookup"><span data-stu-id="cf0db-103">Half-year depreciation convention methodology</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="cf0db-104">Šioje temoje aprašomas ilgalaikio turto metodas, naudojamas norint apskaičiuoti nusidėvėjimą naudojant pusmečio konvenciją.</span><span class="sxs-lookup"><span data-stu-id="cf0db-104">This topic describes the method that is used in fixed assets to calculate depreciation using the half-year convention.</span></span> <span data-ttu-id="cf0db-105">Pusmečio konvencija apskaičiuoja šešių mėnesių nusidėvėjimą per pirmuosius ir paskutiniuosius metus, kai turtas eksploatuojamas.</span><span class="sxs-lookup"><span data-stu-id="cf0db-105">The half-year convention calculates six months of depreciation during an asset’s first and last year of service.</span></span> <span data-ttu-id="cf0db-106">Daugiau informacijos apie nusidėvėjimo konvencijas žr. [Nusidėvėjimo metodai ir konvencijos](Fixed-asset-depreciation-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="cf0db-106">For more information about depreciation conventions, see [Depreciation methods and conventions](Fixed-asset-depreciation-conventions.md).</span></span> 

<span data-ttu-id="cf0db-107">Naudojant šešių mėnesių nusidėvėjimo konvenciją, sistema naudoja įsigijimo metus arba metus, kuriais turtas buvo atiduotas eksploatuoti, tada apskaičiuoja penkerių metų nusidėvėjimą nuo tų metų ir prideda šešis mėnesius.</span><span class="sxs-lookup"><span data-stu-id="cf0db-107">When you use the six-month depreciation convention, the system uses the acquisition year or the year that the asset was placed in service, then calculates five years of depreciation from that year, and then adds six months.</span></span> <span data-ttu-id="cf0db-108">Norėdami iliustruoti šį procesą, įsivaizduokite turtą, kuris buvo įsigytas už 50 000 ir atiduotas eksploatuoti 2020 m. balandžio mėn.</span><span class="sxs-lookup"><span data-stu-id="cf0db-108">To illustrate this process, consider an asset that was acquired for the price of 50,000, and placed in service in April 2020.</span></span> <span data-ttu-id="cf0db-109">Tarkime, kad turto dėvėjimo laikas yra penkeri metai.</span><span class="sxs-lookup"><span data-stu-id="cf0db-109">Also assume that the asset has a five-year service life.</span></span>

<span data-ttu-id="cf0db-110">Pirmieji eksploatavimo metai pasibaigs 2020 m. gruodžio mėn., o tai reiškia, kad turto penkerių metų dėvėjimo laikas pasibaigs 2024 m. gruodžio mėn.</span><span class="sxs-lookup"><span data-stu-id="cf0db-110">The first year of service will conclude in December 2020, which means the end of the asset’s five-year service life will be December 2024.</span></span> <span data-ttu-id="cf0db-111">Pusmečio nusidėvėjimo konvencija pridės šešis mėnesius prie turto dėvėjimo laiko, o tai reiškia, kad jo dėvėjimo laikas pasibaigs 2025 m. birželio mėn.</span><span class="sxs-lookup"><span data-stu-id="cf0db-111">The half-year depreciation convention will add six months to the asset’s life, which means its service life will end in June 2025.</span></span> 

> <span data-ttu-id="cf0db-112">Metinis nusidėvėjimas: 50 000 / 5 = 10 000, mėnesinis nusidėvėjimas: 10 000 / 12 = 833,33</span><span class="sxs-lookup"><span data-stu-id="cf0db-112">Yearly depreciation 50,000/5 = 10,000 monthly depreciation 10,000/12 = 833.33</span></span> <br>
> <span data-ttu-id="cf0db-113">Pirmųjų metų nusidėvėjimas: 10 000 / 2 = 5 000, vėlesnis mėnesinis nusidėvėjimas: 5 000 / 9 = 555,56</span><span class="sxs-lookup"><span data-stu-id="cf0db-113">First year depreciation 10,000/2 = 5,000  and the subsequent monthly depreciation 5,000/9 = 555.56</span></span>

   <span data-ttu-id="cf0db-114">[![Pusmečio nusidėvėjimo konvencijos nusidėvėjimo grafikas](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span><span class="sxs-lookup"><span data-stu-id="cf0db-114">[![Depreciation schedule for half-year depreciation convention](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span></span>

<span data-ttu-id="cf0db-115">Išplėsti nusidėvėjimo laikotarpiai, kuriuos pradeda pusmečio konvencija, leidžia tiksliau paskirstyti nusidėvėjimą.</span><span class="sxs-lookup"><span data-stu-id="cf0db-115">The extended depreciation periods that are added by the half-year convention provide more accurate allocation of depreciation.</span></span> <span data-ttu-id="cf0db-116">Šešių mėnesių konvencija tolygiai nurodo nusidėvėjimo išlaidas, o tai naudinga pelno ir nuostolio išrašo ataskaitose.</span><span class="sxs-lookup"><span data-stu-id="cf0db-116">The six-month convention represents depreciation expenses more equally, which is useful for reporting on the profit and loss statement.</span></span>
