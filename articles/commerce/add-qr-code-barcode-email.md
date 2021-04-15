---
title: QR kodo arba brūkšninio kodo pridėjimas prie operacijų ir kvitų el. laiškų
description: Šioje temoje paaiškinama, kaip įterpti QR kodus ir brūkšninius kodus, užsakymų ID pateikiančius „Microsoft Dynamics 365 Commerce“ operacijų ir gavimo el. laiškuose.
author: bicyclingfool
manager: annbe
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 3cc4fcb1237f8409a89b3d4818c132c60c57b5a0
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555427"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a><span data-ttu-id="3611b-103">QR kodo arba brūkšninio kodo pridėjimas prie operacijų ir kvitų el. laiškų</span><span class="sxs-lookup"><span data-stu-id="3611b-103">Add a QR code or bar code to transactional and receipt emails</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="3611b-104">Šioje temoje paaiškinama, kaip įterpti QR kodus ir brūkšninius kodus, užsakymų ID pateikiančius „Microsoft Dynamics 365 Commerce“ operacijų ir gavimo el. laiškuose.</span><span class="sxs-lookup"><span data-stu-id="3611b-104">This topic explains how to insert QR codes and bar codes that represent order IDs into transactional and receipt emails in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3611b-105">QR kodus ir brūkšninius kodus galima lengvai įtraukti į operacijų el. laiškus, kad būtų lengviau paspartinti užsakymų peržvalgos procesą mažmeninės prekybos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="3611b-105">You can easily include QR codes and bar codes in transactional emails to help speed up the order lookup process in a retail environment.</span></span> <span data-ttu-id="3611b-106">Norėdami QR kodus ir brūkšninius kodus įterpti į el. laiškus, naudokite HTML **\<img\>** žymę, kuri reikalauja QR kodo arba brūkšninio kodo vaizdo iš generavimo ir atvaizdavimo paslaugos.</span><span class="sxs-lookup"><span data-stu-id="3611b-106">To insert QR codes and bar codes into emails, you use an HTML **\<img\>** tag that requests a QR code or bar code image from a generation and rendering service.</span></span> <span data-ttu-id="3611b-107">„Microsoft“ šios paslaugos neteikia.</span><span class="sxs-lookup"><span data-stu-id="3611b-107">Microsoft doesn't provide this service.</span></span> <span data-ttu-id="3611b-108">Tačiau yra daug nemokamų ar nebrangių paslaugų, kurios gali aprūpinti QR kodus arba brūkšninius kodus, kurie dinamiškai generuojami pagal vertę, kuri perduodama užklausos eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3611b-108">However, there are many free or inexpensive services that can serve QR codes or bar codes that are dynamically generated based on a value that is passed in a query string.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a><span data-ttu-id="3611b-109">QR kodo arba brūkšninio kodo pridėjimas prie operacijų el. laiško</span><span class="sxs-lookup"><span data-stu-id="3611b-109">Add a QR code or bar code to a transactional email</span></span>

<span data-ttu-id="3611b-110">Norėdami įterpti QR kodą arba brūkšninį kodą į operacijų el. laišką, kuris siunčiamas kaip el. komercijos pirkimo dalis, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3611b-110">To insert a QR code or bar code into a transactional email that is sent as part of an e-commerce purchase, follow these steps.</span></span>

1. <span data-ttu-id="3611b-111">Atidarykite operacijų el. laiško šablono šaltinio HTML ir pridėkite HTML žymę, kuri nurodo jūsų **\<img\>** QR kodo ar brūkšninio kodo tarnybą.</span><span class="sxs-lookup"><span data-stu-id="3611b-111">Open the source HTML for the transactional email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="3611b-112">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="3611b-112">Here is an example.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    <span data-ttu-id="3611b-113">Toliau pateiktas ankstesnio pavyzdžio paaiškinimas:</span><span class="sxs-lookup"><span data-stu-id="3611b-113">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="3611b-114">**JŪSŲ \_QR \_KODO \_\_BRŪKŠNINIO KODO TARNYBA rodo jūsų \_** QR kodo arba brūkšninio kodo paslaugos domeną.</span><span class="sxs-lookup"><span data-stu-id="3611b-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="3611b-115">**duomenys** nurodo parametrą, kurį QR kodas arba brūkšninių kodų tarnyba naudoja turiniui, kuris turėtų būti atvaizduotas kaip QR kodas arba brūkšninis kodas, gauti.</span><span class="sxs-lookup"><span data-stu-id="3611b-115">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="3611b-116">Vertę **%salesid%** reikia priskirti šiam parametrui.</span><span class="sxs-lookup"><span data-stu-id="3611b-116">The value **%salesid%** must be assigned to this parameter.</span></span> <span data-ttu-id="3611b-117">Šiame pavyzdyje atkreipkite dėmesį, kad vertė taip pat naudojama kaip alternatyvus vaizdo tekstas.</span><span class="sxs-lookup"><span data-stu-id="3611b-117">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="3611b-118">**param1** ir **param2** reiškia papildomus pasirenkamus parametrus.</span><span class="sxs-lookup"><span data-stu-id="3611b-118">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="3611b-119">Eikite į **Mažmeninė prekyba ir komercija \> Būstinės sąranka \> Parametrai \> Organizacijos el. laiškų šablonai** ir įkelkite atnaujintą HTML į atitinkamą operacijų el. laiško šabloną.</span><span class="sxs-lookup"><span data-stu-id="3611b-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the appropriate transactional email template.</span></span>

