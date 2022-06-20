---
title: „SharePoint“ ryšio konfigūravimas
description: Šiame straipsnyje paaiškinama, kaip sukonfigūruoti ryšį, kad elektroninių SF išrašymas galėtų prieiti prie "Microsoft" SharePoint svetainės.
author: dkalyuzh
ms.date: 12/15/2021
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
ms.openlocfilehash: fb4258190b9480c1302060dd7b75145f80bb7f18
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856586"
---
# <a name="configure-a-sharepoint-connection"></a>„SharePoint“ ryšio konfigūravimas

[!include [banner](../includes/banner.md)]

Elektroninių SF išrašymo tarnyba gali skaityti Failus iš "Microsoft" SharePoint aplankų ir įkelti failus į SharePoint. Norėdami užtikrinti, kad elektroninis SF išrašymas gali prieiti prie tam SharePoint tikros svetainės, turite pateikti svetainės kredencialus elektroninių SF išrašymo paslaugai. Be to, norėdami užtikrinti, kad kredencialai saugomi saugiai, tiesiogiai jų nesuteikite. Užuot tai darę, saugokite juos "Azure" rakto saugykloje ir pateikite "Azure Key" "Vault" slaptą saugyklą.

## <a name="grant-access-to-a-sharepoint-folder"></a>Suteikti prieigą prie SharePoint aplanko

1. Kurti programos registraciją nuomininke, kur įdiegta reguliavimo konfigūracijos tarnyba (RCS).

    1. Prisijunkite prie [„Azure“ portalo](https://portal.azure.com/).
    2. Eikite **į programos registracijas**.
    3. Pasirinkite **Nauja registracija**.
    4. Įveskite pavadinimą, pvz.**SharePoint, Elektroninių SF išrašymo programa**, ir baikite registraciją
    5. Pasirinkite naują programos registraciją.
    6. Skirtuke **Autentifikavimas** įgalinkite parinktį **Leisti viešus kliento srautus**.
    4. Skirtuke **Sertifikatai > paslapia**, pasirinkite **Naujas kliento sekimas,** kad sukurtumėte kliento slaptą klientą.
    5. Kopijuokite sukurto slapto failo vertę.

    Vadovaukitės šiais nurodymais:

    - Nenaudokite tos pačios programos registracijos skirtingoms paslaugoms.
    - Vadovaukitės slaptažodžio [strategijos rekomendacijomis](/microsoft-365/admin/misc/password-policy-recommendations?view=o365-worldwide).
    - Nustatyti slaptažodžių sąs rotaciją. Kaitaliojimo metu sukurkite naują kliento programos registracijos slapyme, atnaujinkite rakto saugyklą, tada panaikinkite seną slaptą.

2. Įrašyti programos **registracijos slaptojo** ir **programos (kliento) ID** vertes kaip du naujus paslapius rakto saugykloje elektroninių SF išrašymo aplinkos nustatyme.
3. Pridėkite paslapius, kuriuos sukūrėte RCS elektroninių SF išrašymo aplinkos nustatyme prie "Key Vault" parametrų.
4. "Azure" portale suteikite prieigą prie SharePoint. Šį žingsnį turi atlikti nuomininkų administratorius.

    1. Pasirinkite sukurtą programos registraciją.
    2. **API teisių skirtuke** pasirinkite **Įtraukti teisę**.
    3. Pasirinkite **"Microsoft" diagramos (programos teisės)** \> **svetaines. Pasirinkta.**
    4. Pasirinkite **Subsidijos administratoriaus sutikimą \<user&nbsp;name\>**.
    5. Norėdami įsitikinti **,** kad teisės suteiktos, peržiūrėkite lauką Būsena.

        ![Teisės, suteiktos API teisių skirtuke.](media/configured-permissions.jpg)

    6. Atidaryti [diagramos naršyklę – MicrosoftGraph](https://developer.microsoft.com/graph/graph-explorer) ir prisijungti.
    7. Kairiajame srities skirtuko Užklausų **pavyzdys dalyje** **SharePoint Svetainės pasirinkite** Gauti svetainę **SharePoint pagal santykinį svetainės kelią**.
    8. Įveskite pagrindinio kompiuterio **\{vardo ir\}** su **\{serveriu susijusios maršruto\}** parametrus. Pavyzdžiui, užpildykite pagrindinio `<domain>.sharepoint.com`**\{kompiuterio pavadinimą\}** ir `sites/<siteName>` su **\{serveriu santykinį maršrutą \}**.

        > [!NOTE]
        > Jei svetainė numatytoji, su **\{serveriu susijusiam maršrutui parametro palikite\}** tuščią.

    9. Pasirinkite **Vykdyti užklausą** ir įrašykite rezultatą.
    10. Sukonfigūruokite šią užklausą.

        `POST https://graph.microsoft.com/v1.0/sites/{site-id}/permissions`

        Šioje užklausoje svetainės **\{ID\}** yra ankstesnio užklausos atsakymo **ID** mazgo vertė.

        Čia yra užklausos tekstas.

        ```json
        {
            "roles": [
                "read",
                "write"
            ],
            "grantedToIdentities": [
                {
                    "application": {
                        "id": "{app-id}",
                        "displayName": "{app-name}"
                    }
                }
            ]
        }
        ```

        Šiame užklausos body, **\{app-ID\}** yra programos **(kliento) ID** reikšmė, **\{o programos pavadinimas\}** yra **programos pavadinimo** reikšmė.

        ![REGISTRUOTI užklausą.](media/app-id-query.jpg)

    11. Skirtuke **Modifikuoti teises** pasirinkite Atidaryti **teisių skydą** ir pasirinkite **Sites.FullControl.Visi** \> **sutikimai.** \> **·**
    12. Pasirinkite **Vykdyti užklausą**.

Elektroninių SF išrašymo paslauga dabar turi prieigą prie jūsų SharePoint svetainės.
