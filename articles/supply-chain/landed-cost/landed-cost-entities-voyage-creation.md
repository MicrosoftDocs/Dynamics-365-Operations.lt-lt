---
title: Reiso kūrimo objektai
description: Šiame straipsnyje pateikiama informacija apie reiso kūrimo duomenų objektus, kurie grupuoti duomenų objektus, reikalingus norint sukurti darbo reisą.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 6234dfa61a5859e2ecaca75594c69c49ba326629
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/15/2022
ms.locfileid: "9167678"
---
# <a name="voyage-creation-entities"></a>Reiso kūrimo objektai

[!include [banner](../includes/banner.md)]

Reiso kūrimo duomenų objektai sugrupuoti duomenų objektus, kurių reikia norint sukurti darbo reisą. Jūs arba jūsų krovinių ekspeditorius gali naudoti šiuos duomenų objektus reisui, siuntimo konteineriui, registracijos ir reiso eilutės įrašams, kurie nurodo esamo pirkėjo užsakymo ar perkėlimo užsakymo eilutes, kurti.

## <a name="voyages-itmtableentity"></a>Reisai (ITMTableEntity)

Reisas rodo gaunamų prekių sklypą ir naudojamas kaip aukščiausio lygio išlaidų sritis Įkrautų išlaidų srityje. Joje pateikiama antraštės lygio informacija, susijusi su laivas, kilmės prievadu ir paskirties uostu. Šią funkciją palaiko objektas `ITMTableEntity`. Šioje lentelėje pateikiami laukai ir susiejimai, kurie sudaro šį objektą.

| Vardas | Susiejimas | Duomenų tipas | Raktas | Privalomas |
|---|---|---|---|---|
| Pristatymo būdas | ITMTable.DlvModeId | Nvarchar(10) | Ne | Ne |
| Tarpininkui patarta | ITMTable.ITMBrokerAdvised | Datetime | Ne | Ne |
| Kliento paskyrimas | ITMTable.ITMCustomerAppointment | Datetime | Ne | Ne |
| Pristatymas į sandėlį | ITMTable.ITMDelAtWare² | Datetime | Ne | Ne |
| Pristatymo instrukcijos | ITMTable.ITMDeliveryInstructions | Datetime | Ne | Ne |
| Išvykimo data | ITMTable.ITMDepartureDate | Datetime | Ne | Ne |
| Išleistos prekės | ITMTable.ITMGoodsReleased | Datetime | Ne | Ne |
| Vietinio transporto data | ITMTable.ITMLocalTransportDate | Datetime | Ne | Ne |
| Vietinio transporto laikas | ITMTable.ITMLocalTransportTime | Int | Ne | Ne |
| Išsiųstas originalus važtaraštis | ITMTable.ITMOriginalBOLSebt | Datetime | Ne | Ne |
| Gauti originalūs dokumentai | ITMTable.ITMOriginalDocsReceived | Datetime | Ne | Ne |
| Pirkimo užsakymo būsena | ITMTable.ITMPurchStatus | Int | Ne | Ne |
| Patikrinimo data | ITMTable.ITMVerificationDate | Datetime | Ne | Ne |
| Muitinės įrašo identifikatorius | ITMTable.ShipCustomsEntryId | Nvarchar(20) | Ne | Ne |
| Siuntimo data | ITMTable.ShipDate | Datetime | Ne | Ne |
| Aprašymas | ITMTable.ShipDescription | Nvarchar(60) | Ne | Ne |
| Gauti dokumentai | ITMTable.ShipDocReceived | Int | Ne | Ne |
| Įvertinta pristatymo data | ITMTable.ShipEstDlvDate | Datetime | Ne | Ne |
| ETA siuntimo uoste | ITMTable.ShipEstPortDate | Datetime | Ne | Ne |
| Kilmės uostas | ITMTable.ShipFromPort | Nvarchar(20) | Ne | Ne |
| Namo oru / važtaraštis | ITMTable.ShipABOB | Nvarchar(20) | Ne | Ne |
| Reisas | ITMTable.ShipId | Nvarchar(20) | **Taip** | **Taip** |
| Rezervavimo nuoroda | ITMTable.ShipIdExternal | Nvarchar(20) | Ne | Ne |
| Kelionės šablonas | ITMTable.ShipJourairId | Nvarchar(20) | Ne | Ne |
| Vietinis ekspeditorius | ITMTable.ShipLocalForwarder | Nvarchar(20) | Ne | Ne |
| Pagrindinis oras / važtaraštis | ITMTable.ShipMAWB | Nvarchar(20) | Ne | Ne |
| Matavimas | ITMTable.ShipMeasurement | Skaitinis(32, 6) | Ne | Ne |
| Matavimo vienetas | ITMTable.ShipMeasurementUnit | Int | Ne | Ne |
| Padėklų skaičius | ITMTable.ShipNoOfPallets | Int | Ne | Ne |
| Laukiantis reisas | ITMTable.ShipPending | Int | Ne | Ne |
| Pastabos | ITMTable.ShipRemarks | Nvarchar (maks.) | Ne | Ne |
| Nuoma | ITMTable.ShipRental | Int | Ne | Ne |
| Reiso būsena | ITMTable.ShipStatusId | Nvarchar(20) | Ne | Ne |
| Iš dalies numeris | ITMTable.ShipTallyInNumber | Nvarchar(20) | Ne | Ne |
| Paskirties uostas | ITMTable.ShipToPort | Nvarchar(20) | Ne | Ne |
| Vertinimo data | ITMTable.ShipValuationDate | Datetime | Ne | Ne |
| Gabenimo įmonė | ITMTable.ShipVendAccount | Nvarchar(20) | Ne | Ne |
| Laivas | ITMTable.ShipVesselId | Nvarchar(20) | Ne | **Taip** |
| Išorinis reiso ID | ITMTable.ShipVoyage | Nvarchar(20) | Ne | Ne |

