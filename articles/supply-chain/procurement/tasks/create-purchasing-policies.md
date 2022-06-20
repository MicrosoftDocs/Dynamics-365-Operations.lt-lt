---
title: Pirkimo strategijų kūrimas
description: Šiame straipsnyje aprašoma, kaip sukurti pirkimo strategijas, siekiant suderinti su pirkimo verslo procesais.
author: GalynaFedorova
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 011705723466d746fa5b23c5499d03a548f133f1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878851"
---
# <a name="create-purchasing-policies"></a>Pirkimo strategijų kūrimas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip sukurti pirkimo strategijas, siekiant suderinti su pirkimo verslo procesais. Prieš kurdami pirkimo strategijas turite nustatyti pirkimo strategijos parametrus. Galima kurti, modifikuoti ir nurašyti pirkimo strategiją, bet pirkimo strategijos negalima naikinti. Šią procedūrą paprastai atlieka pirkimo vadovas. Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis.


## <a name="set-up-policy-parameters"></a>Strategijos parametrų nustatymas
1. Naršymo srityje pasirinkite **Moduliai > Įsigijimas ir šaltinio pasirinkimas > Sąranka > Strategijos > Pirkimo strategijos**.
2. Veiksmų srityje pasirinkite **Parametrai**.
- Strategijos pirmumo taisyklės taikomos skirtingiems jūsų organizacijos lygiams. Rodomi organizacijos vienetai priklauso nuo jūsų organizacijos hierarchijos ir nuo to, kuriems hierarchijos lygiams priskirta paskirtis Įsigijimo vidinė kontrolė. Pvz., organizacijoje gali būti juridiniai subjektai, išlaidų centrai, regionai ir padaliniai, bet galbūt tik kai kuriems iš jų priskirta hierarchijos paskirtis Įsigijimo vidinė kontrolė. Pagal numatytuosius parametrus galimas organizacijos tipas Įmonė.  
3. Pasirinkite skirtuką **Strategijos taisyklės tipo parametrai**.
4. Medyje pasirinkite **Pirkimo strategija > Pirkimo paraiškos kontrolės taisyklė**.
- Strategijos taikymo pirmumo tvarką galite nurodyti strategijos lygiu. Tačiau naudodami kai kurių tipų strategijas galite nepaisyti atskirų tipų strategijos taisyklių pirmumo tvarkos. Pvz., galite nustatyto tokią pirkimo strategijų pirmumo tvarką: išlaidų centras, padalinys, įmonė. Taikydami katalogo strategijos taisyklę galite nustatyti tokią pirmumo tvarką: padalinys, išlaidų centras, įmonė. Galite pakeisti katalogo strategijos taisyklės pirmumo tvarką. Kai darbuotojas sukuria paraišką, rodomas katalogas priklauso nuo strategijų, susijusių su darbuotojo padaliniu, tada – su jo išlaidų centru ir su įmone.  
- Jei nurodytas daugiau nei vienas organizacinis lygis, galite naudoti rodyklę Aukštyn / Žemyn, kad nustatytumėte taisyklės Pirkimo paraiškos kontrolė pirmumo tvarką.  
5. Uždarykite puslapį.

## <a name="create-a-new-policy"></a>Kurti naują strategiją
1. Pasirinkite **Naujas**.
2. Lauke **Pavadinimas** įveskite reikšmę.
3. Lauke **Aprašas** įveskite reikšmę.
- Viena pirkimo strategija gali būti taikoma tik vienai organizacijos hierarchijai. Pvz., viena hierarchija vadinasi „Geografinė“, o kita – „Padalinys“, o joms priskirtos pirkimo strategijos skiriasi.  
- Pasirinkite organizaciją, kuriai turėtų būti taikoma strategija.  
4. Norėdami įtraukti pasirinktą organizaciją, spustelėkite rodyklę.
- Galite pakartoti šį procesą, norėdami įtraukti daugiau organizacijų.  

## <a name="add-a-policy-rule"></a>Įtraukti strategijos taisyklę
1. Sąraše **Strategijos taisyklės tipas** pasirinkite **Paraiškos paskirties taisyklė**.
- Sukursite taisyklę, kuri numatytąją paraiškos paskirtį nustato į tipą Suvartojimas, bet suteikia galimybę jį pakeisti į tipą Papildymas.  
2. Pasirinkite **Kurti strategijos taisyklę**.
3. Lauke **Leisti neautomatiškai perrašyti** pasirinkite **Taip**.
4. Pasirinkite **Uždaryti**.
- Dabar galite nustatyti kitas pirkimo strategijos taisykles. Atkreipkite dėmesį, tipe Strategijos taisyklė negali būti persidengiančių taisyklių, kurios vienu metu yra aktyvios vienoje įsigijimo strategijoje.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]