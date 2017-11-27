---
title: "Išplėstinio banko suderinimo apžvalga"
description: "Šiame straipsnyje aprašytas pažangus banko suderinimo proceso srautas. Pažangaus banko suderinimo funkcija leidžia importuoti banko išrašus, kuriuos galima automatiškai suderinti iš banko operacijas."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e069bf65e7dcab7f3b049aa786f3daff07383f4c
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="a3aa2-104">Išplėstinio banko suderinimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="a3aa2-104">Advanced bank reconciliation overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a3aa2-105">Šiame straipsnyje aprašytas pažangus banko suderinimo proceso srautas.</span><span class="sxs-lookup"><span data-stu-id="a3aa2-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="a3aa2-106">Pažangaus banko suderinimo funkcija leidžia importuoti banko išrašus, kuriuos galima automatiškai suderinti iš banko operacijas.</span><span class="sxs-lookup"><span data-stu-id="a3aa2-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="a3aa2-107">Naudodamiesi išplėstinio banko suderinimo funkcija galite importuoti banko išrašus.</span><span class="sxs-lookup"><span data-stu-id="a3aa2-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="a3aa2-108">Importuotą banko išrašą galima automatiškai suderinti banko operacijose.</span><span class="sxs-lookup"><span data-stu-id="a3aa2-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="a3aa2-109">Toliau pateikiami išplėstinio banko suderinimo eigos veiksmai.</span><span class="sxs-lookup"><span data-stu-id="a3aa2-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="a3aa2-110">Nustatykite banko išrašo importavimą.</span><span class="sxs-lookup"><span data-stu-id="a3aa2-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="a3aa2-111">Importuokite banko išrašus naudodami duomenų objekto sistemą.</span><span class="sxs-lookup"><span data-stu-id="a3aa2-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="a3aa2-112">Paprastai yra įtaisyti trys banko išrašų formatai: ISO20022, BAI2 ir MT940.</span><span class="sxs-lookup"><span data-stu-id="a3aa2-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="a3aa2-113">Funkcijas galima išplėsti į bet kokį formatą.</span><span class="sxs-lookup"><span data-stu-id="a3aa2-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="a3aa2-114">Nustatykite numeraciją, kuri bus naudojama išplėstiniam banko suderinimui ir nurodykite banko suderinimo gretinimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="a3aa2-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="a3aa2-115">Derinimo gretinimo taisyklė – tai kriterijų rinkinys, naudojamas vykdant derinimo procesą, norint filtruoti banko išrašo eilutes ir „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ banko operacijos eilutes.</span><span class="sxs-lookup"><span data-stu-id="a3aa2-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 for Finance and Operations, Enterprise edition bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="a3aa2-116">Priklausomai nuo jūsų verslo praktikos, norėdami automatizuoti ir optimizuoti derinimo procesą, galite nustatyti daugiau nei vieną gretinimo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="a3aa2-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="a3aa2-117">Suderinkite banko išrašus su „Finance and Operations“ banko operacijomis.</span><span class="sxs-lookup"><span data-stu-id="a3aa2-117">Reconcile bank statements with Finance and Operations bank transactions.</span></span>
    -   <span data-ttu-id="a3aa2-118">Atlikite automatinį gretinimą ir sukurkite derinimo žurnalus.</span><span class="sxs-lookup"><span data-stu-id="a3aa2-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="a3aa2-119">Peržiūrėkite banko išrašus ir „Finance and Operations“ banko operacijas vieną šalia kito.</span><span class="sxs-lookup"><span data-stu-id="a3aa2-119">View bank statements and Finance and Operations bank transactions side by side.</span></span>
    -   <span data-ttu-id="a3aa2-120">Automatiškai registruokite „Finance and Operations“ banko operacijas, jei jos rodomos banko išraše, bet nebus rodomos „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="a3aa2-120">Automatically post Finance and Operations bank transactions if they appear on a bank statement but don't appear in Finance and Operations.</span></span>
    -   <span data-ttu-id="a3aa2-121">Sugeneruokite derinimo išrašą.</span><span class="sxs-lookup"><span data-stu-id="a3aa2-121">Generate a reconciliation statement.</span></span>