### <a name="number-sequences-for-voyages"></a>Reisų numeracija

Reisų bendrai naudojama numeracija valdo reiso ID paskirstymą.

Vertė, perduota duomenų objektui kaip **Reiso ID** (`ShipId`) vertė, naudojama norint identifikuoti esamą įrašą, kad jį būtų galima atnaujinti. Jei tokio įrašo nėra, veikimo būdas priklauso nuo to, ar priskirta numeracija sukonfigūruota taip, kad leistų įvesti rankiniu būdu:

- Jei įgalintas neautomatinis įrašas, sukuriamas naujas įrašas, kuris naudoja perd sukurtą vertę.
- Jei neautomatinis įrašas neįgalintas, vietoj perduotos vertės naudojamas kitas priskirtos numeracijos numeris.

Importavimo seanso metu, vietos rezervavimo ženklo vertė, importuojama kaip reiso ID, išlaikoma. Taip užtikrinama, kad siuntimo konteineris ir reiso eilutės, kurios nurodo vietos rezervavimo ženklus, yra įtrauktos į reisą ir kad jos atnaujinamos, kad atspindėtų iš numeracijos priskirtą vertę.

### <a name="automatic-cost-transactions"></a>Automatinės išlaidų operacijos

Automatinės išlaidos gali būti pridėtos prie reiso iš Automatinių **išlaidų puslapio** Microsoft Dynamics 365 Supply Chain Management (**Įkainojimo įkainojimo \> nustatymas Automatinės \> išlaidos**). Automatinio išlaidų įrašai taip pat gali būti sukurti naudojant išlaidų operacijų duomenų objektus kiekvienai išlaidų zonai, kurią palaiko įkainotos išlaidos.

Automatinės išlaidos, sukonfigūruotos tiekimo grandinės vadyboje, reisui taikomos, kai sukuriama reiso eilutė. Prieš įrašą nebus matoma jokių išlaidų, kol antraštės įrašas nebus susietas su eilutės informacija.

## <a name="shipping-containers-itmcontainersentity"></a>Siuntimo konteineriai (ITMContainersEntity)

