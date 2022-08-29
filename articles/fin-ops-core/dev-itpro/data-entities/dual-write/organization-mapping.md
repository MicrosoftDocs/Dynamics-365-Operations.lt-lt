---
title: Organizacijos hierarchija Dataverse
description: Šiame straipsnyje aprašomas organizacijos duomenų integravimas tarp finansų ir operacijų programėlių ir Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 48533dd104f62080d0ebd47389a4a829c772db13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289053"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organizacijos hierarchija Dataverse

[!include [banner](../../includes/banner.md)]



Kadangi "Dynamics 365 Financial" yra finansinė sistema, *organizacija* yra pagrindinė sąvoka, o sistemos nustatymas prasideda konfigūravimu pagal organizacijos hierarchiją. Verslo finansai gali būti stebimi organizacijos lygiu ir taip pat bet kuriuo organizacijos hierarchijos lygiu.

Nors „Dataverse“ neturi organizacijos hierarchijos sąvokos, joje yra kelios laisvos sąvokos, pvz., visų pardavimo įplaukos. Kaip „Dataverse“ integravimo dalis, organizacijos hierarchijos duomenų struktūra įtraukiamą į „Dataverse“

## <a name="data-flow"></a>Duomenų srautas

Verslo veiksmų, kuriuos sudaro finansų ir operacijų programėlių ir Dataverse toliau bus organizacijos hierarchija, kūrimas. Ši organizacijos hierarchija kuriama remiantis finansų ir operacijų programėle, Dataverse bet ji pateikiama informaciniais ir extensibility tikslais. Toliau pateikta iliustracija rodo organizacijos hierarchijos informaciją, kuri Dataverse rodoma kaip vien way data flow iš finansų ir operacijų programėlių į Dataverse.

![Struktūros vaizdas.](media/dual-write-data-flow.png)

Organizacijos hierarchijos lentelių schemas galima vienu būdu sinchronizuoti duomenis iš finansų ir operacijų programėlių į Dataverse.

## <a name="templates"></a>Šablonai

Organizacija yra grupė žmonių, kurie dirba kartu vykdydami verslo procesą arba siekdami tikslo. Organizacijos hierarchijos nurodo ryšius tarp organizacijų, kurios sudaro jūsų verslą. Galima nurodyti šių tipų vidines organizacijas: juridinius subjektus, valdymo vienetus ir komandas. Kaip parodyta pateiktoje lentelėje, sukuriamas lentelių žemėlapių rinkinys, skirtas sinchronizuoti juridinius subjektus, valdymo vienetą, s ir susijusią organizacijos hierarchijos informaciją.

„Finance and operations” programos | „Customer engagement“ programos     | Aprašymas
-----------------------|--------------------------------|---
[Juridiniai subjektai](mapping-reference.md#102) | cdm_companies | 
[Juridiniai subjektai](mapping-reference.md#142) | msdyn_internalorganizations |
[Valdymo vienetas](mapping-reference.md#143) | msdyn_internalorganizations |
[Organizacijos hierarchija – publikuota](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti lentelę Organizacijos hierarchija publikuota.
[Organizacijos hierarchijos tikslai](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti lentelę Organizacijos hierarchijos paskirtis.
[Organizacijos hierarchijos tipas](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti lentelę Organizacijos hierarchijos tipas.

## <a name="internal-organization"></a>Vidinė organizacija

Vidinės organizacijos informacija „Dataverse“ platformoje gaunama iš dviejų lentelių – **Valdymo vieneto** ir **Juridinių subjektų**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

