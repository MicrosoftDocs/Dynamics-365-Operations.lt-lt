---
title: Sistemos administratoriai negali išvalyti užsakymų sulaikymas, nes jie nėra įgalioti
description: Sistemos administratoriai negali išvalyti užsakymų sulaikymas, nes jie nėra įgalioti.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026762"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a><span data-ttu-id="f2083-103">Sistemos administratoriai negali išvalyti užsakymų sulaikymas, nes jie nėra įgalioti</span><span class="sxs-lookup"><span data-stu-id="f2083-103">System administrators can't clear order holds because they aren't authorized</span></span>

<span data-ttu-id="f2083-104">KB numeris: 4614642</span><span class="sxs-lookup"><span data-stu-id="f2083-104">KB number: 4614642</span></span>

## <a name="symptoms"></a><span data-ttu-id="f2083-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="f2083-105">Symptoms</span></span>

<span data-ttu-id="f2083-106">Sistemos administratoriai gali išvalyti pardavimo užsakymų sulaikymas, nebent jie turi tam tikrą vaidmenį, kuris priskirtas užsakymo laikymo kodui.</span><span class="sxs-lookup"><span data-stu-id="f2083-106">System administrators can't clear sales order holds unless they have the specific role that is assigned in the order hold code.</span></span>

## <a name="resolution"></a><span data-ttu-id="f2083-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="f2083-107">Resolution</span></span>

<span data-ttu-id="f2083-108">Prieigą prie kai kurių operacijų, pvz., tarpuskaitos pardavimo užsakymų, lemia verslo strategijos nustatymas.</span><span class="sxs-lookup"><span data-stu-id="f2083-108">Access to some operations, such as clearing sales order holds, is driven by the setup of a business policy.</span></span> <span data-ttu-id="f2083-109">Paprastai sistemos administratoriams neleidžiama atlikti šio tipo operacijų.</span><span class="sxs-lookup"><span data-stu-id="f2083-109">System administrators aren't typically allowed to perform operations of this type.</span></span> 

<span data-ttu-id="f2083-110">Dažniausiai prieigą atlikti tam tikrą užduotį valdo verslo strategijos, ir tik konkretūs organizacijos asmenys patvirtinami tai užduočiai atlikti.</span><span class="sxs-lookup"><span data-stu-id="f2083-110">More often, access to perform a specific task is governed by business policies, and only specific persons in an organization are approved to perform that task.</span></span> <span data-ttu-id="f2083-111">Pavyzdžiai apima patvirtinimus, kurie yra darbo eigos patvirtinimų rezultatas ir konkrečios užduotys, kurios yra darbo eigos konfigūracijos rezultatas.</span><span class="sxs-lookup"><span data-stu-id="f2083-111">Examples include approvals that are the result of workflow approvals and specific tasks that are the result of a workflow configuration.</span></span>

<span data-ttu-id="f2083-112">Nors darbo eiga nėra susieta su užsakymų sulaikyme, principas panašus.</span><span class="sxs-lookup"><span data-stu-id="f2083-112">Although no workflow is associated with order holds, the principle is similar.</span></span> <span data-ttu-id="f2083-113">Atitinkamas vaidmuo nurodo tam tikrą organizacijos žmonių grupę, kuri turi teisę išvalyti užsakymų sulaikymas.</span><span class="sxs-lookup"><span data-stu-id="f2083-113">A relevant role designates the specific group of people in an organization who have the right to clear order holds.</span></span> <span data-ttu-id="f2083-114">Ši teisė nebūtinai turi būti suteikta visiems administratoriams, nes šis būdas pažeidžia nustatytą verslo strategiją.</span><span class="sxs-lookup"><span data-stu-id="f2083-114">This right should not necessarily be granted to all administrators, because that approach violates the defined business policy.</span></span>
