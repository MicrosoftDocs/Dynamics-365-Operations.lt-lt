---
title: Bendrojo plano parametrai neegzistuoja
description: Kai bandote patvirtinti suplanuotą užsakymą, rodomas klaidos pranešimas, kuriame teigiama, kad nėra bendrojo plano parametrų.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294139"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a><span data-ttu-id="7ae86-103">Bendrojo plano parametrai neegzistuoja</span><span class="sxs-lookup"><span data-stu-id="7ae86-103">Parameters for the master plan don't exist</span></span>

<span data-ttu-id="7ae86-104">Klaidos kodas: SYS25368</span><span class="sxs-lookup"><span data-stu-id="7ae86-104">Error code: SYS25368</span></span>

## <a name="symptoms"></a><span data-ttu-id="7ae86-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="7ae86-105">Symptoms</span></span>

<span data-ttu-id="7ae86-106">Kai bandote patvirtinti suplanuotą užsakymą, gaunate tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="7ae86-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="7ae86-107">Nėra bendrojo plano %1 parametrų.</span><span class="sxs-lookup"><span data-stu-id="7ae86-107">Parameters for master plan %1 do not exist.</span></span>

## <a name="cause"></a><span data-ttu-id="7ae86-108">Priežastis</span><span class="sxs-lookup"><span data-stu-id="7ae86-108">Cause</span></span>

<span data-ttu-id="7ae86-109">Dėl konfigūravimo problemų sistema negali rasti nurodyto plano parametrų.</span><span class="sxs-lookup"><span data-stu-id="7ae86-109">Because of configuration issues, the system can't find the settings for the specified plan.</span></span>

## <a name="resolution"></a><span data-ttu-id="7ae86-110">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="7ae86-110">Resolution</span></span>

- <span data-ttu-id="7ae86-111">Eikite į **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai** ir įsitikinkite, kad egzistuoja planas su nurodytu pavadinimu.</span><span class="sxs-lookup"><span data-stu-id="7ae86-111">Go to **Master planning \> Setup \> Plans \> Master plans**, and make sure that a plan that has the specified name exists.</span></span>
