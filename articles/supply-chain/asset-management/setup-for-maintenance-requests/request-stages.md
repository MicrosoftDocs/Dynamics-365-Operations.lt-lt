---
title: Priežiūros užklausos ciklo būsenos
description: Šiame straipsnyje aprašoma, kaip turto valdymo modulyje nustatyti priežiūros užklausos ciklo teigiamas vietas.
author: johanhoffmann
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestLifecycleState, EntAssetRequestLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81b30820adf11f0239ea8ff9d1886b5738e38162
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862720"
---
# <a name="maintenance-request-lifecycle-states"></a>Priežiūros užklausos ciklo būsenos

[!include [banner](../../includes/banner.md)]

 


Priežiūros užklausos ciklo būsenos nurodo etapus, kuriuose gali būti užklausa. Pavyzdžiui, **Sukurta**, **Aktyvi** ir **Baigta**. Kai priežiūros užklausa konvertuojama į darbo užsakymą, priežiūros užklausos ciklo būsena turėtų būti atnaujinta į **Baigta** arba **Uždaryta**, siekiant nurodyti, kad priežiūros užklausa yra nebeaktyvi. Sąrašo puslapyje **Visos priežiūros užklausos** galite matyti visas priežiūros užklausas, neatsižvelgiant į jų ciklo būseną.

## <a name="set-up-maintenance-request-lifecycle-states"></a>Priežiūros užklausos ciklo būsenų nustatymas

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Priežiūros užsakymai** \> **Ciklo būsenos**.
2. Pasirinkite **Naujas**, kad sukurtumėte priežiūros užklausos ciklo būseną.
3. Lauke **Ciklo būsena** įveskite ciklo būsenos ID.
4. Tada lauke **Pavadinimas** įveskite pavadinimą.

    „FastTab“ skirtuko **Informacija** lauke **Ciklo modeliai** matysite priežiūros užklausų ciklo modelių, kurie naudoja šią ciklo būseną, skaičių.

5. „FastTab" skirtuke **Bendra** nustatykite parinktį **Aktyvi** į **Taip**, jei priežiūros užklausa turėtų būti aktyvi, kol ji yra šioje ciklo būsenoje.
6. Nustatykite parinkties **Nustatyti faktinę pabaigą** reikšmę į **Taip**, jei faktinė pabaigos data ir laikas turėtų būti automatiškai įvedami į šioje ciklo būsenoje esančią priežiūros užklausą.
7. Nustatykite parinktį **Kurti darbo užsakymą** į **Taip**, jei darbo užsakymas gali būti sukurtas iš šioje ciklo būsenoje esančios priežiūros užklausos.
8. Nustatykite parinktį **Trinti** į **Taip**, jei priežiūros užklausa gali būti ištrinta jai esant šioje ciklo būsenoje.
9. „FastTab“ konteinerio **Atnaujinimas** dalyje **Turtas** esančios parinktys **Gaunama** ir **Siunčiama** yra svarbios, jei naudojate sandėlio remontą. Nustatykite reikiamą parinktį į **Taip**, jei priežiūros užklausoje pasirinkta turto ciklo būsena turėtų būti automatiškai atnaujinta į **Gaunama** arba **Siunčiama**, kai tos priežiūros užklausos ciklo būsena nustatyta kaip **Gaunama** arba **Siunčiama**.

Paveikslėlyje pavaizduotas puslapio **Priežiūros užklausos ciklo būsenos** pavyzdys.

![Priežiūros užklausos ciklo būsenų puslapis.](media/02-setup-for-requests.png)

> [!NOTE]
> Priežiūros užklausos ciklo būsenos, ciklo būsenos grupės bei tipai yra susiję ir naudojami taip pat, kaip ir darbo užsakymo ciklo būsenos, ciklo būsenos grupės bei tipai. 

## <a name="set-up-maintenance-request-lifecycle-models"></a>Priežiūros užklausos ciklo modelių nustatymas

Sukūrę ciklo būsenas, kurios yra reikalingos jūsų priežiūros užklausoms, jas galite suskirstyti į ciklo būsenos grupes arba ciklo modelius. Priežiūros užklausų ciklo modeliai naudojami norint sukurti srautą, kuris gali būti naudojamas įvairių tipų priežiūros užklausoms. Turi būti sukuriamas mažiausiai vienas standartinis priežiūros užklausos ciklo modelis.

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Priežiūros užklausos** \> **Ciklo modeliai**.
2. Pasirinkite **Naujas**, kad sukurtumėte priežiūros užklausos ciklo modelį.
3. Lauke **Ciklo modelis** įveskite ciklo modelio ID.
4. Tada lauke **Pavadinimas** įveskite pavadinimą.

    „FastTab“ skirtuko **Informacija** eilutėje **Ciklo būsenos** rodomas šiame ciklo modelyje pasirinktų ciklo būsenų skaičius. Lauke **Priežiūros užklausos tipai** matysite šiame ciklo modelyje naudojamų priežiūros užklausos tipų skaičių.

5. „FastTab“ skirtuke **Ciklo būsenos** pasirinkite ciklo būsenas, kurios turėtų būti įtrauktos į šį ciklo modelį:

    - Norėdami įtraukti ciklo būseną į ciklo modelį, pasirinkite ją **Likusios ciklo būsenos** skyriuje, o tada pasirinkite dešinės rodyklės mygtuką ![Rodyklė dešinėn.](media/03-setup-for-requests.png) jos perkėlimui į **Pasirinktos ciklo būsenos** skyrių.
    - Norėdami į ciklo modelį įtraukti visas galimas ciklo būsenas, spustelėkite mygtuką **Pasirinkti visas galimas būsenas** ![Pasirinkti visas galimas būsenas.](media/04-setup-for-requests.png). Visos ciklo būsenos bus perkeltos į skyrių **Pasirinktos ciklo būsenos**.
    - Norėdami pašalinti ciklo būseną iš ciklo modelio, pasirinkite ją **Pasirinktos ciklo būsenos** skyriuje, o tada pasirinkite kairės rodyklės mygtuką ![Rodyklė kairėn.](media/05-setup-for-requests.png) jos perkėlimui į **Likusios ciklo būsenos** skyrių.

6. „FastTab“ skirtuko **Bendra** skyriuje **Atnaujinimai** esantys laukai yra svarbūs, jei naudojate sandėlio remontą.

    - Lauke **Gauto turto ciklo būsena** pasirinkite turto ciklo būseną, į kurią priežiūros užklausoje pasirinktas turtas turėtų būti atnaujintas automatiškai, kai jis gaunamas sandėlio remontui.
    - Lauke **Išsiųsto turto ciklo būsena** pasirinkite turto ciklo būseną, į kurią priežiūros užklausoje pasirinktas turtas turėtų būti atnaujintas automatiškai, kai jis bus sugrąžintas po remonto darbų.

Paveikslėlyje pateiktas puslapio **Priežiūros užklausos ciklo būsenos** pavyzdys.

![Priežiūros užklausos ciklo modelių puslapis.](media/06-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]