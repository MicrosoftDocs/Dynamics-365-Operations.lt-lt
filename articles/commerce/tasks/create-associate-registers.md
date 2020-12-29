---
title: " Registrų kūrimas ir susiejimas"
description: Šioje procedūroje parodoma, kaip kurti elektroninio kasos aparato (POS) registrą.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 001bdd61f9266798dadae2ac7c96a4f4c19dbb94
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414406"
---
# <a name="create-and-associate-registers"></a><span data-ttu-id="76c7d-103"> Registrų kūrimas ir susiejimas</span><span class="sxs-lookup"><span data-stu-id="76c7d-103">Create and associate registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76c7d-104">Šioje procedūroje parodoma, kaip kurti elektroninio kasos aparato (POS) registrą.</span><span class="sxs-lookup"><span data-stu-id="76c7d-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="76c7d-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="76c7d-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="76c7d-106">Eikite į Mažmeninė prekyba ir prekyba > Kanalo sąranka > EKA sąranka > Registrai.</span><span class="sxs-lookup"><span data-stu-id="76c7d-106">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="76c7d-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="76c7d-107">Click New.</span></span>
3. <span data-ttu-id="76c7d-108">Lauke Registro numeris įveskite naujo registro ID.</span><span class="sxs-lookup"><span data-stu-id="76c7d-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="76c7d-109">Registro ID paprastai apima kodus, kurie padeda registrą susieti su parduotuve, kuriai jis priklauso, ir su vieta parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="76c7d-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="76c7d-110">Lauke Pavadinimas įrašykite aprašomąjį registro pavadinimą..</span><span class="sxs-lookup"><span data-stu-id="76c7d-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="76c7d-111">Lauke Parduotuvės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="76c7d-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="76c7d-112">Lauke Aparatūros šablonas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="76c7d-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="76c7d-113">Aparatūros šablonai naudojami norint nurodyti išorinius įrenginius, kurie bus prijungti prie registro, pvz., kasos stalčiaus ir kvitų spausdintuvo.</span><span class="sxs-lookup"><span data-stu-id="76c7d-113">Hardware profiles are used to specify the peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="76c7d-114">Lauke Vaizdo šablonas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="76c7d-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="76c7d-115">Vaizdo šablonai naudojami norint nurodyti EKA fone ir prisijungimo puslapyje rodomus vaizdus bei EKA temas.</span><span class="sxs-lookup"><span data-stu-id="76c7d-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="76c7d-116">Lauke EFT EKA registro numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="76c7d-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="76c7d-117">EFT EKA registro numeris naudojamas siekiant informuoti mokėjimo procesorių apie tai, kuris mokėjimo terminalas siunčia autorizavimo užklausas.</span><span class="sxs-lookup"><span data-stu-id="76c7d-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="76c7d-118">Ši reikšmė dažnai yra vadinama Terminalo ID arba TID.</span><span class="sxs-lookup"><span data-stu-id="76c7d-118">This value is often called the "Terminal ID" or "TID".</span></span> <span data-ttu-id="76c7d-119">Paprastai TID galima rasti ant mokėjimo įrenginio lipduko.</span><span class="sxs-lookup"><span data-stu-id="76c7d-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="76c7d-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="76c7d-120">Click Save.</span></span>