Siuntimo konteineris nurodo fizinį konteinerį, kuriame transportuojami prekės. Šis faktinis konteineris gali būti pervežimo konteineris, skirtas pervežimui iš vandenyno, arba vienas padėklas, skirtas transportuoti oru. Siuntimo konteineryje yra antraštės lygio informacija, susijusi su siuntimo konteinerio ID, antspaudo numeriu ir siuntos konteinerio tipu. (Siuntimo konteinerio tipas pateikia dimensijos informaciją.) Šią funkciją palaiko objektas `ITMContainersEntity`. Šioje lentelėje pateikiami laukai ir susiejimai, kurie sudaro šį objektą.

| Vardas | Susiejimas | Duomenų tipas | Raktas | Privalomas |
|---|---|---|---|---|
| Išvykimo data | ITMContainers.ITMDepartureDate | Datetime | Ne | Ne |
| Vietinio transporto data | ITMContainers.ITMLocalTransportDate | Datetime | Ne | Ne |
| Vietinio transporto laikas | ITMContainers.ITMLocalTransportTime | Int | Ne | Ne |
| Pradinis reisas | ITMContainers.OrigShipId | Nvarchar(20) | Ne | Ne |
| Faktinis svoris | ITMContainers.ShipActualWeight | Skaitinis(32, 6) | Ne | Ne |
| Tarpininkui patarta | ITMContainers.ShipBrokerAdvised | Datetime | Ne | Ne |
| Gabenimo konteineris | ITMContainers.ShipContainerId | Nvarchar(20) | **Taip** | **Taip** |
| Gabenimo konteinerio tipas | ITMContainers.ShipContainerTypeId | Nvarchar(20) | Ne | Ne |
| Vieneto tipas | ITMContainers.ShipContainerUnitTypeId | Nvarchar(10) | Ne | Ne |
| Konvertuota į nuomojamą | ITMContainers.ShipConvertedToRental | Int | Ne | Ne |
| Kliento paskyrimas | ITMContainers.ShipCustomerAppointment | Datetime | Ne | Ne |
| Siuntimo data | ITMContainers.ShipDate | Datetime | Ne | Ne |
| Pristatymas į sandėlį | ITMContainers.ShipDelAtWare² | Datetime | Ne | Ne |
| Pristatymo instrukcijos | ITMContainers.ShipDeliveryInstructions | Datetime | Ne | Ne |
| Tyrimo pažymėjimo taikymo data | ITMContainers.ShipECAppliedDate | Datetime | Ne | Ne |
| Tyrimo pažymėjimo galiojimo data | ITMContainers.ShipECExpiryDate | Datetime | Ne | Ne |
| Tyrimo pažymėjimo numeris | ITMContainers.ShipECNum | Nvarchar(20) | Ne | Ne |
| Tyrimo pažymėjimo gavimo data | ITMContainers.ShipECReceivedDate | Datetime | Ne | Ne |
| Įvertinta pristatymo data | ITMContainers.ShipEstDlvDate | Datetime | Ne | Ne |
| ETA siuntimo uoste | ITMContainers.ShipEstPortDate | Datetime | Ne | Ne |
| Numatoma pakrovimo data | ITMContainers.ShipExpectedLoadingDate | Datetime | Ne | Ne |
| Kilmės uostas | ITMContainers.ShipFromPort | Nvarchar(20) | Ne | Ne |
| Prekių aprašas | ITMContainers.ShipGoodsDesc | Nvarchar(60) | Ne | Ne |
| Išleistos prekės | ITMContainers.ShipGoodsReleased | Datetime | Ne | Ne |
| GPS sekimo įrenginys | ITMContainers.ShipGPSUnit | Nvarchar(30) | Ne | Ne |
| Namo oru / važtaraštis | ITMContainers.ShipHAVB | Nvarchar(20) | Ne | Ne |
| Reisas | ITMContainers.ShipId | Nvarchar(20) | **Taip** | **Taip** |
| Kelionės šablonas | ITMContainers.ShipJourairId | Nvarchar(20) | Ne | Ne |
| Vietinis ekspeditorius | ITMContainers.ShipLocalForwarder | Nvarchar(20) | Ne | Ne |
| Matavimas | ITMContainers.ShipMeasurement | Skaitinis(32, 6) | Ne | Ne |
| Matavimo vienetas | ITMContainers.ShipMeasurementUnit | Int | Ne | Ne |
| Kartoninių dėžių skaičius | ITMContainers.ShipNoOfCartons | Skaitinis(32, 6) | Ne | Ne |
| Išsiųstas originalus važtaraštis | ITMContainers.ShipOriginalBOLSebt | Datetime | Ne | Ne |
| Gauti originalūs dokumentai | ITMContainers.ShipOriginalDocsReceived | Datetime | Ne | Ne |
| Mūsų antspaudo numeris | ITMContainers.ShipOurSealNum | Nvarchar(20) | Ne | Ne |
| Naudota | ITMContainers.ShipPendingUsed | Int | Ne | Ne |
| Pirkimo užsakymo būsena | ITMContainers.ShipPurchStatus | Int | Ne | Ne |
| Šaldymo tipas | ITMContainers.ShipRefrigerationTypeId | Nvarchar(10) | Ne | Ne |
| Pastabos | ITMContainers.ShipRemarks | Nvarchar (maks.) | Ne | Ne |
| Nuoma | ITMContainers.ShipRental | Int | Ne | Ne |
| Grąžinama | ITMContainers.ShipReturnable | Int | Ne | Ne |
| Reiso būsena | ITMContainers.ShipStatusId | Nvarchar(20) | Ne | Ne |
| Gabenimo įmonės antspaudo numeris | ITMContainers.ShipTheirSealNum | Nvarchar(20) | Ne | Ne |
| Paskirties uostas | ITMContainers.ShipToPort | Nvarchar(20) | Ne | Ne |
| Patikrinimo data | ITMContainers.ShipVerificationDate | Datetime | Ne | Ne |
| Laivas | ITMContainers.ShipVesselId | Nvarchar(20) | Ne | **Taip** |

