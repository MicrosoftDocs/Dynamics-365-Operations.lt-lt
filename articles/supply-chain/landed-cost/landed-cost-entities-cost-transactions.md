---
title: Kaštų operacijos objektai
description: Šiame straipsnyje pateikiama informacija apie išlaidų operacijų objektus, kurie įgalina išlaidų vertę padalinti tarp išlaidų srities turinio, naudojant parinkimo metodą.
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
ms.openlocfilehash: 0084d47bf85050749b2668d273db07670aaeae2a
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/15/2022
ms.locfileid: "9166810"
---
# <a name="cost-transaction-entities"></a>Kaštų operacijos objektai

[!include [banner](../includes/banner.md)]

## <a name="apportionment"></a>Paskyra

Įkainotos išlaidos įgalina išlaidų vertę padalinti į išlaidų srities turinį (reisą, siuntimo konteinerį ir t. t.) pasirinktą priskyrimo metodą. Šis konfigūravimo metodas nustatomas kaip automatinių išlaidų konfigūravimo pagal verslo taisykles dalis. Sukūrus reiso eilutę, jis ištraukiamas kaip išlaidų dalis.

### <a name="configure-the-apportionment-mapping-for-use-with-data-entities"></a>Konfigūruokite priskyrimo susiejimą, kad jį būtų galima naudoti su duomenų objektais

Kai išlaidos sukuriamos iš išorinio šaltinio, pvz., krovinių ekspeditoraus, kad išorinis šaltinis negali nurodyti pageidaujamo savikainos naudojimo būdo. Priskyrimo susiejimas nurodo numatytąjį kiekvieno išlaidų tipo kodo priskyrimo metodą. Apportionment susiejimo lentelę galima pasiekti iš Apportionment **susiejimo puslapio "Microsoft** " (Dynamics 365 Supply Chain Management **įkainojimo įkainojimo \> nustatymo Apportionment susiejimas \>).**

Jei buvo apibrėžtas susiejimo derinys ir išlaidų, kurios atitinka išlaidų tipo kodą, sukuriamos naudojant išlaidų operacijos objektą, susietas priskyrimo metodas bus naudojamas vietoje bet kokios vertės, kuri buvo pateikta objektui.

Jei susiejimo lentelėje nėra jokios vertės, o vertė pateikta objektui, bus naudojama pateikta vertė.

Jei susiejimo lentelėje arba įraše, pateiktame objektui, nėra jokių verčių, sukurti nepavyks.

### <a name="apportionment-mapping-itmapportionmentmapping"></a>Priskyrimo susiejimas (ITMApportionmentMapping)

Priskyrimo susiejimo objektas (`ITMApportionmentMapping`) sukuria priskyrimo susiejimo ryšius ir įgalina vartotojus kurti arba naujinti įrašus.

| Vardas | Susiejimas | Duomenų tipas | Raktas | Privalomas |
|---|---|---|---|---|
| Paskirstymo metodas | ITMApportionmentMapping.ApportionmentMethod | Int | Ne | Ne |
| Išlaidų tipo kodas | ITMApportionmentMapping.ShipCostTypeId | Nvarchar(20) | **Taip** | Ne |

## <a name="voyage-costs-itmcosttransvoyageentity"></a>Reiso išlaidos (ITMCostTransVoyageEntity)

Reiso išlaidų objektas (`ITMCostTransVoyageEntity`) sukuria reiso išlaidų operacijas, taikomas reiso lygiu. Importavimo proceso metu sistema naudoja Kategorijos **ir** Apportionment **metodo vertes,** įtrauktas į objektą, kad nustatytų, kaip išlaidų vertė yra įtraukta į reiso turinį.

| Vardas | Susiejimas | Duomenų tipas | Raktas | Privalomas |
|---|---|---|---|---|
| Paskirstymo metodas | ITMCostTrans.ApportionmentMethod | Int | Ne | Ne |
| Išlaidų vertė | ITMCostTrans.CostValue | Skaitinis(32, 6) | Ne | Ne |
| Valiuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Ne | **Taip** |
| Eilutės numeris | ITMCostTrans.LineNum | Skaitinis(32, 16) | **Taip** | Ne |
| Susietas išlaidų tipas | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Ne | Ne |
| Mažiausios išlaidos | ITMCostTrans.MinCostAmount | Skaitinis(32, 6) | Ne | Ne |
| Kategorija | ITMCostTrans.ShipCostCategory | Int | Ne | Ne |
| Išlaidų tipo kodas | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Ne | Ne |
| Įmonė | ITMCostTrans.ShipDataArea | Nvarchar(4) | Ne | **Taip** |
| Reisas | ITMCostTrans.TransRecId | Nvarchar(20) | **Taip** | Ne |
| Prekės PVM grupė | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Ne | Ne |