> [!NOTE]
> <span data-ttu-id="3611b-120">Parametrai gali skirtis priklausomai nuo QR kodo ir brūkšninio kodo paslaugų teikėjo.</span><span class="sxs-lookup"><span data-stu-id="3611b-120">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="3611b-121">Todėl kreipkitės į savo paslaugų teikėją ir patvirtinkite parametrus, kuriems turite priskirti vertes.</span><span class="sxs-lookup"><span data-stu-id="3611b-121">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a><span data-ttu-id="3611b-122">QR kodo arba brūkšninio kodo pridėjimas prie gavimo el. laiško</span><span class="sxs-lookup"><span data-stu-id="3611b-122">Add a QR code or bar code to a receipt email</span></span> 

<span data-ttu-id="3611b-123">Norėdami įterpti QR kodą arba brūkšninią kodą į gavimo el. laišką, kurį galim siųsti atlikus pirkimą elektroniniu kasos aparatu (EKA), atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3611b-123">To insert a QR code or bar code into a receipt email that can be sent after a purchase is made at the point of sale (POS), follow these steps.</span></span>

1. <span data-ttu-id="3611b-124">Atidarykite gavimo el. laiško šablono šaltinio HTML ir pridėkite HTML **\<img\>** žymę, kuri nurodo jūsų QR kodo ar brūkšninio kodo tarnybą.</span><span class="sxs-lookup"><span data-stu-id="3611b-124">Open the source HTML for the receipt email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="3611b-125">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="3611b-125">Here is an example below.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    <span data-ttu-id="3611b-126">Toliau pateiktas ankstesnio pavyzdžio paaiškinimas:</span><span class="sxs-lookup"><span data-stu-id="3611b-126">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="3611b-127">**JŪSŲ \_QR \_KODO \_\_BRŪKŠNINIO KODO TARNYBA rodo jūsų \_** QR kodo arba brūkšninio kodo paslaugos domeną.</span><span class="sxs-lookup"><span data-stu-id="3611b-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="3611b-128">**duomenys** nurodo parametrą, kurį QR kodas arba brūkšninių kodų tarnyba naudoja turiniui, kuris turėtų būti atvaizduotas kaip QR kodas arba brūkšninis kodas, gauti.</span><span class="sxs-lookup"><span data-stu-id="3611b-128">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="3611b-129">Vertę **%receiptid%** reikia priskirti šiam parametrui.</span><span class="sxs-lookup"><span data-stu-id="3611b-129">The value **%receiptid%** must be assigned to this parameter.</span></span> <span data-ttu-id="3611b-130">Šiame pavyzdyje atkreipkite dėmesį, kad vertė taip pat naudojama kaip alternatyvus vaizdo tekstas.</span><span class="sxs-lookup"><span data-stu-id="3611b-130">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="3611b-131">**param1** ir **param2** reiškia papildomus pasirenkamus parametrus.</span><span class="sxs-lookup"><span data-stu-id="3611b-131">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="3611b-132">Eikite į **Mažmeninė prekyba ir komercija \> Būstinės sąranka \> Parametrai \> Organizacijos el. laiškų šablonai** ir įkelkite atnaujintą HTML į el. pašto šabloną, kurio el. pašto ID yra **emailrecpt**.</span><span class="sxs-lookup"><span data-stu-id="3611b-132">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the email template that has the email ID **emailrecpt**.</span></span>

> [!NOTE]
> <span data-ttu-id="3611b-133">Parametrai gali skirtis priklausomai nuo QR kodo ir brūkšninio kodo paslaugų teikėjo.</span><span class="sxs-lookup"><span data-stu-id="3611b-133">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="3611b-134">Todėl kreipkitės į savo paslaugų teikėją ir patvirtinkite parametrus, kuriems turite priskirti vertes.</span><span class="sxs-lookup"><span data-stu-id="3611b-134">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3611b-135">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3611b-135">Additional resources</span></span>

[<span data-ttu-id="3611b-136">Kvitų iš „Modern POS“ (MPOS) siuntimas el. paštu</span><span class="sxs-lookup"><span data-stu-id="3611b-136">Send email receipts from Modern POS (MPOS)</span></span>](email-receipts.md)

[<span data-ttu-id="3611b-137">El. laiškų šablonų, skirtų operacijų įvykiams, kūrimas</span><span class="sxs-lookup"><span data-stu-id="3611b-137">Create email templates for transactional events</span></span>](email-templates-transactions.md)