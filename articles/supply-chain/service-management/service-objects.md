---
title: Aptarnavimo objektų apžvalga
description: Aptarnavimo objektai yra kliento turtas ir produktai, dėl kurių galite teikti paslaugas.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dae74ebb59d73e1197426757ec9c050b1905852e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211795"
---
# <a name="service-objects-overview"></a><span data-ttu-id="b55d9-103">Aptarnavimo objektų apžvalga</span><span class="sxs-lookup"><span data-stu-id="b55d9-103">Service objects overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b55d9-104">Aptarnavimo objektai yra kliento turtas ir produktai, dėl kurių galite teikti paslaugas.</span><span class="sxs-lookup"><span data-stu-id="b55d9-104">Service objects are a customer’s assets and products for which you can perform a service.</span></span> <span data-ttu-id="b55d9-105">Atsižvelgiant į paslaugų, kurias teikiate, tipą, objektai gali būti materialūs ir nematerialūs:</span><span class="sxs-lookup"><span data-stu-id="b55d9-105">Depending on the type of service you provide, objects can be tangible or intangible:</span></span>

-  <span data-ttu-id="b55d9-106">Materialūs objektai yra daiktai, tokie kaip mašina ar pastatas, kuriems galite atlikti fizinį faktinę aptarnavimo užduotį.</span><span class="sxs-lookup"><span data-stu-id="b55d9-106">Tangible objects are things, such as a machine or a building, on which you can perform a physical service task.</span></span>

    <span data-ttu-id="b55d9-107">Materialus aptarnavimo objektas taip pat gali būti atsargų prekė, kurią sukuriate formoje Išleisto produkto informacija.</span><span class="sxs-lookup"><span data-stu-id="b55d9-107">A tangible service object can also be an inventory item that you create in the Released product details form.</span></span> <span data-ttu-id="b55d9-108">Atsižvelgiant į atsargų dimensijų grupę, pridedamą prie prekės, jūs galite sukurti aptarnavimo objektą pagal išsamumo lygį, į kurį įeina prekės serijos numeris.</span><span class="sxs-lookup"><span data-stu-id="b55d9-108">Depending on the inventory dimension group that you attach to the item, you can create a service object to a level of detail that includes the item serial number.</span></span> <span data-ttu-id="b55d9-109">Tai pasitarnauja, kai jums reikia stebėti konkrečią prekę, kurią žymi aptarnavimo objektas.</span><span class="sxs-lookup"><span data-stu-id="b55d9-109">This is useful when you must keep track of the exact item that the service object represents.</span></span>

    <span data-ttu-id="b55d9-110">Materialus aptarnavimo objektas taip pat gali būti prekė, netiesiogiai susijusi su įmonės tiesioginės gamybos arba tiekimo grandine.</span><span class="sxs-lookup"><span data-stu-id="b55d9-110">A tangible service object can also be an item that is not directly related to a company's direct production or supply chain.</span></span> <span data-ttu-id="b55d9-111">Pvz., įrankių rinkinys, naudojamas remonto darbams atlikti ir esantis aptarnavimo užsakyme, gali būti aptarnavimo objektas, kuris neįtrauktas į atsargas.</span><span class="sxs-lookup"><span data-stu-id="b55d9-111">For example, a tool kit that is used for repairs in a service order can be a service object that is not included in inventory.</span></span> <span data-ttu-id="b55d9-112">Šiuo atveju negalite užregistruoti jo kaip atsargų prekės.</span><span class="sxs-lookup"><span data-stu-id="b55d9-112">In this case, you don’t register it as an inventory item.</span></span>

-  <span data-ttu-id="b55d9-113">Nematerialūs objektai yra nefiziniai objektai, tokie kaip sąskaitų rinkinys arba teisinis dokumentas, pagal kuriuos atliekama aptarnavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="b55d9-113">Intangible objects are nonphysical things, such as a set of accounts or a legal document, on which you can perform a service task.</span></span>

## <a name="example-of-an-intangible-service-object"></a><span data-ttu-id="b55d9-114">Nematerialaus aptarnavimo objekto pavyzdys</span><span class="sxs-lookup"><span data-stu-id="b55d9-114">Example of an intangible service object</span></span>

<span data-ttu-id="b55d9-115">Įmonė A tvarko finansinius įrašus keliose mažose įmonėse.</span><span class="sxs-lookup"><span data-stu-id="b55d9-115">Company A maintains the financial records for several small companies.</span></span> <span data-ttu-id="b55d9-116">Vienas įmonės A klientų yra vietinė futbolo komanda, kuriai įmonė A atlieka kassavaitinį buhalterijos tvarkymą ir kasmetinį klubo sąskaitų auditą.</span><span class="sxs-lookup"><span data-stu-id="b55d9-116">One of Company A's clients is the local football team, for which Company A does the weekly bookkeeping and annual audit of the club's accounts.</span></span> <span data-ttu-id="b55d9-117">Klubo sąskaitos yra nustatytos formoje Aptarnavimo objektai, o aptarnavimo sutartyje jos nurodytos kaip objektas.</span><span class="sxs-lookup"><span data-stu-id="b55d9-117">The club's accounts are set up in the Service objects form and specified as the object in the service agreement.</span></span> <span data-ttu-id="b55d9-118">Objektui priskiriamos dvi aptarnavimo sutarties eilutės.</span><span class="sxs-lookup"><span data-stu-id="b55d9-118">There are two service agreement lines for the object.</span></span> <span data-ttu-id="b55d9-119">1 eilutė yra kassavaitinis buhalterijos tvarkymas ir eilutei priskirtas savaitės intervalas, o 2 eilutė – kasmetinis auditas, kuriai priskirtas metų intervalas.</span><span class="sxs-lookup"><span data-stu-id="b55d9-119">Line 1 is weekly bookkeeping with a weekly interval assigned to the line, and line 2 is the annual audit with a yearly interval assigned to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b55d9-120">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="b55d9-120">Related topics</span></span>

[<span data-ttu-id="b55d9-121">Aptarnavimo objektų kūrimas</span><span class="sxs-lookup"><span data-stu-id="b55d9-121">Create service objects</span></span>](create-service-objects.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]