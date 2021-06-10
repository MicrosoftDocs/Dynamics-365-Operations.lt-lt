---
title: Darbo su elektroninių SF priedu tarnybos administravimui pradžia
description: Ši tema paaiškina, kaip pradėti su elektroninės sąskaitos priedo paslaugų administravimu.
author: gionoder
ms.date: 05/24/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 7c4d69edd4a8f7c7acc2ac1bc22c1ba6eaba25ae
ms.sourcegitcommit: 90a289962598394ad98209026013689322854b7b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/24/2021
ms.locfileid: "6092411"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a>Darbo su elektroninių SF priedu tarnybos administravimui pradžia

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš užbaigdami procedūrą šioje temoje, būtina atlikti tolesnes išankstines sąlygas:

- Turite turėti savo „Microsoft Dynamics Lifecycle Services“ (LCS) paskyrą.
- Turite turėti LCS projektą, kuris apima versiją 10.0.17 ar vėlesnę „Microsoft Dynamics 365 Finance“ ir „Dynamics 365 Supply Chain Management“. Taip pat, šios programos turi būti talpintos vienoje iš tolesnių „Azure“ geografijų:

    - Jungtinės Valstijos
    - Europa
    - Jungtinė Karalystė
    - Azija

- Turite turėti savo „Dynamics 365 Regulatory Configuration Services“ (RCS) paskyrą.
- Turite aktyvuoti globalizavimo funkciją savo RCS paskyrai funkcijos valdyme. Dėl daugiau informacijos, žr. [„Regulatory Configuration Services“ (RCS) - globalizavimo funkcijos](rcs-globalization-feature.md).
- Turite sukurti pagrindinę vertę ir laikymo paskyrą „Azure“. Daugiau informacijos žr. [Kurti „Azure” saugyklos paskyrą ir talpyklos raktą](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Diekite priedą mikro paslaugoms „Lifecycle Services“

1. Prisijunkite prie savo LCS paskyros ir LCS projekto ataskaitų srityje pasirinkite LCS projektą.
2. Projekto aplinkos ataskaitų srityje pasirinkite LCS diegimo projektą. Projektas, kurį pasirinkote, turi būti vykdomas.
3. Skirtuko **„Power Platform“ integravimas** lauko **Aplinkos papildiniai** grupėje Pasirinkite **Diegti naują priedą**.
4. Rinkitės **SF siuntimas**.
5. Lauke **AAD programos ID** įveskite **„091c98b0-a1c9-4b02-b62c-7753395ccabe**. Tai – fiksuota vertė.
6. Lauke **AAD nuomotojo ID** įveskite savo „Azure” prenumeratos abonemento savininko ID.
7. Peržiūrėkite sąlygas ir nuostatas, o tada pažymėkite žymės langelį.
8. Pasirinkti **Diegti**.


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Nustatykite parametrus RCS integravimui su elektroninės sąskaitos priedu

1. Prisijunkite prie jūsų RCS abonemento.
2. Darbo srities **Elektroninės ataskaitos** dalyje **Susiję saitai** pasirinkite **Elektroninių ataskaitų parametrai**.
3. Skirtuke **el. sąskaitų paslaugos** laukelyje **Paslaugų galinis taškas URI** laukelyje, įveskite paslaugų galinį tašką „Azure“ geogarfijoje kaip parodyta šioje lentelėje.

    | Duomenų centro „Azure“ geografija | Paslaugos galinio punkto URI                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Jungtinės Valstijos              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Europa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Jungtinė Karalystė             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Azija                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

4. Patvirtinkite, kad **Programos Id** laukelis yra nustatytas į **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Ši vertė yra fiksuota vertė.
5. Laukelyje **LCS aplinkos Id** įveskite savo aplinkos LCS prenumeratos ID.
6. Pasirinkite **Įrašyti** ir uždarykite puslapį.

## <a name="create-key-vault-references"></a>Raktų saugyklos nuorodų kūrimas

1. Prisijunkite prie jūsų RCS abonemento.
2. Darbo srities **Globalizacijos funkcijos** dalyje **Aplinka** pasirinkite plytelę **Elektroninių SF išrašymo priedas**.
3. Puslapyje **Aplinkos nustatymai** veiksmų juostoje rinkitės **Paslaugų aplinka** ir tada rinkitės **Pagrindiniai parametrai**.
4. Pasirinkite **Naujas** jei norite sukurti rakto saugyklos nuorodą.
5. **Pavadinimas** laukelyje įveskite pagrindinės talpyklos nuorodą. Lauke **Aprašas** įveskite aprašą.
6. Lauke **Rakto talpyklos URI** įklijuokite slaptą nuorodos saugyklą iš „Azure Key Vault". Daugiau informacijos žr. [Kurti „Azure” saugyklos paskyrą ir talpyklos raktą](e-invoicing-create-azure-storage-account-key-vault.md).
7. Pasirinkite **Įrašyti**.

## <a name="create-storage-account-secret"></a>Kurti Saugyklos paskyros raktą

1. Puslapyje **Aplinkos nustatymai** veiksmų juostoje rinkitės **Paslaugų aplinka** > **Pagrindiniai raktų parametrai**.
2. Pasirinkite rakto **Saugyklos nuorodą** ir skyriuje  **Sertifikatai** pasirinkite **Įtraukti**.
3. **Pavadinimas** laukelyje įveskite tą patį talpyklos paskyros pavadinimą. Daugiau informacijos žr. [Kurti „Azure” saugyklos paskyrą ir talpyklos raktą](e-invoicing-create-azure-storage-account-key-vault.md).
4. Lauke **Aprašas** įveskite aprašą.
5. Lauke **Tipas** pasirinkite **Raktas**.
6. Pasirinkite **Įrašyti** ir uždarykite puslapį.

## <a name="create-a-digital-certificate-secret"></a>Slapto skaitmeninio sertifikato kūrimas

1. Puslapyje **Aplinkos nustatymai** veiksmų juostoje rinkitės **Paslaugų aplinka** ir tada rinkitės **Pagrindiniai parametrai**.
2. Pasirinkite rakto **Saugyklos nuorodą** ir tada skyriuje  **Sertifikatai** pasirinkite **Įtraukti**.
3. **Pavadinimas** laukelyje įveskite tą patį skaitmeninį sertifikato raktą. Daugiau informacijos žr. [Kurti „Azure” saugyklos paskyrą ir talpyklos raktą](e-invoicing-create-azure-storage-account-key-vault.md).
4. Lauke **Aprašas** įveskite aprašą.
5. Lauke **Tipas** pasirinkite **Sertifikatas**.
6. Pasirinkite **Įrašyti** ir uždarykite puslapį.

## <a name="create-a-service-environment"></a>Aptarnavimo aplinkos kūrimas

1. Prisijunkite prie jūsų RCS abonemento.
2. Darbo srities **Globalizacijos funkcijos** dalyje **Aplinka** pasirinkite plytelę **Elektroninių SF išrašymo priedas**.
3. Puslapyje **Aplinkos nustatymai**, veiksmų juostoje pasirinkite **Aptarnavimo aplinka**.
4. Pasirinkite **Nauja**, kad sukurtumėte naują paslaugų aplinką.
5. **Pavadinimas** laukelyje įveskite vietos elektroninių sąskaitų aplinkos pavadinimą. Lauke **Aprašas** įveskite aprašą.
6. **Talpyklos SAS atpažinimo rakto** lauke pasirinkite slaptos saugyklos paskyros, kuri turi būti naudojama, jei norima autentifikuoti prieigą prie saugyklos sąskaitos, pavadinimą.
7. Skyriuje **Vartotojai** rinkitės **Įtraukti** norėdami įtraukti vartotoją, kuriam leidžiama pateikti elektronines SF naudojant aplinką, ir taip pat prisijungti prie saugojimo sąskaitos.
8. Lauke **Vartotojo ID** įveskite vartotojo pravardę. Lauke **El. paštas** įveskite vartotojo el. pašto adresą.
9. Pasirinkite **Įrašyti**.
10. Jei jūsų šalies ar regiono konkrečios sąskaitos reikalauja sertifikatų grandinės siekiant taikyti skaitmeninį parašą, veiksmų juostoje rinkitės **Pagrindiniai talpyklos parametrai**, tada rinkitės **Sertifikatų grandinė** ir alikite šiuos žingsnius:
    1. Pasirinkite **Naujas** tam, kad sukurtumėte sertifikatų grandinę.
    2. **Pavadinimas** laukelyje įveskite sertifikato grandinės pavadinimą. Lauke **Aprašas** įveskite aprašą.
    3. Skyriuje **Sertifikatai** pasirinkite **Įtraukti** kad į grandinę būtų įtrauktas sertifikatas.
    4. Norėdami pakeisti **Aukštyn** arba **Žemyn** poziciją sertifikato grandinėje.
    5. Pasirinkite **Įrašyti** ir uždarykite puslapį.
    6. Uždarykite puslapį.
11. Puslapyje **Paslaugų aplinka** veiksmų juostoje rinkitės **Publikuoti** kad publikuotumėte aplinką debesyje. Vertė **Būsena** laukelyje pakeičiama į **Publikuota**.

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

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a>Elektroninių SF išrašymo priedo integravimo nustatymas „Finance and Supply Chain Management”

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a>Elektroninių SF išrašymo priedo integravimo funkcijos įjungimas

1. Prisijunkite prie savo „Finance and Supply Chain Management“ elemento.
2. Darbo srityje **Funkcijų valdymas** ieškokite naujos funkcijos **Elektroninių SF išrašymo priedo integravimas**. Jei ši funkcija nebus rodoma puslapyje, pasirinkite **Tikrinti, ar yra naujinimų**.
3. Pasirinkite funkciją ir tada pasirinkite **Įjungti dabar**.

### <a name="set-up-the-service-endpoint-url"></a>Paslaugos galinio punkto URL nustatymas

1. Eikite į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**.
2. Skirtuke **Pateikimo paslaugos** laukelyje **Aptarnavimo galutinio taško URL** įveskite atitinkamą „Azure" geografijos paslaugos galinį punktą, kaip parodyta pateiktoje lentelėje.

    | Duomenų centro „Azure“ geografija | Paslaugos galinio punkto URI                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Jungtinės Valstijos              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Europa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Jungtinė Karalystė             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Azija                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Laukelyje **Aplinka** įveskite paslaugų aplinkos publikuotos elektroninėse sąskaitos pavadinimą
4. Pasirinkite **Įrašyti** ir uždarykite puslapį.

### <a name="enable-flighting-keys"></a>Įgalinti skrydžio raktus

Įgalinkite "Microsoft Dynamics 365 Finance“ ar "Microsoft Dynamics 365 Supply Chain Management“ 10.0.17 ar ankstesnių versijų skrydžio raktus. 
1. Vykdykite toliau pateiktą SQL komandą.

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)

2. Atlikite IISreset komandą visiems AOS.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
