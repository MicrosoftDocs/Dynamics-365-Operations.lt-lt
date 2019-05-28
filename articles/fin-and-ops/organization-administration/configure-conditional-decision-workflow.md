---
title: Sąlyginių darbo eigos sprendimų konfigūravimas
description: Naudokite šią procedūrą, norėdami konfigūruoti sąlyginio sprendimo ypatybes.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a01290b3e2810aa1762f2230e8d01d219d6b10bf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554925"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a>Sąlyginių darbo eigos sprendimų konfigūravimas

[!include [banner](../includes/banner.md)]

Naudokite šią procedūrą, norėdami konfigūruoti sąlyginio sprendimo ypatybes.

Sąlyginis sprendimas – tai taškas, kuriame darbo eiga padalijama į dvi šakas. Norėdami darbo eigos rengyklėje konfigūruoti sąlyginį sprendimą, dešiniuoju pelės mygtuku spustelėkite sąlyginį sprendimą ir tada spustelėkite **Ypatybės**, kad atidarytumėte formą **Ypatybės**.

## <a name="name-a-decision"></a>Sprendimo pavadinimas

Norėdami įvesti sąlyginio sprendimo pavadinimą, atlikite šiuos veiksmus.

1. Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.
2. Lauke **Pavadinimas** įveskite unikalų sąlyginio sprendimo pavadinimą.

## <a name="set-conditions"></a> Sąlygų nustatymas

Patikrinusi pateiktą dokumentą sistema nustato, kurią šaką naudoti, ir nustato, ar ji atitinka konkrečias sąlygas.

1. Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.
2. Spustelėkite **Įtraukti sąlygą**.
3. Įveskite sąlygą
4. Įveskite papildomas sąlygas, jei jos reikalingos.
5. Norėdami patikrinti, kad sąlygos, kurias įvedėte yra sukonfigūruotos teisingai, atlikite tolesnius veiksmus.

    1. Spustelėkite **Tikrinti**, norėdami atidaryti formą **Tikrinti darbo eigos sąlygą**.
    2. Formos srityje **Tikrinti sąlygą** pasirinkite įrašą.
    3. Spustelėkite **Išbandyti**. Įvertinusi įrašą sistema nustatys, ar jis tenkina jūsų nurodytą sąlygą.
    4. Spustelėkite **Gerai** arba **Atšaukti**, norėdami vėl atidaryti formą **Ypatybės**.
