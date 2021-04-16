---
title: Darbo su elektroninių SF priedu Egiptui pradžia
description: Šioje temoje pateikiama informacija, kuri padės jums pradėti naudotis Egipto elektroninių SF išrašymo priedu „Finance and Supply Chain Management”.
author: gionoder
ms.date: 03/29/2021
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
ms.openlocfilehash: f6175a50a88d2d636bfafc5988265b8657630758
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840201"
---
# <a name="get-started-with-electronic-invoicing-for-egypt"></a>Darbo su elektroninių SF priedu Egiptui pradžia

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Šioje temoje pateikiama informacija, kuri padės jums pradėti naudotis elektroninių SF išrašymo priedu Egiptui. Šiuose temos vadovuose pateikiama informacija padės jums atlikti konfigūravimo veiksmus, priklausančius nuo „Regulatory Configuration Services” (RCS), ir papildyti temoje [Darbo su elektroniniu SF išrašymo priedu pradžia](e-invoicing-get-started.md) aprašytus veiksmus.

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Šaliai skirta Egipto elektros sąskaitos (EG) elektroninių SF išrašymo priemonės konfigūracija

Kai kurie Brazilijos **Egipto elektroninių sąskaitų (EG) SF priemonės** su numatytosiomis vertėmis. Prieš diegdami elektroninio SF išrašymo funkciją aptarnavimo aplinkoje, peržiūrėkite ir, jei reikia, atnaujinkite vertes, kad geriau atitiktų jūsų verslo operacijos poreikius.

Skyriuje pateikiamas **Elektroninės SF konfigūravimas konkrečiai valstybei elektroninių SF funkcijoje** papildomas aprašas temoje, [Darbo su elektroninių SF išrašymo priedu pradžia](e-invoicing-get-started.md).

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš atlikdami šiame skyriuje nurodytą procedūrą, turite atlikti toliau nurodytus veiksmus.

- Sukurkite slaptą skaitmeninį sertifikatą, kaip aprašyta skyriuje **Slapto skaitmeninio sertifikato kūrimas** skyriuje [Darbo su elektroninių SF priedo pradžios aptarnavimo administravimas](e-invoicing-get-started-service-administration.md). Tikrinimo tikslais Egipto mokesčių inspekcija pateikia specialius tikrinimo skaitmeninius sertifikatus, kuriuos reikia naudoti tik tikrinimo ir sprendimo tikrinimo etapų metu. Daugiau informacijos ieškokite Egipto mokesčių inspekcijos svetainėje, naudodami nuorodą, pateiktą [Egipto el. SF išrašymo SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).

