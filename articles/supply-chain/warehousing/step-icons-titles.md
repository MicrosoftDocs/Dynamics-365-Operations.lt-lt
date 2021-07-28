---
title: „Warehouse Management” mobiliųjų įrenginių programėlės veiksmų piktogramų ir pavadinimų priskyrimas
description: Šioje temoje aprašoma, kaip priskirti veiksmų piktogramas ir pavadinimus naujiems ar pritaikytiems užduočių srautams „Warehouse Management” mobiliųjų įrenginių programėlėje.
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a74847b50512d2f712e5a9a5125e520afc732591
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344500"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a>„Warehouse Management” mobiliųjų įrenginių programėlės veiksmų piktogramų ir pavadinimų priskyrimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip priskirti veiksmų piktogramas ir veiksmų pavadinimus naujiems ar pritaikytiems užduočių srautams „Warehouse Management” mobiliųjų įrenginių programėlėje.

Toliau pateikti pavyzdžiai rodo, kaip veiksmų piktogramos ir pavadinimai rodomi „Warehouse Management” mobiliųjų įrenginių programėlėje.

![Veiksmo piktogramos ir veiksmo pavadinimo pavyzdys „Warehouse Management” mobiliųjų įrenginių programėlėje.](media/step-icon-example.png "Veiksmo piktogramos ir veiksmo pavadinimo pavyzdys „Warehouse Management” mobiliųjų įrenginių programėlėje")

## <a name="turn-on-this-feature-in-your-system"></a>Funkcijos įjungimas jūsų sistemoje

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [Funkcijos valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) nustatymus tam, kad patikrintų funkcijos būseną ir ją įjungtų. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Sandėlio valdymas*
- **Funkcijos pavadinimas:** *Naujos sandėlio programos vartotojo parametrai, piktogramos ir veiksmų pavadinimai*

## <a name="standard-step-ids-classes-and-icons"></a>Standartinės veiksmo ID, klasės ir piktogramos

Kiekvienas užduočių srauto veiksmas identifikuojamas pagal veiksmo ID, o kiekvieno veiksmo ID turi atitinkamą veiksmo klasę. Veiksmo piktograma ir pavadinimas yra nurodyti kiekvienoje veiksmo klasėje.

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a>Veiksmų ID ir veiksmų klasės

Toliau esančioje lentelėje pateikiama kiekvieno šiuo metu prieinamo veiksmo ID ir atitinkama veiksmo klasė. Pirminio įvesties lauko valdiklio pavadinimas yra naudojamas kaip veiksmo ID.

