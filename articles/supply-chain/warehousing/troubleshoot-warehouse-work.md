---
title: Trikčių šalinimo sandėlio darbas
description: Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su sandėlio darbu „Microsoft Dynamics 365 Supply Chain Management“.
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
ms.openlocfilehash: 08cc074fe851b952ebfc942ae3d1cb05240d3b91
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837446"
---
# <a name="troubleshoot-warehouse-work"></a><span data-ttu-id="395d2-103">Trikčių šalinimo sandėlio darbas</span><span class="sxs-lookup"><span data-stu-id="395d2-103">Troubleshoot warehouse work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="395d2-104">Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su sandėlio darbu „Microsoft Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="395d2-104">This topic describes how to fix common issues that you might encounter while you work with warehouse work in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a><span data-ttu-id="395d2-105">Negaliu perkelti licencijos lentelių, kurių serijinio numerio elementai, kai tuščia problema ir tuščias gavimas yra leidžiami sekimo dimensijos grupėje.</span><span class="sxs-lookup"><span data-stu-id="395d2-105">I can't move license plates that have serial number items when blank issue and blank receipt are allowed on the tracking dimension group.</span></span>

### <a name="issue-description"></a><span data-ttu-id="395d2-106">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="395d2-106">Issue description</span></span>

<span data-ttu-id="395d2-107">Negalite perkelti licencijos lentelės naudodami **Perkėlimo** meniu elementą, jei serijinis numeris turi nustatymus *Tuščia problema leidžiama* ir *Tuščias kvitas leidžiamas* sekimo dimensijos grupėje ir jei esama kelių licencijos lentelių toje pačioje vietoje, kurių keletas turi serijinius numerius ir keletas neturi.</span><span class="sxs-lookup"><span data-stu-id="395d2-107">You can't move a license plate by using a **Movement** menu item if the serial number has settings of *Blank issue allowed* and *Blank receipt allowed* on the tracking dimension group, and if there are multiple license plates in the same location, some of which have serial numbers and some of which don't have them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="395d2-108">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="395d2-108">Issue resolution</span></span>

<span data-ttu-id="395d2-109">Ši triktis bus pataisyta pakeitimais, kurie yra patalpinti [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span><span class="sxs-lookup"><span data-stu-id="395d2-109">This issue will be fixed by changes that are deployed in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span></span> <span data-ttu-id="395d2-110">Šie pakeitimai padarys **Serijinio numerio** laukelį pasirenkamą, kai tuščias kvitas ir tuščia triktis yra leidžiami.</span><span class="sxs-lookup"><span data-stu-id="395d2-110">Those changes will make the **Serial number** field optional when blank receipt and blank issue are allowed.</span></span>

## <a name="i-receive-the-following-error-message-in-the-warehouse-management-mobile-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a><span data-ttu-id="395d2-111">Gaunu tolesnį klaidos pranešimą sandėlio valdymo mobiliųjų įrenginių programėlėje, kai apdoroju perkėlimus: „Inventoriaus savininkas %1 neleidžiamas šiame procese.”</span><span class="sxs-lookup"><span data-stu-id="395d2-111">I receive the following error message in the Warehouse Management mobile app when I process movements: "The inventory owner %1 is not allowed in this process."</span></span>

### <a name="issue-description"></a><span data-ttu-id="395d2-112">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="395d2-112">Issue description</span></span>

<span data-ttu-id="395d2-113">Trūksta sekimo dimensijos **Savininkas**, kai sandėlio valdymo mobiliųjų įrenginių programėlė naudojama perkėlimams atlikti.</span><span class="sxs-lookup"><span data-stu-id="395d2-113">The **Owner** tracking dimension is missing when the Warehouse Management mobile app is used to make movements.</span></span> <span data-ttu-id="395d2-114">Įprastas inventoriaus perkelimo žurnalas iš „Supply Chain Management“ kliente ima dirbti kaip numatyta ir gali būti publikuotas tik jei **Savininko** dimensija užpildyta.</span><span class="sxs-lookup"><span data-stu-id="395d2-114">A regular inventory transfer journal from the Supply Chain Management client appears to work as intended and can be posted only if the **Owner** dimension is filled in.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="395d2-115">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="395d2-115">Issue resolution</span></span>

<span data-ttu-id="395d2-116">„Microsoft“ įvertino šią klaidą ir nustatė jos funkcijos apribojimą.</span><span class="sxs-lookup"><span data-stu-id="395d2-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="395d2-117">Šiuo metu sandėlio valdymo procesas palaiko tik inventorių, kurį valdo juridinis asmuo.</span><span class="sxs-lookup"><span data-stu-id="395d2-117">Currently, warehouse management processes support only inventory that is owned by the legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]