### <a name="voyage-id-validation"></a>Reiso ID tikrinimas

Siuntimo konteinerio ID nekontroliuoja numeracija. Tai unikali tik reiso, kuriame jis naudojamas, kontekste.

Jei gabenimo konteinerio objektas (`ITMContainersEntity`) naudojamas nepriklausomai nuo reiso objekto (`ITMTableEntity`), **reiso ID** (`ShipId`) vertė turi atitikti esamą reiso lentelės įrašą. Kitu atveju importuoti nepavyks.

Jei siuntimo konteinerio objektas (`ITMContainersEntity`) ir reiso objektas (`ITMTableEntity`) naudojami kaip to paties importavimo seanso dalis, reiso objektas turi būti prieš tai, kai buvo sukurtas siuntimo konteineris. Kitu atveju **reiso ID** (`ShipId`) vertės sėkmingai patikrinti negalima. Jei vietos rezervavimo **ženklo vertė naudojama reiso ID** () vertei, susiejimą galima sukurti tik tada, `ShipId` jei tas pats vietos rezervavimo ženklas naudojamas kaip reiso ID **(**`ShipId`) vertė siuntimo konteinerio objektui.

### <a name="other-field-validations"></a>Kiti laukų tikrinimas

Toliau pateikiamoje lentelėje rodomi gabenimo konteinerio lentelės (`ITMContainers`) laukai, kurie patikrinti pagal sklypo išlaidų nustatymo lenteles. Joje taip pat rodomi įkrautų išlaidų duomenų objektai, kuriuos krovinių ekspeditorus gali naudoti esamoms vertėms perskaityti ir užtikrinti, kad jūsų aplinkoje bus gautos tinkamos vertės.

| Laukas ITMContainers lentelėje | Įkrautos savikainos duomenų objektas |
|---|---|
| Gabenimo konteinerio tipas | ITMShippingContainerTypeEntity |
| Prekių aprašas | ITMGoodsDescriptionEntity |
| Šaldymo tipas | ITMShippingContainerRefrigerationTypeEntity |

## <a name="folios-itmfolioentity"></a>Fijus (ITMFolioEntity)

