---
title: Abonemento darbo eigos peržiūra
description: Šioje temoje apžvelgiama abonemento darbo eiga.
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dbc87dc9c6327550020270468346800a7b80f4c3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817394"
---
# <a name="subscription-workflow-overview"></a><span data-ttu-id="45da4-103">Abonemento darbo eigos peržiūra</span><span class="sxs-lookup"><span data-stu-id="45da4-103">Subscription workflow overview</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="45da4-104">Esate apšvietimo įmonės, kuri siūlo apšvietimo bokšto aptarnavimo abonementus, administratorius.</span><span class="sxs-lookup"><span data-stu-id="45da4-104">You are the subscriptions administrator for a light company that offers subscriptions for lighting rig maintenance.</span></span> <span data-ttu-id="45da4-105">Klientas kreipiasi į jūsų įmonę norėdamas pirkti apšvietimo bokšto aptarnavimo abonementą metams.</span><span class="sxs-lookup"><span data-stu-id="45da4-105">A customer contacts your company to purchase a yearly subscription for lighting rig maintenance.</span></span>

## <a name="setting-up-subscriptions"></a><span data-ttu-id="45da4-106">Abonementų nustatymas</span><span class="sxs-lookup"><span data-stu-id="45da4-106">Setting up subscriptions</span></span>

<span data-ttu-id="45da4-107">Norėdami nustatyti abonementą, pirmiausia turite sukurti naują aptarnavimo sutarties abonemento grupę arba patikrinti, ar yra abonemento grupė.</span><span class="sxs-lookup"><span data-stu-id="45da4-107">To set up a subscription, you must first create a subscription group for the new service agreement or verify that a subscription group exists.</span></span> <span data-ttu-id="45da4-108">Jei abonemento grupė yra, turite nustatyti ją taip, kad klientui kas metus būtų išrašoma SF ir kiekvieną metų mėnesį būtų kaupiamos pardavimo įplaukos.</span><span class="sxs-lookup"><span data-stu-id="45da4-108">If a subscription group exists, you must set it up to invoice the customer yearly and to accrue sales revenue every month of the year.</span></span> <span data-ttu-id="45da4-109">Daugiau informacijos apie tai, kaip nustatyti abonementus, ieškokite [Abonementų grupių nustatymas](set-up-subscription-groups.md).</span><span class="sxs-lookup"><span data-stu-id="45da4-109">For more information about how to set up subscriptions, see [Set up subscription groups](set-up-subscription-groups.md).</span></span>

<span data-ttu-id="45da4-110">Sukūrę abonementų grupę galite sukurti patį abonementą.</span><span class="sxs-lookup"><span data-stu-id="45da4-110">After the subscription group is created, you can create the subscription.</span></span> <span data-ttu-id="45da4-111">Daugiau informacijos apie tai, kaip sukurti aptarnavimo abonementus, ieškokite [Aptarnavimo abonementų kūrimas naudojant abonementų grupę](create-service-subscriptions-from-subscription-group.md).</span><span class="sxs-lookup"><span data-stu-id="45da4-111">For more information about how to create service subscriptions, see [Create service subscriptions from a subscription group](create-service-subscriptions-from-subscription-group.md).</span></span>

## <a name="create-and-modify-subscription-transactions"></a><span data-ttu-id="45da4-112">Sukurkite ir modifikuokite abonementines operacijas</span><span class="sxs-lookup"><span data-stu-id="45da4-112">Create and modify subscription transactions</span></span>

