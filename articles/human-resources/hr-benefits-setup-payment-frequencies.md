---
title: Mokėjimo dažnumo nustatymas
description: „Microsoft Dynamics 365 Human Resources“ naudoja mokėjimų dažnumą, kad apskaičiuotų metinį išmokų atlyginimą, nustatytų draudimo įnašo sumą, kurią darbuotojas moka kiekvieną laikotarpį ir nustatytų, kaip dažnai mokama teikėjams.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7d86ab4956bc61209054c813cd8def69ca1bff58
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052054"
---
# <a name="set-up-payment-frequencies"></a>Mokėjimo dažnumo nustatymas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

„Microsoft Dynamics 365 Human Resources“ naudoja mokėjimų dažnumą, kad apskaičiuotų metinį išmokų atlyginimą, nustatytų draudimo įnašo sumą, kurią darbuotojas moka kiekvieną laikotarpį ir nustatytų, kaip dažnai mokama teikėjams.

Išmokų mokėjimo dažnumai naudoja konvertavimo koeficientus, kad būtų galima konvertuoti išmokų mokėjimo laikotarpius naudojant mėnesio, pusės mėnesio, dviejų savaičių, savaitės ir dienos mokėjimo dažnumus. Tai leidžia įmonėms apibrėžti tarpusavio priklausomybę tarp išmokų plano mokėjimo dažnumų.

Konvertavimo koeficientų laukuose nustatomas konvertavimo iš mokėjimo dažnumo į standartinius mokėjimo laikotarpius koeficientas ir leidžiama sistemai apskaičiuoti mokėjimo dažnumus. Konvertavimo koeficiento suma taip pat nustato draudimo įmokų sumą, kurią darbuotojas turėtų mokėti per kiekvieną mokėjimo dažnumą.

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Mokėjimo dažnumai**.

2. Pasirinkite **Naujas**.

3. Nurodyti šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Mokėjimo dažnumas** | Unikalus mokėjimo dažnumo pavadinimas. |
   | **Aprašymas** | Mokėjimo dažnumo aprašymas. |
   | **Laikotarpis** | Atitinkamas laikotarpis, kuris geriausiai atitinka išmokų teikėjo ir darbuotojo mokėjimo dažnumą. Laikotarpių sąrašas sudaromas iš standartinių mokėjimo laikotarpių. |
   | **Mokėjimo laikotarpių skaičius** | Mokėjimo laikotarpių skaičius, nurodantis, kaip dažnai mokama išmokų teikėjui arba darbuotojams. Ši suma bus naudojama apskaičiuojant darbuotojo metinę išmokų atlyginimo sumą. |
   | **Metinis konvertavimo koeficientas** | Metinis mokėjimo dažnumo konvertavimo koeficientas. Pavyzdžiui, metinis mėnesinio mokėjimo dažnumo konvertavimo koeficientas yra: </br></br>(12 mėnesinių mokėjimų / 1 metai) = 12 |
   | **Kas pusmetinis konvertavimo koeficientas** | Mokėjimo dažnumo kaspusmetinis konvertavimo koeficientas. Pavyzdžiui, mėnesinio mokėjimo dažnumo kaspusmetinis konvertavimo koeficientas yra: </br></br>(12 mėnesinių mokėjimų / 2 kartai per metus) = 6 |
   | **Ketvirčio konvertavimo koeficientas** | Mokėjimo dažnumo ketvirčio konvertavimo koeficientas. Pavyzdžiui, mėnesinio mokėjimo dažnumo ketvirčio konvertavimo koeficientas yra: </br></br>(12 mėnesinių mokėjimų / 4 ketvirčiai) = 3 |
   | **Mėnesis konvertavimo koeficientas** | Mėnesinis mokėjimo dažnumo konvertavimo koeficientas. Pavyzdžiui, mėnesinio mokėjimo dažnumo mėnesinis konvertavimo koeficientas yra: </br></br>(12 mėnesinių mokėjimų / 12 mėnesių) = 1 |
   | **Pusės mėnesio konvertavimo koeficientas** | Mokėjimo dažnumo pusės mėnesio konvertavimo koeficientas. Pavyzdžiui, mėnesinio mokėjimo dažnumo pusės mėnesio konvertavimo koeficientas yra: </br></br>(12 mėnesinių mokėjimų / 24 (2 k. per mėnesį)) = 0,5 | 
   | **Kas dvi savaites konvertavimo koeficientas** | Metinis mokėjimo dažnumo konvertavimo koeficientas. Pavyzdžiui, metinis mėnesinio mokėjimo dažnumo konvertavimo koeficientas yra: </br></br>(12 mėnesinių mokėjimų / 26 savaitės) = 0,461538 |
   | **Savaitinis konvertavimo koeficientas** | Metinis mokėjimo dažnumo konvertavimo koeficientas. Pavyzdžiui, metinis mėnesinio mokėjimo dažnumo konvertavimo koeficientas yra: </br></br>(12 mėnesinių mokėjimų / 52 savaitės) = 0,230769 |
   | **Dieninis konvertavimo koeficientas** | Metinis mokėjimo dažnumo konvertavimo koeficientas. Pavyzdžiui, metinis mėnesinio mokėjimo dažnumo konvertavimo koeficientas yra: </br></br>(12 mėnesinių mokėjimų / 365 dienos) = 0,032877 |
   | **Valandinis konvertavimo koeficientas** | Metinis mokėjimo dažnumo konvertavimo koeficientas. Pavyzdžiui, metinis mėnesinio mokėjimo dažnumo konvertavimo koeficientas yra: </br></br>(12 mėnesinių mokėjimų / 2080 valandos) = 0,005769

4. Pasirinkite **Įrašyti**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]