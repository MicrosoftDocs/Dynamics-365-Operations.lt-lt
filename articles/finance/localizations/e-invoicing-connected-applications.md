---
title: Prijungtos programos
description: Šiame straipsnyje paaiškinama, kaip nustatyti susijusias programas elektroninių SF išrašymo metu.
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
ms.openlocfilehash: 7a0a9c19009c49b80ca8c182c31592c1a713a2aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906293"
---
# <a name="connected-applications"></a>Prijungtos programos

[!include [banner](../includes/banner.md)]

Prisijungę prašymai yra Microsoft Dynamics 365 finansų Dynamics 365 Supply Chain Management egzemplioriai, kuriuos galite norėti pasiekti per reguliavimo konfigūracijos tarnybą (RCS). Naudodami susijusias programas galite konfigūruoti savo finansų arba tiekimo grandinės valdymo globalizavimo funkcijos dalį, kad veiktų elektroninių SF išrašymo scenarijus.

Kai diegiate savo globalizavimo funkciją, nustatymo informaciją, kuri taikoma jūsų finansų arba tiekimo grandinės valdymo programai, galima publikuoti tiesiogiai iš RCS į atitinkamą prijungtą programą.

Finansų arba tiekimo grandinės valdymo parametrų pasiekiamumas RCS yra naudingas, kai turite kelias programos aplinkas, pvz., vartotojo priėmimo testą (UAT) ir gamybos aplinką, ir jūs norite išlaikyti nustatymą nuoseklų, diegdami tuos pačius parametrus į skirtingas aplinkas.

## <a name="create-a-connected-application"></a>Kurkite sujungtą programą

1. Prisijunkite prie jūsų RCS abonemento.
2. Darbo srities **Globalizacijos funkcijos** dalyje **Aplinka** pasirinkite plytelę **Elektroninių SF išrašymo priedas**.
3. **Aplinkos nustatymo puslapyje**, veiksmų srityje, pasirinkite Sujungtos **programos**.
4. Pasirinkite **Naujas**, kad sujungtumėte programą.
5. **Pavadinimas** laukelyje įveskite sujungiamos programos pavadinimą.
6. Lauke Tipas **pasirinkite** " **Dynamics 365 Finance"**.
7. **Programos lauke** įveskite aplinkos, prie kurios norite prisijungti, URL.
8. **Lauke Nuomininkas** įveskite aplinkos nuomininką.
9. Pasirinkite **Įrašyti**.
10. Veiksmų srityje pasirinkite **Tikrinti ryšį** norėdami patikrinti ryšį su aplinka. Tada uždarykite puslapį.

## <a name="link-connected-applications-to-environments"></a>Susieti prie aplinkos prijungtas programas

1. Aplinkos nustatymo **puslapyje** pasirinkite Naujas **, jei** norite aplinkai priskirti prijungtą programą.
2. Laukelyje **Prijungta programa** pasirinkite sujungtą programą.
3. Lauke **Aptarnavimo aplinka** pasirinkite darbo užsakymo aptarnavimo aplinką.
4. Pasirinkite **Įrašyti** ir uždarykite puslapį.
