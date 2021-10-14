---
title: Grąžinimo mažinimo principai
description: Šioje temoje aprašoma, kaip nustatyti mažinimo principus. Mažinimo principai kontroliuoja veikimo būdą, kai keli grąžinimai yra taikomi tai pačiai prekei arba operacijai.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e6b178704fde18036d526e7a645cb9b4f8bd66c7
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579069"
---
# <a name="rebate-reduction-principles"></a>Grąžinimo mažinimo principai

[!include [banner](../includes/banner.md)]

Galite grupuoti grąžinimo valdymo sandorius į *mažinimo principus* siekiant sumažinti kitas su preke susietas nuostatas ir (arba) sumažinti gautas grąžinimo skaičiavimų vertes. Nustatę grąžinimo mažinimo principus, galite pasirinktinai priskirti juos grąžinimo valdymo sandorių eilutėms, kaip reikalaujama.

Grąžinimo mažinimo principo taisyklės taikomos tik tada, kai grąžinimo sandoriai persidengia. Todėl, jie gali suteikti kelius grąžinimus situacijose, kai keli grąžinimai nėra pareikalauti.

## <a name="manage-rebate-reduction-principles"></a>Grąžinimo mažinimo principų valdymas

Norėdami dirbti su grąžinimo mažinimo principais, eikite į **Grąžinimo valdymas \> Nustatymas \> Grąžinimo mažinimo principai**. Tada naudokite veiksmų srities mygtukus mažinimo principų pridėjimui ir panaikinimui, kaip reikalinga. Kiekvienam principui nustatykite laukus, kaip aprašyta šioje lentelėje.

| Laukas | Aprašas |
|---|---|
| Grąžinimo mažinimo principas | Įveskite unikalųjį grąžinimo mažinimo principo pavadinimą. |
| Aprašas | Įveskite grąžinimo mažinimo principo aprašą. |
| Taikyti mažinimą | Pasirinkite šį žymės langelį, jei norite taikyti mažinimo pagrindą grąžinimams, priklausantiems šiam grąžinimo mažinimo principui. |
| Mažinimo pagrindas | Jei pasirinkote žymės langelį **Taikyti mažinimą**, pasirinkite mažinimo pagrindą (*Nuostata*, *Grąžinimai* arba *Abu*). Jei pasirenkate *Abu* ir jeigu tiek nuostata, tiek grąžinimas buvo užregistruoti ankstesniam sandoriui, bus taikomas tik grąžinimas. |
| Išskirti iš mažinimo | Jei pasirenkamas šis žymės langelis, šiam grąžinimo mažinimo principui priklausančios nuostatos ir grąžinimai nebus įtraukti į vėlesnius sumažinimus. Lauko **Mažinimo pagrindas** nustatymas netaikomas šiam parametrui. |

## <a name="examples-of-rebate-reduction-principle-setups"></a>Grąžinimo mažinimo principo nustatymų pavyzdžiai

Šioje lentelėje pateikiama keletas įprastų grąžinimo mažinimo principo nustatymų pavyzdžių. Kiekvieno iš šių grąžinimo mažinimo principų **Aprašo** lauko reikšmės apibūdina grąžinimo mažinimo principo paskirtį.

| Grąžinimo mažinimo principas | Aprašas | Taikyti mažinimą | Mažinimo pagrindas | Išskirti iš mažinimo |
|---|---|---|---|---|
| Atidėta | Grąžinimo sumažinimas | Taip | Abu | Ne |
| Išskirti grąžinimą | Neįtraukti grąžinimo | Taip | Grąžinimas | Taip |
| Kartotinis | Keli grąžinimai | Taip | Abu | Taip |
| None | Tik nuostata ir grąžinimas | Ne | Abu | Taip |
| Konfigūruoti | Tik nuostata | Taip | Konfigūruoti | Ne |
| Grąžinimas | Tik grąžinimas | Taip | Grąžinimas | Taip |

## <a name="examples-of-rebate-reduction-principle-calculations"></a>Grąžinimo mažinimo principo skaičiavimų pavyzdžiai

Turite pardavimo užsakymą, kuriame yra viena pardavimo užsakymo eilutė. Šios eilutės vertė yra $1000. Užsakymui taikomi šie pasiūlymai:

- **1 pasiūlymas:** 10 procentų nuo $1000
- **2 pasiūlymas:** 15 procentų nuo $1000
- **3 pasiūlymas:** 20 procentų nuo $1000
- **4 pasiūlymas:** 25 procentai nuo $1000

