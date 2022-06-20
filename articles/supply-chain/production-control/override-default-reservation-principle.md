---
title: Numatytojo medžiagų gamybos rezervavimo principo perrašymas
description: Šiame straipsnyje aprašoma, kaip nustatyti kiekvienos prekės modelių grupės numatytąjį rezervavimo principą, kad kiekvienai prekei, kuri yra komplektavimo specifikacijos (KS) arba paketinio užsakymo formulės dalis, automatiškai būtų taikomi skirtingi rezervavimo principai.
author: johanhoffmann
ms.date: 12/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-10
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 381b7fa5046df8f2734e4b242058eb9a673388cf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907238"
---
# <a name="override-the-default-reservation-principle-for-materials-in-production"></a>Numatytojo medžiagų gamybos rezervavimo principo perrašymas

[!include [banner](../includes/banner.md)]

Funkcija *Numatytojo gamybos rezervavimo perrašymas* leidžia nustatyti numatytąjį rezervavimo principą kiekvienai prekių modelių grupei. Todėl galima automatiškai taikyti skirtingus rezervavimo principus kiekvienai prekei, kuri yra gamybos komplektavimo specifikacijos (KS) arba paketinio užsakymo formulės dalis. Galite pasirinkti, ar kiekviena prekių modelių grupė turi pakeisti užsakymui nustatytą numatytąjį rezervavimo principą ir koks principas turėtų būti naudojamas vietoj jo (*neautomatinis*, *įvertinimas*, *planavimas*, *paleidimas* arba *pradžia*).

Kai kuriate naują gamybos arba paketinį užsakymą, esate paraginamas pasirinkti rezervavimo principą, kuris turėtų būti taikomas tam užsakymui ir visoms jo KS arba formulės eilutėms. Kai naudojama *Numatytojo medžiagų gamybos rezervavimo principo perrašymas* funkcija, visos arba kai kurios KS ar formulės eilutės gali perrašyti tą rezervavimo principą ir vietoj jo naudoti atitinkamai prekių modelių grupei nustatytą rezervavimo principą.

Pavyzdžiui, jei turite žaliavų ar ingredientų, kuriems reikia paėmimo darbo, tiems produktams sukurtoms KS ar formulės eilutes reikia rezervuoti faktiškai, nes faktinis rezervavimas yra būtina sandėlio darbo generavimo sąlyga. Paprastai, jei norite, kad rezervavimas būtų atliekamas automatiškai, pasirenkate vieną iš šių rezervavimo principų: *įvertinimas*, *planavimas*, *paleidimas* arba *pradžia*. Kita vertus, jei turite medžiagų ar ingredientų, kuriems nereikia paėmimo darbo, nes jie suvartojami tiesiai iš vietos, paprastai pasirenkate *neautomatinį* rezervavimo principą, kuris neatlieka jokių faktinių rezervavimų ar negeneruoja jokio paėmimo darbo.

## <a name="turn-the-override-default-production-reservation-feature-on-or-off"></a>Įjungti arba išjungti numatytąją gamybos rezervavimo funkciją

Kaip ir tiekimo grandinės valdymo versija 10.0.25 ši funkcija įjungiama pagal numatytąjį nustatymą. Administratoriai šią funkciją gali įjungti arba išjungti, naudodamiesi funkcijų *valdymo darbo srityje funkcija Perrašyti* numatytąją [gamybos rezervavimo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) funkciją.

## <a name="assign-a-production-reservation-policy-to-an-item-model-group"></a>Priskirkite gamybos rezervavimo strategiją prekių modelių grupei

1. Eikite į **Išlaidų valdymas \> Atsargų apskaitos strategijų nustatymas \> Prekių modelių grupės**.
1. Sukurkite arba pasirinkite prekių modelių grupę.
1. „FastTab” **Atsargų strategijos** pasirinkite **Perrašyti prekės gamybos rezervavimą** žymės langelį.
1. Lauke **Rezervavimas** pasirinkite rezervavimo principą prekėms, kurios priklauso pasirinktai modelių grupei. (Šios prekės apima prekes, esančias KS arba formulės eilutėje.)

    - **Neautomatinis** – modelių grupės prekės nebus automatiškai faktiškai rezervuotos gamybai. Tačiau jas vis tiek galima rezervuoti rankiniu būdu, jei reikalinga.
    - **Įvertinimas** – modelių grupės prekės bus faktiškai rezervuotos gamybos užsakymo įvertinimo metu.
    - **Planavimas** – modelių grupės prekės bus faktiškai rezervuotos gamybos užsakymo planavimo metu.
    - **Paleidimas** – modelių grupės prekės bus faktiškai rezervuotos, kai paleidžiamas gamybos užsakymas.
    - **Pradžia** – modelių grupės prekės bus faktiškai rezervuotos gamybos užsakymo pradžioje.

## <a name="example-using-reservation-principles-in-a-bulkpack-scenario"></a>Pavyzdys: Rezervavimo principų naudojimas masinio/supakuoto užsakymo scenarijuje

Masinė tepalo medžiaga gaminama naudojant 1000 litrų talpos maišytuvą. Kai masinė medžiaga yra paruošta, ji išpumpuojama į kelias užpildymo stotis, kur užpildomi skirtingo dydžio buteliai. Baigus užpildymą, buteliai supakuojami į dėžes. Tada šios dėžės yra supakuojamos ant padėklų.

Šiame scenarijuje sukuriamas paketo užsakymas, skirtas sukurti 1000 litrų masinės medžiagos. (Toks užsakymas yra masinis užsakymas.) Kai šis paketinis užsakymas yra baigtas, jis paskelbtas kaip atliktas į užpildymo stočių medžiagų tiekimo vietą. Tada sukuriamas paketinis užsakymas, skirtas užpildyti ir supakuoti kiekvieno dydžio butelį. (Tokie užsakymai yra pakavimo užsakymai.) Juose yra formulė, kurią sudaro masinė medžiaga, tuščias butelis, etiketė ir kitos pakavimo medžiagos. Dėl to, kad masinės medžiagos srautai teka tiesiogiai iš maišytuvo talpyklos į užpildymo stotis, šiam ingredientui paimti nereikia jokio sandėlio darbo, o masinė medžiaga yra suvartojama tiesiai iš tiekimo vietos. Todėl rezervavimo principas yra nustatomas kaip *Neautomatinis*. Kitos medžiagos yra gabenamos į užpildymo stotį paėmimo būdu. Todėl šių eilučių rezervavimo principas nustatytas kaip *paleidimas*, pavyzdžiui, todėl, kad paleidus pakavimo užsakymą, automatiškai įvyksta rezervavimas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]