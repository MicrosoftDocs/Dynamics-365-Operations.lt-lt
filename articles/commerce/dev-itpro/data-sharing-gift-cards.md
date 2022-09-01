---
title: Dovanų kortelių duomenų bendras naudojimas įmonėje
description: Šiame straipsnyje aprašoma, kaip sukonfigūruoti Microsoft Dynamics 365 Commerce naudoti "Dynamics 365" finansų duomenų bendro naudojimo funkcijas tarp duomenų sričių, kad būtų sinchronizuoti dovanų kortelės duomenys.
author: BrianShook
ms.date: 08/26/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: b56890b546c3cd74b75cf447e62495733ea8d288
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/31/2022
ms.locfileid: "9387375"
---
# <a name="cross-company-data-sharing-for-gift-cards"></a>Dovanų kortelių duomenų bendras naudojimas įmonėje

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šiame straipsnyje aprašoma, kaip sukonfigūruoti Microsoft Dynamics 365 Commerce, kad dovanų kortelės duomenims sinchronizuoti būtų naudojama "Dynamics 365" finansų duomenų bendro naudojimo funkcija. Tada duomenų įrašo bendro naudojimo funkciją galima naudoti norint bendrai naudoti duomenis visose įmonėse dviejose duomenų srityse. Tokiu būdu "Commerce" vidinę dovanų lentelę galima bendrai naudoti duomenis tarp dviejų įmonės objektų. Norėdami gauti daugiau informacijos apie "Dynamics 365 Finance" kelių įmonių duomenų bendrinimą, žr. įvairių [įmonių duomenų bendrinimą](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing).

## <a name="key-terms"></a>Pagrindiniai terminai

| Semestras | Aprašymas |
|---|---|
| Įmonė | Juridinis subjektas "Dynamics 365" finansų aplinkoje. |
| Dovanų kortelė | Vidinis Dynamics 365 Commerce dovanų kortelės produktas. |

## <a name="prerequisites"></a>Būtinieji komponentai

Vartotojai turi sukonfigūruoti savo aplinką visų įmonių duomenų bendrai naudoti, kaip aprašyta visų [įmonių duomenų bendrai naudojant](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing).

**Laukas RetailGiftCardTable turi** būti nustatytas kaip **Dubliuotas** **·**, kad būtų galimas dovanų kortelių lentelės įrašų bendrinimo dublikatas (DRS). Daugiau informacijos ieškokite programuotojų [bendrai naudoti kelių įmonių duomenis](/dynamics365/fin-ops-core/dev-itpro/sysadmin/drs-srs-dev).

## <a name="configure-cross-company-data-sharing-for-gift-cards"></a>Konfigūruoti dovanų kortelių kelių įmonių duomenų bendrą naudojimą

Norėdami konfigūruoti dovanų kortelių visų įmonių duomenų bendrą naudojimą, atlikite šiuos veiksmus.

1. "Commerce Headquarters" eikite į Sistemos **administravimo sąranką \>\> Sukonfigūruokite visų įmonių duomenų bendrą naudojimą**.
1. Norėdami įtraukti duomenų bendro naudojimo **įrašą**, veiksmų srityje pasirinkite Naujas.
1. Lauke Pavadinimas **įveskite** duomenų bendro naudojimo įrašo pavadinimą (pvz., Dovanų **kortelės**).
1. Dalies Lentelėse **ir laukuose, kuriuos norite** naudoti bendrai, pasirinkite **Įtraukti**.
1. **Naujos lentelės bendro naudojimo dialogo** lango lauke **Lentelės** pavadinimas įveskite **RETAILGIFTCARDTABLE** (mažmeninės prekybos dovanų kortelių lentelę). Lentelės **žymės laukas** turi būti automatiškai nustatytas kaip **Dovanų kortelės lentelė**.
1. Įsitikinkite, kad **žymės langeliai Įrašyti duomenis pagal** įmonę, **Turi** unikalų indeksą ir **Dar ne** bendrai naudojami žymės langeliai. Šių žymės langelių pasirinkimas suaktyvina patikras, susijusias su duomenų bendro naudojimo funkcijomis.
1. Pasirinkite **Įtraukti lentelę**. Dovanų **kortelių lentelės (RetailGiftCardTable)** įrašas dabar turi būti rodomas bendro naudojimo **lentelėse ir laukuose**. Pasirinkite tarpą (^) simbolį, norėdami peržiūrėti visus lentelės laukus, kurie automatiškai susieti su bendro naudojimo lentele.
1. Įmonėse **, kurios bendrai naudoti šių lentelių skyriaus įrašus**, pasirinkite Įtraukti **,** norėdami įtraukti įmonę, su kuria bendrai naudoti duomenis.
1. Eilutės Įmonė **išplečiamajame** sąraše pasirinkite įmonę.
1. **Lauke Pavadinimas** įveskite įmonės pavadinimą.
1. Norėdami pridėti daugiau įmonės eilučių, pakartokite 8–10 žingsnius.
1. Pridėję įmonės eilutes veiksmų srityje pasirinkite **Įgalinti**.
1. Jūs gaunate perspėjimo pranešimą, kuriame teigiama, kad "Rekomenduojama atlikti šį veiksmą tik ne darbo valandomis. Strategijos lentelėse nepavyks atlikti sutampaių operacijų operacijų. Ar norite tęsti?" Jei norite **sutikti,** pasirinkite Taip.
1. Jūs gaunate įspėjamąjį pranešimą, kuriame teigiama: "Ar norėtumėte dabar nukopijuoti visus esamus duomenis visose bendrai naudojamose įmonėse?" Jei norite **sutikti,** pasirinkite Taip.

Kai sutinkate su abiem pranešimais, lentelės pradės kopijuoti duomenis visose sukonfigūruotose įmonėse. Balansai, atsirasti prieš vieną įmonės dovanų kortelę, bus matomi kitai įmonei.

## <a name="additional-resources"></a>Papildomi ištekliai

[DUK apie mokėjimus](payments-retail.md)

[Pirkimo užbaigimo modulis](../add-checkout-module.md)

[Mokėjimo modulis](../payment-module.md)
