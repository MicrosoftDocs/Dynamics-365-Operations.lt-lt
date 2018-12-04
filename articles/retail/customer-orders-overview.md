---
title: "Kliento užsakymų kūrimas „Retail Modern POS“ (MPOS)"
description: "Šioje temoje pateikiama informacija apie kliento užsakymus „Retail Modern POS“ (MPOS). Kliento užsakymai dar vadinami specialiais užsakymais. Šioje temoje pateikta susijusių parametrų ir operacijų srautų apžvalga."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 8025df4f8498efa867f71892b253f71631b731c7
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---

# <a name="customer-orders-in-retail-modern-pos-mpos"></a>Kliento užsakymų kūrimas „Retail Modern POS“ (MPOS)

[!include [banner](includes/banner.md)]

Šioje temoje pateikiama informacija apie kliento užsakymus „Retail Modern POS“ (MPOS). Kliento užsakymai dar vadinami specialiais užsakymais. Šioje temoje pateikta susijusių parametrų ir operacijų srautų apžvalga.

Integruotų kanalų mažmeninėje prekyboje dauguma pardavėjų suteikia galimybę kurti klientų užsakymus (arba specialius užsakymus) įvairiems produktų ir vykdymo reikalavimams įvykdyti. Toliau nurodomi įprasti scenarijai.

-   Klientas nori, kad produktai būtų pristatyti konkrečią dieną konkrečiu adresu.
-   Klientas nori atsiimti produktus parduotuvėje arba vietoje, kuri nėra parduotuvė arba vieta, kurioje klientas tuos produktus nusipirko.
-   Klientas nori, kad kas nors kitas paimtų jo nupirktus produktus.

Pardavėjai taip pat naudoja kliento užsakymus, norėdami sumažinti prarasto pardavimo kiekius, kuriuos gali lemti atsargų stygius, kadangi prekes galima pristatyti arba atsiimti kitu laiku arba kitoje vietoje.

## <a name="set-up-customer-orders"></a>Kliento užsakymų nustatymas
Toliau pateikiama keletas parametrų, kuriuos galima nustatyti puslapyje **Mažmeninės prekybos parametrai** ir kurie nurodo, kaip kliento užsakymai yra vykdomi.

-   **Numatytasis depozito procentas** – nurodykite sumą, kurią klientas turi sumokėti kaip depozitą prieš patvirtinant užsakymą. Numatytoji depozito suma apskaičiuojama kaip užsakymo vertės procentas. Atsižvelgiant į teises, parduotuvės atstovas gali perrašyti sumą naudodamas parinktį **Depozito perrašymas**.
-   **Atšaukimo mokesčio procentais** – jei atšaukiant kliento užsakymą taikomas mokestis, nurodykite to mokesčio sumą.
-   **Atšaukimo mokesčio kodas** – jei atšaukiant kliento užsakymą taikomas mokestis, tas mokestis bus nurodytas pardavimo užsakymo išlaidų kode. Naudokite šį parametrą, kad nurodytumėte atšaukimo mokesčio kodą.
-   **Siuntimo mokesčio kodas** – pardavėjai gali taikyti papildomą mokestį už prekių siuntimą klientui. To siuntimo mokesčio suma bus nurodyta pardavimo užsakymo išlaidų kode. Naudokite šį parametrą, kad siuntimo mokesčio kodą susietumėte su siuntimo išlaidomis kliento užsakyme.
-   **Grąžinti siuntimo išlaidas** – nurodykite, ar siuntimo išlaidos, susietos su kliento užsakymų, yra grąžinamos.
-   **Maksimali suma, kuriai nereikia gauti patvirtinimo** – jei siuntimo išlaidos yra grąžinamos, nurodykite didžiausią visų grąžinimo užsakymų siuntimo išlaidų grąžinimo sumą. Jei ši suma viršijama, vadovas turi ją perrašyti, kad būtų galima tęsti grąžinimo operaciją. Toliau nurodytais scenarijais siuntimo išlaidų grąžinimo suma gali viršyti anksčiau sumokėtą sumą.
    -   Išlaidos taikomos pardavimo užsakymo antraštės lygyje ir, kai tam tikras produkto eilutės kiekis yra grąžinamas, didžiausios leidžiamos produktų ir kiekio siuntimo išlaidų grąžinimo sumos negalima nustatyti tokiu būdu, kuris tiktų visiems mažmeninės prekybos klientams.
    -   Siuntimo išlaidos patiriamos kiekvieną kartą siunčiant prekes. Jei klientas kelis kartus grąžina produktus, o pardavėjo strategijoje nurodyta, kad pardavėjas padengs grąžinimo siuntimo išlaidų sumą, grąžinimo siuntimo išlaidų suma bus didesnė nei faktinės siuntimo išlaidos.

