---
title: EKA pristatymo būdo keitimas
description: Šioje temoje aprašoma, kaip sukonfigūruoti ir naudoti pristatymo būdo keitimą, esantį EKA.
author: hhainesms
manager: annbe
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 6bfe27a7b4a768da00c67e307a0bd7e57b333d11
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965432"
---
# <a name="change-mode-of-delivery-in-pos"></a><span data-ttu-id="1f80c-103">EKA pristatymo būdo keitimas</span><span class="sxs-lookup"><span data-stu-id="1f80c-103">Change mode of delivery in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1f80c-104">Šioje temoje aprašoma, kaip nustatyti ir naudoti funkciją „pristatymo būdo keitimas“ elektroninio kasos aparato (EKA) aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="1f80c-104">This topic describes how to set up and use the "change mode of delivery" functionality in your point of sale (POS) environment.</span></span> 

<span data-ttu-id="1f80c-105">„Dynamics 365 Commerce“ 10.0.10 ir naujesnėse versijose prieinama operacija **„Pristatymo būdo keitimas“** (647), kuri leidžia pridėti EKA ekrano maketus.</span><span class="sxs-lookup"><span data-stu-id="1f80c-105">In Dynamics 365 Commerce versions 10.0.10 and later, the **Change mode of delivery** operation (647) is available to add to your POS screen layouts.</span></span>

<span data-ttu-id="1f80c-106">Pristatymo būdo keitimo funkcija suteikia galimybę pakeisti vienos ar kelių sukonfigūruotų siuntų pardavimo eilučių pristatymo būdus EKA operacijose.</span><span class="sxs-lookup"><span data-stu-id="1f80c-106">The change mode of delivery feature provides you with the option to change the mode of delivery for one or more shipment-configured sales lines on the POS transaction.</span></span> <span data-ttu-id="1f80c-107">Ankstesnėse „Commerce“ versijose reikėjo pereiti per visus **Siųsti viską** ar **Išsiųsti pasirinktus** konfigūracijos srautus, jei norėjote pakeisti pristatymo būdą esamoje eilutėje, kuri buvo sukonfigūruota siuntai.</span><span class="sxs-lookup"><span data-stu-id="1f80c-107">In previous versions of Commerce, you had to go through the full **Ship all** or **Ship selected** configuration flows if you wanted to change the mode of delivery on an existing line that was configured for shipment.</span></span> <span data-ttu-id="1f80c-108">Šis procesas buvo ilgas, todėl galėjo įvykti atsitiktiniai pristatymo kilmės arba linijos pristatymo datų pakeitimai.</span><span class="sxs-lookup"><span data-stu-id="1f80c-108">This process was time consuming and could result in accidental changes to the delivery origin or delivery dates for the line.</span></span> <span data-ttu-id="1f80c-109">Nauja funkcija pateikia alternatyvų metodą, kaip efektyviai atnaujinti pristatymo būdą šiose pardavimo linijose.</span><span class="sxs-lookup"><span data-stu-id="1f80c-109">The new functionality provides an alternative method for efficiently updating the mode of delivery on these sales lines.</span></span>

