---
title: Modulio Iškrovimo kaina ataskaitos
description: Šiame straipsnyje aprašoma, kaip rasti ir naudoti įvairių tipų ataskaitas, naudojamas sklypų išlaidų modulyje.
author: Weijiesa
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 836d6b538b32d818ed3b825000d004b005ce95d8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905956"
---
# <a name="landed-cost-reports"></a>Modulio Iškrovimo kaina ataskaitos

[!include [banner](../../includes/banner.md)]

## <a name="outstanding-invoices"></a>Neapmokėtos sąskaitos faktūros

Neapmokėtų SF ataskaitoje yra įvairių išlaidų lygių, susijusių su kiekvienu reisu, visų neapmokėtų SF sąrašas. Jis naudojamas reisui ir reiso išlaidoms reguliariai suderinti su didžiosios knygos operacijų sąrašu. Išrašius pridėtinių išlaidų SF, ji pašalinama iš ataskaitos.

Norėdami sugeneruoti neapmokėtų SF ataskaitą, atlikite šiuos veiksmus.

1. Eikite į **Iškrovimo kaina \> Ataskaitos \> Sekimas \> Neapmokėtos SF**.
1. Dialogo lango **Neapmokėtos SF** lauke **Kaip data** nurodykite datą. Bet kuri SF, kuri buvo neapmokėta tą datą arba anksčiau, bus įtraukta į išvestį.
1. Dalyje **Rodyti** pasirinkite vieną iš pateiktų parinkčių.

    - **Išlaidos, kurių SF neišrašyta** – įtraukite siuntų, kurioms išrašytos SF ir kurių savikaina įvertinta, o faktinės išlaidos – ne, išlaidas.
    - **Atsargos, kurių SF neišrašyta** – įtraukite išlaidas, kurių SF išrašytos, bet pirkimo užsakymas dar negautas.
    - **Viskas, kam SF neišrašyta** – įtraukite ir parinkties **Išlaidos, kurių SF neišrašyta**, ir parinkties **Atsargos, kurių SF neišrašyta** rezultatus.

1. Nustatykite parinktį **Įtraukti naujas išlaidas** į *Taip*, norėdami įtraukti išlaidas, kurių faktinių išlaidų dar nėra ir kurių atsargos nėra gautos. Jei nustatysite į *Ne*, ataskaitoje bus įtrauktos tik tos išlaidos, kurių SF išrašytos.
1. Skyriuje **Peržiūra** įgalinkite kiekvieną informacijos tipą, kurį norite įtraukti į ataskaitą.
1. Kaip ir dirbdami su kitų tipų ataskaitomis programoje „Microsoft Dynamics 365 Supply Chain Management”, naudokite „FastTab” **Paskirties vieta**, norėdami pasirinkti ataskaitos išvesties formatą.
1. Kaip ir dirbdami su kitų tipų ataskaitomis „Supply Chain Management”, norėdami toliau riboti įrašus, kurie bus įtraukti į ataskaitą, naudokite „FastTab” **Įtrauktini įrašai**.
1. Pasirinkite **Gerai**, kad sugeneruotumėte šią ataskaitą.

## <a name="activityprovider-analysis-reports"></a>Veiklos / teikėjų analizės ataskaitos

Veiklos / teikėjų analizės ataskaitos leidžia peržiūrėti kiekvieno teikėjo laiko įvertinimo tikslumą.

Norėdami sugeneruoti veiklos / teikėjų analizės ataskaitą, atlikite šiuos veiksmus.

1. Atsižvelgdami į norimos kurti ataskaitos tipą, atlikite vieną iš toliau pateiktų veiksmų.

    - Eikite į **Iškrovimo kaina \> Ataskaitos \> Veiklos / teikėjų analizė pagal veiklą**. Šiuo atveju laiko įvertinimai bus grupuojami pagal veiklą.
    - Eikite į **Iškrovimo kaina \> Ataskaitos \> Veiklos / teikėjų analizė pagal teikėją**. Šiuo atveju laiko įvertinimai bus grupuojami pagal teikėją.

    Rodomas dialogo langas **Veiklos / teikėjų analizė pagal veiklą** arba dialogo langas **Veiklos / teikėjų analizė pagal teikėją**. Abiejuose dialogo languose pateikiamos tos pačios parinktys.

