---
title: Atskaitymų konfigūravimas
description: Naudokite atskaitymus programoje „Microsoft Dynamics 365 Human Resources“, siekdami nustatyti, kiek (jei bus atskaitoma) atskaityti iš kiekvienos darbuotojui mokamos išmokos.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b4817cd6370166b6dfdf17b3d733b13374db8f49
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694913"
---
# <a name="configure-deductions"></a>Atskaitymų konfigūravimas


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Naudokite atskaitymus programoje „Microsoft Dynamics 365 Human Resources“, siekdami nustatyti, kiek (jei bus atskaitoma) atskaityti iš kiekvienos darbuotojui mokamos išmokos. Atskaitymai priklauso nuo datos, todėl galite turėti archyvinį atskaitymo informacijos įrašą. 

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Atskaitymai**.

2. Pasirinkite **Naujas**.

3. Nurodyti šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Atskaitymas** | Unikalus ID, naudojamas išmokos atskaitymui nustatyti. |
   | **Aprašymas** | Atskaitymo aprašas. |
   | **Galioja** | Pradžios data. Numatytoji vertė yra dabartinė sistemos data. |
   | **Galiojimo pabaiga** | Pabaigos datą. Numatytoji reikšmė yra 2154-12-31, kuri reiškia, kad niekada. |
   | **Antraštė** | Antraštės kodas iš algalapių sistemos, kurį šis atskaitymas naudos darbuotojo atskaitymo daliai, atliekant į algalapį įtraukiamų išmokų apdorojimą. Naudojamas, kai naudojate trečiosios šalies algalapio teikėją. |
   | **Darbuotojo algalapio atskaitymo rekomendacija** | Atskaitymo kodas iš algalapių sistemos, kurį šis atskaitymas naudos darbuotojo atskaitymo daliai, atliekant į algalapį įtraukiamų išmokų apdorojimą. |
   | **Sumos antraštė** | Antraštės kodas iš algalapių sistemos, kurį ši atskaitymo suma naudos darbuotojo atskaitymo daliai, atliekant į algalapį įtraukiamų išmokų apdorojimą. Paprastai naudojamas, kai naudojate trečiosios šalies algalapio teikėją. |
   | **Naikinti galima** | Nurodo, ar iš „Dynamics 365 for Finance and Operations“ eksportuota vertė gali panaikinti vertę algalapių sistemoje. |
   | **Suporuoti stulpeliai** | Nurodo, ar eksportuoti antraštės ir atskaitymo sumą, esančią susietuose gretimuose stulpeliuose, į algalapio sistemą. |
   | **Keitimo įsigaliojimo data** | Data, kai įsigalios išmokų atskaitymo pakeitimas. Šią dieną sistema automatiškai pakeičia išmokų atskaitymą ir atnaujina visus su šiuo atskaitymu susijusius išmokų planus, jei vykdysite **atskaitymo keitimo naujinimo** apdorojimą. |
   | **Atskaitymo pakeitimas atliktas** | Žymimasis langelis **Atskaitymo pakeitimas atliktas** bus pasirenkamas automatiškai, kai išmokų atskaitymo pakeitimai bus užbaigti apdorojus atskaitymo pakeitimo atnaujinimą. |
   
4. Norėdami sekti ir tvarkyti išmokų tarifo sąrankos keitimus, pasirinkite **Veiksmai**, tada pasirinkite **Tvarkyti versijas**.

5. Pasirinkite **Įrašyti**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
