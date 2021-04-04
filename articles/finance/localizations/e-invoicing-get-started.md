---
title: Darbo su elektroninių SF išrašymo priedu pradžia
description: Šioje temoje pateikiama informacija, kuri padės jums pradėti naudotis elektroninių SF išrašymo priedu „Microsoft Dynamics 365 Finance” ir „Dynamics 365 Supply Chain Management”.
author: gionoder
manager: AnnBe
ms.date: 02/22/2021
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
ms.openlocfilehash: 56227e031f8205836bcae9ce26006fc8091c2863
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592555"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Darbo su elektroninių SF išrašymo priedu pradžia

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija, kuri padės jums pradėti naudotis elektroninių SF išrašymo priedu.

Tolesnėje lentelėje išvardytos elektroninių sąskaitų išrašymo funkcijos ir joms taikomi verslo dokumentai.

| Funkcijos pavadinimas                         | Verslo dokumentas |
|--------------------------------------|-------------------|
| Austrijos elektroninės SF (AT)    | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> |
| Belgijos elektroninė SF (BE)      | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> |
| Brazilijos NF-e (BR)                  | <p>55 iždo dokumento modelis</p><p>Taisymo laiškas</p> |
| Brazilijos NFS-e ABRASF Curitiba (BR) | Paslaugų mokestinis dokumentas |
| Danijos elektroninė SF (DK)       | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> |
| Egipto elektroninė SF (EG)     | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> |
| Estijos elektroninė SF (EE)     | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> |
| Baigti elektroninę sąskaitą (FI)       | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> |
| Prancūzijos elektroninė SF (FR)       | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> |
| Vokietijos elektroninė SF (DE)       | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> |
| SąskaitaPA (IT)                       | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> |
| Meksikos CFDI Interfactura (MX)       | <p>Pardavimo sąskaita faktūra</p><p>Važtaraštis</p><p>Atsargų perkėlimas</p><p>Mokėjimo užbaigimas</p> |
| Nyderlandų elektroninė SF (NL)        | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> |
| Norvegijos elektroninė SF (NO)    | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> |
| Ispanijos elektroninė SF (ES)      | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> |
| PEPPOL elektroninė SF            | <p>Pardavimo sąskaita faktūra</p><p>Projekto SF</p> |

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš užbaigdami procedūrą šioje temoje, būtina atlikti tolesnes išankstines sąlygas:

