---
title: Kurti čekius, kurių būsena Tuščia
description: Šioje temoje paaiškinama, kaip kurti tuščius banko sąskaitos čekius puslapyje „Čekiai“.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: aa1c4c33b977c0173da98aee409389b9242980fb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976462"
---
# <a name="create-checks-that-have-blank-status"></a><span data-ttu-id="8da33-103">Kurti čekius, kurių būsena Tuščia</span><span class="sxs-lookup"><span data-stu-id="8da33-103">Create checks that have Blank status</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8da33-104">Šioje temoje paaiškinama, kaip kurti tuščius čekius.</span><span class="sxs-lookup"><span data-stu-id="8da33-104">This topic explains how to create blank checks.</span></span> <span data-ttu-id="8da33-105">Pavyzdžiui, galite sukurti tuščią čekį, kad įrašytumėte sugadintą čekį, kurio negalima naudoti mokant.</span><span class="sxs-lookup"><span data-stu-id="8da33-105">For example, you might create a blank check to record a check that has been damaged and can't be used for payment.</span></span>

<span data-ttu-id="8da33-106">Puslapyje **„Čekiai“** atliekamos čekių priežiūros užduotys.</span><span class="sxs-lookup"><span data-stu-id="8da33-106">On the **Checks** page, you perform maintenance tasks for checks.</span></span> <span data-ttu-id="8da33-107">Pavyzdžiui, galite kurti naujus čekių numerius ir naikinti čekius.</span><span class="sxs-lookup"><span data-stu-id="8da33-107">For example, you can create new check numbers and delete checks.</span></span> <span data-ttu-id="8da33-108">Taip pat galite kurti čekius, kurių būsena **Tuščia**.</span><span class="sxs-lookup"><span data-stu-id="8da33-108">You can also create checks that have a status of **Blank**.</span></span> <span data-ttu-id="8da33-109">Sukūrus tuščius čekius, jų negalima naikinti ar pakartotinai naudoti sistemoje.</span><span class="sxs-lookup"><span data-stu-id="8da33-109">After blank checks are created, they can't be deleted or reused in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="8da33-110">Ši funkcija pasiekiama puslapyje **„Čekiai“** tik įjungus funkciją **„Kurti čekius, kurių būsena Tuščia puslapyje „Kurti čekius“** puslapyje **Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="8da33-110">This feature is available on the **Checks** page only if you turn on the **Create checks with a blank status on the Checks page** feature on the **Feature management** page.</span></span> <span data-ttu-id="8da33-111">Jei funkcija neįjungta, čekiai, kurių būsena **Tuščia**, gali būti kuriami tik naudojant dialogo langą **Mokėjimas čekiu** mokėjimų generavimo proceso metu Mokėtinose sumose.</span><span class="sxs-lookup"><span data-stu-id="8da33-111">If the feature isn't turned on, checks that have **Blank** status can be created only from the **Payment by check** dialog box during the payment generation process in Accounts payable.</span></span>

<span data-ttu-id="8da33-112">Norėdami atidaryti puslapį **Čekiai**, eikite į skirtuką **Grynųjų pinigų ir banko valdymas \> Banko sąskaitos \> Banko sąskaitos**, tada skirtuko **Valdyti mokėjimus** srityje „Veiksmas“ grupėje **Susijusi informacija** pasirinkite **Čekiai**.</span><span class="sxs-lookup"><span data-stu-id="8da33-112">To open the **Checks** page, go to **Cash and bank management \> Bank accounts \> Bank accounts**, and then, on the Action Pane, on the **Manage payments** tab, in the **Related information** group, select **Checks**.</span></span> <span data-ttu-id="8da33-113">Arba eikite į skirtuką **Grynųjų pinigų ir banko valdymas \> Užklausos ir ataskaitos \> Čekiai**.</span><span class="sxs-lookup"><span data-stu-id="8da33-113">Alternatively, go to **Cash and bank management \> Inquiries and reports \> Checks**.</span></span>

<span data-ttu-id="8da33-114">Tada, norėdami sukurti čekius, kurių būsena **Tuščia**, srityje „Veiksmas“ pasirinkite **Kurti tuščius čekius**.</span><span class="sxs-lookup"><span data-stu-id="8da33-114">Then, to create checks that have **Blank** status, on the Action Pane, select **Create blank checks**.</span></span> <span data-ttu-id="8da33-115">Kol sistemoje kuriami tušti čekiai, susieta banko sąskaita laikinai yra neaktyvi.</span><span class="sxs-lookup"><span data-stu-id="8da33-115">While the system is creating blank checks, the associated bank account is temporarily inactivated.</span></span> <span data-ttu-id="8da33-116">Taip sumažinama rizika, kad mokėjimai bus sugeneruoti tuo pačiu metu, kai bus sukurti tušti čekiai.</span><span class="sxs-lookup"><span data-stu-id="8da33-116">This behavior reduces the risk that payments will be generated at the same time that blank checks are created.</span></span> <span data-ttu-id="8da33-117">Kai apdorojimas baigiamas, susieta banko sąskaita iš naujo aktyvinama.</span><span class="sxs-lookup"><span data-stu-id="8da33-117">When the processing is completed, the associated bank account is reactivated.</span></span>
