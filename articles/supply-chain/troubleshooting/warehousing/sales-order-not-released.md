---
title: Nepavyko pateikti pardavimo užsakymo, jei yra siuntimo sandėlio ops
description: Yra kelios priežastys, kodėl galite gauti klaidos pranešimą, kad nepavyko išleisti pardavimo užsakymo. Šiame puslapyje paaiškinama, kodėl ir kaip sumažinti išdavimą.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fca5ee1bc97545ea4de56d940fdedd320a6cfe84
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477107"
---
# <a name="sales-order-could-not-be-released-with-outbound-warehouse-operations"></a>Nepavyko negalite išleisti pardavimo užsakymo, jei yra siuntimo sandėlio operacijoms

## <a name="symptoms"></a>Požymiai

Dirbdami su siuntimo sandėlio operacijomis, galite gauti tokį klaidos pranešimą:

> Nepavyko išleisti pardavimo užsakymo.

## <a name="cause"></a>Priežastis

Ši problema gali įvykti dėl kelių priežasčių. Pavyzdžiui, užsakymą sustabdė kredito valdyba ir jokių siuntimų negalima sukurti kol patvirtinimo pašto adresas yra įvestas pardavimo eilutėms susietoms su pardavimo užsakymu. Kitu atveju, užsakymas yra sustabdytas ir turi būti įvertintas prieš tai, kai jis bus išleistas į sandėlį. Šis sulaikymas gali būti konkretus užsakymui arba būti kliento paskyroje.

## <a name="resolution"></a>Sprendimas

Įtraukite ar naujinkite adresą pardavimo užsakyme ir užsakymo eilutėse ir tuomet paleiskite užsakymą į sandėlį. Užsakymai gali būti išleisti į sandėlį tik jei jie turi galiojantį pristatymo adresą (adreso formato nustatymuose **Organizacijos administracijos** modulyje).

Tirkite sustabdytą užsakymą ir adreso problemas. Tuomet pašalinkite sustabdytą užsakymą ar klientą ir išleiskite užsakymą į sandėlį.
