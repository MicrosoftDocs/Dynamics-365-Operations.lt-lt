---
title: "Tiekėjo bendradarbiavimas su klientais"
description: "Šioje temoje aprašoma, kaip galite naudoti tiekėjo bendradarbiavimą programoje „Microsoft Dynamics 365 for Operations“, norėdami dirbti su PU ir stebėti konsignacijos atsargas."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 11cd2242b5a575ae87b0dbcf6f8ce268fcea5377
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-with-customers"></a>Tiekėjo bendradarbiavimas su klientais

Šioje temoje aprašoma, kaip galite naudoti tiekėjo bendradarbiavimą programoje „Microsoft Dynamics 365 for Operations“, norėdami dirbti su PU ir stebėti konsignacijos atsargas.

Šioje temoje aprašoma, kaip galite naudoti tiekėjo bendradarbiavimą, norėdami dirbti su klientais programoje „Microsoft Dynamics 365 for Operations“. Ji apima informacijos apie tai, kaip stebėti ir reaguoti į pirkimo užsakymus, ir kaip stebėti siuntos atsargų. Taip pat galima naudoti tiekėjo bendradarbiavimas dirbant su SF. Daugiau informacijos rasite [tiekėjo bendradarbiavimas, sąskaitų faktūrų išrašymo darbo srities](/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace).

## <a name="working-with-purchase-orders"></a>Darbas su pirkimo užsakymais
Naudojant darbo sritį **Pirkimo užsakymo patvirtinimas** galima reaguoti į peržiūrai atsiųstus PU. Joje taip pat galima peržiūrėti informaciją apie PU, laukiančius kliento veiksmų, ir PU, kurie buvo patvirtinti, bet vis dar yra atviri. Darbo srityje **Pirkimo užsakymo patvirtinimas** pateikiami trys sąrašai.

-   **Pirkimo užsakymų apžvalga** -šis sąrašas rodys gamintojų organizacijoms, kurios bus išsiųstos jums ir laukia jūsų atsakymo. Po to, kai jums atsakyti, PO dingsta iš sąrašo. Jei klientas atsiunčia jums naują PU versiją, o jūs dar neatsakėte į ankstesniąją, rodoma tik naujausia versija.
-   **Laukiama kliento veiksmo** – šiame sąraše galite peržiūrėti PU, į kuriuos atsakėte, bet kurių klientas dar nepatvirtino. Jei priėmėte PU, galite jį stebėti šiame sąraše tol, kol būsena pasikeičia į **Patvirtintas**. Jei PU atmetėte arba priėmėte atlikę keitimų, galite stebėti PU čia tol, kol klientas atsiųs naują versiją.
-   **Atviri patvirtinti pirkimo užsakymai** – šiame sąraše yra visi jūsų sąskaitos PU, kurių būsena yra **Patvirtintas**. Kai pagal PU gauti visi produktai arba paslaugos, PU dingsta iš sąrašo.

Šiame sąraše pateikiami keturi puslapiai, kuriuos galite naudoti, norėdami dirbti su pirkimo užsakymais. Dviejuose jų pateikiama tokia pati informacija kaip darbo srityje.

-   **Pirkimo užsakymai, kuriuos galima peržiūrėti** (žr. anksčiau)
-   **Pirkimo užsakymo tiekėjo patvirtinimo retrospektyva** – šiame puslapyje yra visi PU ir visos PU versijos, išsiųstos tiekėjui, bei visi tiekėjo atsakymai.
-   **Atviri patvirtinti pirkimo užsakymai** (žr. anksčiau)
-   **Visi patvirtinti pirkimo užsakymai** – šiame puslapyje pateikiami visi patvirtinti PU, įskaitant tuos, kurių prekės arba paslaugos yra gautos. Šį sąrašą galite naudoti norėdami stebėti, kurių PU SF galite siųsti.

### <a name="responding-to-purchase-orders"></a>Atsakymas į pirkimo užsakymus

Pirkimo užsakymus, kurių klientas išsiuntė jums peržiūrėti matomos, **pirkimo užsakymo patvirtinimo** darbo srities ir su **pirkimo užsakymus peržiūra** puslapis. Kai atidarote Go, galite jį priimti, atmesti arba priimti pakeitimus. Gali būti priedų PU antraštėje arba atskirose eilutėse. Taip pat galite pridėti informaciją prie atsakymo PU antraštėje arba atskirose eilutėse. Pavyzdžiui, galite pasiūlyti vienos eilutės prekės pakaitalą. Galite peržiūrėti ir spausdinti PU kaip PDF failą, naudodami parinktį **Peržiūrėti / spausdinti**. Naudodami veiksmą **Rodyti dimensijas**, galite slėpti arba rodyti šiuos dimensijų stulpelius: Teritorija, Sandėlis, Spalva, Dydis, Stilius, Konfigūracija. Jei naudojate su **sutikti su pakeitimai** parinktis, galite priimti arba atmesti atskiros eilutės. Taip pat galite šiuos keitimus iki linijos:

-   Keisti datas arba kiekius. Jei norite naujinti patvirtintą pristatymo datą visose eilutėse, naudokite PU antraštės parinktį **Naujinti pristatymo datą**.
-   Eilučių skaldymas naudojant skirtingas pristatymo datas arba kiekius
-   Pakeisti prekę. Norėdami tai padaryti, įveskite prekės aprašymą ir prekės numerį lauke **Išorinis**, kuris yra skyriuje **Eilutės informacija**.

Negalima keisti kainodaros informacijos arba išlaidų, bet galima siūlyti tokius keitimus naudojant pastabas. Jei klientas jums atsiunčia naują PU versiją, versija bus pateikta su priedėliu, kuris nurodys, kad PU yra modifikuota anksčiau paskelbto PU versija. Puslapyje **Pirkimo užsakymo tiekėjo patvirtinimo retrospektyva** galite sekti kiekvieno užsakymo retrospektyvą.

## <a name="monitoring-consignment-inventory"></a>Konsignacijos atsargų sekimas
Jei naudojate konsignacijos atsargas, galite naudoti tiekėjo bendradarbiavimo sąsają, norėdami peržiūrėti informaciją tolesniuose puslapiuose.

-   **Pirkimo užsakymų vartoja siuntos atsargų** -pirkimo užsakymų siuntos atsargų generuojamos, kai klientas prisiima nuosavybės teises į atsargas. Šie konsignacijos pirkimo užsakymai rodomi tik puslapyje **Pirkimo užsakymų naudojamos konsignacijos atsargos**. Jie neįtraukiami į puslapį **Visi patvirtinti pirkimo užsakymai**.
-   **Produktai, gauti iš konsignacijos atsargų** – šiame puslapyje pateikiamos visos operacijos, kuriose produktų nuosavybės teisės buvo perduoto įmonei, kuri naudoja atsargas. Galite naudoti šią informaciją kliento SF išrašyti.
-   **Turimos konsignacijos atsargos** – šiame puslapyje rodomos turimos, jūsų įmonei priklausančios konsignacijos atsargos, esančios klientų sandėlyje.


<a name="see-also"></a>Taip pat žiūrėkite
--------

[Tiekėjo bendradarbiavimo vartotojų valdymas](manage-vendor-collaboration-users.md)


