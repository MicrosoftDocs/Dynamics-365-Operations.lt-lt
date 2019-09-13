---
title: Integruotos svetainės ir sandėliai
description: Šioje temoje aprašoma svetainės ir sandėlio duomenų integracija tarp „Finance and Operations“ ir „Common Data Service“.
author: benebotg
manager: AnnBe
ms.date: 15/8/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 3ee5192138374c58df9f9cfc033503d200356771
ms.sourcegitcommit: 559637f30037f6b52ebc4d4c13d0ecec46d4a051
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/27/2019
ms.locfileid: "1920706"
---
# <a name="integrated-sites-and-warehouses"></a>Integruotos svetainės ir sandėliai

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Šioje temoje aprašoma svetainės ir sandėlio duomenų integracija tarp „Finance and Operations“ ir „Common Data Service“. Operatyviosios svetainės ir sandėliai yra bendrosios koncepcijos „Supply Chain Management“ programoje. Jie naudojami jūsų įmonės tiekimo grandinei modeliuoti.

## <a name="templates"></a>Šablonai

Kartu su „Common Data Service“ integracija, šios koncepcijos ir visa susijusi informacija yra pasiekiama programoje „Common Data Service“ naudojant svetainių ir sandėlių duomenų objektus toliau pateiktoje lentelėje.

„Finance and Operations”  | „Customer Engagement“ programa
--------------------------|---------------------------------
Svetainės                     | msdyn_operationalsites
Sandėliai                | sandėliai

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="operational-sites"></a>Operatyviosios svetainės

Operatyviosios svetainės pasiekiamos programoje „Common Data Service“ naudojant toliau pateiktus susiejimus.

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
Svetainės pavadinimas | >< | msdyn_name
Numatytoji finansinės dimensijos reikšmė | >< | msdyn_defaultfinancialdimensionvalue
Numatytasis atsargų būsenos ID | >< | msdyn_defaultinventorystatusid
Ar leidžiamas gavimo sandėlio perrašymas? | >< | msdyn_isreceivingwarehouseoverrideallowed
Svetainės ID | >< | msdyn_siteid
Svetainės pavadinimas | >< | msdyn_sitename
Mokesčių mokėtojo filialo kodas | >< | msdyn_taxbranchcode
Finansinio padalinio ID | >< | msdyn_fiscalestablishmentid
Ar pagrindinis adresas priskirtas? | >< | msdyn_isprimaryaddressassigned
PRIMARYADDRESSCITY | >< | msdyn_primaryaddresscity
PRIMARYADDRESSCOUNTRYREGIONID | >< | msdyn_primaryaddresscountryregionid
PRIMARYADDRESSCOUNTYID | >< | msdyn_primaryaddresscountyid
Pagrindinio adreso rajono pavadinimas | >< | msdyn_primaryaddressdistrictname
Pagrindinio adreso platuma | >< | msdyn_primaryaddresslatitude
Pagrindinio adreso vietos vaidmenys | >< | msdyn_primaryaddresslocationrole
Pagrindinio adreso vietos PVM grupės kodas | >< | msdyn_primaryaddresslocationsalestaxgroupcode
Pagrindinio adreso ilguma | >< | msdyn_primaryaddresslongitude
PRIMARYADDRESSSTATEID | >< | msdyn_primaryaddressstateid
PRIMARYADDRESSSTREET | >< | msdyn_primaryaddressstreet
PRIMARYADDRESSZIPCODE | >< | msdyn_primaryaddresszipcode
Pagrindinio adreso pastato papildoma informacija | >< | msdyn_primaryaddressbuildingcompliment
Pagrindinio adreso miesto „kana“ pavadinimas | >< | msdyn_primaryaddresscityinkana
Pagrindinio adreso gatvės „kana“ pavadinimas | >< | msdyn_primaryaddressstreetinkana
Pagrindinio adreso aprašas | >< | msdyn_primaryaddressdescription
FORMATTEDPRIMARYADDRESS | >< | msdyn_formattedprimaryaddress
Ar bendrai suplanuoti svetainės viduje vykstantys perkėlimai naudoja perdavimo žurnalus? | >< | msdyn_masterplannedusestransferjournal
Pagrindinio adreso pašto dėžutė | >< | msdyn_primaryaddresspostbox
Pagrindinio adreso gatvės numeris | >< | msdyn_primaryaddressstreetnumber


