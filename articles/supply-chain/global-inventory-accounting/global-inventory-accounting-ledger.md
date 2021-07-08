---
title: Visuotinės Atsargų Apskaitos didžioji knyga
description: Šioje temoje aprašomos Visuotinės atsargų apskaitos didžiosios knygos, kurias apibrėžia valiutos, kalendoriaus, konvencijos ir susiejimo su juridiniu subjektu derinys.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273196"
---
# <a name="global-inventory-accounting-ledger"></a><span data-ttu-id="3bf9f-103">Visuotinės Atsargų Apskaitos didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="3bf9f-103">Global Inventory Accounting ledger</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="3bf9f-104">Visuotinė atsargų apskaita turi savo didžiųjų knygų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-104">Global Inventory Accounting has its own set of ledgers.</span></span> <span data-ttu-id="3bf9f-105">Kiekvieną kartą, kai su atsargomis susijusi operacija apdorojama susijusiam juridiniam subjektui, sistema gali atlikti tos operacijos apskaitą tiek Visuotinės atsargų apskaitos didžiosiose knygose, kiek reikia.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-105">Each time an inventory-related transaction is processed for a relevant legal entity, the system can account for that transaction in any number of Global Inventory Accounting ledgers, as required.</span></span>

<span data-ttu-id="3bf9f-106">Didžioji knyga yra debeto ir kredito priemonių registras.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-106">A ledger is a register of debit and credit measures.</span></span> <span data-ttu-id="3bf9f-107">Šios priemonės klasifikuotos naudojant išlaidų elementus ir papildomos knygos sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-107">These measures are classified by using cost elements and subledger accounts.</span></span> <span data-ttu-id="3bf9f-108">Visuotinės atsargų apskaitos didžiąją knygą apibrėžia valiutos, kalendoriaus, konvencijos ir susiejimo su juridiniu subjektu derinys.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-108">A Global Inventory Accounting ledger is defined by its combination of a currency, a calendar, a convention, and an association with a legal entity.</span></span>

<span data-ttu-id="3bf9f-109">Norėdami nustatyti savo Visuotinės atsargų apskaitos didžiąsias knygas, eikite į **Visuotinį atsargų apskaita \> Nustatymas \> Visuotinės atsargų apskaitos didžiosios knygos**.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-109">To set up your Global Inventory Accounting ledgers, go to **Global inventory accounting \> Setup \> Global inventory accounting ledgers**.</span></span> <span data-ttu-id="3bf9f-110">Kiekvienai didžiajai knygai nustatykite toliau pateiktus laukus:</span><span class="sxs-lookup"><span data-stu-id="3bf9f-110">For each ledger, set the following fields:</span></span>

