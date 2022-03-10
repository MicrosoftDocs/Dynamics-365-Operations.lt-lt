---
title: Elektroninis SF išrašymas Egipto
description: Šioje temoje pateikiama informacija, kuri padės jums pradėti nuo Elektroninio SF išrašymo Egipto Microsoft ir Programoje Dynamics 365 Finance Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 02/09/2022
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
ms.openlocfilehash: 6fe1dd4254db8b390c17558320a6eaff2b0dcd19
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371361"
---
# <a name="electronic-invoicing-for-egypt"></a>Elektroninis SF išrašymas Egipto

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija, kuri padės jums pradėti naudotis elektroninių SF išrašymo priedu Egiptui. Tai padės jums atlikti konfigūravimo veiksmus, kurie priklauso nuo šalies kontrolės konfigūracijos tarnybos (RCS). Šie veiksmai papildo veiksmus, aprašytus nustatyti elektroninių [SF išrašymą](e-invoicing-set-up-overview.md).

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradėdami šioje temoje nurodytas procedūras, atlikite šiuos būtinuosius komponentus:

- Susipažinti su elektroninių SF išrašymu, kaip aprašyta elektroninių SF [išrašymo apžvalgoje](e-invoicing-service-overview.md).
- Registruoti RCS ir nustatyti elektroninių SF išrašymą. Daugiau informacijos ieškokite šiose temose:

    - [Registruotis ir diegti elektroninių SF išrašymo paslaugą](e-invoicing-sign-up-install.md)
    - [Nustatyti "Azure" išteklius elektroninėms SF išrašyti](e-invoicing-set-up-azure-resources.md)
    - [Diekite priedą mikro paslaugoms „Lifecycle Services“](e-invoicing-install-add-in-microservices-lcs.md)
    
