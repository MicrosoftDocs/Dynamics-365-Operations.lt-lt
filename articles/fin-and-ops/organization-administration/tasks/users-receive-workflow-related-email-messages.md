---
title: Leidimas vartotojams gauti su darbo eiga susijusius el. laiškus
description: Galite sukonfigūruoti sistemą siųsti el. laiškus vartotojams, kai įvyksta su darbo eiga susiję įvykiai.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e08f95ef6d263ee0f8c0a94b258c8a2795786bc
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916397"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="3d1b5-103">Leidimas vartotojams gauti su darbo eiga susijusius el. laiškus</span><span class="sxs-lookup"><span data-stu-id="3d1b5-103">Enable users to receive workflow-related email messages</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3d1b5-104">Galite sukonfigūruoti sistemą siųsti el. laiškus vartotojams, kai įvyksta su darbo eiga susiję įvykiai.</span><span class="sxs-lookup"><span data-stu-id="3d1b5-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="3d1b5-105">Pvz., galima siųsti el. laiškus vartotojams, kai jiems priskiriami dokumentai, kuriuos reikia patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="3d1b5-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="3d1b5-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="3d1b5-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="3d1b5-107">Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Užklausos > Paketinė užduotis**.</span><span class="sxs-lookup"><span data-stu-id="3d1b5-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="3d1b5-108">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3d1b5-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3d1b5-109">**Veiksmų srityje** spustelėkite **Vartotojo parinktys**.</span><span class="sxs-lookup"><span data-stu-id="3d1b5-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="3d1b5-110">Spustelėkite skirtuką **Darbo eiga**. Įsitikinkite, ar skyrius **Pranešimai** išplėstas.</span><span class="sxs-lookup"><span data-stu-id="3d1b5-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="3d1b5-111">Skyriuje **Pranešimai** galite nurodyti, kaip vartotojui turėtų būti pranešta apie įvykius, susijusius su darbo eiga.</span><span class="sxs-lookup"><span data-stu-id="3d1b5-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="3d1b5-112">Lauke **Eilutės elemento darbo eigos pranešimo tipas** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="3d1b5-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="3d1b5-113">Sugrupuota – pranešimai apie eilučių elementus sugrupuojami į vieną el. laišką.</span><span class="sxs-lookup"><span data-stu-id="3d1b5-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="3d1b5-114">Po vieną – el. laiškas siunčiamas apie kiekvieną eilutės elementą.</span><span class="sxs-lookup"><span data-stu-id="3d1b5-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="3d1b5-115">Jeigu norite, kad vartotojas pranešimus gautų kliente, pažymėkite žymės langelį **Siųsti pranešimus el. paštu**.</span><span class="sxs-lookup"><span data-stu-id="3d1b5-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="3d1b5-116">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3d1b5-116">Click **Save**.</span></span>
7. <span data-ttu-id="3d1b5-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3d1b5-117">Close the page.</span></span>