- <span data-ttu-id="3bf9f-111">**Pavadinimas** – įveskite didžiosios knygos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-111">**Name** – Enter the name of the ledger.</span></span>
- <span data-ttu-id="3bf9f-112">**Aprašas** – įveskite didžiosios knygos aprašą.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-112">**Description** – Enter a description of the ledger.</span></span>
- <span data-ttu-id="3bf9f-113">**Finansinis kalendorius** – Nurodykite didžiosios knygos finansinį kalendorių.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-113">**Fiscal calendar** – Specify the fiscal calendar for the ledger.</span></span>
- <span data-ttu-id="3bf9f-114">**Valiutos ir valiutos kurso tipas** – Norėdami pasirinkti didžiosios knygos naudojamą apskaitos valiutą ir valiutos kurso tipą naudokite šio „FastTab” laukus.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-114">**Currency and exchange rate type** – Use the fields on this FastTab to select the accounting currency that the ledger uses, and the exchange rate type.</span></span> <span data-ttu-id="3bf9f-115">Jūsų pasirinkta valiuta gali skirtis nuo juridinio subjekto naudojamos valiutos.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-115">The currency that you select can differ from the currency that the legal entity uses.</span></span> <span data-ttu-id="3bf9f-116">Visuotinėje atsargų apskaitoje vartotojai gali apibrėžti tiek įkainojimo didžiųjų knygų, kiek reikia.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-116">In Global Inventory Accounting, users can define as many costing ledgers as they require.</span></span> <span data-ttu-id="3bf9f-117">Visuotinė atsargų apskaita palaiko atsargų apskaitą keliomis valiutomis ir keliais vertinimais.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-117">Global Inventory Accounting supports inventory accounting in multiple currencies and in multiple valuations.</span></span> <span data-ttu-id="3bf9f-118">Užpildykite toliau nurodytus laukus:</span><span class="sxs-lookup"><span data-stu-id="3bf9f-118">Set the following fields:</span></span>

    - <span data-ttu-id="3bf9f-119">**Valiuta** – Pasirinkite įkainojimo valiutą, kuria tvarkomos su atsargomis susijusios vertės.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-119">**Currency** – Select the costing currency that inventory-related values are maintained in.</span></span> <span data-ttu-id="3bf9f-120">Šios vertės apima atsargų vertę, parduotų prekių savikainą, tranzito atsargas ir visų rūšių nuokrypius.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-120">These values include the inventory value, cost of goods sold, inventory in transit, and all kinds of variance.</span></span>
    - <span data-ttu-id="3bf9f-121">**Valiutos kurso tipas** – Pasirinkite valiutos kursą, kurį sistema turėtų naudoti operacijos sumai konvertuoti į operacijos valiutą ir standartinei prekių savikainai konvertuoti į įkainojimo valiutą.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-121">**Exchange rate type** – Select the exchange rate that the system should use to convert the transaction amount in the transaction currency and the standard cost of the items into the costing currency.</span></span>

- <span data-ttu-id="3bf9f-122">**Konvencijos pavadinimas** – Nurodykite konvenciją.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-122">**Convention name** – Specify a convention.</span></span> <span data-ttu-id="3bf9f-123">Konvencija yra strategijų, nustatančių kaip išlaidos bus apskaičiuotos šioje didžiojoje knygoje, rinkinys.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-123">A convention is a collection of policies that establish how costs will be accounted in this ledger.</span></span>
- <span data-ttu-id="3bf9f-124">**Juridinis subjektas** – Didžioji knyga surašys dokumentus, užregistruotus pasirinktame juridiniame subjekte.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-124">**Legal entity** – The ledger will account the documents that are posted to the selected legal entity.</span></span>
- <span data-ttu-id="3bf9f-125">**Turto valdymas** – Pasirinkite, ar atsargų operacijos, sukurtos prieš didžiosios knygos sukūrimą, turėtų būti apdorojamos pagal didžiosios knygos valiutą ir konvenciją.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-125">**Priming** – Select whether inventory transactions that were created before the ledger was created should be processed according to the currency and convention in the ledger.</span></span> <span data-ttu-id="3bf9f-126">Pasirinkite vieną iš šių reikšmių:</span><span class="sxs-lookup"><span data-stu-id="3bf9f-126">Select one of the following values:</span></span>

    - <span data-ttu-id="3bf9f-127">**Suaktyvinta** – Didžioji knyga turi apdoroti operacijas, kurios buvo sukurtos prieš didžiosios knygos sukūrimą.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-127">**Activated** – The ledger should process transactions that were created before the ledger was created.</span></span>
    - <span data-ttu-id="3bf9f-128">**Išjungta** – Didžioji knyga turi apdoroti tik tas operacijas, kurios bus sukurtos po didžiosios knygos sukūrimo.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-128">**Deactivated** – The ledger should process only transactions that are created after the ledger was created.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="3bf9f-129">Jūs **negalėsite** grįžti ir nustatyti šio lauko po to, kai įvesite naujus dokumentus.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-129">You will **not** be able to come back and set this field after you enter new documents.</span></span>

- <span data-ttu-id="3bf9f-130">**Būsena** – Sistema automatiškai nustato naujai sukurtų didžiųjų knygų būseną į *Paruošti*.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-130">**Status** – The system automatically sets the status of newly created ledgers to *Prepare*.</span></span>
