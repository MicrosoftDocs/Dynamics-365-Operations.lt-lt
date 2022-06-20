---
title: Ilgalaikio turto vertės modelis ir nusidėvėjimo knygos suliejimas
description: 'Ankstesniuose leidimuose buvo naudojamos dvi ilgalaikio turto vertinimo sąvokos: vertinimo modelis ir nusidėvėjimo knygos. „Microsoft Dynamics 365 for Operations“ (1611) leidime vertinimo modelio funkcija ir nusidėvėjimo knygų funkcija buvo sujungtos į vieną sąvoką, vadinama knyga.'
author: moaamer
ms.date: 10/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 221564
ms.assetid: 7c68eb7c-8b1a-4dd9-afb8-04b4040e305e
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f4f06b7916fb2eeed802b2dce95edfce448dcd97
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880851"
---
# <a name="fixed-asset-value-model-and-depreciation-book-merge"></a>Ilgalaikio turto vertės modelis ir nusidėvėjimo knygos suliejimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomos dabartinio ilgalaikio turto knygos funkcijos. Naujos knygos funkcionalumas pagrįstas ankstesnio vertės modelio funkcionalumu, kuris buvo ankstesnėse versijose, bet taip pat apima visą anksčiau tik nusidėvėjimo knygose pateikiamą funkcionalumą.

Knygų funkcijos leidžia naudoti vieną puslapių, užklausų ir ataskaitų rinkinį visų jūsų organizacijos ilgalaikio turto procesų metu. Šio straipsnio lentelėse aprašomos ankstesnės nusidėvėjimo knygų ir vertinimo modelių funkcijos bei dabartinės knygų funkcijos.

## <a name="setup"></a>Sąranka
Pagal numatytuosius parametrus knygos registruojamos ir didžiojoje knygoje (DK), ir ilgalaikio turto papildomoje knygoje. Knygose pateikiama nauja parnktis **Registruoti didžiojoje knygoje**, kuria naudodamiesi galite išjungti registravimą DK ir registruoti tik ilgalaikio turto papildomoje knygoje. Ši funkcija primena ankstesnę nusidėvėjimo knygų registravimo veikseną. Žurnalų pavadinimų sąranka turi naują registravimo sluoksnį, kurio pavadinimas Nėra. Šis registravimo sluoksnis pridėtas specialiai ilgalaikio turto operacijoms. Norėdami registruoti į DK neregistruojančių knygų operacijas, privalote naudoti žurnalo pavadinimą, kuriame nustatyta registravimo sluoksnio nuostata **Nėra**.


| &nbsp;                                           | Nusidėvėjimo knyga               | Vertinimo modelis                     | Knyga (nauja)                                              |
|--------------------------------------------------|---------------------------------|---------------------------------|---------------------------------------------------------|
| Registruoti didžiojoje knygoje                                   | Niekada                           | Visada                          | Parinktis registruoti didžiojoje knygoje                                |
| Registravimo sluoksniai                                   | Netaikoma                  | 3: Dabartiniai duomenys, operacijos ir mokesčiai | 11: Dabartiniai duomenys, operacijos, mokesčiai, 7 pasirinktiniai sluoksniai ir nėra |
| Žurnalų pavadinimai                                    | Nusidėvėjimo knygos žurnalo pavadinimai | DK - žurnalo ataskaitos              | DK - žurnalo ataskaitos                                      |
| Išvestinės knygos                                    | Neleidžiama                     | Leidžiama                         | Leidžiama                                                 |
| Nusidėvėjimo profilio nepaisymas turto lygiu | Leidžiama                         | Neleidžiama                     | Leidžiama                                                 |

## <a name="processes"></a>Procesai
Procesuose dabar naudojamas bendrasis puslapis. Kai kurie procesai leidžiami tik tuo atveju, jeigu knygos sąrankoje nustatyta parinkties **Registruoti didžiojoje knygoje** nuostata **Ne**.

| &nbsp;                                           | Nusidėvėjimo knyga               | Vertės modelis                     | Knyga (nauja)                                              |
|--------------------------------|---------------------------|---------------------|------------------------------------------|
| Operacijos įvedimas              | Nusidėvėjimo knygos žurnalas | Ilgalaikio turto žurnalas | Ilgalaikio turto žurnalas                      |
| Papildomas nusidėvėjimas             | Leidžiama                   | Neleidžiama         | Leidžiama                                  |
| Naikinti ankstesnes operacijas | Leidžiama                   | Neleidžiama         | Leidžiama, jeigu neregistruojate didžiojoje knygoje |
| Masinis atnaujinimas                    | Leidžiama                   | Neleidžiama         | Leidžiama, jeigu neregistruojate didžiojoje knygoje |

## <a name="inquiries-and-reports"></a>Užklausos ir ataskaitos
Užklausos ir ataskaitos palaiko visas knygas. Į toliau pateikiamą lentelę neįtrauktos ataskaitos anksčiau palaikė ir nusidėvėjimo knygas, ir vertės modelius, o dabar palaikys visus knygų tipus. Laukas **Registravimo sluoksnis** taip pat įtrauktas į ataskaitas, kad galėtumėte lengviau identifikuoti operacijų registravimus.

| &nbsp;                                           | Nusidėvėjimo knyga               | Vertės modelis                     | Knyga (nauja)                                              |
|---------------------------------------|--------------------------------|--------------------------|--------------------------|
| Užklausos                             | Nusidėvėjimo knygos operacijos | Ilgalaikio turto operacijos | Ilgalaikio turto operacijos |
| Ilgalaikio turto išrašas                 | Neleidžiama                    | Leidžiama                  | Leidžiama                  |
| Ilgalaikio turto pagrindas                     | Leidžiama                        | Neleidžiama              | Leidžiama                  |
| Ketvirčio vidurio ilgalaikio turto taikomumas | Leidžiama                        | Neleidžiama              | Leidžiama                  |

## <a name="upgrade"></a>Atnaujinti
Atnaujinimo procesas perkels esamą jūsų sąranką ir visas esamas jūsų operacijas į naują knygos struktūrą. Vertės modeliai liks tokie patys, kokie yra šiuo metu, kaip knyga, kuri registruoja į didžiąją knygą. Tačiau nusidėvėjimo knygos bus perkeltos į knygą, kurioje nustatyta parinkties **Registruoti į DK** nuostata **Ne**. Nusidėvėjimo knygos žurnalų pavadinimai bus perkelti į DK žurnalo pavadinimą, kuriame nustatyta registravimo sluoksnio nuostata **Nėra**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
