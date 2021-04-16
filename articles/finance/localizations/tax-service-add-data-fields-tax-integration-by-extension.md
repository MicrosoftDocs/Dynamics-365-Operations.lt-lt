---
title: Įtraukti duomenų laukus į mokesčių integravimą naudojant plėtinius
description: Šioje temoje paaiškinama, kaip naudoti X++ plėtinius norint įtraukti duomenų laukus į mokesčių integravimą.
author: qire
ms.date: 03/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fdf112bbdd5245d19ab1d07cfcf94c58bf8208c5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830345"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a><span data-ttu-id="ead97-103">Įtraukti duomenų laukus į mokesčių integravimą naudojant plėtinį</span><span class="sxs-lookup"><span data-stu-id="ead97-103">Add data fields in the tax integration by using extension</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="ead97-104">Šioje temoje paaiškinama, kaip naudoti X++ plėtinius norint įtraukti duomenų laukus į mokesčių integravimą.</span><span class="sxs-lookup"><span data-stu-id="ead97-104">This topic explains how to use X++ extensions to add data fields in the tax integration.</span></span> <span data-ttu-id="ead97-105">Šiuos laukus galima išplėsti iki mokesčių tarnybos mokesčių duomenų modelio ir naudoti mokesčių kodams nustatyti.</span><span class="sxs-lookup"><span data-stu-id="ead97-105">These fields can be extended to the tax data model of the tax service and used to determine tax codes.</span></span> <span data-ttu-id="ead97-106">Daugiau informacijos ieškokite Mokesčių [konfigūracijų duomenų laukų](tax-service-add-data-fields-tax-configurations.md) įtraukimas.</span><span class="sxs-lookup"><span data-stu-id="ead97-106">For more information, see [Add data fields in tax configurations](tax-service-add-data-fields-tax-configurations.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="ead97-107">Duomenų modelis</span><span class="sxs-lookup"><span data-stu-id="ead97-107">Data model</span></span>

<span data-ttu-id="ead97-108">Duomenų modelio duomenis vykdo objektai ir su įdiegė klasės.</span><span class="sxs-lookup"><span data-stu-id="ead97-108">The data in the data model is carried by objects and implemented by classes.</span></span>

<span data-ttu-id="ead97-109">Toliau pateiktas pagrindinių objektų sąrašas:</span><span class="sxs-lookup"><span data-stu-id="ead97-109">Here is a list of the major objects:</span></span>

* <span data-ttu-id="ead97-110">AxClass /TaxIntegration **dokumento** objektas</span><span class="sxs-lookup"><span data-stu-id="ead97-110">AxClass/TaxIntegration **Document** Object</span></span>
* <span data-ttu-id="ead97-111">AxClass /TaxIntegration **Eilutės** objektas</span><span class="sxs-lookup"><span data-stu-id="ead97-111">AxClass/TaxIntegration **Line** Object</span></span>
* <span data-ttu-id="ead97-112">AxClass /TaxIntegration **Mokesčių eilutės** objektas</span><span class="sxs-lookup"><span data-stu-id="ead97-112">AxClass/TaxIntegration **TaxLine** Object</span></span>

<span data-ttu-id="ead97-113">Šioje iliustracijoje parodyta, kaip šie objektai yra susiję.</span><span class="sxs-lookup"><span data-stu-id="ead97-113">The following illustration shows how these objects are related.</span></span>

