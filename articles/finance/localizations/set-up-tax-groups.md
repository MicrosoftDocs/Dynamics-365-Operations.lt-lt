---
title: Mokesčių grupių nustatymas
description: Šiame straipsnyje paaiškinama, kaip nustatyti mokesčių grupes mokesčių skaičiavimo tarnybose.
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
ms.openlocfilehash: 89c5670ee7e78f2dc51f128c3ae8d284bb6b925b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862905"
---
# <a name="set-up-tax-groups"></a>Mokesčių grupių nustatymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti mokesčių grupes mokesčių skaičiavimo tarnybose. Taip pat paaiškinama, kaip nustatyti mokesčių grupės taikomumo taisyklės matricą ir konfigūruoti matricos eilutes.

Mokesčių grupių sąvoka mokesčių skaičiavimo paslaugoje yra panaši į Microsoft Dynamics PVM grupių 365 finansuose sąvoką. Tai mokesčių kodų grupės. Mokesčių skaičiavimo tarnyba mokesčių kodams nustatyti naudoja mokesčių grupės ir prekės mokesčių grupės sukirtimo grupę.

Tačiau mokesčių skaičiavimo tarnybos mokesčių grupės skiriasi nuo finansų PVM grupių, nes nėra papildomų jų parametrų, pvz., **Naudojimo mokestis** ir Neapmokestinamas **mokestis**. Vietoj to šie parametrai galimi mokesčių kodo lygyje.

> [!IMPORTANT]
> Mokesčių grupių nustatymas mokesčių skaičiavimo paslaugoje yra juridinis subjektas – agnostinis. Šį nustatymą reguliavimo konfigūracijos tarnybos (RCS) galite užbaigti tik vieną kartą. Kai įjungsite mokesčių skaičiavimo tarnybą finansuose, mokesčių grupės bus automatiškai sinchronizuojamos su pasirinktu juridiniu subjektu.

## <a name="set-up-a-tax-group"></a>Mokesčių grupės kūrimas

Norėdami nustatyti mokesčių grupę, atlikite šiuos veiksmus.

1. Prisijungti prie [reguliavimo konfigūracijos tarnybos](https://marketing.configure.global.dynamics.com/).
2. Eikite į **darbo sričių** \> **globalizavimo priemones Mokesčių** \> **skaičiavimas.**
3. Pasirinkite priemonę ir versiją, kurią norite nustatyti, tada pasirinkite **Redaguoti**.
4. Skirtuke **Bendra** pasirinkite Konfigūracijos **versija**.
5. Skirtuke **Mokesčių grupė** pasirinkite Tvarkyti **stulpelį**. Jei pirmą kartą nustatote mokesčių grupę, automatiškai nustatomi laukai, esantys **stulpelio** Valdyti dialogo lange.
6. Sąraše kairėje išplėskite mazgą **Eilutės** ir pažymėkite mokesčių grupės žymės **langelį**.

    ![Mokesčių grupė, pasirinkta eilučių mazge, dialogo lange Stulpelių valdymas.](media/select-tax-group.png)

7. Pasirinkite rodyklės dešinėn mygtuką, jei **norite pridėti mokesčių** grupę **į dešinėje pusėje esantį** pasirinktų stulpelių sąrašą.

    ![Mokesčių grupė įtraukta į pasirinktų stulpelių sąrašą.](media/add-tax-group.png)

8. Pasirinkite **Gerai**.

## <a name="configure-a-tax-group"></a>Mokesčių grupės konfigūravimas

Nustačius mokesčių grupę, sukuriama mokesčių grupės taikomumo taisyklės matrica. Norėdami konfigūruoti mokesčių grupę, prie matricos galite pridėti eilučių.

1. Skirtuke **Mokesčių grupė** pasirinkite **Įtraukti**.
2. **Į lauką** Mokesčių grupė įveskite mokesčių grupės pavadinimą.

    > [!IMPORTANT]
    > Rekomenduojame mokesčių grupės pavadinimą riboti iki 10 simbolių. Šis pavadinimas sinchronizuojamas su finansais, kurių PVM grupių pavadinimų riba – 10 simbolių.

3. Pvm kodų **lauke** pažymėkite kiekvieno mokesčio kodo, kurį norite įtraukti į mokesčių grupę, žymės langelį. Į vieną mokesčių grupę galite įtraukti keletą mokesčių kodų.

    ![Mokesčių kodų lauke pasirinkti keli mokesčių kodai.](media/multiple-tax-codes-selection.png)

4. Pakartokite 1–3 žingsnius, jei norite pridėti daugiau mokesčių grupių.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
