--- 
title: " Registrų kūrimas ir susiejimas"
description: "Šioje procedūroje parodoma, kaip kurti elektroninio kasos aparato (POS) registrą."
author: rubencdelgado
manager: AnnBe
ms.date: 10/05/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 54117e070a99b62702cc677813a33b636a24af7e
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---
# <a name="create-and-associate-registers"></a><span data-ttu-id="e53fe-103"> Registrų kūrimas ir susiejimas</span><span class="sxs-lookup"><span data-stu-id="e53fe-103">Create and associate registers</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e53fe-104">Šioje procedūroje parodoma, kaip kurti elektroninio kasos aparato (POS) registrą.</span><span class="sxs-lookup"><span data-stu-id="e53fe-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="e53fe-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="e53fe-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="e53fe-106">Pasirinkite Mažmeninė prekyba ir prekyba > Kanalo sąranka > EKA sąranka > Registrai.</span><span class="sxs-lookup"><span data-stu-id="e53fe-106">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="e53fe-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="e53fe-107">Click New.</span></span>
3. <span data-ttu-id="e53fe-108">Lauke Registro numeris įveskite naujo registro ID.</span><span class="sxs-lookup"><span data-stu-id="e53fe-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="e53fe-109">Registro ID paprastai apima kodus, kurie padeda registrą susieti su parduotuve, kuriai jis priklauso, ir su vieta parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="e53fe-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="e53fe-110">Lauke Pavadinimas įrašykite aprašomąjį registro pavadinimą..</span><span class="sxs-lookup"><span data-stu-id="e53fe-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="e53fe-111">Lauke Parduotuvės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e53fe-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="e53fe-112">Lauke Aparatūros šablonas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e53fe-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="e53fe-113">Aparatūros šablonai naudojami norint nurodyti mažmeninės prekybos išorinius įrenginius, kurie bus prijungti prie registro, pvz., kasos stalčiaus ir kvitų spausdintuvo.</span><span class="sxs-lookup"><span data-stu-id="e53fe-113">Hardware profiles are used to specify the retail peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="e53fe-114">Lauke Vaizdo šablonas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e53fe-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="e53fe-115">Vaizdo šablonai naudojami norint nurodyti EKA fone ir prisijungimo puslapyje rodomus vaizdus bei EKA temas.</span><span class="sxs-lookup"><span data-stu-id="e53fe-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="e53fe-116">Lauke EFT EKA registro numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e53fe-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="e53fe-117">EFT EKA registro numeris naudojamas siekiant informuoti mokėjimo procesorių apie tai, kuris mokėjimo terminalas siunčia autorizavimo užklausas.</span><span class="sxs-lookup"><span data-stu-id="e53fe-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="e53fe-118">Ši reikšmė dažnai yra vadinama Terminalo ID arba TID.</span><span class="sxs-lookup"><span data-stu-id="e53fe-118">This value is often called the "Terminal ID" or “TID”.</span></span> <span data-ttu-id="e53fe-119">Paprastai TID galima rasti ant mokėjimo įrenginio lipduko.</span><span class="sxs-lookup"><span data-stu-id="e53fe-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="e53fe-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="e53fe-120">Click Save.</span></span>


