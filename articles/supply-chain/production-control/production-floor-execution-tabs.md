---
title: Sukurti gamybos aukšto vykdymo sąsają
description: Šioje temoje aprašoma, kaip sukurti vartotojo sąsajos turinį kiekvienam konfigūravimui.
author: johanhoffmann
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 786ea9a3da98e9f1812b007d4301cb47680e6894
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/28/2021
ms.locfileid: "5077583"
---
# <a name="design-the-production-floor-execution-interface"></a>Sukurti gamybos aukšto vykdymo sąsają

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Galite sukurti vartotojo sąsajos turinį kiekvienam konfigūravimui naudojamui gamybos aukšto vykdymo sąsajoje. Pavyzdžiui, darbuotojams viename darbo laukelyje gali reikėti atverti darbo instrukcijas gamybos aukšte, o kitame darbo laukelyje, instrukcijų nereikia. Tokiu atveju, reikia sukurti du konfigūravimus, vieną su mygtuku dokumentų priedų atvėrimui ir vieną be šio mygtuko.

## <a name="design-a-tab"></a>Sukurkite skirtuką

Puslapyje **Konfigūruoti gamybos aukšto vykdymą** galite sukurti ir konfigūruoti skirtukus pasirinkdami **Kurti skirtukus** veiksmų juostoje.

Visi skirtukai padalyti į keturis skyrius kaip parodyti tolesniame paveisklėlyje.

![Skirtuko išdėstymas](media/pfe-tab-layout.png "Skirtuko išdėstymas")

Tolesni elementai rodomi paveikslėlyje:

1. Pagrindinė įrankių juosta
1. Antrinė įrankių juosta
1. Pagrindinis rodinys
1. Išsamus rodinys

Norėdami sukurti ir konfigūruoti naują skirtuką, atlikite šiuos žingsnius:

1. Eikite į **Gamybos valdymą &gt; Nusttymai &gt; Gamybos vykdymas**.

1. Rinkitės **Sukurti skirtukus** veiksmų juostoje, tam, kad atvertumėte **Kūrimo skirtukų** puslapį.

    ![Kūrimo skirtukų puslapis](media/pfe-design-tabs.png "Kūrimo skirtukų puslapis")

1. Veiksmų srityje pasirinkite **Nauja**.

1. Nustatykite tolesnius nustatymus antraštės puslapyje:

    - **Skirtuko pavadinimas** - Nurodykite skirtuko pavadinimą.
    - **Pagrindinis rodinys** - Pasirinkite tarp dviejų iš anksto nustatytų darbo sąrašų (*Įjungti darbai*, *Visi darbai* arba *Mano mašina*).
    - **Išsamios informacijos rodinys** - Pasirinkite tarp tuščios vertės ar **Išsamios darbo informacijos**. Jei pasirinkote tuščią vertę, nebus jokio išsamios informacijos rodinio skirtuke. Jei pasirinkote **Išsami darbo informacija**, išsamiame rodinyje bus išsamus darbo aprašas iš pasirinkto darbo aprašo pagrindiniame rodinyje.

1. Skyriuje **Pirminė įrankių juosta** pasirinkite, kurie mygtukai turi būti prieinami pirminėje įrankių juostoje. Stulpelis **Prieinami veiksmai** rodo visų mygtukų sąrašą, kurie gali būti įtraukti. Stulpelis **Pasirinkti veiksmai** rodo visų mygtukų, įtrauktų į esamą organizaciją, sąrašą. Naudokite mygtukus tarp stulpelių, kad judintumėte pasirinktas prekes tarp stuleplių, kaip būtina. Naudokite mygtukus į viršų ir į apačią šalia **Pasirinkti veiksmai** stulpelius, kad valdytumėte užsakymą, kuriame mygtukai yra rodomi vartotojo sąsajoje.

1. Skyriuje **Antroji** **įrankių juosta** pasirinkite, kurie mygtukai turi būti prieinami antrojoje įrankių juostoje. Stulpelis **Prieinami veiksmai** rodo visų mygtukų sąrašą, kurie gali būti įtraukti. Stulpelis **Pasirinkti veiksmai** rodo visų mygtukų, įtrauktų į esamą organizaciją, sąrašą. Naudokite mygtukus tarp stulpelių, kad judintumėte pasirinktas prekes tarp stuleplių, kaip būtina. Naudokite mygtukus į viršų ir į apačią šalia **Pasirinkti veiksmai** stulpelius, kad valdytumėte užsakymą, kuriame mygtukai yra rodomi vartotojo sąsajoje.

## <a name="associate-a-tab-with-a-configuration"></a>Susiekite skirtuką su konfigūravimu

Jums sukūrųs visus būtinus skirtukus, galite susieti juos su konfigūravimu.

1. Eikite į **Gamybos valdymą &gt; Nusttymai &gt; Konfigūravimo gamybos aukšto vykdymas**.

    ![Konfigūruoti gamybos vietos vykdymą](media/pfe-config-prod-floor-execution.png "Konfigūruoti gamybos vietos vykdymą")

1. „FastTab“ **Skirtuko pasirinkimas** rinkitės **Įtraukti**.

1. Nauja eilutė yra įtraukta į tinklelį. Šiai naujai eilutei, pasirinkite skirtuko pavadinimą, kurį norite įtraukti į konfigūravimą.

1. Tęskite įtraukdami papildomus skirtukus, kaip būtina.

1. Naudokite mygtukus **Judėti aukštyn** ir **Judėti žemyn** įrankių juostoje, kad sudėliotumėte skirtukus kaip reikia. Skirtukai bus rodomi iš kairės į dešinę tvarka rodoma virš momentinės ekrano nuotraukos (skirtukos viršuje rodomas kairėje).
