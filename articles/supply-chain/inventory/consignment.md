---
title: Konsignacijos nustatymas
description: Šiame straipsnyje paaiškinama, kaip naudoti atvežimo konsignacijos atsargų procesus.
author: yufeihuang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentDraftReplenishmentOrderJournal, ConsignmentProductReceiptLines, ConsignmentReplenishmentOrder, ConsignmentVendorPortalOnHand, InventJournalOwnershipChange, InventOnHandItemListPage, PurchTable, PurchTablePart, PurchVendorPortalConfirmedOrders, DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220834
ms.assetid: 3c9d6de4-45d4-459a-aef7-0d9ad2c22b3a
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0087abebccca107a094a40d3e2d5a5de330532af
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014915"
---
# <a name="set-up-consignment"></a>Konsignacijos nustatymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip naudoti atvežimo konsignacijos atsargų procesus.

Konsignacijos atsargos yra tiekėjo turimos atsargos, kurios laikomos jūsų vietoje. Kai esate pasiruošę vartoti ar naudoti atsargas, atsargos tampa jūsų nuosavybe. Šiame straipsnyje pateikta informacija apie tai, kaip faktiškai gauti tiekėjo turimų atsargų nesukuriant DK operacijų, kaip pradėti gamybos procesą, kuriame tiekėjo turimos atsargos gali būti faktiškai rezervuojamos. ir kaip pakeisti žaliavų savininką, kad būtų galima apdoroti suvartojimą kaip gamybos užsakymo apdorojimo dalį. Taip pat yra šiek tiek informacijos apie tai, kaip tiekėjai gali stebėti savo atsargų vartojimą naudodami tiekėjo bendradarbiavimo sąsają.

## <a name="overview-of-the-consignment-process"></a>Konsignacijos proceso apžvalga

Šio scenarijaus pavyzdyje įmonė USMF su tiekėju US-104 yra sudariusi konsignacijos sutartį dėl žaliavos M9211CI.

1. Kažkas įmonėje USMF pagal numatytą poreikį rankiniu būdu sukuria konsignacijos papildymo užsakymą. Sukuriamas tiekėjo US-104 užsakymas ir pridedama prekės MS9211CI eilutė.
1. Tiekėjas informuojamas apie numatomą pristatymą. Tai gali įvykti vienu iš trijų būdų:
    - Kas nors dirbantis USMF tiekėjui nusiunčia užsakymo informaciją.
    - Tiekėjas gali stebėti numatomas turimas atsargas naudodamas tiekėjo bendradarbiavimo sąsają.
    - Kas nors dirbantis USMF filtruoja puslapio **Turimos atsargos** duomenis, kad būtų rodomi tik tiekėjo US-104 įrašai, kurių gavimo būsena **Užsakyta**, o po to siunčia šią informaciją tiekėjui.
1. Atsargas pristato tiekėjas US-104 įmonei USMF.
1. Kai medžiagos atvyksta į USMF, konsignacijos papildymo užsakymas atnaujinamas pateikiant gavimo dokumentą. Įrašomas tik faktinis tiekėjo turimų atsargų kiekis. Didžiosios knygos operacijos nesukuriamos, nes atsargos vis dar priklauso tiekėjui.
1. Tiekėjas stebi faktinių turimų atsargų atnaujinimus naudodamas puslapį **Turimos konsignacijos atsargos**.
1. Dabar, kai jau turimos faktinės atsargos, gamybos procesas rezervuoja tiekėjo turimas atsargas ir pradeda pagamintų prekių, kurioms pagaminti bus naudojama žaliava M9211CI, gamybos užsakymą.
1. Rezervuotos žaliavos, kuri bus suvartota šiandienos gamybos procese, savininkas pakeičiamas iš US-104 į USMF. Tai atliekama naudojant atsargų nuosavybės pakeitimo žurnalą. Šis procesas sukuria pirkimo užsakymus, kuriuose nustatoma lauko **Kilmė** nuostata **Konsignacija**.
1. Tiekėjas stebi suvartojimą (nuosavybės pakeitimas) puslapyje **Iš konsignacijos atsargų gauti produktai** ir, remdamasis šių dviejų įmonių sutartimis, pateikia sąskaitą faktūrą.
1. Gamybos procese žaliava naudojama per gamybos išrinkimo dokumentą. Faktinis rezervavimas atnaujinamas automatiškai, kad būtų matoma, jog turimos atsargos priklauso USMF.
1. Sąskaita faktūra iš US-104 apdorojama pagal pirkimo užsakymus, kurie buvo automatiškai sugeneruoti apdorojant atsargų nuosavybės pakeitimą. Mokėjimas atliekamas tiekėjui US-104 už suvartotas atsargas.

USMF atlieka papildomus periodinius procesus:

- Faktinis tiekėjui priklausančių atsargų judėjimas tarp skirtingų sandėlių apdorojamas naudojant perkėlimo žurnalą.
- Faktinės turimos atsargos atnaujinamos naudojant žurnalą **Prekių skaičiavimas**. Tiekėjas taip pat gali naudoti skaičiavimą norėdamas atnaujinti turimas atsargas, jeigu turi leidimą tai daryti.

Tiekėjas US-104 gali stebėti naujinimus naudodamas puslapį **Turimos konsignacijos atsargos**.

## <a name="consignment-replenishment-orders"></a>Konsignacijos papildymo užsakymai

