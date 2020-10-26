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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29d2cf6a496fed8d9932d5c6d49f4560d7eabbbb
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979117"
---
# <a name="service-objects-overview"></a><span data-ttu-id="ac34c-103">Aptarnavimo objektų apžvalga</span><span class="sxs-lookup"><span data-stu-id="ac34c-103">Service objects overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac34c-104">Aptarnavimo objektai yra kliento turtas ir produktai, dėl kurių galite teikti paslaugas.</span><span class="sxs-lookup"><span data-stu-id="ac34c-104">Service objects are a customer’s assets and products for which you can perform a service.</span></span> <span data-ttu-id="ac34c-105">Atsižvelgiant į paslaugų, kurias teikiate, tipą, objektai gali būti materialūs ir nematerialūs:</span><span class="sxs-lookup"><span data-stu-id="ac34c-105">Depending on the type of service you provide, objects can be tangible or intangible:</span></span>

-  <span data-ttu-id="ac34c-106">Materialūs objektai yra daiktai, tokie kaip mašina ar pastatas, kuriems galite atlikti fizinį faktinę aptarnavimo užduotį.</span><span class="sxs-lookup"><span data-stu-id="ac34c-106">Tangible objects are things, such as a machine or a building, on which you can perform a physical service task.</span></span>

    <span data-ttu-id="ac34c-107">Materialus aptarnavimo objektas taip pat gali būti atsargų prekė, kurią sukuriate formoje Išleisto produkto informacija.</span><span class="sxs-lookup"><span data-stu-id="ac34c-107">A tangible service object can also be an inventory item that you create in the Released product details form.</span></span> <span data-ttu-id="ac34c-108">Atsižvelgiant į atsargų dimensijų grupę, pridedamą prie prekės, jūs galite sukurti aptarnavimo objektą pagal išsamumo lygį, į kurį įeina prekės serijos numeris.</span><span class="sxs-lookup"><span data-stu-id="ac34c-108">Depending on the inventory dimension group that you attach to the item, you can create a service object to a level of detail that includes the item serial number.</span></span> <span data-ttu-id="ac34c-109">Tai pasitarnauja, kai jums reikia stebėti konkrečią prekę, kurią žymi aptarnavimo objektas.</span><span class="sxs-lookup"><span data-stu-id="ac34c-109">This is useful when you must keep track of the exact item that the service object represents.</span></span>

    <span data-ttu-id="ac34c-110">Materialus aptarnavimo objektas taip pat gali būti prekė, netiesiogiai susijusi su įmonės tiesioginės gamybos arba tiekimo grandine.</span><span class="sxs-lookup"><span data-stu-id="ac34c-110">A tangible service object can also be an item that is not directly related to a company's direct production or supply chain.</span></span> <span data-ttu-id="ac34c-111">Pvz., įrankių rinkinys, naudojamas remonto darbams atlikti ir esantis aptarnavimo užsakyme, gali būti aptarnavimo objektas, kuris neįtrauktas į atsargas.</span><span class="sxs-lookup"><span data-stu-id="ac34c-111">For example, a tool kit that is used for repairs in a service order can be a service object that is not included in inventory.</span></span> <span data-ttu-id="ac34c-112">Šiuo atveju negalite užregistruoti jo kaip atsargų prekės.</span><span class="sxs-lookup"><span data-stu-id="ac34c-112">In this case, you don’t register it as an inventory item.</span></span>

-  <span data-ttu-id="ac34c-113">Nematerialūs objektai yra nefiziniai objektai, tokie kaip sąskaitų rinkinys arba teisinis dokumentas, pagal kuriuos atliekama aptarnavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="ac34c-113">Intangible objects are nonphysical things, such as a set of accounts or a legal document, on which you can perform a service task.</span></span>

## <a name="example-of-an-intangible-service-object"></a><span data-ttu-id="ac34c-114">Nematerialaus aptarnavimo objekto pavyzdys</span><span class="sxs-lookup"><span data-stu-id="ac34c-114">Example of an intangible service object</span></span>

<span data-ttu-id="ac34c-115">Įmonė A tvarko finansinius įrašus keliose mažose įmonėse.</span><span class="sxs-lookup"><span data-stu-id="ac34c-115">Company A maintains the financial records for several small companies.</span></span> <span data-ttu-id="ac34c-116">Vienas įmonės A klientų yra vietinė futbolo komanda, kuriai įmonė A atlieka kassavaitinį buhalterijos tvarkymą ir kasmetinį klubo sąskaitų auditą.</span><span class="sxs-lookup"><span data-stu-id="ac34c-116">One of Company A's clients is the local football team, for which Company A does the weekly bookkeeping and annual audit of the club's accounts.</span></span> <span data-ttu-id="ac34c-117">Klubo sąskaitos yra nustatytos formoje Aptarnavimo objektai, o aptarnavimo sutartyje jos nurodytos kaip objektas.</span><span class="sxs-lookup"><span data-stu-id="ac34c-117">The club's accounts are set up in the Service objects form and specified as the object in the service agreement.</span></span> <span data-ttu-id="ac34c-118">Objektui priskiriamos dvi aptarnavimo sutarties eilutės.</span><span class="sxs-lookup"><span data-stu-id="ac34c-118">There are two service agreement lines for the object.</span></span> <span data-ttu-id="ac34c-119">1 eilutė yra kassavaitinis buhalterijos tvarkymas ir eilutei priskirtas savaitės intervalas, o 2 eilutė – kasmetinis auditas, kuriai priskirtas metų intervalas.</span><span class="sxs-lookup"><span data-stu-id="ac34c-119">Line 1 is weekly bookkeeping with a weekly interval assigned to the line, and line 2 is the annual audit with a yearly interval assigned to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac34c-120">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="ac34c-120">Related topics</span></span>

[<span data-ttu-id="ac34c-121">Aptarnavimo objektų kūrimas</span><span class="sxs-lookup"><span data-stu-id="ac34c-121">Create service objects</span></span>](create-service-objects.md)

