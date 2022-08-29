---
title: Integravimas trečiosios šalies gamybos vykdymo sistemose
description: Šiame straipsnyje paaiškinama, kaip integruoti "Microsoft Dynamics 365 Supply Chain Management " į trečiosios šalies gamybos vykdymo sistemą (MES).
author: johanhoffmann
ms.date: 08/09/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-10-01
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 8629ef2581a114609d14999a3c1fc48b49c988e0
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336222"
---
# <a name="integrate-with-third-party-manufacturing-execution-systems"></a>Integravimas trečiosios šalies gamybos vykdymo sistemose

[!include [banner](../includes/banner.md)]

Kai kurios gamybos organizacijos, kurios naudoja "Microsoft Dynamics 365 Supply Chain Management " naudoja gimtąją "Dynamics 365" funkciją, kad galėtų kontroliuoti savo įrenginių, įrangos ir personalo gamybos veiklą. Tačiau kitos gamybos organizacijos, ypač tos, kurios turi išplėstinių gamybos reikalavimų, naudoja trečiosios šalies gamybos vykdymo sistemą (MES). Organizacijos gali pasirinkti trečiosios šalies MES sprendimą, nes, pavyzdžiui, jis specialiai pritaikytas jų vertikaliai pramonei.

Integruotuose sprendimuose duomenų mainai yra visiškai automatizuoti ir vyksta beveik realiuoju laiku. Todėl duomenys laikomi dabartiniai abiejose sistemose ir nereikia įvesti duomenų neautomatiniu būdu. Pavyzdžiui, kai medžiagų suvartojimas registruojamas MES, integracija užtikrina, kad "Dynamics 365" registruojamas ir tas pats suvartojimas. Todėl naujausiais atsargų įrašais galima naudotis kitiems svarbiams procesams, pvz., planavimui ir pardavimui.

Sprendimas yra greitesnis, paprastesnis ir paprastesnis tiekimo grandinės valdymo vartotojams, kad jie galėtų integruotis su trečiosios šalies MES. Jis siūlo šias funkcijas:

