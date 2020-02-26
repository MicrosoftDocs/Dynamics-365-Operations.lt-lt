---
title: Atskaitymų konfigūravimas
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7ee9e8f3bc0e9027e41d3aa91bd097a3f046cbb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009960"
---
# <a name="configure-deductions"></a>Atskaitymų konfigūravimas

[!include [banner](includes/preview-feature.md)]

Naudokite atskaitymus programoje „Microsoft Dynamics 365 Human Resources“, siekdami nustatyti, kiek (jei bus atskaitoma) atskaityti iš kiekvienos darbuotojui mokamos išmokos. Atskaitymai priklauso nuo datos, todėl galite turėti archyvinį atskaitymo informacijos įrašą. 

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Atskaitymai**.

2. Pasirinkite **Naujas**.

3. Nurodyti šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | Atskaitymas | Unikalus ID, naudojamas išmokos atskaitymui nustatyti. |
   | Aprašymas | Atskaitymo aprašas. |
   | Galioja | Pradžios data. Numatytoji vertė yra dabartinė sistemos data. |
   | Galiojimo pabaiga | Pabaigos datą. Numatytoji reikšmė yra 2154-12-31, kuri reiškia, kad niekada. |
   | Antraštė | Antraštės kodas iš algalapių sistemos, kurį šis atskaitymas naudos darbuotojo atskaitymo daliai, atliekant į algalapį įtraukiamų išmokų apdorojimą. Naudojamas, kai naudojate trečiosios šalies algalapio teikėją. |
   | Darbuotojo algalapio atskaitymo rekomendacija | Atskaitymo kodas iš algalapių sistemos, kurį šis atskaitymas naudos darbuotojo atskaitymo daliai, atliekant į algalapį įtraukiamų išmokų apdorojimą. |
   | Sumos antraštė | Antraštės kodas iš algalapių sistemos, kurį ši atskaitymo suma naudos darbuotojo atskaitymo daliai, atliekant į algalapį įtraukiamų išmokų apdorojimą. Paprastai naudojamas, kai naudojate trečiosios šalies algalapio teikėją. |
   | Naikinti galima | Nurodo, ar iš „Dynamics 365 for Finance and Operations“ eksportuota vertė gali panaikinti vertę algalapių sistemoje. |
   | Suporuoti stulpeliai | Nurodo, ar eksportuoti antraštės ir atskaitymo sumą, esančią susietuose gretimuose stulpeliuose, į algalapio sistemą. |
   | Keitimo įsigaliojimo data | Data, kai įsigalios išmokų atskaitymo pakeitimas. Šią dieną sistema automatiškai pakeis išmokų atskaitymą ir atnaujins visus su šiuo atskaitymu susijusius išmokų planus, jei vykdysite atskaitymo keitimo naujinimo apdorojimą. |
   | Atskaitymo pakeitimas atliktas | Žymimasis langelis „Atskaitymo pakeitimas atliktas” bus pasirenkamas automatiškai, kai išmokų atskaitymo pakeitimai bus užbaigti apdorojus atskaitymo pakeitimo atnaujinimą. |
   
4. Norėdami sekti ir tvarkyti išmokų tarifo sąrankos keitimus, pasirinkite **Veiksmai**, tada pasirinkite **Tvarkyti versijas**.

5. Pasirinkite **Įrašyti**. 
