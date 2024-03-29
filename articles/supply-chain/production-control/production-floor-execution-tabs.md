---
title: Sukurti gamybos aukšto vykdymo sąsają
description: Šiame straipsnyje aprašoma, kaip sukurti kiekvienos konfigūracijos vartotojo sąsajos turinį.
author: johanhoffmann
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration, JmgProductionFloorExecutionConfigurationTab
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 66190ab261d19c718e13801c17a34b915ccf158c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852250"
---
# <a name="design-the-production-floor-execution-interface"></a>Sukurti gamybos aukšto vykdymo sąsają

[!include [banner](../includes/banner.md)]

Galite sukurti vartotojo sąsajos turinį kiekvienam konfigūravimui, kuris naudojamas gamybos aukšto vykdymo sąsajoje. Pavyzdžiui, darbuotojams viename darbo laukelyje gali reikėti atverti darbo instrukcijas gamybos aukšte, o kitame darbo laukelyje, instrukcijų nereikia. Tokiu atveju, reikia sukurti du konfigūravimus, vieną su mygtuku dokumentų priedų atvėrimui ir vieną be šio mygtuko.

## <a name="design-a-tab"></a>Sukurkite skirtuką

Puslapyje **Konfigūruoti gamybos aukšto vykdymą** galite sukurti ir konfigūruoti skirtukus pasirinkdami **Kurti skirtukus** veiksmų juostoje.

Visi skirtukai padalyti į keturis skyrius, kaip parodyta tolesniame paveikslėlyje.

![Skirtuko išdėstymas.](media/pfe-tab-layout.png "Skirtuko išdėstymas")

Tolesni elementai rodomi paveikslėlyje:

1. Pagrindinė įrankių juosta
1. Antrinė įrankių juosta
1. Pagrindinis rodinys
1. Išsamus rodinys

Norėdami sukurti ir konfigūruoti naują skirtuką, atlikite šiuos žingsnius:

1. Eikite į **Gamybos kontrolė \> Sąranka \> Gamybos vykdymas \> Gamybos cecho vykdymo konfigūravimas**.

1. Rinkitės **Sukurti skirtukus** veiksmų juostoje, tam, kad atvertumėte **Kūrimo skirtukų** puslapį.

    ![Kūrimo skirtukų puslapis.](media/pfe-design-tabs.png "Kūrimo skirtukų puslapis")

1. Veiksmų srityje pasirinkite **Nauja**.

1. Nustatykite tolesnius nustatymus antraštės puslapyje:

    - **Skirtuko** pavadinimas – nurodykite skirtuko pavadinimą.
    - **Pagrindinis rodinys** – pasirinkite iš anksto apibrėžtų užduočių sąrašų (*aktyvių* užduočių, *visų užduočių*, mano *užduočių* ir mano *įrenginio*).
    - **Informacijos rodinys** – pasirinkite tarp tuščios vertės arba **užduoties informacijos**. Jei pasirinkote tuščią vertę, nebus jokio išsamios informacijos rodinio skirtuke. Jei pasirinkote **Išsami darbo informacija**, išsamiame rodinyje bus išsamus darbo aprašas iš pasirinkto darbo aprašo pagrindiniame rodinyje.

1. Skyriuje **Pirminė įrankių juosta** pasirinkite, kurie mygtukai turi būti prieinami pirminėje įrankių juostoje. Stulpelis **Prieinami veiksmai** rodo visų mygtukų sąrašą, kurie gali būti įtraukti. Stulpelis **Pasirinkti veiksmai** rodo visų mygtukų, įtrauktų į esamą organizaciją, sąrašą. Naudokite mygtukus tarp stulpelių, kad judintumėte pasirinktas prekes tarp stulpelių, kaip būtina. Naudokite mygtukus į viršų ir į apačią šalia **Pasirinkti veiksmai** stulpelius, kad valdytumėte užsakymą, kuriame mygtukai yra rodomi vartotojo sąsajoje.

1. Antrinės įrankių **juostos skyriuje** pasirinkite, kurie mygtukai turi būti galimi antrinėje įrankių juostoje. Stulpelis **Prieinami veiksmai** rodo visų mygtukų sąrašą, kurie gali būti įtraukti. Stulpelis **Pasirinkti veiksmai** rodo visų mygtukų, įtrauktų į esamą organizaciją, sąrašą. Naudokite mygtukus tarp stulpelių, kad judintumėte pasirinktas prekes tarp stulpelių, kaip būtina. Naudokite mygtukus į viršų ir į apačią šalia **Pasirinkti veiksmai** stulpelius, kad valdytumėte užsakymą, kuriame mygtukai yra rodomi vartotojo sąsajoje.

## <a name="associate-a-tab-with-a-configuration"></a>Susiekite skirtuką su konfigūravimu

Sukūrę visus būtinus skirtukus galite susieti juos su konfigūravimu.

1. Eikite į **Gamybos kontrolė \> Sąranka \> Gamybos vykdymas \> Gamybos cecho vykdymo konfigūravimas**.

    ![Konfigūruoti gamybos vietos vykdymą.](media/pfe-config-prod-floor-execution.png "Konfigūruoti gamybos vietos vykdymą")

1. „FastTab“ **Skirtuko pasirinkimas** rinkitės **Įtraukti**.

1. Nauja eilutė yra įtraukta į tinklelį. Šiai naujai eilutei, pasirinkite skirtuko pavadinimą, kurį norite įtraukti į konfigūravimą.

1. Tęskite įtraukdami papildomus skirtukus, kaip būtina.

1. Naudokite mygtukus **Judėti aukštyn** ir **Judėti žemyn** įrankių juostoje, kad sudėliotumėte skirtukus kaip reikia. Skirtukai bus rodomi iš kairės į dešinę tvarka rodoma virš momentinės ekrano nuotraukos (skirtuko viršuje rodomas kairėje).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