<span data-ttu-id="45da4-113">Nustatę abonementą, galite sukurti abonementinio mokesčio operaciją pirmajam apskaitomam laikotarpiui, kuris yra vieneri metai.</span><span class="sxs-lookup"><span data-stu-id="45da4-113">After you set up the subscription, you create the subscription fee transaction for the first invoicing period, which is one year.</span></span> <span data-ttu-id="45da4-114">Operacijų tipas – **Įprastas**.</span><span class="sxs-lookup"><span data-stu-id="45da4-114">The transactions are of the **Regular** type.</span></span> <span data-ttu-id="45da4-115">Todėl galite sukurti tik tas abonementines operacijas, kurių pradžios ir pabaigos datos atitinka laikotarpius, anksčiau sukurtus formoje **Laikotarpių tipai**.</span><span class="sxs-lookup"><span data-stu-id="45da4-115">Therefore, you can only create subscription transactions where the from date and the to date correspond to periods that were previously created in the **Period types** form.</span></span> <span data-ttu-id="45da4-116">Daugiau informacijos apie mokesčių operacijas ieškokite [Abonementinio mokesčio operacijų kūrimas](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="45da4-116">For more information about fee transactions, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="45da4-117">Nustatę kliento abonementą prisimenate, kad susitarėte dėl 10 procentų nuolaidos visoms nustatytoms aptarnavimo pasiūlymų kainoms.</span><span class="sxs-lookup"><span data-stu-id="45da4-117">After you set up the subscription for your customer, you remember that they have negotiated a 10 percent discount on all list prices for service offerings.</span></span> <span data-ttu-id="45da4-118">Todėl turite sumažinti sukurto operacijos mokesčio kainą.</span><span class="sxs-lookup"><span data-stu-id="45da4-118">Therefore, you must reduce the price of the transaction fee that you created.</span></span>

<span data-ttu-id="45da4-119">Vėliau jūsų kliento kontaktinis asmuo paskambinęs praneša, kad vis dar nori sudaryti apšvietimo bokšto aptarnavimo sutartį, bet naują apšvietimo bokštą planuoja pristatyti vėliau tais pačiais metais.</span><span class="sxs-lookup"><span data-stu-id="45da4-119">Later in the day, your customer contact calls to say that, although they still want the service agreement for the lighting rig, they plan to introduce a new lighting rig later in the year.</span></span> <span data-ttu-id="45da4-120">Todėl jiems aptarnavimas reikalingas tik iki 2013 m. spalio mėn.</span><span class="sxs-lookup"><span data-stu-id="45da4-120">Therefore, they only need maintenance coverage until October 2013.</span></span> <span data-ttu-id="45da4-121">Norėdami sumažinti kliento abonemento mėnesių skaičių, sukuriate naują abonemento mokesčio operaciją, paremtą pagal tipą **Sumažinimo dienos**.</span><span class="sxs-lookup"><span data-stu-id="45da4-121">To reduce the number of months for the customer’s subscription, you create a new subscription fee transaction of the **Reduction days** type.</span></span> <span data-ttu-id="45da4-122">Daugiau informacijos apie tai, kaip sumažinti dienų, ieškokite [Abonementinio mokesčio dienų sumažinimas](reduce-the-days-on-subscription-fees.md).</span><span class="sxs-lookup"><span data-stu-id="45da4-122">For more information about how to reduce days, see [Reduce the days on subscription fees](reduce-the-days-on-subscription-fees.md).</span></span>

## <a name="invoice-and-accrue-subscription-transactions"></a><span data-ttu-id="45da4-123">Išrašykite SF ir kaupkite abonementines operacijas</span><span class="sxs-lookup"><span data-stu-id="45da4-123">Invoice and accrue subscription transactions</span></span>

<span data-ttu-id="45da4-124">Nustatėte abonementą ir esate pasiruošę už tai savo klientui išrašyti SF.</span><span class="sxs-lookup"><span data-stu-id="45da4-124">You have now finished setting up the subscription, and you are ready to invoice your customer for it.</span></span> <span data-ttu-id="45da4-125">Daugiau informacijos apie tai, kaip už abonementus išrašyti SF, ieškokite [Abonementinės operacijos, kurioms išrašyta SF](invoice-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="45da4-125">For more information about how to invoice subscriptions, see [Invoice subscription transactions](invoice-subscription-transactions.md).</span></span>

<span data-ttu-id="45da4-126">Po dviejų dienų jūsų klientas paskambina ir praneša, kad SF už abonementą reikia išrašyti JAV doleriais, o ne eurais.</span><span class="sxs-lookup"><span data-stu-id="45da4-126">Two days later, your customer calls to say that the subscription should be invoiced in U.S. dollars, not Euros.</span></span> <span data-ttu-id="45da4-127">Todėl sukuriate kredito pažymą ir naują abonementinę operaciją tinkama valiuta.</span><span class="sxs-lookup"><span data-stu-id="45da4-127">Therefore, you create a credit note, and you also create a new subscription transaction in the correct currency.</span></span> <span data-ttu-id="45da4-128">Daugiau informacijos apie tai, kaip kredituoti abonementines operacijas, ieškokite [Abonementinių operacijų kreditavimas](credit-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="45da4-128">For more information about how to credit subscription transactions, see [Credit subscription transactions](credit-subscription-transactions.md).</span></span>

<span data-ttu-id="45da4-129">Kiekvieno mėnesio pabaigoje vieno mėnesio kliento abonemento įplaukas galima sukaupti pelno ir nuostolių sąskaitoje bei NG sąskaitose.</span><span class="sxs-lookup"><span data-stu-id="45da4-129">At the end of each month, one month's revenue can be accrued from the customer's subscription to the profit and loss account and the WIP accounts.</span></span> <span data-ttu-id="45da4-130">Daugiau informacijos apie tai, kaip sukaupti abonementų įplaukas, ieškokite [Abonemento įplaukų kaupimas](accrue-subscription-revenue.md).</span><span class="sxs-lookup"><span data-stu-id="45da4-130">For more information about how to accrue revenue for subscriptions, see [Accrue subscription revenue](accrue-subscription-revenue.md).</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]