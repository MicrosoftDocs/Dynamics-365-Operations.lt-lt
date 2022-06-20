---
title: Atidėto mokesčių skaičiavimo įjungimas žurnaluose
description: Šiame straipsnyje paaiškinama, kaip įjungti funkciją Atidėtas mokesčių skaičiavimas, kad būtų pagerintas mokesčių skaičiavimų našumas, kai žurnalo eilučių skaičius labai didelis.
author: EricWang
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 02a038318d4c0fb44b6fcc4bb159ea87c2e9368a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887925"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a>Atidėto mokesčių skaičiavimo įjungimas žurnaluose
[!include [banner](../includes/banner.md)]


Šiame straipsnyje paaiškinama, kaip atidėti PVM skaičiavimą žurnaluose. Ši galimybė padeda pagerinti mokesčių skaičiavimo efektyvumą, kai yra daug žurnalo eilučių.

Esant numatytiesiems nustatymams, žurnalo eilučių PVM sumos apskaičiuojamos, kai atnaujinami su mokesčiais susiję laukai. Šie laukai apima PVM grupių ir prekės PVM grupių laukus. Atnaujinus bet kurią žurnalo eilutę, perskaičiuojamos visos žurnalo eilutės. Nors toks veikimas leidžia vartotojui matyti realiu laiku apskaičiuojamas mokesčių sumas, tai taip pat gali turėti įtakos našumui, jei žurnalo eilučių skaičius yra labai didelis.

Atidėto mokesčių skaičiavimo funkcija leidžia atidėti mokesčių skaičiavimą žurnaluose, todėl padeda spręsti našumo problemas. Kai ši funkcija įjungta, mokesčių sumos bus apskaičiuotos tik tada, kai vartotojas pasirinks **PVM** arba užregistruos žurnalą.

Galite atidėti PVM skaičiavimą trijuose lygiuose:

- Juridinis subjektas
- Žurnalo pavadinimas
- Žurnalo antraštė

Sistema teikia prioritetą žurnalo antraštės parametrui. Esant numatytiesiems parametrams, šis parametras gaunamas iš žurnalo pavadinimo. Esant numatytiesiems parametrams, žurnalo pavadinimas gaunamas iš puslapio **DK parametrai**, kai sukuriamas žurnalo pavadinimas. Tolesniuose skyriuose paaiškinama, kaip įjungti atidėtą mokesčių skaičiavimą juridiniams subjektams, žurnalų pavadinimams ir žurnalų antraštėms.

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a>Atidėto mokesčių skaičiavimo įjungimas juridinio subjekto lygyje

1. Eikite į **Didžioji knyga \> Didžiosios knygos nustatymas \> DK parametrai**.
2. Skirtuke **PVM**, „FastTab“ **Bendra**, nustatykite parinkties **Uždelstas mokesčių skaičiavimas** reikšmę **Taip**.

![Didžiosios knygos parametrų vaizdas.](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a>Atidėto mokesčių skaičiavimo įjungimas žurnalo pavadinimo lygyje

1. Eikite į **Didžioji knyga \> Žurnalo nustatymas \> Žurnalo pavadinimai**.
2. „FastTab“ **Bendra**, dalyje **PVM**, nustatykite parinkties **Uždelstas mokesčių skaičiavimas** reikšmę **Taip**.

![Žurnalų pavadinimų vaizdas.](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a>Atidėto mokesčių skaičiavimo įjungimas žurnalo antraštės lygyje

1. Eikite į **Didžioji knyga \> Žurnalų įrašai \> Bendrieji žurnalai**.
2. Pasirinkite **Naujas**.
3. Pasirinkite žurnalo pavadinimą.
4. Skirtuke **Sąranka** nustatykite parinkties **Uždelstas mokesčių skaičiavimas** reikšmę **Taip**.

![Bendrojo žurnalo puslapio vaizdas.](media/delayed-tax-calculation-journal-header.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
