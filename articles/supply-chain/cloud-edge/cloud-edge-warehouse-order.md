---
title: Sandėlio užsakymai, skirti debesies ir briaunos skalės vienetams
description: Šioje temoje pateikiama informacija apie sandėlio užsakymo galimybę, naudojamą kaip sandėlio skalės vieneto darbo krūvio dalis.
author: perlynne
manager: tfeyr
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c04127b9fe621d962be2d7fe06358b3bd1b78916
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/02/2021
ms.locfileid: "5105720"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a>Sandėlio užsakymai, skirti debesies ir briaunos skalės vienetams

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Ne visos verslo funkcijos yra visiškai palaikomos viešojoje peržiūros versijoje, kai naudojami skalės vieneto darbo krūviai. Jei naudojate skalės vienetus, įsitikinkite, kad naudojate tik tuos procesus, kuriuos išsamiai aprašo šis skyrius kaip palaikomus.

## <a name="what-are-warehouse-orders"></a>Kas yra sandėlio užsakymai?

*Sandėlio užsakymai* yra užsakymo, sukurto palaikyti telkinio ir skalės vienetų sandėlio diegimus, tipas. Jie leidžia jums gauti atsargas, kai vykdote sandėlio darbo krūvį skalės vienete. Šiuo metu jie naudojami tik su pirkimo užsakymais.

Sandėlio užsakymai naudojami kaip sandėlio valdymo apdorojimo dalis, pavyzdžiui, kai sandėlio programa naudojama faktinėms turimoms atsargoms registruoti gaunamo pirkimo užsakymo apdorojimo metu. Sandėlio užsakymai kuriami kaip dalis *Išleidimo į sandėlį* proceso, prieinamo pirkimo užsakymams, kurie nurodo skalės vieneto sandėlį ir prekes, įgalintas naudoti sandėlio valdymo procesus.

> [!IMPORTANT]
> Sandėlio užsakymai galimi tik diegimams, naudojantiems [sandėlio valdymo darbo krūvius debesiui ir briaunai skalės vienetams](cloud-edge-workload-warehousing.md).

## <a name="create-a-warehouse-order"></a>Sandėlio užsakymo kūrimas

Norėdami sukurti sandėlio užsakymą, atlikite toliau nurodytus veiksmus.

1. Prisijunkite prie „Microsoft Dynamics 365 Supply Chain Management“ egzemplioriaus, vykdomo telkinyje. (Turite inicijuoti *Išleidimo į sandėlį* procesą, kai esate prisijungę telkinyje.)
1. Eikite į **Pirkimas ir tiekėjų parinkimas \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.
1. Veiksmų srities skirtuke **Sandėlis** grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**.
1. Norėdami peržiūrėti susijusias sandėlio užsakymo eilutes, atidarykite reikiamą pirkimo užsakymą, pasirinkite eilutę, esančią skyriuje **Pirkimo užsakymo eilutės** ir tada įrankių juostoje pasirinkite **Sandėlis \> Sandėlio užsakymo eilutės**. Norėdami peržiūrėti visas eilutes, eikite į **Sandėlio valdymas \> Užklausos ir ataskaitos \> Sandėlio užsakymo eilutės**.

## <a name="cancel-a-warehouse-order"></a>Sandėlio užsakymo atšaukimas

Kaip *Išleidimo į sandėlį* proceso dalis, pirkimo užsakymo atsargų operacijos yra susietos su sandėlio užsakymais ir jų negalima atnaujinti telkinyje. Jeigu suklydote išleisdami prekes į sandėlį ar turite kitą priežastį atšaukti sandėlio užsakymo eilučių sukūrimą, galite pateikti sandėlio užsakymo eilučių atšaukimo užklausą.

Norėdami atšaukti sandėlio užsakymo eilutes, atlikite toliau nurodytus veiksmus.

1. Prisijunkite prie „Supply Chain Management“ egzemplioriaus, vykdomo telkinyje.
1. Eikite į **Sandėlio valdymas \> Užklausos ir ataskaitos \> Sandėlio užsakymo eilutės**.
1. Pasirinkite reikalingą eilutę.
1. Veiksmų srityje pasirinkite **Atšaukti sandėlio užsakymo eilutes**.

> [!NOTE]
> Eilučių atšaukimo prašymas bus atmestas bet kurioms eilutėms, kurios jau laukia atšaukimo arba kurios aktyviai apdorojamos sandėlyje, kuriame vykdomas jos darbo krūvis skalės vienetais.

## <a name="monitor-a-warehouse-order"></a>Sandėlio užsakymo stebėjimas

Rodinyje **Sandėlio užsakymo eilutės** galite stebėti gavimo eigą peržiūrėdami **Likęs gautinas kiekis** stulpelį. Norėdami peržiūrėti išsamią informaciją, susijusią su darbu, atliktu naudojant sandėlio programą, atlikite vieną iš šių veiksmų.

- Eikite į **Sandėlio valdymas \> Užklausos ir ataskaitos \> Sandėlio užsakymo eilutės** ir naudokite filtrą rasti ieškomoms eilutėms.
- Eikite į **Įsigijimas ir šaltiniai \> Pirkimo užsakymai \> Visi pirkimo užsakymai** ir atidarykite reikiamą pirkimo užsakymą. Skyriuje **Pirkimo užsakymo eilutės** pasirinkite vieną ar daugiau eilučių ir tada įrankių juostoje pasirinkite **Sandėlis \> Sandėlio gavimo įrašai**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]