---
title: Turto skolinimas
description: Šioje temoje aprašoma, kaip modulyje Turto valdymas užregistruoti skolinamą turtą.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cba680d0ad626e0275539d7478a83639a9d22635
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433657"
---
# <a name="asset-loans"></a><span data-ttu-id="86da5-103">Turto skolinimas</span><span class="sxs-lookup"><span data-stu-id="86da5-103">Asset loans</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="86da5-104">Jei jūsų įmonė vykdo iš vidinių vietų ar klientų gauto turto remonto darbus ar priežiūros užduotis, ir jei jūs laikinai skolinate turtą šioms vietoms ar klientams, modulyje Turto valdymas galima sekti ir turto skolinimą.</span><span class="sxs-lookup"><span data-stu-id="86da5-104">If your company receives assets for repair or maintenance jobs from either internal locations or customers, and if you temporarily loan assets to those locations or customers, Asset Management can track the asset loans.</span></span>

## <a name="register-asset-loans-on-a-maintenance-request"></a><span data-ttu-id="86da5-105">Turto skolinimo registravimas pagal priežiūros užklausą</span><span class="sxs-lookup"><span data-stu-id="86da5-105">Register asset loans on a maintenance request</span></span>

1. <span data-ttu-id="86da5-106">Pasirinkite **Turto valdymas** \> **Bendra** \> **Priežiūros užklausos** \> **Visos priežiūros užklausos** arba **Aktyvios priežiūros užklausos**.</span><span class="sxs-lookup"><span data-stu-id="86da5-106">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="86da5-107">Pasirinkite priežiūros užklausą, kad užregistruotumėte skolinamą turtą, tada pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="86da5-107">Select the maintenance request to register an asset loan on, and then select **Edit**.</span></span>
3. <span data-ttu-id="86da5-108">Puslapyje **Užklausa** pasirinkite **Siųsti skolinamą turtą**.</span><span class="sxs-lookup"><span data-stu-id="86da5-108">On the **Request** page, select **Send loan asset**.</span></span>
4. <span data-ttu-id="86da5-109">Pasirinkite turtą ir įveskite numatomą grąžinimo datą.</span><span class="sxs-lookup"><span data-stu-id="86da5-109">Select the asset, and enter the expected return date.</span></span>
5. <span data-ttu-id="86da5-110">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="86da5-110">Select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="86da5-111">Skolinamą turtą galite siųsti tik tuo atveju, jei pasiekiamas to paties tipo turtas.</span><span class="sxs-lookup"><span data-stu-id="86da5-111">You can send a loan asset only if an asset of the same asset type is available.</span></span>
> - <span data-ttu-id="86da5-112">Jūsų skolinamas turtas turi turėti turto ciklo būseną, kuri leidžia jį naudoti kaip skolinamą turtą, kaip pvz., **InStorage**.</span><span class="sxs-lookup"><span data-stu-id="86da5-112">The asset that you loan must have an asset lifecycle state that allows it to be used as a loan asset, such as **InStorage**.</span></span> <span data-ttu-id="86da5-113">Kai užregistruojamas skolinamas turtas, turto ciklo būsena automatiškai atnaujinama, kaip pvz., **OnLoan**.</span><span class="sxs-lookup"><span data-stu-id="86da5-113">When the asset loan is registered, the asset lifecycle state of the asset is automatically updated to, for example, **OnLoan**.</span></span>

<span data-ttu-id="86da5-114">Norėdami peržiūrėti visą turto, kurį paskolinote kitoms vietoms ar klientams, sąrašą, pasirinkite **Turto valdymas** \> **Bendra** \> **Paskola su įkeistu turtu** \> **Visos paskolos su įkeistu turtu**.</span><span class="sxs-lookup"><span data-stu-id="86da5-114">To view a list of all the assets that you've loaned to other locations or customers, select **Asset management** \> **Common** \> **Asset loan** \> **All asset loans**.</span></span> <span data-ttu-id="86da5-115">Jei prie turto pažymėtas žymės langelis **Baigta**, turtas buvo užregistruotas kaip grąžintas jūsų įmonei.</span><span class="sxs-lookup"><span data-stu-id="86da5-115">If the **Ended** check box is selected for an asset, the asset has been registered as returned to your company.</span></span>

![Priežiūros užklausų valdymas](media/06-manage-maintenance-requests.png)

<span data-ttu-id="86da5-117">Puslapyje **Aktyvusis turto skolinimas** galite peržiūrėti visą paskolinto turto, kuris dar nebuvo grąžintas jūsų įmonei, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="86da5-117">On the **Active asset loans** page, you can view a list of all the loan assets that haven't yet been returned to your company.</span></span>

## <a name="register-loan-assets-as-returned"></a><span data-ttu-id="86da5-118">Skolinto turto grąžinimo registravimas</span><span class="sxs-lookup"><span data-stu-id="86da5-118">Register loan assets as returned</span></span>

1. <span data-ttu-id="86da5-119">Pasirinkite **Turto valdymas** \> **Bendra** \> **Paskola su įkeistu turtu** \> **Aktyvios paskolos su įkeistu turtu**.</span><span class="sxs-lookup"><span data-stu-id="86da5-119">Select **Asset management** \> **Common** \> **Asset loan** \> **Active asset loans**.</span></span>
2. <span data-ttu-id="86da5-120">Pasirinkite paskolintą turtą, kurią norite užregistruoti kaip grąžintą, tada pasirinkite **Grąžinti paskolintą turtą**.</span><span class="sxs-lookup"><span data-stu-id="86da5-120">Select the asset loan to register as returned, and then select **Return asset loan**.</span></span>
3. <span data-ttu-id="86da5-121">Laukelyje **Grąžinta** nustatykite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="86da5-121">In the **Returned** field, enter the date and time.</span></span>
4. <span data-ttu-id="86da5-122">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="86da5-122">Select **OK**.</span></span>
5. <span data-ttu-id="86da5-123">Atnaujinkite sąrašo puslapį **Aktyvusis turto skolinimas** ir pamatysite, kad paskolintas turtas nebėra rodomas sąraše.</span><span class="sxs-lookup"><span data-stu-id="86da5-123">Refresh the **Active asset loans** list page, and notice that the asset loan no longer appears in the list.</span></span>