Registracijos pavadinimas nurodo prekių grupę siuntimo konteineryje muitinės deklaracijoms. Registracijose yra antraštės lygio informacija, susijusi su muitinės brokeriu, ir prekių aprašymas. Šią funkciją palaiko objektas `ITMFolioEntity`. Šioje lentelėje pateikiami laukai ir susiejimai, kurie sudaro šį objektą.

| Vardas | Susiejimas | Duomenų tipas | Raktas | Privalomas |
|---|---|---|---|---|
| Tarpininkui patarta | ITMFolioTable.ShipBrokerAdvised | Datetime | Ne | Ne |
| Krovinio kontrolinis numeris | ITMFolioTable.ShipCargoControlNumber | Nvarchar(20) | Ne | Ne |
| Kliento paskyrimas | ITMFolioTable.ShipCustomerAppointment | Datetime | Ne | Ne |
| Muitinės tarpininkas | ITMFolioTable.ShipCustomsBroker | Nvarchar(20) | Ne | Ne |
| Muitinės ID | ITMFolioTable.ShipCustomsId | Nvarchar(60) | Ne | Ne |
| Įmonė | ITMFolioTable.ShipDataArea | Nvarchar(4) | Ne | **Taip** |
| Pristatymas į sandėlį | ITMFolioTable.ShipDelAtWare² | Datetime | Ne | Ne |
| Pristatymo instrukcijos | ITMFolioTable.ShipDeliveryInstructions | Datetime | Ne | Ne |
| Gauti dokumentai | ITMFolioTable.ShipDocReceived | Int | Ne | Ne |
| Įvertinta pristatymo data | ITMFolioTable.ShipEstDlvDate | Datetime | Ne | Ne |
| ETA siuntimo uoste | ITMFolioTable.ShipEstPortDate | Datetime | Ne | Ne |
| Eksportuotojas | ITMFolioTable.ShipExporterId | Nvarchar(20) | Ne | Ne |
| Vardas | ITMFolioTable.ShipExporterName | Nvarchar(60) | Ne | Ne |
| Registravimo lapo data | ITMFolioTable.ShipFolioDate | Datetime | Ne | Ne |
| Registravimo lapas | ITMFolioTable.ShipFolioId | Nvarchar(20) | **Taip** | **Taip** |
| Kilmės uostas | ITMFolioTable.ShipFromPort | Nvarchar(20) | Ne | Ne |
| Prekių aprašas | ITMFolioTable.ShipGoodsDesc | Nvarchar(60) | Ne | Ne |
| Išleistos prekės | ITMFolioTable.ShipGoodsReleased | Datetime | Ne | Ne |
| Namo oru / važtaraštis | ITMFolioTable.ShipHAVB | Nvarchar(20) | Ne | Ne |
| Reisas | ITMFolioTable.ShipId | Nvarchar(20) | Ne | **Taip** |
| Matavimas | ITMFolioTable.ShipMeasurement | Skaitinis(32, 6) | Ne | Ne |
| Matavimo vienetas | ITMFolioTable.ShipMeasurementUnit | Int | Ne | Ne |
| Kartoninių dėžių skaičius | ITMFolioTable.ShipNoOfCartons | Skaitinis(32, 6) | Ne | Ne |
| Išsiųstas originalus važtaraštis | ITMFolioTable.ShipOriginalBOLSebt | Datetime | Ne | Ne |
| Gauti originalūs dokumentai | ITMFolioTable.ShipOriginalDocsReceived | Datetime | Ne | Ne |
| Pirkimo užsakymo būsena | ITMFolioTable.ShipPurchStatus | Int | Ne | Ne |
| Pastabos | ITMFolioTable.ShipRemarks | Nvarchar (maks.) | Ne | Ne |
| Reiso būsena | ITMFolioTable.ShipStatusId | Nvarchar(20) | Ne | Ne |
| Tarifo kodas | ITMFolioTable.ShipTariffCode | Nvarchar(10) | Ne | Ne |
| Paskirties uostas | ITMFolioTable.ShipToPort | Nvarchar(20) | Ne | Ne |
| Vertinimo data | ITMFolioTable.ShipValuationDate | Datetime | Ne | Ne |
| Patikrinimo data | ITMFolioTable.ShipVerificationDate | Datetime | Ne | Ne |
| Tiekėjo paskyra | ITMFolioTable.VendAccount | Nvarchar(20) | Ne | Ne |