1. Kaip ir dirbdami su kitų tipų ataskaitomis „Supply Chain Management”, naudokite „FastTab” **Paskirties vieta**, norėdami pasirinkti ataskaitos išvesties formatą.
1. Kaip ir dirbdami su kitų tipų ataskaitomis „Supply Chain Management”, norėdami toliau riboti įrašus, kurie bus įtraukti į ataskaitą, naudokite „FastTab” **Įtrauktini įrašai**.
1. Pasirinkite **Gerai**, kad sugeneruotumėte šią ataskaitą.

## <a name="voyage-costing-reports"></a>Reiso įkainojimo ataskaitos

Reiso įkainojimo ataskaitos nurodo prekių išlaidas ir importavimo išlaidas pagal sąskaitos lapą, gabenimo konteinerį ar reisą, atsižvelgiant į parinktis, kurias pažymėjote generuodami ataskaitą. Kiekviena reiso įkainojimo ataskaita leidžia palyginti reiso įvertintą savikainą su faktinėmis išlaidomis ir ataskaitą galima išskaidyti pagal keletą identifikavimo veiksnių.

Norėdami sugeneruoti reiso įkainojimo ataskaitą, atlikite šiuos veiksmus.

1. Atsižvelgdami į norimos kurti ataskaitos tipą, atlikite vieną iš toliau pateiktų veiksmų.

    - Eikite į **Iškrovimo kaina \> Ataskaitos \> Įkainojimas \> Reiso įkainojimas pagal atskiras išlaidas**. Šiuo atveju atskirų išlaidų parinktis nurodys kiekvieno išlaidų tipo kodo ir išlaidų srities importo išlaidas.
    - Eikite į **Iškrovimo kaina \> Ataskaitos \> Įkainojimas \> Reiso įkainojimas pagal ataskaitos kategoriją**. Šiuo atveju importo išlaidos bus išskaidytos į įvairias ataskaitų kategorijas. Išlaidų tipai grupuojami pagal ataskaitų kategorijas.

    Atsiranda dialogo langas **Reiso įkainojimas pagal atskiras išlaidas** arba dialogo langas **Reiso įkainojimas pagal ataskaitos kategoriją**. Šie dialogo langai panašūs. Bet kokie skirtumai pažymimi likusioje šios procedūros dalyje.

1. Jei atidarėte dialogo langą **Reiso įkainojimas pagal ataskaitos kategoriją**, lauke **Išlaidos** pasirinkite vieną iš toliau pateiktų reikšmių.

    - **Išlaidų vertė** – vertė skaičiuojama naudojant automatines išlaidas arba rankiniu būdu sukuriama išlaidų srityje.
    - **Įvertinta** – kai prekės gautos, nustatoma įvertinta savikaina.
    - **Faktinės išlaidos** – kai užsakymo SF išrašyta, faktinės išlaidos nustatomos pagal SF nurodytas išlaidas.
    - **Tinkamiausia** – sistema naudos tinkamiausią iš aukščiau pateiktų trijų parinkčių. (Rekomenduojame pažymėti šią parinktį.)

1. Norėdami parodyti kiekvienos prekės išlaidas, nustatykite parinktį **Kiekvienos prekės** į *Taip*. Nustatykite į *Ne*, kad išlaidos būtų rodomos pagal reisą.
1. Skyriuje **Peržiūra** pasirinkite kategorijas, pagal kurias norite išskaidyti išlaidas.
1. Skyriuje **Dimensijos** pasirinkite dimensijas, kurios bus įtrauktos į ataskaitą.
1. Kaip ir dirbdami su kitų tipų ataskaitomis „Supply Chain Management”, naudokite „FastTab” **Paskirties vieta**, norėdami pasirinkti ataskaitos išvesties formatą.
1. Kaip ir dirbdami su kitų tipų ataskaitomis „Supply Chain Management”, norėdami toliau riboti įrašus, kurie bus įtraukti į ataskaitą, naudokite „FastTab” **Įtrauktini įrašai**.
1. Pasirinkite **Gerai**, kad sugeneruotumėte šią ataskaitą.

