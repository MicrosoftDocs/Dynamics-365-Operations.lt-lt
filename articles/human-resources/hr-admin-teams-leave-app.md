---
title: „Human Resources“ programa platformoje „Teams“
description: Šioje temoje pristatoma „Microsoft Dynamics 365 Human Resources” programa, veikianti platformoje „Microsoft Teams“.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 423ec36a73e8af9d915c5cfe16bd4d552448e2b6
ms.sourcegitcommit: d1541831d556b722a71aed442043ffb4a4576d87
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/20/2020
ms.locfileid: "3388121"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="2ffb5-103">„Human Resources“ programa platformoje „Teams“</span><span class="sxs-lookup"><span data-stu-id="2ffb5-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="2ffb5-104">„Microsoft Teams“ veikianti programa „Microsoft Dynamics 365 Human Resources“ leidžia darbuotojams greitai prašyti išleisti iš darbo ir peržiūrėti savo ne darbo laiko balanso informaciją programoje „Microsoft Teams“.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="2ffb5-105">Norėdami prašyti informacijos, darbuotojai gali bendrauti su robotu.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="2ffb5-106">Skirtuke **Ne darbo laikas** pateikiama išsamesnė informacija.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-106">The **Time off** tab provides more detailed information.</span></span>

![„Human Resources Teams“ atostogų programos robotas](./media/hr-admin-teams-leave-app-bot.png)

