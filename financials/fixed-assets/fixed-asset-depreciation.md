---
title: "Ilgalaikio turto nusidėvėjimas"
description: "Šiame straipsnyje apžvelgiamas ilgalaikio turto nusidėvėjimas."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a7f27847832e7c4814f1dc5982b6352c2ba98741
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017

---

# <a name="fixed-asset-depreciation"></a>Ilgalaikio turto nusidėvėjimas

[!include[banner](../includes/banner.md)]


Šiame straipsnyje apžvelgiamas ilgalaikio turto nusidėvėjimas.

Nusidėvėjimas yra periodinė operacija, kuri paprastai balanso sąskaitoje sumažina ilgalaikio turto vertę. Ji pelno ir nuostolio sąskaitose užrašoma kaip išlaidos. Todėl pagrindinė sąskaita paprastai yra naudojama periodiniam nusidėvėjimui balanse kredituoti. Korespondentinė sąskaita yra sąskaitų plano pelno ir nuostolio dalies sąskaita.

## <a name="depreciation-adjustment"></a>Nusidėvėjimo koregavimas
Paprastai užregistruotos nusidėvėjimo operacijos taisymas yra registruojamas kaip nusidėvėjimo koregavimas. Todėl pagrindinė sąskaita ir korespondentinė sąskaita yra nustatomos kaip nusidėvėjimo sąskaitos. Nusidėvėjimo koregavimas gali būti teigiama arba neigiama suma, bet pagrindinės sąskaitos (kaip balanso sąskaitos) ir korespondentinės sąskaitos (paprastai kaip pelno ir nuostolio sąskaitos) funkcija yra tokia pati.

## <a name="extraordinary-depreciation"></a>Visiškas nusidėvėjimas
Visiškas nusidėvėjimas veikia taip, kaip pagrindinis nusidėvėjimas. Todėl pagrindinė sąskaita yra naudojama nusidėvėjimo sumai balanse kredituoti ir ilgalaikio turto vertei sumažinti. Korespondentinė sąskaita yra pelno ir nuostolio sąskaita, kurioje apskaičiuotas ataskaitinio laikotarpio nusidėvėjimas nustatomas kaip išlaidos. 

Visiškas nusidėvėjimas veikia nepriklausomai nuo pagrindinio nusidėvėjimo. Jei visišką nusidėvėjimą naudosite kaip atskirą operacijos tipą, galėsite registruoti visišką nusidėvėjimą atskirai nuo pagrindinio nusidėvėjimo.

## <a name="special-depreciation-allowance"></a>Specialioji nusidėvėjimo nuolaida
Norėdami įtraukti visiško nusidėvėjimo sumas per pirmuosius metus, kai turtas atiduodamas eksploatuoti ir nusidėvi, galite naudoti specialiąją nusidėvėjimo nuolaidą. Specialiosios nusidėvėjimo nuolaidos turi būti visada apskaičiuojamos pirmiau nei visi kiti nusidėvėjimo skaičiavimai. Kadangi specialiosios nusidėvėjimo nuolaidos dažnai yra nežinomos, kol nepraeina tam tikras ilgalaikio turto dėvėjimo laikas, geriausia šį nusidėvėjimo tipą naudoti su knyga, kuri DK neregistruojama. Galite naudoti periodinę funkciją Panaikinti operacijas, kurios neužregistruotos DK, norėdami naikinti šių knygų praeities operacijas. Tada galite naikinti ilgalaikio turto knygos nusidėvėjimo retrospektyvą, registruoti specialiąją nusidėvėjimo nuolaidą, kai ji žinoma, ir tada registruoti likusias metų nusidėvėjimo operacijas. 

Galite kurti neribotą specialiosios nusidėvėjimo nuolaidos įrašų skaičių. Kai priskirsite tuos įrašus turto grupės knygai, jie bus taikomi turto knygoje. 

Specialioji nusidėvėjimo nuolaida įvedama procentais arba fiksuota suma. Kai užregistruosite nusidėvėjimo pasiūlymus, knygoje specialiosios nusidėvėjimo nuolaidos operacijos bus registruojamos atskirai nei nusidėvėjimo operacijos.

## <a name="depreciation-calendars"></a> Nusidėvėjimo kalendoriai
Kiekviena knyga turi kalendorių, kuris naudojamas nustatant ilgalaikio turto nusidėvėjimą. Pagal numatytuosius parametrus, jei nenurodote knygos kalendoriaus, knyga naudos DK finansinį kalendorių. Turite pasirinkti knygos finansinį kalendorių, kai susijusiame knygos nusidėvėjimo šablone yra naudojami finansiniai nusidėvėjimo metai. 

Bendrai naudojamus kalendorius galite kurti DK puslapyje **Finansiniai kalendoriai**.

Norėdami daugiau informacijos žr. [Nusidėvėjimo metodai ir konvencijos](depreciation-methods-conventions.md).




