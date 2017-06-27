---
title: Konsignacija
description: "Šioje temoje paaiškinama, kaip naudoti gaunamų konsignacijos atsargų procesus."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentDraftReplenishmentOrderJournal, ConsignmentProductReceiptLines, ConsignmentReplenishmentOrder, ConsignmentVendorPortalOnHand, InventJournalOwnershipChange, InventOnHandItemListPage, PurchTable, PurchVendorPortalConfirmedOrders
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220834
ms.assetid: 3c9d6de4-45d4-459a-aef7-0d9ad2c22b3a
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a6e3f0e58e14cc4d68d2249a4e3b69515f23e838
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="consignment"></a>Konsignacija

[!include[banner](../includes/banner.md)]


Šioje temoje paaiškinama, kaip naudoti gaunamų konsignacijos atsargų procesus.

Konsignacijos atsargos yra tiekėjo turimos atsargos, kurios laikomos jūsų vietoje. Kai esate pasiruošę vartoti ar naudoti atsargas, atsargos tampa jūsų nuosavybe. Šioje temoje pateikiama informacija apie tai, kaip faktiškai gauti šiuo metu tiekėjo turimų atsargų nesukuriant didžiosios knygos operacijų, kaip pradėti gamybos procesą, kai tiekėjo turimas atsargas galima rezervuoti faktiškai, ir kaip pakeisti žaliavų savininką, kad būtų galima apdoroti suvartojimą kaip gamybos užsakymo apdorojimo dalį. Taip pat yra šiek tiek informacijos apie tai, kaip tiekėjai gali stebėti savo atsargų vartojimą naudodami tiekėjo bendradarbiavimo sąsają. Norėdami gauti informacijos apie tai, kaip įgalinti ir konfigūruoti gaunamus konsignacijos procesus, žr. [Konsignacijos nustatymas](set-up-consignment.md).

## <a name="overview-of-the-consignment-process"></a>Konsignacijos proceso apžvalga
Šio scenarijaus pavyzdyje įmonė USMF su tiekėju US-104 yra sudariusi konsignacijos sutartį dėl žaliavos M9211CI.

1.  Kažkas įmonėje USMF pagal numatytą poreikį rankiniu būdu sukuria konsignacijos papildymo užsakymą. Sukuriamas tiekėjo US-104 užsakymas ir pridedama prekės MS9211CI eilutė.
2.  Tiekėjas informuojamas apie numatomą pristatymą. Tai gali įvykti vienu iš trijų būdų:
    -   Kas nors dirbantis USMF tiekėjui nusiunčia užsakymo informaciją.
    -   Tiekėjas gali stebėti numatomas turimas atsargas naudodamas tiekėjo bendradarbiavimo sąsają.
    -   Kas nors dirbantis USMF filtruoja puslapio **Turimos atsargos** duomenis, kad būtų rodomi tik tiekėjo US-104 įrašai, kurių gavimo būsena **Užsakyta**, o po to siunčia šią informaciją tiekėjui.

3.  Atsargas pristato tiekėjas US-104 įmonei USMF.
4.  Kai medžiagos atvyksta į USMF, konsignacijos papildymo užsakymas atnaujinamas pateikiant gavimo dokumentą. Įrašomas tik faktinis tiekėjo turimų atsargų kiekis. Didžiosios knygos operacijos nesukuriamos, nes atsargos vis dar priklauso tiekėjui.
5.  Tiekėjas stebi faktinių turimų atsargų atnaujinimus naudodamas puslapį **Turimos konsignacijos atsargos**.
6.  Dabar, kai jau turimos faktinės atsargos, gamybos procesas rezervuoja tiekėjo turimas atsargas ir pradeda pagamintų prekių, kurioms pagaminti bus naudojama žaliava M9211CI, gamybos užsakymą.
7.  Rezervuotos žaliavos, kuri bus suvartota šiandienos gamybos procese, savininkas pakeičiamas iš US-104 į USMF. Tai atliekama naudojant atsargų nuosavybės pakeitimo žurnalą. Šis procesas sukuria pirkimo užsakymus, kuriuose nustatoma lauko **Kilmė** nuostata **Konsignacija**.
8.  Tiekėjas stebi suvartojimą (nuosavybės pakeitimas) puslapyje **Iš konsignacijos atsargų gauti produktai** ir, remdamasis šių dviejų įmonių sutartimis, pateikia sąskaitą faktūrą.
9.  Gamybos procese žaliava naudojama per gamybos išrinkimo dokumentą. Faktinis rezervavimas atnaujinamas automatiškai, kad būtų matoma, jog turimos atsargos priklauso USMF.
10. Sąskaita faktūra iš US-104 apdorojama pagal pirkimo užsakymus, kurie buvo automatiškai sugeneruoti apdorojant atsargų nuosavybės pakeitimą. Mokėjimas atliekamas tiekėjui US-104 už suvartotas atsargas.