## <a name="shipping-container-costs-itmcosttransshippingcontainerentity"></a>Siuntimo konteinerio išlaidos (ITMCostTransShippingContainerEntity)

Siuntimo konteinerio savikainos objektas (`ITMCostTransShippingContainerEntity`) sukuria siuntimo konteinerio išlaidas, taikomas siuntimo konteinerio lygiu. Importavimo proceso metu sistema naudoja Kategorijos ir Apportionment **metodo vertes,** **kurios** įtrauktos į objektą, kad nustatytų, kaip išlaidų vertė yra pateikiama siuntimo konteinerio turinyje.

Sujungti **,** atkarpos **ir** susietosios **atkarpos** laukai yra specifiniai įrašams, kuriuose **išlaidų srities vertė yra** siuntimo *konteineris*. Todėl jų nėra kitų išlaidų sričių duomenų objektuose.

| Vardas | Susiejimas | Duomenų tipas | Raktas | Privalomas |
|---|---|---|---|---|
| Sujungti | ITMCostTrans.AggregatedCost | Int | Ne | Ne |
| Paskirstymo metodas | ITMCostTrans.ApportionmentMethod | Int | Ne | Ne |
| Išlaidų vertė | ITMCostTrans.CostValue | Skaitinis(32, 6) | Ne | Ne |
| Valiuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Ne | **Taip** |
| Eilutės numeris | ITMCostTrans.LineNum | Skaitinis(32, 16) | **Taip** | Ne |
| Susietas išlaidų tipas | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Ne | Ne |
| Susieta atkarpa | ITMCostTrans.LinkLegId | Nvarchar(20) | Ne | Ne |
| Mažiausios išlaidos | ITMCostTrans.MinCostAmount | Skaitinis(32, 6) | Ne | Ne |
| Siuntimo konteineris | ITMCostTrans.TransRecId | Nvarchar(20) | **Taip** | Ne |
| Kategorija | ITMCostTrans.ShipCostCategory | Int | Ne | Ne |
| Išlaidų tipo kodas | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Ne | Ne |
| Įmonė | ITMCostTrans.ShipDataArea | Nvarchar(4) | Ne | **Taip** |
| Reisas | ITMCostTrans.TransRecId | Nvarchar(20) | **Taip** | Ne |
| Atkarpa | ITMCostTrans.ShipLegId | Nvarchar(20) | Ne | Ne |
| Prekės PVM grupė | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Ne | Ne |

## <a name="folio-costs-itmcosttransfolioentity"></a>Registracijos išlaidos (ITMCostTransFolioEntity)

Išlaidų objekto () registracijos objektas`ITMCostTransFolioEntity` sukuria išlaidų operacijų įrašus, kurie taikomi registracijos lygiui. Importavimo proceso metu sistema naudoja Kategorijos **ir** Apportionment **metodo vertes,** kurios įtrauktos į objektą, kad nustatytų, kaip išlaidų vertė yra įtraukta į kiekvienos lentelės turinį.

| Vardas | Susiejimas | Duomenų tipas | Raktas | Privalomas |
|---|---|---|---|---|
| Paskirstymo metodas | ITMCostTrans.ApportionmentMethod | Int | Ne | Ne |
| Išlaidų vertė | ITMCostTrans.CostValue | Skaitinis(32, 6) | Ne | Ne |
| Valiuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Ne | **Taip** |
| Eilutės numeris | ITMCostTrans.LineNum | Skaitinis(32, 16) | **Taip** | Ne |
| Susietas išlaidų tipas | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Ne | Ne |
| Mažiausios išlaidos | ITMCostTrans.MinCostAmount | Skaitinis(32, 6) | Ne | Ne |
| Kategorija | ITMCostTrans.ShipCostCategory | Int | Ne | Ne |
| Išlaidų tipo kodas | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Ne | Ne |
| Įmonė | ITMCostTrans.ShipDataArea | Nvarchar(4) | Ne | **Taip** |
| Registravimo lapas | ITMCostTrans.TransRecId | Nvarchar(20) | **Taip** | Ne |
| Prekės PVM grupė | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Ne | Ne |

