---
title: Turto kūrimas remiantis pirkimo užsakymais
description: Šiame straipsnyje paaiškinama, kaip sukurti turto prekių sąrašą, kurį galima naudoti kaip pagrindą kuriant turtą turto valdymo priežiūros darbams.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccd14493aac6484dc54ccf51ae159a071c8697a5
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015615"
---
# <a name="create-assets-based-on-purchase-orders"></a>Turto kūrimas remiantis pirkimo užsakymais

[!include [banner](../../includes/banner.md)]

 

Šiame straipsnyje paaiškinama, kaip sukurti turto prekių sąrašą, kurį galima naudoti kaip pagrindą kuriant turtą turto valdymo priežiūros darbams. Atsižvelgdami į turto elementus, galite peržiūrėti pirkimo užsakymo eilučių sąrašą, sukurtą konkretiems elementams. Ši funkcija padeda lengvai sukurti turtą modulyje Turto valdymas pagal pirkimo užsakymą.

Pirmiausia nustatykite elementus, kurie bus naudojami kuriant turtą iš pirkimo užsakymo, esančio **Turto elementai**. Sukūrę pirkimo užsakymo eilutę, sukurkite turtą, naudodami **Turtas, laukiantis patvirtinimo**. Galite nuspręsti, kuriame pirkimo užsakymo etape norėsite sukurti turtą.


## <a name="select-asset-items"></a>Pasirinkite turto elementus

1. Spustelėkite **Turto valdymas** > **Konfigūracija** > **Turtas** > **Elementai**.
2. Spustelėję **Nauja** sukurkite naują prekių grupę.
3. Lauke **Prekės numeris** pasirinkite prekę. Uždarius šį lauką, elemento pavadinimas automatiškai įterpiamas į lauką **Produkto pavadinimas**.
4. „FastTab“ skirtuke **Bendra** pasirinkite elemento turto tipą.
5. Pasirinkite turto gamintoją ir elemento modelį.
6. Įrašykite elementą.


## <a name="create-assets-from-pending-assets"></a>Turto sukūrimas naudojant turtą, laukiantį patvirtinimo

1. Spustelėkite **Turto valdymo turtas** > **Laukiantis** > **turtas**.
2. Pamatysite atnaujintą pirkimo užsakymų sąrašą pagal elementus, pasirinktus modulyje **Turto elementai**.
3. Galite filtruoti pirkimo užsakymų būseną, kad pasirinktumėte, kurioje ciklo būsenoje turtas turėtų būti sukurtas. Pavyzdžiui, galite pasirinkti sukurti turtą tik tada, kai produkto gavimo kvitas užregistruotas pirkimo užsakyme.
4. Daugiau informacijos apie elementą rasite paspaudę nuorodą **Nuorodos numeris**, esančią pirkimo užsakymo eilutėje.
5. Jei norite redaguoti, kurios dimensijos yra rodomos „FastTab“ skirtuke **Atsargų dimensijos**, spustelėkite mygtuką **Rodyti dimensijas** ir redaguokite pasirinkimą.
6. Jei norite kurti turtą pagal pirkimo užsakymo eilutę, sąrašo puslapyje pažymėkite tos eilutės žymės langelį stulpelyje **Žyma** ir spustelėkite **Kurti turtą**. Pasirodys pranešimas apie turto ID.
7. Sąraše **Visas turtas** pasirinkite turtą ir spustelėkite **Redaguoti**, kad pridėtumėte daugiau informacijos apie turtą.
8. Jei lauke **Laukiantis turtas** norite panaikinti eilutę, nes nenorite sukurti turto, pasirinkite tos eilutės žymės langelį stulpelyje **Žymėti** ir spustelėkite **Atmesti laukiantį turtą**. Pasirodys pranešimas apie turto ID. Jūs nepanaikinate pirkimo užsakymo arba pardavimo užsakymo, panaikinamas tik įrašas, iš kurio galėjote sukurti turtą modulyje **Turto valdymas**.

>[!NOTE]
>Visos produkto dimensijos (dydis, spalva, konfigūracija ir kt.) automatiškai perkeliamos į turto atributus. Sekimo dimensijos (serijos numeris) yra išsaugomos sukurtame turte.


## <a name="find-pending-assets"></a>Turto, laukiančio patvirtinimo, paieška

Galite paleisti funkciją **Laukiančio turto skaičiavimas**, norėdami patikrinti, ar yra turto, laukiančio patvirtinimo. Pavyzdžiui, ši funkcija gali būti naudojama kiekvieną kartą gavus pranešimą apie tai, kad turtas, laukiantis patvirtinimo, yra parengtas būti sukurtas kaip turtas.

1. Spustelėkite **Turto valdymas** > **Periodinis** > **Turtas** > **Turto, laukiančio patvirtinimo, skaičiavimas**.
2. Spustelėkite **Gerai**, jei norite vykdyti užduotį ir atnaujinti sąrašą, esantį **Laukiantis turtas**.
3. Galite nustatyti, kad ši užduotis būtų vykdoma kaip paketinė užduotis, pvz., kartą per dieną.

**Atsargiai:** Įspėjimas: jei pirkimo užsakymo duomenys pakeičiami *jau* sukūrus turtą pagal jam priklausantį elementą, pakeitimai neturės turtui jokios įtakos.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]