- Verslo įvykiai ir sąsajos, kurios palaiko pagrindinius [gamybos vykdymo procesus](#processes-available-for-mes-integration)
- Centralizuota skelbimų skelbimų skelbimų sritis, kurioje galite sekti įvykių apdorojimo retrospektyvą ir šalinti bei taisyti procesus, kurie nepavyko

Toliau esanti iliustracija pateikia įprastą verslo įvykių, procesų ir pranešimų, kurie keičiamasi integruotuose sprendimuose, rinkinį.

![Įprastas integravimo scenarijus.](media/3p-mes-scenario.png "Įprastas integravimo scenarijus.")

## <a name="turn-on-the-mes-integration-feature"></a>Įjungti MES integravimo funkciją

Prieš tai kai galėsite naudoti šią priemonę, administratorius turi įjungti ją jūsų sistemoje, kaip aprašyta toliau pateiktoje procedūroje.

1. Eikite į **Sistemos administravimas \> Sąranka \> Licencijos konfigūracija**.
1. Įsitikinkite, kad **laiko ir lankomumo** licencijos raktas įgalintas (rodoma varnelė). Šis licencijos raktas yra būtinas, kadangi jis valdo gamybos vykdymo sistemos funkcijas ir duomenis. Jei ji neįgalinta, atlikite šiuos veiksmus:
    1. Įdėkite savo sistemą į priežiūros režimą kaip aprašyta [Priežiūros režime](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
    1. Licencijos konfigūracijos **puslapyje** pažymėkite žymės langelį **Laikas ir lankomumas**.
    1. Išjungti priežiūros režimą, kaip aprašyta priežiūros [režimu](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)
1. Eikite į **sistemos administravimo \> darbo sričių \> funkcijų valdymą**.
1. Norėdami įjungti [gamybos vykdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sistemos integravimo funkciją, naudokite *funkcijų valdymo darbo* sritį. (Kaip ir tiekimo grandinės valdymo versija 10.0.29, ši funkcija veikia pagal numatytąjį nustatymą.)

## <a name="processes-available-for-mes-integration"></a>Galimi MES integravimo procesai

Galite įgalinti bet kurį arba visus šiuos integravimo procesus.

| Proceso pavadinimas | Aprašymas |
|---|---|
| Išleisti gamybos užsakymus ir gamybos užsakymo būsenos keitimo verslo įvykius | Šis procesas suteikia verslo įvykį, kurį MES gali klausyti, norėdami gauti informacijos apie gamybos užsakymus, kurie turi būti pateikti. Tikimasi, kad su gamybos užsakymu susiję nuorodos duomenys bus bendrai naudojami tiekimo grandinės valdymo metu su MES per atvirą duomenų protokolą (OData) arba duomenų objektus. |
| Gamybos užsakymo pradžia | Šis procesas suteikia tiekimo grandinės valdymą ir informaciją apie gamybos užsakymus, kurie pradėti naudojant MES. Taip užtikrinama, kad abiejose sistemose yra naujausias visų gamybos veiklų rodinys. |
| Ataskaita apie pagamintą arba nurašytą kiekį | Šis procesas suteikia tiekimo grandinės valdymą ir informaciją apie gerų ir klaidų kiekius, kurie pranešami gamybos užduotyje naudojant MES. Taip užtikrinama, kad darbo laiko prižiūrėtojai turėtų naujausias gamybos plano eigos vaizdą. |
| Ataskaita apie medžiagų suvartojimą | Šis procesas teikia tiekimo grandinės valdymą, remiantis MES, informacija apie suvartotų medžiagų kiekį. Ji atlieka naujausias atsargų įrašus, prieinamus kitiems svarbiams procesams, pvz., planavimui ir pardavimui. |
| Ataskaitai skirtas laikas, sunaudotas operacijai | Šis procesas suteikia tiekimo grandinės valdymą ir informaciją apie laiką, kuris naudojamas specialiai operacijai. |
| Baigti gamybos užsakymą | Šis procesas informuoja tiekimo grandinės valdymą, kad MES atnaujino gamybos užsakymą į galutinę būseną *Baigta*. Ši būsena nurodo, kad pagal gamybos užsakymą daugiau kiekių nebus gaminama. |

## <a name="monitor-incoming-messages"></a>Gautų pranešimų stebėjimas

Norėdami stebėti į sistemą gaunamus pranešimus, atidarykite gamybos **vykdymo sistemų integravimo** puslapį. Galima peržiūrėti, apdoroti ir šalinti triktis.

Visi konkretaus gamybos užsakymo pranešimai apdorojami jų gavimo tvarka. Tačiau skirtingų gamybos užsakymų pranešimai gali būti apdorojami ne gavimo sekoje, nes paketinės užduotys apdorojamos lygiagrečiai. Jei triktis, paketinė užduotis bandys apdoroti kiekvieną pranešimą tris kartus prieš nustatydami būseną *Nepavyko*.

## <a name="call-the-api"></a>Iškviesti API

Norėdami iškviesti MES integravimo API, siųskite užklausą `POST` šiuo galinio punkto URL:

`/api/services/SysMessageServices/SysMessageService/SendMessage`

Jūsų siunčiamos užklausos tekstas turėtų būti panašus į šį pavyzdį. Pakeiskite, ir`_companyId``_messageType`, jei reikia`_messageContent`, vertes. Informacijos apie įvairius pranešimų tipus, kuriuos PALAIKO API, ir kaip kurti jų turinį, ieškokite kitame skyriuje.

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

*Pradžios gamybos užsakymo* pranešimo vertė `_messageType` yra `ProdProductionOrderStart`. Toliau pateikiamoje lentelėje rodomi laukai, kuriuos palaiko šis pranešimas.

| Lauko pavadinimas | Būsena | Tipas |
|---|---|---|
| `ProductionOrderNumber` | Privalomas | Eilutė |
| `StartedQuantity` | Pasirinktina | Tikrasis |
| `StartedDate` | Pasirinktina | Data |
| `AutomaticBOMConsumptionRule` | Pasirinktina | Išvardijimas (FlushingPrincip \| visada niekada \|) |

### <a name="report-as-finished-message"></a>Pranešti apie pabaigimo pranešimą

*Pranešimo, kuris yra baigtas*, vertė `_messageType` yra `ProdProductionOrderReportFinished`. Toliau pateikiamoje lentelėje rodomi laukai, kuriuos palaiko šis pranešimas.

| Lauko pavadinimas | Būsena | Tipas |
|---|---|---|
| `ProductionOrderNumber` | Privalomas | Eilutė |
| `ReportFinishedLines` | Privalomas | Eilučių (bent vienos), kurių kiekvienoje yra mokamų kūstų, aprašytų toliau esančioje lentelėje, sąrašas |

Toliau pateikiamoje lentelėje rodomi laukai, kuriuos palaiko kiekviena `ReportFinishedLines` pranešimo `ProdProductionOrderReportFinished` skyriaus eilutė.

| Lauko pavadinimas | Būsena | Tipas |
|---|---|---|
| `LineNumber` | Pasirinktina | Tikrasis |
| `ItemNumber` | Pasirinktina | Eilutė|
| `ProductionType` | Pasirinktina | Išvardiimas (MainItem \| formulės \| KS \| Co_Product \| By_Product \| Nėra), extensible |
| `ReportedErrorQuantity` | Pasirinktina | Tikrasis|
| `ReportedGoodQuantity` | Pasirinktina | Tikrasis|
| `ReportedErrorCatchWeightQuantity` | Pasirinktina | Tikrasis |
| `ReportedGoodCatchWeightQuantity` | Pasirinktina | Tikrasis |
| `AcceptError` | Pasirinktina | Išvardimis (Taip \| ne) |
| `ErrorCause` | Pasirinktina | Išvardiimas \| (nėra medžiagų \|\| mašinos valdymostafo), extensible |
| `ExecutedDateTime` | Pasirinktina | DateTime |
| `ReportAsFinishedDate` | Pasirinktina | Data |
| `AutomaticBOMConsumptionRule` | Pasirinktina | Išvardijimas (FlushingPrincip \| visada niekada \|) |
| `AutomaticRouteConsumptionRule` | Pasirinktina |Išvardiimas (RouteDependent \| visada niekada \|) |
| `RespectFlushingPrincipleDuringOverproduction` | Pasirinktina | Išvardimis (Taip \| ne) |
| `ProductionJournalNameId` | Pasirinktina | Eilutė |
| `PickingListProductionJournalNameId` | Pasirinktina | Eilutė|
| `RouteCardProductionJournalNameId` | Pasirinktina | Eilutė |
| `FromOperationNumber` | Pasirinktina | Sveikasis skaičius|
| `ToOperationNumber` | Pasirinktina | Sveikasis skaičius|
| `InventoryLotId` | Pasirinktina | Eilutė |
| `BaseValue` | Pasirinktina | Eilutė |
| `EndJob` | Pasirinktina | Išvardimis (Taip \| ne) |
| `EndPickingList` | Pasirinktina | Išvardimis (Taip \| ne) |
| `EndRouteCard` | Pasirinktina | Išvardimis (Taip \| ne) |
| `PostNow` | Pasirinktina | Išvardimis (Taip \| ne) |
| `AutoUpdate` | Pasirinktina | Išvardimis (Taip \| ne) |
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
| `InventoryDimension1`– `InventoryDimension12` | Pasirinktina | Eilutė |

12 extensible dimensijų (`InventoryDimension1` per `InventoryDimension12`) reikalauja pritaikymo, bet ne visada naudojamos. Daugiau informacijos apie jas rasite naujų atsargų [dimensijų pridėjimas naudojant plėtinį](../../fin-ops-core/dev-itpro/extensibility/inventory-dimensions.md).

### <a name="material-consumption-picking-list-message"></a>Medžiagų suvartojimo (išrinkimo sąrašas) pranešimas

Medžiagų suvartojimo *(išrinkimo dokumentų) pranešimas* yra `_messageType` vertė `ProdProductionOrderPickingList`. Toliau pateikiamoje lentelėje rodomi laukai, kuriuos palaiko šis pranešimas.

| Lauko pavadinimas | Būsena | Tipas |
|---|---|---|
| `ProductionOrderNumber` | Privalomas | Eilutė |
| `JournalNameId` | Pasirinktina | Eilutė |
| `PickingListLines` | Privalomas | Eilučių (bent vienos), kurių kiekvienoje yra mokamų kūstų, aprašytų toliau esančioje lentelėje, sąrašas |

Toliau pateikiamoje lentelėje rodomi laukai, kuriuos palaiko kiekviena `PickingListLines` pranešimo `ProdProductionOrderPickingList` skyriaus eilutė.

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
| `IsConsumptionEnded` | Pasirinktina | Išvardimis (Taip \| ne) |
| `ErrorCause` | Pasirinktina | Išvardiimas \| (nėra medžiagų \|\| mašinos valdymostafo), extensible |
| `InventoryLotId` | Pasirinktina | Eilutė |

### <a name="time-used-for-operation-route-card-message"></a>Operacijos laiko (maršruto kortelės) pranešimas

Laiko, *kuris naudojamas operacijos (maršruto kortelės) pranešimui*, vertė `_messageType` yra `ProdProductionOrderRouteCard`. Toliau pateikiamoje lentelėje rodomi laukai, kuriuos palaiko šis pranešimas.

| Lauko pavadinimas | Būsena | Tipas |
|---|---|---|
| `ProductionOrderNumber` | Privalomas | Eilutė |
| `JournalNameId` | Pasirinktina | Eilutė |
| `RouteCardLines` | Privalomas | Eilučių (bent vienos), kurių kiekvienoje yra mokamų kūstų, aprašytų toliau esančioje lentelėje, sąrašas |

Toliau pateikiamoje lentelėje rodomi laukai, kuriuos palaiko kiekviena `RouteCardLines` pranešimo `ProdProductionOrderRouteCard` skyriaus eilutė.

| Lauko pavadinimas | Būsena | Tipas |
|---|---|---|
| `OperationNumber` | Privalomas | Sveikasis skaičius |
| `OperationPriority` | Pasirinktina | Išvardimis (pirminis antrinis1 \| antrinis2 \| ... \|\| Antrinis 20) |
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
| `TaskType` | Pasirinktina | Išvardijimo (QueueBefore nustatymo procesas \| persidengia \|\| su transportavimo \| darbo laiko \| neefektyviais \| elementais) |
| `ErrorCause` | Pasirinktina | Išvardiimas \| (nėra medžiagų \|\| mašinos valdymostafo), extensible |
| `OperationCompleted` | Pasirinktina | Išvardimis (Taip \| ne) |
| `BOMConsumption` | Pasirinktina | Išvardimis (Taip \| ne) |
| `ReportAsFinished` | Pasirinktina | Išvardimis (Taip \| ne) |

### <a name="end-production-order-message"></a>Baigti gamybos užsakymo pranešimą

*Pabaigos gamybos užsakymo* pranešimo vertė `_messageType` yra `ProdProductionOrderEnd`. Toliau pateikiamoje lentelėje rodomi laukai, kuriuos palaiko šis pranešimas.

| Lauko pavadinimas | Būsena | Tipas |
|---|---|---|
| `ProductionOrderNumber` | Privalomas | Eilutė |
| `ExecutedDateTime` | Pasirinktina | DateTime |
| `EndedDate` | Pasirinktina | Data |
| `UseTimeAndAttendanceCost` | Pasirinktina | Išvardimis (Taip \| ne) |
| `AutoReportAsFinished` | Pasirinktina | Išvardimis (Taip \| ne) |
| `AutoUpdate` | Pasirinktina | Išvardimis (Taip \| ne) |

## <a name="other-production-information"></a>Kita gamybos informacija

Pranešimai palaiko veiksmus ar įvykius, kurie vyksta darbo laiko metu. Jie apdorojami naudojant MES integravimo sistemą, aprašytą šiame straipsnyje. Dizaine laikoma, kad kita nuorodos informacija, kuri bus bendrai naudojama su MES (pvz., su produktu susijusi informacija arba KS ar maršrutas (su konkrečiais nustatymo ir konfigūravimo laikais)), naudojama tam tikroje gamybos užsakyme, [bus](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#data-entities) nuskaitoma iš sistemos, naudojant duomenų objektus per rinkmenos perdavimą ar OData.

## <a name="receive-feedback-about-the-state-of-a-message"></a>Gauti grįžtamąjį ryšį apie pranešimo būseną

Po to, kai MES išsiunčia pranešimą tiekimo grandinės valdymui, gali būti svarbu tiekimo grandinės valdymui, kad būtų grąžinamas grįžtamasis ryšys apie pranešimo būseną. Pateikiami keli atvejų, kai šis veikimo būdas gali būti svarbus, pavyzdžiai:

- Nėra asmens, atsakingo už MES integravimo priežiūrą.
- Asmuo, atsakingas už MES integravimo priežiūrą, nori būti persiųstas el. paštu, kai pranešimas nepavyksta, taigi jis žino, kad turi imtis veiksmų.
- MES turi rodyti klaidos pranešimą, kad informuos darbo laiko operatorių arba jau iš IT padalinio, kad turi imtis veiksmų.
- MES turi perskaičiuoti užsakymo grafiką po to, kai jis gauna klaidos pranešimą (pvz., dėl to, kad nepavyko pradėti gamybos užsakymo).

Tokiais atvejais galite pasinaudoti standartine tiekimo grandinės valdymo įspėjimo funkcija. Informacijos apie tai, kaip veikia standartiniai įspėjimai, ieškokite toliau pateikiamame ištetelyje:

- Žinyno straipsnis: [įspėjimų peržiūra](../../fin-ops-core/fin-ops/get-started/alerts-overview.md)
- Vaizdo įrašas: [įspėjimo taisyklių parinktys finansinėse ir operacijose](https://www.youtube.com/watch?v=cpzimwOjicM&ab_channel=MicrosoftDynamics365)

Pavyzdžiui, galite nustatyti šiuos įspėjimus, kad galėtumėte pateikti atsiliepimus apie pranešimo būseną:

- Kurti verslo įvykį ("Siųsti išoriškai"), kuris naudojamas, kai pranešimas *nepavyko*.
- Siųsti pranešimą ir el. laišką IT administratoriui arba gamybos laiko vadybininkui.

