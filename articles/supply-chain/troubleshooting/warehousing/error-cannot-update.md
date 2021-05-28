---
title: Registruojant išrinkimo sąrašą pasirenkama vieta, įvyko klaida
description: Registruojant išrinkimo sąrašą pasirenkama vieta, įvyko klaida.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b7fc579821f9a80d94aea949fcc0301b9d8f6935
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026729"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a><span data-ttu-id="54983-103">Registruojant išrinkimo sąrašą pasirenkama vieta, įvyko klaida</span><span class="sxs-lookup"><span data-stu-id="54983-103">An error occurs when the location is selected during picking list registration</span></span>

<span data-ttu-id="54983-104">KB numeris: 4613106</span><span class="sxs-lookup"><span data-stu-id="54983-104">KB number: 4613106</span></span>

## <a name="symptoms"></a><span data-ttu-id="54983-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="54983-105">Symptoms</span></span>

<span data-ttu-id="54983-106">Ši problema kyla, kai jūsų sistema konfigūruota automatiškai rezervuoti pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="54983-106">This issue occurs when your system is configured to automatically reserve sales orders.</span></span> <span data-ttu-id="54983-107">Jei bandote pasirinkti vietą išrinkimo dokumento registravimo eilutei, naudodami sandėlio valdymo (WMS) rezervavimo procesus, gaunate toliau nurodytą klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="54983-107">If you try to select the location for a picking list registration line, you receive the following error message when you use warehouse management (WMS) reservation processes:</span></span>

> <span data-ttu-id="54983-108">Negalima atnaujinti kiekio su naujomis dimensijomis</span><span class="sxs-lookup"><span data-stu-id="54983-108">Can't update quantity with new dimensions</span></span>

<span data-ttu-id="54983-109">Šis išdavimas gali atsirasti, nes tam tikrai vietai nepakanka turimų atsargų.</span><span class="sxs-lookup"><span data-stu-id="54983-109">This issue can occur because you don't have enough on-hand inventory at a specified location.</span></span>

## <a name="resolution"></a><span data-ttu-id="54983-110">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="54983-110">Resolution</span></span>

<span data-ttu-id="54983-111">Sistema veikia kaip sukurta.</span><span class="sxs-lookup"><span data-stu-id="54983-111">The system is behaving as designed.</span></span>

<span data-ttu-id="54983-112">Scenarijuose, kuriuose naudojate sandėlio lygio rezervavimo procesą, jei turimos atsargos nebus rezervuojamos visuose atsargų dimensijų lygiuose ir jei tam tikrai vietai nepakanka turimų atsargų, rekomenduojame naudoti rezervavimo iš išrinkimo eilutės neautomatiniu būdu procesą.</span><span class="sxs-lookup"><span data-stu-id="54983-112">In scenarios where you use the warehouse-level reservation process, if the on-hand inventory won't be reserved on all inventory dimension levels, and you don't have enough on-hand inventory at a specified location, we recommend that you use the manual reservation process from the picking line.</span></span> <span data-ttu-id="54983-113">Tada galite naudoti funkciją *Rezervuoti partiją* norėdami paskirstyti visų turimus kiekius mažesnius rezervavimus, pvz., vietą.</span><span class="sxs-lookup"><span data-stu-id="54983-113">You can then use the *Reserve lot* function to distribute the lower reservations, such as location, for all the available on-hand quantities.</span></span>