![„Human Resources Teams“ atostogų programos skirtukas Ne darbo laikas](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="2ffb5-109">Diegimas ir nustatymas</span><span class="sxs-lookup"><span data-stu-id="2ffb5-109">Install and setup</span></span>

<span data-ttu-id="2ffb5-110">Programą „Human Resources“ galite rasti „Teams“ parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="2ffb5-111">Daugiau informacijos, kaip įdiegti „Teams“ programą, žr. [Atostogų prašymų valdymas „Teams“](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="2ffb5-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="2ffb5-112">Informacijos apie programų teisių valdymą „Teams“ žr. [Programų teisių strategijų valdymas programoje „Microsoft Teams“](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="2ffb5-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="known-issues"></a><span data-ttu-id="2ffb5-113">Žinomos problemos</span><span class="sxs-lookup"><span data-stu-id="2ffb5-113">Known issues</span></span>

| <span data-ttu-id="2ffb5-114">Išdavimas</span><span class="sxs-lookup"><span data-stu-id="2ffb5-114">Issue</span></span> | <span data-ttu-id="2ffb5-115">Būsena</span><span class="sxs-lookup"><span data-stu-id="2ffb5-115">Status</span></span> |
| --- | --- |
| <span data-ttu-id="2ffb5-116">Balansas yra netinkamas, kai ne darbo laikas pateikiamas būsimo laikotarpio datai.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-116">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="2ffb5-117">Prognozavimas dar negalimas.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-117">Forecasting isn't yet available.</span></span> <span data-ttu-id="2ffb5-118">Rodomas dabartinio laikotarpio balansas.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-118">The balance displays for the current date.</span></span> |
| <span data-ttu-id="2ffb5-119">Sumažinus esamos užklausos valandų skaičių, **Likęs balandas** sumažėja, o ne padidėja.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-119">When reducing the number of hours taken in an existing request, the **Remaining balance** goes down instead of up.</span></span> | <span data-ttu-id="2ffb5-120">Šią žinomą problemą spręsime ateityje.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-120">We'll address this known issue in the future.</span></span> <span data-ttu-id="2ffb5-121">Rodoma netinkamai, tačiau tinkami kiekiai koreguojami pateikus.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-121">The display is incorrect, but the correct amounts are adjusted upon submission.</span></span> |
| <span data-ttu-id="2ffb5-122">Toms pačioms datoms rodomos dvi kortelės **Būsimas ne darbo laikas**.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-122">Two **Upcoming time off** cards display for the same dates.</span></span> | <span data-ttu-id="2ffb5-123">Kortelės atitinka atskiras pateiktis.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-123">The cards represent individual submissions.</span></span> <span data-ttu-id="2ffb5-124">Toliau priimsime atsiliepimus ir atliksime koregavimus.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-124">We'll continue to take feedback and make adjustments.</span></span> |
| <span data-ttu-id="2ffb5-125">Nepavyksta atšaukti užklausos **Peržiūrima**.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-125">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="2ffb5-126">Ši funkcija šiuo metu nepalaikoma ir bus įtraukta į būsimą leidimą.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-126">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="2ffb5-127">Balanso informacija skaičiuojama iki šios dienos.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-127">Balance information is calculated as of today.</span></span> | <span data-ttu-id="2ffb5-128">Sistema šiuo metu nerodo balansų iki kaupimo laikotarpio, net jei tai sukonfigūruotaa atostogų ir neatvykimo parametruose.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-128">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="2ffb5-129">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="2ffb5-129">Privacy notice</span></span>

<span data-ttu-id="2ffb5-130">Naudojant „Dynamics 365 Human Resources“ robotą programoje „Microsoft Teams“, analizuojamos vartotojo tekstinės įvestys, kad būtų suprasta pagrindinė užklausa / ketinimas.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-130">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="2ffb5-131">Vartotojo įvestis, pvz., „Ieškoti Contoso paskyroje“, yra nukreipiama į vieną iš „Microsoft Cognitive Services“ tarnybų – „Language Understanding Intelligent Service“ (LUIS).</span><span class="sxs-lookup"><span data-stu-id="2ffb5-131">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="2ffb5-132">Daugiau apie LUIS skaitykite  [čia](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="2ffb5-132">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="2ffb5-133">LUIS tarnyba išaiškina arba supranta vartotojo įvesties ketinimą (šiuo atveju ketinimas yra rasti informaciją) ir paskirties objektą (šiuo atveju numatomas objektas yra „Contoso“ paskyra).</span><span class="sxs-lookup"><span data-stu-id="2ffb5-133">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="2ffb5-134">Tada ši informacija perduodama į „Microsoft“  [„Azure“ roboto sistemą](https://azure.microsoft.com/services/bot-service/) , kuri sąveikauja su duomenimis, gautais iš „Dynamics 365 Human Resources“, ir nuskaito reikiamą vartotojo užklausos informaciją.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-134">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="2ffb5-135">Įdiegdami ir suteikdami prieigos teisę naudoti robotą jūs sutinkate leisti LUIS tarnybai ir „Azure“ roboto sistemai apdoroti įvesties ketinimą, o tai tampa patobulinta vartotojo šnekamąja patirtimi.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-135">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="2ffb5-136">LUIS tarnyba ir „Azure“ roboto sistema gali turėti skirtingus atitikties lygius, palyginti su „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-136">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2ffb5-137">LUIS tarnyba turi prieigą tik prie vartotojo užklausų ir nėra skirta būti prijungta prie vartotojo „Dynamics 365 Human Resources“ duomenų ar paskyros, o „Dynamics 365 Human Resources“ roboto vartotojas gali savanoriškai įvesti užklausą su kliento duomenimis, asmens duomenimis arba kitais duomenimis, ir toks užklausos turinys gali būti išiųstas į LUIS tarnybą ir „Azure“ roboto sistemą.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-137">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="2ffb5-138">Vartotojo užklausų ir pranešimų turinys saugomas LUIS sistemoje ne ilgiau nei 30 dienų, neaktyvios būsenos duomenys yra užšifruojami ir nenaudojami mokymui ir tarnybos tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="2ffb5-138">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="2ffb5-139">Daugiau apie „Cognitive Services“ skaitykite  [čia](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="2ffb5-139">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="2ffb5-140">Jei norite programų administravimo parametrus valdyti platformoje „Microsoft Teams“, eikite į [„Microsoft Teams“ administravimo centrą](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="2ffb5-140">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="2ffb5-141">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="2ffb5-141">See also</span></span> 

[<span data-ttu-id="2ffb5-142">„Microsoft Teams“ atsisiuntimas ir diegimas</span><span class="sxs-lookup"><span data-stu-id="2ffb5-142">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="2ffb5-143">„Microsoft Teams“ pagalbos centras</span><span class="sxs-lookup"><span data-stu-id="2ffb5-143">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="2ffb5-144">Atostogų prašymų valdymas „Teams“</span><span class="sxs-lookup"><span data-stu-id="2ffb5-144">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

