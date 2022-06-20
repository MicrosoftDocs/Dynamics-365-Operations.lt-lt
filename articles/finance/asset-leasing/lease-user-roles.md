---
title: Vartotojo vaidmenų nuomos priskyrimas
description: Šiame straipsnyje aprašomi saugos vaidmenys, naudojami turto pereije. Jis taip pat paaiškina, kaip priskirti vartotojus šiems vaidmenims.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 38c859d64742d582d0709506d83600ea26a21147
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878137"
---
# <a name="assign-lease-user-roles"></a>Vartotojo vaidmenų nuomos priskyrimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomi saugos vaidmenys, naudojami turto pereije. Jis taip pat paaiškina, kaip priskirti vartotojus šiems vaidmenims.

Trys vartotojo vaidmenys atskiria prieigą turto nuomoje. Vienas vaidmuo yra tinkamas išnuomoti nuomos sutartis, jis tinkamas peržiūrėti nuomos sutartis, o vienas yra tinkamas nuomos sekretoriaus pareigoms atlikti. Kiekvienas vaidmuo turi konkrečias visų nuomos puslapių teises ir leidžia vartotojams peržiūrėti, kurti, redaguoti arba naikinti nuomos sutartis pagal savo pareigas.

| Vaidmuo           | aprašymas |
|----------------|-------------|
| Nuomos valdymas | Šio vaidmens vartotojai gali pridėti, redaguoti, naikinti ir peržiūrėti nuomos sutartis. Šis vaidmuo yra skirtas kasdieniam vartotojui, kurio užduotys apima mėnesio žurnalų įrašų kūrimą ir registravimą bei naujos nuomos įtraukimą. Šis vaidmuo suteikia prieigą prie visų turto išperkamosios nuomos funkcinių galimybių. |
| Nuomos peržiūra     | Šio vaidmens vartotojai gali peržiūrėti tik nuomos įrašus, grafikus ir vykdyti ataskaitas. Jie negali sukurti naujos nuomos, redaguoti esamos nuomos arba kurti žurnalo įrašus pagal nuomos sutartis. Šis vaidmuo yra skirtas vartotojams, kurie tereikia Peržiūrėti nuomos sutartis, nuomos grafikus ir operacijas, kurios vyksta prieš šias nuomos sutartis. |
| Nuomos klerkas    | Šio vaidmens vartotojai gali kurti tik naujas nuomos sutartis. Jie negali redaguoti arba naikinti esamos nuomos, peržiūrėti išperkamosios nuomos tvarkaraščius arba registruoti lizingo žurnalų įrašus. Šis vaidmuo yra skirtas vartotojams, kurie dirba duomenų įvedimo pajėgumui. |

Atlikite šiuos veiksmus, norėdami vartotojus priskirti vaidmenims, naudojamiems turto lizingui.

1. Eikite į **Sistemos administravimas \> Sauga \> Priskirti vartotojus vaidmenims**.
2. Pasirinkite vaidmenį **Nuomos valdymas**, **Nuomos klerkas** arba **Nuomos peržiūra** ir pasirinkite **Neautomatiškai priskirti / pašalinti vartotojus**.
3. Pasirinkite vartotoją, kurį norite priskirti vaidmeniui, tada pasirinkite **Priskirti vaidmeniui**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
