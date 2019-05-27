---
title: Banko žurnalo sudėtinio objekto naujinimas
description: Norėdami papildomą lauką BankTransactionType įtraukti į sudėtinį BankJournalEntity formatas, atlikite toliau nurodytus veiksmus.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 70db65dca4cfadd1ed8769386b4b437cecc217a2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565931"
---
# <a name="update-the-bank-journal-composite-entity"></a><span data-ttu-id="ada04-103">Banko žurnalo sudėtinio objekto naujinimas</span><span class="sxs-lookup"><span data-stu-id="ada04-103">Update the bank journal composite entity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ada04-104">Norėdami papildomą lauką BankTransactionType įtraukti į sudėtinį BankJournalEntity formatas, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ada04-104">The following steps are needed in order to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

<span data-ttu-id="ada04-105">Norėdami papildomą lauką BankTransactionType įtraukti į sudėtinį BankJournalEntity formatas, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ada04-105">Use the following steps to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

1.  <span data-ttu-id="ada04-106">Kompiliuokite ir sinchronizuokite toliau nurodytus banko žurnalo sudėtinius objektus, objektus ir išdėstymo lenteles.</span><span class="sxs-lookup"><span data-stu-id="ada04-106">Compile and synchronize the following bank journal composite entities, entities, and staging tables:</span></span>
    -   <span data-ttu-id="ada04-107">Sudėtinis objektas\\BankJournalEntity</span><span class="sxs-lookup"><span data-stu-id="ada04-107">Composite Entity\\BankJournalEntity</span></span>
    -   <span data-ttu-id="ada04-108">Objektas\\BankJournalHeaderEntity</span><span class="sxs-lookup"><span data-stu-id="ada04-108">Entity\\BankJournalHeaderEntity</span></span>
    -   <span data-ttu-id="ada04-109">Objektas\\BankJournalLineEntity</span><span class="sxs-lookup"><span data-stu-id="ada04-109">Entity\\BankJournalLineEntity</span></span>
    -   <span data-ttu-id="ada04-110">Lentelė\\BankJournalHeaderStaging</span><span class="sxs-lookup"><span data-stu-id="ada04-110">Table\\BankJournalHeaderStaging</span></span>
    -   <span data-ttu-id="ada04-111">Lentelė\\BankJournalLineStaging</span><span class="sxs-lookup"><span data-stu-id="ada04-111">Table\\BankJournalLineStaging</span></span>

2.  <span data-ttu-id="ada04-112">Duomenų valdymas\\duomenų projektai</span><span class="sxs-lookup"><span data-stu-id="ada04-112">Data management\\data projects</span></span>
    -   <span data-ttu-id="ada04-113">Makete **Šaltinio duomenys** rodykite tipą **Banko operacija**.</span><span class="sxs-lookup"><span data-stu-id="ada04-113">Expose the **Bank Transaction** type on **Source Data** layout.</span></span>
        -   <span data-ttu-id="ada04-114">Šaltinio duomenų formatas = XML-Element</span><span class="sxs-lookup"><span data-stu-id="ada04-114">Source data format = XML-Element</span></span>
        -   <span data-ttu-id="ada04-115">Objekto pavadinimas = banko žurnalas</span><span class="sxs-lookup"><span data-stu-id="ada04-115">Entity name = Bank Journal</span></span>
        -   <span data-ttu-id="ada04-116">Nusiuntimo duomenų failas = nauja SampleBankJournalCompositeEntity.xml versija</span><span class="sxs-lookup"><span data-stu-id="ada04-116">Upload data file = new version SampleBankJournalCompositeEntity.xml</span></span>
        -   <span data-ttu-id="ada04-117">Jei norite perrašyti esamą failą, spustelėkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="ada04-117">Click **Yes** to overwrite the existing file.</span></span>
        -   <span data-ttu-id="ada04-118">Jeigu norite generuoti susiejimą nuo pradžių, spustelėkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="ada04-118">Click **Yes** to generate mapping from scratch.</span></span>
        -   <span data-ttu-id="ada04-119">Patikrinkite, ar banko operacijos tipas yra susietas.</span><span class="sxs-lookup"><span data-stu-id="ada04-119">Verify that the Bank Transaction Type is mapped.</span></span>
            -   <span data-ttu-id="ada04-120">Objekte Eilutė spustelėkite **Peržiūrėti schemą**.</span><span class="sxs-lookup"><span data-stu-id="ada04-120">Click **View map** on Line entity.</span></span>
            -   <span data-ttu-id="ada04-121">Patikrinkite, ar banko operacijos tipas yra susietas nuo šaltinio iki išdėstymo.</span><span class="sxs-lookup"><span data-stu-id="ada04-121">Verify that Bank Transaction type is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="ada04-122">Importuokite naują išrašą.</span><span class="sxs-lookup"><span data-stu-id="ada04-122">Import the new statement.</span></span>




