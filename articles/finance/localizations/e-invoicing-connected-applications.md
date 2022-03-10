---
title: Prijungtos programos
description: Šioje temoje paaiškinama, kaip nustatyti susijusias programas elektroninių SF išrašymo metu.
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 59b67589139c0ce332716acf998825c6a024bded
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371919"
---
# <a name="connected-applications"></a>Prijungtos programos

[!include [banner](../includes/banner.md)]

Sujungtos programos yra "Microsoft" egzemplioriai Dynamics 365 Finance Dynamics 365 Supply Chain Management, kuriuos galite pasiekti naudodami reguliavimo konfigūracijos tarnybą (RCS). Naudodami susijusias programas galite konfigūruoti savo finansų arba tiekimo grandinės valdymo globalizavimo funkcijos dalį, kad veiktų elektroninių SF išrašymo scenarijus.

Kai diegiate savo globalizavimo funkciją, nustatymo informaciją, kuri taikoma jūsų finansų arba tiekimo grandinės valdymo programai, galima publikuoti tiesiogiai iš RCS į atitinkamą prijungtą programą.

Finansų arba tiekimo grandinės valdymo parametrų pasiekiamumas RCS yra naudingas, kai turite kelias programos aplinkas, pvz., vartotojo priėmimo testą (UAT) ir gamybos aplinką, ir jūs norite išlaikyti nustatymą nuoseklų, diegdami tuos pačius parametrus į skirtingas aplinkas.

## <a name="create-a-connected-application"></a>Kurkite sujungtą programą

1. Prisijunkite prie jūsų RCS abonemento.
2. Darbo srities **Globalizacijos funkcijos** dalyje **Aplinka** pasirinkite plytelę **Elektroninių SF išrašymo priedas**.
3. **Aplinkos nustatymo puslapyje**, veiksmų srityje, pasirinkite Sujungtos **programos**.
4. Pasirinkite **Naujas**, kad sujungtumėte programą.
5. **Pavadinimas** laukelyje įveskite sujungiamos programos pavadinimą.
6. Lauke **Tipas** pasirinkite **„Dynamics 365 Finance”**.
7. **Programos lauke** įveskite aplinkos, prie kurios norite prisijungti, URL.
8. **Lauke Nuomininkas** įveskite aplinkos nuomininką.
9. Pasirinkite **Įrašyti**.
10. Veiksmų srityje pasirinkite **Tikrinti ryšį** norėdami patikrinti ryšį su aplinka. Tada uždarykite puslapį.

## <a name="link-connected-applications-to-environments"></a>Susieti prie aplinkos prijungtas programas

1. Aplinkos nustatymo **puslapyje** pasirinkite Naujas **, jei** norite aplinkai priskirti prijungtą programą.
2. Laukelyje **Prijungta programa** pasirinkite sujungtą programą.
3. Lauke **Aptarnavimo aplinka** pasirinkite darbo užsakymo aptarnavimo aplinką.
4. Pasirinkite **Įrašyti** ir uždarykite puslapį.
