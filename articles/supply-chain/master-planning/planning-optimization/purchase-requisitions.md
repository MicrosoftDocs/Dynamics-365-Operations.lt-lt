---
title: Pirkimo paraiškos
description: Šiame straipsnyje aprašomos pirkimo paraiškos.
author: t-benebo
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: d9d55186307b18f4c3be78ae0828b08d3c987aad
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740690"
---
# <a name="purchase-requisitions"></a>Pirkimo paraiškos

[!include [banner](../../includes/banner.md)]

Bendrasis planavimas gali papildyti patvirtintas pirkimo paraiškas. Todėl norint padengti pirkimo paraiškas, vartotojams nereikia naudoti darbo eigos pirkimo užsakymų kūrimui. Vietoj to, pirkimo paraiškas gali atlikti bendrasis planavimas. Dėl šios funkcijos, pirkimo paraiška gali sukurti pirkimo, perkėlimo arba gamybos užsakymą, atsižvelgiant į **Suplanuoto užsakymo tipo** vertę, nustatytą susijusiam produktui.

## <a name="enable-master-plans-to-include-requisitions"></a>Bendrųjų planų įgalinimas paraiškoms įtraukti

Norėdami įtraukti paraiškas bendrojo plano padengimo skaičiavimo metu, atlikite šiuos veiksmus.

1. Eikite į **Bendrasis planavimas** \> **Sąranka** \> **Planai** \> **Bendrieji planai**.
1. Sukurkite arba pasirinkite bendrąjį planą.
1. „FastTab“ **Bendra** nustatykite parinktį **Įtraukti paraiškas** į *Taip*.
1. Pakartokite 2 ir 3 veiksmus kiekvienam papildomam bendrajam planui, į kurį norite įtraukti paraiškas.

## <a name="approved-requisitions-time-fence"></a>Patvirtintų paraiškų laiko riba

Skirtukas *Patvirtintų paraiškų laiko riba* nustato, kiek laiko (dienų) į bendrąjį planą bus įtrauktas patvirtintų papildymo paraiškų poreikis. Galite nustatyti patvirtintų paraiškų laiko ribas tiek padengimo grupės, tiek bendrojo plano lygiu.

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a>Patvirtintų paraiškų laiko ribos nustatymas padengimo grupei

1. Pasirinkite **Bendrasis planavimas** \> **Sąranka** \> **Padengimas** \> **Padengimo grupės**.
1. Kurkite arba pasirinkite padengimo grupę.
1. „FastTab” **Kita** nustatykite lauką **Patvirtintų paraiškų laiko riba (dienos)** į laiko ribą norimų įtraukti dienų skaičių.
1. Pakartokite 2 ir 3 veiksmus kiekvienai papildomai padengimo grupei, kuriai norite nustatyti patvirtintų paraiškų laiko ribas.

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a>Patvirtintų paraiškų laiko ribos nustatymas individualiems bendriesiems planams

Kai nustatote patvirtintų paraiškų laiko ribas individualiam bendrajam planui, parametras pakeičia laiko ribos parametrą bet kuriai taikytinai padengimo grupei.

1. Eikite į **Bendrasis planavimas** \> **Sąranka** \> **Planai** \> **Bendrieji planai**.
1. Sukurkite arba pasirinkite bendrąjį planą.
1. „FastTab” **Laiko ribos dienomis** nustatykite lauką **Patvirtintų paraiškų laiko riba (dienos)** į laiko ribą norimų įtraukti dienų skaičių.
1. Pakartokite 2 ir 3 veiksmus kiekvienam papildomam bendrajam planui, kuriam norite nustatyti patvirtintų paraiškų laiko ribas.

> [!IMPORTANT]
> Planavimo optimizavimas nepalaiko patvirtintų paraiškų laiko ribų. Kol jos taps palaikomos, nepaisoma visų lauke **Patvirtintų paraiškų laiko ribos (dienos)** įvedamų reikšmių.

## <a name="independent-supply-regardless-of-coverage-code"></a>Nepriklausomas tiekimas, nepaisant padengimo kodo

Pirkimo paraiškas visada padengia atskiri suplanuoti užsakymai, neatsižvelgiant į padengimo kodą. Taip užtikrinamas aiškus atsekamumas ir darbo eigos tarp pirkimo paraiškų ir papildymo užsakymų.

### <a name="example-1"></a>1 pavyzdys

Produktas nustatytas taip, kad jo **Padengimo kodo** vertė būtų *„Min/maks”*. Jis turi šias atsargų ir paraiškų būsenas:

- Turimų atsargų kiekis = 10.
- Mažiausias atsargų kiekis = 15.
- Didžiausias atsargų kiekis = 20.
- Yra vieno vieneto pirkimo paraiška. Jos pageidaujama data yra šiandien.

Kai vykdomas bendrasis planavimas, sukuriami du suplanuoti užsakymai: vienas – 10 vienetų papildyti atsargoms iki didžiausio kiekio, ir vienas – vienam vienetui papildyti pirkimo paraiškai.

### <a name="example-2"></a>2 pavyzdys

Produktas nustatytas taip, kad jo **Padengimo kodo** vertė būtų *„Min/maks”*. Jis turi šias atsargų ir paraiškų būsenas:

- Turimų atsargų kiekis = 17.
- Mažiausias atsargų kiekis = 15.
- Didžiausias atsargų kiekis = 20.
- Yra vieno vieneto pirkimo paraiška. Jos pageidaujama data yra šiandien.

Kai vykdomas bendrasis planavimas, sukuriamas vieno vieneto suplanuotas užsakymas papildyti pirkimo paraiškai.

### <a name="example-3"></a>3 pavyzdys

Produktas nustatytas taip, kad **Padengimo kodo** reikšmė yra *Laikotarpis,* o jo trukmė yra septynios dienos. Jo atsargų, pardavimo užsakymo ir paraiškos būsenos yra:

- Turimų atsargų kiekis = 0.
- Yra penkių vienetų pardavimo užsakymas. Jos numatoma siuntimo data yra šiandien ir dar viena diena.
- Yra trijų vienetų pirkimo paraiška. Jos pageidaujama data yra šiandien ir dar trys dienos.

Kai vykdomas bendrasis planavimas, sukuriami du suplanuoti užsakymai: vienas – trims vienetams papildyti pirkimo paraiškai ir vienas – penkiems vienetams papildyti pardavimo užsakymo poreikį.

> [!NOTE]
> Kai patvirtinamas suplanuotas užsakymas, iškviestas pirkimo paraiškai, planavimo modulis išlaiko iškvietimą į pirkimo paraišką. Jei patvirtintame užsakyme vėliau pritrūksta tam tikro kiekio, reikalingo pirkimo paraiškai įvykdyti, sistema sukurs naują suplanuotą užsakymą skirtumui padengti.

Daugiau informacijos apie pirkimo paraiškas žiūrėkite [Pirkimo paraiškos apžvalga](../../procurement/purchase-requisitions-overview.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]