Konsignacijos papildymo užsakymas yra dokumentas, naudojamas norint pateikti užklausą ir stebėti produktų, kuriuos tiekėjas numato pristatyti per tam tikrą laiko intervalą, atsargų kiekius sukuriant užsakytų atsargų operacijas. Paprastai tai bus pagrįsta prognoze ir faktiniu konkrečių produktų poreikiu. Atsargos, kurios bus gautos pateikus konsignacijos papildymo užsakymą, lieka tiekėjo nuosavybė. Įrašomi tik su faktinio gavimo atnaujinimu susiję turimi produktai, todėl nėra jokių didžiosios knygos operacijos atnaujinimų.

Dimensija **Savininkas** naudojama norint atskirti informaciją apie tai, kurios atsargos priklauso tiekėjui, o kurios priklauso gaunančiam juridiniam subjektui. Konsignacijos papildymo užsakymo eilučių būsena yra **Atviras užsakymas** tol, kol negaunamas arba neatšaukiamas visas eilučių kiekis. Kai visas kiekis gaunamas arba atšaukiamas, būsena pakeičiama į **Baigta**. Faktines su konsignacijos papildymo užsakymu susijusias turimas atsargas galima įrašyti naudojant registravimo procesą ir gavimo dokumento atnaujinimo procesą. Registraciją galima atlikti kaip prekių gavimo proceso dalį arba rankiniu būdu atnaujinant užsakymo eilutes. Kai naudojamas gavimo dokumento atnaujinimo procesas, produkto gavimo žurnale pateikiamas įrašas, kurį galima naudoti norint patvirtinti prekių gavimą tiekėjams.

[![Konsignacijos papildymo užsakymai.](./media/consignment-replenishment-order.png)](./media/consignment-replenishment-order.png)

## <a name="inventory-ownership-change-journal"></a>Atsargų nuosavybės pakeitimo žurnalas

Žurnalas **Atsargų nuosavybės pakeitimas** naudojamas norint įrašyti konsignacijos atsargų savininko pakeitimą iš tiekėjo į jį naudojantį juridinį subjektą. Žurnale numatomų atsargų operacijos nekuriamos. Kaip ir bet kuriame atsargų žurnale, jame turi būti nurodytas atsargų žurnalo pavadinimas. Šie pavadinimai sukuriami puslapyje **Atsargų žurnalo pavadinimai** ir turi būti nustatyta dalies **Žurnalo tipas** parinktis **Nuosavybės pakeitimas**.

Kuriamos tik tos atsargų operacijos, kurios susijusios su užregistruotu žurnalu. Kada žurnalas buvo užregistruotas:

- Tiekėjui priklausančios atsargos išduodamos naudojant nuorodą **Nuosavybės keitimas**, kurios būsena **Parduota**.
- Turimas atsargas jas naudojantis juridinis subjektas gauna pirkimo užsakyme naudodamas gavimo dokumento atnaujintą atsargų operaciją. Taip nustatoma užsakymo būsena **Gauta**. Nustatoma konsignacijoms naudojamų pirkimo užsakymų lauko **Kilmė** nuostata **Konsignacija**.

Sukūrus užsakymą konsignacijos pirkimo užsakymo eilučių skaičiaus atnaujinti neįmanoma.

[![Atsargų nuosavybės keitimo žurnalas.](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Tiekėjų bendradarbiavimas konsignacijos procesuose

Jei jūsų tiekėjai naudoja tiekėjų bendradarbiavimo sąsają, jie gali ją panaudoti norėdami stebėti atsargų suvartojimą jūsų vietoje. Tiekėjo bendradarbiavimo sąsajoje yra trys su gaunamu konsignacijos procesu susiję puslapiai:

- **Pirkimo užsakymai**, **naudojantys konsignacijos atsargas** – rodoma išsami pirkimo užsakymo informacija, susijusi su nuosavybės pakeitimu iš konsignacijos proceso.
- **Produktai, gauti iš konsignacijos atsargų** – rodoma informacija apie prekes ir kiekius, kurių gavimo dokumentai atnaujinti nuosavybės pakeitimo proceso metu.
- **Turimos konsignacijos atsargos** – rodoma informacija apie konsignacijos prekes, kurias numatoma pristatyti, ir prekes, kurias jau faktiškai galima įsigyti kliento vietoje.

Norėdami gauti daugiau informacijos apie tiekėjų nustatymą naudoti tiekėjų bendradarbiavimą, žr. Tvarkyti [tiekėjų bendradarbiavimo vartotojus](../procurement/manage-vendor-collaboration-users.md).

## <a name="inventory-owners"></a>Atsargų savininkai

Norėdami įrašyti faktines gaunamos konsignacijos atsargas, turite nurodyti tiekėją, kuriam jos priklauso. Tai atliekama puslapyje **Atsargų savininkas**. Pasirinkus **Tiekėjo sąskaita** sugeneruojamos numatytosios laukų **Vardas** ir **Savininkas** vertės. Lauko **Savininkas** vertė matoma tiekėjui, todėl jeigu jūsų tiekėjo paskyros vardus kitiems gali būti sunku atpažinti, gali tekti juos pakeisti. Lauką **Savininkas** galima redaguoti, bet tik iki veiksmo, kai išsaugomas įrašas **Atsargų savininkas**. Lauke **Vardas** įrašomas su tiekėjo paskyra susietos šalies vardas ir jo negalima keisti.

[![Atsargų savininkai.](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>Sekimo dimensijų grupė

Konsignacijos procesuose ketinamus naudoti elementus būtina susieti su **Sekimo dimensijų grupe**, kurios dimensijos **Savininkas** nuostata **Aktyvi**. Visada pažymėtos dimensijos Savininkas parinktys **Faktinės atsargos** ir **Finansinės atsargos**. Parinktis **Padengimo planas pagal dimensiją** niekada nepažymimas.

[![Sekimo dimensijų grupė.](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