- Konfigūruokite savo „Regulatory Configuration Service“ (RCS) ir savo „Microsoft Dynamics 365 Finance“ ar „Dynamics 365 Supply Chain Management“ aplinką taip, kad galėtumėte pateikti į elektroninės sąskaitos priedą.
- Kurkite paslaugų aplinką ir publikuokite ją į elektroninės sąskaitos priedą. Dėl daugiau informacijos, žr. [Pradėti su elektroninės sąskaitos priedo paslaugų administravimu](e-invoicing-get-started-service-administration.md).
- Kurti prijungtą programą. Dėl daugiau informacijos, žr. [Pradėti su elektroninės sąskaitos priedo paslaugų administravimu](e-invoicing-get-started-service-administration.md).
- Kurti konfigūruotą tiekėją jūsų organizacijai. Dėl daugiau informacijos, žr. [Kurti konfigūruotą tiekėją ir žymėti juos kaip aktyvius](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Importuoti elektroninės sąskaitos išrašymo funkciją iš „Microsoft“ konfigūravimo tiekėjo 

1. Prisijungti prie savo reguliavimo kongigūravimo paslaugų (RCS) paskyros.
2. Darbo srities **Globalizacijos funkcijos** dalyje **Funkcijos** pasirinkite plytelę **Elektroninių SF išrašymo priedas**.
3. Pasirinkite **Importuoti** ir tada rinkitės **Sinchronizuoti**.
4. Filtruokite **Konfigūravimo tiekėjas** stulpelį pagal sąvoką **„Microsoft“**.
5. Rinkitės elektroninės sąskaitos funkcijos pavadinimą iš lentelės šios temos pradžioje ir tada rinkitės **Importuoti**.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Sukurkite elektroninių sąskaitų funkciją jūsų organizacijos tiekėjuje

1. RCS pasirinkus dalį **Funkcijos**, esančią darbo srityje **Globalizacijos funkcija**, pasirinkite plytelę **Elektroninių SF priedas**.
2. Rinkitės **Įtraukti** > **Pagal esančią funkciją** ir laukelyje **Pavadinimas**, įveskite elektroninės sąskaitos funkcijos pavadinimą.
3. Laukelyje **Aprašas** įveskite funkcijos aprašą.
4. **Pagrindinės funkcijos laukelis**, rinkiės importuojamą elektroninės sąskaitos funkciją iš „Microsoft“ konfigūravimo tiekėjo.
5. Pasirinkite **Sukurti funkciją**.

## <a name="configure-the-electronic-invoicing-feature"></a>Kurkite elektroninės sąskaitos išrašymo funkciją

Priklausomai nuo šalies ar regiono, elektroninės sąskaitos funkcijai gali reikėti papildomo konfigūravimo. 

Konkretiesm žingsniams, žr. „Pradžia“ dokumentus, kurie yra prieinami jūsų šaliai ar regionui.

## <a name="configure-the-application-setup"></a>Konfigūruokite programos nustatymus

1. Rinkitės jūsų sukurtą elektroninės sąskaitos funkciją.
2. Skirtuke **Versija** patvirtinkite **Šablonas** pasirinktą versiją.
3. Skirtuke **Nustatymai“** pasirinkite **Programos nustatymai“**.

    > [!NOTE]
    > Patvirtinkite, kad jūsų organizacija yra nustatyta kaip **Aktyvus** konfigūravimo tiekėjas. Dėl daugiau informacijos, žr. [Kurti konfigūruotą tiekėją ir žymėti juos kaip aktyvius.](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

4. Rinkitės **Funkcijos nustatymai** ir tada rinkitės **Sujungta programa**.
5. Skyriuje **Elektroninio dokumento tipai** rinkitės **Įtraukti**.
6. Kiekvienam funkcijos palaikomam verslo dokumentui, rinkitės ir įveskite **Lentelės pavadinimo** vertę pagal tolesnę lentelę.

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

7. Kiekvienam funkcijos palaikomam verslo dokumentui, rinkitės ir įveskite **Konteksto** vertę pagal tolesnę lentelę.

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

8. Kiekvienam funkcijos palaikomam verslo dokumentui, rinkitės ir įveskite **Verslo dokumento žemėlapio** vertę pagal tolesnę lentelę.

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

Priklausomai nuo šalies ar regiono, elektroninės sąskaitos funkcijai gali reikėti papildomo konfigūravimo.

Konkretiesm žingsniams, žr. „Pradžia“ dokumentus, kurie yra prieinami jūsų šaliai ar regionui.

## <a name="deploy-the-electronic-invoicing-feature"></a>Talpinkite elektroninės sąskaitos išrašymo funkciją

1. Skirtuke **Versijos** rinkitės elektroninės sąskaitos funkcijos versiją, kurią norite talpinti.
2. Pasirinkite **Keisti statusą** \> **Užbaigtas**.
3. Rinkitės **Keiskite būseną** \> **Publikuoti**.
4. Rinkitės **Talpinkite**.
5. Nustatykite **Talpinti į susietą programą** parinktį į **Taip**.
6. Puslapyje **Sujungti programą** rinkitės sujungimą, kuris yra susietas su jūsų elementu „Finance“ ar „Supply Chain Management“.
7. Nustatykite **Talpinti į paslaugų aplinką** parinktį į **Taip**.
8. Laukelyje **Paslaugų aplinka** rinkiės elektroninės sąskaitos priedų paslaugos aplinką, kurioje norite talpinti elektroninių sąskaitų funkciją.
9. Laukelyje **Nuo dienos** rinkitės datą, kai elektroninių sąskaitų funkcija turi įsigalioti elektroninių sąskaitų papildiniuose.
10. Pasirinkite **Gerai**.

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
2. „FastTab“ **Įrašyti siekiant įtraukti** rinkitės **Filtras**.
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
- [Darbo su Brazilijos elektroninių SF išrašymo priedu pradžia](e-invoicing-bra-get-started.md)
- [Darbo su Meksikos elektroninių SF išrašymo priedu pradžia](e-invoicing-mex-get-started.md)
- [Darbo su Italijos elektroninių SF išrašymo priedu pradžia](e-invoicing-ita-get-started.md)
- [Kliento elektroninės sąskaitos Egipte](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
