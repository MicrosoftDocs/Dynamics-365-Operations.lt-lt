---
title: Pradėti naudoti Prancūzijos elektroninių SF išrašymo priedą
description: Šiame straipsnyje pateikiama informacija, kuri padės jums pradėti naudoti Prancūzijos elektroninių SF išrašymo priedą.
author: dkalyuzh
ms.date: 07/07/2022
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-00-02
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: 365316b204b6d76fa6ee6b2402fefee50c8ff3ef
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220717"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-france"></a>Pradėti naudoti Prancūzijos elektroninių SF išrašymo priedą

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Šiame straipsnyje pateikiama informacija, kuri padės jums pradėti nuo Prancūzijos elektroninių SF išrašymo. Tai padės jums atlikti konfigūravimo veiksmus, kurie priklauso nuo šalies kontrolės konfigūracijos tarnybos (RCS). Šie veiksmai papildo veiksmus, aprašytus dalyje [Darbo pradžia, naudojant elektroninės SF išrašymo priedą](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Šaliai konkreti konfigūracija, skirta Prancūzijos Chorus Pro pateikimo (FR) Elektroninių SF išrašymo funkcijai

Norint sukonfigūruoti Prancūzijos **Chorus Pro pateikimo (FR)** elektroninių SF išrašymo priemonę reikia atlikti kai kuriuos veiksmus. Kai kurie konfigūracijos parametrai publikuojami su numatytosiomis reikšmėmis. Šias vertes reikia peržiūrėti ir atnaujinti, kad jos geriau atspindėtų jūsų verslo operacijas.

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradėdami šiame straipsnyje nurodytas procedūras, atlikite šiuos būtinuosius komponentus:

- Susipažinti su elektroninių SF išrašymu. Daugiau informacijos rasite elektroninių SF [išrašymo peržiūra](e-invoicing-service-overview.md).
- Registruoti RCS ir nustatyti elektroninių SF išrašymą. Daugiau informacijos ieškokite šiuose straipsniuose:

    - [Registruotis ir diegti elektroninių SF išrašymo paslaugą](e-invoicing-sign-up-install.md)
    - [Elektroninių SF išrašymo „Azure“ išteklių nustatymas](e-invoicing-set-up-azure-resources.md)
    - [Įdiekite priedą, skirtą „Lifecycle Services“ mikro paslaugoms](e-invoicing-install-add-in-microservices-lcs.md)
    - [Aktyvinti ir nustatyti integravimą](e-invoicing-activate-setup-integration.md) su elektroninių SF išrašymu – Microsoft Dynamics Norėdami aktyvinti integravimą tarp jūsų 365 Dynamics 365 Supply Chain Management finansų ar programos ir elektroninių SF išrašymo paslaugos, naudokite šiame straipsnyje nurodytą informaciją.
    - [NAF kodai ir siret numeriai](emea-fra-naf-codes-siret-numbers.md) bei [Naf kodų ir Siret numerių nustatymas – norėdami savo juridiniuose subjektuose nustatyti NAF ir Siret](tasks/fr-00003-naf-codes-siret-numbers.md) numerius naudokite šiuose straipsnius. 

- Jūsų organizacija turi būti užregistruota dirbti su Chorus Pro. "Microsoft" integravimą su Chorus pro OAuth2 režimu per programos programavimo sąsają (API). Išsamesnės informacijos apie Chorus Pro registravimą ir prašymo aktyvinimą ieškokite oficialioje [dokumentacijoje](https://communaute.chorus-pro.gouv.fr/documentation/help-for-api-developers-in-oauth2-mode/).

    Norėdami registruotis į Chorus Pro, atlikite šiuos veiksmus.

    1. Norėdami pradėti registraciją [, eikite į PISTE portalą](https://piste.gouv.fr/en/component/apiportal/registration). 
    2. Užregistruokite programą ir suaktyvinkite atvirus autorizavimo (OAuth) kredencialus.
    3. Kopijuokite ir įrašykite OAuth kredencialų ir slaptojo rakto kliento ID. Šią informaciją naudosite vėlesniais veiksmais.
    4. Eiti į [Chorus Pro portalą](https://portail.chorus-pro.gouv.fr/aife_csm/?id=aife_enrollment) registruoti. 
    5. Sukurkite techninio abonemento API prieigai. Daugiau informacijos ieškokite techninės [sąskaitos, įtrauktos į API prieigą prie gamybos, sukūrimas](https://communaute.chorus-pro.gouv.fr/documentation/creation-of-a-technical-account-for-an-api-access-in-production/).
    6. Nukopijuokite techninio abonemento vartotojo ID ir slaptažodį. Šią informaciją naudosite vėlesniais veiksmais.

## <a name="country-specific-configuration-of-the-application-setup-for-the-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Šaliai skirta programos nustatymo konfigūravimas Prancūzijos Chorus Pro pateikimo (FR) Elektroninių SF išrašymo funkcijai

Kai kurie Prancūzijos **Chorus Pro pateikimo (FR)** elektroninių SF išrašymo priemonės parametrai publikuojami su numatytosios vertės. Prieš diegiant elektroninių SF išrašymo funkciją tarnybos aplinkoje, peržiūrėkite ir atnaujinkite numatytąsias vertes, kad jos geriau atspindėtų jūsų verslo operacijas.

1. "Azure" rakto saugykloje sukurkite jų slapymetes ir atitinkamas nuorodas. Norėdami gauti daugiau informacijos, žr. [Kliento sertifikatus ir paslapius](e-invoicing-customer-certificates-secrets.md).
2. Importuokite naujausią Prancūzijos **Chorus Pro pateikimo (FR)** globalizavimo funkcijos [versiją, kaip aprašyta importavimo priemonėse iš visuotinės saugyklos](e-invoicing-import-feature-global-repository.md).
3. Sukurkite importuotos globalizavimo funkcijos kopiją ir pasirinkite savo konfigūracijos teikėją. Daugiau informacijos ieškokite Globalizavimo [funkcijos kūrimas](e-invoicing-create-new-globalization-feature.md).
4. Skirtuke **Versijos** patikrinkite, ar pasirinkta versija **Šablonas**.
5. Tinklelio **skirtuke** Nustatymai pasirinkite UBL pardavimo **SF išvestinį funkcijų** nustatymą.
6. Pasirinkite **Redaguoti**, tada pardavimo **galimybių** apdorojimo skirtuke, **pardavimo** galimybių apdorojimo skyriuje, **pasirinkite (Peržiūra) Integruokite su Prancūzijos Chorus Pro** **su veiksmo pavadinimu Prancūzijos Chorus Pro pateikti.**
7. Parametrų **skyriaus** kliento **ID slaptojo vardo** lauke pasirinkite slaptą pavadinimą, kurį sukūrėte kliento ID rakto saugykloje.
8. Kliento slapto **vardo lauke** pasirinkite slaptą pavadinimą, kurį sukūrėte kliento slaptui rakto saugykloje.
9. Lauke Techninio **registravimosi slapto** registravimosi vardas pasirinkite slaptą pavadinimą, kurį sukūrėte techninės sąskaitos prisijungimui rakto saugykloje.
10. Lauke Techninio **slaptažodžio slaptažodžio slaptažodis** pasirinkite techninės sąskaitos slaptažodžio saugos pavadinimą, kurį sukūrėte "Key Vault".
11. Pardavimo galimybių **apdorojimo** skyriaus skirtuke **Apdorojimo** galimybės pasirinkite **Integruoti į Prancūzijos Chorus Pro** **su veiksmo pavadinimu Prancūzijos Chorus Pro užklausos būsena**.
12. Parametrų **skyriaus** kliento **ID slaptojo vardo** lauke pasirinkite slaptą pavadinimą, kurį sukūrėte kliento ID rakto saugykloje.
13. Kliento slapto **vardo lauke** pasirinkite slaptą pavadinimą, kurį sukūrėte kliento slaptui rakto saugykloje.
14. Lauke Techninio **registravimosi slapto** registravimosi vardas pasirinkite slaptą pavadinimą, kurį sukūrėte techninės sąskaitos prisijungimui rakto saugykloje.
15. Lauke Techninio **slaptažodžio slaptažodžio slaptažodis** pasirinkite techninės sąskaitos slaptažodžio saugos pavadinimą, kurį sukūrėte "Key Vault".
16. Pasirinkite **Įrašyti** ir uždarykite puslapį.
17. UBL **projekto SF išvestinės funkcijos nustatymo,** UBL pardavimo kredito pažymos išvestinio funkcijos nustatymo ir **UBL** **projekto kredito pažymos išvestinės funkcijos nustatymo pakartokite veiksmus nuo 6 iki 16.**

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių SF išrašymo priedo apžvalga](e-invoicing-service-overview.md)
- [Darbo su elektroninių SF priedu tarnybos administravimui pradžia](e-invoicing-get-started-service-administration.md)
- [Darbo su elektroninių SF priedu pradžia](e-invoicing-get-started.md)
