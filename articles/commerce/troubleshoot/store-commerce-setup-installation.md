---
title: Parduotuvės "Commerce" nustatymo ir diegimo trikčių šalinimas
description: Šiame straipsnyje paaiškinama, kaip šalinti nustatymo ir diegimo problemas parduotuvės " Microsoft Dynamics 365 Commerce Commerce" programoje.
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 8af2c476ced05fc159a53131f8b51ad914a6c7c3
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/16/2022
ms.locfileid: "9168953"
---
# <a name="troubleshoot-store-commerce-setup-and-installation-issues"></a>Parduotuvės "Commerce" nustatymo ir diegimo trikčių šalinimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip šalinti nustatymo ir diegimo problemas parduotuvės " Microsoft Dynamics 365 Commerce Commerce" programoje.

## <a name="i-cant-activate-the-app-and-i-receive-a-connectivity-error-message"></a>Nepavyko suaktyvinti programos, ir rodomas ryšio klaidos pranešimas

Įvesdami tinkamą debesies point of Sale (CPOS) URL, galite gauti jungiamumo klaidos pranešimą, kuris yra panašus į tokį pavyzdį:

> Įvyko ryšio klaida ir jūsų įrenginys negali prisijungti prie CPOS. Gali kilti tam tikrų problemų tarp CPOS URL.

Tokiu atveju peržiūrėkite netipinių grafinių klaidų URL arba nustatykite, ar negalima pasiekti CPOS, nes ji neprisijungus.

Be to, patikrinkite, ar debesies skalės vieneto (CSU) versija 10.0.25 (9.35.\*.\*) arba vėliau. Norint naudoti "Store Commerce" programą, reikia CPOS 10.0.25 ar naujesnės versijos.

## <a name="i-cant-install-the-app-because-modern-pos-is-already-installed"></a>Nepavyko įdiegti programos, nes "Modern POS" jau įdiegtas

Diegimo metu galite gauti klaidos pranešimą, pvz.:

> Šio produkto ("Modern POS") versija (9.\*.\*.\*) įdiegta senesnėje diegimo programoje.

Norėdami ištaisyti klaidą, turite pašalinti modernaus kasos aparato (MPOS) programą visiems įrenginio vartotojams ir bandykite dar kartą. Galite patvirtinti, ar MPOS buvo pašalintas visiems vartotojams, vykdydami šią "PowerShell" komandą.

```PowerShell
Get-AppxPackage | Where-Object {$_.PackageFullName -like "Microsoft.Dynamics.*.Pos"} | Remove-AppxPackage -Allusers
```

## <a name="i-cant-activate-the-app-because-of-an-invalid-url-or-an-error-state"></a>Nepavyko suaktyvinti programos dėl netinkamo URL arba klaidos būsenos

Jei jūsų įvestas CPOS URL yra netinkamas ir norite jį pakeisti arba jei parduotuvės "Commerce" programos būsena aktyvinimo metu yra klaidos būsena, galite iš naujo paleisti procesą iš naujo nustatę programą. Parduotuvės "Commerce" programa įrašys tik tinkamą CPOS URL.

Norėdami iš naujo nustatyti "Store Commerce" programą, atlikite šiuos veiksmus.

1. "Windows" **meniu Pradėti** pasirinkite ir laikykite (arba spustelėkite dešiniuoju pelės mygtuku) programėlę ir pasirinkite Daugiau **\> programos parametrų**.
2. Paslinkite programos parametrų puslapį žemyn, kol rasite mygtuką **Nustatyti iš** naujo.
3. Pasirinkite **Nustatyti iš naujo**. Tada, kai būsite paraginti, patvirtinkite, kad norite iš naujo nustatyti programą.