USMF atlieka papildomus periodinius procesus:

-   Faktinis tiekėjui priklausančių atsargų judėjimas tarp skirtingų sandėlių apdorojamas naudojant perkėlimo žurnalą.
-   Faktinės turimos atsargos atnaujinamos naudojant žurnalą**Prekių skaičiavimas**. Tiekėjas taip pat gali naudoti skaičiavimą norėdamas atnaujinti turimas atsargas, jeigu turi leidimą tai daryti.

Tiekėjas US-104 gali stebėti naujinimus naudodamas puslapį **Turimos konsignacijos atsargos**.

## <a name="consignment-replenishment-orders"></a>Konsignacijos papildymo užsakymai
Konsignacijos papildymo užsakymas yra dokumentas, naudojamas norint pateikti užklausą ir stebėti produktų, kuriuos tiekėjas numato pristatyti per tam tikrą laiko intervalą, atsargų kiekius sukuriant užsakytų atsargų operacijas. Paprastai tai bus pagrįsta prognoze ir faktiniu konkrečių produktų poreikiu. Atsargos, kurios bus gautos pateikus konsignacijos papildymo užsakymą, lieka tiekėjo nuosavybė. Įrašomi tik su faktinio gavimo atnaujinimu susiję turimi produktai, todėl nėra jokių didžiosios knygos operacijos atnaujinimų. Dimensija **Savininkas** naudojama norint atskirti informaciją apie tai, kurios atsargos priklauso tiekėjui, o kurios priklauso gaunančiam juridiniam subjektui. Konsignacijos papildymo užsakymo eilučių būsena yra **Atviras užsakymas** tol, kol negaunamas arba neatšaukiamas visas eilučių kiekis. Kai visas kiekis gaunamas arba atšaukiamas, būsena pakeičiama į **Baigta**. Faktines su konsignacijos papildymo užsakymu susijusias turimas atsargas galima įrašyti naudojant registravimo procesą ir gavimo dokumento atnaujinimo procesą. Registraciją galima atlikti kaip prekių gavimo proceso dalį arba rankiniu būdu atnaujinant užsakymo eilutes. Kai naudojamas gavimo dokumento atnaujinimo procesas, produkto gavimo žurnale pateikiamas įrašas, kurį galima naudoti norint patvirtinti prekių gavimą tiekėjams. 

[![Konsignacijos papildymo užsakymas](./media/consignment-replenishment-order.png)](./media/consignment-replenishment-order.png)

## <a name="inventory-ownership-change-journal"></a>Atsargų nuosavybės pakeitimo žurnalas
Atsargų savininko keitimo iš tiekėjo į gaunantį juridinį subjektą procesas atliekamas naudojant atsargų nuosavybės pakeitimo žurnalą. Žurnale numatomų atsargų operacijos nekuriamos. Kuriamos tik tos atsargų operacijos, kurios susijusios su užregistruotu žurnalu. Kada žurnalas buvo užregistruotas:

-   Tiekėjui priklausančios atsargos išduodamos naudojant nuorodą **Nuosavybės keitimas**, kurios būsena **Parduota**.
-   Turimas atsargas jas naudojantis juridinis subjektas gauna pirkimo užsakyme naudodamas gavimo dokumento atnaujintą atsargų operaciją. Taip nustatoma užsakymo būsena **Gauta**. Nustatoma konsignacijoms naudojamų pirkimo užsakymų lauko **Kilmė** nuostata **Konsignacija**.

Sukūrus užsakymą konsignacijos pirkimo užsakymo eilučių skaičiaus atnaujinti neįmanoma. 

[![Atsargų nuosavybės pakeitimo žurnalas](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Tiekėjų bendradarbiavimas konsignacijos procesuose
Tiekėjo bendradarbiavimo sąsajoje yra trys su gaunamu konsignacijos procesu susiję puslapiai:

-   **Pirkimo užsakymai**, **naudojantys konsignacijos atsargas** – rodoma išsami pirkimo užsakymo informacija, susijusi su nuosavybės pakeitimu iš konsignacijos proceso.
-   **Produktai, gauti iš konsignacijos atsargų** – rodoma informacija apie prekes ir kiekius, kurių gavimo dokumentai atnaujinti nuosavybės pakeitimo proceso metu.
-   **Turimos konsignacijos atsargos** – rodoma informacija apie konsignacijos prekes, kurias numatoma pristatyti, ir prekes, kurias jau faktiškai galima įsigyti kliento vietoje.





