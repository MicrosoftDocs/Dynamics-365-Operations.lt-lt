---
title: Tarptautinio banko sąskaitos numerio (IBAN) sąskaitos tikrinimo valdymas
description: Šioje temoje paaiškinama, kaip valdyti tarptautinio banko sąskaitos numerio (IBAN) sąskaitos tikrinimą.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 28abef376e8462c9a69dbd8e5033ea799b6a4b3a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446009"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a>Tarptautinio banko sąskaitos numerio (IBAN) sąskaitos tikrinimo valdymas

[!include [banner](../includes/banner.md)]

Taikant tarptautinio banko sąskaitos numerio (IBAN) tikrinimą padaugėja tikrinimų, kurie yra atliekami, kai įtraukiate IBAN į banko sąskaitą.

Informacija apie IBAN struktūrą saugoma „Microsoft Dynamics 365 Finance“. Ši informacija automatiškai įkeliama pirmą kartą naudojantis IBAN banko sąskaitose. Ji apima IBAN ilgį, banko sąskaitos numerio ir įmonės registracijos numerio pradžios taškus, taip pat banko sąskaitos numerio ir įmonės registracijos numerio ilgį.

## <a name="set-up-iban-structures"></a>IBAN struktūrų nustatymas

1. Pasirinkite **Grynųjų pinigų ir banko valdymas \> Nustatymas \> IBAN struktūros**.
2. Atkreipkite dėmesį, kad kiekvienos šalies ar regiono IBAN struktūros nustatomos automatiškai.
3. Jei norite tinkinti konkrečios šalies ar regiono struktūras, galite jas redaguoti.
4. Struktūrų aprašai bus kiekvieno naujo leidimo dalis. Galite naudoti meniu **Struktūrų nustatymas iš naujo**, kad po kiekvieno atnaujinimo įkeltumėte naujausius aprašus.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Banko sąskaitos IBAN struktūros tikrinimas

1. Pasirinkite **Grynųjų pinigų ir banko valdymas \> Banko sąskaitos \> Banko sąskaitos**.
2. Sukurkite banko sąskaitą.
3. „FastTab“ skirtuke **Papildoma informacija** įveskite IBAN.

    Jei IBAN ilgis neatitinka nurodyto kiekvienai šaliai ar regionui būdingo ilgio, gausite įspėjamąjį pranešimą. Negalima tęsti, jei IBAN ilgis neatitinka IBAN struktūroje nurodyto ilgio.

    Tikrinimo metu taip pat patikrinama, ar banko sąskaitos numeris sutampa su IBAN dalimi, kuri nurodo banko sąskaitos numerį. Jei banko sąskaitos numeris nesutampa, gausite įspėjamąjį pranešimą. Šis pranešimas yra tik perspėjimas. Galite tęsti net jei banko sąskaitos numeris nesutampa.

    Tikrinimo metu taip pat patikrinama, ar banko įmonės registracijos numeris sutampa su ta IBAN dalimi, kurioje nurodomas banko įmonės registracijos numeris. Įmonės registracijos numeris apima banko numerį ir (dažnai) papildomą banko filialą. Jei banko įmonės registracijos numeris nesutampa, gausite įspėjamąjį pranešimą. Šis pranešimas yra tik perspėjimas. Galite tęsti net jei banko įmonės registracijos numeris nesutampa.
