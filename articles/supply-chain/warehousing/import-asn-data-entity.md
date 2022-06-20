---
title: Importuokite gaunamus ASN per V3 duomenų objektą
description: Šiame straipsnyje paaiškinama, kaip valdyti gaunamų išplėstinių siuntimo pranešimų (ASN) importą naudojant gaunamų ASN duomenų objektą.
author: GalynaFedorova
ms.date: 05/11/2022
ms.topic: article
ms.search.form: WHSInboundASNV3Entity, WHSInboundASNEntity, DMFEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0ac45e070d0473547c48da1380377de3d4bf60bd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907122"
---
# <a name="import-inbound-asns-through-the-v3-data-entity"></a>Importuokite gaunamus ASN per V3 duomenų objektą

[!include [banner](../../includes/banner.md)]

Išplėstiniai siuntimo pranešimai (ASN) praneša jums apie tiekėjo pristatymus. Jie padeda siuntėjui aprašyti siuntos turinį ir papildomą informaciją apie ją, pavyzdžiui, prekes ir pakuotę.

ASN gali padėti sandėlio darbuotojams sužinoti, kada kas atvežama. Todėl jie gali pasiruošti. Be to, sandėlio darbuotojai gali naudoti ASN, kad siuntos informacija būtų suderinta su susijusiu pirkimo užsakymu, sukurtu anksčiau.

Šiame straipsnyje pateikite scenarijų, kurie parodyti pavyzdžiais, kaip dirbti su ASN failais, rinkinį.

> [!IMPORTANT]
> *Gaunamo ASN* importavimas taikomas tik toms prekėms, kurios yra įgalintos išplėstiniam sandėlio valdymui (WMS). Prieš gaudami ASN, sistemoje turi būti užregistruotas pirkimo užsakymas pagal tiekėją, kuris siunčia tą ASN.

## <a name="inbound-asn-v3-entity"></a>Gaunamo ASN V3 objektas

Gaunamo ASN importuojate naudodami gaunamų *ASN V3 sudėtinių* duomenų objektą. *Gaunamo ASN V3* naudojasi šiais objektais:

- Gaunamo krovinio antraštė
- Gaunamos siuntos antraštė
- Gaunamo krovinio pakavimo struktūros
- Gaunamo krovinio pakavimo struktūros dėžės
- Gaunamo krovinio pakavimo struktūros dėžių eilutės
- Gaunamo krovinio pakavimo struktūros eilutės

Sudėtinis *Gaunamo ASN V3* duomenų objektas yra skirtas asinchroninio integravimo scenarijams, kuriuose naudojami XML failu pagrįsti importavimai.

## <a name="xml-format-for-importing-asns"></a>XML formatas ASN importavimui

„Microsoft Dynamics 365 Supply Chain Management” palaiko šį XML formatą ASN importavimui. Kiekvienas XML failo mazgas atspindi atributą iš atskiro objekto.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV3Entity>
                    </WHSInboundPackingStructureCaseLineV3Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV3Entity>
                </WHSInboundLoadPackingStructureLineV3Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a>Pavyzdžiai

Toliau pateikti poskyriai pateikia tiekėjo siuntų ASN XML importavimo failų pavyzdžius.

### <a name="example-1"></a>1 pavyzdys

Šiame pavyzdyje rodomas tiekėjo siuntų importavimo XML failas, skirta vienam pirkimo užsakymui, kai neįtraukiama jokia atvejo informacija.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a>2 pavyzdys

Šiame pavyzdyje rodomas tiekėjo siuntų importavimo XML failas, skirta vienam pirkimo užsakymui, kai įtraukiama atvejo informacija.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLine3Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a>3 pavyzdys

Šiame pavyzdyje rodomas tiekėjo siuntų importavimo XML failas, skirta keliems pirkimo užsakymams, kai įtraukiama atvejo informacija.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a>ASN failo importavimo rezultatų patikrinimas

Atlikite šiuos veiksmus norėdami patikrinti ASN failo importavimo rezultatus.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Suraskite ir atidarykite krovinį, kuris buvo sukurtas kaip ASN importavimo dalis.
1. „FastTab” **Krovinys** turėtumėte matyti reikšmes, pagrįstas XML failu.
1. „FastTab” **Krovinio eilutės** turėtumėte matyti pardavimo užsakymo numerius ir prekės informaciją, pagrįstus XML failu.
1. Veiksmų srities skirtuko **Siųsti ir gauti** grupėje **Gauti** pasirinkite **Pakavimo struktūra**, kad peržiūrėtumėte krovinio pakavimo struktūrą.
1. „FastTab” **Paletės** turėtumėte matyti numerio lenteles, pagrįstas XML failu.
1. „FastTab” **Atvejai** turėtumėte matyti atvejus, pagrįstus XML failu.
1. „FastTab” **Prekės** turėtumėte matyti prekes ir kiekius, pagrįstus XML failu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
