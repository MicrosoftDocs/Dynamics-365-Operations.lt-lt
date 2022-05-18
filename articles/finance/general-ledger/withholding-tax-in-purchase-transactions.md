---
title: Atskaitymo mokestis pirkimo perlaidose
description: Pardavėjams, kuriems taikomas atskaitymo mokestis, galite priskirti numatytą **Atskaitomo mokesčio grupę** puslapyje **Visi pardavėjai**.
author: kailiang
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: c2220159cef31bf3343bcf39325c7a0ff3e0cf47
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727208"
---
# <a name="withholding-tax-in-purchase-transactions"></a>Atskaitymo mokestis pirkimo perlaidose

Pardavėjams, kuriems taikomas atskaitymo mokestis, galite priskirti numatytą **Atskaitomo mokesčio grupę** puslapyje **Visi pardavėjai**.

1. Eikite į **Naršymo juosta > Moduliai > Mokėtinos sąskaitos > Pardavėjai > Visi pardavėjai**.

2. Paspauskite atitinkamą Pardavėjo sąskaitą, spauskite **Redaguoti**.

3. Skirtuke **Sąskaita ir pristatymas** nustatykite **Skaičiuoti atskaitomą mokestį** laukelį į **Taip**.

   > [!NOTE] 
   > Atskaitomas mokestis nebus skaičiuojamas, jei **Skaičiuoti atskaitomą mokestį** nėra perjungiamas pardavėjui pagrindiniuose duomenyse.

4. Rinkitės atskaitomą mokesčio grupę **Mokesčių išskaitymo grupėje**.

5. Spustelėkite **Įrašyti**.

Prekėms ir paslaugoms, kurioms taikomas atskaitomas mokestis, galite priskirti numatytą **Prekės atskaitomo mokesčio grupę** **Išleisti produktai**.

1. Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Produktai > Patvirtinti produktai**.

2. Paspauskite atitinkamą prekės numerį, spauskite **Redaguoti**.

3. Skirtuke **Įsigyti** spauskite **Skaičiuoti atskaitomą mokestį**.

   > [!NOTE] 
   > Atskaitomas mokestis nebus skaičiuojamas, jei **Skaičiuoti atskaitomą mokestį** nėra nustatomas į **Taip** šiai prekei **Pirkti** skirtuke **Išleistas produktas** puslapyje.

4. Rinkitės prekę atskaitomą mokesčio grupę **Prekės atskaitymo mokesčio grupės** sąraše.

5. Spustelėkite **Įrašyti**.

Atskaitymo mokesčio grupės ir Prekės atskaitymo mokesčio grupės gali būti priskirtos puslapiuose: 

- **Pirkimo užsakymas**
- **Tiekėjo SF**
- **SF žurnalas**

Numatyta Atskaitomo mokesčio grupė ir prekės atskaitomo mokesčio grupė bus perkeliama į eilutes kuriant **Pirkimo užsakymai** ir (arba) **Laukiančios pardavėjo sąskaitos**. **Pardavėjo sąskaitos žurnale**, galite perjungti **Skaičiuoti atskaitomą mokestį** ir rinkitės **Prekės atskaitymo mokesčio grupę** skirtuke **Bendri** žurnale.

Laikina atskaitomo mokesčio suma yra prieinama laukelyje **Pakeistas atskaitomas mokestis** skirtuke **Bendri** puslapyje **Pirkimo užsakymas**.

![Atskaitomas mokestis yra įtrauktas į pardavimo užsakymą.](media/withholding-tax-adjusted.png)

Atskaitomas mokestis yra skaičiuojamas **Pardavėjo mokėjimo žurnale**. Galite rankiniu būdu keisti taikomą atskaitomo mokesčio kodus, taip pat kaip realią atskaitomo mokesčio sumas **Atskaitomo mokesčio** skirtuke **Nustatytos transakcijos** puslapyje.

![Atskaitymą galima rankiniu būdu valdyti Nustatymų transakcijų puslapyje.](media/withholding-tax-vendor-payment-tab.png)

Išvestas atskaitoma mokesčio suma bus atskaičiuojama iš pardavėjo mokėjimo ir publikuojama **Atskaitomo mokesčio sąskaitos** susijusiame kvite.

![Atskaitomo mokesčio sąskaita rodo susijusį kvitą.](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
