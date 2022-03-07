---
title: Automatiškai taikyti išankstinį mokėjimą tiekėjų sąskaitoms
description: Šioje temoje aprašomas galimybės automatiškai taikyti išankstinius apmokėjimus tiekėjo SF.
author: sunfzam
ms.date: 10/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: b1ea73a50f5adaa1a00c9ddfa8c983375e0d47be
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675739"
---
# <a name="automatically-apply-to-vendor-invoices"></a>Automatiškai taikyti išankstinį mokėjimą tiekėjų sąskaitoms

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas galimybės automatiškai taikyti išankstinius apmokėjimus tiekėjo SF. Išankstinis apmokėjimas gali būti sukurtas pirkimo užsakymui kaip pirkimo sutarties dalis. Kai gauta tiekėjo SF, išankstinis apmokėjimas gali būti naudojamas sudengti mokėtinas sumas iš tiekėjo SF. Nauja funkcija leidžia sistemai automatiškai naudoti pirkimo užsakymo numerius tiekėjo SF, kad būtų ieškoma atitinkamų išankstinių mokėjimų importuotos tiekėjo SF.

Jei randami išankstiniai mokėjimai ir juos galima taikyti, eilutės pridedami prie esamų SF eilučių, kad būtų galima taikyti išankstinius apmokėjimus. Išankstinio mokėjimo eilučių neįrašoma SF gretinimo proceso metu.

Toliau pateikti taškai apibūdina, kaip taikomi išankstiniai mokėjimai, kai sekami skirtingi pirkimo procesai:

- **Viena tiekėjo SF vienam pirkimo užsakymui** – išankstinis apmokėjimas pirkimo užsakyme bus taikomas tiekėjo SF.
- **Viena tiekėjo SF keliems pirkimo užsakymams** – išankstinis apmokėjimas visiems pirkimo užsakymams bus taikomas tiekėjo SF.
- **Kelių tiekėjų SF vienam pirkimo užsakymui** – išankstinis apmokėjimas pirkimo užsakyme bus taikomas tiekėjo pirmoji importuota SF. Jei išankstinio mokėjimo suma viršija SF sumą, išankstinio apmokėjimo prašymas nepavyksta ir jūs turite taikyti išankstinį apmokėjimą rankiniu būdu.
- **Kelių tiekėjų SF keliems pirkimo užsakymui** – išankstinis apmokėjimas pirkimo užsakyme bus taikomas tiekėjo pirmoji atitinkamai importuotai SF. Jei išankstinio mokėjimo suma viršija SF sumą, išankstinio apmokėjimo prašymas nepavyksta ir jūs turite taikyti išankstinį apmokėjimą rankiniu būdu. Jei visi išankstiniai mokėjimai, liekami po išankstinių mokėjimų, yra taikomi pirmai SF, jie gali būti taikomi toliau skirtoms SF.

Jei sistema bando taikyti išankstinį apmokėjimą, bet programa veikia nesėkmingai, ji priklauso nuo to, kaip veikia **blokavimo automatizavimo procesas, jei yra išankstinio apmokėjimo programos trikčių** pasirinktis:

- **Taip** – klaidos pranešimas „Automatinis išankstinio apmokėjimo taikymas: nepavyko" įtrauktas į automatizavimo retrospektyvą, o SF lieka laukiančių tiekėjo SF sąraše. SF bus užblokuota, kol išankstinis apmokėjimas nebus taikomas rankiniu būdu.

    Norėdami išankstinius apmokėjimus taikyti rankiniu būdu, eikite į laukiančią tiekėjo SF. SF **informacijos puslapyje** nustatykite parinktį **Įtraukti į automatizuotą apdorojimą**, kai užblokuota SF yra **Ne**. Dabar galite taikyti išankstinį apmokėjimą rankiniu būdu. Kai išankstinis apmokėjimas buvo pritaikytas, nustatykite parinktį **Įtraukti į automatinį apdorojimą** parinktį atgal į **Taip** kad SF būtų galima apdoroti automatiškai.

    Taip pat galite apeiti automatinį išankstinio apmokėjimo taikymą, nustatydami pasirinktį **Įtraukti į automatinį apdorojimą** parinktį į **Ne** nustatydami vėl **Taip**. Gausite tokį pranešimą: „Jau yra pirkimo užsakymo išankstinis apmokėjimas. Ar norite nepaisyti pasirinkto tiekėjo SF?“ Pasirinkite **Taip**. Pranešimas „Išankstinio apmokėjimo taikymas apeitas rankiniu būdu" įtraukiamas į automatizavimo retrospektyvą, o tiekėjo SF nebus užblokuota, kai automatiškai vykdomas procesas dar kartą.

- **Ne** – bus tęsiamas automatizavimo procesų sekimas. Sudengimo metu dar galite taikyti išankstinį apmokėjimą.