### <a name="number-sequences-for-folios"></a>Nuaso numeracijos

Folio ID priskyrimas valdomas pagal numerių numeraciją.

Vertė, perduota duomenų objektui kaip **registracijos ID** (`FolioId`) vertė, naudojama norint identifikuoti esamą įrašą, kurį reikia atnaujinti. Jei tokio įrašo nėra, veikimo būdas priklauso nuo to, ar priskirta numeracija sukonfigūruota taip, kad leistų įvesti rankiniu būdu:

- Jei įgalintas neautomatinis įrašas, sukuriamas naujas įrašas, kuris naudoja perd sukurtą vertę.
- Jei neautomatinis įrašas neįgalintas, vietoj perduotos vertės naudojamas kitas priskirtos numeracijos numeris.

Importavimo seanso metu išlaikoma vietos rezervavimo ženklo vertė, importuojama kaip registracijos ID. Taip užtikrinama, kad reiso eilutės, kuriose nurodo vietos rezervavimo ženklą, yra tinkamai susietos ir kad jos atnaujinamos, kad atspindėtų iš numeracijos priskirtą vertę.

### <a name="field-validations"></a>Lauko tikrinimas

Prekių **aprašymo** laukas registracijos lentelėje (`ITMFolioTable`) patikrintas pagal to paties pavadinimo sklypų išlaidų nustatymo lentelę. Krovinių ekspeditoratorius gali naudoti įkrautų `ITMGoodsDescriptionEntity` išlaidų duomenų objektą, kad perskaitytų esamas vertes ir užtikrintų, jog jūsų aplinkoje gautos tinkamos vertės.

## <a name="voyage-lines-for-purchase-orders-itmpurchaselineentity"></a>Pirkimo užsakymų reiso eilutės (ITMPurchaseLineEntity)

Reiso eilutė rodo vieną pirkimo užsakymo eilutę, įtrauktą į reisą. Šis ryšys nustatomas pirkimo užsakymo **numerio ir** pirkimo **eilutės numerio laukuose**. Reiso eilutė nurodo kiekvieną ankstesnį reiso, siuntimo konteinerio ir registracijos įrašą. Šią funkciją palaiko objektas `ITMPurchaseLineEntity`. Šioje lentelėje pateikiami laukai ir susiejimai, kurie sudaro šį objektą.

| Vardas | Susiejimas | Duomenų tipas | Raktas | Privalomas |
|---|---|---|---|---|
| Valiuta | ITMLine. CurrencyCode | Nvarchar(3) | Ne | Ne |
| Grynoji suma | ITMLine.LineAmountMST | Skaitinis(32, 6) | Ne | Ne |
| Pirkimo eilutės numeris | ITMLine.RefRecId | Skaitinis(32, 6) | **Taip** | Ne |
| Gabenimo konteineris | ITMLine.ShipContainerId | Int | Ne | Ne |
| Įmonė | ITMLine.ShipDataArea | Nvarchar(20) | **Taip** | Ne |
| Deklaruotas kiekis | ITMLine.ShipDeclaredQty | Nvarchar(4) | Ne | Ne |
| Registravimo lapas | ITMLine.ShipFolioId | Skaitinis(32, 6) | Ne | Ne |
| Reisas | ITMLine.ShipId | Nvarchar(20) | **Taip** | Ne |
| Prekės numeris | ITMLine.ShipItemId | Nvarchar(20) | Ne | Ne |
| Matavimas | ITMLine.ShipMeasurement | Nvarchar(20) | Ne | Ne |
| Matavimo vienetas | ITMLine.ShipMeasurementUnit | Skaitinis(32, 6) | Ne | Ne |
| Kartoninių dėžių skaičius | ITMLine.ShipNoOfCartons | Int | Ne | Ne |
| Pozicija | ITMLine.ShipPosition | Skaitinis(32, 6) | Ne | Ne |
| Kiekis | ITMLine.ShipQty | Int | Ne | Ne |
| Pirkimo užsakymo numeris | ITMLine.TransRefId | Skaitinis(32, 6) | **Taip** | Ne |
| Vienetas | ITMLine. UnitId | Int | Ne | Ne |
| Kiekis | ITMLine. Tūris | Nvarchar(10) | Ne | Ne |
| Svoris | ITMLine.Svoris | Skaitinis(32, 6) | Ne | Ne |

