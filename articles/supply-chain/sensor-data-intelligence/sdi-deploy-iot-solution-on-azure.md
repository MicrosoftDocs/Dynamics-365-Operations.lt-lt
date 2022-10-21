---
title: „IoT“ sprendimo diegimas „Azure“
description: "\"Jutiklio duomenų įžvalgos\" naudoja jutiklių, kurie sujungti, duomenis Microsoft Azure. Šiame straipsnyje paaiškinama, kaip į savo \"Azure\" abonementą įdiegti objektų (internetu) sprendimą."
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreAzureResourceDeploymentWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 5f0f49c0f7daaacb85b75dc11b9f015b6aa4e997
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689727"
---
# <a name="deploy-an-iot-solution-on-azure"></a>„IoT“ sprendimo diegimas „Azure“

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

"Jutiklio duomenų įžvalgos" naudoja jutiklių, kurie sujungti, duomenis Microsoft Azure. Norėdami įgalinti Azure gauti Dynamics 365 Supply Chain Management duomenis iš jūsų jutiklių ir bendrai naudoti juos, "Azure" abonemente turite įdiegti "Things" ("IoT) sprendimą. Šioje architektūros diagramoje pateikiama sprendimo ir jo komponentų apžvalga.

![Jutiklio duomenų įžvalgų diagrama.](media/sdi-architecture.png "Jutiklio duomenų įžvalgų diagrama")

## <a name="video-instructions"></a>Vaizdo įrašų instrukcijos

Toliau pateiktame vaizdo įraše parodyta, kaip [įjungti "Azure" duomenų tyrimų funkciją](sdi-enable-feature.md) ir įdiegti reikiamus "Azure" išteklius. Kitas šio straipsnio skyrius pateikia tas pačias instrukcijas tekstiniu formatu.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE58g3I]

## <a name="procedure"></a>Procedūra

Norėdami įdiegti reikiamus išteklius "Azure", atlikite šiuos veiksmus.

1. Prisijungti prie tiekimo grandinės valdymo kaip administratorius.
1. Eiti į sistemos **administravimo nustatymo "\>\> Intelligence IntelligenceDeploy" \> ir sujunkite "Azure" išteklius**, kad atidarytumėte diegimo vedlį.
1. Pasisveikimo **puslapyje** perskaitykite informaciją ir pasirinkite **Pirmyn**.
1. **"Deploy" "IoT" sprendimo pavyzdys "Azure**" puslapyje, perskaitykite informaciją, **tada** instrukcijų skyriuje pasirinkite **Diegti**.
1. Atidaromas naujas naršyklės skirtukas, į kurį pereisite į "Azure" portalą, kad būtų galima diegti "Azure" išteklius. Jei būsite paraginti, prisiregistruokite naudodami savo "Azure" abonemento kredencialus.
1. Pasirinktinio **diegimo** puslapio lauke Abonementas **pasirinkite** abonementą.
1. Išteklių grupės **lauke pasirinkite** Kurti naują **, kad sukurtumėte** "Azure" komponentų, kuriuos diegiate, išteklių grupę.
1. Išplečiamajame dialogo lange, **kuris** pasirodo lauke Pavadinimas, įveskite naujos išteklių grupės pavadinimą (pvz., *IoT-demo*). Tada pasirinkite **Gerai**.
1. Užpildykite toliau nurodytus laukus:

    - **Išteklių grupė** – pasirinkite ką tik sukurtą išteklių grupę.
    - **Regionas** – pasirinkite regioną, geriausia tai, kuriame įdiegta tiekimo grandinės valdymo aplinka. Atkreipkite dėmesį, kad "Azure" regionai turi skirtingas kainas. Galite peržiūrėti numatomas savo regiono išlaidas naudodami Jutiklio duomenų [įžvalgų kainos skaičiuotuvą](https://azure.com/e/c36c4947ebff4215b2e62590c2a24c68).
    - **Tiekimo grandinės valdymo aplinkos URL** – įveskite savo tiekimo grandinės valdymo aplinkos URL.
    - **Pakartotinai naudoti esamą "Azure" "Azure" "IoT"** centrą – palikite šį žymės langelį išvalytą.

1. Pasirinkite **Pirmyn: Peržiūra + Kurti**.
1. Pasirinktinio **diegimo puslapyje** patikrinkite, ar tikrinimas ėjo sėkmingai, tada pasirinkite **Kurti**.
1. Diegimo **puslapis seka** diegimo eigą. Diegimo procesas gali užtrukti iki 30 minučių. Kai diegimas **vyksta puslapyje,** nurodoma, kad diegimas baigtas, pasirinkite išteklių grupės pavadinimo saitą, kad atidarytumėte puslapį, kuriame rodomas grupėje įdiegtų išteklių sąrašas.
1. Išteklių sąraše raskite įrašą, kuriame laukas **Tipas nustatytas** kaip Valdoma *tapatybė*. Stulpelyje **Pavadinimas** pasirinkite pavadinimą, kad atidarytumėte ištekliaus informacijos puslapį.
1. Kopijuoti vertę lauke Kliento **ID** (pvz., pasirenkant mygtuką **Kopijuoti į mainų** sritį).
1. Grįžkite į naršyklės skirtuką, kuriame vykdomas tiekimo grandinės valdymas, *tačiau neuždaryti "Azure" portalo skirtuko*. Vis **tiek reikia atidaryti "Azure** " vedlio puslapyje įdiegti "IoT" sprendimo pavyzdį. 
1. Pasirinkite **Toliau**.
1. **"Connect Azure" išteklių** puslapyje, programos kliento **Azure AD ID** lauke, įklijuokite nukopijuotą **kliento ID** vertę.
1. Grįžkite į naršyklės skirtuką, kuriame atidarytas "Azure" portalas, *tačiau neuždaryti tiekimo grandinės valdymo skirtuko*. Ištekliaus informacijos puslapis vis tiek turi būti atidarytas.
1. Pasirinkite naršyklės mygtuką Grįžti **, norėdami** grįžti į naujos išteklių grupės išteklių sąrašą.
1. Išteklių sąraše raskite įrašą, kur tipo laukas nustatytas **kaip** "Azure" talpykla *, skirta "Redis"*. Stulpelyje **Pavadinimas** pasirinkite pavadinimą, kad atidarytumėte ištekliaus informacijos puslapį.
1. Kairiojoje naršymo srityje pasirinkite Prieigos **raktai**.
1. Prieigos raktų **puslapyje kopijuokite reikšmę, kuri rodoma pirminio jungimosi eilutėje (StackExchange.Redis)** (pvz., **pasirinkdami** mygtuką Kopijuoti į mainų **sritį**).
1. Grįžti prie naršyklės skirtuko, kuriame veikia tiekimo grandinės valdymas. " **Connect Azure" išteklių** puslapį vis tiek reikia atidaryti.
1. **Redis metrinės saugyklos ryšio eilutės** lauke įklijuokite **nukopijuotą pirminio jungimosi eilutę (StackExchange.Redis).**
1. Pasirinkite **Baigti**.

"Azure" ištekliai, skirti "Azure" duomenų įžvalgoms, diegiami jūsų "Azure" abonemente.

> [!NOTE]
> Bet kuriuo metu galite peržiūrėti arba redaguoti ryšio informaciją **, įrašytą tiekimo grandinės valdymo dalyje, atidarę "Jutiklio duomenų tyrimų" parametrų** puslapį. Norėdami gauti daugiau informacijos, žr. " [Jutiklio duomenų tyrimų" parametrus](sdi-parameters.md).
