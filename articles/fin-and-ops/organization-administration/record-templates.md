---
title: "Įrašų šablonai"
description: "Šiame straipsnyje pristatyta įrašų šablonų sąvoka ir paaiškinta, kaip juos galima naudoti, norint sukurti informaciją bendrai naudojančius įrašus."
author: pvillads
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 426fd8fafec061b649cbb31109ffe8fabc24917d
ms.contentlocale: lt-lt
ms.lasthandoff: 12/18/2018

---

# <a name="record-templates"></a><span data-ttu-id="b9595-103">Įrašų šablonai</span><span class="sxs-lookup"><span data-stu-id="b9595-103">Record templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9595-104">Šiame straipsnyje pristatyta įrašų šablonų sąvoka ir paaiškinta, kaip juos galima naudoti, norint sukurti informaciją bendrai naudojančius įrašus.</span><span class="sxs-lookup"><span data-stu-id="b9595-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="b9595-105">Įrašų šablonai gali padėti greičiau sukurti įrašus naudojant „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="b9595-105">Record templates can help you to create records more quickly in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="b9595-106">Naudodami „Microsoft Dynamics 365 for Finance and Operations“ galite kurti tik kai kurių įrašų tipų įrašų šablonus.</span><span class="sxs-lookup"><span data-stu-id="b9595-106">You can create record templates for only some of the record types in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="b9595-107">Pavyzdžiui, įsivaizduokite, kad įvedate automobilio nuomos verslo, esančio San Franciske, nuomos informaciją.</span><span class="sxs-lookup"><span data-stu-id="b9595-107">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="b9595-108">Kadangi dauguma klientų gali būti iš San Francisko teritorijos, būtų gerai, jei galėtumėte automatiškai užpildyti laukų **Valstija**, **Šalis** ir **Miestas** nuomos formos.</span><span class="sxs-lookup"><span data-stu-id="b9595-108">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span>

> [!NOTE]
> <span data-ttu-id="b9595-109">Šablonus galite taikyti tik toms „Finance and Operations“ sritims, prie kurių turite prieigą.</span><span class="sxs-lookup"><span data-stu-id="b9595-109">You can apply templates only for the areas of Finance and Operations that you have access to.</span></span> <span data-ttu-id="b9595-110">Tačiau visi šablonų pavaidinimai matomi jums, kai kuriate naują įrašą, ir kitiems vartotojams, jei kuriate šablonus, kurie bus pasiekiami visiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="b9595-110">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="b9595-111">Turėkite tai omenyje, kai šablonams suteiksite pavadinimus.</span><span class="sxs-lookup"><span data-stu-id="b9595-111">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="b9595-112">Pvz., nenaudokite pavadinimų, kuriuose yra žodžiai, pvz., „komisiniai“, jei tai, kad kai kurie darbuotojai įmonėje gauna atlyginimus taikant komisinius, yra slapta informacija.</span><span class="sxs-lookup"><span data-stu-id="b9595-112">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span>

<span data-ttu-id="b9595-113">Kai pasiekiamas vienas ar daugiau konkrečios formos šablonų, prie kurių turite prieigą, ir bandote sukurti naują įrašą formoje, rodomas puslapis **Pasirinkti šabloną, skirtą**.</span><span class="sxs-lookup"><span data-stu-id="b9595-113">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="b9595-114">Iš sąrašo pasirinkus šabloną sukuriamas naujas įrašas, kuriame yra pagal pasirinktą šabloną numatyta informacija.</span><span class="sxs-lookup"><span data-stu-id="b9595-114">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="b9595-115">Jei nenorite naudoti šablonų kurdami naujus įrašus, puslapyje **Pasirinkti šabloną** pažymėkite žymės langelį **Daugiau neklausti**.</span><span class="sxs-lookup"><span data-stu-id="b9595-115">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="b9595-116">Norėdami vėl rodyti šablono pasirinkimo dialogo langą, dešiniuoju pelės klavišu spustelėkite bet kurį įrašą, spustelėkite **Įrašo informacija**, o po to spustelėkite **Rodyti šablonų parinktis**.</span><span class="sxs-lookup"><span data-stu-id="b9595-116">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>