Apdorojimo tvarka yra labai svarbi. Apdorojimo tvarka yra pagrįsta jūsų darbo būdu, kaip aprašyta skyriuje [Grąžinimų apdorojimas, peržiūra ir registravimas](process-review-post.md).

Pavyzdžiui, šioje lentelėje apibendrinami rezultatai, jei naudojate tvarką *„1, 2, 3, 4”* ir jei apdorojate tik nuostatas.

| Pasiūlymas | Aprašymas ir parametrai | Nuostatos rezultatas |
|---|---|---|
| 1 | <p>Klasifikavimas netikrina kitų pasiūlymų dėl mažinimų. Atliekama tiek nuostatų, tiek grąžinimų patikra.</p><ul><li>**Taikyti mažinimą:** *Ne*</li><li>**Mažinimo pagrindas** *Abu*</li><li>**Išskirti iš mažinimo** *Ne*</li></ul> | $1 000 × 10% = $100 |
| 2 | <p>Klasifikavimas tikrina kitus pasiūlymus dėl sumažinamų, bet yra pažymėtas taip, kad pats būtų nepaisomas. Atliekama tik grąžinimų patikra.</p><ul><li>**Taikyti mažinimą:** *Taip*</li><li>**Mažinimo pagrindas:** *Grąžinimas*</li><li>**Išskirti iš mažinimo** *Taip*</li></ul> | $1000 × 15% = $150 |
| 3 | <p>Klasifikavimas tikrina kitus pasiūlymus dėl mažinimų. Atliekama tiek nuostatų, tiek grąžinimų patikra.</p><ul><li>**Taikyti mažinimą:** *Taip*</li><li>**Mažinimo pagrindas** *Abu*</li><li>**Išskirti iš mažinimo** *Ne*</li></ul> | ($1000 – 1 pasiūlymas) × 20% = $180 |
| 4 | <p>Klasifikavimas tikrina kitus pasiūlymus dėl mažinimų. Atliekama tiek nuostatų, tiek grąžinimų patikra.</p><ul><li>**Taikyti mažinimą:** *Taip*</li><li>**Mažinimo pagrindas** *Abu*</li><li>**Išskirti iš mažinimo** *Ne*</li></ul> | ($1000 – 1 pasiūlymas – 3 pasiūlymas) × 25% = $180 |

Šioje lentelėje pateikiami keli pavyzdžiai, kur nuostata apdorojama skirtinguose užsakymuose ir dėl to pasiektos skirtingos bendrosios sumos. Nukrypimas nuo nuostatų priklauso nuo tvarkos, pagal kurią sistema apdoroja pasiūlymus Svarbu suprasti, kaip apdorojimo tvarka paveikia galutinę grąžinimo sumą.

| Seka | Skaičiavimas |
|---|---|
| 1<br>„(1, 2, 3, 4)” | <ul><li>**1 pasiūlymas:** $1000 × 10% = $100</li><li>**2 pasiūlymas:** $1000 × 15% = $150</li><li>**3 pasiūlymas:** ($1000 – 1 pasiūlymas) × 20% = $180</li><li>**4 pasiūlymas:** ($1000 – 1 pasiūlymas – 2 pasiūlymas) × 25% = $180</li><li>**Bendroji suma:** $610</li></ul> |
| 2<br>„(4, 3, 2, 1)” | <ul><li>**4 pasiūlymas:** $1000 x 25% = $250</li><li>**3 pasiūlymas:** ($1000 – 4 pasiūlymas) × 20% = $150</li><li>**2 pasiūlymas:** $1000 x 15% = $150</li><li>**1 pasiūlymas:** $1000 x 10% = $100</li><li>**Bendroji suma:** $650</li></ul> |
| 3<br>„(3, 2, 1, 4)” | <ul><li>**3 pasiūlymas:** $1000 x 20% = $200</li><li>**2 pasiūlymas:** $1000 x 15% = $150</li><li>**1 pasiūlymas:** $1000 x 10% = $100</li><li>**4 pasiūlymas:** ($1000 – 3 pasiūlymas – 1 pasiūlymas) × 25% = $175</li><li>**Bendroji suma:** $625</li></ul> |
| 4<br>„(2, 4, 1, 3)” | <ul><li>**2 pasiūlymas:** $1000 × 15% = $150</li><li>**4 pasiūlymas:** $1000 × 25% = $250</li><li>**1 pasiūlymas:** $1000 × 10% = $100</li><li>**3 pasiūlymas:** ($1000 – 4 pasiūlymas – 1 pasiūlymas) × 20% = $130</li><li>**Bendroji suma:** $630</li></ul> |
