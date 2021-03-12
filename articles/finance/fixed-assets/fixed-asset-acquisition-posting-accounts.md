---
title: Ilgalaikio turto įsigijimo registravimo sąskaitos
description: Šiame straipsnyje paaiškinama, kaip nustatyti turto įgijimo DK registravimo sąskaitas.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa0d73790a20f3fe5bb76b87e635b1f16e034479
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976121"
---
# <a name="fixed-asset-acquisition-posting-accounts"></a><span data-ttu-id="fb66f-103">Ilgalaikio turto įsigijimo registravimo sąskaitos</span><span class="sxs-lookup"><span data-stu-id="fb66f-103">Fixed asset acquisition posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb66f-104">Šiame straipsnyje paaiškinama, kaip nustatyti turto įgijimo DK registravimo sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="fb66f-104">This article explains how to set up general ledger posting accounts for acquiring assets.</span></span>

<span data-ttu-id="fb66f-105">Sąskaitos, naudojamos registruoti ilgalaikio turto įsigijimams, gali skirtis – tai priklauso nuo turtui įsigyti naudoto metodo.</span><span class="sxs-lookup"><span data-stu-id="fb66f-105">Accounts used for posting fixed asset acquisitions may vary depending upon the method used to acquire the asset.</span></span> <span data-ttu-id="fb66f-106">Ilgalaikio turto registravimo profilių puslapyje, skirtuke DK sąskaitos pasirinkite Įsigijimas ir Įsigijimo koregavimas, kad nustatytumėte ilgalaikio turto sąskaitas, registruotinas DK.</span><span class="sxs-lookup"><span data-stu-id="fb66f-106">On the Fixed asset posting profiles page, on the Ledger accounts tab, select Acquisition and Acquisition adjustment to set up fixed asset accounts to post to the ledger.</span></span> 

<span data-ttu-id="fb66f-107">Dažniausiai žurnaluose ir pirkimo užsakymuose DK sąskaita yra balanso sąskaita, kurioje yra pridedama naujo ilgalaikio turto įgijimo vertė.</span><span class="sxs-lookup"><span data-stu-id="fb66f-107">In journals and on purchase orders, Ledger account is typically the balance sheet account, where the acquisition value of the new fixed asset is debited.</span></span> <span data-ttu-id="fb66f-108">Ši sąskaita nerodoma žurnale ir negali būti pakeista operacijose.</span><span class="sxs-lookup"><span data-stu-id="fb66f-108">This account is not displayed in the journal and cannot be replaced in transactions.</span></span> 

<span data-ttu-id="fb66f-109">Korespondentinė sąskaita taip pat yra balanso sąskaita.</span><span class="sxs-lookup"><span data-stu-id="fb66f-109">Offset account is also a balance sheet account.</span></span> <span data-ttu-id="fb66f-110">Bendrajame ir ilgalaikio turto žurnaluose, ši sąskaita dažnai naudojama kaip banko sąskaita, iš kurios mokama už turto įsigijimą.</span><span class="sxs-lookup"><span data-stu-id="fb66f-110">In the general journal and in the fixed assets journal, this account often will be the bank account that is used to pay for the acquisition of the asset.</span></span> <span data-ttu-id="fb66f-111">Korespondentinė sąskaita yra numatytoji, kuri yra siūloma žurnaluose.</span><span class="sxs-lookup"><span data-stu-id="fb66f-111">The offset account is a default account, which is suggested in the journals.</span></span> <span data-ttu-id="fb66f-112">Žurnale ji gali būti pakeista bet kuria kita sąskaita iš sąskaitų plano arba tiekėjo sąskaita, jei ilgalaikis turtas buvo pirktas iš tiekėjo.</span><span class="sxs-lookup"><span data-stu-id="fb66f-112">It can be changed in the journal to any other account from the chart of accounts or to a vendor account, if the fixed asset was purchase from a vendor.</span></span> 

<span data-ttu-id="fb66f-113">Kai SF žurnalas arba Pirkimo užsakymai, esantys Mokėtinose sumose, naudojami ilgalaikiam turtui įsigyti, ilgalaikio turto operacijos korespondentinė sąskaita pakeičiama operacijai pasirinkta tiekėjo sąskaita.</span><span class="sxs-lookup"><span data-stu-id="fb66f-113">When Invoice journal or Purchase orders in Accounts payable are used for fixed asset acquisitions, the offset account for the fixed asset transaction is replaced by the vendor account that is selected for the transaction.</span></span>

<span data-ttu-id="fb66f-114">Įgijimams, registruotiems naudojant žurnalą Atsargos į ilgalaikį turtą, esančiu DK, ilgalaikis turtas perkamas ne iš išorinių šaltinių, o perkeliamas iš įmonės atsargų.</span><span class="sxs-lookup"><span data-stu-id="fb66f-114">For acquisitions posted using the Inventory to fixed assets journal in General ledger, the fixed asset is not bought from external sources, but transferred from the company's own inventory.</span></span> <span data-ttu-id="fb66f-115">Todėl korespondentinė sąskaita yra atsargų valdymo atsargų prekės išdavimo sąskaita.</span><span class="sxs-lookup"><span data-stu-id="fb66f-115">Therefore, the offset account is an inventory issue account for the inventory item in Inventory management.</span></span>

<span data-ttu-id="fb66f-116">Norėdami gauti daugiau informacijos, žr. [Turto pirkimas įsigyjant](acquire-assets-procurement.md).</span><span class="sxs-lookup"><span data-stu-id="fb66f-116">For more information, see [Acquire assets through procurement](acquire-assets-procurement.md).</span></span>



