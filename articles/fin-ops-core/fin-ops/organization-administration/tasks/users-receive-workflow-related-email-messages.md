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
ms.openlocfilehash: f4c9f2f22bc4b5ca5b4351f7956ad2eb6d3b903d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140426"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="f9f66-103">Leidimas vartotojams gauti su darbo eiga susijusius el. laiškus</span><span class="sxs-lookup"><span data-stu-id="f9f66-103">Enable users to receive workflow-related email messages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f9f66-104">Galite sukonfigūruoti sistemą siųsti el. laiškus vartotojams, kai įvyksta su darbo eiga susiję įvykiai.</span><span class="sxs-lookup"><span data-stu-id="f9f66-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="f9f66-105">Pvz., galima siųsti el. laiškus vartotojams, kai jiems priskiriami dokumentai, kuriuos reikia patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="f9f66-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="f9f66-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="f9f66-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="f9f66-107">Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Užklausos > Paketinė užduotis**.</span><span class="sxs-lookup"><span data-stu-id="f9f66-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="f9f66-108">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f9f66-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f9f66-109">**Veiksmų srityje** spustelėkite **Vartotojo parinktys**.</span><span class="sxs-lookup"><span data-stu-id="f9f66-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="f9f66-110">Spustelėkite skirtuką **Darbo eiga**. Įsitikinkite, ar skyrius **Pranešimai** išplėstas.</span><span class="sxs-lookup"><span data-stu-id="f9f66-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="f9f66-111">Skyriuje **Pranešimai** galite nurodyti, kaip vartotojui turėtų būti pranešta apie įvykius, susijusius su darbo eiga.</span><span class="sxs-lookup"><span data-stu-id="f9f66-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="f9f66-112">Lauke **Eilutės elemento darbo eigos pranešimo tipas** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="f9f66-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="f9f66-113">Sugrupuota – pranešimai apie eilučių elementus sugrupuojami į vieną el. laišką.</span><span class="sxs-lookup"><span data-stu-id="f9f66-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="f9f66-114">Po vieną – el. laiškas siunčiamas apie kiekvieną eilutės elementą.</span><span class="sxs-lookup"><span data-stu-id="f9f66-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="f9f66-115">Jeigu norite, kad vartotojas pranešimus gautų kliente, pažymėkite žymės langelį **Siųsti pranešimus el. paštu**.</span><span class="sxs-lookup"><span data-stu-id="f9f66-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="f9f66-116">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="f9f66-116">Click **Save**.</span></span>
7. <span data-ttu-id="f9f66-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f9f66-117">Close the page.</span></span>

