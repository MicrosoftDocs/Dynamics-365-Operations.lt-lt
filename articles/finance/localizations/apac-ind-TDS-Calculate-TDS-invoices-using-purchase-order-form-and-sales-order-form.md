---
title: Skaičiuoti TDS SF naudojant pirkimo užsakymo formą ir pardavimo užsakymo formą
description: Šioje temoje pateikiami žurnalų iš šaltinio (TDS) išskaityamų mokesčių skaičiavimo veiksmai su įvairių rūšių sąskaitomis.
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
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023438"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a>Skaičiuoti TDS SF naudojant pirkimo užsakymo formą ir pardavimo užsakymo formą

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiami veiksmai, kaip apskaičiuoti iš šaltinio (TDS) atskaičius mokesčius įvairių tipų SF, naudojant **pirkimo užsakymą**, **pirkimo žurnalą**, **bendrą užsakymą**, ir **Pardavimo užsakymą** puslapius.

1. Naudodami šį puslapį sukurkite pirkimo užsakymą, pirkimo žurnalą, bendrą pirkimo užsakymą arba pardavimo užsakymą. Įveskite reikiamą informaciją.

2. Norėdami **peržiūrėti** tiekėjo arba kliento vertinimo pobūdį, pasirinkite nustatymo skirtuką. Ši informacija pateikta **apmokestinimo pobūdžio** lauke, išskaitomo **mokesčio grupės laukų** grupėje.

3. Lauke **TDS grupė** peržiūrėkite arba modifikuokite numatytąją TDS grupę, nurodytą tiekėjui ar klientui.

   > [!NOTE]
   > Lauke **TCS grupės** negalimas, kai TDS grupės lauke pasirenkate **TDS grupę**. TDS skaičiuojamas tik jei **Skaičiuoti išskaitomą mokestį** žymimas laukelis yra pažymėtas tiekėjui ar klientui **Visi tiekėjai** ar **Visi klientai** puslapyje.  

4. Sukurkite prekės eilutes skirtuke **Eilutės** ir įveskite reikiamą informaciją.

5. Norėdami **peržiūrėti** arba pakeisti antraštės lygyje nurodytą TDS grupę, pasirinkite nustatymo skirtuką (eilutės lygis). TDS grupė rodoma **TDS grupės** lauke, kuris yra išskaitomo **mokesčio grupės laukų** grupėje.

6. Pasirinkite **mokesčių informacijos** skirtuką ir rinkitės alternatyvius įmonės, nustatytos įmonės pavadinimus, kurie rodomi šiame lauke. Įmonės pavadinimas rodomas lauke **Pavadinimas**, kuris yra **įmonės informacijos** laukų grupėje. 

   Pasirinktos įmonės pavadinimo TAN rodomas **mokesčių sąskaitos numerio** (**TAN**) lauke, išskaitomo **mokesčio lauko** grupėje. 

7. Rinkitės **Išskaitomas mokestis** norėdami atverti **Laikino išskaitomo mokesčio operacijų** puslapį. Peržiūrėti šiuos laukus, rodomus viršutinėje laikino išskaitomo **mokesčio operacijų puslapio** srityje.

   - **Išskaitomo** **mokesčio** **suma** **iš** **viso** - bendroji TDS grupės operacijos TDS suma.

   - **Vertė** – bendrasis procentas, naudojamas operacijos TDS apskaičiuoti. Bendrasis procentas remiasi formule, kuri nustatyta TDS mokesčių kodams, pridėtiems prie TDS grupės.

   - **Pakoreguota išskaitomo mokesčio suma visa** – bendroji koreguota TDS suma, skirta visiems TDS grupės mokesčių kodams.

   - **TDS** – jei pasirinkta, prie operacijos pridedama TDS grupė.

Laukeliai **Peržiūra**, **Bendra**, ir **Koregavimas** laikinų išskaitomo **mokesčių operacijų puslapyje** rodo apskaičiuotą TDS sumą ir pakoreguotos TDS sumos informaciją kiekvienam TDS mokesčių kodui, pridėtame prie TDS grupės.

8. Pasirinkite **Ribinės vertės** lauką, kad atidarytumėte **slenkstį**. Peržiūrėkite šiame puslapyje nurodytą TDS mokesčio komponento, pridėto prie konkretaus TDS mokesčio kodo, ribinės vertės ir išimties ribą.

9. Norėdami **atidaryti formulės** konstruktoriaus puslapį, pasirinkite **Formulės konstruktorius**. Peržiūrėkite šiame puslapyje nurodytą konkretaus TDS mokesčio kodo formulę. 

10. Registruoti SF. Pirkimo SF apskaičiuota TDS suma užregistruojama mokėtinoje sąskaitoje, o pardavimo SF apskaičiuota TDS suma užregistruojama gautinų sumų sąskaitoje, kuri nustatyta kiekvienam TDS mokesčio kodui TDS grupėje. TDS mokesčių kodų mokėtinos sumos arba gautinos sąskaitos nustatomos puslapyje **Išskaitomo mokesčio kodai**.

11. Rinkitės **Užklausos** mygtukas **> Sąskaita > Publikuotas išskaitomas mokestis** mygtuką norėdami atverti **Išskaitomo mokesčio perlaidų** puslapį. Galite peržiūrėti **Vertė** laukelyje bendrąjį procentą, naudojamą rodyti operacijas ir TDS apskaičiuoti.

Laukeliai **Peržiūra**, **Bendra** ir **Suma** skirtukuose **Išskaitomo mokesčio operacijų** puslapyje rodo apskaičiuotos operacijos TDS informaciją. Peržiūrėti TDS skaičiavimo informaciją apie kiekvieną TDS mokesčių kodą, pridėtą prie TDS grupės.