## <a name="purchase-order-costs-itmcosttranspurchaseentity"></a>Pirkimo užsakymo išlaidos (ITMCostTransPurchaseEntity)

Pirkimo užsakymo išlaidų objektas (`ITMCostTransPurchaseEntity`) sukuria išlaidų operacijas, kurios taikomos pirkėjo užsakymo antraštei. Importavimo proceso metu sistema naudoja Kategorijos **ir** Apportionment **metodo vertes,** kurios įtrauktos į objektą, kad nustatytų, kaip išlaidų vertė yra įtraukta į kiekvienos lentelės turinį.

| Vardas | Susiejimas | Duomenų tipas | Raktas | Privalomas |
|---|---|---|---|---|
| Paskirstymo metodas | ITMCostTrans.ApportionmentMethod | Int | Ne | Ne |
| Išlaidų vertė | ITMCostTrans.CostValue | Skaitinis(32, 6) | Ne | Ne |
| Valiuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Ne | **Taip** |
| Eilutės numeris | ITMCostTrans.LineNum | Skaitinis(32, 16) | **Taip** | Ne |
| Susietas išlaidų tipas | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Ne | Ne |
| Mažiausios išlaidos | ITMCostTrans.MinCostAmount | Skaitinis(32, 6) | Ne | Ne |
| Pirkimo užsakymas | ITMCostTrans.TransRecId | Nvarchar(20) | **Taip** | Ne |
| Kategorija | ITMCostTrans.ShipCostCategory | Int | Ne | Ne |
| Išlaidų tipo kodas | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Ne | Ne |
| Įmonė | ITMCostTrans.ShipDataArea | Nvarchar(4) | Ne | **Taip** |
| Prekės PVM grupė | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Ne | Ne |

## <a name="item-costs-itmcosttransitementity"></a>Prekių išlaidos (ITMCostTransItemEntity)

Prekės išlaidų objektas (`ITMCostTransItemEntity`) sukuria išlaidų operacijas, kurios taikomos prekės lygiui. Šis objektas yra konkretus pirkimo užsakymo eilučių prekėms. Išlaidų vertė eilutei taikoma visa.

Koregavimo **sumos ir** **vertės koregavimo** laukai yra specifiniai eilutės lygio išlaidų sritims. Todėl jų nėra kitų išlaidų sričių duomenų objektuose.

| Vardas | Susiejimas | Duomenų tipas | Raktas | Privalomas |
|---|---|---|---|---|
| Koregavimo suma | ITMCostTrans.AdjustmentAmount | Skaitinis(32, 6) | Ne | Ne |
| Išlaidų vertė | ITMCostTrans.CostValue | Skaitinis(32, 6) | Ne | Ne |
| Valiuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Ne | **Taip** |
| Eilutės numeris | ITMCostTrans.LineNum | Skaitinis(32, 16) | **Taip** | Ne |
| Susietas išlaidų tipas | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Ne | Ne |
| Mažiausios išlaidos | ITMCostTrans.MinCostAmount | Skaitinis(32, 6) | Ne | Ne |
| Pirkimo užsakymas | ITMCostTrans.TransRecId | Nvarchar(20) | **Taip** | Ne |
| Pirkimo užsakymo eilutės numeris | ITMCostTrans.TransRecId | Nvarchar(20) | **Taip** | Ne |
| Kategorija | ITMCostTrans.ShipCostCategory | Int | Ne | Ne |
| Išlaidų tipo kodas | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Ne | Ne |
| Įmonė | ITMCostTrans.ShipDataArea | Nvarchar(4) | Ne | **Taip** |
| Prekės PVM grupė | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Ne | Ne |
| Vertės koregavimas | ITMCostTrans.ValueAdjustmentMethod | Int | Ne | Ne |

## <a name="transfer-line-costs-itmcosttranstransferlineentity"></a>Perkėlimo eilutės išlaidos (ITMCostTransTransferLineEntity)

Perkėlimo eilutės savikainos objektas (`ITMCostTransTransferLineEntity`) sukuria išlaidų operacijas, kurios taikomos perkėlimo užsakymo eilutės lygiui. Šių išlaidų vertė visiškai taikoma perkėlimo užsakymo eilutei.

Koregavimo **sumos ir** **vertės koregavimo** laukai yra specifiniai eilutės lygio išlaidų sritims. Todėl jų nėra kitų išlaidų sričių duomenų objektuose.

