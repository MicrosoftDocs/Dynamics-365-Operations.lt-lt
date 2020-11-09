---
title: Trikčių, susijusių su sprendimo supratimu, šalinimas
description: Šioje temoje pateikiama trikčių šalinimo informacija, kuri gali padėti išspręsti problemas, susijusias su sprendimo supratimu.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 7f1a6e424996201ecae1b624c13cfc573745dc0a
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997283"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a><span data-ttu-id="56441-103">Trikčių, susijusių su sprendimo supratimu, šalinimas</span><span class="sxs-lookup"><span data-stu-id="56441-103">Troubleshoot issues related to solution awareness</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="56441-104">Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Common Data Service“ programų trikčių šalinimo informacija.</span><span class="sxs-lookup"><span data-stu-id="56441-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="56441-105">Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, susijusias su sprendimo supratimu.</span><span class="sxs-lookup"><span data-stu-id="56441-105">Specifically, it provides information that can help you fix issues that are related to solution awareness.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="56441-106">Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų.</span><span class="sxs-lookup"><span data-stu-id="56441-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="56441-107">Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.</span><span class="sxs-lookup"><span data-stu-id="56441-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="error-on-the-dual-write-page"></a><span data-ttu-id="56441-108">Dvigubo rašymo funkcijos puslapyje įvyko klaida</span><span class="sxs-lookup"><span data-stu-id="56441-108">Error on the Dual-write page</span></span>

<span data-ttu-id="56441-109">**Dvigubo rašymo** funkcijos puslapyje galite gauti klaidos pranešimų, panašių į toliau pateiktą pavyzdį:</span><span class="sxs-lookup"><span data-stu-id="56441-109">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="56441-110">*Objektas pavadinimu 'msdyn\_dualwriteentitymap' su namemapping='Logical' nebuvo rastas MetadataCache.*</span><span class="sxs-lookup"><span data-stu-id="56441-110">*The entity with a name 'msdyn\_dualwriteentitymap' with namemapping='Logical' was not found in the MetadataCache.*</span></span>

<span data-ttu-id="56441-111">Norėdami išspręsti šią problemą, įsitikinkite, kad „Common Data Service” įdiegtas dvigubo rašymo funkcijos pagrindinis sprendimas.</span><span class="sxs-lookup"><span data-stu-id="56441-111">To fix the issue, make sure that the dual-write core solution is installed in Common Data Service.</span></span> <span data-ttu-id="56441-112">Dvigubo rašymo funkcijos pagrindinis sprendimas yra būtinas siekiant suprasti sprendimą.</span><span class="sxs-lookup"><span data-stu-id="56441-112">The dual-write core solution is a prerequisite for solution awareness.</span></span>
