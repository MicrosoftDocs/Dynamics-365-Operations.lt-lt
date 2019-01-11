---
title: "Sąskaitų faktūrų apmokėjimo scenarijų nustatymas"
description: "Šioje temoje aprašoma, kaip sukonfigūruoti „Dynamics 365 for Retail“, kad būtų palaikomi įvairūs scenarijai, susiję su sąskaitų faktūrų apmokėjimu."
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: b7132dc9b3c78fa04fcfc38ea72b5678ad08deb2
ms.contentlocale: lt-lt
ms.lasthandoff: 01/04/2019

---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="9cb09-103">Sąskaitų faktūrų apmokėjimo scenarijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="9cb09-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9cb09-104">„Dynamics 365 for Retail“ funkcija Apmokėti sąskaitą faktūrą išplėsta ir palaiko tolesnius scenarijus.</span><span class="sxs-lookup"><span data-stu-id="9cb09-104">The Pay invoice functionality in Dynamics 365 for Retail has been expanded to support:</span></span>

- <span data-ttu-id="9cb09-105">Kelių pardavimo užsakymų sąskaitų faktūrų apmokėjimas atliekant vieną EKA operaciją.</span><span class="sxs-lookup"><span data-stu-id="9cb09-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="9cb09-106">Įvairių tipų kliento SF, įskaitant laisvos formos sąskaitas faktūras, projektines sąskaitas faktūras ir kredito pažymas, apmokėjimas.</span><span class="sxs-lookup"><span data-stu-id="9cb09-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="9cb09-107">Norint įjungti šiuos scenarijus reikia sukonfigūruoti parduotuvių funkcijų profilį taip, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="9cb09-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="9cb09-108">Eikite į **Mažmeninė prekyba \> Kanalų sąranka \> EKA sąranka \> EKA profiliai \> Funkcijų profiliai** ir pasirinkite profilį, susietą su parduotuvėmis, kurioms norite atlikti keitimus.</span><span class="sxs-lookup"><span data-stu-id="9cb09-108">Go to **Retail \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="9cb09-109">Skirtuke **Funkcijos** pagal poreikį sukonfigūruokite tolesnius parametrus.</span><span class="sxs-lookup"><span data-stu-id="9cb09-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="9cb09-110">**Pardavimo užsakymo sąskaita faktūra** – pasirinkite **Taip**, jei vartotojams norite leisti atliekant vieną EKA operaciją apmokėti vieną ar kelias pardavimo užsakymu paremtas sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="9cb09-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="9cb09-111">**Laisvos formos sąskaita faktūra** – pasirinkite **Taip**, jei vartotojams norite leisti atliekant vieną EKA operaciją apmokėti vieną ar kelias laisvos formos sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="9cb09-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="9cb09-112">**Projekto sąskaita faktūra** – pasirinkite **Taip**, jei vartotojams norite leisti atliekant vieną EKA operaciją apmokėti vieną ar kelias projektines sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="9cb09-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="9cb09-113">**Pardavimo užsakymo kredito pažyma** – pasirinkite **Taip**, jei vartotojams norite leisti pagal atidarytas sąskaitas faktūras sudengti kelias pardavimo užsakymu paremtas kredito pažymas arba apdoroti pinigų grąžinimą klientui už atidarytą kredito pažymą.</span><span class="sxs-lookup"><span data-stu-id="9cb09-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="9cb09-114">Galimybės apmokėti ar sudengti dalines sumas dar nėra.</span><span class="sxs-lookup"><span data-stu-id="9cb09-114">Payment or settlement of partial amounts is not yet supported.</span></span>

