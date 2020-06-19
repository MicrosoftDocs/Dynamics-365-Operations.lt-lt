---
title: „Azure Active Directory” EKA prisijungimo autentifikavimo įjungimas
description: Šioje temoje paaiškinama, kaip sukonfigūruoti „Microsoft Dynamics 365 Commerce” elektroninio kasos aparato (EKA) prisijungimo funkcijas, kad būtų naudojamas „Azure Active Directory” autentifikavimas.
author: boycezhu
manager: annbe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 4f5a02348e8cef44424ae5d6a49de02d762ba245
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410040"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="dc604-103">„Azure Active Directory” EKA prisijungimo autentifikavimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="dc604-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="dc604-104">Daug klientų, kurie naudoja „Microsoft Dynamics 365 Commerce”, taip pat naudoja kitas „Microsoft” debesies tarnybas ir jie gali naudoti „Azure Active Directory” („Azure AD”) šioms tarnyboms valdyti vartotojo kredencialus.</span><span class="sxs-lookup"><span data-stu-id="dc604-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="dc604-105">Tokiais atvejais klientai gali norėti naudoti tą pačią „Azure AD” paskyrą keliose programose.</span><span class="sxs-lookup"><span data-stu-id="dc604-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="dc604-106">Šioje temoje paaiškinama, kaip sukonfigūruoti „Commerce” elektroninio kasos aparato (EKA) prisijungimo funkcijas, kad būtų naudojamas „Azure AD” autentifikavimas.</span><span class="sxs-lookup"><span data-stu-id="dc604-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="dc604-107">„Azure AD” autentifikavimo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="dc604-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="dc604-108">Norėdami, kad „Azure AD” būtų pasiekiama kaip EKA prisijungimo prie parduotuvės autentifikavimo metodas, turite sukonfigūruoti parduotuvės funkcijų šablono parametrus ir tada taikyti šiuos parametrus EKA klientams.</span><span class="sxs-lookup"><span data-stu-id="dc604-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="dc604-109">Norėdami sukonfigūruoti funkcijų šabloną, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dc604-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="dc604-110">Eikite į **„Retail and Commerce“** \> **Kanalo sąranka** \> **EKA sąranka** \> **EKA profiliai** \> **Funkcionalumo profiliai**.</span><span class="sxs-lookup"><span data-stu-id="dc604-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="dc604-111">Pasirinkite funkcijų šabloną, kurį norite pakeisti.</span><span class="sxs-lookup"><span data-stu-id="dc604-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="dc604-112">„FastTab” **Funkcijos**, skyriuje **EKA darbuotojų prisijungimas**, pakeiskite lauko **Prisijungimo autentifikavimo būdas** vertę iš **Darbuotojo ID ir slaptažodis** į **„Azure Active Directory”**.</span><span class="sxs-lookup"><span data-stu-id="dc604-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="dc604-113">Pagal numatytuosius parametrus visi funkcijų šablonai naudoja **Darbuotojo ID ir slaptažodis** kaip EKA autentifikavimo metodą.</span><span class="sxs-lookup"><span data-stu-id="dc604-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="dc604-114">Todėl, jei norite naudoti „Azure AD”, turite pakeisti lauko **Prisijungimo autentifikavimo metodas** vertę.</span><span class="sxs-lookup"><span data-stu-id="dc604-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="dc604-115">Atlikus šį pakeitimą bus paveiktos visos mažmeninės prekybos parduotuvės, kurios yra susijusios su pasirinktu funkcijų šablonu.</span><span class="sxs-lookup"><span data-stu-id="dc604-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="dc604-116">Norėdami taikyti parametrus EKA klientams, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dc604-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="dc604-117">Eikite į **„Retail and Commerce“** \> **„Retail and Commerce IT“** \> **Paskirstymo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="dc604-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="dc604-118">Paleiskite paskirstymo grafiką **1070** (**Kanalo konfigūracija**).</span><span class="sxs-lookup"><span data-stu-id="dc604-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="dc604-119">„Azure AD” autentifikavimui reikia interneto ryšio.</span><span class="sxs-lookup"><span data-stu-id="dc604-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="dc604-120">Jis neveiks, kai EKA veikia atjungties režimu.</span><span class="sxs-lookup"><span data-stu-id="dc604-120">It won't work when POS is in offline mode.</span></span>
> 
> <span data-ttu-id="dc604-121">Šiuo metu **valdytojo nepaisymo** funkcija nepalaiko „Azure AD“ kaip autentifikavimo būdo.</span><span class="sxs-lookup"><span data-stu-id="dc604-121">Currently, the **Manager override** function doesn't support Azure AD as an authentication method.</span></span> <span data-ttu-id="dc604-122">Operatoriaus ID ir slaptažodis yra privalomi, net jei jie „Azure AD“ sukonfigūruoti kaip EKA prisijungimo autentifikavimo metodas.</span><span class="sxs-lookup"><span data-stu-id="dc604-122">An operator ID and password are required even if Azure AD is configured as the authentication method for POS sign-in.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="dc604-123">„Azure AD” paskyros susiejimas su darbininku</span><span class="sxs-lookup"><span data-stu-id="dc604-123">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="dc604-124">Prieš tai, kai parduotuvės darbininkas gali naudoti „Azure AD” paskyrą, kad prisijungtų prie EKA programos, „Azure AD” paskyra turi būti susieta su tuo darbininku.</span><span class="sxs-lookup"><span data-stu-id="dc604-124">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="dc604-125">Norėdami susieti „Azure AD” paskyrą su darbininku, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dc604-125">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="dc604-126">Eikite į **Mažmeninė prekyba ir prekyba** \> **Darbuotojai** \> **Darbininkai**.</span><span class="sxs-lookup"><span data-stu-id="dc604-126">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="dc604-127">Atidarykite darbininko informacijos puslapį.</span><span class="sxs-lookup"><span data-stu-id="dc604-127">Open the details page for a worker.</span></span>
1. <span data-ttu-id="dc604-128">Veiksmų srities skirtuko **Prekyba** grupėje **Išorinė tapatybė** pasirinkite **Susieti esamą tapatybę**.</span><span class="sxs-lookup"><span data-stu-id="dc604-128">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="dc604-129">Dialogo lange **Naudoti esamą išorinę tapatybę** pasirinkite **Ieškoti pagal el. paštą**, įveskite „Azure AD” el. pašto adresą ir pasirinkite **Ieškoti**.</span><span class="sxs-lookup"><span data-stu-id="dc604-129">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="dc604-130">Pasirinkite gautą „Azure AD” paskyrą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="dc604-130">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="dc604-131">Darbininko informacijos puslapio laukai **Pseudonimas**, **UPN**, **Išorinis antrinis identifikatorius**, esančius skirtuke **Prekyba**, bus automatiškai užpildomi.</span><span class="sxs-lookup"><span data-stu-id="dc604-131">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dc604-132">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="dc604-132">Additional resources</span></span>

[<span data-ttu-id="dc604-133">MPOS ir „Cloud POS“ išplėstinės registracijos funkcijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="dc604-133">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="dc604-134">Mažmeninės prekybos funkcijų šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="dc604-134">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="dc604-135"> Konfigūruoti darbininką</span><span class="sxs-lookup"><span data-stu-id="dc604-135">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
