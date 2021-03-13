---
title: Atskaytimo mokestis pardavimo perlaidose
description: Šioje temoje išvardyti žingsniai, kuriais galima išvengti išskaitymo mokesčio skaičiavimo pasirinktiems klientams. Klientams, kurie nurodo išskaitymo mokestį jų mokėjimuose jums, galite priskirti numatytą išskaitymo mokesčio grupę.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: c50f6df1c63c91107da65f463934565f786d6ccd
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060771"
---
# <a name="withholding-tax-in-sales-transactions"></a>Atskaytimo mokestis pardavimo perlaidose

Šioje temoje išvardyti žingsniai, kuriais galima išvengti išskaitymo mokesčio skaičiavimo pasirinktiems klientams. Klientams, kurie nurodo išskaitymo mokestį jų mokėjimuose jums, galite priskirti numatytą numatytą **Išskaitymo mokesčio grupę** puslapyje **Klientai**. 

1. Eikite į **Naršymo juosta > Moduliai > Gautinos sąskaitos > Klientai > Visi klientai**.

2. Paspauskite atitinkamą kliento sąskaitą, spauskite **Redaguoti**.

3. Skirtuke **Sąskaita ir pristatymas** nustatykite **Skaičiuoti atskaitomą mokestį** laukelį į **Taip**.

   > [!NOTE] 
   > Atskaitomas mokestis nebus skaičiuojamas, jei **Skaičiuoti atskaitomą mokestį** nėra perjungiamas klientui pagrindiniuose duomenyse.

4. Rinkitės atskaitomą mokesčio grupę **Mokesčių išskaitymo grupėje**.

5. Spustelėkite **Įrašyti**.

Prekėms ir paslaugoms, kurioms taikomas atskaitomas mokestis, galite priskirti numatytą **Prekės atskaitomo mokesčio grupę** **Išleisti produktai**.

1. Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Produktai > Patvirtinti produktai**.

2. Paspauskite atitinkamą prekės numerį, spauskite **Redaguoti**.

3. Skirtuke **Parduoti** spauskite **Skaičiuoti atskaitomą mokestį**.

   > [!NOTE] 
   > Atskaitomas mokestis nebus skaičiuojamas, jei **Skaičiuoti atskaitomą mokestį** nėra nustatomas į **Taip** šiai prekei **Parduoti** skirtuke **Išleistas produktas** puslapyje.

4. Rinkitės prekės atskaitomą mokesčio grupę **Prekės atskaitymo mokesčio grupės** sąraše.

5. Spustelėkite **Įrašyti**.

Atskaitymo mokesčio grupės ir Prekės atskaitymo mokesčio grupės gali būti priskirtos naudojant **Prekybos užsakymą** puslapį. 

Numatyta Atskaitomo mokesčio grupė ir prekės atskaitomo mokesčio grupė bus naudojamos kaip numatytieji objektai prekybos užsakymo eilutėse, kai kuriate naują prekybos užsakymą.

Atskaitomas mokestis yra skaičiuojamas ir publikuojamas **Kliento mokėjimo žurnalas**. Galite rankiniu būdu keisti taikomą atskaitomo mokesčio kodą, taip pat kaip realią atskaitomo mokesčio sumą **Atskaitomo mokesčio** skirtuke **Nustatytos transakcijos** puslapyje.

Apskaičiuota atskaitoma mokesčio suma bus atskaičiuojama iš kliento mokėjimo ir publikuojama **Atskaitomo mokesčio nustatymas** sąskaita susijusiame kvite.
