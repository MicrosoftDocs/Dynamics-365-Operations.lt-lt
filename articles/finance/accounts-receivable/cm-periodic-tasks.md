---
title: Periodinės kredito valdymo užduotys
description: Šioje temoje aprašomos periodinės užduotys, kurios yra būtina klientų kredito limitų valdymo proceso dalis.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4ca9bb7f77283ec30d4648d6763f4156494050ac
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124167"
---
# <a name="periodic-credit-management-tasks"></a><span data-ttu-id="beefe-103">Periodinės kredito valdymo užduotys</span><span class="sxs-lookup"><span data-stu-id="beefe-103">Periodic credit management tasks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="beefe-104">Šioje temoje aprašomos periodinės užduotys, kurios yra būtina klientų kredito limitų valdymo proceso dalis.</span><span class="sxs-lookup"><span data-stu-id="beefe-104">This topic describes the periodic tasks that are a necessary part of the process of managing credit limits for customers.</span></span>

## <a name="update-risk-scores"></a><span data-ttu-id="beefe-105">Naujinti rizikos rezultatus</span><span class="sxs-lookup"><span data-stu-id="beefe-105">Update risk scores</span></span>

<span data-ttu-id="beefe-106">Kai verslas vystosi ir pasikeičia aplinkybės, tam tikro kliento kredito rizika taip pat gali pasikeisti.</span><span class="sxs-lookup"><span data-stu-id="beefe-106">As businesses evolve and circumstances change, the credit risks for a given customer can also change.</span></span> <span data-ttu-id="beefe-107">Norėdami padėti išlaikyti atitinkamus savo klientų kreditų limitus, turite periodiškai peržiūrėti kiekvieno rizikos balo kriterijus ir atnaujinti kiekvieno kliento balus.</span><span class="sxs-lookup"><span data-stu-id="beefe-107">To help maintain appropriate credit limits for your customers, you must periodically review the criteria for each risk score and update the scores for each customer.</span></span> <span data-ttu-id="beefe-108">Galite atnaujinti šiuos balus puslapyje **Naujinti rizikos balus** (**Kreditai ir mokėjimų priežiūra \> Periodinės užduotys \> Kreditų valdymas \> Naujinti rizikos balus**).</span><span class="sxs-lookup"><span data-stu-id="beefe-108">You can update the following scores by using the **Update risk scores** page (**Credit and collections \> Periodic tasks \> Credit management \> Update risk scores**).</span></span> <span data-ttu-id="beefe-109">Visi vartotojo apibrėžti skaičiavimai taip pat apdorojami.</span><span class="sxs-lookup"><span data-stu-id="beefe-109">All user-defined calculations are also processed.</span></span>

- <span data-ttu-id="beefe-110">**Vidutinės mokėjimo dienos** – šis balas yra vidutinis dienų, per kurias klientas turi apmokėti SF, skaičius.</span><span class="sxs-lookup"><span data-stu-id="beefe-110">**Average payment days** – This score is the average number of days that a customer takes to pay invoices.</span></span>
- <span data-ttu-id="beefe-111">**Klientas nuo datos** – šis balas yra metų, kuriuos klientas yra jūsų organizacijos klientas, skaičius.</span><span class="sxs-lookup"><span data-stu-id="beefe-111">**Customer since** – This score is the number of years that a customer has been a customer of your organization.</span></span>
- <span data-ttu-id="beefe-112">**Vykdo verslą nuo** – šis balas yra metų, kuriuos klientas vykdo verslą, skaičius.</span><span class="sxs-lookup"><span data-stu-id="beefe-112">**In business since** – This score is the number of years that a customer has been in business.</span></span> <span data-ttu-id="beefe-113">Tai naudoja lauko **Verslo pradžios data** puslapyje **Klientai** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="beefe-113">It uses the value of the **Business start** field on the **Customers** page.</span></span>
- <span data-ttu-id="beefe-114">**Neapmokėto pardavimo dienos** – šis balas yra paremtas gautinų sumų balansu, pardavimo įplaukomis ir dienų skaičiumi per ankstesnį 12 mėnesių laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="beefe-114">**Days sales outstanding** – This score is based on the accounts receivable balance, sales revenue, and number of days for the previous 12-month period.</span></span>
- <span data-ttu-id="beefe-115">**Vidutinis balansas** – šis balas paremtas gautinų sumų balansu per ankstesnį 12 mėnesių laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="beefe-115">**Average balance** – This score is based on the accounts receivable balance for the previous 12-month period.</span></span>
- <span data-ttu-id="beefe-116">**Kredito valdymo grupė**, **Sąskaitų būsena** ir **Šalis** – šie balai naudoja kliento informaciją.</span><span class="sxs-lookup"><span data-stu-id="beefe-116">**Credit management group**, **Account status**, and **Country** – These scores use information from the customer.</span></span>

## <a name="update-customer-balance-statistics"></a><span data-ttu-id="beefe-117">Kliento balanso statistikos naujinimas</span><span class="sxs-lookup"><span data-stu-id="beefe-117">Update customer balance statistics</span></span>

<span data-ttu-id="beefe-118">Galite vykdyti procesą **Kliento balanso statistikos naujinimas** norėdami atnaujinti balanso statistikos, rodomos puslapyje **Balanso statistikos užklausos**, skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="beefe-118">You can run the **Update customer balance statistics** process to update the calculation of balance statistics that is shown on the **Balance statistics inquiry** page.</span></span> <span data-ttu-id="beefe-119">Ši informacija naudojama norint apskaičiuoti rizikos balus ir reikšmes, kurios rodomos statistikos „FactBox“ puslapyje **Klientas**.</span><span class="sxs-lookup"><span data-stu-id="beefe-119">This information is used to calculate risk scores and the values that are shown in the credit statistics FactBoxes on the **Customer** page.</span></span>

<span data-ttu-id="beefe-120">Paleidus procesą, jis atnaujina vieno kliento balanso statistiką.</span><span class="sxs-lookup"><span data-stu-id="beefe-120">When you run the process, it updates customer balance statistics for a single customer.</span></span> <span data-ttu-id="beefe-121">Norėdami nustatyti paketines užduotis, kad būtų galima vykdyti procesą keliems klientams, galite naudoti puslapį **Skaičiuoti balanso statistiką** (**Kreditų valdymas \> Periodinės užduotys \> Skaičiuoti balanso statistiką**).</span><span class="sxs-lookup"><span data-stu-id="beefe-121">To set up a batch job to run the process for multiple customers, you can use the **Calculate balance statistics** page (**Credit management \> Periodic tasks \> Calculate balance statistics**).</span></span>