## <a name="warehouses"></a>Sandėliai

Sandėliai pasiekiami naudojant toliau pateiktus susiejimus.

Šaltinio laukas | Schemos tipas | Paskirties laukas
---|---|---
Numatytojo konteinerio tipo ID | >> | msdyn_defaultcontainertypeid
Ar prekių padengimas planuojamas rankiniu būdu? | >> | msdyn_areitemscoverageplannedmanually
Ar leistini darbo standartai? | >> | msdyn_arelaborstandardsallowed
Pagrindinio adreso pastato papildoma informacija | >> | msdyn_primaryaddressbuildingcompliment
Pagrindinio adreso pašto dėžutė | >> | msdyn_primaryaddresspostbox
Pagrindinio adreso gatvės numeris | >> | msdyn_primaryaddressstreetnumber
Ar sandėlio vietos kontrolinis numeris yra unikalus? | >> | msdyn_arewarehouselocationcheckdigitsunique
Atsargų skaičiavimo priežasties kodo strategijos pavadinimas | >> | msdyn_inventorycountingreasoncodepolicyname
Automatinio atnaujinimo siuntimo taisyklė | >> | msdyn_autoupdateshipmentrule
Sandėlio išleidimo rezervavimo reikalavimo taisyklė | >> | msdyn_warehousereleasereservationrequirement
Išorėje esančio sandėlio tiekėjo paskyros numeris | >> | msdyn_externallylocatedwarehousevendoraccountnu
Atsargų būsenos keitimo rezervavimo pašalinimo lygis | >> | msdyn_inventorystatuschangereservationremoval
Sandėlio darbo apdorojimo strategijos pavadinimas | >> | msdyn_warehouseworkprocessingpolicyname
Ar sandėlis apdorojamas? | >> | msdyn_isfallbackwarehouse
Ar leistinos finansinės neigiamos parduotuvės atsargos? | >> | msdyn_financialnegativestoreinventoryallowed
Ar leidžiamas padėklo perkėlimas ciklo skaičiavimo metu? | >> | msdyn_palletmovementduringcyclecountingallowed
Ar leidžiamos faktinės neigiamos parduotuvės atsargos? | >> | msdyn_physicalnegativestoreinventoryallowed
Papildymas iš pagrindinio sandėlio | >> | msdyn_isrefilledfrommainwarehouse
Parduotuvės sandėlis | >> | msdyn_isretailstorewarehouse
Pagrindinio papildymo sandėlio ID | >> | msdyn_mainrefillingwarehouseid.msdyn_warehouseid
Bendrojo planavimo darbo kalendoriaus ID | >> | msdyn_masterplanningworkcalendarid
Maksimalus paketo išrinkimo sąrašo kiekis | >> | msdyn_maximumbatchpickinglistquantity
Maksimalus išrinkimo sąrašo kiekis | >> | msdyn_maximumpickinglistlinequantity
Operatyviosios svetainės ID | >> | msdyn_operationalsiteid.msdyn_siteid
Sulaikymo sandėlio ID | >> | msdyn_quarantinewarehouseid.msdyn_warehouseid
Parduotuvės kiekio priskyrimo papildymo svorio taisyklė | > | msdyn_storeqtyallocationreplenishmentweight
Ar sandėlio vietos ID turi apimti perėjimo ID? | >> | msdyn_shouldwarehouselocationincludeaisleid
Tranzito sandėlio ID | >> | msdyn_transitwarehouseid.msdyn_warehouseid
Sandėlio ID | >> | msdyn_warehouseid
Sandėlio vietos ID talpyklos ID formatu | >> | msdyn_warehouselocationidbinidformat
Sandėlio vietos ID „rack ID“ formatu | >> | msdyn_warehouselocationidrackidformat
Sandėlio vietos ID „shelf ID“ formatu | >> | msdyn_warehouselocationidshelfidformat
Sandėlio pavadinimas | >> | msdyn_name
Sandėlio pavadinimas | >> | msdyn_warehousename
Sandėlio specialus numatytų atsargų būsenos ID | >> | msdyn_warehousespecificdefaultinventorystatusid
Sandėlio tipas | >> | msdyn_warehousetype
Ar pagrindinis adresas priskirtas? | >> | msdyn_isprimaryaddressassigned
PRIMARYADDRESSCITY | >> | msdyn_primaryaddresscity
PRIMARYADDRESSCOUNTRYREGIONID | >> | msdyn_primaryaddresscountryregionid
PRIMARYADDRESSCOUNTYID | >> | msdyn_primaryaddresscountyid
Pagrindinio adreso rajono pavadinimas | >> | msdyn_primaryaddressdistrictname
Pagrindinio adreso platuma | >> | msdyn_primaryaddresslatitude
Pagrindinio adreso ilguma | >> | msdyn_primaryaddresslongitude
Pagrindinio adreso vietos vaidmenys | >> | msdyn_primaryaddresslocationroles
Pagrindinio adreso vietos PVM grupės kodas | >> | msdyn_primaryaddresslocationsalestaxgroupcode
PRIMARYADDRESSSTATEID | >> | msdyn_primaryaddressstateid
PRIMARYADDRESSSTREET | >> | msdyn_primaryaddressstreet
PRIMARYADDRESSZIPCODE | >> | msdyn_primaryaddresszipcode
Išorėje esančio sandėlio kliento paskyros numeris | >> | msdyn_externallylocatedwarehousecustomeraccount
Pagrindinio adreso miesto „kana“ pavadinimas | >> | msdyn_primaryaddresscityinkana
Pagrindinio adreso gatvės „kana“ pavadinimas | >> | msdyn_primaryaddressstreetinkana
Pagrindinio adreso aprašas | >> | msdyn_primaryaddressdescription
Ar taikomi išplėstiniai sandėlio valdymo procesai? | >> | msdyn_uesadvancedwarehousemanagementprocesses
Išrinkimo sąrašų pristatymo specialus režimas | >> | msdyn_arepickinglistsdeliverymodespecific
AREPICKINGLISTSSHIPMENTSPECIFICONLY | >> | msdyn_arepickinglistshipmentspecificonly
FORMATTEDPRIMARYADDRESS | >> | msdyn_formattedprimaryaddress
Ar taikytinas važtaraščio spausdinimas prieš siuntimo patvirtinimą? | >> | msdyn_printbillofladingbeforeshipconfirmation
Žaliavų išrinkimo atsargų problemų būsena | >> | msdyn_rawmaterialpickinginventoryissuestatus
At automatinis krovinio išleidimas rezervuos atsargas? | >> | msdyn_willautomaticloadreleaseinventory
Ar atsargų būsenos keitimas pašalina blokavimą? | >> | msdyn_willinventorystatuschangeremoveblocking
Ar rankinis krovinio išleidimas rezervuos atsargas? | >> | msdyn_willmanualloadreleasereserveinventory
Ar užsakymo pateikimas konsoliduoja siuntimus? | >> | msdyn_willorderreleasingconsolidateshipments
Ar gamybos KS rezervuos tik sandėlio lygį? | >> | msdyn_productionbomsreservewarehouselevel
Ar siuntimo atšaukimas sumažins krovinio kiekį? | >> | msdyn_shippingcanceldecrementloadquantity
Ar sandėlio vietos ID apims talpyklos ID pagal numatytuosius nustatymus? | >> | msdyn_warehouselocationidincludeblindid
Ar sandėlio vietos ID apims „rack ID“ pagal numatytuosius nustatymus? | >> | msdyn_warehouselocationincluderackidbydefault
Ar sandėlio vietos ID apims „shelf ID“ pagal numatytuosius nustatymus? | >> | msdyn_warehouselocationidincludeshelfid
