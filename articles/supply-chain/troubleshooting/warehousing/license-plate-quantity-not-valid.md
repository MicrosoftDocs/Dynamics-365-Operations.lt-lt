---
title: Registruojant gaunamo užsakymo kiekį, jis yra netinkamas
description: 'Jeigu numerio lentelėje nurodytas kiekis viršija kiekį, kurį vis dar reikia gauti pagal dabartines dimensijas, gausite klaidos pranešimą: „Kiekis negalioja“.'
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5099b320447bf59c72f5017564ea660f19c690a5
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477132"
---
# <a name="license-plate-quantity-is-not-valid-when-registering-inbound-orders"></a>Leidimo ženklo kiekis negalioja registruojant ateinančius užsakymus

## <a name="symptoms"></a>Požymiai

Kai bandote registruoti ateinančius užsakymus, galite gaut tokį klaidos pranešimą:

> Netinkamas kiekis.

Jeigu laukas **Numerio lentelių grupavimo politika** nustatytas į *Vartotojo apibrėžtas* mobiliojo įrenginio meniu elementui, naudojamam registruoti gaunamiems užsakymams, gausite klaidos pranešimą („Netinkamas kiekis”) ir negalėsite užbaigti registracijos.

## <a name="cause"></a>Priežastis

Kai *Vartotojo apibrėžta* yra naudojama kaip registracijos numerių grupavimo strategija, sistema išskaido gaunamas atsargas į atskiras numerio lenteles, kaip nurodyta pagal vienetų sekų grupę. Jeigu paketo ar serijos numeriai yra naudojami gaunamai prekei sekti, kiekvieno paketo ar serijos kiekiai turi būti nurodyti užregistruotoje numerio lentelėje. Jeigu numerio lentelėje nurodytas kiekis viršija kiekį, kurį vis dar reikia gauti pagal dabartines dimensijas, gausite tokį klaidos pranešimą.

## <a name="resolution"></a>Sprendimas

Kai registruojate prekę naudodami mobiliojo įrenginio meniu elementą, kurio laukas **Numerio lentelių grupavimo strategija** nustatytas į *Vartotojo apibrėžta*, sistema gali reikalauti, kad patvirtintumėte arba įvestumėte numerio lentelės, paketo arba serijos numerius.

Numerio lentelės patvirtinimo puslapyje sistema rodys kiekį, priskirtą dabartinei numerio lentelei. Paketo arba serijos patvirtinimo puslapiuose sistema rodys kiekį, kuris vis dar turi būti gautas pagal dabartinę numerio lentelę. Juose taip pat bus laukas, kuriame galite įvesti registruotiną kiekį tam numerio lentelės ir paketo ar serijos numerio deriniui. Tokiu atveju įsitikinkite, kad registruojamas numerio lentelės kiekis neviršija kiekio, kuris vis dar turi būti gautas.

Kitu atveju, jei gavimo užsakymo registracijoje generuojama per daug numerio numerių, lauko **Numerio lentelių grupavimo strategija** reikšmė gali pasikeisti į *Numerio lentelių grupavimas*, nauja vienetų sekos grupės gali būti priskirta prekei arba parinktis **Numerio lentelių grupavimas** vienetų sekos grupei gali būti deaktyvuota.
