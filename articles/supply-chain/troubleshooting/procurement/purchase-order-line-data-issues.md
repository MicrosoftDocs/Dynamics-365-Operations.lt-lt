---
title: Pirkimo užsakymo eilutės duomenų nesutapimų
description: Pamatysite duomenų nesutapimų ar duomenų sugadinimo jūsų pirkimo užsakymo eilutėse duomenis.
author: SmithaNataraj
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: PurchLineManualCorrection, PurchTable, PurchLine, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: ee2cb9a07c8a00a92c71e3e99d8ec20aa27fb20e
ms.sourcegitcommit: b9799a58d6ec221df86788bc37c4fbd28b435e89
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/08/2022
ms.locfileid: "8100784"
---
# <a name="purchase-order-line-data-discrepancies"></a>Pirkimo užsakymo eilutės duomenų nesutapimų

## <a name="symptoms"></a>Požymiai

Patikrindami pirkimo užsakymo eilutes, pastebite vieną ar daugiau iš šių problemų:

- Pirkimo užsakymo eilutės likučiuose (pristatymo ar SF) yra duomenų nesutapimų ar sugadinimo.
- Pirkimo užsakymo eilutėje arba antraštės būsenoje gali būti sugadinimo.
- Negalite išrašyti pirkimo užsakymo sąskaitos faktūros, nes, pavyzdžiui, gaunate vieną ar daugiau iš šių klaidos pranešimų:

    - "Sustabdyta (klaida): operacija jau užregistruota."
    - "Kiekiui negalima išrašyti SF, nes nepakanka atsargų operacijų, kurių būsena – gauta".
    - "Nepakanka atsargų operacijų, kurių būsena Nupirkta" prekių kiekiui%0%1.

- Negalite baigti ar uždaryti pirkimo užsakymo dėl, pvz., vieno iš šių problemų:

    - Mygtuko **Baigti** nėra.
    - Negalima atšaukti pirkimo užsakymo, kurio būsena patvirtintas ir gautas, pirkimo užsakymo eilutėje užsakyto kiekio.

## <a name="cause"></a>Priežastis

Šie dalykai dažniausiai kyla dėl duomenų sugadinimo arba dėl vienos ar daugiau pirkimo užsakymo eilučių likučio kiekių neatitikimo.

## <a name="resolution"></a>Paaiškinimas

Paprastai šiuos problemos ištaisomos atnaujinant atitinkamų pirkimo užsakymo eilučių pirkimo būseną, pristatymo likučius ir /arba SF likučius, kaip apibūdinta šioje procedūroje.

1. Eikite **į Įsigijimo ir pirkimo periodines užduotis \> Rankinis \> pirkimo \> užsakymo eilučių valymas**.
1. Lauke Pirkimo **užsakymas** raskite ir pasirinkite pirkimo užsakymą, kuris jums suteikia problemų.
1. Pirkimo užsakymo **eilučių skyriuje** pasirinkite eilutę, kurioje rastas neatitikimas.
1. **Atsargų operacijų skyriuje** patikrinkite rodomą informaciją. Jei pastebite bet kokį pirkimo užsakymo eilutės ir jos atsargų operacijų nenuoseklumą, veiksmų srityje pasirinkite vieną iš šių komandų, atsižvelgdami į tai, kur matote nenuoseklumo atvejus:

    - **Perskaičiuoti pristatymo likučio \> perskaičiavimą – automatiškai** atnaujinti pirkimo užsakymo eilutę ir antraščių būsenas. Ši funkcija taikoma tik sandėliuojamims pirkimo užsakymo eilutėms (tai yra eilutėms, kuriose prekė yra atsargų prekė). Nelaikomos prekės ir esamo svorio prekės šiuo metu nepalaikomos.
    - **Perskaičiuoti sf \> likučio perskaičiavimą – automatiškai** atnaujinti pirkimo užsakymo eilutę ir antraščių būsenas. Ši funkcija taikoma tik sandėliuojamims pirkimo užsakymo eilutėms (tai yra eilutėms, kuriose prekė yra atsargų prekė). Nelaikomos prekės ir esamo svorio prekės šiuo metu nepalaikomos.
    - **Perskaičiuoti \> būseną Perskaičiuoti** – perskaičiuoti pasirinktos eilutės būseną. Šis skaičiavimas pagrįstas esama logika. Todėl, atsižvelgiant į naujos pirkimo užsakymo eilutės būseną, pirkimo užsakymo antraštės būsena bus atnaujinta, kaip reikalaujama.

1. Jei likučių kiekiuose vis dar matote nenuoseklumų, galite naudoti šiuos laukus tiesiogiai juos redaguoti, kai to reikia:

    - Pristatymo likutis
    - Pristatytinų atsargų likutis
    - SF likutis
    - Atsargų SF likutis
