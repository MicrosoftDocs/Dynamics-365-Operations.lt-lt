---
title: „Azure Active Directory” EKA prisijungimo autentifikavimo įjungimas
description: Šioje temoje paaiškinama, kaip sukonfigūruoti „Microsoft Dynamics 365 Commerce” elektroninio kasos aparato (EKA) prisijungimo funkcijas, kad būtų naudojamas „Azure Active Directory” autentifikavimas.
author: boycezhu
manager: annbe
ms.date: 03/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: dfc49585434383385b6b993893d93b95ef888384
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/08/2020
ms.locfileid: "3248945"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="5f052-103">„Azure Active Directory” EKA prisijungimo autentifikavimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="5f052-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="5f052-104">Daug klientų, kurie naudoja „Microsoft Dynamics 365 Commerce”, taip pat naudoja kitas „Microsoft” debesies tarnybas ir jie gali naudoti „Azure Active Directory” („Azure AD”) šioms tarnyboms valdyti vartotojo kredencialus.</span><span class="sxs-lookup"><span data-stu-id="5f052-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="5f052-105">Tokiais atvejais klientai gali norėti naudoti tą pačią „Azure AD” paskyrą keliose programose.</span><span class="sxs-lookup"><span data-stu-id="5f052-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="5f052-106">Šioje temoje paaiškinama, kaip sukonfigūruoti „Commerce” elektroninio kasos aparato (EKA) prisijungimo funkcijas, kad būtų naudojamas „Azure AD” autentifikavimas.</span><span class="sxs-lookup"><span data-stu-id="5f052-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="5f052-107">„Azure AD” autentifikavimo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="5f052-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="5f052-108">Norėdami, kad „Azure AD” būtų pasiekiama kaip EKA prisijungimo prie parduotuvės autentifikavimo metodas, turite sukonfigūruoti parduotuvės funkcijų šablono parametrus ir tada taikyti šiuos parametrus EKA klientams.</span><span class="sxs-lookup"><span data-stu-id="5f052-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="5f052-109">Norėdami sukonfigūruoti funkcijų šabloną, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5f052-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="5f052-110">Eikite į **„Retail and Commerce“** \> **Kanalo sąranka** \> **EKA sąranka** \> **EKA profiliai** \> **Funkcionalumo profiliai**.</span><span class="sxs-lookup"><span data-stu-id="5f052-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="5f052-111">Pasirinkite funkcijų šabloną, kurį norite pakeisti.</span><span class="sxs-lookup"><span data-stu-id="5f052-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="5f052-112">„FastTab” **Funkcijos**, skyriuje **EKA darbuotojų prisijungimas**, pakeiskite lauko **Prisijungimo autentifikavimo būdas** vertę iš **Darbuotojo ID ir slaptažodis** į **„Azure Active Directory”**.</span><span class="sxs-lookup"><span data-stu-id="5f052-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="5f052-113">Pagal numatytuosius parametrus visi funkcijų šablonai naudoja **Darbuotojo ID ir slaptažodis** kaip EKA autentifikavimo metodą.</span><span class="sxs-lookup"><span data-stu-id="5f052-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="5f052-114">Todėl, jei norite naudoti „Azure AD”, turite pakeisti lauko **Prisijungimo autentifikavimo metodas** vertę.</span><span class="sxs-lookup"><span data-stu-id="5f052-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="5f052-115">Atlikus šį pakeitimą bus paveiktos visos mažmeninės prekybos parduotuvės, kurios yra susijusios su pasirinktu funkcijų šablonu.</span><span class="sxs-lookup"><span data-stu-id="5f052-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="5f052-116">Norėdami taikyti parametrus EKA klientams, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5f052-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="5f052-117">Eikite į **„Retail and Commerce“** \> **„Retail and Commerce IT“** \> **Paskirstymo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="5f052-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="5f052-118">Paleiskite paskirstymo grafiką **1070** (**Kanalo konfigūracija**).</span><span class="sxs-lookup"><span data-stu-id="5f052-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="5f052-119">„Azure AD” autentifikavimui reikia interneto ryšio.</span><span class="sxs-lookup"><span data-stu-id="5f052-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="5f052-120">Jis neveiks, kai EKA veikia atjungties režimu.</span><span class="sxs-lookup"><span data-stu-id="5f052-120">It won't work when POS is in offline mode.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="5f052-121">„Azure AD” paskyros susiejimas su darbininku</span><span class="sxs-lookup"><span data-stu-id="5f052-121">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="5f052-122">Prieš tai, kai parduotuvės darbininkas gali naudoti „Azure AD” paskyrą, kad prisijungtų prie EKA programos, „Azure AD” paskyra turi būti susieta su tuo darbininku.</span><span class="sxs-lookup"><span data-stu-id="5f052-122">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="5f052-123">Norėdami susieti „Azure AD” paskyrą su darbininku, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5f052-123">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="5f052-124">Eikite į **Mažmeninė prekyba ir prekyba** \> **Darbuotojai** \> **Darbininkai**.</span><span class="sxs-lookup"><span data-stu-id="5f052-124">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="5f052-125">Atidarykite darbininko informacijos puslapį.</span><span class="sxs-lookup"><span data-stu-id="5f052-125">Open the details page for a worker.</span></span>
1. <span data-ttu-id="5f052-126">Veiksmų srities skirtuko **Prekyba** grupėje **Išorinė tapatybė** pasirinkite **Susieti esamą tapatybę**.</span><span class="sxs-lookup"><span data-stu-id="5f052-126">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="5f052-127">Dialogo lange **Naudoti esamą išorinę tapatybę** pasirinkite **Ieškoti pagal el. paštą**, įveskite „Azure AD” el. pašto adresą ir pasirinkite **Ieškoti**.</span><span class="sxs-lookup"><span data-stu-id="5f052-127">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="5f052-128">Pasirinkite gautą „Azure AD” paskyrą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5f052-128">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="5f052-129">Darbininko informacijos puslapio laukai **Pseudonimas**, **UPN**, **Išorinis antrinis identifikatorius**, esančius skirtuke **Prekyba**, bus automatiškai užpildomi.</span><span class="sxs-lookup"><span data-stu-id="5f052-129">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5f052-130">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="5f052-130">Additional resources</span></span>

[<span data-ttu-id="5f052-131">MPOS ir „Cloud POS“ išplėstinės registracijos funkcijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="5f052-131">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="5f052-132">Mažmeninės prekybos funkcijų šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="5f052-132">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="5f052-133"> Konfigūruoti darbininką</span><span class="sxs-lookup"><span data-stu-id="5f052-133">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
