---
title: Nustatyti pažangų banko suderinimo importavimą naudojant elektronines ataskaitas
description: Šioje temoje paaiškinama, kaip naudoti elektronines ataskaitas norint nustatyti pažangų BAI2 išrašų banko suderinimo importavimo procesą.
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 39f1d8ba561ab0e36346f1dfb4f70df318c92a37
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544557"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Nustatyti pažangų banko suderinimo importavimą naudojant elektronines ataskaitas

[!include [banner](../includes/banner.md)]

Išplėstinės banko suderinimo priemonė leidžia importuoti elektroninius banko išrašus ir automatiškai suderinti juos Microsoft Dynamics su banko operacijomis,-365 finansuose. Šioje temoje paaiškinama, kaip nustatyti savo BAI2 banko išrašų importavimo funkcijas.

## <a name="set-up-the-electronic-reporting-configuration"></a>Elektroninių ataskaitų konfigūracijos parametrai

1. Eikite į **darbo sričių elektronines \> ataskaitas**.
2. "Microsoft" konfigūracijos teikėjo **išklotijoje** pasirinkite **Saugyklos**.
3. Pasirinkite **Visuotiniai ištekliai** ir pasirinkite **Atidaryti**.
4. Jei reikia užmegzti ryšį su saugykla, dialogo lange pasirinkite mėlyną saitą.
5. Konfigūracijos sąraše rasti BAI2 banko **išrašo \> modelio banko išrašo modelį**.
6. **Pasirinkti BAI2** formatą.
7. Skirtuke **Versijos** FastTab pasirinkite naujausią versiją, tada pasirinkite **Importuoti**.

## <a name="set-up-the-bank-statement-format"></a>Banko išrašo formato nustatymas

1. Eikite į **grynųjų pinigų ir banko valdymo \> nustatymą Išplėstinis \> banko suderinimo nustatymo banko išrašo \> formatas**.
2. Pasirinkite **Nauja**.
3. Nustatykite išrašo **formatą** ir **pavadinimo** laukus.
4. Pažymėkite žymės **langelį Bendrasis elektroninio importavimo** formatas.
5. Nustatyti importavimo **formato konfigūracijos** lauką **BAI2** formatu.

## <a name="set-up-the-bank-account"></a>Nustatyti banko sąskaitą

1. Pasirinkite **Grynųjų pinigų ir banko valdymas \> Banko sąskaitos \> Banko sąskaitos**.
2. Atidarykite banko sąskaitą.
3. Suderinimo "**FastTab**" nustatykite išplėstinio **banko suderinimo pasirinktį** kaip **Taip**.
4. Nustatyti anksčiau **sukurto** BAI2 **formato išrašo** formato lauką.

## <a name="import-the-bank-statement"></a>Importuoti banko išrašą

1. Eiti į grynųjų **pinigų ir banko valdymo banko išrašų \> suderinimo banko išrašus \>**.
2. Banko išrašų puslapio **viršuje pasirinkite** Importuoti **išrašą**.
3. Išraše **nustatykite** banko sąskaitos lauką kaip banko sąskaitą.
4. Nustatyti anksčiau **sukurto** BAI2 **formato išrašo** formato lauką.
5. Pasirinkite **Naršyti** ir pasirinkite **BAI** failą.
6. Pasirinkite **Nusiųsti**.
7. Pasirinkite **Gerai**, jei norite importuoti pasirinktą failą.