1. RCS pasirinkus dalį **Funkcijos**, esančią darbo srityje **Globalizacijos funkcija**, pasirinkite plytelę **Elektroninių SF priedas**.
2. Puslapyje **Elektroninių SF išrašymo priedo funkcijos** patikrinkite, ar pasirinkta jūsų sukurta elektroninio SF išrašymo funkcija **Egipto elektroninė SF (EG)**.
3. Skirtuke **Versijos** patikrinkite, ar pasirinkta versija **Šablonas**.
4. Tinklelio skirtuke **Nustatymai** pasirinkite funkcijos nustatymą **Pardavimų sąskaita**.
5. Pasirinkite **Redaguoti** ir skirtuke **Veiksmai**, laukelių grupėje **Veiksmai** pasirinkite **Pasirašyti json dokumentą Egipto mokesčių inspekcijai**.
6. Laukelių grupėje **Parametrai** pasirinkite parametrą, **Sertifikato pavadinimas** ir pasirinkite skaitmeninio sertifikato, sukurto naudoti kartu su elektroninių SF išrašymo funkcija, pavadinimą.
7. Laukelių grupėje **Veiksmai** pasirinkite **Integruoti su Egipto ETA tarnyba**. Pakartokite šį veiksmą dviem šio veiksmo pasikartojimais.
8. Laukelių grupėje **Parametrai** pasirinkite **Žiniatinklio tarnybos URL** ir **Prijungti tarnybos URL** ir prireikus peržiūrėkite URL parametrus. Informacijos apie tai, kaip gauti tikrinimo ir produkcijos URL, ieškokite Egipto mokesčių inspekcijos svetainėje, naudodami nuorodą, pateiktą [Egipto el. SF išrašymo SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).
9. Pasirinkite **Išsaugoti** ir uždarykite puslapį.
10. Norėdami įdiegti elektroninių SF išrašymo funkciją į paslaugų aplinką, žr. skyrių [Darbo su elektroninių SF išrašymo priedu pradžia](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Šaliai skirta Egipto elektroninių SF (EG) elektroninių SF išrašymo priemonės programos sąrankos konfigūracija

Prieš diegdami programos nustatymą su „Finance“ ar „Supply Chain Management Connected“ programoje atlikite šiuos veiksmus.

Skyriuje pateikiamas **Elektroninės SF konfigūravimas programos nustatymuose** papildomas aprašas temoje, [Darbo su elektroninių SF išrašymo priedu pradžia](e-invoicing-get-started.md).

1. RCS pasirinkus dalį **Funkcijos**, esančią darbo srityje **Globalizacijos funkcija**, pasirinkite plytelę **Elektroninių SF priedas**.
2. Puslapyje **Elektroninių SF išrašymo priedo funkcijos** patikrinkite, ar pasirinkta elektroninio SF išrašymo funkcija **Egipto elektroninė SF (EG)**.
3. Skirtuke **Versijos** patikrinkite, ar pasirinkta versija **Šablonas**.
4. Skirtuke **Nustatymai** pasirinkite **Programos sąranka** ir laukelyje **Prijungta programa** pasirinkite programą, kurioje norite diegti.
5. Lauke **Lentelės pavadinimas** patikrinkite, ar pasirinktas kliento SF žurnalas.
6. Pasirinkite **Atsakymų tipai**, o tada pasirinkite **Nauja**.
7. Laukelyje **Atsakymo tipas** įveskite „Atsakymas“, o laukelyje **Aprašas** įveskite „Aprašas“.
8. Lauke **Pateikimo būsena** pasirinkite **Laukiama**.
9. Laukelyje **Modelio susiejimas** pasirinkite funkciją **Modelio susiejimas iš atsakymo pranešimo** bei **(Peržiūra) Atsakymo pranešimo importavimo formatas**, o tada pasirinkite **Išsaugoti**.
10. Pasirinkite **Naujas** ir laukelyje **Atsakymo tipas** įveskite „Atsakymo duomenys“ kaip fiksuotą vertę. Lauke **Aprašas** įveskite „Aprašas“.
11. Lauke **Pateikimo būsena** pasirinkite **Laukiama**.
12. Laukelyje **Duomenų objekto pavadinimas** pasirinkite **Pardavimo SF antraščių V2**.
13. Laukelyje **Modelio susiejimas** pasirinkite funkciją **Egipto atsakymo duomenų importavimas** bei **(Peržiūra) Egipto atsakymo duomenų importavimas**, o tada pasirinkite **Išsaugoti**.
14. Norėdami įdiegti programos nustatymą su „Finance“ ar „Supply Chain Management“ programoje, žr. [Pradėta išrašant elektronines SF](e-invoicing-get-started.md).

## <a name="privacy-notice"></a>Privatumo pranešimas

Norint įjungti funkciją **Egipto elektroninė SF (EG)** gali prireikti siųsti ribotus duomenis, įskaitant įmonės mokesčių registravimo ID. Šie duomenys bus persiunčiami mokesčių inspekcijos patvirtintoms trečiųjų šalių agentūroms, kad būtų galima siųsti elektronines SF šiai mokesčių inspekcijai iš anksto nustatytu formatu, reikalingu integravimui su vyriausybės žiniatinklio tarnyba. Administratorius gali įjungti ir išjungti funkciją, nuėjęs į **Organizacijos administravimas** > **Nustatymas** > **Elektroninių dokumentų parametrai**. Skirtuke **Funkcijos** pasirinkite eilutę, kurioje yra funkcija **Egipto elektroninė SF (EG)**, ir tinkamai pasirinkite. Duomenims, importuotiems iš šių išorinių sistemų į šią „Dynamics 365” internetinę paslaugą, taikomos [privatumo nuostatos](https://go.microsoft.com/fwlink/?LinkId=512132). Daugiau informacijos ieškokite skyriuose Privatumo pranešimas, esančiuose konkrečios šalies funkcijos dokumentacijoje.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių SF išrašymo priedo apžvalga](e-invoicing-service-overview.md)
- [Darbo su elektroninių SF priedu tarnybos administravimui pradžia](e-invoicing-get-started-service-administration.md)
- [Darbo su elektroninių SF priedu pradžia](e-invoicing-get-started.md)
- [Kliento elektroninės sąskaitos faktūros Egipte](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