## <a name="transaction-flow-for-customer-orders"></a>Kliento užsakymų operacijų srautas
### <a name="create-a-customer-order-in-retail-modern-pos"></a>Kliento užsakymo kūrimas „Retail Modern POS“

1.  Įtraukite į operaciją klientą.
2.  Įtraukite produktų į krepšelį.
3.  Spustelėkite **Kurti kliento užsakymą** ir tada pasirinkite užsakymo tipą. Užsakymo tipas gali būti **Kliento užsakymas** arba **Pasiūlymas**.
4.  Spustelėkite **Siųsti pasirinktus** arba **Siųsti viską**, norėdami siųsti produktus kliento sąskaitoje nurodytu adresu, nurodykite pageidaujamą siuntimą datą ir siuntimo išlaidas.
5.  Spustelėkite **Paimti pasirinktus** arba **Paimti viską**, norėdami pasirinkti produktus, kurie nurodytą dieną bus paimti iš dabartinės parduotuvės arba kitos parduotuvės.
6.  Surinkite depozito sumą, jei depozitas reikalingas.

### <a name="edit-an-existing-customer-order"></a>Esamo kliento užsakymo redagavimas

1.  Pagrindiniame puslapyje spustelėkite **Rasti užsakymą**.
2.  Raskite ir pasirinkite užsakymą, kurį norite redaguoti. Puslapio apačioje spustelėkite **Redaguoti**.

### <a name="pick-up-an-order"></a>Užsakymo paėmimas

1.  Pagrindiniame puslapyje spustelėkite **Rasti užsakymą**.
2.  Pasirinkite paimtiną užsakymą. Puslapio apačioje spustelėkite **Paėmimas ir pakavimas**.
3.  Spustelėkite **Paimti**.

### <a name="cancel-an-order"></a>Užsakymo atšaukimas

1.  Pagrindiniame puslapyje spustelėkite **Rasti užsakymą**.
2.  Pasirinkite atšauktiną užsakymą. Puslapio apačioje spustelėkite **Atšaukti**.

#### <a name="create-a-return-order"></a>Grąžinimo užsakymo kūrimas

1.  Pagrindiniame puslapyje spustelėkite **Rasti užsakymą**.
2.  Pasirinkite grąžintiną užsakymą, pasirinkite užsakymo SF ir tada pasirinkite grąžintinų prekių produkto eilutę.
3.  Puslapio apačioje spustelėkite **Grąžinimo užsakymas**.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Kliento užsakymų asinchroninių operacijų srautas
Klientų užsakymus galima kurti iš elektroninio kasos aparato (EKA) kliento sinchroniniu arba asinchroniniu režimu.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Kliento užsakymų kūrimo asinchroniniu režimu funkcijos įjungimas

1.  Spustelėkite **Mažmeninė prekyba** &gt; **Kanalų sąranka** &gt; **EKA sąranka** &gt; **EKA profilis** &gt; **Funkcijų profiliai**.
2.  „FastTab“ **Bendra** nustatykite parinktį **Kurti kliento užsakymą asinchroniniu režimu** į **Taip**.

Kai parinktis **Kurti kliento užsakymą asinchroniniu režimu** nustatyta į **Taip**, kliento užsakymai visada kuriami asinchroniniu režimu, net jei galima naudoti „Retail Transaction Service“ (RTS). Jei šią parinktį nustatysite į **Ne**, kliento užsakymai bus visada kuriami sinchroniniu režimu naudojant RTS. Kai kliento užsakymai kuriami asinchroniniu režimu, jie perkeliami ir įterpiami į „Retail“ naudojant perkėlimo (P) užduotis. Atitinkami pardavimo užsakymai sukuriami „Retail“, kai parinktis **Sinchronizuoti užsakymus** paleidžiama neautomatiškai arba paketinio vykdymo metu.

<a name="additional-resources"></a>Papildomi ištekliai
--------

[Hibridiniai kliento užsakymai](hybrid-customer-orders.md)




