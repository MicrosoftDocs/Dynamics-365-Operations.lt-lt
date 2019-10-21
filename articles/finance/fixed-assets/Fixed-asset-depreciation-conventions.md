---
title: Ilgalaikio turto nusidėvėjimo konvencijos
description: Šioje temoje apžvelgiamos ilgalaikio turto nusidėvėjimo konvencijos.
author: saraschi2
manager: AnnBe
ms.date: 03/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad44282de9d999aa211548601eb416f4bdba2047
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179020"
---
# <a name="fixed-asset-depreciation-conventions"></a>Ilgalaikio turto nusidėvėjimo konvencijos

[!include [banner](../includes/banner.md)]

Nusidėvėjimo konvencijos naudojamos norint nustatyti, kada ir kaip skaičiuojamas metų, kuriais ilgalaikis turtas įsigyjamas, ir metų, kuriais ilgalaikis turtas likviduojamas, nusidėvėjimas.

Nusidėvėjimo konvencijas galima priskirti ilgalaikio turto grupės knygos sąrankai. Norėdami peržiūrėti arba priskirti nusidėvėjimo konvenciją, ilgalaikio turto nustatymo srityje pasirinkite **Ilgalaikio turto** grupes. Paspauskite mygtuką **Knygos**. Šiuo atveju priskirtos nusidėvėjimo konvencijos naudojamos kaip numatytosios reikšmės, kai kuriamos ilgalaikio turto knygos. Nusidėvėjimo konvencijas taip pat galima nustatyti atskirose ilgalaikio turto knygose. Norėdami tai padaryti, ilgalaikio turto nustatymo srityje pasirinkite **Knygos**, paskui paspauskite mygtuką **Ilgalaikio turto grupės**.


|  Nusidėvėjimo konvencija  |   Aprašas  |
|---------------------------|-----------------|
|           Nėra            |  Turto nusidėvėjimo pradžios data – <strong>Atiduota eksploatuoti</strong>.|
|         Pusmetis         |  Pusmečio nusidėvėjimas atimamas tiek iš pirmųjų, tiek iš paskutiniųjų metų, kuriais registruojamas nuosavybės nusidėvėjimas. Visų metų nusidėvėjimas atimamas iš kiekvienų kitų atkūrimo laikotarpio metų. |
|        Visas mėnuo         | Turto, kurio lauke <strong>Atiduota eksploatuoti</strong> nurodyta data gali būti bet kuri mėnesio diena, nusidėvėjimas prasideda pirmąją to mėnesio dieną. Laikoma, kad turtas, kuris grąžinamas bet kuriuo mėnesio metu, yra grąžinamas nusidėvėjimo tikslais paskutiniąją ankstesnio mėnesio dieną.  |
|        Ketvirčio vidurys        | Norėdami apskaičiuoti metų, kuriais nuosavybė atiduota eksploatuoti, nusidėvėjimą, visų metų nusidėvėjimą padauginkite iš ketvirčio, kurį nuosavybė atiduota eksploatuoti, procento, kaip parodyta toliau pateiktoje lentelėje.<table><thead><tr><th>Ketvirtis</th><th>Procentai</th></tr></thead><tbody><tr><td>Pirma</td><td>87,5</td></tr><tr><td>Antra</td><td>62,5</td></tr><tr><td>Trečia</td><td>37,5</td></tr><tr><td>Ketvirta</td><td>12,5</td></tr></tbody></table>Pusė ketvirčio nusidėvėjimo paimama iš likvidavimo ketvirčio (arba visiško nusidėvėjimo ketvirčio). |
| Mėnesio vidurys (mėnesio 1 d.)  | Turto, kurio lauke <strong>Atiduota eksploatuoti</strong> nurodyta data yra pirmoje mėnesio pusėje (1–15 d.), nusidėvėjimas prasideda pirmąją mėnesio, kuriama yra lauke <strong>Atiduota eksploatuoti</strong> nurodyta data, dieną. Turto, kurio lauke <strong>Atiduota eksploatuoti</strong> nurodyta data yra antroje mėnesio pusėje (nuo 16 d. iki mėnesio pabaigos), nusidėvėjimas prasideda pirmąją mėnesio, sekančio po mėnesio, kuriama yra lauke <strong>Atiduota eksploatuoti</strong> nurodyta data, dieną. Laikoma, kad turtas, kuris grąžinamas per pirmąją mėnesio pusę (1–15 d.), yra grąžinamas nusidėvėjimo tikslais paskutiniąją ankstesnio mėnesio dieną. Laikoma, kad turtas, kuris grąžinamas per antrąją mėnesio pusę (nuo 16 d. iki mėnesio pabaigos), yra grąžinamas nusidėvėjimo tikslais paskutiniąją grąžinimo mėnesio dieną. |
| Mėnesio vidurys (mėnesio 15 d.) |  Norėdami apskaičiuoti metų, kuriais nuosavybė atiduota eksploatuoti, nusidėvėjimą, visų metų nusidėvėjimą padauginkite iš trupmenos. Šios trupmenos skaitiklis (viršutinis skaitmuo) yra metų, kuriais nuosavybė eksploatuojama, visų mėnesių skaičius plius 1/2 arba (0,5). Vardiklis (apatinis skaitmuo) yra 12. Jei nuosavybė nurašoma prieš atkūrimo laikotarpio pabaigą, naudokite tą patį metodą skaičiuodami perdavimo metų nusidėvėjimą.   |
| Pusė metų (metų pradžia) | Turto, kurio lauke <strong>Atiduota eksploatuoti</strong> nurodyta data yra pirmoje metų pusėje, nusidėvėjimas prasideda pirmąją metų dieną (visi metai). Turto, kurio lauke <strong>Atiduota eksploatuoti</strong> nurodyta data yra antroje metų pusėje, nusidėvėjimas prasideda metų viduryje.|
|   Pusė metų (kiti metai)   |   Turto, kurio lauke <strong>Atiduota eksploatuoti</strong> nurodyta data yra pirmoje metų pusėje, nusidėvėjimas prasideda pirmąją metų dieną (visi metai). Turto, kurio lauke <strong>Atiduota eksploatuoti</strong> nurodyta data yra antroje metų pusėje, nusidėvėjimas prasideda pirmąją kitų metų dieną. Laikoma, kad turtas, kuris grąžinamas per pirmąją metų pusę, yra grąžinamas nusidėvėjimo tikslais paskutiniąją ankstesnių metų dieną. Nusidėvėjimas, kuris užregistruotas einamaisiais metais, turi būti atšauktas arba pakoreguotas. Laikoma, kad turtas, kuris grąžinamas per antrąją metų pusę, yra grąžinamas nusidėvėjimo tikslais paskutiniąją grąžinimo metų dieną.|
