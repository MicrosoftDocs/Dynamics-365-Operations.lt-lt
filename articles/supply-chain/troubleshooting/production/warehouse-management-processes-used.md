---
title: „Warehouse management“ procesai šiuo metu naudojami
description: Rezervuojant ar išleidžiant darbą, galima gauti pranešimą, kad šiuo metu naudojami „Warehouse management“ procesai. Išspręskite problemą vienu iš šių veiksmų.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bfda2fae824cdc64d722310d20cf16e6306d766c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477044"
---
# <a name="cant-reserve-or-release-work-because-processes-are-currently-being-used"></a>Negalima rezervuoti arba išleisti darbo, nes šiuo metu naudojami procesai

## <a name="symptoms"></a>Požymiai

Dirbdami su pranešimais, jūs gaunate šią klaidą:

> „Warehouse management“ procesai šiuo metu naudojami. Jei darbo eilučių dar neregistravote, galite atšaukti sukurtą darbą ir bet kurį krovinį ar siuntimo eilutes ir tuomet tęsti paėmimą ar siuntimo procesą.

## <a name="cause"></a>Priežastis

Ši klaida atsitinka, jei bandote rezervuoti ar atlaisvinti darbą eilutei, bet inventoriaus perleidimo būsena yra *Paimta*, kuri rodo, kad medžiaga buvo paimta.

## <a name="resolution"></a>Sprendimas

Norėdami ištaisyti šią klaidą, atlikite vieną iš tolesnių veiksmų.

- Keiskite gamybos užsakymo būseną atgal į *Apskaičiuota* ar *Išleista*.
- Atverkite informacijos puslapį atitinkamam gamybos užsakymui. Veiksmų juostoje, **Sandėlio** skirtuke **Stabdymo** grupėje pasirinkite **Stabdyti ir išpakuoti** siekiant išpakuoti visas supakuotas perlaidas. Tada pasirinkite **Panaikinti stabdymą** tam, kad apdorotumėte gamybos darbą.

Čia pateikiamas funkcijų *Išpakuoti* ir *Stabdyti* paaiškinimas:
  
- **Išpakuoti** – Ši funkcija atkeičia inventoriaus perlaidų būseną medžiagų važtaraščiui (BOM) eilutėms ir formulės eilutes, kurios turi būseną iš *Paimta* iki *Užsakyme*. Kai darbas žaliavų paėmimui yra užbaigtas, būsena eilutėms nustatyta į *Paimta*. Ši būsena neleidžia gamybos užsakymo paleisti iš naujo į *Sukurta* būseną. Šiuo atveju, galite naudoti *Išpakuoti* funkciją, kad grąžintumėte perlaidas iš *Paimta* būsenos ir tada paleistumėte iš naujo gamybos užsakymą į *Sukurta* būseną.
- **Stabdyti** – Ši funkcija nustato **Sustabdyta** vėliavą gamybos užsakyme siekiant apsaugoti bet kokią naujinimo užsakymo būseną. Galite rasti **Sustabdyta** vėliavą **Sandėlio** „FastTab“ gamybos užsakymo išsamios informacijos puslapyje.

> [!NOTE]
>
> - Mygtukai yra matomi tik, kai gamybos užsakymas yra sukuriamas prekėms įjungtoms sandėlio procesuose.
> - **Stabdymo** grupė yra matoma tik **Sandėlio** skirtuke gamybos užsakymo veiksmų juostos išsamios informacijos puslapyje. Ji nėra matoma **Sandėlio** „FastTab“ puslapyje **Gamybos užsakymai**.
