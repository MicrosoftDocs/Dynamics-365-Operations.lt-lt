---
title: Trikčių šalinimo gerinimo ir perkėlimas į papildomą sandėlio valdymą
description: Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti naujindami ir perkeldami siekiant pagerinti sandėlio valdymą.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 12dcadae2a65d71614a2eee9468ec93cac284a7b
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907892"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a><span data-ttu-id="2e8f8-103">Trikčių šalinimo gerinimo ir perkėlimas į papildomą sandėlio valdymą</span><span class="sxs-lookup"><span data-stu-id="2e8f8-103">Troubleshoot upgrade and migration to advanced warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e8f8-104">Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti naujindami ir perkeldami siekiant pagerinti sandėlio valdymą.</span><span class="sxs-lookup"><span data-stu-id="2e8f8-104">This topic describes how to fix common issues that you might encounter while you upgrade and migrate to advanced warehouse management.</span></span>

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a><span data-ttu-id="2e8f8-105">Gaunu tolesnį klaidos pranešimą: „java.security.cert.certPathValidatorException: Pasitikėjimo inkaras sertifikavimo keliui nerastas."</span><span class="sxs-lookup"><span data-stu-id="2e8f8-105">I receive the following error message: "java.security.cert.certPathValidatorException: Trust anchor for certification path is not found."</span></span>

### <a name="issue-description"></a><span data-ttu-id="2e8f8-106">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="2e8f8-106">Issue description</span></span>

<span data-ttu-id="2e8f8-107">Gavote šį klaidos pranešimą sandėlio valdymo mobiliųjų įrenginių programėlėje, kadangi „Android“ 8+ vietinėse aplinkose nepasitikima savaime prisijungusiais sertifikatais.</span><span class="sxs-lookup"><span data-stu-id="2e8f8-107">You receive this error message in the Warehouse Management mobile app, because self-signed certificates aren't trusted on Android 8+ in on-premises environments.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2e8f8-108">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="2e8f8-108">Issue resolution</span></span>

<span data-ttu-id="2e8f8-109">Naudokite išorės (viešąją) seritfikavimo įstaigą (CA).</span><span class="sxs-lookup"><span data-stu-id="2e8f8-109">Use an external (public) certifying authority (CA).</span></span> <span data-ttu-id="2e8f8-110">Šios trikties pašalinimas yra prieinamas sandėlio programose 1.9.0.0 versijoje.</span><span class="sxs-lookup"><span data-stu-id="2e8f8-110">A fix for this issue is available in version 1.9.0.0 of the warehouse app.</span></span> <span data-ttu-id="2e8f8-111">Daugiau informacijos apie šią problemą ir kaip ją išspręsti rasite [Sandėlio valdymo mobiliųjų įrenginių programėlės ryšio trikčių diagnostika](troubleshoot-warehouse-app-connection.md).</span><span class="sxs-lookup"><span data-stu-id="2e8f8-111">For more information about this issue and how to fix it, see [Troubleshoot Warehouse Management mobile app connection issues](troubleshoot-warehouse-app-connection.md).</span></span>

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a><span data-ttu-id="2e8f8-112">Kas yra patvirtintas procesas perkėlimui iš pagrindinio sandėliavimo į pagerintą sandėliavimą?</span><span class="sxs-lookup"><span data-stu-id="2e8f8-112">What is the approved process for moving from basic warehousing to advanced warehousing?</span></span>

### <a name="issue-description"></a><span data-ttu-id="2e8f8-113">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="2e8f8-113">Issue description</span></span>

<span data-ttu-id="2e8f8-114">Dabar vykdote sandėliavimo/inventoriaus valdymą ir naudojate pagrindines sandėlio funkcijas ir norite perkelti išplėstinį sandėliavimą tam, kad pasinaudotumėte mobiliuoju įrenginiu, bangomis ir darbu geriau.</span><span class="sxs-lookup"><span data-stu-id="2e8f8-114">You're currently running under stock/inventory management and using basic stock functionality, and you want to move to advanced warehousing to take advantage of mobile devices, waves, and work.</span></span> <span data-ttu-id="2e8f8-115">Nepaisant to, patiriate trikčių bandydami padaryti šį perkėlimą.</span><span class="sxs-lookup"><span data-stu-id="2e8f8-115">However, you're experiencing issues when you try to make this move.</span></span> <span data-ttu-id="2e8f8-116">Pavyzdžiui, negali pakeisti savo produktų taip, kad jie naudotų talpinimo matmenis (vietą, sandėlį ir vietą), nes produktai turi perlaidas jų atžvilgiu.</span><span class="sxs-lookup"><span data-stu-id="2e8f8-116">For example, you can't change your products so that they use storage dimensions (site, warehouse, and location), because the products have transactions against them.</span></span> <span data-ttu-id="2e8f8-117">Dėl to, privalote išmokti patvirtintą procesą perkėlimui iš pagrindinio sandėliavimo į pagerintą sandėliavimą.</span><span class="sxs-lookup"><span data-stu-id="2e8f8-117">Therefore, you must learn the approved process for moving from basic warehousing to advanced warehousing.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2e8f8-118">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="2e8f8-118">Issue resolution</span></span>

<span data-ttu-id="2e8f8-119">Dėl daugiau informacijos apie procesą perkėlimui iš pagrindinio sandėliavimo į pagerintą sandėliavimą, žr. tolesnius tinklaraščio įrašus ir dokumentus:</span><span class="sxs-lookup"><span data-stu-id="2e8f8-119">For more information about the process for moving from basic warehousing to advanced warehousing, see the following blog posts and documentation:</span></span>

- [<span data-ttu-id="2e8f8-120">Įjungti sandėlio valdymo procesą esantiems elementams ir sandėliams</span><span class="sxs-lookup"><span data-stu-id="2e8f8-120">Enable warehouse management process for existing items and warehouses</span></span>](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [<span data-ttu-id="2e8f8-121">„Microsoft Dynamics AX“ perkėlimas WMS į naują R3 sandėlį ir gabenimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="2e8f8-121">Migration of Microsoft Dynamics AX WMS to new R3 warehouse and transportation functionality</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [<span data-ttu-id="2e8f8-122">WMSI/WMS2 elemento perkėlimas</span><span class="sxs-lookup"><span data-stu-id="2e8f8-122">WMSI/WMS2 item migration</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [<span data-ttu-id="2e8f8-123">Sandėlio valdymo pagerinimas iš „Microsoft Dynamics“ AX 2012 iki „Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="2e8f8-123">Upgrade warehouse management from Microsoft Dynamics AX 2012 to Supply Chain Management</span></span>](./upgrade-migration-warehouse-management-processes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]