## <a name="voyage-lines-for-transfer-orders-itmtransferlineentity"></a>Perkėlimo užsakymų reiso eilutės (ITMTransferLineEntity)

Reiso eilutė rodo vieną perkėlimo užsakymo eilutę, kuri įtraukta į reisą. Šis ryšys nustatomas naudojant laukus **Perkėlimo užsakymo numeris** ir **Perkėlimo eilutės** numeris. Reiso eilutė nurodo kiekvieną ankstesnį reiso, siuntimo konteinerio ir registracijos įrašą. Šią funkciją palaiko objektas `ITMTransferLineEntity`. Šioje lentelėje pateikiami laukai ir susiejimai, kurie sudaro šį objektą.

| Vardas | Susiejimas | Duomenų tipas | Raktas | Privalomas |
|---|---|---|---|---|
| Valiuta | ITMLine. CurrencyCode | Nvarchar(3) | Ne | Ne |
| Grynoji suma | ITMLine.LineAmountMST | Skaitinis(32, 6) | Ne | Ne |
| Gabenimo konteineris | ITMLine.ShipContainerId | Int | Ne | Ne |
| Įmonė | ITMLine.ShipDataArea | Nvarchar(20) | **Taip** | Ne |
| Deklaruotas kiekis | ITMLine.ShipDeclaredQty | Nvarchar(4) | Ne | Ne |
| Registravimo lapas | ITMLine.ShipFolioId | Skaitinis(32, 6) | Ne | Ne |
| Reisas | ITMLine.ShipId | Nvarchar(20) | **Taip** | Ne |
| Prekės numeris | ITMLine.ShipItemId | Nvarchar(20) | Ne | Ne |
| Matavimas | ITMLine.ShipMeasurement | Nvarchar(20) | Ne | Ne |
| Matavimo vienetas | ITMLine.ShipMeasurementUnit | Skaitinis(32, 6) | Ne | Ne |
| Kartoninių dėžių skaičius | ITMLine.ShipNoOfCartons | Int | Ne | Ne |
| Pozicija | ITMLine.ShipPosition | Skaitinis(32, 6) | Ne | Ne |
| Kiekis | ITMLine.ShipQty | Int | Ne | Ne |
| Perkėlimo eilutės numeris | ITMLine.TransferLineNumber | Skaitinis(32, 6) | **Taip** | Ne |
| Perkėlimo užsakymo numeris | ITMLine.TransRefId | Skaitinis(32, 6) | **Taip** | Ne |
| Vienetas | ITMLine. UnitId | Int | Ne | Ne |
| Kiekis | ITMLine. Tūris | Nvarchar(10) | Ne | Ne |
| Svoris | ITMLine.Svoris | Skaitinis(32, 6) | Ne | Ne |

### <a name="reference-table"></a>Nuorodų lentelė

Reiso eilutės kuriamos susiejimu su atvira gaunamo užsakymo eilute. Ši eilutė gali būti pirkimo užsakyme arba perkėlimo užsakyme gali būti gavimo operacija. Reiso `RefTableId` eilutės lentelės laukas (`ITMLine`) nurodo, su kuriuo užsakymo tipu eilutė susijusi, nurodant lentelės numerį. Jei lentelėje, kurioje kuriami duomenys, nurodyti konkretūs lentelės numeriai, objektai skaidomi remiantis tomis vertėmis.

