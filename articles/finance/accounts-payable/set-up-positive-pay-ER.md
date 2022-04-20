---
title: Nustatyti ir sugeneruoti teigiamo mokėjimo failus naudojant elektronines ataskaitas
description: Šioje temoje paaiškinama, kaip nustatyti teigiamą užmokestį naudojant elektronines ataskaitas.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 43dd1a9cba1fe8df5cff26fe76af7e2957a0d6a4
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544553"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Nustatyti teigiamo mokėjimo failus naudojant elektroninę ataskaitą

Nustatykite teigiamą mokėjimą, jei norite generuoti bankui teikiamą elektroninį čekių sąrašą. Tada, kai čekis pateikiamas bankui, bankas jį lygina su čekių sąrašu. Jei čekis atitinka sąraše esantįjį, bankas jį patvirtina. Jei čekis sąraše esančio čekio neatitinka, bankas jį pasilieka peržiūrėti.

## <a name="set-up-the-electronic-reporting-configuration"></a>Elektroninių ataskaitų konfigūracijos parametrai

1. Eikite į **darbo sričių elektronines \> ataskaitas**.
2. "Microsoft" konfigūracijos teikėjo **išklotijoje** pasirinkite **Saugyklos**.
3. Pasirinkite **Visuotiniai ištekliai** ir pasirinkite **Atidaryti**.
4. Jei reikia užmegzti ryšį su saugykla, dialogo lange pasirinkite mėlyną saitą.
5. Konfigūracijos sąraše suraskite ir pasirinkite Teigiamo mokėjimo **modelio teigiamo \> mokėjimo formatą**.
6. Skirtuke **Versijos** FastTab pasirinkite naujausią versiją, tada pasirinkite **Importuoti**.

## <a name="set-up-a-positive-pay-format"></a>Teigiamo mokėjimo formato nustatymas

1. Eikite į **grynųjų pinigų ir banko valdymo nustatymo \> teigiamo \> mokėjimo formatus**.
2. Pasirinkite **Nauja**.
3. Nustatykite **mokėjimo formatą** ir **aprašymo** laukus.
4. Pažymėkite žymės **langelį Bendrasis elektroninis eksportavimo** formatas.
5. Nustatykite eksportavimo **formato konfigūracijos** lauką kaip **teigiamo mokėjimo formatą**.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Teigiamo mokėjimo formato priskyrimas banko sąskaitai

1. Eiti į grynųjų **pinigų ir banko valdymo \> banko sąskaitas \> Banko sąskaitos**.
2. Atidarykite banko sąskaitą.
3. Skirtuko Bendra **FastTab** lauke Teigiamo mokėjimo **formatas nustatykite** anksčiau sukurtą formatą.
4. Nustatykite **teigiamo mokėjimo pradžios datos** lauką į dabartinę datą.

## <a name="generate-a-positive-pay-file"></a>Generuoti teigiamų mokėjimų failą

1. Eiti į grynųjų **pinigų ir banko valdymo \> banko sąskaitų \> banko sąskaitas**.
2. Atidarykite banko sąskaitą, kurios teigiamas mokėjimas nustatytas.
3. Pasirinkite Tvarkyti **mokėjimus teigiamo mokėjimo \> teigiamo mokėjimo failą \>**.
4. Nustatykite **iškirptos datos lauką**. Čekiai, sugeneruoti prieš šią datą, bus įtraukti.

Gautas XML failas bus atsisiųstas.
