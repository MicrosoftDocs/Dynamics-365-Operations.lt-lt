---
title: Paskutinio patikrintos datos laukas nėra atnaujinamas, kai sukuriami keli kokybės užsakymai
description: Paskutinio patikrintos datos laukas nėra atnaujinamas, kai sukuriami keli kokybės užsakymai.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026756"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a><span data-ttu-id="76a45-103">Paskutinio patikrintos datos laukas nėra atnaujinamas, kai sukuriami keli kokybės užsakymai</span><span class="sxs-lookup"><span data-stu-id="76a45-103">The Last tested date field isn't updated when multiple quality orders are created</span></span>

<span data-ttu-id="76a45-104">KB numeris: 4612803</span><span class="sxs-lookup"><span data-stu-id="76a45-104">KB number: 4612803</span></span>

## <a name="symptoms"></a><span data-ttu-id="76a45-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="76a45-105">Symptoms</span></span>

<span data-ttu-id="76a45-106">Laukas **paskutinio patikrintos dato** nėra atnaujinamas, kai sukuriami keli kokybės užsakymai.</span><span class="sxs-lookup"><span data-stu-id="76a45-106">The **Last tested date** field isn't updated when multiple quality orders are created.</span></span>

## <a name="resolution"></a><span data-ttu-id="76a45-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="76a45-107">Resolution</span></span>

<span data-ttu-id="76a45-108">Sistema veikia kaip sukurta.</span><span class="sxs-lookup"><span data-stu-id="76a45-108">The system is behaving as designed.</span></span> <span data-ttu-id="76a45-109">Paskutinė patikrinta data nėra susijusi su kokybės užsakymais.</span><span class="sxs-lookup"><span data-stu-id="76a45-109">The last tested date isn't related to quality orders.</span></span> <span data-ttu-id="76a45-110">Joje saugoma data, kada baigtos prekės pirmą kartą buvo nupirktos arba pagamintos.</span><span class="sxs-lookup"><span data-stu-id="76a45-110">It stores the date when the finished goods were first purchased or manufactured.</span></span> <span data-ttu-id="76a45-111">Ši data naudojama apskaičiuojant pranešimo apie laikymo trukmę datą.</span><span class="sxs-lookup"><span data-stu-id="76a45-111">This date is used to calculate the shelf life advice date.</span></span>
