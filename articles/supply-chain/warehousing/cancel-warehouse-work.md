---
title: Darbo sandėlyje atšaukimas dėl išimčių tvarkymo
description: Šioje temoje aprašomas darbo funkcijų atšaukimas, kuris leidžia sandėlio prižiūrėtojams tvarkyti užblokuotą darbą.
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: daa8f0d19de75e6c126fe7a5fe312bca24c89bdc
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016246"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a><span data-ttu-id="a4af0-103">Darbo sandėlyje atšaukimas dėl išimčių tvarkymo</span><span class="sxs-lookup"><span data-stu-id="a4af0-103">Cancel warehouse work for exception handling</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4af0-104">„Microsoft Dynamics 365 Supply Chain Management“ darbo atšaukimo funkcija leidžia administratoriui atšaukti konkretų vykdomą sandėlio darbą, kuris yra blokuojamas sistemos arba kurio negalima baigti dėl išimtinių aplinkybių.</span><span class="sxs-lookup"><span data-stu-id="a4af0-104">The Cancel work functionality in Microsoft Dynamics 365 Supply Chain Management lets the admin user cancel specific warehouse work that is currently in progress, but that is blocked by the system or can't be completed because of exceptional circumstances.</span></span> <span data-ttu-id="a4af0-105">Ši funkcija yra patraukli ir saugi alternatyva SQL koreguojamiems scenarijams, kurie nustato prieštaringus duomenis.</span><span class="sxs-lookup"><span data-stu-id="a4af0-105">This functionality is an attractive and secure alternative to SQL corrective scripts that fix inconsistent data.</span></span> <span data-ttu-id="a4af0-106">Tačiau, kadangi šie scenarijai įprastai yra reikalaujami iš IT profesionalų, darbo atšaukimo funkciją gali naudoti įmonės vartotojai, turintys administratoriaus teises.</span><span class="sxs-lookup"><span data-stu-id="a4af0-106">However, whereas these scripts are typically requested from IT professionals, the Cancel work functionality can be used by users in the company who have admin rights.</span></span>

<span data-ttu-id="a4af0-107">Darbo atšaukimo funkciją galite pasiekti **Sandėlio valdymas** \> **Periodinės užduotys** \> **Valyti \> Atšaukti darbą**.</span><span class="sxs-lookup"><span data-stu-id="a4af0-107">You can access the Cancel work functionality at **Warehouse management** \> **Periodic tasks** \> **Clean up \> Cancel work**.</span></span> <span data-ttu-id="a4af0-108">Dialogo lange **Atšaukti darbą** nurodykite darbo, kurį norite atšaukti, ID ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a4af0-108">In the **Cancel work** dialog box, specify the work ID of the work to cancel, and then select **OK**.</span></span>

## <a name="warehouse-work-that-can-be-canceled"></a><span data-ttu-id="a4af0-109">Sandėlio darbas, kurį galima atšaukti</span><span class="sxs-lookup"><span data-stu-id="a4af0-109">Warehouse work that can be canceled</span></span>

<span data-ttu-id="a4af0-110">Atliekant sandėlio paėmimo veiksmus, darbuotojas gali susidurti su situacijomis, kuriose jis užregistravo kiekius, paimtus iš saugojimo vietos į vartotojo vietą, tačiau negali užregistruoti padėjimo veiksmo.</span><span class="sxs-lookup"><span data-stu-id="a4af0-110">During warehouse picking operations, a worker might encounter situations where they have registered quantities as picked from a storage location to their user location, but then they can't register the put operation.</span></span> <span data-ttu-id="a4af0-111">Nesuderinami sandėlio duomenys dažnai, bet ne visada yra priežastis, kodėl darbas blokuojamas.</span><span class="sxs-lookup"><span data-stu-id="a4af0-111">Inconsistent warehouse data is often, but not always, the reason why work is blocked.</span></span>

<span data-ttu-id="a4af0-112">Skirtingai nuo įprastos atšaukimo funkcijos, kurią galima pasiekti naudojant darbo antraštėje esantį mygtuką **Atšaukti** , darbo atšaukimo funkcija nereikalauja, kad paskutinio užbaigto darbo eilutė būtų **padėjimo** tipo darbo eilutė.</span><span class="sxs-lookup"><span data-stu-id="a4af0-112">Unlike the regular Cancel functionality that can be accessed by using the **Cancel** button on the work header, the Cancel work functionality doesn't require that the last completed work line be a work line of the **put** type.</span></span> <span data-ttu-id="a4af0-113">Kitaip tariant, dirbant su darbo atšaukimo funkcija, atšaukimo logika gali būti vykdoma, net jei darbo eilutėje nurodytas prekių kiekis yra vartotojo vietoje.</span><span class="sxs-lookup"><span data-stu-id="a4af0-113">In other words, for the Cancel work functionality, cancellation logic can be run even if the item quantity on a work line is in a user location.</span></span>

> [!NOTE]
> <span data-ttu-id="a4af0-114">Esant darbui, kurį reikia atšaukti dėl darbinių priežasčių, sandėlio vartotojai turi toliau naudoti įprastinę atšaukimo funkciją darbo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="a4af0-114">For work that must be canceled for operational reasons, warehouse users must continue to use the regular Cancel functionality on the work page.</span></span>

<span data-ttu-id="a4af0-115">Naudojant darbo atšaukimo funkciją galima atšaukti tik darbus, kurių tipas yra **Pardavimas** , **Perkėlimo išdavimas** , **Žaliavų paėmimas** arba **Papildymas**.</span><span class="sxs-lookup"><span data-stu-id="a4af0-115">Only work of the **Sales** , **Transfer issue** , **Raw material picking** , or **Replenishment** type can be canceled by using the Cancel work functionality.</span></span> <span data-ttu-id="a4af0-116">Atšaukimo logika nebus vykdoma sušaldytos žaliavos paėmimo darbui arba darbui, kurį galima atšaukti naudojant įprastą atšaukimo funkciją (žr. ankstesnę pastabą).</span><span class="sxs-lookup"><span data-stu-id="a4af0-116">Cancellation logic won't be run for frozen raw material picking work or work that can be canceled by using the regular Cancel functionality (see the preceding note).</span></span>

<span data-ttu-id="a4af0-117">Norint atblokuoti darbą, sistema atšaukia likusias darbo eilutes ir nustato sandėlio duomenis, susietus su vartotojo nurodytu darbo ID.</span><span class="sxs-lookup"><span data-stu-id="a4af0-117">To unblock the work, the system cancels any remaining work lines and fixes the warehouse data that is associated with the work ID that the user specified.</span></span> <span data-ttu-id="a4af0-118">Tada galės būti tęsiami bet kokie įprasti sandėlio tvarkymo veiksmai, susiję su paveiktu prekių kiekiu.</span><span class="sxs-lookup"><span data-stu-id="a4af0-118">Any regular warehouse-handling operations that involve the affected item quantity can then resume.</span></span>

<span data-ttu-id="a4af0-119">Norėdamas perkelti paveiktą prekę į konkrečią vietą po to, kai buvo atšauktas darbas, vartotojas turi atlikti atsargų perkėlią arba kiekio koregavimą mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="a4af0-119">To put the affected item in a specific location after the work is canceled, the user must use an inventory movement or quantity adjustment operation on a mobile device.</span></span>
