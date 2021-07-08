---
title: Importuoti gaunamus ASN naudojant V2 duomenų objektą
description: Šioje temoje paaiškinama, kaip valdyti gaunamų išplėstinių siuntimo pranešimų (ASN) importavimą naudojant Gaunamų ASN V2 duomenų objektą.
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: WHSInboundASNV2Entity, WHSInboundASNEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 470cc0c39f211a5d0f106c4c6e193867388e2b53
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249141"
---
# <a name="import-inbound-asns-through-the-v2-data-entity"></a><span data-ttu-id="6ddae-103">Importuoti gaunamus ASN naudojant V2 duomenų objektą</span><span class="sxs-lookup"><span data-stu-id="6ddae-103">Import inbound ASNs through the V2 data entity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6ddae-104">Išplėstiniai siuntimo pranešimai (ASN) praneša jums apie tiekėjo pristatymus.</span><span class="sxs-lookup"><span data-stu-id="6ddae-104">Advanced shipping notices (ASNs) notify you about vendor deliveries.</span></span> <span data-ttu-id="6ddae-105">Jie padeda siuntėjui aprašyti siuntos turinį ir papildomą informaciją apie ją, pavyzdžiui, prekes ir pakuotę.</span><span class="sxs-lookup"><span data-stu-id="6ddae-105">They help the sender describe the contents of a shipment and additional information about it, such as the items and packaging.</span></span>

<span data-ttu-id="6ddae-106">ASN gali padėti sandėlio darbuotojams sužinoti, kada kas atvežama.</span><span class="sxs-lookup"><span data-stu-id="6ddae-106">ASNs can help warehouse workers learn what is arriving when.</span></span> <span data-ttu-id="6ddae-107">Todėl jie gali pasiruošti.</span><span class="sxs-lookup"><span data-stu-id="6ddae-107">Therefore, they can prepare.</span></span> <span data-ttu-id="6ddae-108">Be to, sandėlio darbuotojai gali naudoti ASN, kad siuntos informacija būtų suderinta su susijusiu pirkimo užsakymu, sukurtu anksčiau.</span><span class="sxs-lookup"><span data-stu-id="6ddae-108">In addition, warehouse workers can use ASNs to match the details of a shipment to the related purchase order that was previously created.</span></span>

<span data-ttu-id="6ddae-109">Šioje temoje pateikiamas scenarijų rinkinys, kuris pavyzdžiais parodo, kaip dirbti su ASN failais.</span><span class="sxs-lookup"><span data-stu-id="6ddae-109">This topic presents a collection of scenarios that show, through examples, how to work with ASN files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ddae-110">*Gaunamo ASN* importavimas taikomas tik toms prekėms, kurios yra įgalintos išplėstiniam sandėlio valdymui (WMS).</span><span class="sxs-lookup"><span data-stu-id="6ddae-110">*Inbound ASN* import applies only to items that are enabled for advanced warehouse management (WMS).</span></span> <span data-ttu-id="6ddae-111">Prieš gaudami ASN, sistemoje turi būti užregistruotas pirkimo užsakymas pagal tiekėją, kuris siunčia tą ASN.</span><span class="sxs-lookup"><span data-stu-id="6ddae-111">Before you receive an ASN, a purchase order must be registered in the system against the vendor who is sending that ASN.</span></span>

## <a name="inbound-asn-v2-entity"></a><span data-ttu-id="6ddae-112">Gaunamo ASN V2 objektas</span><span class="sxs-lookup"><span data-stu-id="6ddae-112">Inbound ASN V2 entity</span></span>

<span data-ttu-id="6ddae-113">Importuojate gaunamus ASN naudodami sudėtinį *Gaunamo ASN V2* duomenų objektą.</span><span class="sxs-lookup"><span data-stu-id="6ddae-113">You import inbound ASNs by using the *Inbound ASN V2* composite data entity.</span></span> <span data-ttu-id="6ddae-114">*Gaunamo ASN V2* naudojasi šiais objektais:</span><span class="sxs-lookup"><span data-stu-id="6ddae-114">*Inbound ASN V2* takes advantage of the following entities:</span></span>

- <span data-ttu-id="6ddae-115">Gaunamo krovinio antraštė</span><span class="sxs-lookup"><span data-stu-id="6ddae-115">Inbound load header</span></span>
- <span data-ttu-id="6ddae-116">Gaunamos siuntos antraštė</span><span class="sxs-lookup"><span data-stu-id="6ddae-116">Inbound shipment header</span></span>
- <span data-ttu-id="6ddae-117">Gaunamo krovinio pakavimo struktūros</span><span class="sxs-lookup"><span data-stu-id="6ddae-117">Inbound load packing structures</span></span>
- <span data-ttu-id="6ddae-118">Gaunamo krovinio pakavimo struktūros dėžės</span><span class="sxs-lookup"><span data-stu-id="6ddae-118">Inbound load packing structure cases</span></span>
- <span data-ttu-id="6ddae-119">Gaunamo krovinio pakavimo struktūros dėžių eilutės</span><span class="sxs-lookup"><span data-stu-id="6ddae-119">Inbound load packing structure case lines</span></span>
- <span data-ttu-id="6ddae-120">Gaunamo krovinio pakavimo struktūros eilutės</span><span class="sxs-lookup"><span data-stu-id="6ddae-120">Inbound load packing structure lines</span></span>

<span data-ttu-id="6ddae-121">Sudėtinis *Gaunamo ASN V2* duomenų objektas yra skirtas asinchroninio integravimo scenarijams, kuriuose naudojami XML failu pagrįsti importavimai.</span><span class="sxs-lookup"><span data-stu-id="6ddae-121">The *Inbound ASN V2* composite data entity is intended for asynchronous integration scenarios where XML file–based imports are used.</span></span>