<span data-ttu-id="1f80c-110">Daugiau informacijos apie tai, kaip į mygtuką, esantį jūsų EKA mygtukyne, įtraukti operaciją, rasite skyriuje [„Elektroninio kasos aparato ekrano maketai“](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span><span class="sxs-lookup"><span data-stu-id="1f80c-110">For more information about how to add an operation to a button on your POS button grid, see [Screen layouts for the point of sale](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span></span>

<span data-ttu-id="1f80c-111">Kai ši funkcija sukonfigūruota EKA, pasirinkus **„Pristatymo būdo keitimas“**, pateikiamas sąrašo puslapis, kuriame galėsite pasirinkti operacijos eilutes, kurių pristatymo būdą norite pakeisti.</span><span class="sxs-lookup"><span data-stu-id="1f80c-111">After this feature is configured in POS, when you select **Change mode of delivery**, you will be presented with a list page that allows you to choose the lines of the transaction that you want to change the mode of delivery for.</span></span> <span data-ttu-id="1f80c-112">Galite pasirinkti kelias eilutes, visas eilutes arba išeiti neatlikus jokių pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="1f80c-112">You can choose some or all of the lines, or exit without making any changes.</span></span> <span data-ttu-id="1f80c-113">Galite pakeisti tik tas pardavimų eilutes, kurios anksčiau buvo sukonfigūruotos siuntimui.</span><span class="sxs-lookup"><span data-stu-id="1f80c-113">The sales lines that were previously configured for shipment are the only lines in the list that you can change.</span></span> <span data-ttu-id="1f80c-114">Jei norite pakeisti eilutę, skirtą paėmimui arba pristatymui į namus atlikti, naudokite operaciją **Siųsti viską** arba **Išsiųsti pasirinktus**.</span><span class="sxs-lookup"><span data-stu-id="1f80c-114">If you want to change a line designated for pickup or carryout to ship, you must use the **Ship all** or **Ship selected** operations.</span></span> <span data-ttu-id="1f80c-115">Ir atvirkščiai, jei norite pakeisti eilutę, kuri buvo pažymėta kaip siuntos paėmimas arba išsineštinis, naudokite operacijas **Paimti viską**, **Paimti pasirinktus**, **Išsinešti visus** arba **Išsinešti pasirinktus**.</span><span class="sxs-lookup"><span data-stu-id="1f80c-115">Conversely, if you want to change a line designated as a shipment to a pickup or carryout, you must use the  **Pickup all**, **Pickup selected**, **Carryout all**, or **Carryout selected** operations.</span></span>

<span data-ttu-id="1f80c-116">Pasirinkę eilutes, kurias norite pakeisti, spustelėkite **Pristatymo būdo keitimas**, kad būtų galima pasirinkti pristatymo būdo parinktis.</span><span class="sxs-lookup"><span data-stu-id="1f80c-116">After you select the lines that you want to change, click **Change mode of delivery** to be prompted to select the delivery mode options.</span></span> <span data-ttu-id="1f80c-117">Jei pasirinkote keletą eilučių, kurias norite pakeisti, EKA bus rodomi tik tie pristatymo būdai, kurie buvo sukonfigūruoti kaip leistini visiems pasirinktiems produktams.</span><span class="sxs-lookup"><span data-stu-id="1f80c-117">If you selected multiple lines to change, POS will only display modes of delivery that have been configured as allowable for all of the selected products.</span></span> <span data-ttu-id="1f80c-118">Pristatymo būdus galima sukonfigūruoti taip, kad jie palaikytų konkrečius produktus ir pristatymo adresus.</span><span class="sxs-lookup"><span data-stu-id="1f80c-118">Modes of delivery can be configured to support specific products and delivery addresses.</span></span> <span data-ttu-id="1f80c-119">Jei yra pristatymo būdas, kuris yra priimtinas vienam produktui ir adresų deriniui, bet nepriimtinas kitam pasirinktam produktui ir adreso deriniui, pristatymo būdas negalimas.</span><span class="sxs-lookup"><span data-stu-id="1f80c-119">If there is a mode of delivery that is acceptable for one product and address combination but is not acceptable for another selected product and address combination, the mode of delivery is not available.</span></span> <span data-ttu-id="1f80c-120">Jei norite pasirinkti pristatymo būdą vienam produktui, kurio nepalaiko kitas produktas, gali tekti pasirinkti eilutes po vieną ir pakeisti kiekvienos eilutės pristatymo būdą atskirai.</span><span class="sxs-lookup"><span data-stu-id="1f80c-120">You may need to select lines one by one and change the mode of delivery for each line separately if you want to select a mode of delivery for one product that is not supported by another product.</span></span>  

<span data-ttu-id="1f80c-121">Pasirinkus naują pristatymo būdą, rodomas operacijos puslapis.</span><span class="sxs-lookup"><span data-stu-id="1f80c-121">After you select the new mode of delivery, the transaction page is displayed.</span></span> <span data-ttu-id="1f80c-122">Norėdami peržiūrėti naujus pristatymo būdo pasirinkimus, operacijų sąraše pasirinkite skirtuką **Pristatymas**.</span><span class="sxs-lookup"><span data-stu-id="1f80c-122">To review your new delivery mode selections, select the **Delivery** tab on the transaction list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1f80c-123">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1f80c-123">Additional resources</span></span>

[<span data-ttu-id="1f80c-124">Skambučių centro užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="1f80c-124">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="1f80c-125">Tinkinti perlaidų el. paštus pagal pristatymo būdą</span><span class="sxs-lookup"><span data-stu-id="1f80c-125">Customize transactional emails by mode of delivery</span></span>](customize-email-delivery-mode.md)