| Vardas | Susiejimas | Duomenų tipas | Raktas | Privalomas |
|---|---|---|---|---|
| Koregavimo suma | ITMCostTrans.AdjustmentAmount | Skaitinis(32, 6) | Ne | Ne |
| Išlaidų vertė | ITMCostTrans.CostValue | Skaitinis(32, 6) | Ne | Ne |
| Valiuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Ne | **Taip** |
| Eilutės numeris | ITMCostTrans.LineNum | Skaitinis(32, 16) | **Taip** | Ne |
| Susietas išlaidų tipas | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Ne | Ne |
| Mažiausios išlaidos | ITMCostTrans.MinCostAmount | Skaitinis(32, 6) | Ne | Ne |
| Kategorija | ITMCostTrans.ShipCostCategory | Int | Ne | Ne |
| Išlaidų tipo kodas | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Ne | Ne |
| Įmonė | ITMCostTrans.ShipDataArea | Nvarchar(4) | Ne | **Taip** |
| Perkėlimo užsakymas | ITMCostTrans.TransRecId | Nvarchar(20) | **Taip** | Ne |
| Perkėlimo užsakymo eilutės numeris | ITMCostTrans.TransRecId | Nvarchar(20) | **Taip** | Ne |
| Prekės PVM grupė | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Ne | Ne |
| Vertės koregavimas | ITMCostTrans.ValueAdjustmentMethod | Int | Ne | Ne |

### <a name="transaction-table"></a>Operacijos lentelė

Išlaidų operacijos įrašas siejamas su išlaidų sritis per operacijos lentelės numerio priskyrimą (`TransTableId`). Kai reikia tam tikrų lentelės identifikavimo numerių, objektai skaidomi remiantis šiomis vertėmis, kad objektas būtų kiekvienoje išlaidų srityje.

Operacijų lentelės vertė (`TransTableId`) išlaidų operacijos objekto pasirinkimo metu netiesiogiai.

### <a name="calculated-fields"></a>Suskaičiuoti laukai

Toliau nurodytų laukų negalima įterpti arba atnaujinti naudojant išlaidų operacijos objektą, nes šie laukai nustatomi tik tada, kai atlikti specialūs veiksmai su reiso įrašu:

- **Įvertinta savikaina** – šis laukas nustatomas, kai reiso (pirkimo užsakymo) arba perkėlimo SF užregistruojama.
- **Įvertinta išlaidų valiuta** – šis laukas nustatomas, kai reiso (pirkimo užsakymo) arba perkėlimo SF užregistruojama.
- **Faktinės** išlaidos – šis laukas nustatomas užregistrus tiekėjo SF. Jis susietas su išlaidomis.

### <a name="find-auto-costs"></a>Rasti aut. išlaidas

Automatinės **savikainos** radimo mygtukas, kurį galima naudoti kiekvienoje išlaidų srityje (reisas, siuntimo konteineris ir t. t.) suteikia būdą atnaujinti tos savikainos srities išlaidų operacijas iš konfigūracijos lentelių informacijos. Pasirinkus išlaidų srities mygtuką sistema išvalo esamas tos išlaidų srities išlaidas ir kuria naujus įrašus remdamasi dabartine automatinio išlaidų nustatymo lentelių konfigūracija.

Išlaidų operacijų įrašai, sukurti naudojant duomenų objektą, pažymėti kaip importuoti. Šie įrašai nėra naikinami pasirinkus Rasti automatines **išlaidas**, nes jie nebus sukurti iš naujo iš automatinio išlaidų nustatymo lentelių. Tačiau išlaidų operacijos įrašas, pažymėtas kaip importuotas, vis tiek gali būti panaikintas.

### <a name="linked-fields"></a>Susieti laukai

Kiekviena išlaidų operacija gali būti susieta su kitu tos pačios išlaidų srities įrašu. Šis susiejimas nustatomas lauke **Susietų išlaidų** tipas. Tai leidžia apskaičiuoti išlaidų vertę kaip kitų išlaidų procentą.

Susietų **išlaidų tipo** lauką galima tikrinti tik tada, jei pirmiausia apdorojamas nuorodas įrašas arba jei jis jau yra lentelėje. Tie patys reikalavimai taikomi susietame atkarpų **lauke**, kuris naudojamas tik gabenimo konteinerio išlaidų srities išlaidoms.