## <a name="shipping-container-receipts-list"></a>Gabenimo konteinerio gavimo kvitų sąrašas

Gabenimo konteinerio gavimo kvitų sąraše pateikiami visi negauti kiekiai, kurių terminas yra numatytą datą arba anksčiau. Sandėlio darbuotojai šią ataskaitą gali naudoti norėdami identifikuoti numatomas prekes gabenimo konteineryje. Ją taip pat galima naudoti prekėms, gautoms gabenimo konteineryje, tikrinti rankiniu būdu.

Norėdami sugeneruoti gabenimo konteinerio gavimo kvitų sąrašą, atlikite šiuos veiksmus.

1. Eikite į **Iškrovimo kaina \> Ataskaitos \> Sekimas \> Gabenimo konteinerio gavimo kvitų sąrašas**.
1. Dialogo lango **Gabenimo konteinerio gavimo kvitų sąrašas** lauke **Numatyta data** nurodykite datą. Visi kiekiai, kurie nebuvo gauti tą datą arba anksčiau, bus įtraukti į išvestį.
1. Skyriuje **Dimensijos** pasirinkite dimensijas, kurios bus įtrauktos į ataskaitą.
1. Kaip ir dirbdami su kitų tipų ataskaitomis „Supply Chain Management”, naudokite „FastTab” **Paskirties vieta**, norėdami pasirinkti ataskaitos išvesties formatą.
1. Kaip ir dirbdami su kitų tipų ataskaitomis „Supply Chain Management”, norėdami toliau riboti įrašus, kurie bus įtraukti į ataskaitą, naudokite „FastTab” **Įtrauktini įrašai**.
1. Pasirinkite **Gerai**, kad sugeneruotumėte šią ataskaitą.

## <a name="expected-delivery-report"></a>Numatomo pristatymo ataskaita

Numatomo pristatymo ataskaitoje yra pagrindinė informacija apie reisą, gabenimo konteinerį, sąskaitos lapą, prekes ir numatomą pristatymo datą.

Norėdami sugeneruoti numatomo pristatymo ataskaitą, atlikite šiuos veiksmus.

1. Eikite į **Iškrovimo kaina \> Ataskaitos \> Sekimas \> Numatomas pristatymas**.
1. Dialogo lango **Numatytas pristatymas** lauke **Numatyta data** pasirinkite datą, kada tikimasi prekių pristatymo į galutinį paskirties sandėlį. Į išvestį bus įtraukta bet kuri reiso eilutė, kurios numatoma data yra tą datą arba anksčiau, tačiau ji dar nėra gauta.
1. Pasirinktinai: lauke **Tiekėjo sąskaita** pasirinkite tiekėjo sąskaitą, norėdami įtraukti tik konkretaus tiekėjo pristatymus.
1. Skyriuje **Dimensijos** pasirinkite dimensijas, kurios bus įtrauktos į ataskaitą.
1. Kaip ir dirbdami su kitų tipų ataskaitomis „Supply Chain Management”, naudokite „FastTab” **Paskirties vieta**, norėdami pasirinkti ataskaitos išvesties formatą.
1. Kaip ir dirbdami su kitų tipų ataskaitomis „Supply Chain Management”, norėdami toliau riboti įrašus, kurie bus įtraukti į ataskaitą, naudokite „FastTab” **Įtrauktini įrašai**.
1. Pasirinkite **Gerai**, kad sugeneruotumėte šią ataskaitą.
