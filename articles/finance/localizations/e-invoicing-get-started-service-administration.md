---
title: Pradėti su elektroninės sąskaitos priedo paslaugų administravimu
description: Ši tema paaiškina, kaip pradėti su elektroninės sąskaitos priedo paslaugų administravimu.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 05b00380cec7511adad2467d3f252799a4aaee5c
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592531"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a>Pradėti su elektroninės sąskaitos priedo paslaugų administravimu

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš užbaigdami procedūrą šioje temoje, būtina atlikti tolesnes išankstines sąlygas:

- Turite turėti savo „Microsoft Dynamics Lifecycle Services“ (LCS) paskyrą.
- Turite turėti LCS projektą, kuris apima versiją 10.0.17 ar vėlesnę „Microsoft Dynamics 365 Finance“ ir „Dynamics 365 Supply Chain Management“. Taip pat, šios programos turi būti talpintos vienoje iš tolesnių „Azure“ geografijų:

    - Rytų JAV
    - Vakarų JAV
    - Šiaurės ES
    - Vakarų ES

- Turite turėti savo „Dynamics 365 Regulatory Configuration Services“ (RCS) paskyrą.
- Turite aktyvuoti globalizavimo funkciją savo RCS paskyrai funkcijos valdyme. Dėl daugiau informacijos, žr. [„Regulatory Configuration Services“ (RCS) - globalizavimo funkcijos](rcs-globalization-feature.md).
- Turite sukurti pagrindinę vertę ir laikymo paskyrą „Azure“. Daugiau informacijos žr. [Kurti „Azure” saugyklos paskyrą ir talpyklos raktą](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a>Diekite priedą mikro paslaugoms „Lifecycle Services“

1. Prisijunkite prie jūsų LCS abonemento.
2. Rinkitės **Išankstinis funkcijos valdymo** plytelę.
3. Skyriuje **Viešo išankstinio rodymo funkcijos** rinkitės **el. sąskaitų paslaugos**.
4. Įsitikinkite, kad **Išankstinės funkcijos įjungimas** parinktis yra nustatyta į **Taip**.
5. LCS skelbimų lentoje pasirinkite LCS diegimo projektą. Turi būti vykdomas LCS projektas.
7. „FastTab“ skirtuke **Aplinkos papildiniai** pasirinkite **Diegti naują papildinį**.
8. Pasirinkite **El. SF paslaugos** ir laukelyje **AAD programos ID** įveskite **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Tai – fiksuota vertė.
10. Lauke **AAD nuomotojo ID** įveskite savo „Azure” prenumeratos abonemento savininko ID.
11. Peržiūrėkite sąlygas ir nuostatas, o tada pažymėkite žymės langelį.
12. Pasirinkti **Diegti**.


## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a>Nustatykite parametrus RCS integravimui su elektroninės sąskaitos priedu

1. Prisijunkite prie jūsų RCS abonemento.
2. Darbo srities **Elektroninės ataskaitos** dalyje **Susiję saitai** pasirinkite **Elektroninių ataskaitų parametrai**.
3. Skirtuke **el. sąskaitų paslaugos** laukelyje **Paslaugų galinis taškas URI** laukelyje, įveskite paslaugų galinį tašką „Azure“ geogarfijoje kaip parodyta šioje lentelėje.

    | Duomenų centro „Azure“ geografija | Paslaugos galinio punkto URI                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Rytų JAV                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | Vakarų JAV                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Šiaurės ES                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Vakarų ES                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. Patvirtinkite, kad **Programos Id** laukelis yra nustatytas į **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Ši vertė yra fiksuota vertė.
5. Laukelyje **LCS aplinkos Id** įveskite savo LCS prenumeratos sąskaitos ID.
6. Pasirinkite **Įrašyti** ir uždarykite puslapį.

## <a name="create-key-vault-secret"></a>Kurkite pagrindinį raktą

1. Prisijunkite prie jūsų RCS abonemento.
2. Darbo srities **Globalizacijos funkcijos** dalyje **Aplinka** pasirinkite plytelę **Elektroninių SF išrašymo priedas**.
3. Puslapyje **Aplinkos nustatymai** veiksmų juostoje rinkitės **Paslaugų aplinka** ir tada rinkitės **Pagrindiniai parametrai**.
4. Pasirinkite **Naujas** jei norite sukurti rakto saugyklos slaptą.
5. **Pavadinimas** laukelyje įveskite pagrindinės talpyklos pavadinimą. Lauke **Aprašas** įveskite aprašą.
6. Lauke **Rakto talpyklos URI** įklijuokite slaptą kodą iš „Azure Key Vault".
7. Pasirinkite **Įrašyti**.

## <a name="create-storage-account-secret"></a>Kurti Saugyklos paskyros raktą

1. Eikite į **Sistemos administravimas** > **Sąranka** > **Raktų saugyklos parametrai** ir pasirinkite slaptą raktų saugyklą.
2. Skyriuje **Sertifikatai** pasirinkite **Pridėti**.
3. Laukelyje **Pavadinimas** įveskite slaptos saugyklos paskyros pavadinimą ir laukelyje **Aprašas** įveskite aprašą.
4. Lauke **Tipas** pasirinkite **Sertifikatas**.
5. Pasirinkite **Įrašyti** ir uždarykite puslapį.

## <a name="create-a-digital-certificate-secret"></a>Slapto skaitmeninio sertifikato kūrimas

1. Eikite į **Sistemos administravimas** > **Sąranka** > **Raktų saugyklos parametrai** ir pasirinkite slaptą raktų saugyklą.
2. Skyriuje **Sertifikatai** pasirinkite **Pridėti**.
3. Laukelyje **Pavadinimas** įveskite slapto skaitmeninio sertifikato pavadinimą ir laukelyje **Aprašas** įveskite aprašą.
4. Lauke **Tipas** pasirinkite **Sertifikatas**.
5. Pasirinkite **Įrašyti** ir uždarykite puslapį.

## <a name="create-an-electronic-invoicing-add-on-environment"></a>Elektroninių SF išrašymo priedo aplinkos kūrimas

1. Prisijunkite prie jūsų RCS abonemento.
2. Darbo srities **Globalizacijos funkcijos** dalyje **Aplinka** pasirinkite plytelę **Elektroninių SF išrašymo priedas**.

## <a name="create-a-service-environment"></a>Aptarnavimo aplinkos kūrimas

1. Puslapyje **Aplinkos nustatymai**, veiksmų juostoje pasirinkite **Aptarnavimo aplinka**.
2. Pasirinkite **Nauja**, kad sukurtumėte naują paslaugų aplinką.
3. **Pavadinimas** laukelyje įveskite vietos elektroninių sąskaitų aplinkos pavadinimą. Lauke **Aprašas** įveskite aprašą.
4. **Talpyklos SAS atpažinimo rakto** lauke pasirinkite slaptos saugyklos paskyros, kuri turi būti naudojama, jei norima autentifikuoti prieigą prie saugyklos sąskaitos, pavadinimą.
5. Skyriuje **Vartotojai** rinkitės **Įtraukti** norėdami įtraukti vartotoją, kuriam leidžiama pateikti elektronines SF naudojant aplinką, ir taip pat prisijungti prie saugojimo sąskaitos.
6. Lauke **Vartotojo ID** įveskite vartotojo pravardę. Lauke **El. paštas** įveskite vartotojo el. pašto adresą.
7. Pasirinkite **Įrašyti**.
8. Jei jūsų šalies ar regiono konkrečios sąskaitos reikalauja sertifikatų grandinės siekiant taikyti skaitmeninį parašą, veiksmų juostoje rinkitės **Pagrindiniai talpyklos parametrai**, tada rinkitės **Sertifikatų grandinė** ir alikite šiuos žingsnius:

    1. Pasirinkite **Naujas** tam, kad sukurtumėte sertifikatų grandinę.
    2. **Pavadinimas** laukelyje įveskite sertifikato grandinės pavadinimą. Lauke **Aprašas** įveskite aprašą.
    3. Skyriuje **Sertifikatai** pasirinkite **Įtraukti** kad į grandinę būtų įtrauktas sertifikatas.
    4. Norėdami pakeisti **Aukštyn** arba **Žemyn** poziciją sertifikato grandinėje.
    5. Pasirinkite **Įrašyti** ir uždarykite puslapį.
    6. Uždarykite puslapį.
9. Puslapyje **Paslaugų aplinka** veiksmų juostoje rinkitės **Publikuoti** kad publikuotumėte aplinką debesyje. Vertė **Būsena** laukelyje pakeičiama į **Publikuota**.

## <a name="create-a-connected-application"></a>Kurkite sujungtą programą

1. **Aplinkos nustatymų** puslapyje, veiksmų juostoje pasirinkite **Sujungtos programos**.
2. Pasirinkite **Naujas**, kad sujungtumėte programą.
3. **Pavadinimas** laukelyje įveskite sujungiamos programos pavadinimą.
4. Laukelyje **Programa** įveskite „Finance and Supply Chain Management“ sujungiamos aplinkos URL.
4. Laukelyje **Nuomotojo** įveskite „Finance and Supply Chain Management“ nuomotojo aplinką.
5. Pasirinkite **Įrašyti**.
6. Veiksmų srityje pasirinkite **Tikrinti ryšį** norėdami patikrinti ryšį su aplinka. Tada uždarykite puslapį.

## <a name="link-connected-applications-to-environments"></a>Susieti prie aplinkos prijungtas programas

1. **Aplinkos nustatymų** puslapyje pasirinkite **Naujas** jei norite aplinkai priskirt prijungtą programą.
2. Laukelyje **Prijungta programa** pasirinkite sujungtą programą.
3. Lauke **Aptarnavimo aplinka** pasirinkite darbo užsakymo aptarnavimo aplinką.
4. Pasirinkite **Įrašyti** ir uždarykite puslapį.

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a>Elektroninių SF išrašymo priedo integravimo nustatymas „Finance and Supply Chain Management”

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>Elektroninių SF išrašymo priedo integravimo funkcijos įjungimas

1. Prisijunkite prie savo „Finance and Supply Chain Management“ elemento.
2. Darbo srityje **Funkcijų valdymas** ieškokite naujos funkcijos **Elektroninių SF išrašymo priedo integravimas**. Jei ši funkcija nebus rodoma puslapyje, pasirinkite **Tikrinti, ar yra naujinimų**.
3. Pasirinkite funkciją ir tada pasirinkite **Įjungti dabar**.

### <a name="set-up-the-service-endpoint-url"></a>Paslaugos galinio punkto URL nustatymas

1. Eikite į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**.
2. Skirtuke **Pateikimo paslaugos** laukelyje **Aptarnavimo galutinio taško URL** įveskite atitinkamą „Azure" geografijos paslaugos galinį punktą, kaip parodyta pateiktoje lentelėje.

    | Duomenų centras „Azure" geografijoje | Paslaugos galinio punkto URL                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Rytų JAV                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | Vakarų JAV                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Šiaurės ES                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Vakarų ES                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. Laukelyje **Aplinka** įveskite elektroninės sąskaitos priedo aplinką.
4. Pasirinkite **Įrašyti** ir uždarykite puslapį.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