## <a name="xml-format-for-importing-asns"></a><span data-ttu-id="6ddae-122">XML formatas ASN importavimui</span><span class="sxs-lookup"><span data-stu-id="6ddae-122">XML format for importing ASNs</span></span>

<span data-ttu-id="6ddae-123">„Microsoft Dynamics 365 Supply Chain Management” palaiko šį XML formatą ASN importavimui.</span><span class="sxs-lookup"><span data-stu-id="6ddae-123">Microsoft Dynamics 365 Supply Chain Management supports the following XML format for importing ASNs.</span></span> <span data-ttu-id="6ddae-124">Kiekvienas XML failo mazgas atspindi atributą iš atskiro objekto.</span><span class="sxs-lookup"><span data-stu-id="6ddae-124">Each node in the XML file represents an attribute from an individual entity.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV2Entity>
                    </WHSInboundPackingStructureCaseLineV2Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV2Entity>
                </WHSInboundLoadPackingStructureLineV2Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a><span data-ttu-id="6ddae-125">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="6ddae-125">Examples</span></span>

<span data-ttu-id="6ddae-126">Toliau pateikti poskyriai pateikia tiekėjo siuntų ASN XML importavimo failų pavyzdžius.</span><span class="sxs-lookup"><span data-stu-id="6ddae-126">The following subsections provide examples of ASN XML import files for vendor shipments.</span></span>

### <a name="example-1"></a><span data-ttu-id="6ddae-127">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="6ddae-127">Example 1</span></span>

<span data-ttu-id="6ddae-128">Šiame pavyzdyje rodomas tiekėjo siuntų importavimo XML failas, skirta vienam pirkimo užsakymui, kai neįtraukiama jokia atvejo informacija.</span><span class="sxs-lookup"><span data-stu-id="6ddae-128">The following example shows an XML file for importing vendor shipments for one purchase order when no case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a><span data-ttu-id="6ddae-129">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="6ddae-129">Example 2</span></span>

<span data-ttu-id="6ddae-130">Šiame pavyzdyje rodomas tiekėjo siuntų importavimo XML failas, skirta vienam pirkimo užsakymui, kai įtraukiama atvejo informacija.</span><span class="sxs-lookup"><span data-stu-id="6ddae-130">The following example shows an XML file for importing vendor shipments for one purchase order when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a><span data-ttu-id="6ddae-131">3 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="6ddae-131">Example 3</span></span>

<span data-ttu-id="6ddae-132">Šiame pavyzdyje rodomas tiekėjo siuntų importavimo XML failas, skirta keliems pirkimo užsakymams, kai įtraukiama atvejo informacija.</span><span class="sxs-lookup"><span data-stu-id="6ddae-132">The following example shows an XML file for importing vendor shipments for multiple purchase orders when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a><span data-ttu-id="6ddae-133">ASN failo importavimo rezultatų patikrinimas</span><span class="sxs-lookup"><span data-stu-id="6ddae-133">Inspect the results of importing an ASN file</span></span>

<span data-ttu-id="6ddae-134">Atlikite šiuos veiksmus norėdami patikrinti ASN failo importavimo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="6ddae-134">Follow these steps to inspect the results of importing an ASN file.</span></span>

1. <span data-ttu-id="6ddae-135">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="6ddae-135">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="6ddae-136">Suraskite ir atidarykite krovinį, kuris buvo sukurtas kaip ASN importavimo dalis.</span><span class="sxs-lookup"><span data-stu-id="6ddae-136">Find and open a load that was created as part of an ASN import.</span></span>
1. <span data-ttu-id="6ddae-137">„FastTab” **Krovinys** turėtumėte matyti reikšmes, pagrįstas XML failu.</span><span class="sxs-lookup"><span data-stu-id="6ddae-137">On the **Load** FastTab, you should see values that are based on the XML file.</span></span>
1. <span data-ttu-id="6ddae-138">„FastTab” **Krovinio eilutės** turėtumėte matyti pardavimo užsakymo numerius ir prekės informaciją, pagrįstus XML failu.</span><span class="sxs-lookup"><span data-stu-id="6ddae-138">On the **Load lines** FastTab, you should see purchase order numbers and item details that are based on the XML file.</span></span>
1. <span data-ttu-id="6ddae-139">Veiksmų srities skirtuko **Siųsti ir gauti** grupėje **Gauti** pasirinkite **Pakavimo struktūra**, kad peržiūrėtumėte krovinio pakavimo struktūrą.</span><span class="sxs-lookup"><span data-stu-id="6ddae-139">On the Action Pane, on the **Ship and receive** tab, in the **Receive** group, select **Packing structure** to review the packing structure of the load.</span></span>
1. <span data-ttu-id="6ddae-140">„FastTab” **Paletės** turėtumėte matyti numerio lenteles, pagrįstas XML failu.</span><span class="sxs-lookup"><span data-stu-id="6ddae-140">On the **Pallets** FastTab, you should see license plates that are based on the XML file.</span></span>
1. <span data-ttu-id="6ddae-141">„FastTab” **Atvejai** turėtumėte matyti atvejus, pagrįstus XML failu.</span><span class="sxs-lookup"><span data-stu-id="6ddae-141">On the **Cases** FastTab, you should see cases that are based on the XML file.</span></span>
1. <span data-ttu-id="6ddae-142">„FastTab” **Prekės** turėtumėte matyti prekes ir kiekius, pagrįstus XML failu.</span><span class="sxs-lookup"><span data-stu-id="6ddae-142">On the **Items** FastTab, you should see items and quantities that are based on the XML file.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
