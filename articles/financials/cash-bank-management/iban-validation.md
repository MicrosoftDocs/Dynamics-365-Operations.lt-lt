---
title: "Tarptautinio banko sąskaitos numerio (IBAN) sąskaitos tikrinimo valdymas"
description: "Šioje temoje paaiškinama, kaip valdyti tarptautinio banko sąskaitos numerio (IBAN) sąskaitos tikrinimą."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: lt-lt
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a>Tarptautinio banko sąskaitos numerio (IBAN) sąskaitos tikrinimo valdymas

[!include [banner](../includes/banner.md)]

Taikant tarptautinio banko sąskaitos numerio (IBAN) sąskaitos tikrinimą padaugėja tikrinimų, kurie yra atliekami, kai įtraukiate IBAN į banko sąskaitą.

IBAN struktūra saugoma „Dynamics 365 for Finance and Operations“ ir įkeliama automatiškai, kai pirmą kartą naudojate IBAN banko sąskaitose. Banko sąskaitos numeris yra nurodytos IBAN numerio struktūros dalis. Priklausomai nuo tos struktūros, jei IBAN sąskaitos numerio vieta ir ilgis neatitinka vietos, nurodytos kiekvienos šalies ar regiono struktūroje, matysite perspėjimo pranešimus.

## <a name="set-up-iban-structures"></a>IBAN struktūrų nustatymas

1. Pasirinkite **Grynųjų pinigų ir banko valdymas \> Nustatymas \> IBAN struktūros**.
2. Atkreipkite dėmesį, kad kiekvienos šalies ar regiono IBAN struktūros nustatomos automatiškai.
3. Jei reikia tinkinti konkrečios šalies ar regiono struktūras, galite jas redaguoti.
4. Struktūrų aprašai bus kiekvieno naujo leidimo dalis. Galite naudoti meniu **Struktūrų nustatymas iš naujo**, kad po kiekvieno atnaujinimo įkeltumėte naujausius aprašus.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Banko sąskaitos IBAN struktūros tikrinimas

1. Pasirinkite **Grynųjų pinigų ir banko valdymas \> Banko sąskaitos \> Banko sąskaitos**.
2. Sukurkite banko sąskaitą.
3. „FastTab“ skirtuke **Papildoma informacija** įveskite IBAN.

    Jei IBAN sąskaitos numerio vieta ir ilgis neatitinka vietos, nurodytos kiekvienos šalies ar regiono struktūroje, matysite pranešimą. Negalima tęsti, jei IBAN ilgis neatitinka IBAN struktūros ilgio.

    Tikrinimo metu taip pat patikrinama, ar banko sąskaitos numeris sutampa su IBAN dalimi, kuri nurodo banko sąskaitos numerį. Jei banko sąskaitos numeris nesutampa, matysite perspėjimo pranešimą. Šis pranešimas yra tik perspėjimas. Galite tęsti net jei banko sąskaitos numeris nesutampa.

