---
title: Tarptautinio banko sąskaitos numerio (IBAN) sąskaitos tikrinimo valdymas
description: Šiame straipsnyje paaiškinama, kaip valdyti tarptautinės banko sąskaitos numerio (IBAN) sąskaitos tikrinimą.
author: twheeloc
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 3d825e8699fbe10e080cd85f15d3d86f8c780f15
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880905"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a>Tarptautinio banko sąskaitos numerio (IBAN) sąskaitos tikrinimo valdymas

[!include [banner](../includes/banner.md)]

Taikant tarptautinio banko sąskaitos numerio (IBAN) tikrinimą padaugėja tikrinimų, kurie yra atliekami, kai įtraukiate IBAN į banko sąskaitą.

Informacija apie IBAN Microsoft Dynamics struktūrą saugoma 365 finansuose ir automatiškai įkeliama, kai pirmą kartą naudojate IBAN banko sąskaitose. Ji apima IBAN ilgį, banko sąskaitos numerio ir įmonės registracijos numerio pradžios taškus, taip pat banko sąskaitos numerio ir įmonės registracijos numerio ilgį.

## <a name="set-up-iban-structures"></a>IBAN struktūrų nustatymas

1. Pasirinkite **Grynųjų pinigų ir banko valdymas \> Nustatymas \> IBAN struktūros**.
2. Atkreipkite dėmesį, kad kiekvienos šalies ar regiono IBAN struktūros nustatomos automatiškai.
3. Jei struktūrą **reikia** atnaujinti pagal konkrečią šalį arba regioną, pasirinkite mygtuką Redaguoti.
4. Struktūrų aprašai bus kiekvieno naujo leidimo dalis. Galite naudoti meniu **Struktūrų nustatymas iš naujo**, kad po kiekvieno atnaujinimo įkeltumėte naujausius aprašus.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Banko sąskaitos IBAN struktūros tikrinimas

1. Pasirinkite **Grynųjų pinigų ir banko valdymas \> Banko sąskaitos \> Banko sąskaitos**.
2. Sukurkite banko sąskaitą.
3. „FastTab“ skirtuke **Papildoma informacija** įveskite IBAN.

    Jei IBAN ilgis neatitinka nurodyto kiekvienai šaliai ar regionui būdingo ilgio, gausite įspėjamąjį pranešimą. Negalima tęsti, jei IBAN ilgis neatitinka IBAN struktūroje nurodyto ilgio.

    Tikrinimo metu taip pat patikrinama, ar banko sąskaitos numeris sutampa su IBAN dalimi, kuri nurodo banko sąskaitos numerį. Jei banko sąskaitos numeris nesutampa, gausite įspėjamąjį pranešimą. Šis pranešimas yra tik perspėjimas. Galite tęsti net jei banko sąskaitos numeris nesutampa.

    Tikrinimo metu taip pat patikrinama, ar banko įmonės registracijos numeris sutampa su ta IBAN dalimi, kurioje nurodomas banko įmonės registracijos numeris. Įmonės registracijos numeris apima banko numerį ir (dažnai) papildomą banko filialą. Jei banko įmonės registracijos numeris nesutampa, gausite įspėjamąjį pranešimą. Šis pranešimas yra tik perspėjimas. Galite tęsti net jei banko įmonės registracijos numeris nesutampa.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
