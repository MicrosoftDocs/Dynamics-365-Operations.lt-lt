---
title: Automatiškai taikyti išankstinį mokėjimą tiekėjų sąskaitoms
description: Šiame straipsnyje aprašoma, kaip galima automatiškai taikyti išankstinius apmokėjimus tiekėjo SF.
author: sunfzam
ms.date: 10/19/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 547573d187460a900df7f4927ac062bd9d456729
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900077"
---
# <a name="automatically-apply-to-vendor-invoices"></a>Automatiškai taikyti išankstinį mokėjimą tiekėjų sąskaitoms

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip galima automatiškai taikyti išankstinius apmokėjimus tiekėjo SF. Išankstinis apmokėjimas gali būti sukurtas pirkimo užsakymui kaip pirkimo sutarties dalis. Kai gauta tiekėjo SF, išankstinis apmokėjimas gali būti naudojamas sudengti mokėtinas sumas iš tiekėjo SF. Nauja funkcija leidžia sistemai automatiškai naudoti pirkimo užsakymo numerius tiekėjo SF, kad būtų ieškoma atitinkamų išankstinių mokėjimų importuotos tiekėjo SF.

Jei randami išankstiniai mokėjimai ir juos galima taikyti, eilutės pridedami prie esamų SF eilučių, kad būtų galima taikyti išankstinius apmokėjimus. Išankstinio mokėjimo eilučių neįrašoma SF gretinimo proceso metu.

Toliau pateikti taškai apibūdina, kaip taikomi išankstiniai mokėjimai, kai sekami skirtingi pirkimo procesai:

- **Viena tiekėjo SF vienam pirkimo užsakymui** – išankstinis apmokėjimas pirkimo užsakyme bus taikomas tiekėjo SF.
- **Viena tiekėjo SF keliems pirkimo užsakymams** – išankstinis apmokėjimas visiems pirkimo užsakymams bus taikomas tiekėjo SF.
- **Kelių tiekėjų SF vienam pirkimo užsakymui** – išankstinis apmokėjimas pirkimo užsakyme bus taikomas tiekėjo pirmoji importuota SF. Jei išankstinio mokėjimo suma viršija SF sumą, išankstinio apmokėjimo prašymas nepavyksta ir jūs turite taikyti išankstinį apmokėjimą rankiniu būdu.
- **Kelių tiekėjų SF keliems pirkimo užsakymui** – išankstinis apmokėjimas pirkimo užsakyme bus taikomas tiekėjo pirmoji atitinkamai importuotai SF. Jei išankstinio mokėjimo suma viršija SF sumą, išankstinio apmokėjimo prašymas nepavyksta ir jūs turite taikyti išankstinį apmokėjimą rankiniu būdu. Jei visi išankstiniai mokėjimai, liekami po išankstinių mokėjimų, yra taikomi pirmai SF, jie gali būti taikomi toliau skirtoms SF.

Jei bandymas taikyti išankstinį apmokėjimą nesėkmingas, **bloko** veiksmų automatizavimo proceso nustatymas išankstinio apmokėjimo programos trikčių atveju lems kitus veiksmus:

- **Taip** – klaidos pranešimas „Automatinis išankstinio apmokėjimo taikymas: nepavyko" įtrauktas į automatizavimo retrospektyvą, o SF lieka laukiančių tiekėjo SF sąraše. SF bus užblokuota, kol išankstinis apmokėjimas nebus taikomas rankiniu būdu.

Norėdami išankstinius apmokėjimus taikyti rankiniu būdu, eikite į laukiančią tiekėjo SF. SF **informacijos puslapyje** nustatykite parinktį **Įtraukti į automatizuotą apdorojimą**, kai užblokuota SF yra **Ne**. Dabar galite taikyti išankstinį apmokėjimą rankiniu būdu. Kai išankstinis apmokėjimas buvo pritaikytas, nustatykite parinktį **Įtraukti į automatinį apdorojimą** parinktį atgal į **Taip** kad SF būtų galima apdoroti automatiškai.

Taip pat galite apeiti automatinį išankstinio apmokėjimo taikymą, nustatydami pasirinktį **Įtraukti į automatinį apdorojimą** parinktį į **Ne** nustatydami vėl **Taip**. Gausite tokį pranešimą: „Jau yra pirkimo užsakymo išankstinis apmokėjimas. Ar norite nepaisyti pasirinkto tiekėjo SF?“ Pasirinkite **Taip**. Pranešimas „Išankstinio apmokėjimo taikymas apeitas rankiniu būdu" įtraukiamas į automatizavimo retrospektyvą, o tiekėjo SF nebus užblokuota, kai automatiškai vykdomas procesas dar kartą.

- **Ne** – bus tęsiamas automatizavimo procesų sekimas. Sudengimo metu dar galite taikyti išankstinį apmokėjimą.