Nuorodų lentelės () ir operacijos tipo (`RefTableId``TransType`) vertės netiesiogiai yra pasirinktyje Įkainotų išlaidų pirkimo eilutės objektas arba Įkainotų išlaidų perkėlimo eilutės objektas.

### <a name="validation"></a>Patikrinimas

Reiso eilutė tiesiogiai nurodo reiso įrašą, siuntimo konteinerio įrašą ir registracijos įrašą. Jei pirkimo eilutės objektas (`ITMPurchaseLinesEntity`) arba perkėlimo eilutės objektas (`ITMPurchaseLinesEntity`) naudojamas neatsižvelgiant į objektus, kurie naudojami kuriant šiuos nuorodos įrašus, **reiso ID** (`ShipId`),**siuntimo** konteinerio (`ShipContainerId`**·**) ir registracijos (`ShipFolioId`) vertės turi atitikti esamą įrašą atitinkamose lentelėse. Kitu atveju importuoti nepavyks.

Jei eilutės objektas naudojamas kaip to paties importavimo seanso dalis, prieš kuriant reiso eilutę šie kiti objektai turi būti sukurti. Kitaip verčių sėkmingai patikrinti negalima. Jei vietos rezervavimo ženklo vertė naudojama reiso arba registracijos numeriui, susiejimą galima sukurti tik tuo atveju, jei reiso eilutės objektui naudojamas tas pats vietos rezervavimo ženklas arba registracijos numeris.

Jei pirkimo užsakymas arba perkėlimo užsakymo eilutė jau priskirta esamai reiso eilutei, nauja reiso eilutė nebus sukurta. Kad užsakymo eilutė galėtų būti priskirta naujam reisui, ji turi būti pašalinta iš dabartinės reiso.

### <a name="order-line-identification"></a>Užsakymo eilutės identifikavimas

Reiso eilutės tiesiogiai nurodo nuorodos **įrašo ID** (`RefRecId`), **atsargų dimensijos ID** (`InventDimId`) **ir atsargų operacijos ID** (`InventTransId`) vertes. Šių verčių daugiau nereikia įtraukti, kai naudojamas duomenų objektas. Vietoj to, užsakymo eilutės numerį dabar reikia įtraukti. Užsakymo eilutės numeris ir užsakymo numeris leidžia identifikuoti kiekvieną iš šių nuorodos verčių.

### <a name="voyage-line-quantity"></a>Reiso eilutės kiekis

Kadangi reiso eilutė tiesiogiai susieta su užsakymo eilute, **naudojant** objektą įvesta kiekio (`ShipQty`) vertė reikalauja, kad vertės atitiktų. Tikrinimas vykdomas pagal kiekį, nurodytą pirkimo užsakymo eilutėje arba perkėlimo eilutėje. Jei patikrinimas nesėkmingas, įrašas nebus apdorotas.

### <a name="calculated-fields"></a>Suskaičiuoti laukai

**Apskaičiuoti** svorio **ir** tūrio laukai priima vertes, kurios gautos naudojant duomenų objektą. Jei verčių nėra, sistemos vertės naudojamos šiems laukams atnaujinti, jei sistemos vertės galimos. Įkainotų išlaidų vertės skaičiuojamos tokiu būdu:

- *·* = *Svorio kiekis* × *Prekės bruto svoris*
- *Tūrio* = *kiekio* × (prekės *bruto gylis* × *prekės bruto aukštis* × *prekės bruto plotis*)

## <a name="sequencing"></a>Seka

Pirmiausia reikia sukurti reiso įrašą dėl lentelių priklausomybės. Reiso eilutę galima sukurti tik po to, kai buvo sukurtas reisas, siuntimo konteineris ir tts.

Norint sukurti reisą be tikrinimo įspėjimų, sistema turi apdoroti objektus tokia tvarka:

1. Reisai (`ITMTableEntity`)
1. Siuntimo konteineriai (`ITMContainersEntity`)
1. Fijus (`ITMFolioTableEntity`)
1. Reiso eilutės (`ITMPurchaseLinesEntity` arba `ITMTransferLinesEntity`)
