---
title: Trikčių šalinimo sandėlio darbas
description: Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su sandėlio darbu „Microsoft Dynamics 365 Supply Chain Management“.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a00ae517ff583e4231099d8e9f5d5b5a696cf7f7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645798"
---
# <a name="troubleshoot-warehouse-work"></a><span data-ttu-id="a0141-103">Trikčių šalinimo sandėlio darbas</span><span class="sxs-lookup"><span data-stu-id="a0141-103">Troubleshoot warehouse work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0141-104">Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su sandėlio darbu „Microsoft Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="a0141-104">This topic describes how to fix common issues that you might encounter while you work with warehouse work in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a><span data-ttu-id="a0141-105">Negaliu perkelti licencijos lentelių, kurių serijinio numerio elementai, kai tuščia problema ir tuščias gavimas yra leidžiami sekimo dimensijos grupėje.</span><span class="sxs-lookup"><span data-stu-id="a0141-105">I can't move license plates that have serial number items when blank issue and blank receipt are allowed on the tracking dimension group.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a0141-106">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="a0141-106">Issue description</span></span>

<span data-ttu-id="a0141-107">Negalite perkelti licencijos lentelės naudodami **Perkėlimo** meniu elementą, jei serijinis numeris turi nustatymus *Tuščia problema leidžiama* ir *Tuščias kvitas leidžiamas* sekimo dimensijos grupėje ir jei esama kelių licencijos lentelių toje pačioje vietoje, kurių keletas turi serijinius numerius ir keletas neturi.</span><span class="sxs-lookup"><span data-stu-id="a0141-107">You can't move a license plate by using a **Movement** menu item if the serial number has settings of *Blank issue allowed* and *Blank receipt allowed* on the tracking dimension group, and if there are multiple license plates in the same location, some of which have serial numbers and some of which don't have them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a0141-108">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="a0141-108">Issue resolution</span></span>

<span data-ttu-id="a0141-109">Ši triktis bus pataisyta pakeitimais, kurie yra patalpinti [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span><span class="sxs-lookup"><span data-stu-id="a0141-109">This issue will be fixed by changes that are deployed in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span></span> <span data-ttu-id="a0141-110">Šie pakeitimai padarys **Serijinio numerio** laukelį pasirenkamą, kai tuščias kvitas ir tuščia triktis yra leidžiami.</span><span class="sxs-lookup"><span data-stu-id="a0141-110">Those changes will make the **Serial number** field optional when blank receipt and blank issue are allowed.</span></span>

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a><span data-ttu-id="a0141-111">Gaunu tolesnį klaidos pranešimą sandėlio pgramoje, kai apdoroju perkėlimus: „Inventoriaus savininkas %1 neleidžiamas šiame procese."</span><span class="sxs-lookup"><span data-stu-id="a0141-111">I receive the following error message in the warehouse app when I process movements: "The inventory owner %1 is not allowed in this process."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a0141-112">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="a0141-112">Issue description</span></span>

<span data-ttu-id="a0141-113">**Savininko** sekimo dimensijos trūksta, kai sandėlio programa naudojama siekiant atlikti perkėlimus.</span><span class="sxs-lookup"><span data-stu-id="a0141-113">The **Owner** tracking dimension is missing when the warehouse app is used to make movements.</span></span> <span data-ttu-id="a0141-114">Įprastas inventoriaus perkelimo žurnalas iš „Supply Chain Management“ kliente ima dirbti kaip numatyta ir gali būti publikuotas tik jei **Savininko** dimensija užpildyta.</span><span class="sxs-lookup"><span data-stu-id="a0141-114">A regular inventory transfer journal from the Supply Chain Management client appears to work as intended and can be posted only if the **Owner** dimension is filled in.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a0141-115">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="a0141-115">Issue resolution</span></span>

<span data-ttu-id="a0141-116">„Microsoft“ įvertino šią klaidą ir nustatė jos funkcijos apribojimą.</span><span class="sxs-lookup"><span data-stu-id="a0141-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="a0141-117">Šiuo metu sandėlio valdymo procesas palaiko tik inventorių, kurį valdo juridinis asmuo.</span><span class="sxs-lookup"><span data-stu-id="a0141-117">Currently, warehouse management processes support only inventory that is owned by the legal entity.</span></span>
