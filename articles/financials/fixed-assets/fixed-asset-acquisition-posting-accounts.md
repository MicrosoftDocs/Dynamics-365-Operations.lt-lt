---
title: "Ilgalaikio turto įsigijimo registravimo sąskaitos"
description: "Šiame straipsnyje paaiškinama, kaip nustatyti turto įgijimo DK registravimo sąskaitas."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 887616463856875e2382a00b1d56520391ead844
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="fixed-asset-acquisition-posting-accounts"></a><span data-ttu-id="2aa04-103">Ilgalaikio turto įsigijimo registravimo sąskaitos</span><span class="sxs-lookup"><span data-stu-id="2aa04-103">Fixed asset acquisition posting accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2aa04-104">Šiame straipsnyje paaiškinama, kaip nustatyti turto įgijimo DK registravimo sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="2aa04-104">This article explains how to set up general ledger posting accounts for acquiring assets.</span></span>

<span data-ttu-id="2aa04-105">Sąskaitos, naudojamos registruoti ilgalaikio turto įsigijimams, gali skirtis – tai priklauso nuo turtui įsigyti naudoto metodo.</span><span class="sxs-lookup"><span data-stu-id="2aa04-105">Accounts used for posting fixed asset acquisitions may vary depending upon the method used to acquire the asset.</span></span> <span data-ttu-id="2aa04-106">Ilgalaikio turto registravimo profilių puslapyje, skirtuke DK sąskaitos pasirinkite Įsigijimas ir Įsigijimo koregavimas, kad nustatytumėte ilgalaikio turto sąskaitas, registruotinas DK.</span><span class="sxs-lookup"><span data-stu-id="2aa04-106">On the Fixed asset posting profiles page, on the Ledger accounts tab, select Acquisition and Acquisition adjustment to set up fixed asset accounts to post to the ledger.</span></span> 

<span data-ttu-id="2aa04-107">Dažniausiai žurnaluose ir pirkimo užsakymuose DK sąskaita yra balanso sąskaita, kurioje yra pridedama naujo ilgalaikio turto įgijimo vertė.</span><span class="sxs-lookup"><span data-stu-id="2aa04-107">In journals and on purchase orders, Ledger account is typically the balance sheet account, where the acquisition value of the new fixed asset is debited.</span></span> <span data-ttu-id="2aa04-108">Ši sąskaita nerodoma žurnale ir negali būti pakeista operacijose.</span><span class="sxs-lookup"><span data-stu-id="2aa04-108">This account is not displayed in the journal and cannot be replaced in transactions.</span></span> 

<span data-ttu-id="2aa04-109">Korespondentinė sąskaita taip pat yra balanso sąskaita.</span><span class="sxs-lookup"><span data-stu-id="2aa04-109">Offset account is also a balance sheet account.</span></span> <span data-ttu-id="2aa04-110">Bendrajame ir ilgalaikio turto žurnaluose, ši sąskaita dažnai naudojama kaip banko sąskaita, iš kurios mokama už turto įsigijimą.</span><span class="sxs-lookup"><span data-stu-id="2aa04-110">In the general journal and in the fixed assets journal, this account often will be the bank account that is used to pay for the acquisition of the asset.</span></span> <span data-ttu-id="2aa04-111">Korespondentinė sąskaita yra numatytoji, kuri yra siūloma žurnaluose.</span><span class="sxs-lookup"><span data-stu-id="2aa04-111">The offset account is a default account, which is suggested in the journals.</span></span> <span data-ttu-id="2aa04-112">Žurnale ji gali būti pakeista bet kuria kita sąskaita iš sąskaitų plano arba tiekėjo sąskaita, jei ilgalaikis turtas buvo pirktas iš tiekėjo.</span><span class="sxs-lookup"><span data-stu-id="2aa04-112">It can be changed in the journal to any other account from the chart of accounts or to a vendor account, if the fixed asset was purchase from a vendor.</span></span> 

<span data-ttu-id="2aa04-113">Kai SF žurnalas arba Pirkimo užsakymai, esantys Mokėtinose sumose, naudojami ilgalaikiam turtui įsigyti, ilgalaikio turto operacijos korespondentinė sąskaita pakeičiama operacijai pasirinkta tiekėjo sąskaita.</span><span class="sxs-lookup"><span data-stu-id="2aa04-113">When Invoice journal or Purchase orders in Accounts payable are used for fixed asset acquisitions, the offset account for the fixed asset transaction is replaced by the vendor account that is selected for the transaction.</span></span>

<span data-ttu-id="2aa04-114">Įgijimams, registruotiems naudojant žurnalą Atsargos į ilgalaikį turtą, esančiu DK, ilgalaikis turtas perkamas ne iš išorinių šaltinių, o perkeliamas iš įmonės atsargų.</span><span class="sxs-lookup"><span data-stu-id="2aa04-114">For acquisitions posted using the Inventory to fixed assets journal in General ledger, the fixed asset is not bought from external sources, but transferred from the company's own inventory.</span></span> <span data-ttu-id="2aa04-115">Todėl korespondentinė sąskaita yra atsargų valdymo atsargų prekės išdavimo sąskaita.</span><span class="sxs-lookup"><span data-stu-id="2aa04-115">Therefore, the offset account is an inventory issue account for the inventory item in Inventory management.</span></span>

<span data-ttu-id="2aa04-116">Norėdami gauti daugiau informacijos, žr. [Turto pirkimas įsigyjant](acquire-assets-procurement.md).</span><span class="sxs-lookup"><span data-stu-id="2aa04-116">For more information, see [Acquire assets through procurement](acquire-assets-procurement.md).</span></span>




