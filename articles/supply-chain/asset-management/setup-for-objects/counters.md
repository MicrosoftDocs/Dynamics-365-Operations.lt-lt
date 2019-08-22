---
title: Turto matai
description: Šioje temoje paaiškinta, kaip kurti turto matus turto valdyme.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783469"
---
# <a name="asset-measures"></a>Turto matai

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Šioje temoje paaiškinta, kaip kurti turto matus turto valdyme. Turto matų tipai naudojami norint atlikti turto matavimo vienetų registravimus, pvz., gamybos valandų skaičių arba pagaminto turto kiekį. Turto tipai susiję su turto matų tipais. Tai reiškia, kad turto matas gali būti naudojamas turtui tik tuo atveju, jei turto matas nustatomas naudojamo turto tipui.

Prieš atliekant turto matavimo vienetų registravimus būtina sukurti turto matų tipus, kuriuos norite naudoti dalyje **Skaitikliai**. Tada galima kurti turto matavimo vienetų registravimus dalyje **Turto matai**. 

Turto matai gali būti naudojami priežiūros planuose. Priežiūros plano eilutė gali būti tipo „Skaitiklis“, pavyzdžiui, susijusi su gamybos valandų skaičiumi arba pagamintu kiekiu. 

Turto matavimo vienetų registravimus galima atnaujinti rankiniu būdu arba automatiškai, atsižvelgiant į gamybos valandas arba pagamintą kiekį. Turto matas gali būti nustatytas naudoti vieną iš trijų naujinimo metodų (pasirinktų lauke **Naujinti** dalyje **Skaitikliai**):
  
- Rankinis – būtina užregistruoti turto matavimo vienetų reikšmes rankiniu būdu.  
- Gamybos valandos – skaitiklis automatiškai atnaujinamas pagal gamybos valandų skaičių.  
- Gamybos kiekis – skaitiklis automatiškai atnaujinamas pagal pagamintą kiekį.  

>[!NOTE]
>Jei naudojamas pagamintas kiekis, *visi* užregistruoti elementai įtraukiami į matavimo vienetų registravimą, tiek tinkamas, tiek netinkamas kiekis. Jei reikia, visada galima rankiniu būdu atlikti turto matavimo vienetų registravimus.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Turto skaitiklio registravimų skaitiklio tipų kūrimas

1. Pasirinkite **Turto valdymas** > **Sąranka** > **Turto tipai** > **Skaitikliai**.
2. Pasirinkite **Naujas**, kad sukurtumėte naują turto matavimo vieneto tipą.
3. Lauke **Skaitiklis** įterpkite ID, o lauke **Pavadinimas** – skaitiklio pavadinimą.
4. „FastTab“ **Bendra** pasirinkite matavimo vienetą lauke **Vienetas**.
5. Lauke **Naujinti** pasirinkite turto matui naudojamą naujinimo metodą.
6. Perjungimo mygtuke **Paveldėti skaitiklio reikšmes** pasirinkite „Taip“, jei antrinis turtas turto struktūroje turėtų automatiškai paveldėti turto matų registravimus, atliktus pagrindiniame turte.
7. Lauke **Bendroji agreguota reikšmė** pasirinkite turto matų sumavimo metodą naudojant šį turto mato tipą. „Sum“ yra standartinis pasirinkimas, naudojamas norint nuolat įtraukti užregistruotas reikšmes į bendrąją reikšmę. „Average“ gali būti naudojama, jei turto matas nustatytas stebėti ribines reikšmes, pvz., temperatūrą, vibraciją ar turto nusidėvėjimą. 
8. Lauke **Nuokrypis virš** įterpkite viršutinę procentinę reikšmę tikrinant, ar rankiniai turto matų registravimai patenka į numatytą diapazoną. Tikrinimas pagrįstas esamo turto mato registravimų linijiniu padidėjimu.
9. Lauke **Nuokrypis po** įterpkite apatinę procentinę reikšmę tikrinant, ar rankiniai turto matų registravimai patenka į numatytą diapazoną. Tikrinimas pagrįstas esamo turto mato registravimų linijiniu sumažėjimu.
10. Lauke **Tipas** pasirinkite pranešimo tipą (informacija, įspėjimas, klaida), kuris bus rodomas, jei rankinio turto mato registravimų metu atsiranda nuokrypių už apibrėžto diapazono.
11. „FastTab“ **Turto tipai** įtraukite turto tipus, kurie turėtų naudoti turto matą.
12. „FastTab“ **Susijusio turto matai** įtraukite turto matus, kurie bus automatiškai atnaujinti atnaujinus šį turto matą.


>[!NOTE]
>Susijęs turto matas automatiškai atnaujinamas tik tuo atveju, jei turto mato nustatymuose susijęs turto matas yra turto tipo, su kuriuo jis yra susijęs. Pavyzdžiui: galima nustatyti turto matą „Gamybos valandoms“ ir įtraukti turto tipą „Sunkvežimio variklis“. Kai šis turto matas atnaujinamas, susijęs skaitiklis „Nafta“ taip pat atnaujinamas pagal tas pačias turto matų reikšmes. Nustatymai dalyje **Skaitikliai** apima nustatymus „Valandos“. Be to, „Nafta“ turto mate turto tipas „Sunkvežimio variklis“ turi būti įtrauktas į „FastTab“ **Turto tipai**, kad būtų užtikrintas turto mato ryšys. Žr. toliau pateiktus ekrano vaizdus, kus pateiktas Valandų ir Naftos turto matų nustatymo pavyzdys.

Kai turto tipai įtraukiami į turto mato tipą dalyje **Skaitikliai**, tas turto matas automatiškai įtraukiamas į turto tipus „FastTab“ **Skaitikliai** dalyje [Turto tipai](../setup-for-objects/object-types.md).

![1 pav.](media/071-setup-for-objects.png)


