---
title: Sąskaitų faktūrų apmokėjimo scenarijų nustatymas
description: Šioje temoje aprašoma, kaip sukonfigūruoti „Dynamics 365 Commerce“, kad būtų palaikomi įvairūs scenarijai, susiję su sąskaitų faktūrų apmokėjimu.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6f818fa552fe5651dc7d56de265fe989c57fa822
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257078"
---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="80635-103">Sąskaitų faktūrų apmokėjimo scenarijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="80635-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="80635-104">„Dynamics 365 Commerce“ funkcija Apmokėti sąskaitą faktūrą išplėsta ir palaiko tolesnius scenarijus.</span><span class="sxs-lookup"><span data-stu-id="80635-104">The Pay invoice functionality in Dynamics 365 Commerce has been expanded to support:</span></span>

- <span data-ttu-id="80635-105">Kelių pardavimo užsakymų sąskaitų faktūrų apmokėjimas atliekant vieną EKA operaciją.</span><span class="sxs-lookup"><span data-stu-id="80635-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="80635-106">Įvairių tipų kliento SF, įskaitant laisvos formos sąskaitas faktūras, projektines sąskaitas faktūras ir kredito pažymas, apmokėjimas.</span><span class="sxs-lookup"><span data-stu-id="80635-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="80635-107">Norint įjungti šiuos scenarijus reikia sukonfigūruoti parduotuvių funkcijų profilį taip, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="80635-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="80635-108">Eikite į **Mažmeninė prekyba ir prekyba \> Kanalų sąranka \> EKA sąranka \> EKA profiliai \> Funkcijų profiliai** ir pasirinkite profilį, susietą su parduotuvėmis, kurioms norite atlikti keitimus.</span><span class="sxs-lookup"><span data-stu-id="80635-108">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="80635-109">Skirtuke **Funkcijos** pagal poreikį sukonfigūruokite tolesnius parametrus.</span><span class="sxs-lookup"><span data-stu-id="80635-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="80635-110">**Pardavimo užsakymo sąskaita faktūra** – pasirinkite **Taip**, jei vartotojams norite leisti atliekant vieną EKA operaciją apmokėti vieną ar kelias pardavimo užsakymu paremtas sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="80635-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="80635-111">**Laisvos formos sąskaita faktūra** – pasirinkite **Taip**, jei vartotojams norite leisti atliekant vieną EKA operaciją apmokėti vieną ar kelias laisvos formos sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="80635-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="80635-112">**Projekto sąskaita faktūra** – pasirinkite **Taip**, jei vartotojams norite leisti atliekant vieną EKA operaciją apmokėti vieną ar kelias projektines sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="80635-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="80635-113">**Pardavimo užsakymo kredito pažyma** – pasirinkite **Taip**, jei vartotojams norite leisti pagal atidarytas sąskaitas faktūras sudengti kelias pardavimo užsakymu paremtas kredito pažymas arba apdoroti pinigų grąžinimą klientui už atidarytą kredito pažymą.</span><span class="sxs-lookup"><span data-stu-id="80635-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="80635-114">Galimybės apmokėti ar sudengti dalines sumas dar nėra.</span><span class="sxs-lookup"><span data-stu-id="80635-114">Payment or settlement of partial amounts is not yet supported.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]