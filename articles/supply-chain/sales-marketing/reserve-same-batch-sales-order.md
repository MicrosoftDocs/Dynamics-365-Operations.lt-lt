---
title: To paties pardavimo užsakymo paketo rezervavimas
description: Šiame straipsnyje paaiškinta, kaip nustatyti produktą, kad būtų leidžiamas atsargų rezervavimas pagal vieną atsargų paketą.
author: omulvad
manager: tfehr
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce750745d6f094a296b43827568ee1745179de2d
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434006"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a>To paties pardavimo užsakymo paketo rezervavimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinta, kaip nustatyti produktą, kad būtų leidžiamas atsargų rezervavimas pagal vieną atsargų paketą.

To paties paketo rezervavimas leidžia pardavimo užsakymo eilutės atsargas rezervuoti pagal vieną atsargų paketą. Pvz., klientas, kuris užsisako tapetų, gali reikalauti, kad visas užsakymas būtų užpildytas iš to pačio paketo ar partijos, kad būtų išvengta rulonų neatitikimų. Norint nustatyti, kad su produktu būtų naudojamas to paties paketo rezervavimas, prekių modelių grupėje, sekimo dimensijų grupėje ir saugojimo dimensijų grupėje, kurias priskiriate produktui, turi būti aktyvios tolesnės nuostatos.

- **Prekių modelių grupės** – prekių modelių grupėje turi būti pasirinkti atsargų strategijų laukų grupės **Rezervavimas** laukai **To paties paketo parinkimas** ir **Konsoliduoti reikalavimą**.
- **Sekimo dimensijų grupės** – sekimo dimensijų grupėje turi būti pasirinktas paketo numerio laukas **Padengimo planas pagal dimensiją**.
- **Saugojimo dimensijų grupės** – saugojimo dimensijų grupėje turi būti pasirinktas **Teritorijos** ir **Sandėlio** laukas **Padengimo planas pagal dimensiją**.

Kai produkto atsargas rezervuojate pardavimo užsakymo eilutėje, su kuria nustatyta naudoti to paties paketo parinkimą, sistema užsakytą kiekį bando rezervuoti iš vieno atsargų paketo. Taip pat atsižvelgiama į visus konkrečius paketo atributo reikalavimus. Jei kiekio iš vieno paketo užpildyti negalima, rodomas puslapis **To paties paketo rezervavimo nesuderinamumas**. Šiame puslapyje apibūdinamos problemos bei veiksmai, kuriuos galite atlikti norėdami tęsti rezervavimą. Paketas gali būti nerezervuojamas esant tolesnėms sąlygoms.

- Paketo perdavimo kodo pardavimo parinktis **Blokuoti rezervavimą** pažymėta kaip **Užblokuota**.
- Paketas baigė galioti pagal galiojimo pabaigos datą ir bet kokias taikomas klientų pardavimo dienas. Prekė vis dar gali būti svarstytina rezervuoti, jei prekės modelių grupė yra data valdomas rezervavimas „pirmas baigė galioti – pirmas baigėsi“ (FEFO) ir jei kaip paėmimo kriterijus pasirinkta galiojimo pabaigos data.
- Liko nepakankamai paketo galiojimo dienų, atsižvelgiant į galiojimo pabaigos datą ir geriausia iki datą bei visas kliento pardavimo dienas.

Elementams, susijusiems su saugyklos dimensijų grupe, kuriuose įjungta funkcija **„Naudoti sandėlio tvarkymo procesus“**, galite rezervuoti konkrečius paketų numerius, naudodami rezervavimo hierarchiją su paketo numerio atsargų dimensija, kuri apibrėžta virš vietos dimensijos. Puslapyje **Paketo rezervacija**, kuris skirtas pardavimams ir užsakymo perkėlimo eilutėms, taip pat galima pasirinkti ir rezervuoti kelias eilutes, atsižvelgiant į galimus paketų numerius. Norėdami gauti daugiau informacijos apie tai, ką daryti, jei naudojate rezervavimo hierarchiją, kurios paketo numerio dimensija yra žemiau už vietos dimensiją, žr. [Lanksti sandėlio lygio dimensijos rezervavimo politika](../warehousing/flexible-warehouse-level-dimension-reservation.md).
