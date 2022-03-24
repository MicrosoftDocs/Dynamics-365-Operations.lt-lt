---
title: Skirtumas tarp įtaisytojo bendrojo planavimo ir „Planning Optimization“
description: Šioje temoje pateikiamos funkcijos, kurių „Planning Optimization“ dar nepalaiko ir kurių nėra „Planning Optimization“ analizės puslapyje.
author: ChristianRytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 575aef709a0ac3b0cf8150f1e816dac04c069814
ms.sourcegitcommit: ddcab9726e9dbcf3296cb0988b97a3ae7ccb3dfb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/08/2022
ms.locfileid: "8396504"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>Skirtumas tarp įtaisytojo bendrojo planavimo ir „Planning Optimization“

[!include [banner](../../includes/banner.md)]

„Planning Optimization“ rezultatai gali skirtis nuo įtaisyto bendrojo planavimo modulio rezultatų. Skirtumus gali sukelti laukimo funkcijos. Šioje temoje pateikiamos funkcijos, kurių „Planning Optimization“ dar nepalaiko ir kurių nėra **[„Planning Optimization“ analizės](planning-optimization-fit-analysis.md)** puslapyje].

| Funkcija | Dabartinė „Planning Optimization“ elgsena |
|---|---|
| Esamo svorio produktai | Esamo svorio produktai laikomi įprastais produktais.|
| Extensible dimensijos | Suplanuotuose užsakymuose extensible dimensijos yra tuščios, net jei **Saugojimo dimensijų grupių arba** žymimas laukelis **Padengimo planas pagal** ar **Sekimo dimensijų grupės** puslapyje. |
| Filtruoti gamybos vykdymai | Daugiau informacijos ieškokite [Gamybos planavimas – Filtrai](production-planning.md#filters). |
| Prognozės planavimas | Prognozės planavimas nepalaikomas. Patariame naudoti bendrąjį planavimą, kai prognozės modelis priskiriamas prie bendrojo plano. |
| Suplanuotų užsakymų sekų skaičius | Suplanuotų užsakymų numeracijos nepalaikomos. Suplanuotų užsakymų numeriai generuojami aptarnavimo pusėje. Suplanuoto užsakymo numeris paprastai rodomas 10 skaitmenų, bet iš tikrųjų jį sudaro 20 simbolių, planavimo vykdymo skaičiui priskirta 10 skaitmenų ir kiti 10 suplanuotų užsakymų skaičiavimo skaitmenų. |
| Planuoti kopijavimą, naikinti planą ir plano versijos valymą | <p>Šie elementai išjungti bendrojo planavimo **bendrojo planavimo \> tvarkymo planuose \> naršymo srityje**:</p><ul><li>Plano kopija</li><li>Naikinti planą</li><li>Plano versijos valymas</li></ul> |
| Grąžinimo užsakymai | Grąžinimo užsakymų nelaikomos. |
| Susijusių funkcijų planavimas | Daugiau informacijos žr. [Planavimas, naudojant neribotą pajėgumą](infinite-capacity-planning.md#limitations). |
| Saugos atsargų pildymas | Planavimo optimizavimas visada naudoja *Šiandienos data + įsigijimo laikas* parinktį, skirtą **Įvykdyti minimalų poreikį** laukui, esančiam **Prekės padengimo** puslapyje. Tai padeda sustabdyti nenorimus suplanuotus užsakymus ir kitas problemas, nes jeigu įsigijimo laikas neįtrauktas į saugos atsargas, suplanuoti užsakymai, sukurti dabartinėms mažoms turimoms atsargos, visada bus atidėti dėl gamybos laiko. |
| Saugos atsargų iškvietimas ir grynieji poreikiai | *Saugos atsargų* reikalavimo tipas nėra įtrauktas ir nėra rodomas **Grynųjų poreikių** puslapyje. Saugos atsargos neatspindi poreikio ir neturi su juo susietos poreikio datos. Vietoj to jis nustato apribojimą, kiek atsargų visada turi būti pasiekiama. Tačiau vis dar atsižvelgiama į lauko **Mažiausia** reikšmę apskaičiuojant suplanuotus užsakymus bendrojo planavimo metu. Rekomenduojame patikrinti **Sukauptas kiekis** stulpelį, esantį **Grynųjų poreikių** puslapyje, kad pamatytumėte, jog į šią reikšmę buvo atsižvelgta. |
| Transportavimo kalendoriai | Pristatymo būdų puslapio **Transportavimo kalendorius** stulpelio **vertė ignoruojama**. |
| Min. / maks. padengimo kodas be verčių| Naudojant įtaisytą planavimo sistemą, kai naudojate min. / maks. padengimo kodą, kuriame nėra nustatytos minimalios ar maksimalios vertės, planavimo variklis padengimo kodą laiko reikalavimu ir kiekvienam poreikiui sukuria vieną užsakymą. Sistema sukurs vieną užsakymą per dieną planavimo optimizavimui padengti visą tos dienos sumą.  |

## <a name="additional-resources"></a>Papildomi ištekliai

- [Planavimo optimizavimo tinkamumo analizė](planning-optimization-fit-analysis.md)
- [Planavimo optimizavimo nenaudojami parametrai](not-used-parameters.md)
- [Datos ir laiko parametrai, naudojami „Planning Optimization“](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
