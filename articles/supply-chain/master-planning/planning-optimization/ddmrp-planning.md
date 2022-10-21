---
title: Poreikio planavimas
description: Šiame straipsnyje aprašoma, kaip generuoti suplanuotus prekių, kurios nustatytos kaip atsišiejimo taškai, užsakymus.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: f1e2cfca47d507c8de7f9323bb8e4262a0e90949
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689210"
---
# <a name="demand-driven-planning"></a>Poreikio planavimas

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Šiame straipsnyje aprašoma, kaip generuoti suplanuotus prekių, kurios nustatytos kaip atsišiejimo taškai, užsakymus.

## <a name="net-flow-and-qualified-demand"></a>Grynasis srautas ir reikalavimus atitinkantis poreikis

Bendrojo planavimo metu sistema taiko grynojo srauto sąvoką, kad nustatytų faktiškai turimas atsargas bei užsakytas atsargas (esamus tiekimo užsakymus, kurie dar ne gauti), *atėmus* tai, *kas* vadinama apibrėžtu poreikiu (patikslinęs būsimą pardavimą), kaip parodyta toliau pateiktoje pavyzdyje. Kai sistema nustato, kuriai buferio zonai priklauso prekė ir koks turėtų būti užsakytas kiekis, sistema įvertina grynąjį srautą, o ne faktines turimų atsargų atsargas.

![Grynojo srauto skaičiavimo diagramos pavyzdys.](media/ddmrp-net-flow-example.png "Grynojo srauto skaičiavimo diagramos pavyzdys")

Kai suplanuotas užsakymas suaktyvinamas planavimo vykdymo metu, užsakytas kiekis bus maksimalus lygis, atėmus grynąjį srautą. Užsakymų prioritetui priskirti sistema naudoja prioriteto [planavimo funkcijas](priority-based-planning.md), o ne poreikio datas. Poreikio valdomas medžiagų poreikių planavimas (DDMRP) priskiria suplanuoto užsakymo prioritetą, remiantis užsakymu kiekiu kaip maksimalių atsargų procentinė dalis. Ankstesniame pavyzdyje užsakytas kiekis yra 53% didžiausio kiekio. Todėl papildymo užsakymo prioritetas bus 53. (Kontekstas 0 yra aukščiausias prioritetas, o 100 – žemiausias prioritetas.)

*Reikalavimus atitinkantis* poreikis yra praeities poreikis, šiandienos poreikis ir būsimas apibrėžto užsakymo praėjimas. Toliau esanti iliustracija pateikia šiandienos (birželio 12 d.) ir kitų trijų dienų poreikio lygių pavyzdį. DDMRP leidžia nustatyti užsakymo slenkstį, siekiant nustatyti poreikį, kuris viršija įprastas lūkesčius. Jei nustatytas 25 vienetų slenkstis, dvi iš pavyzdyje parodytų būsimų datų gali būti laikomos užsakymo siejikaimis. Turite kiekvienam produktui priskirti užsakymo **slenkstį** atskirai, naudodami jo prekių padengimo puslapį, [kaip aprašyta iššiupimo taškų prekės buferių nurodyme](ddmrp-buffer-profile-and-levels.md#set-up-buffers).

![Apibrėžto poreikio skaičiavimo diagramos pavyzdys.](media/ddmrp-net-qualified-demand-example.png "Apibrėžto poreikio skaičiavimo diagramos pavyzdys")

Atsižvelgdami į tai, kad nėra vėliausio poreikio, dabar galite pridėti šiandienos poreikį (18) prie dviejų užsakymo kiekių (29 ir 26), kad būtų reikalaujama apibrėžto poreikio 73. Nors reikia birželio 23 d., atkreipkite dėmesį, kad jis neįtrauktas į grynojo srauto skaičiavimą, nes DDMRP suaktyvina suplanuotą užsakymą kitaip nei tradicinės planavimo padengimo grupės.

## <a name="generating-planned-orders-with-ddmrp"></a>Suplanuotų užsakymų generavimas su DDMRP

Planuojant sistema sukurs naują suplanuotą užsakymą, jei prekės grynasis srautas bus žemiau užsakymo vietos žemiau. Naudojant DDMRP, paprastai planavimas vykdomas kiekvieną dieną. Todėl iš esmės jūs iš esmės tikrinate savo atsargų lygius kartą per dieną, kad nustatytumėte, kurios prekės turi būti papildytos.

Šis pavyzdys rodo situacijos, kurioje birželio 20 d. turite 18 vienetų užsakymą, birželio 21 d. – 29 vienetai, birželio 22 d. – 26 vienetai, birželio 23 d. – 20 vienetų, pavyzdys. Kadangi nustatytas 25 vienetų slenkstis, du iš šių užsakymų pažymėti kaip slenkstis. Yra 220 šios prekės vienetų.

![1 planavimo pavyzdys.](media/ddmrp-planning-example-1.png "1 planavimo pavyzdys")

Jei paleisite bendrąjį planavimą dabar, bus sugeneruotas suplanuotas užsakymas, jei bus rastas grynasis srautas žemiau užsakymo taško (šiame pavyzdyje – 219 vienetų).

![2 planavimo pavyzdys.](media/ddmrp-planning-example-2.png "2 planavimo pavyzdys")

Pagal šį pavyzdį pateikiamas suplanuotas pirkimo užsakymas, kurio kiekis yra 130, o jis lygus maksimaliam lygiui, atėmus grynąjį srautą. Suplanuotam užsakymui priskiriamas 53,07 prioritetas, remiantis jo didžiausio kiekio procentu. Kadangi šios vertės buvo rastas birželio 20 d., sistema sukuria suplanuotą užsakymą, kuris data yra birželio 20 d., pridėjus nurodytą prekės gamybos laiką (šiame pavyzdyje penkios verslo dienos). Todėl, kadangi šiandien yra penkios darbo dienos, tai yra viena savaitė, suplanuoto užsakymo data yra birželio 27 d.

> [!NOTE]
> Planavimo optimizavimas skaičiuoja tik išjungtas prekes naudojant DDMRP. Visos kitos prekės skaičiuojamos naudojant standartinių medžiagų poreikių planavimą (MRP).
