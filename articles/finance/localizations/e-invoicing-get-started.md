---
title: Darbo su elektroninių SF priedu pradžia
description: Šioje temoje pateikiama informacija, kuri padės jums pradėti naudotis elektroninių SF išrašymo priedu „Microsoft Dynamics 365 Finance” ir „Dynamics 365 Supply Chain Management”.
author: gionoder
ms.date: 08/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 3ba0b68ee61b130b8d0304d0bac6d1d720af8139
ms.sourcegitcommit: baf82100f0aa7d5f5f47c7f54bc155d8a07beab5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463845"
---
# <a name="get-started-with-electronic-invoicing"></a>Darbo su elektroninių SF priedu pradžia

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija, kuri padės jums pradėti naudotis elektroninių SF išrašymo priedu Egiptui. Ši tema padės jums atlikti bendrus konfigūravimo veiksmus „Regulatory Configuration Services“ (RCS) ir pateikia veiksmus, kuriuos turite atlikti norėdami pateikti verslo dokumentus ir peržiūrėti „Dynamics 365 Finance“ apdorojimo rezultatus.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš užbaigdami procedūrą šioje temoje, būtina atlikti tolesnes išankstines sąlygas:

- Konfigūruokite „Microsoft Dynamics Lifecycle Services“ (LCS), reguliavimo konfigūracijos tarnybą (RCS) ir „Microsoft Dynamics 365 Finance“ arba „Dynamics 365 Supply Chain Management“ aplinką. Dėl daugiau informacijos, žr. [Pradėti su elektroninės sąskaitos priedo paslaugų administravimu](e-invoicing-get-started-service-administration.md).
- Kurti konfigūruotą tiekėją jūsų organizacijai. Dėl daugiau informacijos, žr. [Kurti konfigūruotą tiekėją ir žymėti juos kaip aktyvius](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Importuoti elektroninės sąskaitos išrašymo funkciją iš „Microsoft“ konfigūravimo tiekėjo 

1. Prisijungti prie savo reguliavimo kongigūravimo paslaugų (RCS) paskyros.
2. RCS pasirinkus dalį **Visuotinės funkcijos**, esančią darbo srityje **Funkcijos**, pasirinkite plytelę **Elektroninių SF priedas**.
3. Pasirinkite **Importuoti** ir tada rinkitės **Sinchronizuoti**.
4. Filtruokite **Konfigūravimo tiekėjas** stulpelį pagal sąvoką **„Microsoft“**.
5. Rinkitės elektroninės sąskaitos funkcijos pavadinimą iš lentelės šios temos pradžioje ir tada rinkitės **Importuoti**.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Sukurkite elektroninių sąskaitų funkciją jūsų organizacijos tiekėjuje

1. RCS pasirinkus dalį **Funkcijos**, esančią darbo srityje **Globalizacijos funkcijos**, pasirinkite plytelę **Elektroninių SF priedas**.
2. Rinkitės **Įtraukti** > **Pagal esančią funkciją** ir laukelyje **Pavadinimas**, įveskite elektroninės sąskaitos funkcijos pavadinimą.
3. Laukelyje **Aprašas** įveskite funkcijos aprašą.
4. **Pagrindinės funkcijos laukelis**, rinkiės importuojamą elektroninės sąskaitos funkciją iš „Microsoft“ konfigūravimo tiekėjo.
5. Pasirinkite **Sukurti funkciją**.

## <a name="country-specific-configuration-for-electronic-invoicing-feature"></a>Šaliai skirta elektroninių SF išrašymo priemonės konfigūracija

Priklausomai nuo šalies ar regiono, elektroninės sąskaitos funkcijai gali reikėti konkretaus konfigūravimo. 

Konkretiesm žingsniams, žr. „Pradžia“ dokumentus, kurie yra prieinami jūsų šaliai ar regionui.

## <a name="import-the-model-mapping-configurations-from-electronic-reporting"></a>Importuokite modelių susiejimo konfigūracijas iš elektroninių ataskaitų

1. RCS pasirinkite elektroninių **ataskaitų darbo** sritį.
2. Iš **„Microsoft“** konfigūravimo tiekėjų sąrašo, rinkitės **Saugyklos**.
3. Pasirinkite **Visuotinis** ir Veiksmų srityje pasirinkite **Atidaryti**.
4. Importuoti modelio susiejimo konfigūracijas pagal šią lentelę pagal priemonės pavadinimą.

| Funkcijos pavadinimas                         | Modelio susiejimo konfigūracija |
|--------------------------------------|-----------------------------|
| Austrijos elektroninės SF (AT)    | <p>Kliento SF konteksto modelis</p><p>Sąskaitos faktūros modelis</p> |
| Belgijos elektroninė SF (BE)      | <p>Kliento SF konteksto modelis</p><p>Sąskaitos faktūros modelis</p> |
| Brazilijos NF-e (BR)                  | <p>Kliento SF konteksto modelis</p><p>Finansinis dokumentas</p><p>Atsakymo pranešimo modelis</p> |
| Brazilijos NFS-e ABRASF Curitiba (BR) | <p>Kliento SF konteksto modelis</p><p>Finansinis dokumentas</p><p>Atsakymo pranešimo modelis</p> |
| Danijos elektroninė SF (DK)       | <p>Kliento SF konteksto modelis</p><p>Sąskaitos faktūros modelis</p> |
| Egipto elektroninė SF (EG)     | <p>Kliento SF konteksto modelis</p><p>Sąskaitos faktūros modelis</p><p>Atsakymo pranešimo modelis</p> |
| Estijos elektroninė SF (EE)     | <p>Kliento SF konteksto modelis</p><p>Sąskaitos faktūros modelis</p> |
| Baigti elektroninę sąskaitą (FI)       | <p>Kliento SF konteksto modelis</p><p>Sąskaitos faktūros modelis</p> |
| Prancūzijos elektroninė SF (FR)       | <p>Kliento SF konteksto modelis</p><p>Sąskaitos faktūros modelis</p> |
| Vokietijos elektroninė SF (DE)       | <p>Kliento SF konteksto modelis</p><p>Sąskaitos faktūros modelis</p> |
| SąskaitaPA (IT)                       | <p>Kliento SF konteksto modelis</p><p>Sąskaitos faktūros modelis</p> |
| Meksikos CFDI Interfactura (MX)       | <p>Kliento SF konteksto modelis</p><p>Sąskaitos faktūros modelis</p><p>Atsakymo pranešimo modelis</p> |
| Nyderlandų elektroninė SF (NL)        | <p>Kliento SF konteksto modelis</p><p>Sąskaitos faktūros modelis</p> |
| Norvegijos elektroninė SF (NO)    | <p>Kliento SF konteksto modelis</p><p>Sąskaitos faktūros modelis</p> |
| Ispanijos elektroninė SF (ES)      | <p>Kliento SF konteksto modelis</p><p>Sąskaitos faktūros modelis</p> |
| PEPPOL elektroninė SF            | <p>Kliento SF konteksto modelis</p><p>Sąskaitos faktūros modelis</p> |


## <a name="configure-the-application-setup"></a>Konfigūruokite programos nustatymus

1. Rinkitės jūsų sukurtą elektroninės sąskaitos funkciją.
2. Skirtuke **Nustatymai“** pasirinkite **Programos nustatymai“**.
3. Laukelyje **Sujungti programą** rinkitės sujungimą, kuris yra susietas su jūsų elementu „Finance“ ar „Supply Chain Management“.
4. Skyriuje **Elektroninio dokumento tipai** rinkitės **Įtraukti**.
5. Pasirinkite ir įveskite **lentelės pavadinimo vertę pagal šią** lentelę.

    | Funkcijos pavadinimas                         | Verslo dokumentas | Lentelės pavadinimas |
    |--------------------------------------|-------------------|------------|
    | Austrijos elektroninės SF (AT)    | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento SF žurnalas</p><p>Projekto SF</p> |
    | Belgijos elektroninė SF (BE)      | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento SF žurnalas</p><p>Projekto SF</p> |
    | Brazilijos NF-e (BR)                  | <p>Iždo dokumentas</p><p>Taisymo laiškas</p> | Iždo dokumentas |
    | Brazilijos NFS-e ABRASF Curitiba (BR) | Paslaugų mokestinis dokumentas | Iždo dokumentas |
    | Danijos elektroninė SF (DK)       | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento SF žurnalas</p><p>Projekto SF</p> |
    | Egipto elektroninė SF (EG)     | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento SF žurnalas</p><p>Projekto SF</p> |
    | Estijos elektroninė SF (EE)     | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento SF žurnalas</p><p>Projekto SF</p> |
    | Baigti elektroninę sąskaitą (FI)       | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento SF žurnalas</p><p>Projekto SF</p> |
    | Prancūzijos elektroninė SF (FR)       | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento SF žurnalas</p><p>Projekto SF</p> |
    | Vokietijos elektroninė SF (DE)       | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento SF žurnalas</p><p>Projekto SF</p> |
    | SąskaitaPA (IT)                       | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF | <p>Kliento SF žurnalas</p><p>Projekto SF</p> |
    | Meksikos CFDI Interfactura (MX)       | <p>Pardavimo sąskaita faktūra</p><p>Važtaraštis</p><p>Atsargų perkėlimas</p><p>Mokėjimo užbaigimas</p> | Kliento SF žurnalas |
    | Nyderlandų elektroninė SF (NL)        | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento SF žurnalas</p><p>Projekto SF</p> |
    | Norvegijos elektroninė SF (NO)    | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento SF žurnalas</p><p>Projekto SF</p> |
    | Ispanijos elektroninė SF (ES)      | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento SF žurnalas</p><p>Projekto SF</p> |
    | PEPPOL elektroninė SF            | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento SF žurnalas</p><p>Projekto SF</p> |

6. Kiekvienam jūsų sukurtos lentelės pavadinimui, pasirinkite ir įveskite konteksto vertę pagal tolesnę lentelę.

    | Funkcijos pavadinimas                         | Verslo dokumentas | Kontekstas |
    |--------------------------------------|-------------------|---------|
    | Austrijos elektroninės SF (AT)    | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento sąskaitos konteksto modelis - Kliento sąskaitos kontekstas</p><p>Kliento sąskaitos konteksto modelis - Projekto sąskaitos kontekstas</p> |
    | Belgijos elektroninė SF (BE)      | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento sąskaitos konteksto modelis - Kliento sąskaitos kontekstas</p><p>Kliento sąskaitos konteksto modelis - Projekto sąskaitos kontekstas</p> |
    | Brazilijos NF-e (BR)                  | <p>Iždo dokumentas</p><p>Taisymo laiškas</p> | <p>Kliento sąskaitos konteksto modelis - Mokesčių dokumento kontekstas</p><p>Kliento sąskaitos konteksto modelis - FD taisymo laiško kontekstas</p> |
    | Brazilijos NFS-e ABRASF Curitiba (BR) | Paslaugų mokestinis dokumentas| Kliento sąskaitos konteksto modelis - Mokesčių dokumento kontekstas |
    | Danijos elektroninė SF (DK)       | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento sąskaitos konteksto modelis - Kliento sąskaitos kontekstas</p><p>Kliento sąskaitos konteksto modelis - Projekto sąskaitos kontekstas</p> |
    | Egipto elektroninė SF (EG)     | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento sąskaitos konteksto modelis - Kliento sąskaitos kontekstas</p><p>Kliento sąskaitos konteksto modelis - Projekto sąskaitos kontekstas</p> |
    | Estijos elektroninė SF (EE)     | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento sąskaitos konteksto modelis - Kliento sąskaitos kontekstas</p><p>Kliento sąskaitos konteksto modelis - Projekto sąskaitos kontekstas</p> |
    | Baigti elektroninę sąskaitą (FI)       | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento sąskaitos konteksto modelis - Kliento sąskaitos kontekstas</p><p>Kliento sąskaitos konteksto modelis - Projekto sąskaitos kontekstas</p> |
    | Prancūzijos elektroninė SF (FR)       | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento sąskaitos konteksto modelis - Kliento sąskaitos kontekstas</p><p>Kliento sąskaitos konteksto modelis - Projekto sąskaitos kontekstas</p> |
    | Vokietijos elektroninė SF (DE)       | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento sąskaitos konteksto modelis - Kliento sąskaitos kontekstas</p><p>Kliento sąskaitos konteksto modelis - Projekto sąskaitos kontekstas</p> |
    | SąskaitaPA (IT)                       | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento sąskaitos konteksto modelis - Kliento sąskaitos kontekstas</p><p>Kliento sąskaitos konteksto modelis - Projekto sąskaitos kontekstas</p> |
    | Meksikos CFDI Interfactura (MX)       | <p>Pardavimo sąskaita faktūra</p><p>Važtaraštis</p><p>Atsargų perkėlimas</p><p>Mokėjimo užbaigimas</p> | Kliento sąskaitos konteksto modelis - Kliento sąskaitos kontekstas |
    | Nyderlandų elektroninė SF (NL)        | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento sąskaitos konteksto modelis - Kliento sąskaitos kontekstas</p><p>Kliento sąskaitos konteksto modelis - Projekto sąskaitos kontekstas</p> |
    | Norvegijos elektroninė SF (NO)    | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento sąskaitos konteksto modelis - Kliento sąskaitos kontekstas</p><p>Kliento sąskaitos konteksto modelis - Projekto sąskaitos kontekstas</p> |
    | Ispanijos elektroninė SF (ES)      | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento sąskaitos konteksto modelis - Kliento sąskaitos kontekstas</p><p>Kliento sąskaitos konteksto modelis - Projekto sąskaitos kontekstas</p> |
    | PEPPOL elektroninė SF            | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Kliento sąskaitos konteksto modelis - Kliento sąskaitos kontekstas</p><p>Kliento sąskaitos konteksto modelis - Projekto sąskaitos kontekstas</p> |

7. Kiekvienam lentelės pavadinimu ir kontekstui, rinkitės ir įveskite verslo dokumentų žemėlapio vertę pagal tolesnę lentelę.

    | Funkcijos pavadinimas                         | Verslo dokumentas | Verslo dokumentų susiejimas |
    |--------------------------------------|-------------------|---------------------------|
    | Austrijos elektroninės SF (AT)    | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Sąskaitos modelio žemėlapis - Projekto sąskaitos kontekstas</p><p>Sąskaitos modelio žemėlapis - Projekto sąskaita</p> |
    | Belgijos elektroninė SF (BE)      | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Sąskaitos modelio žemėlapis - Projekto sąskaitos kontekstas</p><p>Sąskaitos modelio žemėlapis - Projekto sąskaita</p> |
    | Brazilijos NF-e (BR)                  | <p>Iždo dokumentas</p><p>Taisymo laiškas</p> | <p>Mokesčio dokumento žemėlapis - Mokesčio dokumento žemėlapis</p><p>Mokesčio dokumento žemėlapis - taisymo laiško žemėlapis</p> |
    | Brazilijos NFS-e ABRASF Curitiba (BR) | Paslaugų mokestinis dokumentas | Mokesčio dokumento žemėlapis - Mokesčio dokumento žemėlapis |
    | Danijos elektroninė SF (DK)       | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Sąskaitos modelio žemėlapis - Projekto sąskaitos kontekstas</p><p>Sąskaitos modelio žemėlapis - Projekto sąskaita</p> |
    | Egipto elektroninė SF (EG)     | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Sąskaitos modelio žemėlapis - Projekto sąskaitos kontekstas</p><p>Sąskaitos modelio žemėlapis - Projekto sąskaita</p> |
    | Estijos elektroninė SF (EE)     | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Sąskaitos modelio žemėlapis - Projekto sąskaitos kontekstas</p><p>Sąskaitos modelio žemėlapis - Projekto sąskaita</p> |
    | Baigti elektroninę sąskaitą (FI)       | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Sąskaitos modelio žemėlapis - Projekto sąskaitos kontekstas</p><p>Sąskaitos modelio žemėlapis - Projekto sąskaita</p> |
    | Prancūzijos elektroninė SF (FR)       | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Sąskaitos modelio žemėlapis - Projekto sąskaitos kontekstas</p><p>Sąskaitos modelio žemėlapis - Projekto sąskaita</p> |
    | Vokietijos elektroninė SF (DE)       | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Sąskaitos modelio žemėlapis - Projekto sąskaitos kontekstas</p><p>Sąskaitos modelio žemėlapis - Projekto sąskaita</p> |
    | SąskaitaPA (IT)                       | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Sąskaitos modelio žemėlapis - Projekto sąskaitos kontekstas</p><p>Sąskaitos modelio žemėlapis - Projekto sąskaita</p> |
    | Meksikos CFDI Interfactura (MX)       | <p>Pardavimo sąskaita faktūra</p><p>Važtaraštis</p><p>Atsargų perkėlimas</p><p>Mokėjimo užbaigimas</p> | Sąskaitos modelio žemėlapis - Projekto sąskaitos kontekstas |
    | Nyderlandų elektroninė SF (NL)        | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Sąskaitos modelio žemėlapis - Projekto sąskaitos kontekstas</p><p>Sąskaitos modelio žemėlapis - Projekto sąskaita</p> |
    | Norvegijos elektroninė SF (NO)    | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Sąskaitos modelio žemėlapis - Projekto sąskaitos kontekstas</p><p>Sąskaitos modelio žemėlapis - Projekto sąskaita</p> |
    | Ispanijos elektroninė SF (ES)      | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Sąskaitos modelio žemėlapis - Projekto sąskaitos kontekstas</p><p>Sąskaitos modelio žemėlapis - Projekto sąskaita</p> |
    | PEPPOL elektroninė SF            | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> | <p>Sąskaitos modelio žemėlapis - Projekto sąskaitos kontekstas</p><p>Sąskaitos modelio žemėlapis - Projekto sąskaita</p> |


## <a name="country-specific-configuration-of-application-setup"></a>Šaliai konkreti programos nustatymo konfigūracija

Priklausomai nuo šalies ar regiono, programos nustatymo funkcijai gali reikėti konkretaus konfigūravimo. 

Konkretiesm žingsniams, žr. „Pradžia“ dokumentus, kurie yra prieinami jūsų šaliai ar regionui.

## <a name="deploy-the-electronic-invoicing-feature-to-service-environment"></a>Elektroninių SF išrašymo funkcijos talpinimas į aptarnavimo aplinką

1. Skirtuke **Versijos** rinkitės elektroninės sąskaitos funkcijos versiją, kurią norite talpinti.
2. Pasirinkite **Keisti statusą** \> **Užbaigtas**.
3. Rinkitės **Keiskite būseną** \> **Publikuoti**.
4. Rinkitės **Talpinkite**.
5. Nustatykite **Talpinti į susietą programą** parinktį į **Ne**.
6. Nustatykite **Talpinti į paslaugų aplinką** parinktį į **Taip**.
7. Laukelyje **Paslaugų aplinka** rinkitės elektroninės sąskaitos priedų paslaugos aplinką, kurioje norite talpinti elektroninių sąskaitų funkciją.
8. Laukelyje **Nuo dienos** rinkitės datą, kai elektroninių sąskaitų funkcija turi įsigalioti elektroninių sąskaitų papildiniuose.
9. Pasirinkite **Gerai**.

## <a name="deploy-the-electronic-invoicing-feature-to-connected-application"></a>Elektroninių SF išrašymo funkcijos talpinimas į susietą programą

1. Skirtuke **Versijos** rinkitės elektroninės sąskaitos funkcijos versiją, kurią norite talpinti.
2. Rinkitės **Talpinkite**.
3. Nustatykite **Talpinti į susietą programą** parinktį į **Taip**.
4. Laukelyje **Sujungti programą** rinkitės sujungimą, kuris yra susietas su jūsų elementu „Finance“ ar „Supply Chain Management“.
5. Nustatykite **Talpinti į paslaugų aplinką** parinktį į **Ne**.
6. Pasirinkite **Gerai**.

## <a name="turn-on-the-electronic-invoicing-feature-in-finance-or-supply-chain-management"></a>Įsijunkite elektroninės sąskaitos funkciją „Finance“ ar „Supply Chain Management“

1. Prisijunkite prie „Finance“ ar „Supply Chain Management“ ir patikrinkite, ar esate tinkamame juridiniame asmenyje.
2. Eikite į **Organizacijos administravimas** \> **Nustatymas** \> **Elektroninio dokumento parametrai**.
3. Skirtuke **Funkcijos** pasirinkite šalies / regiono funkciją, kad įjungtumėte elektroninių SF išrašymo funkciją, skirtą „Finance” arba „Supply Chain Management”. Toliau esančioje lentelėje pateikiamas elektroninių SF išrašymo priemonių, galimų tam tikrose šalyse / regionuose, sąrašas. 

    | Funkcijos pavadinimas                                          | Šalis/regionas  |
    |-------------------------------------------------------|-----------------|
    | Austrijos elektroninės SF (AT)                     | Austrija         |
    | Belgijos elektroninė SF (BE)                       | Belgija         |
    | CFDI Meksikos elektroninė SF (MX)                  | Meksika          |
    | Danijos elektroninė SF (DK)                        | Danija         |
    | Nyderlandų elektroninė SF (NL)                         | Nyderlandai |
    | Egipto elektroninė SF (EG)                      | Egiptas           |
    | Estijos elektroninė SF (EE)                      | Estija         |
    | Suomijos elektroninė SF (FI)                       | Suomija         |
    | Prancūzijos elektroninė SF (FR)                        | Prancūzija          |
    | Vokietijos elektroninė SF (DE)                        | Vokietija         |
    | Italijos elektroninė SF (IT)                       | Italija           |
    | NF-e federalinės Brazilijos elektroninės sąskaitos (BR)      | Brazilija          |
    | NFS-e – Brazilijos paslaugų (miesto) elektroninė sąskaita faktūra   | Brazilija          |
    | Norvegijos elektroninė SF (NO)                     | Norvegija          |
    | PEPPOL elektroninė SF                             | Bendroji          |
    | Ispanijos elektroninė SF (ES)                       | Ispanija           |

4. Pasirinkite **Įrašyti**.

## <a name="issue-electronic-invoices"></a>Išduoti elektronines sąskaitas

1. Eikite į **Organizacijos administravimas** \> **Periodinė** \> **Elektroniniai dokumentai** \> **Pateikti elektroninius dokumentus**.
2. „FastTab„ **Įtrauktini įrašai** pasirinkite **Filtruoti**.
3. Rinkitės **Įtraukti** tam, kad įtrauktumėte lentelės pavadinimą į laukimo filtrą.
4. Rinkitės lentelę, kurioje yra sąskaitos.

    > [!NOTE]
    > Lentelės pavadinimas turi būti įtrauktas į lentelę [Konfigūruoti programos nustatymus](#configure-the-application-setup) skyrių anksčiau šioje temoje.

5. Rinkitės laukelio pavadinimą iš lentelės, kurioje norite talpinti laukimą.
6. Įveskite lentelės pavadinimą ir laukelio pavadinimos kriterijams, pagal kuriuos laukiama.
7. Kartokite veiksmus 5 ir 6 siekiant įtraukti daugiau laukelių ir kriterijų į laukimą ir tada rinkitės **Gerai**.
8. Pasirinkite **Gerai**.

## <a name="view-submission-logs"></a>Pateikimo žurnalų peržiūra

1. Eikite į **Organizacijos administravimas** \> **Periodinė** \> **Elektroniniai dokumentai** \> **Elektroninio dokumento teikimo žurnalas**.
2. Laukelyje **Dokumento tipas** rinkitės lentelę, kurioje yra sąskaitos.

    > [!NOTE]
    > Lentelės pavadinimas turi būti įtrauktas į lentelę [Konfigūruoti programos nustatymus](#configure-the-application-setup) skyrių anksčiau šioje temoje.

3. Rinkitės sąskaitą tinklelyje ir tada rinkitės **Teirautis** \> **Teikimo išsami informacija**.


## <a name="related-topics"></a>Susijusios temos

- [Elektroninių SF išrašymo priedo apžvalga](e-invoicing-service-overview.md)
- [Darbo su elektroninių SF priedu tarnybos administravimui pradžia](e-invoicing-get-started-service-administration.md)
- [Darbo su elektroninių SF priedu Brazilijai pradžia](e-invoicing-bra-get-started.md)
- [Darbo su elektroninių SF priedu Meksikai pradžia](e-invoicing-mex-get-started.md)
- [Darbo su elektroninių SF priedu Italijai pradžia](e-invoicing-ita-get-started.md)
- [Kliento elektroninės sąskaitos faktūros Egipte](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
