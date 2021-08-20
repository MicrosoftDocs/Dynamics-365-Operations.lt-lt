---
title: TDS skaičiavimų formulės konstruktorius
description: Šioje temoje pateikiamas pavyzdys, kaip apskaičiuojamas mokestis iš šaltinio (TDS), remiantis formule, nurodyta kiekvienam TDS mokesčio kodui TDS grupėje, kuri pridėta prie operacijos.
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
ms.openlocfilehash: e9c97982233b1f3dc3924fa42954b5cb8d09ffcaa07d19a3892b25737a6c29c5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778874"
---
# <a name="formula-designer-for-tds-calculations"></a>TDS skaičiavimų formulės konstruktorius

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiamas pavyzdys, kaip apskaičiuojamas mokestis iš šaltinio (TDS) remiantis formule, nustatyta kiekvienam TDS mokesčio kodui. TDS mokesčių kodai yra nustatyti TDS grupėje, kuri pridėta prie operacijos. Prieš sukurkite TDS formules, atlikite pagrindinį TDS reikalingą nustatymą, kaip nurodyta toliau nurodytus veiksmus. 

- Nustatykite TDS komponento grupes naudodami **Mokesčių išskaitymo komponento grupių** puslapį. 
- Nustatykite TDS komponentus ir pridėkite TDS komponentų grupę prie TDS komponentų, naudodami **išskaitomo mokesčio komponentų** puslapį. 
- Nustatykite TDS mokesčio kodus ir pridėkite TDS komponentus į mokesčių kodus naudodami **išskaitomo mokesčio kodų** puslapį 
- Nustatykite TDS mokesčio grupes naudodami **Mokesčių išskaitymo komponento grupių** puslapį. Tada pridėkite TDS mokesčių kodus prie mokesčių grupės ir, naudodami **formulės dizaino** įrankio puslapį nustatykite formulę. 

**Formulės pavyzdys**

Šiame pavyzdyje TDS grupė „Nuoma" pridėta prie pirkimo SF, sukurtos tiekėjui A. SF suma yra $100 000. Norėdami peržiūrėti SF TDS skaičiavimą žr. pateiktą lentelę.

| TDS grupė                                                   | TDS mokesčių kodai, pridėti prie TDS grupės | Reikšmė              | Apmokestinama pagrindas (formulės konstruktorius) | Skaičiavimo išraiška (formulės konstruktorius) | Pagrindinė suma | Apskaičiuota TDS suma |
| ------------------------------------------------------------ | --------------------------------------- | ------------------ | --------------------------------- | :----------------------------------------: | ----------- | --------------------- |
| Nuoma                                                         | TDS  (TDS komponento-TDS)                | 10 %                | Bendra suma                      |                                            | 100,000      | 10,000                 |
| Papildomas mokestis (TDS komponentas – papildomas mokestis)                         | 10 %                                     | Neįskaičiuota bendra suma | +TDS                              |                   10000                    | 1000        |                       |
| PE-Justs (TDS komponentas – PE–Ūsai)                            | 2 %                                      | Neįskaičiuota bendra suma | +TDS+Perviršis                    |                   11000                    | 220         |                       |
| SHE Narių (TDS komponentas - SHE Gans)                          | 1 %                                      | Neįskaičiuota bendra suma | +TDS+Perviršis                    |                   11000                    | 110         |                       |
| **Bendroji** **TDS**  **apskaičiuota** **skirta** **šiai** **sąskaitai** | **11,330**                               |                    |                                   |                                            |             |                       |

Kvito įrašai kuriami taip.

| Paskyra           | Debetas  | Kreditas |
| ----------------- | ------ | ------ |
| Nuoma              | 100,000 |        |
| Tiekėjas A          |        | 100,000 |
| Tiekėjas A          | 11,330  |        |
| Mokėtinas TDS       |        | 10,000  |
| Mokėtinas perviršis |        | 1000   |
| Mokėtinos SUMOS PE-Pis   |        | 220    |
| SHE Mokėtina suma  |        | 110    |
