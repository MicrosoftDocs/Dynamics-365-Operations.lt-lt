---
title: Integravimas trečiosios šalies gamybos vykdymo sistemose
description: Šioje temoje paaiškinama, kaip galite integruoti Dynamics 365 Supply Chain Management "Microsoft" į trečiosios šalies gamybos vykdymo sistemą (MES).
author: t-benebo
ms.date: 10/01/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-01
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 14e86a49777eefefae711bfe0d756361b09d69c2
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778454"
---
# <a name="integrate-with-third-party-manufacturing-execution-systems"></a>Integravimas trečiosios šalies gamybos vykdymo sistemose

[!include [banner](../includes/banner.md)]

Kai kurios gamybos organizacijos, kurios naudoja "Microsoft" naudoja gimtąją "Dynamics 365" funkciją, kad galėtų kontroliuoti savo įrenginių, įrangos ir personalo Dynamics 365 Supply Chain Management gamybos veiklą. Tačiau kitos gamybos organizacijos, ypač tos, kurios turi išplėstinių gamybos reikalavimų, naudoja trečiosios šalies gamybos vykdymo sistemą (MES). Organizacijos gali pasirinkti trečiosios šalies MES sprendimą, nes, pavyzdžiui, jis specialiai pritaikytas jų vertikaliai pramonei.

Integruotuose sprendimuose duomenų mainai yra visiškai automatizuoti ir vyksta beveik realiuoju laiku. Todėl duomenys laikomi dabartiniai abiejose sistemose ir nereikia įvesti duomenų neautomatiniu būdu. Pavyzdžiui, kai medžiagų suvartojimas registruojamas MES, integracija užtikrina, kad "Dynamics 365" registruojamas ir tas pats suvartojimas. Todėl naujausiais atsargų įrašais galima naudotis kitiems svarbiams procesams, pvz., planavimui ir pardavimui.

Sprendimas yra greitesnis, paprastesnis ir paprastesnis tiekimo grandinės valdymo vartotojams, kad jie galėtų integruotis su trečiosios šalies MES. Jis siūlo šias funkcijas:

