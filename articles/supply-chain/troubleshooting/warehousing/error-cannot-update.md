---
title: Registruojant išrinkimo sąrašą pasirenkama vieta, įvyko klaida
description: Registruojant išrinkimo sąrašą pasirenkama vieta, įvyko klaida.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: da5905fb7ed1e890c85e891843379aa07de3279bd8972d6fc57136aa703c9ea4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762799"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a>Registruojant išrinkimo sąrašą pasirenkama vieta, įvyko klaida

KB numeris: 4613106

## <a name="symptoms"></a>Požymiai

Ši problema kyla, kai jūsų sistema konfigūruota automatiškai rezervuoti pardavimo užsakymus. Jei bandote pasirinkti vietą išrinkimo dokumento registravimo eilutei, naudodami sandėlio valdymo (WMS) rezervavimo procesus, gaunate toliau nurodytą klaidos pranešimą:

> Negalima atnaujinti kiekio su naujomis dimensijomis

Šis išdavimas gali atsirasti, nes tam tikrai vietai nepakanka turimų atsargų.

## <a name="resolution"></a>Skiriamoji geba

Sistema veikia kaip sukurta.

Scenarijuose, kuriuose naudojate sandėlio lygio rezervavimo procesą, jei turimos atsargos nebus rezervuojamos visuose atsargų dimensijų lygiuose ir jei tam tikrai vietai nepakanka turimų atsargų, rekomenduojame naudoti rezervavimo iš išrinkimo eilutės neautomatiniu būdu procesą. Tada galite naudoti funkciją *Rezervuoti partiją* norėdami paskirstyti visų turimus kiekius mažesnius rezervavimus, pvz., vietą.