Pavyzdį, kuriame parodyta, kaip naudojamos šios veiksmų ID ir klasės, rasite „`WHSMobileAppStepInfoBuilder.stepId()`” metodo diegimo straipsnyje [Pavyzdys: Pasirinktinio srauto veiksmų piktogramų ir pavadinimų priskyrimas](#example), pateiktame toliau šioje temoje.

| Veiksmo ID | Veiksmo klasė |
|-|-|
| „BatchDisposition” | „WHSMobileAppStepBatchDisposition” |
| Vežėjas | „WHSMobileAppStepCarrier” |
| „CatchWeight” | „WHSMobileAppStepCatchWeight” |
| „CatchWeightQtyOutboundWeight” | „WHSMobileAppStepCatchWeight” |
| „CatchWeightTag” | „WHSMobileAppStepCatchWeightTag” |
| „CatchWeightTagWeight” | „WHSMobileAppStepCatchWeightTagWeight” |
| „ChangeWarehouseSuccess” | „WHSMobileAppStepChangeWarehouseSuccess” |
| „CheckDigit” | „WHSMobileAppStepCheckDigit” |
| „ClusterId” | „WHSMobileAppStepClusterId” |
| „ClusterPickQtyVerification” | „WHSMobileAppStepQtyVerification” |
| „ClusterPosition” | „WHSMobileAppStepClusterPosition” |
| „ConfigId” | „WHSMobileAppStepConfigId” |
| Patvirtinimas | „WHSMobileAppStepConfirmation” |
| „ConsolidateFromLicensePlateId” | „WHSMobileAppStepConsolidateFromLicensePlateId” |
| „ConsolidateLPConfirmation” | „WHSMobileAppStepConsolidateLPConfirmation” |
| „ConsolidateToLicensePlateId” | „WHSMobileAppStepConsolidateToLicensePlateId” |
| „ContainerType” | „WHSMobileAppStepContainerType” |
| „CountingReasonCode” | „WHSMobileAppStepCountingReasonCode” |
| „CycleCountingAddLPOrFinish” | „WHSMobileAppStepCycleCountingAddLPOrFinish” |
| „CycleCountQty1” | „WHSMobileAppStepCycleCountQty” |
| „CycleCountQty2” | „WHSMobileAppStepCycleCountQty” |
| „CycleCountQty3” | „WHSMobileAppStepCycleCountQty” |
| „CycleCountQty4” | „WHSMobileAppStepCycleCountQty” |
| Perdavimas | „WHSMobileAppStepDisposition” |
| „DriverCheckInConfirmation” | „WHSMobileAppStepDriverCheckInConfirmation” |
| „DriverCheckInId” | „WHSMobileAppStepDriverCheckInId” |
| „DriverCheckOutConfirmation” | „WHSMobileAppStepDriverCheckOutConfirmation” |
| „DriverCheckOutId” | „WHSMobileAppStepDriverCheckOutId” |
| „ExpDate” | „WHSMobileAppStepExpDate” |
| „FromBatchDisposition” | „WHSMobileAppStepFromBatchDisposition” |
| „FromInventoryStatus” | „WHSMobileAppStepInventoryStatusFrom” |
| „FullQty” | „WHSMobileAppStepFullQty” |
| „InboundPut” | „WHSMobileAppStepInboundPut” |
| „InventBatchId” | „WHSMobileAppStepBatch” |
| „InventColorId” | „WHSMobileAppStepInventColorId” |
| „InventLocation” | „WHSMobileAppStepInventLocation” |
| „InventLocationId” | „WHSMobileAppStepWarehouse” |
| „InventSerialId” | „WHSMobileAppStepInventSerialId” |
| „InventSizeId” | „WHSMobileAppStepInventSizeId” |
| „InventStatusId” | „WHSMobileAppStepInventStatus” |
| „InventStyleId” | „WHSMobileAppStepInventStyleId” |
| „InventVersionId” | „WHSMobileAppStepInventVersionId” |
| „ItemId” | „WHSMobileAppStepItem” |
| „ITMContainerID” | „ITMMobileAppStepContainerId” |
| „ITMShipmentID” | „ITMMobileAppStepShipmentId” |
| „KanbanCardId” | „WHSMobileAppStepKanbanCard” |
| „KanbanCardToEmpty” | „WHSMobileAppStepKanbanCardToEmpty” |
| „KanbanOrCardId” | „WHSMobileAppStepKanbanCard” |
| „LicensePlateId” | „WHSMobileAppStepLicensePlate” |
| „LoadId” | „WHSMobileAppStepLoadId” |
| „LocationLicensePlatePosition” | „WHSMobileAppStepLocationLicensePlatePosition” |
| „LocOrLP” | „WHSMobileAppStepLocOrLP” |
| „LocOrLP_From” | „WHSMobileAppStepLocOrLPFrom” |
| „LocOrLP_To” | „WHSMobileAppStepLocOrLPTo” |
| „LocOrLPCheck” | „WHSMobileAppStepLocOrLPCheck” |
| „LocVerification” | „WHSMobileAppStepLocVerification” |
| „LPAdjustIn” | „WHSMobileAppStepLPAdjustIn” |
| „LPBreakChildLP” | „WHSMobileAppStepLPBreakChildLP” |
| „LPBreakParentLP” | „WHSMobileAppStepLPBreakParentLP” |
| „LPBuildChildLP” | „WHSMobileAppStepLPBuildChildLP” |
| „LPBuildParentLP” | „WHSMobileAppStepLPBuildParentLP” |
| „LPVerification” | „WHSMobileAppStepLPVerification” |
| „MergeContainerId” | „WHSMobileAppStepMergeContainerId” |
| „MixedLPLineNum” | „WHSMobileAppStepMixedLPLineNum” |
| „MobileDeviceQueueMessageCollectionIdentifierId” | „WHSMobileAppStepSelectOrder” |
| „MovementConfirmCancel” | „WHSMobileAppStepMovementConfirmCancel” |
| „NewCaptureWeight” | „WHSMobileAppStepCatchWeight” |
| „NewQty” | „WHSMobileAppStepNewQty” |
| „OutboundCatchWeightTag” | „WHSMobileAppStepCatchWeightTag” |
| „OutboundPut” | „WHSMobileAppStepOutboundPut” |
| „OutboundWeight” | „WHSMobileAppStepCatchWeight” |
| „OverridePutNewLocation” | „WHSMobileAppStepOverridePutNewLocation” |
| „PieceByPieceConfirmation” | „WHSMobileAppStepQtyVerification” |
| „POLineNum” | „WHSMobileAppStepPOLineNum” |
| PU numeris | „WHSMobileAppStepPONum” |
| „PositionFull” | „WHSMobileAppStepPositionFull” |
| „PositionFullQty” | „WHSMobileAppStepPositionFullQty” |
| Stiprumas | „WHSMobileAppStepPotency” |
| „PrinterName” | „WHSMobileAppStepPrinterName” |
| „ProdId” | „WHSMobileAppStepProdId” |
| „ProdLastPalletConfirmation” | „WHSMobileAppStepProdLastPalletConfirmation” |
| „ProductConfirmation” | „WHSMobileAppStepProductConfirmation” |
| „ProductionScrapConfirmation” | „WHSMobileAppStepProductionScrapConfirmation” |
| Dėti | „WHSMobileAppStepPut” |
| „PutawayClusterId” | „WHSMobileAppStepPutawayClusterId” |
| Kiekis | „WHSMobileAppStepQty” |
| „QtyAdjust” | „WHSMobileAppStepQtyAdjust” |
| „QtyShort” | „WHSMobileAppStepQtyShort” |
| „QtyToConsume” | „WHSMobileAppStepQtyToConsume” |
| „QtyToPick” | „WHSMobileAppStepQtyToPick” |
| „QtyToPut” | „WHSMobileAppStepQtyToPut” |
| „QtyToScrap” | „WHSMobileAppStepQtyToScrap” |
| „QtyVerification” | „WHSMobileAppStepQtyVerification” |
| „QtyWithScanningLimit” | „WHSMobileAppStepQtyAdjust” |
| „ReasonString” | „WHSMobileAppStepReasonString” |
| „RecvLocationId” | „WHSMobileAppStepRecvLocationId” |
| „RemoveContainerId” | „WHSMobileAppStepRemoveContainerId” |
| „ReprintLabelConfirmation” | „WHSMobileAppStepReprintLabelConfirmation” |
| „RMANum” | „WHSMobileAppStepRMANum” |
| „ShortPickReason” | „WHSMobileAppStepShortPickReason” |
| „SortConOrLP” | „WHSMobileAppStepSortConOrLP” |
| „SortLicensePlateId” | „WHSMobileAppStepSortLicensePlateId” |
| „SortPositionId” | „WHSMobileAppStepSortPositionId” |
| „SortVerification” | „WHSMobileAppStepSortVerification” |
| „StartLocationId” | „WHSMobileAppStepStartLocationId” |
| „StartProdOrderConfirmation” | „WHSMobileAppStepStartProdOrderConfirmation” |
| „TargetLicensePlateId” | „WHSMobileAppStepTargetLicensePlateId” |
| „TOLineNum” | „WHSMobileAppStepTOLineNum” |
| „ToLocation” | „WHSMobileAppStepToLocation” |
| „TONum” | „WHSMobileAppStepTONum” |
| „ToWarehouse” | „WHSMobileAppStepWarehouseTo” |
| „TransportLoadId” | „WHSMobileAppStepTransportLoadId” |
| „WaveLabelId” | „WHSMobileAppStepWaveLabelId” |
| „WaveLblQty” | „WHSMobileAppStepWaveLblQty” |
| Svoris | „WHSMobileAppStepWeight” |
| „WeightToConsume” | „WHSMobileAppStepWeightToConsume” |
| „WHSAdjustmentType” | „WHSMobileAppStepWHSAdjustmentType” |
| „WHSReceivingException” | „WHSMobileAppStepWHSReceivingException” |
| „WHSWorkException” | „WHSMobileAppStepWHSWorkException” |
| „WHSWorkLicensePlateId” | „WHSMobileAppStepWorkLicensePlateId” |
| „WMSLocationId” | „WHSMobileAppStepLocation” |
| „WorkId” | „WHSMobileAppStepWorkId” |
| „WorkIdToCancel” | „WHSMobileAppStepWorkIdToCancel” |
| „WorkLPIdPutawayCluster” | „WHSMobileAppStepWorkLPIdPutawayCluster” |
| „WorkPoolId” | „WHSMobileAppStepWorkPoolId” |
| „ZoneId” | „WHSMobileAppStepZoneId” |

### <a name="available-step-icons"></a><a name="step-icons"></a>Galimos veiksmų piktogramos

Sistemoje yra standartinių veiksmų piktogramų, kurias taip pat galite naudoti atlikdami pasirinktinius veiksmus, rinkinys. Šiuo metu negalite įkelti pasirinktinių veiksmų piktogramų. Todėl visada turite pasirinkti vieną iš standartinių veiksmų piktogramų.

Šioje lentelėje rodoma kiekviena šiuo metu prieinama standartinė veiksmo piktograma ir jos pavadinimas.

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Apie veiksmo piktogramą"><br>Apie</td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Numerio lentelės įtraukimo arba prekės veiksmo piktograma"><br>„AddLpOrItem”</td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Paketų perdavimo veiksmo piktograma"><br>„BatchDisposition”</td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Vežėjo veiksmo piktograma"><br>Vežėjas</td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Esamo svorio žymės veiksmo piktograma"><br>„CatchWeightTag”</td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Esamo svorio žymės svorio veiksmo piktograma"><br>„CatchWeightTagWeight”</td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Skaitmens tikrinimo veiksmo piktograma"><br>„CheckDigit”</td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Įsiregistravimo arba išsiregistravimo ID veiksmo piktograma"><br>„CheckInOutId”</td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Antrinės numerio lentelės veiksmo piktograma"><br>„ChildLP”</td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Klasterio ID veiksmo piktograma"><br>„ClusterId”</td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Klasterio padėties veiksmo piktograma"><br>„ClusterPosition”</td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Konfigūracijos ID veiksmo piktograma"><br>„ConfigId”</td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Sukonfigūruoto lauko veiksmo piktograma"><br>„ConfiguredField”</td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Konfigūravimo arba numerio lentelės veiksmo piktograma"><br>„ConOrLP”</td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Konsoliduoja iš numerio lentelės ID veiksmo piktogramos"><br>„ConsolidateFromLicensePlateID”</td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Konsoliduoja į numerio lentelės ID veiksmo piktogramą"><br>„ConsolidateToLicensePlateID”</td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Konteinerio tipo veiksmo piktograma"><br>„ContainerType”</td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Inventorizacijos veiksmo piktograma"><br>Inventorizacija</td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Inventorizacijos priežasties kodo veiksmo piktograma"><br>„CountingReasonCode”</td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Kilmės šalies kodo veiksmo piktograma"><br>„CountryOfOrigin”</td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Perdavimo veiksmo piktograma"><br>Perdavimas</td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Atlikto veiksmo piktograma"><br>Atlikta</td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Vairuotojo įsiregistravimo patvirtinimo veiksmo piktograma"><br>„DriverCheckInConfirmation”</td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Vairuotojo įsiregistravimo ID veiksmo piktograma"><br>„DriverCheckInId”</td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Vairuotojo išsiregistravimo ID veiksmo piktograma"><br>„DriverCheckOutId”</td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Galiojimo datos veiksmo piktograma"><br>„ExpDate”</td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Lauko veiksmo piktograma"><br>Laukas</td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Perdavimo iš paketo veiksmo piktograma"><br>„FromBatchDisposition”</td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Būsenos iš atsargų veiksmo piktograma"><br>„FromInventoryStatus”</td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="ID atributo veiksmo piktograma"><br>„IdAttribute”</td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Atsargų paketo ID veiksmo piktograma"><br>„InventBatchID”</td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Atsargų spalvos ID veiksmo piktograma"><br>„InventColorID”</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Atsargų vietos veiksmo piktograma"><br>„InventLocation”</td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Atsargų serijos ID veiksmo piktograma"><br>„InventSerialID”</td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Atsargų dydžio ID veiksmo piktograma"><br>„InventSizeID”</td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Atsargų būsenos ID veiksmo piktograma"><br>„InventStatusID”</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Atsargų stiliaus ID veiksmo piktograma"><br>„InventStyleID”</td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Atsargų versijos ID veiksmo piktograma"><br>„InventVersionID”</td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Prekės ID veiksmo piktograma"><br>„ItemID”</td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="ITM konteinerio ID veiksmo piktograma"><br>„ITMContainerID”</td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="ITM siuntos ID veiksmo piktograma"><br>„ITMShipmentID”</td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="„Kanban” kortelės ID veiksmo piktograma"><br>„KanbanCardID”</td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="„Kanban” arba kortelės ID veiksmo piktograma"><br>„KanbanOrCardID”</td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Numerio lentelės ID veiksmo piktograma"><br>„LicensePlateID”</td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Krovinio ID veiksmo piktograma"><br>„LoadId”</td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Vietos numerio lentelės padėties veiksmo piktograma"><br>„LocationLicensePlatePosition”</td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Vietos arba numerio lentelės veiksmo piktograma"><br>„LocOrLP”</td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Vietos arba numerio lentelės patikrinimo veiksmo piktograma"><br>„LocOrLPCheck”</td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Iš vietos arba numerio lentelės piktograma"><br>„LocOrLPFrom”</td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Į vietą arba numerio lentelę veiksmo piktograma"><br>„LocOrLPTo”</td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Užbaigto ilgo proceso piktograma"><br>„LongProcessCompleted”</td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="Numerio lentelės lūžio pirminės numerio lentelės veiksmo piktograma"><br>„LPBreakParentLP”</td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Konteinerių suliejimo ID veiksmo piktograma"><br>„MergeContainerId”</td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Mišrios numerio lentelės eilutės numerio veiksmo piktograma"><br>„MixedLPLineNum”</td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Siunčiamo svorio veiksmo piktograma"><br>„OutboundWeight”</td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Savininko veiksmo piktograma"><br>Savininkas</td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Pirminės numerio lentelės veiksmo piktograma"><br>„ParentLP”</td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Patvirtinkite veiksmo piktogramą"><br>„PleaseConfirm”</td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Pirkimo užsakymo eilutės numerio veiksmo piktograma"><br>„POLineNum”</td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Pirkimo užsakymo numerio veiksmo piktograma"><br>PU numeris</td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Pilnos padėties veiksmo piktograma"><br>„PositionFull”</td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Stiprumo veiksmo piktograma"><br>Stiprumas</td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Spausdintuvo pavadinimo veiksmo piktograma"><br>„PrinterName”</td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Gamybos ID veiksmo piktograma"><br>„ProdId”</td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Produkto patvirtinimo veiksmo piktograma"><br>„ProductConfirmation”</td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Padėjimo veiksmo piktograma"><br>Dėti</td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Atidėjimo klasterio ID veiksmo piktograma"><br>„PutawayClusterId”</td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Kiekio veiksmo piktograma"><br>Kiekis</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Kiekio koregavimo veiksmo piktograma"><br>„QtyAdjustIn”</td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Nevisiškai paimto kiekio veiksmo piktograma"><br>„QtyShort”</td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Suvartotino kiekio veiksmo piktograma"><br>„QtyToConsume”</td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Atidėtino kiekio veiksmo piktograma"><br>„QtyToPut”</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Nurašytino kiekio veiksmo piktograma"><br>„QtyToScrap”</td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Kiekio patvirtinimo veiksmo piktograma"><br>„QuantityConfirmation”</td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Paskelbimo apie baigtą užduotį veiksmo piktograma"><br>„RAFEndJob”</td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Vietos gavimo ID veiksmo piktograma"><br>„RecvLocationID”</td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Konteinerių šalinimo ID veiksmo piktograma"><br>„RemoveContainerID”</td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="RMA numerio veiksmo piktograma"><br>„RMANum”</td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Užsakymo pasirinkimo veiksmo piktograma"><br>„SelectOrder”</td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Nevisiško paėmimo priežasties veiksmo piktograma"><br>„ShortPickReason”</td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Rikiavimo padėties ID veiksmo piktograma"><br>„SortPositionId”</td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Tikslinės numerio lentelės ID veiksmo piktograma"><br>„TargetLicensePlateId”</td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Į eilutės numerį veiksmo piktograma"><br>„ToLineNum”</td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Į vietą veiksmo piktograma"><br>„ToLocation”</td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Į numerį veiksmo piktograma"><br>„ToNum”</td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Į sandėlį veiksmo piktograma"><br>„ToWarehouse”</td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Krovinio transportavimo ID veiksmo piktograma"><br>„TransportLoadId”</td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Tiekėjo paketo ID veiksmo piktograma"><br>„VendBatchId”</td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Bangos žymos ID veiksmo piktograma"><br>„WaveLabelId”</td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Bangos žymos kiekio veiksmo piktograma"><br>„WaveLblQty”</td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Svorio veiksmo piktograma"><br>Svoris</td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Suvartotino svorio veiksmo piktograma"><br>„WeightToConsume”</td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="WHS koregavimo tipo veiksmo piktograma"><br>„WHSAdjustmentType”</td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="WHS gavimo išimties veiksmo piktograma"><br>„WHSReceivingException”</td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="WMS vietos ID veiksmo piktograma"><br>„WMSLocationID”</td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Darbo ID veiksmo piktograma"><br>„WorkId”</td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Atšauktino darbo ID veiksmo piktograma"><br>„WorkIdToCancel”</td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Darbo numerio lentelės ID veiksmo piktograma"><br>„WorkLicensePlateId”</td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Darbo numerio lentelės atidėjimo klasterio ID veiksmo piktograma"><br>„WorkLPIDPutawayCluster”</td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Darbo telkinio ID veiksmo piktograma"><br>„WorkPoolID”</td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Zonos ID veiksmo piktograma"><br>„ZoneID”</td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a>Pavyzdys: Priskirkite pasirinktinio srauto veiksmų piktogramas ir pavadinimus

Šiame pavyzdyje paaiškinama, kaip nustatyti pasirinktinio užduočių srauto veiksmų piktogramas ir pavadinimus. Scenarijus yra sukurtas pagal pasirinktinio užduočių srauto pavyzdį, kuris yra pateiktas ir išsamiau ištyrinėtas šiame tinklaraščio skelbime: [Sandėliavimo mobiliųjų įrenginių programėlės tinkinimas](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app). Užduočių srautas veikia toliau nurodytu būdu:

1. Programoje rodomas puslapis, kuriame darbuotojas paraginamas pateikti konteinerio ID (pavyzdžiui, nuskaitant brūkšninį kodą).
1. Jei konteinerio ID tinkamas, programa atidaro naują puslapį, kuriame darbuotojas yra paraginamas įvesti informaciją apie svorį. (Jei konteinerio ID netinkamas, darbuotojas grąžinamas į pirmąjį puslapį.)
1. Kai darbuotojas įveda tinkamą svorį, sistema išsaugo svorį ir grąžina darbuotoją į pirmąjį puslapį.

Toliau pateiktoje iliustracijoje vaizduojamas šis užduoties srautas.

![Užduoties srauto diagrama.](media/step-icons-example-task-flow.png "Užduoties srauto diagrama")

### <a name="create-a-step-class-for-the-container-input-page"></a>Veiksmo klasės kūrimas konteinerio įvesties puslapiui

Konteinerio įvesties puslapis leidžia darbuotojui nuskaityti arba įvesti konteinerio ID.

![Konteinerio įvesties puslapis.](media/step-icons-example-container-input.png "Konteinerio įvesties puslapis")

Konteinerio įvesties puslapyje įvesties lauko valdiklio pavadinimas yra „`ContainerId`”. Kadangi šio valdiklio pavadinimo nėra [veiksmų ID sąraše](#step-ids-classes), nerasite juo pagrįsto esamo veiksmo. Todėl turite sukurti veiksmo klasę, atspindinčią veiksmą. Toliau pateikiamas pavyzdys.

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

Veiksmo piktogramos identifikatorius yra saugomas „`defaultStepIcon`” klasės nariui, o veiksmo pavadinimas yra saugomas „`defaultStepTitle`” klasės nariui.

Norėdami priskirti veiksmo piktogramą, nustatykite „`defaultStepIcon`” į vieną iš piktogramos ID, išvardytų skyriuje [Galimos veiksmų piktogramos](#step-icons), esančiame anksčiau šioje temoje.

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a>Standartinės arba pasirinktinės veiksmo piktogramos ir pavadinimo naudojimas svorio įvesčiai

Svorio įvesties puslapis leidžia darbuotojui įvesti svorį.

![Svorio įvesties puslapis.](media/step-icons-example-weight-input.png "Svorio įvesties puslapis")

Svorio įvesties puslapio įvesties lauko valdiklio pavadinimas yra „`Weight`”, kuris yra [veiksmų ID sąraše](#step-ids-classes). Todėl, jei jums priimtini veiksmo piktograma ir pavadinimas, apibrėžti „`WHSMobileAppStepWeight`” klasėje, šiame veiksme jums nereikia nieko keisti.

Tačiau, jei norite naudoti kitą šio veiksmo piktogramą ar pavadinimą, galite pakeisti „`stepId()`” arba „`stepInfo()`” metodą daryklės klasėje. Kiekvienas užduočių srautas turi savo veiksmų informacijos daryklę.

#### <a name="override-the-stepid-method"></a>Metodo „stepId()” keitimas

Toliau pateiktame pavyzdyje parodomas vienas būdas, kuriuo galite modifikuoti daryklės klasę, pakeisdami „`stepId()`” metodą.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

Tada sukuriate veiksmo klasę „`NewWeight`” veiksmui. Kodas turėtų būti panašus į „`ContainerId`” pavyzdžio kodą, parodytą anksčiau šioje temoje.

#### <a name="override-the-stepinfo-method"></a>Metodo „stepInfo()” keitimas

Toliau pateiktame pavyzdyje parodomas vienas būdas, kuriuo galite modifikuoti daryklės klasę, pakeisdami „`stepInfo()`” metodą.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

Tada sukonstruojate „`WHSMobileAppStepInfo`” objektą ir tiesiogiai nustatote piktogramą ir (arba) pavadinimą.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Sandėlio valdymo mobiliųjų įrenginių programėlės diegimas ir prijungimas](install-configure-warehouse-management-app.md)
- [Mobiliojo įrenginio naudotojo nustatymai](mobile-device-user-settings.md)
