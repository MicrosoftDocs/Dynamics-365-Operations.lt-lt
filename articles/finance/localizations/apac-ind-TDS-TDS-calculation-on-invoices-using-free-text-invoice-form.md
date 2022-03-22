---
title: TDS skaičiavimas SF iš laisvos formos SF puslapio
description: Šioje temoje paaiškinama, kaip apskaičiuoti iš šaltinio (TDS) atskaičius mokesčius, naudojant laisvos formos SF puslapį.
author: kailiang
ms.date: 02/12/2021
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
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: c543876c48eca55eaaa6fd67585ec357dfea276ffbf8abad3c28c6f4cf29f782
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750369"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a>TDS skaičiavimas SF iš laisvos formos SF puslapio

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip apskaičiuoti iš šaltinio (TDS) atskaičius mokesčius, naudojant **laisvos formos SF** puslapį.

1. Pasirinkite **Gautinos sumos \> Sąskaitos faktūros \> Visos laisvos formos SF**.

    [![Laisvos formos SF puslapis.](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)

2. Rinkitės **Nauja** norėdami sukurti laisvo teksto sąskaitą ir įvesti reikiamą informaciją.
3. Rinkitės **SF** skirtuką. Skyriuje **Išskaitomo mokesčio grupė** lauke **Vertinamo pobūdis** lauke rodomas vertinamos kliento kategorijos pobūdis.
4. Lauke **TDS grupė** peržiūrėkite arba keiskite numatytąją TDS grupę, nurodytą tiekėjui ar klientui.

    > [!NOTE]
    > Jums pasirinkus vertę **TDS grupės** laukelyje, **TCS grupės** laukelis tampa nebeprieinamas. TDS skaičiuojamas tik jei **Skaičiuoti išskaitomą mokestį** parinktis yra nustatyta į **Taip** klientui **Visi klientai** puslapyje.

5. Skirtuke **Mokesčių informacija** ir **Įmonės informacija** skyrius, lauke **Pavadinimas** pasirinkite įmonės pavadinimą alternatyviam adresui, kuris nustatytas įmonei.

    **Išskaitomo mokesčio** skyriuje, laukas **Mokesčių sąskaitos numeris (TAN)** rodo pasirinktos įmonės mokesčių sąskaitos numerį (TAN).

6. Skirtuke **SF eilutės** kurkite SF eilutes ir įveskite būtiną informaciją.

    **Išskaitomų mokesčių grupės** skyriuje laukas **Mokesčių sąskaitos numeris (TAN)** rodo TAN, o **TDS grupės** lauke rodoma TDS grupė.

7. Rinkitės **Išskaitomas mokestis** norėdami atverti **Laikino išskaitomo mokesčio operacijų** puslapį. Viršutinėje šio puslapio dalyje yra šie laukai:

    - **Bendroji išskaitomo mokesčio suma** – bendroji TDS grupės operacijos TDS apskaičiuota suma.
    - **Vertė** – bendrasis procentas, kuris buvo naudojamas operacijos TDS apskaičiuoti. Bendrasis procentas remiasi formule, kuri nustatyta TDS mokesčių kodams, pridėtiems prie TDS grupės.
    - **Pakoreguota išskaitomo mokesčio suma visa** – bendroji koreguota TDS suma, skirta visiems TDS grupės mokesčių kodams.
    - **TDS** – pasirinktas žymės langelis rodo, kad prie operacijos pridėta TDS grupė.

    Laukeliai **Peržiūra**, **Bendra** ir **Koreguota** skirtukuose išskaitomo mokesčių operacijų puslapyje rodo apskaičiuotos TDS sumos informaciją ir pakoreguotos TDS sumos informaciją kiekvienam TDS mokesčių kodui, pridėtame prie TDS grupės.

8. Norėdami atidaryti **ribinės vertės** puslapį, rinkitės **Ribinė vertė** puslapį, kur galite peržiūrėti TDS mokesčio komponento, pridėto prie konkretaus TDS mokesčio kodo, vertės limitą, pasirinkite Ribinę vertę.
9. Pasirinkite **formulės konstruktorių,** norėdami atverti **Formulės konstruktoriaus** puslapį, kuriame galite peržiūrėti formulę nurodytą konkrečiam TDS mokesčio kodui.
10. Registruoti laisvos formos SF. TDS suma, apskaičiuota pardavimo laisvo teksto sąskaitai, užregistruojama gautinų sumų sąskaitoje, kuri nustatoma kiekvienam TDS mokesčio kodui TDS grupėje. TDS mokesčių kodų mokėtinos sumos arba gautinos sąskaitos nustatomos puslapyje **Išskaitomo mokesčio kodai**.
11. Rinkitės **Publikuotas išskaitomas mokestis** norėdami atverti **Išskaitomo mokesčio perlaidų** puslapį. Laukelis **Vertė** – bendrasis procentas, kuris buvo naudojamas operacijos TDS apskaičiuoti.

    Skirtuko **Peržiūra**, **Bendra** ir **Suma** rodo apskaičiuotas pagal SF eilutes TDS sumas, apskaičiuotas SF eilutėse.

12. Peržiūrėti TDS skaičiavimo informaciją apie kiekvieną TDS mokesčių kodą, pridėtą prie TDS grupės.
