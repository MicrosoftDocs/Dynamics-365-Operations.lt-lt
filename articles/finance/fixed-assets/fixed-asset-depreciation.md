---
title: Ilgalaikio turto nusidėvėjimas
description: Šiame straipsnyje pateikta ilgalaikio turto nusidėvėjimo apžvalga.
author: moaamer
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.form: AssetBonus, AssetBookTable
ms.openlocfilehash: 9761fc9846324d1c165274b72033e195bf4ea3e0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275302"
---
# <a name="fixed-asset-depreciation"></a>Ilgalaikio turto nusidėvėjimas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šiame straipsnyje pateikta ilgalaikio turto nusidėvėjimo apžvalga.

Nusidėvėjimas yra periodinė operacija, kuri paprastai balanso sąskaitoje sumažina ilgalaikio turto vertę. Ji pelno ir nuostolio sąskaitose užrašoma kaip išlaidos. Todėl pagrindinė sąskaita paprastai yra naudojama periodiniam nusidėvėjimui balanse kredituoti. Korespondentinė sąskaita yra sąskaitų plano pelno ir nuostolio dalies sąskaita.

Kaip ir versija 10.0.24, knygos puslapyje esanti pasirinktis **Skaičiuoti teigiamo nusidėvėjimo turto knygą leidžia nusidėvėjimui debetuoti ilgalaikį turtą,** **kuris** įsigytas su neigiama balansine verte (kreditu).

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

Norėdami gauti daugiau informacijos žr. [Nusidėvėjimo metodai ir konvencijos](depreciation-methods-conventions.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
