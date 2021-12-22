---
title: Nustatyti prekių mokesčių grupes
description: Šioje temoje paaiškinama, kaip nustatyti prekės mokesčių grupes Mokesčių skaičiavimo tarnybose.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 88dd8e2fd9d4d4e5172dcc7b1bd27a70a2f59f03
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883909"
---
# <a name="set-up-item-tax-groups"></a>Nustatyti prekių mokesčių grupes

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti prekės mokesčių grupes Mokesčių skaičiavimo tarnybose. Taip pat paaiškinama, kaip nustatyti prekių mokesčių grupės taikomumo taisyklės matricą ir konfigūruoti matricos eilutes.

Prekių mokesčių grupių sąvoka mokesčių skaičiavimo tarnybose yra panaši į "Microsoft" prekių PVM grupių sąvoką Dynamics 365 Finance. Tai mokesčių kodų grupės. Mokesčių skaičiavimo tarnyba mokesčių kodams nustatyti naudoja mokesčių grupės ir prekės mokesčių grupės sukirtimo grupę.

> [!IMPORTANT]
> Prekių mokesčių grupių nustatymas mokesčių skaičiavimo paslaugoje yra juridinis subjektas – agnostinis. Šį nustatymą reguliavimo konfigūracijos tarnybos (RCS) galite užbaigti tik vieną kartą. Kai finansų tarnyba įgalinsite Mokesčių skaičiavimą, prekių mokesčių grupės bus automatiškai sinchronizuojamos su pasirinktu juridiniu subjektu.

## <a name="set-up-an-item-tax-group"></a>Prekės mokesčių grupės kūrimas 

Norėdami nustatyti prekės mokesčių grupę, atlikite šiuos veiksmus.

1. Prisijungti prie [reguliavimo konfigūracijos tarnybos](https://marketing.configure.global.dynamics.com/).
2. Eikite **į darbo sričių** \> **globalizavimo priemones Mokesčių** \> **skaičiavimas.**
3. Pasirinkite priemonę ir versiją, kurią norite nustatyti, tada pasirinkite **Redaguoti**.
4. Skirtuke **Bendra** pasirinkite Konfigūracijos **versija**.
5. Skirtuke **Prekių mokesčių grupė pasirinkite stulpelį** **Valdyti**. Jei prekės PVM grupę nustatote pirmą kartą, laukai, esantys stulpelio Valdyti **dialogo** lange, nustatomi automatiškai.
6. Sąraše kairėje išplėskite mazgą **Eilutės ir pažymėkite prekių mokesčių grupės žymės** **langelį**.

    ![Prekės mokesčių grupė, pasirinkta eilučių mazge, dialogo lange Stulpelių valdymas.](media/select-item-tax-group.png)

7. Pasirinkite rodyklės dešinėn **mygtuką, jei norite pridėti prekių** mokesčių **grupę į dešinėje pusėje esantį** pasirinktų stulpelių sąrašą.

    ![Prekės mokesčių grupė įtraukta į pasirinktų stulpelių sąrašą.](media/add-item-tax-group.png)

8. Pasirinkite **Gerai**.

## <a name="configure-an-item-tax-group"></a>Prekės mokesčių grupės konfigūravimas

Nustačius prekės mokesčių grupę, sukuriama pritaikymo taisyklės matrica. Norėdami konfigūruoti prekės mokesčių grupę, prie matricos galite pridėti eilučių.

1. Skirtuke **Prekių mokesčių grupė pasirinkite** **Įtraukti**.
2. Lauke **Prekių mokesčių** grupė įveskite prekių mokesčių grupės pavadinimą.

    > [!IMPORTANT]
    > Patariame prekių mokesčių grupės pavadinimą riboti iki 10 simbolių. Šis pavadinimas sinchronizuojamas su finansais, kurių prekių PVM grupių pavadinimų limitas yra 10 simbolių.

3. Pvm **kodų** lauke pažymėkite kiekvieno mokesčio kodo, kurį norite įtraukti į prekės mokesčių grupę, žymės langelį. Į vieną prekės mokesčių grupę galite įtraukti keletą mokesčių kodų.

    ![Mokesčių kodų lauke pasirinkti keli mokesčių kodai.](media/multiple-tax-codes-selection.png)

4. Norėdami pridėti daugiau prekės mokesčių grupių, pakartokite 1–3 žingsnius.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
