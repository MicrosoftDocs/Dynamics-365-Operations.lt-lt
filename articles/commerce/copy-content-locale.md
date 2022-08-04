---
title: Kopijuoti turinį į kitą vietą
description: Šiame straipsnyje aprašoma, kaip kopijuoti esamą turinį į kitą svetainės generatoriaus Microsoft Dynamics 365 Commerce svetainės vietą.
author: psimolin
ms.date: 07/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: bcfa3c7cb2ea8018422803d85df6b6761b8d1145
ms.sourcegitcommit: d719d0a549aecac231fad0abb42250eab9dd0ded
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/07/2022
ms.locfileid: "9126470"
---
# <a name="copy-content-to-another-locale"></a>Kopijuoti turinį į kitą vietą

[!include[banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip kopijuoti esamą turinį į kitą svetainės generatoriaus Microsoft Dynamics 365 Commerce svetainės vietą.

Kuriant turinį "Commerce" svetainės generatoriuje, jis visada siejamas su vietos identifikatoriumi, pvz., "en-us". Galite kopijuoti atskirus puslapius ir turtą į kitą tos pačios el. komercijos svetainės vietą, perjungdami lokalę, kai redaguojate turinio elementą ir tada sukuriate naują prekės variantą. Kai kuriais atvejais, pavyzdžiui, visiškai naują lokalę jūsų parduotuvės pirmame kompiuteryje paleidžiate, yra logiška dubliuoti visus esamos vietos turinio elementus į naują lokalę. Jei naujos vietos pagrindinė kalba yra tokia pati kaip vienos iš esamų lokalių, galite naudoti esamą lokalę kaip vietos kopijavimo operacijos šaltinio lokalę. (Pvz., "en-us" ir "en-au" lokalės naudoja anglų kalbą.) Tokiu būdu padedate sumažinti pastangas, reikalingų naujos vietos turiniui lokalizuoti.

Šiose procedūrose paaiškinama, kaip į esamą kanalą įtraukti naują lokalę, kopijuoti visus turinio elementus iš esamos vietos į naują lokalę ir stebėti vietos kopijavimo operacijos būseną.

## <a name="add-a-new-locale"></a>Įtraukti naują lokalę

Norėdami įtraukti naują vietą į "Commerce" svetainių generatorių, atlikite šiuos veiksmus.

1. Svetainės generatoriuje eikite į savo svetainę.
1. Kairiajame naršymo lange pasirinkite Svetainės **parametrai** ir pasirinkite **Kanalai**.
1. Dalyje **Kanalas** pasirinkite kanalą, į kurį norite įtraukti naują lokalę.
1. Kanalo dialogo lange, kuris rodomas dešinėje, pasirinkite **Įtraukti lokalę**.
1. Dialogo lango **Įtraukti lokalę** lauke **Lokalė, kad būtų galima** palaikyti, pasirinkite lokalę.
1. Patvirtinkite, kad **domeno** reikšmė teisinga.
1. Įveskite **unikalų** URL maršrutą (pvz., **en-us arba anglų** **kalba**).
1. Pasirinkite **Gerai**.
1. Uždarykite kanalo dialogo langą.
1. Dalyje **Kanalas** patvirtinkite, kad nauja lokalė pateikta šalia tinkamo kanalo.
1. Pasirinkite **įrašyti ir publikuoti**.

> [!NOTE]
> Kad būtų galima konfigūruoti naują vietą svetainės generatoriuje, ji turi būti pridėta prie susieto interneto parduotuvės kanalo, kuris yra "Commerce Headquarters".

## <a name="copy-all-content-items-to-a-new-locale"></a>Kopijuoti visus turinio elementus į naują lokalę

Norėdami kopijuoti visus turinio elementus į naują "Commerce Site Builder" vietą, atlikite šiuos veiksmus.

1. Svetainės generatoriuje eikite į savo svetainę.
1. Kairiajame naršymo lange pasirinkite Svetainės **parametrai** ir pasirinkite **Kanalai**.
1. Komandų juostoje pasirinkite Kurti **vietos kopiją**.
1. Dialogo lange **Kurti lokalę,** kuris rodomas dešinėje pusėje, dalyje Šaltinio **svetainė** patvirtinkite, kad pasirinkta teisinga svetainė.
1. **Lauke Šaltinio kanalas** pasirinkite šaltinio kanalą.
1. Paskirties kanalo **lauke pasirinkite** tą patį šaltinio kanalą.
1. **Lauke Šaltinio lokalė** pasirinkite šaltinio lokalę.
1. **Lauke Paskirties vieta pasirinkite** naują vietą.
1. Pasirinkite **Kopijuoti lokalę**. Pranešimas patvirtina, kad vietos kopijavimo operacija pradėta.

> [!NOTE]
> Taip pat galite kopijuoti turinį skirtinguose kanaluose.

## <a name="monitor-the-status-of-the-locale-copy"></a>Stebėti vietos kopijos būseną

Norėdami stebėti vietos kopijavimo operacijos būseną, atlikite šiuos veiksmus.

1. Svetainės generatoriuje eikite į savo svetainę.
1. Kairiajame naršymo lange pasirinkite Svetainės **parametrai** ir pasirinkite **Užduotys**.
1. Dabartinių **užduočių** dalyje pasirinkite norimą stebėti užduotį. Užduoties informacija rodoma dešinėje pusėje atsirandaiame dialogo lange.
