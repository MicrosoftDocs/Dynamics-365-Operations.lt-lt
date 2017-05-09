---
title: "Papildomas nusidėvėjimas"
description: "Šiame straipsnyje pateikta papildomo nusidėvėjimo funkcijos apžvalga."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: ca22ae7ba0f30085ad453e7b2c16418dba4dbbe9
ms.lasthandoff: 03/31/2017


---

# <a name="bonus-depreciation"></a>Papildomas nusidėvėjimas

[!include[banner](../includes/banner.md)]


Šiame straipsnyje pateikta papildomo nusidėvėjimo funkcijos apžvalga.

Naudodami papildomą nusidėvėjimą, pirmaisiais metais, kai turtas pradedamas eksploatuoti ir ima nusidėvėti, galite pridėti papildomų nusidėvėjimo sumų. Papildomas nusidėvėjimas turi būti visada apskaičiuojamas pirmiau nei visi kiti nusidėvėjimo skaičiavimai. Todėl geriausia kartu naudoti papildomą nusidėvėjimą ir knygas, kuriose išjungta funkcija Registruoti DK. Galite naudoti parinktį **Panaikinti operacijas, kurios neužregistruotos DK**, norėdami naikinti knygų praeities operacijas, kurios DK neregistruotos. Papildomą nusidėvėjimą galite vėliau nustatyti turto cikle, panaikindami anksčiau užregistruotas nusidėvėjimo operacijas. 

Papildomą nusidėvėjimą galite apskaičiuoti naudodami pasiūlymo procesą, arba galite sukurti neautomatines papildomo nusidėvėjimo operacijas. Negalima kurti papildomo nusidėvėjimo operacijų, jei toje turto nusidėvėjimo knygoje yra nusidėvėjimo operacijų arba koregavimo operacijų.

Kai skaičiuoti papildomam nusidėvėjimui naudojate pasiūlymo procesą, į pagrindo skaičiavimą įtraukiamos visos esamos papildomos operacijos. Skaičiavimas taip pat apima visus ankstesnius papildomus turto nusidėvėjimus, įvestus neautomatiniu būdu. 

Jei turtui bus taikomas daugiau nei vienas papildomas nusidėvėjimas, bus laikomasi prioritetų. Dėl kiekvieno papildomo nusidėvėjimo sumažėja kitas papildomas turto pagrindo nusidėvėjimas. Skaičiuojant papildomą nusidėvėjimą neatsižvelgiama į turto pagrindo likvidacinę vertę ir jam netaikoma nusidėvėjimo konvencija. 

Šiuo metu Jungtinėse Amerikos Valstijose tam tikra nuosavybė yra laikoma nuosavybe, patenkančia į 179 skyrių. Naudodami 179 skyriaus atskaitymą, iki tam tikros ribos galite atkurti visą tam tikrą nuosavybę arba jos dalį. Išlaidas galima susigrąžinti, jas išskaitant tais metais, kai nuosavybė pradedama eksploatuoti.

## <a name="example"></a>Pavyzdys
Toliau pateiktas papildomas nusidėvėjimas yra susijęs su turto knyga.

-   **179 skyrius:** 1 000,00, 1 prioritetas
-   **Laisvoji zona:** 30 proc., 2 prioritetas

Turto įsigijimo kaina yra 5 000,00. Kai skaičiuojamas papildomas nusidėvėjimas, pirmoji 179 nusidėvėjimo skyriaus papildomo nusidėvėjimo suma bus 1 000,00. 

Kita papildomo nusidėvėjimo suma pagal laisvosios zonos nusidėvėjimą skaičiuojama, kaip parodyta toliau. 

Įsigijimo išlaidos – 1 000 (179 skyriaus nusidėvėjimas) × 30 proc. = 1 200 

Jei papildomo nusidėvėjimo suma yra didesnė už likusias įsigijimo išlaidas, papildomo nusidėvėjimo suma bus laikomas arba apskaičiuotas papildomas nusidėvėjimas, arba likusios įsigijimo išlaidos, t. y. mažesnė suma. 

Jei likusios įsigijimo išlaidos yra 0 (nulis) arba mažesnės, papildomo nusidėvėjimo operacijos nebus generuojamos. 

Kai papildomas nusidėvėjimas skaičiuojamas naudojant pasiūlymo procesą, sukuriamos visų nusidėvėjimo įrašų, susijusių su turto knyga, papildomo nusidėvėjimo operacijos. 

Galite kurti neribotą papildomo nusidėvėjimo įrašų skaičių. Kai priskirsite tuos įrašus turto grupės knygai, jie bus taikomi turto knygoje. 

Papildomas nusidėvėjimas įvedamas arba procentais, arba fiksuota suma. Kai užregistruosite nusidėvėjimo pasiūlymus, knygoje papildomo nusidėvėjimo operacijos bus registruojamos atskirai nuo nusidėvėjimo operacijų.




