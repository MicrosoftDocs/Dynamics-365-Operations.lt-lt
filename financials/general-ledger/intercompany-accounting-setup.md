---
title: "Vidinės įmonės ataskaitų nustatymas"
description: "Šioje temoje aiškinama, kaip nustatyti tvarkant vidinių įmonių apskaitą taip, kad galite naudoti žurnalų vidinės įmonės DK paskirstymuose ir finansinių žurnalų, pvz., kasdieninių žurnalų, tiekėjo SF žurnalas ir mokėjimų žurnalas."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5fd279327013f26230146be38e23e9955c6f12c7
ms.lasthandoff: 03/31/2017


---

# <a name="intercompany-accounting-setup"></a>Vidinės įmonės ataskaitų nustatymas

Šioje temoje aiškinama, kaip nustatyti tvarkant vidinių įmonių apskaitą taip, kad galite naudoti žurnalų vidinės įmonės DK paskirstymuose ir finansinių žurnalų, pvz., kasdieninių žurnalų, tiekėjo SF žurnalas ir mokėjimų žurnalas.

Vidinės įmonės žurnalai gali būti sukurta įvairiose situacijose, pavyzdžiui, kasdieninių žurnalų, tiekėjo SF žurnalais, DK paskirstymuose ir centralizuoti mokėjimai. Norėdami įgalinti šiuos scenarijus, turite nustatyti vidinės įmonės apskaitą.

## <a name="define-main-accounts"></a>Apibrėžti pagrindiniai apskaitos
Pirmiausia, turite sukurti vidinės įmonės pagrindines sąskaitas, kurios bus naudojamos apskaitos įrašams „Gavėjas“ ir „Mokėtojas“. Tikslinga kiekvienam įmonei naudoti unikalias pagrindines sąskaitas, kad būtų galima paprasčiau derinti ir šalinti vidinės įmonės apskaitos įrašus. Jei naudojate prekybos partneris ar kolega dimensijos nustatyti vidinės įmonės partijos, galite nustatyti šį aspektą kaip fiksuota dimensija pagrindinė sąskaita, kuri yra nurodyta tvarkant vidinių įmonių apskaitą. Nustatydami pagrindinės sąskaitos, jūs turėtumėte nustatyti į **pagrindinės sąskaitos tipas** lauko į **balanso** ant to **pagrindinės sąskaitos** puslapis.

## <a name="define-journal-names"></a>Apibrėžti pavadinimus
Tada turite nustatyti žurnalo pavadinimą. Nustatyti, **žurnalo tipą** lauko į **kasdien** ant, **žurnalų pavadinimai** puslapis. Tikslinga naudoti konkretų žurnalo pavadinimą vidinės įmonės apskaitai.

## <a name="define-intercompany-accounting-setup"></a>Nustatyti vidinės įmonės ataskaitų nustatymas
Į **tvarkant vidinių įmonių apskaitą** puslapyje yra naudojami sukurti poras juridinių asmenų, kurie gali sudaryti sandorius su kitu. Vidinės įmonės apskaitos nustatymas yra bendra, todėl konfigūracija yra matomas iš per visi juridiniai asmenys. Kurdami naują juridinį asmenį pora, užtikrinti tiksliai žinosite, koks juridinis subjektas yra apibrėžiamas kaip kilmės bendrovė ir paskirties įmonės. Į vidinės įmonės operacijas, sandoris nustato, koks juridinis subjektas yra pradedant ar kilmės operacija. Pvz., tvarkant vidinių įmonių apskaitą yra nustatyti USMF (kilmės) ir USSI (paskirties). Jeigu vartotojas yra aktyvus USSI ir įveda vidinės įmonės operacija su USMF, sandorio neregistruos nes tvarkant vidinių įmonių apskaitą apibrėžiama tik USMF yra iniciatorius. Jei bet kuri bendrovė gali būti sandoris, jums reikės kurti antrą juridinio asmens poros tarpusavio sąrankos. 

Pasirinkite į **debetuoja sąskaitą (sumokėti)** ir **kredito sąskaitos (turi)** tiek kilmės ir paskirties juridinio subjekto. Nustatyti, **žurnalo pavadinimas** bus naudojamas, kai sandoris yra sukurta įmonėje. Žurnalas už kilmės įmonės jau žinoma, nes jis yra pažymėtas vartotojas, kai sukuriamas vidinės įmonės operacijos. 

Galiausiai pasirinkite, koks juridinis subjektas gaus apskaitos paramos sumos, pvz., mokėjimo nuolaidos arba Realizuoto pelno/nuostolio centralizuoti mokėjimai. 

Tarpusavio santykius galima lengvai nustatyti dėl į **tvarkant vidinių įmonių apskaitą** puslapis naudojant į **sukurti tarpusavio santykių** mygtuką po pirmojo juridinio asmens pora yra sukurta. Sukūrus abipusę poros, informacijos paskirties įmonės kopijuojamas į kilmės įmonę ir atvirkščiai. Apibrėžtos paskirties įmonės žurnale lieka. Dauguma organizacijų naudokite vardų suteikimo konvencijos žurnalo pavadinimai, kad žurnalo pavadinimas yra toks pat. Jei žurnalo pavadinimai skiriasi, įspėjimas pasirodys pranešti jums, kad žurnalą neegzistuoja ir galima pasirinkti skirtingus žurnalo lauke.


