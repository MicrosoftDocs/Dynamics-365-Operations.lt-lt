---
title: Atsargų matomumo papildinio apžvalga
description: Šioje temoje paaiškinama, kas yra Atsargų matomumas, ir aprašomos jos funkcijos.
author: yufeihuang
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dfc1bc0d457d0b0b2632aa2e2e5ba6a3c2f3fae7
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575176"
---
# <a name="inventory-visibility-add-in-overview"></a>Atsargų matomumo papildinio apžvalga

[!include [banner](../includes/banner.md)]

Inventoriaus matomumo papildinys yra (taip pat vadinamas *Inventoriaus matomumu*) yra nepriklausomos ir labai išdidinamos mikropaslaugos, kurios įjungia realaus laiko turimo inventoriaus sekimą ir taip suteikia bendrą inventoriaus vaizdą. Todėl joje pateikiamas visuotinis atsargų vaizdas.

Išorinės sistemos prieigą prie paslaugos per RESTful API. Tokiu būdu jie gali pateikti turimų atsargų informacijos užklausą duotame dimensijų rinkiniuose arba pakeisti jūsų atsargas skirtinguose pritaikytuose duomenų šaltiniuose.

Kaip mikroservice, įtaisyta „Microsoft Dataverse“ atsargų matomumui, suteikia extensibility. Galite naudoti „Power Apps“ programėlei kurti. Taip pat galite taikyti „Power BI“ norėdami pateikti pritaikytą funkciją, atitinkančią jūsų verslo poreikius.

Galite integruoti atsargų matomumą su keliomis trečiųjų šalių sistemomis, nustatydami standartizuotų atsargų dimensijų konfigūravimo pasirinktis ir nustatydami operacijų tipus. Atsargų matomumas taip pat palaiko pritaikytą extensibility per konfigūruojamus apskaičiuotus kiekius.

## <a name="inventory-visibility-integration-with-dynamics-365-supply-chain-management"></a>Atsargų matomumo integravimo nustatymas su „Dynamics 365 Supply Chain Management“

Integruotas sprendimas atsargų duomenis nuolat seka „Dynamics 365 Supply Chain Management“ iš atsargų pokyčių. Norėdami gauti daugiau informacijos, [įdiekite ir nustatykite atsargų matomumą](inventory-visibility-setup.md) ir [Konfigūruokite atsargų matomumą](inventory-visibility-configuration.md).

## <a name="get-a-global-view-of-inventory"></a>Gauti visuotinį atsargų rodinį

Integruotas sprendimas leidžia apibrėžti savo duomenų šaltinius ir centralizuoti atsargų duomenis. Dėl daugiau informacijos, žr. [Inventoriaus matomumo papildinio konfigūravimas](inventory-visibility-configuration.md).

Yra du būdai savo atsargų peržiūrai:

- Pateikti užklausą naudojant didelio efektyvumo API. Ši API gali grąžinti beveik realiuoju laiku duomenis tiesiai iš talpykloje saugomo egzemplioriaus. Sutarčių ir pavyzdžių galite rasti atsargų [matomumo viešuose API](inventory-visibility-api.md).
- Peržiūrėti turimų atsargų sąrašą. Šis sąrašas yra periodiškai sinchronizuojamas iš talpykloje saugomo egzemplioriaus, jis matomas „Dataverse“. Dėl daugiau informacijos, žr. [Inventoriaus matomumo programa](inventory-visibility-power-platform.md).

## <a name="soft-reservations"></a>Švelniai rezervavimai

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Taikomas švelniai rezervavimas, kai įmonė turi rezervuoti tam tikrą produktų kiekį, kad palaikytų, pvz., pardavimo užsakymų įvykdyimą, kuris išvengs per daug pardavimo. Kai tiekimo grandinės valdymo ar kitose „Supply Chain Management“ sukuriamas ir patvirtinamas pardavimo užsakymas, prašymas rezervuoti kiekį siunčiamas į atsargų matomumą. Atsargų matomumas leidžia rezervuoti produktus, kurių dimensijos informacija ir konkretūs atsargų operacijų tipai yra specifiniai. (Daugiau informacijos žr. [Atsargų matomumo programa](inventory-visibility-power-platform.md).) Kai kiekis sėkmingai rezervuotas, grąžinamas rezervavimo ID. Šį rezervavimo ID galite naudoti norėdami susieti su pradiniu užsakymu „Supply Chain Management“ arba kitose užsakymų valdymo sistemose.

Funkcija sukurta taip, kad rezervavimas atsargų matomume nepakeičia bendrojo kiekio. Vietoj to ji žymi tik rezervuotą kiekį. (Dėl šios priežasties tai vadinama *švelniai rezervavimu*.) Rezervuotą kiekį galima koresponduoti, kai produktai suvartojami „Supply Chain Management“ arba trečiosios šalies sistemoje, kviečiant API vėl atlikti kiekio atskaitymą ir atnaujinti bendrą kiekį atsargų matomumo srityje. Dėl daugiau informacijos, žr. [Inventoriaus matomumo rezervavimas](inventory-visibility-reservations.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
