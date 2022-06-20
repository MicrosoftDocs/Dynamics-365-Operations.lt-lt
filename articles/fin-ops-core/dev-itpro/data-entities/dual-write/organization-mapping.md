---
title: Organizacijos hierarchija Dataverse
description: Šiame straipsnyje aprašomas organizacijos duomenų integravimas tarp finansų ir operacijų programėlių ir Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a4edaf5b9c50e9d8781ff703328ac786d71ee782
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884738"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organizacijos hierarchija Dataverse

[!include [banner](../../includes/banner.md)]



Kadangi "Dynamics 365 Financial" yra finansinė sistema, *organizacija* yra pagrindinė sąvoka, o sistemos nustatymas prasideda konfigūravimu pagal organizacijos hierarchiją. Verslo finansai gali būti stebimi organizacijos lygiu ir taip pat bet kuriuo organizacijos hierarchijos lygiu.

Nors „Dataverse“ neturi organizacijos hierarchijos sąvokos, joje yra kelios laisvos sąvokos, pvz., visų pardavimo įplaukos. Kaip „Dataverse“ integravimo dalis, organizacijos hierarchijos duomenų struktūra įtraukiamą į „Dataverse“

## <a name="data-flow"></a>Duomenų srautas

Verslo ekosistema, kurią sudaro „Finance and Operations“ programos ir „Dataverse“, toliau turės organizacijos hierarchiją. Ši organizacijos hierarchija pagrįsta „Finance and Operations“ programomis, tačiau ji rodoma programoje „Dataverse“ informaciniais ir išplėtimo tikslais. Toliau pateiktame paveikslėlyje pavaizduota organizacijos hierarchijos informacija, kuri rodoma programoje „Dataverse” kaip vienpusis duomenų srautas iš „Finance and Operations“ programų į „Dataverse”.

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