<span data-ttu-id="ead97-114">[![Duomenų modelio objekto ryšys](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span><span class="sxs-lookup"><span data-stu-id="ead97-114">[![Data model object relationship](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span></span>

<span data-ttu-id="ead97-115">Dokumento **objekte** gali būti **daug eilutės** objektų.</span><span class="sxs-lookup"><span data-stu-id="ead97-115">A **Document** object can contain many **Line** objects.</span></span> <span data-ttu-id="ead97-116">Kiekviename objekte yra mokesčių tarnybos metaduomenys.</span><span class="sxs-lookup"><span data-stu-id="ead97-116">Each object contains metadata for the tax service.</span></span>

- <span data-ttu-id="ead97-117">`TaxIntegrationDocumentObject` yra `originAddress` metaduomenų, kuriuose yra informacijos apie šaltinio adresą ir `includingTax` metaduomenis, kurie nurodo, ar eilutės suma apima PVM.</span><span class="sxs-lookup"><span data-stu-id="ead97-117">`TaxIntegrationDocumentObject` has `originAddress` metadata, which contains information about the source address, and `includingTax` metadata, which indicates whether the line amount includes sales tax.</span></span>
- <span data-ttu-id="ead97-118">`TaxIntegrationLineObject` yra `itemId`, `quantity` ir `categoryId` metaduomenys.</span><span class="sxs-lookup"><span data-stu-id="ead97-118">`TaxIntegrationLineObject` has `itemId`, `quantity`, and `categoryId` metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="ead97-119">`TaxIntegrationLineObject` taip pat įdiegia **mokesčio** objektus.</span><span class="sxs-lookup"><span data-stu-id="ead97-119">`TaxIntegrationLineObject` also implements **Charge** objects.</span></span>

## <a name="integration-flow"></a><span data-ttu-id="ead97-120">integravimo eiga</span><span class="sxs-lookup"><span data-stu-id="ead97-120">Integration flow</span></span>

<span data-ttu-id="ead97-121">Srauto duomenis valdo veikla.</span><span class="sxs-lookup"><span data-stu-id="ead97-121">The data in the flow is manipulated by activities.</span></span>

### <a name="key-activities"></a><span data-ttu-id="ead97-122">Pagrindinės veiklos</span><span class="sxs-lookup"><span data-stu-id="ead97-122">Key activities</span></span>

* <span data-ttu-id="ead97-123">AxClass /TaxIntegration **skaičiavimo** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="ead97-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span></span>
* <span data-ttu-id="ead97-124">AxClass /TaxIntegration **valiutos kursas** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="ead97-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span></span>
* <span data-ttu-id="ead97-125">AxClass /TaxIntegration **duomenų išlikimas** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="ead97-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span></span>
* <span data-ttu-id="ead97-126">AxClass /TaxIntegration **duomenų gavimas** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="ead97-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span></span>
* <span data-ttu-id="ead97-127">AxClass /TaxIntegration **nustatymų gavimas** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="ead97-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span></span>

<span data-ttu-id="ead97-128">Veiklos yra paleidžiamos tokia tvarka:</span><span class="sxs-lookup"><span data-stu-id="ead97-128">Activities are run in the following order:</span></span>

1. <span data-ttu-id="ead97-129">Nustatomas nuskaitimas</span><span class="sxs-lookup"><span data-stu-id="ead97-129">Setting Retrieval</span></span>
2. <span data-ttu-id="ead97-130">Duomenų nuskaitymas</span><span class="sxs-lookup"><span data-stu-id="ead97-130">Data Retrieval</span></span>
3. <span data-ttu-id="ead97-131">Skaičiavimo tarnyba</span><span class="sxs-lookup"><span data-stu-id="ead97-131">Calculation Service</span></span>
4. <span data-ttu-id="ead97-132">Valiutos kursas</span><span class="sxs-lookup"><span data-stu-id="ead97-132">Currency Exchange</span></span>
5. <span data-ttu-id="ead97-133">Duomenų pastovumas</span><span class="sxs-lookup"><span data-stu-id="ead97-133">Data Persistence</span></span>

<span data-ttu-id="ead97-134">Pavyzdžiui, **pratęskite duomenų** nuskaitymą prieš skaičiavimo **paslaugas**.</span><span class="sxs-lookup"><span data-stu-id="ead97-134">For example, extend **Data Retrieval** before **Calculation Service**.</span></span>

#### <a name="data-retrieval-activities"></a><span data-ttu-id="ead97-135">Duomenų gavimo veiklos</span><span class="sxs-lookup"><span data-stu-id="ead97-135">Data Retrieval activities</span></span>

<span data-ttu-id="ead97-136">**Duomenų** nuskaityme nuskaitomi duomenys iš duomenų bazės.</span><span class="sxs-lookup"><span data-stu-id="ead97-136">**Data Retrieval** activities retrieve data from the database.</span></span> <span data-ttu-id="ead97-137">Skirtingų operacijų adapterius galima nuskaityti duomenis iš skirtingų operacijų lentelių:</span><span class="sxs-lookup"><span data-stu-id="ead97-137">Adapters for different transactions are available to retrieve data from different transaction tables:</span></span>

- <span data-ttu-id="ead97-138">AxClass/TaxIntegration **Įsigijimo lentelė** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ead97-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span></span>
- <span data-ttu-id="ead97-139">AxClass/TaxIntegration **„PurchParmTable“** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ead97-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span></span>
- <span data-ttu-id="ead97-140">AxClass/TaxIntegration **„PurchREQTable“** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ead97-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span></span>
- <span data-ttu-id="ead97-141">AxClass/TaxIntegration **„PurchRFQTable“** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ead97-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span></span>
- <span data-ttu-id="ead97-142">AxClass/TaxIntegration **„VendInvoiceInfoTable“** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ead97-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span></span>
- <span data-ttu-id="ead97-143">AxClass/TaxIntegration **„SalesTable“** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ead97-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span></span>
- <span data-ttu-id="ead97-144">AxClass/TaxIntegration **„SalesParm“** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="ead97-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span></span>

<span data-ttu-id="ead97-145">Šiose duomenų **nuskaityme** duomenys kopijuojami iš duomenų bazės į `TaxIntegrationDocumentObject` ir `TaxIntegrationLineObject`.</span><span class="sxs-lookup"><span data-stu-id="ead97-145">In these **Data Retrieval** activities, data is copied from the database to `TaxIntegrationDocumentObject` and `TaxIntegrationLineObject`.</span></span> <span data-ttu-id="ead97-146">Kadangi visos šios veiklos išplečia tą pačią abstrakčią šablono klasę, jos turi bendrus metodus.</span><span class="sxs-lookup"><span data-stu-id="ead97-146">Because all these activities extend the same abstract template class, they have common methods.</span></span>

#### <a name="calculation-service-activities"></a><span data-ttu-id="ead97-147">Apskaičiavimo paslaugų veikla</span><span class="sxs-lookup"><span data-stu-id="ead97-147">Calculation Service activities</span></span>

<span data-ttu-id="ead97-148">Skaičiavimo **paslaugos veikla yra sąsaja tarp mokesčių tarnybos ir mokesčių** integravimo.</span><span class="sxs-lookup"><span data-stu-id="ead97-148">The **Calculation Service** activity is the link between the tax service and the tax integration.</span></span> <span data-ttu-id="ead97-149">Ši veikla yra atsakinga už šias funkcijas:</span><span class="sxs-lookup"><span data-stu-id="ead97-149">This activity is responsible for the following functions:</span></span>

1. <span data-ttu-id="ead97-150">Kurti užklausą.</span><span class="sxs-lookup"><span data-stu-id="ead97-150">Construct the request.</span></span>
2. <span data-ttu-id="ead97-151">Užregistruokite užklausą mokesčių tarnybai.</span><span class="sxs-lookup"><span data-stu-id="ead97-151">Post the request to the tax service.</span></span>
3. <span data-ttu-id="ead97-152">Gauti atsakymą iš mokesčių tarnybos.</span><span class="sxs-lookup"><span data-stu-id="ead97-152">Get the response from the tax service.</span></span>
4. <span data-ttu-id="ead97-153">Atmesti atsakymą.</span><span class="sxs-lookup"><span data-stu-id="ead97-153">Parse the response.</span></span>

<span data-ttu-id="ead97-154">Duomenų laukas, kurį įtraukiate į užklausą, bus registruojamas kartu su kitais metaduomenimis.</span><span class="sxs-lookup"><span data-stu-id="ead97-154">A data field that you add to the request will be posted together with other metadata.</span></span> 

## <a name="extension-implementation"></a><span data-ttu-id="ead97-155">Plėtinio diegimas</span><span class="sxs-lookup"><span data-stu-id="ead97-155">Extension implementation</span></span>

<span data-ttu-id="ead97-156">Šiame skyriuje pateikiami išsamūs veiksmai, paaiškinays, kaip įdiegti plėtinį.</span><span class="sxs-lookup"><span data-stu-id="ead97-156">This section provides detailed steps that explain how to implement the extension.</span></span> <span data-ttu-id="ead97-157">Jis naudoja išlaidų **centrą ir projekto finansines** **dimensijas** kaip pavyzdžius.</span><span class="sxs-lookup"><span data-stu-id="ead97-157">It uses the **Cost center** and **Project** financial dimensions as examples.</span></span>

### <a name="step-1-add-the-data-variable-in-the-object-class"></a><span data-ttu-id="ead97-158">1 veiksmas.</span><span class="sxs-lookup"><span data-stu-id="ead97-158">Step 1.</span></span> <span data-ttu-id="ead97-159">Įtraukti duomenų kintamąjį į objektų klasę</span><span class="sxs-lookup"><span data-stu-id="ead97-159">Add the data variable in the object class</span></span>

<span data-ttu-id="ead97-160">Objekto klasėje yra duomenų kintamųjų ir getterių/seter metodų.</span><span class="sxs-lookup"><span data-stu-id="ead97-160">The object class contains the data variable and getter/setter methods for the data.</span></span> <span data-ttu-id="ead97-161">Priklausomai nuo lauko lygio, `TaxIntegrationDocumentObject` duomenų ar `TaxIntegrationLineObject`, lauką įtraukite į jį arba į jį.</span><span class="sxs-lookup"><span data-stu-id="ead97-161">Add the data field to either `TaxIntegrationDocumentObject` or `TaxIntegrationLineObject`, depending on the level of the field.</span></span> <span data-ttu-id="ead97-162">Toliau pavyzdyje naudojamas eilutės lygis, o failo vardas `TaxIntegrationLineObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="ead97-162">The following example uses the line level, and the file name is `TaxIntegrationLineObject_Extension.xpp`.</span></span>

> [!NOTE]
> <span data-ttu-id="ead97-163">Jei duomenų laukas, kurį pridedate, yra dokumento lygyje, pakeiskite failo vardą į `TaxIntegrationDocumentObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="ead97-163">If the data field that you're adding is at the document level, change the file name to `TaxIntegrationDocumentObject_Extension.xpp`.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

<span data-ttu-id="ead97-164">**Išlaidų centras** ir projektas įtraukiami kaip privačios **kintamieji**.</span><span class="sxs-lookup"><span data-stu-id="ead97-164">**Cost center** and **Project** are added as private variables.</span></span> <span data-ttu-id="ead97-165">Sukurkite šių duomenų laukų getterio ir nustatymo metodus duomenims valdyti.</span><span class="sxs-lookup"><span data-stu-id="ead97-165">Create getter and setter methods for these data fields to manipulate the data.</span></span>

### <a name="step-2-retrieve-data-from-the-database"></a><span data-ttu-id="ead97-166">2 veiksmas.</span><span class="sxs-lookup"><span data-stu-id="ead97-166">Step 2.</span></span> <span data-ttu-id="ead97-167">Nuskaityti duomenis iš duomenų bazės</span><span class="sxs-lookup"><span data-stu-id="ead97-167">Retrieve data from the database</span></span>

<span data-ttu-id="ead97-168">Nurodykite operaciją ir pratęskite atitinkamas adapterio klases, kad gautumėte duomenis.</span><span class="sxs-lookup"><span data-stu-id="ead97-168">Specify the transaction, and extend the appropriate adapter classes to retrieve the data.</span></span> <span data-ttu-id="ead97-169">Pavyzdžiui, jei naudojate pirkimo užsakymo **operaciją**, turite išplėsti `TaxIntegrationPurchTableDataRetrieval` ir `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="ead97-169">For example, if you use a **Purchase order** transaction, you must extend `TaxIntegrationPurchTableDataRetrieval` and `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span></span> 

> [!NOTE]
> <span data-ttu-id="ead97-170">`TaxIntegrationPurchParmTableDataRetrieval` yra paveldėta iš `TaxIntegrationPurchTableDataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="ead97-170">`TaxIntegrationPurchParmTableDataRetrieval` is inherited from `TaxIntegrationPurchTableDataRetrieval`.</span></span> <span data-ttu-id="ead97-171">Jos keisti negalima, nebent skiriasi `purchTable` lentelių ir lentelių `purchParmTable` logika.</span><span class="sxs-lookup"><span data-stu-id="ead97-171">It should not be changed unless the logic of the `purchTable` and `purchParmTable` tables differs.</span></span>

<span data-ttu-id="ead97-172">Jei duomenų laukas turi būti pridėtas prie visų operacijų, išplėskite visas `DataRetrieval` klases.</span><span class="sxs-lookup"><span data-stu-id="ead97-172">If the data field should be added for all transactions, extend all `DataRetrieval` classes.</span></span>

<span data-ttu-id="ead97-173">Kadangi visos **duomenų** nuskaitymos veiklos išplečia tą pačią šablono klasę, klasių struktūros, kintamieji ir metodai yra panašūs.</span><span class="sxs-lookup"><span data-stu-id="ead97-173">Because all **Data Retrieval** activities extend the same template class, the class structures, variables, and methods are similar.</span></span>

```X++
protected TaxIntegrationDocumentObject document;

/// <summary>
/// Copies to the document.
/// </summary>
protected abstract void copyToDocument()
{
    // It is recommended to implement as:
    //
    // this.copyToDocumentByDefault();
    // this.copyToDocumentFromHeaderTable();
    // this.copyAddressToDocument();
}
 
/// <summary>
/// Copies to the current line of the document.
/// </summary>
/// <param name = "_line">The current line of the document.</param>
protected abstract void copyToLine(TaxIntegrationLineObject _line)
{
    // It is recommended to implement as:
    //
    // this.copyToLineByDefault(_line);
    // this.copyToLineFromLineTable(_line);
    // this.copyQuantityAndTransactionAmountToLine(_line);
    // this.copyAddressToLine(_line);
    // this.copyToLineFromHeaderTable(_line);
}
```

<span data-ttu-id="ead97-174">Šiame pavyzdyje parodyta pagrindinė struktūra, `PurchTable` kai naudojama lentelė.</span><span class="sxs-lookup"><span data-stu-id="ead97-174">The following example shows the basic structure when the `PurchTable` table is used.</span></span>

```X++
public class TaxIntegrationPurchTableDataRetrieval extends TaxIntegrationAbstractDataRetrievalTemplate
{
    protected PurchTable purchTable;
    protected PurchLine purchLine;

    // Query builder methods
    [Replaceable]
    protected SysDaQueryObject getDocumentQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineQueryObject()
    [Replaceable]
    protected SysDaQueryObject getDocumentChargeQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineChargeQueryObject()

    // Data retrieval methods
    protected void copyToDocument()
    protected void copyToDocumentFromHeaderTable()
    protected void copyToLine(TaxIntegrationLineObject _line)
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    ...
}
```

<span data-ttu-id="ead97-175">`CopyToDocument` Iškvietus metodą, `this.purchTable` buferis jau yra.</span><span class="sxs-lookup"><span data-stu-id="ead97-175">When the `CopyToDocument` method is called, the `this.purchTable` buffer already exists.</span></span> <span data-ttu-id="ead97-176">Šio metodo paskirtis yra kopijuoti visus reikiamus duomenis iš objekto naudojant klasėje sukurtą `this.purchTable` į `document` `DocumentObject` metodą.</span><span class="sxs-lookup"><span data-stu-id="ead97-176">The purpose of this method is to copy all the required data from `this.purchTable` to the `document` object by using the setter method that was created in the `DocumentObject` class.</span></span>

<span data-ttu-id="ead97-177">Taip pat šis metodas `this.purchLine` jau yra `CopyToLine` buferis.</span><span class="sxs-lookup"><span data-stu-id="ead97-177">Likewise, a `this.purchLine` buffer already exists in the `CopyToLine` method.</span></span> <span data-ttu-id="ead97-178">Šio metodo paskirtis yra kopijuoti visus reikiamus duomenis iš objekto naudojant klasėje sukurtą `this.purchLine` į `_line` `LineObject` metodą.</span><span class="sxs-lookup"><span data-stu-id="ead97-178">The purpose of this method is to copy all the required data from `this.purchLine` to the `_line` object by using the setter method that was created in the `LineObject` class.</span></span>

<span data-ttu-id="ead97-179">Pats tiesiausias būdas yra išplėsti `CopyToDocument` ir `CopyToLine` metodus.</span><span class="sxs-lookup"><span data-stu-id="ead97-179">The most straightforward approach is to extend the `CopyToDocument` and `CopyToLine` methods.</span></span> <span data-ttu-id="ead97-180">Tačiau pirmiausia rekomenduojame išbandyti `copyToDocumentFromHeaderTable` ir `copyToLineFromLineTable` metodus.</span><span class="sxs-lookup"><span data-stu-id="ead97-180">However, we recommend that you try the `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable` methods first.</span></span> <span data-ttu-id="ead97-181">Jei jie neveikia taip, kaip jums reikia, įtinkite savo metodą ir iškieskite `CopyToDocument` ir `CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="ead97-181">If they don't work as you require, implement your own method, and call it in `CopyToDocument` and `CopyToLine`.</span></span> <span data-ttu-id="ead97-182">Yra trys bendrosios situacijos, kuriose galite naudoti šį būdą:</span><span class="sxs-lookup"><span data-stu-id="ead97-182">There are three common situations where you might use this approach:</span></span>

- <span data-ttu-id="ead97-183">Būtinas laukas yra `PurchTable` arba `PurchLine`.</span><span class="sxs-lookup"><span data-stu-id="ead97-183">The required field is in `PurchTable` or `PurchLine`.</span></span> <span data-ttu-id="ead97-184">Tokiu atveju galite išplėsti `copyToDocumentFromHeaderTable` ir `copyToLineFromLineTable`.</span><span class="sxs-lookup"><span data-stu-id="ead97-184">In this situation, you can extend `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable`.</span></span> <span data-ttu-id="ead97-185">Čia yra pavyzdžio kodas.</span><span class="sxs-lookup"><span data-stu-id="ead97-185">Here is the sample code.</span></span>

    ```X++
    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        next copyToLineFromLineTable(_line);
        // if we already added XXX in TaxIntegrationLineObject
        _line.setXXX(this.purchLine.XXX);
    }
    ```

- <span data-ttu-id="ead97-186">Reikalaujami duomenys nėra numatytoje operacijos lentelėje.</span><span class="sxs-lookup"><span data-stu-id="ead97-186">The required data isn't in the default table of the transaction.</span></span> <span data-ttu-id="ead97-187">Tačiau kai kurie ryšiai su numatytąja lentele yra sujungti, o lauką reikia naudoti daugelyje eilučių.</span><span class="sxs-lookup"><span data-stu-id="ead97-187">However, there are some join relationships with the default table, and the field is required on most lines.</span></span> <span data-ttu-id="ead97-188">Tokiu atveju pakeiskite lentelę `getDocumentQueryObject` arba `getLineObject` pateikite užklausą dėl ryšio sujungtų ryšių.</span><span class="sxs-lookup"><span data-stu-id="ead97-188">In this situation, replace `getDocumentQueryObject` or `getLineObject` to query the table by join relationship.</span></span> <span data-ttu-id="ead97-189">Šiame pavyzdyje laukas **Pristatyti dabar yra** integruotas su pardavimo užsakymu eilutės lygiu.</span><span class="sxs-lookup"><span data-stu-id="ead97-189">In the following example, the **Deliver Now** field is integrated with the sales order at the line level.</span></span>

    ```X++
    public class TaxIntegrationSalesTableDataRetrieval
    {
        protected MCRSalesLineDropShipment mcrSalesLineDropShipment;

        /// <summary>
        /// Gets the query for the lines of the document.
        /// </summary>
        /// <returns>The query for the lines of the document</returns>
        [Replaceable]
        protected SysDaQueryObject getLineQueryObject()
        {
            return SysDaQueryObjectBuilder::from(this.salesLine)
                .where(this.salesLine, fieldStr(SalesLine, SalesId)).isEqualToLiteral(this.salesTable.SalesId)
                .outerJoin(this.mcrSalesLineDropShipment)
                .where(this.mcrSalesLineDropShipment, fieldStr(MCRSalesLineDropShipment, SalesLine)).isEqualTo(this.salesLine, fieldStr(SalesLine, RecId))
                .toSysDaQueryObject();
        }
    }
    ```

    <span data-ttu-id="ead97-190">Šiame pavyzdyje `mcrSalesLineDropShipment` buferis paskelbiamas ir užklausa apibrėžiama `getLineQueryObject`.</span><span class="sxs-lookup"><span data-stu-id="ead97-190">In this example, a `mcrSalesLineDropShipment` buffer is declared, and the query is defined in `getLineQueryObject`.</span></span> <span data-ttu-id="ead97-191">Užklausa naudoja `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`ryšį.</span><span class="sxs-lookup"><span data-stu-id="ead97-191">The query uses the relationship `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span></span> <span data-ttu-id="ead97-192">Kol išplečiate šią situaciją, galite pakeisti savo `getLineQueryObject` sudaryti užklausos objektą.</span><span class="sxs-lookup"><span data-stu-id="ead97-192">While you're extending in this situation, you can replace `getLineQueryObject` with your own constructed query object.</span></span> <span data-ttu-id="ead97-193">Tačiau atminkite tolesnius taškus:</span><span class="sxs-lookup"><span data-stu-id="ead97-193">However, note the following points:</span></span>

    * <span data-ttu-id="ead97-194">Kadangi yra metodo grąžinama `getLineQueryObject` vertė, turite `SysDaQueryObject` sudaryti šį objektą naudodami SysDa būdą.</span><span class="sxs-lookup"><span data-stu-id="ead97-194">Because the return value of the `getLineQueryObject` method is `SysDaQueryObject`, you must construct this object by using the SysDa approach.</span></span>
    * <span data-ttu-id="ead97-195">Negalima pašalinti buvusios lentelės.</span><span class="sxs-lookup"><span data-stu-id="ead97-195">Can't remove existed table.</span></span>

- <span data-ttu-id="ead97-196">Reikiami duomenys sudėtingu sujungimo ryšiu yra susiję su operacijų lentele arba ryšys nėra vienas su vienu (1:1), o su daugeliu (1:N).</span><span class="sxs-lookup"><span data-stu-id="ead97-196">The required data is related to the transaction table by a complicated join relationship, or the relation isn't one to one (1:1) but one to many (1:N).</span></span> <span data-ttu-id="ead97-197">Šioje situacijoje dalykai tampa šiek tiek sudėtingi.</span><span class="sxs-lookup"><span data-stu-id="ead97-197">In this situation, things become a little complicated.</span></span> <span data-ttu-id="ead97-198">Ši situacija taikoma finansinių dimensijų pavyzdyje.</span><span class="sxs-lookup"><span data-stu-id="ead97-198">This situation applies to the example of financial dimensions.</span></span> 

    <span data-ttu-id="ead97-199">Tokiu atveju galite įdiegti savo metodą duomenims nuskaityti.</span><span class="sxs-lookup"><span data-stu-id="ead97-199">In this situation, you can implement your own method to retrieve the data.</span></span> <span data-ttu-id="ead97-200">Čia yra pavyzdžio kodas `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` faile.</span><span class="sxs-lookup"><span data-stu-id="ead97-200">Here is the sample code in the `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` file.</span></span>

    ```X++
    [ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
    final class TaxIntegrationPurchTableDataRetrieval_Extension
    {
        private const str CostCenterKey = 'CostCenter';
        private const str ProjectKey = 'Project';

        /// <summary>
        /// Copies to the current line of the document from.
        /// </summary>
        /// <param name = "_line">The current line of the document.</param>
        protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
        {
            Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
            if (dimensionAttributeMap.exists(CostCenterKey))
            {
                _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
            }
            if (dimensionAttributeMap.exists(ProjectKey))
            {
                _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
            }
            next copyToLineFromLineTable(_line);
        }
        private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
        {
            DimensionAttribute dimensionAttribute;
            DimensionAttributeValue dimensionAttributeValue;
            DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
            Map ret = new Map(Types::String, Types::String);

            select Name, RecId from dimensionAttribute
                join dimensionAttributeValue
                    where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
                join DimensionAttributeValueSetItem
                    where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                        && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;

            while(dimensionAttribute.RecId)
            {
                ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
                next dimensionAttribute;
            }
            return ret;
        }
    }
    ```

### <a name="step-3-add-data-to-the-request"></a><span data-ttu-id="ead97-201">3 veiksmas.</span><span class="sxs-lookup"><span data-stu-id="ead97-201">Step 3.</span></span> <span data-ttu-id="ead97-202">Įtraukti duomenis į užklausą</span><span class="sxs-lookup"><span data-stu-id="ead97-202">Add data to the request</span></span>

<span data-ttu-id="ead97-203">Išplėskite `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` arba `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` metodą, norėdami įtraukti duomenis į užklausą.</span><span class="sxs-lookup"><span data-stu-id="ead97-203">Extend the `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` or `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method to add data to the request.</span></span> <span data-ttu-id="ead97-204">Čia yra pavyzdžio kodas `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` faile.</span><span class="sxs-lookup"><span data-stu-id="ead97-204">Here is the sample code in the `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` file.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```

<span data-ttu-id="ead97-205">Šiuo kodu yra `_destination` viršelio objektas, naudojamas registruoti užklausai generuoti, `_source` ir yra `TaxIntegrationLineObject` objektas.</span><span class="sxs-lookup"><span data-stu-id="ead97-205">In this code, `_destination` is the wrapper object that is used to generate the post request, and `_source` is the `TaxIntegrationLineObject` object.</span></span> 

> [!NOTE]
> * <span data-ttu-id="ead97-206">Apibrėžkite raktą, kuris naudojamas užklausos formoje kaip `private const str`.</span><span class="sxs-lookup"><span data-stu-id="ead97-206">Define the key that is used in the request form as `private const str`.</span></span>
> * <span data-ttu-id="ead97-207">Naudodami metodą `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` nustatykite metodo `SetField` lauką.</span><span class="sxs-lookup"><span data-stu-id="ead97-207">Set the field in the `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method by using the `SetField` method.</span></span> <span data-ttu-id="ead97-208">Antrojo parametro duomenų tipas turi būti `string`.</span><span class="sxs-lookup"><span data-stu-id="ead97-208">The data type of the second parameter should be `string`.</span></span> <span data-ttu-id="ead97-209">Jei duomenų tipas ne, konvertuoti `string` į `string`.</span><span class="sxs-lookup"><span data-stu-id="ead97-209">If the data type isn't `string`, convert it to `string`.</span></span>

## <a name="appendix"></a><span data-ttu-id="ead97-210">Priedas</span><span class="sxs-lookup"><span data-stu-id="ead97-210">Appendix</span></span>

<span data-ttu-id="ead97-211">Šiame priede rodomas visas finansinių dimensijų (išlaidų centro ir projekto) integravimo eilutės lygiu **pavyzdžio** **kodas** .</span><span class="sxs-lookup"><span data-stu-id="ead97-211">This appendix shows the complete sample code for the integration of financial dimensions (**Cost center** and **Project**) at the line level.</span></span>

### <a name="taxintegrationlineobject_extensionxpp"></a><span data-ttu-id="ead97-212">TaxIntegrationLineObject_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="ead97-212">TaxIntegrationLineObject_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a><span data-ttu-id="ead97-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="ead97-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
final class TaxIntegrationPurchTableDataRetrieval_Extension
{
    private const str CostCenterKey = 'CostCenter';
    private const str ProjectKey = 'Project';

    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
        if (dimensionAttributeMap.exists(CostCenterKey))
        {
            _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
        }
        if (dimensionAttributeMap.exists(ProjectKey))
        {
            _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
        }
        next copyToLineFromLineTable(_line);
    }
    private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
    {
        DimensionAttribute dimensionAttribute;
        DimensionAttributeValue dimensionAttributeValue;
        DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
        Map ret = new Map(Types::String, Types::String);
        select Name, RecId from dimensionAttribute
            join dimensionAttributeValue
                where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
            join DimensionAttributeValueSetItem
                where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                    && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;
        while(dimensionAttribute.RecId)
        {
            ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
            next dimensionAttribute;
        }
        return ret;
    }
}
```

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a><span data-ttu-id="ead97-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="ead97-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```