- Verslo įvykiai ir sąsajos, kurios palaiko [pagrindinius gamybos vykdymo procesus](#processes-available-for-mes-integration)
- Centralizuota skelbimų skelbimų skelbimų sritis, kurioje galite sekti įvykių apdorojimo retrospektyvą ir šalinti bei taisyti procesus, kurie nepavyko

Toliau esanti iliustracija pateikia įprastą verslo įvykių, procesų ir pranešimų, kurie keičiamasi integruotuose sprendimuose, rinkinį.

![Įprastas integravimo scenarijus.](media/3p-mes-scenario.png "Įprastas integravimo scenarijus.")

## <a name="turn-on-the-mes-integration-feature"></a>Įjungti MES integravimo funkciją

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Gamybos kontrolė*
- **Funkcijos pavadinimas:** *gamybos vykdymo sistemos integravimas*

## <a name="processes-available-for-mes-integration"></a>Galimi MES integravimo procesai

Galite įgalinti bet kurį arba visus šiuos integravimo procesus.

| Proceso pavadinimas | Aprašymas |
|---|---|
| Išleisti gamybos užsakymus ir gamybos užsakymo būsenos keitimo verslo įvykius | Šis procesas suteikia verslo įvykį, kurį MES gali klausyti, norėdami gauti informacijos apie gamybos užsakymus, kurie turi būti pateikti. Tikimasi, kad su gamybos užsakymu susiję nuorodos duomenys bus bendrai naudojami tiekimo grandinės valdymo metu su MES per atvirą duomenų protokolą (OData) arba duomenų objektus. |
| Gamybos užsakymo pradžia | Šis procesas suteikia tiekimo grandinės valdymą ir informaciją apie gamybos užsakymus, kurie pradėti naudojant MES. Taip užtikrinama, kad abiejose sistemose yra naujausias visų gamybos veiklų rodinys. |
| Ataskaita apie pagamintą arba nurašytą kiekį | Šis procesas suteikia tiekimo grandinės valdymą ir informaciją apie gerų ir klaidų kiekius, kurie pranešami gamybos užduotyje naudojant MES. Taip užtikrinama, kad darbo laiko prižiūrėtojai turėtų naujausias gamybos plano eigos vaizdą. |
| Ataskaita apie medžiagų suvartojimą | Šis procesas teikia tiekimo grandinės valdymą, remiantis MES, informacija apie suvartotų medžiagų kiekį. Ji atlieka naujausias atsargų įrašus, prieinamus kitiems svarbiams procesams, pvz., planavimui ir pardavimui. |
| Ataskaitai skirtas laikas, sunaudotas operacijai | Šis procesas suteikia tiekimo grandinės valdymą ir informaciją apie laiką, kuris naudojamas specialiai operacijai. |
| Baigti gamybos užsakymą | Šis procesas informuos tiekimo grandinės valdymą, kad MES atnaujino gamybos užsakymą į galutinę būseną *·* Baigta. Ši būsena nurodo, kad pagal gamybos užsakymą daugiau kiekių nebus gaminama. |

## <a name="monitor-incoming-messages"></a>Gautų pranešimų stebėjimas

Norėdami stebėti į sistemą gaunamus pranešimus, atidarykite **gamybos vykdymo sistemų integravimo** puslapį. Čia galite peržiūrėti, apdoroti ir šalinti triktis.

## <a name="call-the-api"></a>Iškviesti API

Norėdami iškviesti MES integravimo API, siųskite `POST` užklausą šiuo galinio punkto URL:

`/api/services/SysMessageServices/SysMessageService/SendMessage`

Jūsų siunčiamos užklausos tekstas turėtų būti panašus į šį pavyzdį. Pakeiskite, `_companyId``_messageType` ir, jei `_messageContent` reikia, vertes. Informacijos apie įvairius pranešimų tipus, kuriuos PALAIKO API, ir kaip kurti jų turinį, ieškokite kitame skyriuje.

```json
{
    "_companyId": "USMF",
    "_messageQueue": "JmgMES3P",
    "_messageType": "ProdProductionOrderReportFinished",
    "_messageContent":
    "{\"ProductionOrderNumber\": \"P000123\", \"ReportFinishedLines\": [{\"ItemNumber\": \"A0001\", \"ReportedGoodQuantity\": 10, \"ReportAsFinishedDate\": \"2021-01-01\"}]}"
}
```

## <a name="api-message-types-and-content"></a>API pranešimų tipai ir turinys

Šiame skyriuje aprašomas kiekvienas pranešimų, kuriuos galima pakeisti naudojant MES integravimo API, tipas.

### <a name="start-production-order-message"></a>Pradėti gamybos užsakymo pranešimą

Pradžios *gamybos užsakymo* pranešimo vertė `_messageType``ProdProductionOrderStart` yra. Toliau pateikiamoje lentelėje rodomi laukai, kuriuos palaiko šis pranešimas.

| Lauko pavadinimas | Būsena | Tipas |
|---|---|---|
| `ProductionOrderNumber` | Privalomas | Eilutė |
| `StartedQuantity` | Pasirinktina | Tikrasis |
| `StartedDate` | Pasirinktina | Data |
| `AutomaticBOMConsumptionRule` | Pasirinktina | Išvardijimas (FlushingPrincip \| visada \| niekada) |

### <a name="report-as-finished-message"></a>Pranešti apie pabaigimo pranešimą

Pranešimo, *kuris yra* baigtas, vertė `_messageType``ProdProductionOrderReportFinished` yra. Toliau pateikiamoje lentelėje rodomi laukai, kuriuos palaiko šis pranešimas.

| Lauko pavadinimas | Būsena | Tipas |
|---|---|---|
| `ProductionOrderNumber` | Privalomas | Eilutė |
| `ReportFinishedLines` | Privalomas | Eilučių (bent vienos), kurių kiekvienoje yra mokamų kūstų, aprašytų toliau esančioje lentelėje, sąrašas |

Toliau pateikiamoje lentelėje rodomi laukai, kuriuos palaiko `ReportFinishedLines` kiekviena pranešimo `ProdProductionOrderReportFinished` skyriaus eilutė.

| Lauko pavadinimas | Būsena | Tipas |
|---|---|---|
| `LineNumber` | Pasirinktina | Tikrasis |
| `ItemNumber` | Pasirinktina | Eilutė|
| `ProductionType` | Pasirinktina | Išvardiimas (MainItem \|\| formulės \| KS Co_Product By_Product \|\| Nėra), extensible |
| `ReportedErrorQuantity` | Pasirinktina | Tikrasis|
| `ReportedGoodQuantity` | Pasirinktina | Tikrasis|
| `ReportedErrorCatchWeightQuantity` | Pasirinktina | Tikrasis |
| `ReportedGoodCatchWeightQuantity` | Pasirinktina | Tikrasis |
| `AcceptError` | Pasirinktina |Bulio logika |
| `ErrorCause` | Pasirinktina | Išvardiimas \| (nėra \| medžiagų mašinos \| valdymostafo), extensible |
| `ExecutedDateTime` | Pasirinktina | DateTime |
| `ReportAsFinishedDate` | Pasirinktina | Data |
| `AutomaticBOMConsumptionRule` | Pasirinktina | Išvardijimas (FlushingPrincip \| visada \| niekada) |
| `AutomaticRouteConsumptionRule` | Pasirinktina |Išvardiimas (RouteDependent \| visada \| niekada) |
| `RespectFlushingPrincipleDuringOverproduction` | Pasirinktina | Bulio logika |
| `ProductionJournalNameId` | Pasirinktina | Eilutė |
| `PickingListProductionJournalNameId` | Pasirinktina | Eilutė|
| `RouteCardProductionJournalNameId` | Pasirinktina | Eilutė |
| `FromOperationNumber` | Pasirinktina | Sveikasis skaičius|
| `ToOperationNumber` | Pasirinktina | Sveikasis skaičius|
| `InventoryLotId` | Pasirinktina | Eilutė |
| `BaseValue` | Pasirinktina | Eilutė |
| `EndJob` | Pasirinktina | Bulio logika |
| `EndPickingList` | Pasirinktina | Bulio logika |
| `EndRouteCard` | Pasirinktina | Bulio logika |
| `PostNow` | Pasirinktina | Bulio logika |
| `AutoUpdate` | Pasirinktina | Bulio logika |
| `ProductColorId` | Pasirinktina | Eilutė|
| `ProductConfigurationId` | Pasirinktina | Eilutė |
| `ProductSizeId` | Pasirinktina | Eilutė |
| `ProductStyleId` | Pasirinktina | Eilutė |
| `ProductVersionId` | Pasirinktina | Eilutė |
| `ItemBatchNumber` | Pasirinktina | Eilutė |
| `ProductSerialNumber` | Pasirinktina | Eilutė |
| `LicensePlateNumber` | Pasirinktina | Eilutė |
| `InventoryStatusId` | Pasirinktina | Eilutė |
| `ProductionWarehouseId` | Pasirinktina | Eilutė |
| `ProductionSiteId` | Pasirinktina | Eilutė |
| `ProductionWarehouseLocationId` | Pasirinktina | Eilutė |
| Nuo `InventoryDimension1` iki `InventoryDimension12` | Pasirinktina | Eilutė |

12 extensible dimensijų `InventoryDimension1``InventoryDimension12` (per) reikalauja pritaikymo, bet ne visada naudojamos. Daugiau informacijos apie jas rasite [plėtiniu Įtraukti naujas atsargų dimensijas.](../../fin-ops-core/dev-itpro/extensibility/inventory-dimensions.md)

### <a name="material-consumption-picking-list-message"></a>Medžiagų suvartojimo (išrinkimo sąrašas) pranešimas

Medžiagų *suvartojimo (išrinkimo dokumentų)* pranešimas `_messageType` yra `ProdProductionOrderPickingList` vertė. Toliau pateikiamoje lentelėje rodomi laukai, kuriuos palaiko šis pranešimas.

| Lauko pavadinimas | Būsena | Tipas |
|---|---|---|
| `ProductionOrderNumber` | Privalomas | Eilutė |
| `JournalNameId` | Pasirinktina | Eilutė |
| `PickingListLines` | Privalomas | Eilučių (bent vienos), kurių kiekvienoje yra mokamų kūstų, aprašytų toliau esančioje lentelėje, sąrašas |

Toliau pateikiamoje lentelėje rodomi laukai, kuriuos palaiko `PickingListLines` kiekviena pranešimo `ProdProductionOrderPickingList` skyriaus eilutė.

| Lauko pavadinimas | Būsena | Tipas |
|---|---|---|
| `ItemNumber` | Privalomas | Eilutė |
| `ConsumptionBOMQuantity` | Pasirinktina | Tikrasis |
| `ProposalBOMQuantity` | Pasirinktina | Tikrasis |
| `ScrapBOMQuantity` | Pasirinktina | Tikrasis |
| `BOMUnitSymbol` | Pasirinktina | Eilutė |
| `ConsumptionInventoryQuantity` | Pasirinktina | Tikrasis |
| `ProposalInventoryQuantity` | Pasirinktina | Tikrasis |
| `ConsumptionCatchWeightQuantity` | Pasirinktina | Tikrasis |
| `ProposalCatchWeightQuantity` | Pasirinktina | Tikrasis |
| `ConsumptionDate` | Pasirinktina | Data |
| `OperationNumber` | Pasirinktina | Sveikasis skaičius |
| `LineNumber` | Pasirinktina | Tikrasis |
| `PositionNumber` | Pasirinktina | Eilutė |
| `IsConsumptionEnded` | Pasirinktina | Bulio logika |
| `ErrorCause` | Pasirinktina | Išvardiimas \| (nėra \| medžiagų mašinos \| valdymostafo), extensible |

### <a name="time-used-for-operation-route-card-message"></a>Operacijos laiko (maršruto kortelės) pranešimas

Laiko, *kuris naudojamas operacijos (maršruto kortelės)* pranešimui, `_messageType` vertė `ProdProductionOrderRouteCard` yra. Toliau pateikiamoje lentelėje rodomi laukai, kuriuos palaiko šis pranešimas.

| Lauko pavadinimas | Būsena | Tipas |
|---|---|---|
| `ProductionOrderNumber` | Privalomas | Eilutė |
| `JournalNameId` | Pasirinktina | Eilutė |
| `RouteCardLines` | Privalomas | Eilučių (bent vienos), kurių kiekvienoje yra mokamų kūstų, aprašytų toliau esančioje lentelėje, sąrašas |

Toliau pateikiamoje lentelėje rodomi laukai, kuriuos palaiko `RouteCardLines` kiekviena pranešimo `ProdProductionOrderRouteCard` skyriaus eilutė.

| Lauko pavadinimas | Būsena | Tipas |
|---|---|---|
| `OperationNumber` | Privalomas | Privaloma, integer |
| `OperationPriority` | Pasirinktina | Išvardimis \| (pirminis antrinis1 \| antrinis2... \|\| Antrinis 20) |
| `OperationId` | Pasirinktina | Eilutė |
| `OperationsResourceId` | Pasirinktina | Eilutė |
| `Worker` | Pasirinktina | Eilutė |
| `HoursRouteCostCategoryId` | Pasirinktina | Eilutė |
| `QuantityRouteCostCategoryId` | Pasirinktina | Eilutė |
| `HourlyRate` | Pasirinktina | Tikrasis |
| `Hours` | Pasirinktina | Tikrasis |
| `GoodQuantity` | Pasirinktina | Tikrasis |
| `ErrorQuantity` | Pasirinktina | Tikrasis |
| `CatchWeightGoodQuantity` | Pasirinktina | Tikrasis |
| `CatchWeightErrorQuantity` | Pasirinktina | Tikrasis |
| `QuantityPrice` | Pasirinktina | Tikrasis |
| `ProcessingPercentage` | Pasirinktina | Tikrasis |
| `ConsumptionDate` | Pasirinktina | Data |
| `TaskType` | Pasirinktina | Išvardijimo (QueueBefore \| nustatymo procesas \|\| persidengia su transportavimo darbo laiko \|\| neefektyviais \| elementais) |
| `ErrorCause` | Pasirinktina | Išvardiimas \| (nėra \| medžiagų mašinos \| valdymostafo), extensible |
| `OperationCompleted` | Pasirinktina | Bulio logika |
| `BOMConsumption` | Pasirinktina | Bulio logika |
| `ReportAsFinished` | Pasirinktina | Bulio logika |

### <a name="end-production-order-message"></a>Baigti gamybos užsakymo pranešimą

Pabaigos *gamybos užsakymo* pranešimo vertė `_messageType``ProdProductionOrderEnd` yra. Toliau pateikiamoje lentelėje rodomi laukai, kuriuos palaiko šis pranešimas.

| Lauko pavadinimas | Būsena | Tipas |
|---|---|---|
| `ProductionOrderNumber` | Privalomas | Eilutė |
| `ExecutedDateTime` | Pasirinktina | DateTime |
| `EndedDate` | Pasirinktina | Data |
| `UseTimeAndAttendanceCost` | Pasirinktina | Bulio logika |
| `AutoReportAsFinished` | Pasirinktina | Bulio logika |
| `AutoUpdate` | Pasirinktina | Bulio logika |

## <a name="receive-feedback-about-the-state-of-a-message"></a>Gauti grįžtamąjį ryšį apie pranešimo būseną

Po to, kai MES išsiunčia pranešimą tiekimo grandinės valdymui, gali būti svarbu tiekimo grandinės valdymui, kad būtų grąžinamas grįžtamasis ryšys apie pranešimo būseną. Pateikiami keli atvejų, kai šis veikimo būdas gali būti svarbus, pavyzdžiai:

- Nėra asmens, atsakingo už MES integravimo priežiūrą.
- Asmuo, atsakingas už MES integravimo priežiūrą, nori būti persiųstas el. paštu, kai pranešimas nepavyksta, taigi jis žino, kad turi imtis veiksmų.
- MES turi rodyti klaidos pranešimą, kad informuos darbo laiko operatorių arba jau iš IT padalinio, kad turi imtis veiksmų.
- MES turi perskaičiuoti užsakymo grafiką po to, kai jis gauna klaidos pranešimą (pvz., dėl to, kad nepavyko pradėti gamybos užsakymo).

Tokiais atvejais galite pasinaudoti standartine tiekimo grandinės valdymo įspėjimo funkcija. Informacijos apie tai, kaip veikia standartiniai įspėjimai, ieškokite toliau pateikiamame ištetelyje:

- Žinyno tema: [įspėjimų peržiūra](../../fin-ops-core/fin-ops/get-started/alerts-overview.md)
- Vaizdo įrašas: [įspėjimo taisyklės parinktys Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=cpzimwOjicM&ab_channel=MicrosoftDynamics365)

Pavyzdžiui, galite nustatyti šiuos įspėjimus, kad galėtumėte pateikti atsiliepimus apie pranešimo būseną:

- Kurti verslo įvykį ("Siųsti išoriškai"), kuris naudojamas, kai pranešimas *·* nepavyko.
- Siųsti pranešimą ir el. laišką IT administratoriui arba gamybos laiko vadybininkui.