- Suaktyvinkite jūsų "Microsoft" ar programos Dynamics 365 Finance Dynamics 365 Supply Chain Management ir elektroninių SF išrašymo tarnybos integravimą, kaip aprašyta integravimo su elektroninių [SF išrašymu aktyvavimas ir nustatymas](e-invoicing-activate-setup-integration.md).
- Sukurkite skaitmeninio sertifikato slaptą "Azure Key Vault" ir nustatykite jį taip, kaip aprašyta klientų [sertifikatuose ir paslapčių aprašuose](e-invoicing-customer-certificates-secrets.md). Tikrinimo tikslais Egipto mokesčių inspekcija pateikia specialius tikrinimo skaitmeninius sertifikatus, kuriuos reikia naudoti tik tikrinimo ir sprendimo tikrinimo etapų metu. Norėdami gauti daugiau informacijos, eikite į Egipto mokesčių inspekcijos svetainę naudodami [saitą, pateiktą Egipto el. SF išrašymo SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-feature"></a>Šaliai skirta Egipto elektroninės SF (EG) priemonės konfigūracija

Kai kurie Egipto elektroninės SF **(EG)** elektroninių SF išrašymo priemonės parametrai publikuojami su numatytosmis vertėmis. Prieš diegiant elektroninių SF išrašymo funkciją tarnybos aplinkoje, peržiūrėkite numatytąsias vertes ir atnaujinkite jas taip, kad geriau atspindėtų jūsų verslo operaciją.

1. Importuokite naujausią Egipto elektroninės SF **(EG)** globalizavimo funkcijos versiją, kaip aprašyta [importavimo priemonėse iš visuotinės saugyklos](e-invoicing-import-feature-global-repository.md).
2. Sukurkite importuotos globalizavimo funkcijos kopiją ir pasirinkite savo konfigūracijos teikėją, kaip aprašyta [dalyje Globalizavimo funkcijos kūrimas](e-invoicing-create-new-globalization-feature.md).
3. Skirtuke **Versijos** patikrinkite, ar pasirinkta versija **Šablonas**.
4. Tinklelio **skirtuke** Nustatymai pasirinkite išvestinės pardavimo **SF priemonių** nustatymą.
5. Pasirinkite **Redaguoti**.
6. Pardavimo galimybių **apdorojimo** skirtuko dalyje Apdorojimo **galimybės pasirinkite** Pasirašyti **json dokumentą Egipto mokesčių inspekcijai**.
7. Parametrų **skyriuje** pasirinkite Sertifikato **pavadinimas**, tada pasirinkite sukurto skaitmeninio sertifikato pavadinimą.
8. Pardavimo galimybių **apdorojimo skyriuje** pasirinkite Integruoti **su Egipto ETA tarnyba**. Pakartokite šį veiksmą dviem šio veiksmo pasikartojimais.
9. Parametrų **skyriuje** pasirinkite tinklo tarnybos **URL ir** registravimosi **tarnybos URL**. Tada peržiūrėkite URL parametrus. Norėdami gauti tikrinimo ir gamybos URL, [eikite į Egipto mokesčių inspekcijos svetainę naudodami saitą, pateiktą Egipto el. SF išrašymo SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).
10. Pasirinkite **Išsaugoti** ir uždarykite puslapį.
11. Norėdami nustatyti projekto SF išvestą priemonę pakartokite **4–** 10 žingsnius.

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-application-setup"></a>Šalies konfigūracija, skirta Egipto elektroninės SF (EG) programos nustatymui

Yra parametrų, kuriuos reikia nustatyti jūsų finansų arba tiekimo grandinės valdymo aplinkoje. Šį nustatymą galite užbaigti bet kuriose iš dviejų vietų:

- Tiesiogiai savo finansų arba tiekimo grandinės valdymo aplinkoje. Daugiau informacijos ieškokite Elektroninių SF išrašymo [parametrų nustatymas](e-invoicing-set-up-parameters.md).
- In RCS. Elektroninių SF išrašymo priemonės nustatymo srityje galite nurodyti visus parametrus ir įdiegti juos tiesiogiai į savo finansų arba tiekimo grandinės valdymo aplinką, kai diegiate elektroninių SF išrašymo funkciją.

Abiejų pasirinkčių parametrai yra tokie patys. Jei nustatote savo pirmą elektroninio SF išrašymo tarnybos funkciją, rekomenduojame atlikti šiuos veiksmus, kad RCS parametrai būtų nustatyti, o tada juos įdiegti į prijungtą programą.

> [!NOTE]
> Kai kuriose elektroninių SF išrašymo priemonės versijose gali būti iš anksto nustatytas programai bingų parametrų rinkinys, skirtas finansų arba tiekimo grandinės valdymui. Šiuo atveju turėtumėte patikrinti, ar duomenys teisingi. Kitu atveju parametrus nustatykite rankiniu būdu.

1. Raskite sukurtos Egipto **elektroninės SF (EG)** globalizavimo priemonės kopiją.
2. Skirtuke **Versijos** patikrinkite, ar pasirinkta versija **Šablonas**.
3. Skirtuke **Nustatymai“** pasirinkite **Programos nustatymai“**.
4. **Lauke Prijungtos** programos pasirinkite programą, kurioje norite diegti parametrus.
5. Puslapyje Elektroniniai **dokumentų tipai** pasirinkite Įtraukti **, kad** sukurtumėte įrašą.
6. Lauke Lentelės **pavadinimas pridėkite** **CustInvoiceJour**.
7. Konteksto **lauke** pridėkite nuorodą prie kliento SF **konteksto susiejimo** pavadinimo. Konfigūracija yra kliento **SF konteksto modelis**.
8. Elektroninio **dokumento susiejimo** lauke pridėkite nuorodą prie kliento **SF susiejimo** pavadinimo. Konfigūracija yra SF **modelio susiejimas**.
9. Pasirinkite **Įrašyti**.
10. Atsakymų **tipų puslapyje** pasirinkite **Įtraukti**.
11. Lauke **Atsakymo tipas** įveskite **Atsakymas**.
12. Aprašymo **lauke** įveskite Proceso **atsakymas**.
13. Lauke **Pateikimo būsena** pasirinkite **Laukiama**.
14. Modelio susiejimo **lauke** pasirinkite Atsakymo **pranešimo importavimas**. Konfigūracija yra Egipto **atsakymo pranešimo importavimas (EG)**.
15. Pasirinkite **Įrašyti**.
16. Pasirinkite **Įtraukti**.
17. Atsakymo **tipo** lauke įveskite **ResponseData**.
18. Aprašymo **lauke** įveskite Proceso **atsakymo duomenis**.
19. Lauke **Pateikimo būsena** pasirinkite **Laukiama**.
20. Duomenų objekto **pavadinimo lauke pasirinkite** **SalesInvoiceHeaderV2Entity**.
21. Modelio susiejimo **lauke** pasirinkite Atsakymo **duomenų importavimas**. Konfigūracija yra Egipto **atsakymo duomenų importavimo formatas (EG)**.
22. Pasirinkite **Išsaugoti** ir uždarykite puslapį.
23. Uždarykite puslapį.

Norėdami įdiegti funkciją paslaugų aplinkoje ir programos nustatymą prijungtoje finansų arba tiekimo grandinės valdymo programoje, [žr. Užbaigta, paskelbti ir įdiegti globalizavimo funkciją.](e-invoicing-complete-publish-deploy-globalization-feature.md)

## <a name="privacy-notice"></a>Privatumo pranešimas

Įgalinus **Egipto elektroninės SF (EG)** priemonę, gali reikėti siųsti ribotą duomenų dalį. Šie duomenys apima organizacijos mokesčių registracijos ID. Duomenys bus perduoti trečiųjų šalių agentūroms, kurias mokesčių inspekcija įgaliojo siųsti elektronines SF tai mokesčių inspekcijai iš anksto nustatytu formatu, kurio reikia integravimui su vyriausybės žiniatinklio tarnyba. Administratorius gali įjungti ir išjungti funkciją nueięs prie organizacijos **administravimo nustatymo** \> **elektroninio** \> **dokumento parametrų.** Skirtuke **Funkcijos** pasirinkite eilutę, kurioje yra funkcija **Egipto elektroninė SF (EG)**, ir tinkamai pasirinkite. Iš išorinių sistemų importuojamiems į šią "Dynamics 365" interneto paslaugą duomenims taikomas mūsų privatumo [patvirtinimas](https://go.microsoft.com/fwlink/?LinkId=512132). Daugiau informacijos ieškokite konkrečios šalies priemonių dokumentuose skyriuje "Privatumo pranešimas".

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių SF išrašymo priedo apžvalga](e-invoicing-service-overview.md)
- [Darbo su elektroninių SF priedu tarnybos administravimui pradžia](e-invoicing-get-started-service-administration.md)
- [Darbo su elektroninių SF priedu pradžia](e-invoicing-get-started.md)
- [Kliento elektroninės sąskaitos faktūros Egipte](emea-egy-e-invoices.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
