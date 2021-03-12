---
title: Įrašų šablonų apžvalga
description: Šiame straipsnyje pristatyta įrašų šablonų sąvoka ir paaiškinta, kaip juos galima naudoti, norint sukurti informaciją bendrai naudojančius įrašus.
author: pvillads
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca9ddaed0c4aad6aeb3877384778d33f83e6e4aa
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796857"
---
# <a name="record-templates-overview"></a><span data-ttu-id="64fcc-103">Įrašų šablonų apžvalga</span><span class="sxs-lookup"><span data-stu-id="64fcc-103">Record templates overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64fcc-104">Šiame straipsnyje pristatyta įrašų šablonų sąvoka ir paaiškinta, kaip juos galima naudoti, norint sukurti informaciją bendrai naudojančius įrašus.</span><span class="sxs-lookup"><span data-stu-id="64fcc-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="64fcc-105">Naudodami įrašų šablonus, įrašus sukursite greičiau, tačiau galite kurti ne visų įrašų tipų įrašų šablonus.</span><span class="sxs-lookup"><span data-stu-id="64fcc-105">Record templates can help you to create records more quickly, however you can only create record templates for some record types.</span></span>

<span data-ttu-id="64fcc-106">Pavyzdžiui, įsivaizduokite, kad įvedate automobilio nuomos verslo, esančio San Franciske, nuomos informaciją.</span><span class="sxs-lookup"><span data-stu-id="64fcc-106">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="64fcc-107">Kadangi dauguma klientų gali būti iš San Francisko teritorijos, būtų gerai, jei galėtumėte automatiškai užpildyti laukų **Valstija**, **Šalis** ir **Miestas** nuomos formos.</span><span class="sxs-lookup"><span data-stu-id="64fcc-107">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span>

> [!NOTE]
> <span data-ttu-id="64fcc-108">Galite taikyti šablonus tik toms sritims, prie kurių turite prieigą.</span><span class="sxs-lookup"><span data-stu-id="64fcc-108">You can apply templates only in areas that you have access to.</span></span> <span data-ttu-id="64fcc-109">Tačiau visi šablonų pavaidinimai matomi jums, kai kuriate naują įrašą, ir kitiems vartotojams, jei kuriate šablonus, kurie bus pasiekiami visiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="64fcc-109">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="64fcc-110">Turėkite tai omenyje, kai šablonams suteiksite pavadinimus.</span><span class="sxs-lookup"><span data-stu-id="64fcc-110">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="64fcc-111">Pvz., nenaudokite pavadinimų, kuriuose yra žodžiai, pvz., „komisiniai“, jei tai, kad kai kurie darbuotojai įmonėje gauna atlyginimus taikant komisinius, yra slapta informacija.</span><span class="sxs-lookup"><span data-stu-id="64fcc-111">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span>

<span data-ttu-id="64fcc-112">Kai pasiekiamas vienas ar daugiau konkrečios formos šablonų, prie kurių turite prieigą, ir bandote sukurti naują įrašą formoje, rodomas puslapis **Pasirinkti šabloną, skirtą**.</span><span class="sxs-lookup"><span data-stu-id="64fcc-112">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="64fcc-113">Iš sąrašo pasirinkus šabloną sukuriamas naujas įrašas, kuriame yra pagal pasirinktą šabloną numatyta informacija.</span><span class="sxs-lookup"><span data-stu-id="64fcc-113">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="64fcc-114">Jei nenorite naudoti šablonų kurdami naujus įrašus, puslapyje **Pasirinkti šabloną** pažymėkite žymės langelį **Daugiau neklausti**.</span><span class="sxs-lookup"><span data-stu-id="64fcc-114">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="64fcc-115">Norėdami vėl rodyti šablono pasirinkimo dialogo langą, dešiniuoju pelės klavišu spustelėkite bet kurį įrašą, spustelėkite **Įrašo informacija**, o po to spustelėkite **Rodyti šablonų parinktis**.</span><span class="sxs-lookup"><span data-stu-id="64fcc-115">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>
