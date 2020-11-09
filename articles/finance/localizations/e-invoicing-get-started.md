---
title: Darbo su elektroninių SF išrašymo priedu pradžia
description: Šioje temoje pateikiama informacija, kuri padės jums pradėti naudotis elektroninių SF išrašymo priedu „Microsoft Dynamics 365 Finance” ir „Dynamics 365 Supply Chain Management”.
author: gionoder
manager: AnnBe
ms.date: 10/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 7b2a3aae43d42060c7fcd9e1ea3db814fc5d8f22
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039851"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Darbo su elektroninių SF išrašymo priedu pradžia

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija, kuri padės jums pradėti naudotis elektroninių SF išrašymo priedu. Pirmiausia ši tema padės atlikti konfigūracijos veiksmus, esančius „Microsoft Dynamics Lifecycle Services” (LCS), „Regulatory Configuration Services” (RCS) ir „Dynamics 365 Finance”. Taip pat joje aprašytas dokumentų pateikimo per paslaugą naudojant „Dynamics 365 Finance” arba „Dynamics 365 Supply Chain Management” procesas. Taip pat sužinosite, kaip interpretuoti pateikimo žurnalus.

## <a name="availability"></a>Prieinamumas

Elektroninių SF išrašymo priedas iš pradžių pasiekiamas keliose šalyse. Priedas palaiko elektroninių SF kūrimą ir toliau nurodytų verslo dokumentų pateikimą.

| Šalis/regionas  | Verslo dokumentas                          |
|-----------------|--------------------------------------------|
| Austrija         | Pardavimo ir projekto SF                 |
| Belgija         | Pardavimo ir projekto SF                 |
| Brazilija          | Elektroninio finansinio dokumento 55 modelis (NF-e) |
| Danija         | Pardavimo ir projekto SF                 |
| Estija         | Pardavimo ir projekto SF                 |
| Suomija         | Pardavimo ir projekto SF                 |
| Prancūzija          | Pardavimo ir projekto SF                 |
| Vokietija         | Pardavimo ir projekto SF                 |
| Italija           | Pardavimo ir projekto SF                 |
| Meksika          | CFDI sąskaita faktūra                               |
| Olandija     | Pardavimo ir projekto SF                 |
| Norvegija          | Pardavimo ir projekto SF                 |
| Ispanija           | Pardavimo ir projekto SF                 |
| Europa          | PEPPOL pardavimo ir projekto SF          |
    
## <a name="licensing"></a>Licencijavimas

Elektroninių SF išrašymo priedą galite naudoti su jūsų dabartine licencija. Norint naudoti paslaugą nereikia papildomų licencijų.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš atlikdami šioje temoje esančius veiksmus, turite įvykdyti toliau nurodytas būtinąsias sąlygas.

- Prieiga prie jūsų LCS abonemento.
- LCS diegimo projektas, kuriame yra „Finance” arba „Supply Chain Management” 10.0.13 ar naujesnė versija.
- Prieiga prie jūsų RCS abonemento.
- Įjunkite jūsų RCS abonemento globalizacijos funkciją naudodami modulį **Funkcijų valdymas**. Daugiau informacijos žr. [„Regulatory Configuration Services“ (RCS) – globalizacijos funkcijos](rcs-globalization-feature.md)
- Sukurkite raktų saugyklos išteklius ir saugyklos abonementą „Azure”. Daugiau informacijos žr. [„Azure” saugyklos abonemento ir „Key Vault” kūrimas](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="overview"></a>Peržiūra

Toliau pateiktame paveikslėlyje nurodyti penki pagrindiniai veiksmai, kuriuos atliksite šioje temoje.

![Penkių šios temos veiksmų apžvalga](media/e-invoicing-services-get-started-overview-5-steps.png)

1. **„Azure” išteklių nustatymas:** konfigūruokite „Azure” saugyklą ir nusiųskite skaitmeninius sertifikatus į „Azure Key Vault”.
2. **LCS nustatymas:** įdiekite „Microservices” papildinį.
3. **RCS nustatymas:** nustatykite aplinką, vartotojo prieigą ir el. SF išrašymo funkcijas.
4. **Kliento nustatymas:** nustatykite ryšį tarp kliento ir elektroninių SF išrašymo priedo ir išjunkite senas funkcijas, skirtas elektroninių dokumentų atsakymams pateikti ir gauti.
5. **SF pateikimas:** pateikite elektroninius dokumentus naudodami elektroninių SF išrašymo priedą ir gaukite atsakymus.

> [!NOTE]
> Kai kurie šios temos konfigūracijos veiksmai yra dažni ir nesusiję su šalimi / regionu. Konkrečių šalių / regionų veiksmai ir nustatymo procedūros yra aprašyti konkrečių šalių / regionų temose.

## <a name="lcs-setup"></a>LCS sąranka

1. Prisijunkite prie jūsų LCS abonemento.
2. Pasirinkite plytelę **Peržiūros funkcijų valdymas** ir laukų grupėje **Viešosios peržiūros funkcijos** pasirinkite **BusinessDocumentSubmission**.
3. Pažymėkite lauką **Peržiūros funkcija įjungta**.
4. Pasirinkite LCS diegimo projektą. Kad galėtumėte pasirinkti projektą, jis turi būti nustatytas ir vykdomas.
5. „FastTab” **Aplinkos papildiniai** pasirinkite **Diegti naują papildinį**.
6. Pasirinkite **Verslo dokumentų pateikimas**.
7. Dialogo lango **Papildinio nustatymas** lauke **AAD programos ID** įveskite **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Ši vertė yra fiksuota vertė.
8. Lauke **AAD nuomotojo ID** įveskite jūsų „Azure” prenumeratos abonemento ID.

    ![Dialogo langas Papildinio nustatymas, esantis LCS](media/e-invoicing-services-get-started-lcs-addin-setup.png)

9. Pažymėkite žymės langelį, kad sutiktumėte su sąlygomis.
10. Pasirinkti **Diegti**.

## <a name="rcs-setup"></a>RCS sąranka

RCS nustatymo metu galėsite atlikti toliau pateiktas užduotis.

1. Nustatykite raktų saugyklą RCS.
2. Nustatykite RCS integravimą su elektroninių SF išrašymo priedo serveriu.
3. Sukurkite jūsų organizacijai skirtą elektroninių SF išrašymo aplinką.

### <a name="set-up-the-key-vault-in-rcs"></a>Raktų saugyklos nustatymas RCS

1. Prisijunkite prie jūsų RCS abonemento.
2. Darbo srities **Globalizacijos funkcijos** dalyje **Aplinkos** pasirinkite plytelę **El. SF išrašymas**.
3. Pasirinkite **Paslaugų aplinkos**.

    ![Paslaugų aplinkų pasirinkimas](media/e-invoicing-services-get-started-select-service-environments.png)

> [!NOTE]
> Parinktis **Prijungtos programos** suteikia prieigą prie automatinio elektroninių SF išrašymo priedo konfigūravimo „Finance” arba „Supply Management” naudojant RCS. Tačiau šiuo metu ši funkcija vis dar kuriama.

4. Veiksmų srityje pasirinkite **„Key Vault” parametrai**.

    ![„Key Vault” parametro pasirinkimas](media/e-invoicing-services-get-started-select-key-vault-parameters.png)

5. Veiksmų srityje pasirinkite **Naujas** , norėdami įtraukti raktų saugyklą.
6. Lauke **Raktų saugyklos URI** įveskite raktų saugyklos išteklių, kuriuos sukonfigūravote „Azure”, atributo reikšmę **DNS pavadinimas**. Informacijos apie tai, kur rasti reikšmę **DNS pavadinimas** , žr. [„Azure” saugyklos abonemento ir „Key Vault” kūrimas](e-invoicing-create-azure-storage-account-key-vault.md).

    ![„Key Vault” URI laukas](media/e-invoicing-services-get-started-enter-key-vault-uri.png)

7. Norėdami įvesti visus skaitmeninių sertifikatų pavadinimus ir raktų saugyklos slaptuosius raktus, kurių reikia norint nustatyti patikimus ryšius, „FastTab” **Sertifikatai** pasirinkite **Įtraukti**. Stulpelyje **Tipas** galite nurodyti, ar tai sertifikatas, ar slaptasis raktas. Abu reikšmių rinkiniai yra sukonfigūruoti raktų saugyklos ištekliuose „Azure”.

    ![Sertifikatų įtraukimas](media/e-invoicing-services-get-started-add-digital-certificates.png)

8. Jei jūsų konkrečios šalies / regiono SF reikia sertifikatų grandinės, kad būtų taikomas skaitmeninis parašas, veiksmų srityje pasirinkite **Sertifikatų grandinė** ir įveskite sertifikatų arba raktų saugyklos slaptųjų raktų, sudarančių grandinę, seką.

### <a name="set-up-the-rcs-integration-with-the-electronic-invoicing-add-on-server"></a>RCS integravimo su elektroninių SF išrašymo priedo serveriu nustatymas

1. Darbo srities **Globalizacijos funkcijos** dalyje **Susiję parametrai** pasirinkite saitą **Elektroninių ataskaitų parametrai**.
2. Pasirinkite **Spustelėkite čia, kad prisijungtumėte prie „Lifecycle Services”**. Jei nenorite prisijungti prie LCS, pasirinkite **Atšaukti**.
3. Skirtuko **El. SF išrašymo paslaugos** lauke **Paslaugos galinio punkto URI** įveskite reikšmę, atsižvelgdami į galimus regionus: `https://businessdocumentsubmission.us.operations365.dynamics.com/` arba `https://businessdocumentsubmission.eu.operations365.dynamics.com/`.
4. Lauke **Programos ID** patvirtinkite, kad nurodytas ID **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Ši vertė yra fiksuota vertė.
5. Lauke **LCS aplinkos ID** įveskite jūsų LCS prenumeratos abonemento ID.

![Elektroninių SF išrašymo priedo parametrų įvedimas](media/e-invoicing-services-get-started-enter-e-invoicing-parameters.png)

### <a name="add-an-electronic-invoicing-add-on-environment"></a>Elektroninių SF išrašymo priedo aplinkos įtraukimas

Galite sukurti skirtingas elektroninių SF išrašymo priedo aplinkas, pvz., kūrimo, tikrinimo ar gamybos aplinkas.

1. Darbo srities **Globalizacijos funkcijos** dalyje **Aplinkos** pasirinkite plytelę **El. SF išrašymas**.
2. Pasirinkite **Nauja** , kad sukurtumėte aplinką.
3. Lauke **Saugyklos SAS atpažinimo ženklo abonementas** įveskite raktų saugyklos slaptojo rakto, kurį sukonfigūravote RCS raktų saugykloje, pavadinimą.

    ![Laukas Saugyklos SAS atpažinimo ženklo abonementas](media/e-invoicing-services-get-started-enter-sas-token-secret.png)

4. „FastTab” **Vartotojai** pasirinkite **Naujas** , kad suteiktumėte vartotojams prieigą prie šios aplinkos.

    ![Paslaugos vartotojų įtraukimas](media/e-invoicing-services-get-started-enter-service-users.png)

5. Veiksmų srityje pasirinkite **Publikuoti** , kad publikuotumėte aplinką elektroninių SF išrašymo priedo serveryje.

    ![Mygtukas Publikuoti](media/e-invoicing-services-get-started-publish-service-environment.png)

### <a name="e-invoicing-feature-setup"></a>El. SF išrašymo funkcijos nustatymas

„El. SF išrašymo funkcija” yra bendras išteklių, sukonfigūruotų ir publikuotų siekiant naudoti elektroninių SF išrašymo priedo serverį, pavadinimas. El. SF išrašymo funkcijos nustatymas be viso kito apima elektroninių ataskaitų (ER) konfigūracijos formatų naudojimą konfigūruojamiems eksportavimo ir importavimo failams kurti ir veiksmų bei veiksmų srautų naudojimą konfigūruojamų taisyklių kūrimui įgalinti, kad būtų galima siųsti užklausas, importuoti atsakymus ir analizuoti atsakymo turinį.

El. SF išrašymo funkcijos nustatymas priklauso nuo šalies / regiono, nes SF formatai ir veiksmų srautai skiriasi.

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Elektroninių SF išrašymo priedo integravimo nustatymas „Finance” arba „Supply Chain Management” 

Šio nustatymo metu galėsite atlikti toliau pateiktas užduotis.

1. Atidaryti testuojamą funkciją
2. Įjungti elektroninių SF išrašymo priedo integravimo funkciją siekiant įgalinti integravimą su „Finance”.
3. Nustatyti elektroninių SF išrašymo priedo galinio punkto URL.
4. Importuoti ER konfigūracijas, susijusias su konkrečių šalių / regionų el. SF išrašymo funkcija.
5. Įjungti taikomą konkrečių šalių / regionų el. SF išrašymo funkciją.
6. Importuoti ER konfigūracijas ir nustatyti atsakymų tipus, kurių reikia norint atnaujinti jūsų konkrečioms šalims / regionams skirtą SF dokumentą kaip pateikimo proceso rezultatą.

### <a name="open-flighted-feature"></a>Testuojamos funkcijos atidarymas
Elektroninių SF integravimo funkcija įjungiama naudojant testavimą. Testavimas leidžia funkcijos įjungimą arba išjungimą pagal numatytuosius nustatymus. Toliau pateikti veiksmai leidžia įjungti testavimą ne gamybos aplinkoje. 

1. Vykdykite toliau pateiktą SQL komandą.

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)
    
2. Atlikę pirmiau minėtą keitimą, vykdykite IISReset visuose AOS

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>Elektroninių SF išrašymo priedo integravimo funkcijos įjungimas

1. Prisijunkite prie „Finance” arba „Supply Chain Management“.
2. Darbo srityje **Funkcijų valdymas** ieškokite naujos funkcijos **Konfigūruojamas elektroninių SF išrašymo priedo integravimas**. Jei funkcija vis tiek nerodoma puslapyje Funkcijų valdymas, paleiskite funkciją **Tikrinti, ar yra naujinimų**
3. Pasirinkite funkciją ir tada pasirinkite **Įjungti dabar**.

### <a name="set-up-the-service-endpoint-url"></a>Paslaugos galinio punkto URL nustatymas

1. Eikite į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**.
2. Skirtuko **Pateikimo paslauga** lauke **Paslaugos galinio punkto URL** įveskite `https://businessdocumentsubmission.us.operations365.dynamics.com/`.
3. Lauke **Aplinka** įveskite elektroninių SF išrašymo priedo aplinkos, kurią sukūrėte RCS nustatymo metu, pavadinimą.

![Paslaugos parametrų įvedimas](media/e-invoicing-services-get-started-enter-service-endpoint.png)

### <a name="import-the-er-configurations"></a>ER konfigūracijų importavimas

Norėdami įgalinti verslo duomenis, kad jie būtų renkami ir siunčiami į elektroninių SF išrašymo priedą, turite importuoti ER duomenų modelį ir ER duomenų modelio konfigūraciją, susijusius su konkrečių šalių / regionų el. SF išrašymo funkcija, kurią norite naudoti.

1. Darbo srities **Elektroninės ataskaitos** dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **„Microsoft”**. Įsitikinkite, kad šis konfigūracijos teikėjas nustatytas kaip **Aktyvus**. Daugiau informacijos apie tai, kaip nustatyti teikėją į **Aktyvus** , žr. [Konfigūracijų teikėjų kūrimas ir jų pažymėjimas kaip aktyviais](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Pasirinkite **Saugyklos**.
4. Pasirinkite **Visuotiniai ištekliai** ir pasirinkite **Atidaryti**.
5. Dialogo lange **Prisijungti prie „Lifecycle Services”** pasirinkite **Spustelėkite čia, kad prisijungtumėte prie „Lifecycle Services”**.
6. Atsižvelgdami į šalį ar regioną, kuriame norite naudoti el. SF išrašymo funkciją, turite importuoti taikomą duomenų modelį, duomenų modelio susiejimą ir formatus. Daugiau informacijos apie ER konfigūracijas, kurias turėtumėte importuoti, žr. konkrečių šalių / regionų temą „Darbo su elektroninių SF išrašymo priedu pradžia”.
7. Importuokite **kliento SF konteksto modelį**. Šiame modelyje yra papildomų parametrų, kurie, be viso kito, apibūdina „Finance” aplinką, naudojamą su elektroninių SF išrašymo priedu verslo duomenų pateikimo metu.

### <a name="turn-on-countryregion-specific-e-invoicing-features"></a><a name="region-specific"></a>Konkrečių šalių / regionų el. SF išrašymo funkcijų įjungimas

Norėdami įjungti konkrečių šalių / regionų el. SF išrašymo funkcijas, kad jos veiktų kartu su elektroninių SF išrašymo priedu, turite įjungti funkciją kiekviename juridiniame subjekte, kuriame norite ją naudoti. Po to seno elektroninių SF išrašymo integravimo nebebus galima naudoti, o integravimas su nauju elektroninių SF išrašymo priedu bus įjungtas.

1. Eikite į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**.
2. Skirtuke **Funkcijos** , esančiame funkcijos, susijusios su jūsų konkrečių šalių / regionų el. SF išrašymo funkcija, stulpelyje, pažymėkite žymės langelį, esantį stulpelyje **Įjungta**. Daugiau informacijos apie tai, kurią funkciją turėtumėte įjungti, žr. konkrečių šalių / regionų temą „Darbo su elektroninių SF išrašymo priedu pradžia”.

![Elektroninių SF išrašymo funkcijos įjungimas](media/e-invoicing-services-get-started-enable-invoicing-feature.png)

> [!NOTE]
> Jei yra keli juridiniai subjektai, sukonfigūruoti skirtingoms šalims ar regionams, galite įjungti kiekvieno juridinio subjekto konkrečių šalių / regionų el. SF išrašymo funkciją.

### <a name="import-er-configurations-and-set-up-the-response-types-to-update-your-countryregion-specific-invoice-document"></a>ER konfigūracijų importavimas ir atsakymų tipų nustatymas norint atnaujinti jūsų konkrečių šalių / regionų SF dokumentą

Jei pateiktą SF dokumentą reikia atnaujinti po pateikimo į vyriausybės autorizavimo tarnybas atsakymo, turite importuoti specialų ER duomenų modelį ir konfigūracijas, kad būtų galima įjungti SF dokumento būseną arba atnaujinti bet kurį kitą papildomą lauką.

1. Darbo srities **Elektroninės ataskaitos** dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **„Microsoft”**.
2. Pasirinkite **Saugyklos**.
3. Pasirinkite **Visuotiniai ištekliai** ir pasirinkite **Atidaryti**.
4. Importuokite **Atsakymo pranešimo modelis** , **Atsakymo pranešimo importavimo formatas** , **Atsakymo pranešimo modelio susiejimas su paskirties vieta** ir **Failo turinio importavimo formatas**.
5. Eikite į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**.
6. Skirtuke **Elektroninis dokumentas** pasirinkite **Įtraukti** , kad įvestumėte lentelės, susijusios su jūsų konkrečių šalių / regionų SF dokumentu, pavadinimą. Daugiau informacijos apie tai, kuriuos lentelių pavadinimus pasirinkti, žr. konkrečių šalių / regionų temą „Darbo su elektroninių SF išrašymo priedu pradžia”.
7. Pasirinkite **Atsakymų tipai** , kad sukonfigūruotumėte atsakymų tipus. Daugiau informacijos apie tai, kuriuos lentelių pavadinimus pasirinkti, žr. konkrečių šalių / regionų temą „Darbo su elektroninių SF išrašymo priedu pradžia”.

![Atsakymų tipų nustatymas](media/e-invoicing-services-get-started-set-up-response-types.png)

## <a name="e-invoicing-feature-names-by-country"></a>El. SF išrašymo funkcijų pavadinimai pagal šalį 
Toliau pateiktoje lentelėje aprašomos kitos el. SF išrašymo funkcijos, kurias galima atsisiųsti iš elektroninių ataskaitų visuotinės saugyklos siekiant generuoti elektronines SF.
RCS galite atsisiųsti toliau pateiktoje lentelėje nurodytas el. SF išrašymo funkcijas, ER konfigūracijas ir galimus el. SF išrašymo funkcijų nustatymus.
„Finance” galite įjungti susijusias funkcijų nuorodas puslapyje **Elektroninių dokumentų parametrai** , kad būtų galima išduoti elektronines SF toliau pateiktoms šalims. Daugiau informacijos žr. šios temos ankstesniame skyriuje [Konkrečių šalių / regionų el. SF išrašymo funkcijų įjungimas](#region-specific).

| Funkcijos pavadinimas                      | aprašymas                                 | ER konfigūracijos                                                                                                  | Nustatymai                                                                                                                                                         | Šalis/regionas  | Funkcijos nuoroda      |
|-----------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------|------------------------|
| Austrijos elektroninės SF (AT) | Austrijos pardavimo ir projekto SF      | - OIOUBL pardavimo SF <br>- OIOUBL projekto SF <br>- OIOUBL pardavimo kredito pažyma <br>- OIOUBL projekto kredito pažyma | - Pardavimo SF generavimas (AT) <br>- Projekto SF generavimas (AT) <br>- Pardavimo kredito pažymos generavimas (AT) <br>- Projekto kredito pažymos generavimas (AT)         | Austrija         | EUR-00023              |
| Belgijos elektroninė SF (BE)   | Belgijos pardavimo ir projekto SF      | - UBL pardavimo SF BE <br>- UBL projekto SF BE <br>- UBL projekto kredito pažyma BE <br>- UBL pardavimo kredito pažyma BE | - Pardavimo SF generavimas (BE)<br>- Projekto SF generavimas (BE) <br>- Pardavimo kredito pažymos generavimas (BE) <br>- Projekto kredito pažymos generavimas (BE)         | Belgija         | EUR-00023              |
| Danijos elektroninė SF (DK)    | Danijos pardavimo ir projekto SF      | - OIOUBL pardavimo SF <br>- OIOUBL projekto SF <br>- OIOUBL pardavimo kredito pažyma <br>- OIOUBL projekto kredito pažyma | - Pardavimo SF generavimas (DK) <br>- Projekto SF generavimas (DK) <br>- Pardavimo kredito pažymos generavimas (DK)<br>- Projekto kredito pažymos generavimas (DK)         | Danija         | EUR-00023<br> DK-00001 |
| Nyderlandų elektroninė SF (NL)     | Nyderlandų pardavimo ir projekto SF  | - UBL pardavimo SF NL <br>- UBL projekto SF NL <br>- UBL pardavimo kredito pažyma NL <br>- UBL projekto kredito pažyma NL | - Pardavimo SF generavimas (NL) <br> - Projekto SF generavimas (NL) <br> - Pardavimo kredito pažymos generavimas (NL) <br>- Projekto kredito pažymos generavimas (NL)          | Nyderlandai | EUR-00023              |
| Estijos elektroninė SF (EE)  | Estijos pardavimo ir projekto SF      | - Pardavimo SF (EE) <br> - Projekto SF (EE)                                                                     | - Pardavimo SF generavimas (EE) <br>- Projekto SF generavimas (EE)                                                                                           | Estija         | EUR-00023              |
| Suomijos elektroninė SF (FI)   | Suomijos pardavimo ir projekto SF      | - Pardavimo SF (FI) <br>- Projekto SF generavimas (FI)                                                          | - Pardavimo SF generavimas (FI) <br>- Projekto SF generavimas (FI)                                                                                           | Suomija         | EUR-00023              |
| Prancūzijos elektroninė SF (FR)    | Prancūzijos pardavimo ir projekto SF    | - UBL pardavimo SF FR <br> - UBL projekto SF FR <br> - UBL pardavimo kredito pažyma FR <br>- UBL projekto kredito pažyma FR | - Pardavimo SF generavimas (FR) <br> - Projekto SF generavimas (FR) <br>- Pardavimo kredito pažymos generavimas (FR) <br>- Projekto kredito pažymos generavimas (FR)         | Prancūzija          | EUR-00023              |
| Vokietijos elektroninė SF (DE)    | Vokietijos pardavimo ir projekto SF      |- Pardavimo SF (DE) <br> - Projekto SF <DE>                                                                     | - Pardavimo SF generavimas (DE) <br>- Projekto SF generavimas (DE)                                                                                           | Vokietija         | EUR-00023              |
| Norvegijos elektroninė SF (NO) | Norvegijos pardavimo ir projekto SF       | - OIOUBL pardavimo SF <br>- OIOUBL projekto SF <br>- OIOUBL pardavimo kredito pažyma <br>- OIOUBL projekto kredito pažyma | - Pardavimo SF generavimas (NO) <br>- Projekto SF generavimas (NO) <br>- Pardavimo kredito pažymos generavimas (NO) <br>- Projekto kredito pažymos generavimas (NO)          | Norvegija          | EUR-00023<br> NO-00010 |
| Ispanijos elektroninė SF (ES)   | Ispanijos pardavimo ir projekto SF        | - Pardavimo SF (ES) <br>- Projekto SF (ES)                                                                     | - Pardavimo SF generavimas (ES) <br>- Projekto SF generavimas (ES)                                                                                           | Ispanija           | EUR-00023 <br>ES-00025 |
| Italijos elektroninė SF (IT)   | Italijos pardavimo ir projekto SF        | - (Peržiūra) Pardavimo SF (IT) <br> - Projekto SF (IT)                                                           | - Pardavimo SF <br> - Projekto SF                                                                                                                           | Italija           | EUR-00023 <br>IT-00036 |
| PEPPOL elektroninė SF         | PEPPOL pardavimo ir projekto SF generavimas | - PEPPOL pardavimo SF <br>- PEPPOL projekto SF <br>- PEPPOL pardavimo kredito pažyma <br> - PEPPOL projekto kredito pažyma | - PEPPOL pardavimo SF generavimas <br>- PEPPOL projekto SF generavimas <br>- PEPPOL pardavimo kredito pažymos generavimas <br>- PEPPOL projekto kredito pažymos generavimas |                 | EUR-00023              |


## <a name="electronic-invoice-processing-in-finance-and-supply-chain-management"></a>Elektroninių SF apdorojimas „Finance” ir „Supply Chain Management”

Apdorojimo metu galėsite atlikti toliau pateiktas užduotis.

1. Pateikti verslo dokumentą (SF) naudodami elektroninių SF išrašymo priedą.
2. Peržiūrėti pateikimo vykdymo žurnalus.

### <a name="submit-business-documents"></a>Verslo dokumentų pateikimas

Vykdant įprastą pateikimo procesą, ryšys tarp kliento ir elektroninių SF išrašymo priedo yra dvikryptis. Tikslas yra atlikti dvi toliau pateiktas pagrindines užduotis elektroninių dokumentų teikimo metu.

1. Siųsti visus elektroninius dokumentus, kurie laukia „Finance” pateikimo, kurių pateikimo būsena teisinga ir kurie atitinka atrankos kriterijus.
2. Importuoti atsakymą į „Finance”, kurį elektroninių SF išrašymo priedas grąžina anksčiau pateiktiems elektroniniams dokumentams. Importavus atsakymai išanalizuojami, o verslo dokumentų būsena atitinkamai atnaujinama.

Verslo dokumentus galite pateikti neautomatiniu būdu arba pagal jūsų grafiko reikalavimus.

1. Eikite į **Organizacijos administravimas \> Laikotarpio \> Elektroniniai dokumentai \> Pateikti elektroninius dokumentus**.
2. Pirmą kartą pateikę bet kokį dokumentą, visada nustatykite parinktį **Iš naujo pateikti dokumentus** į **Ne**. Jei turite iš naujo pateikti dokumentą naudodami paslaugą, nustatykite šią parinktį į **Taip**.
3. „FastTab” **Įtrauktini įrašai** pasirinkite **Filtruoti** , kad būtų atidarytas dialogo langas **Užklausa** , kuriame galite kurti užklausą, norėdami pasirinkti dokumentus pateikimui.

![Dialogo langas Pateikti elektroninius dokumentus](media/e-invoicing-services-get-started-submission-form.png)

### <a name="filter-query"></a>Filtro užklausa

1. Dialogo lango **Užklausa** skirtuke **Diapazonas** įveskite filtro kriterijus, naudodami laukus **Lentelė** , **Išvestinė lentelė** , **Laukas** ir **Kriterijai**.
2. Pasirinkite **Įtraukti** , norėdami įtraukti tiek papildomų kriterijų, kiek reikia verslo dokumentų pasirinkimui.

    ![Pateikimo filtro kriterijų nustatymas](media/e-invoicing-services-get-started-set-up-submission-filter-criteria.png)

3. Pasirinkite **Gerai** , kad uždarytumėte dialogo langą **Užklausa**.
4. Pasirinkite **Gerai** , norėdami pateikti pasirinktus verslo dokumentus elektroninių SF išrašymo priedui.

    > [!NOTE]
    > Pirmą kartą bandant pateikti dokumentą naudojant paslaugą, būsite paraginti patvirtinti ryšį su elektroninių SF išrašymo priedu. Pasirinkite **Spustelėkite čia, kad prisijungtumėte prie elektroninių dokumentų pateikimo paslaugos**.
    >
    > ![Pranešimo langas Prisijungti prie elektroninių dokumentų pateikimo paslaugos](media/e-invoicing-services-get-started-dialog-form-connect-e-Invoicing-services.png)
    >
    > Jei ryšys sėkmingas, gaunamas patvirtinimo pranešimas.
    >
    > ![Ryšio su elektroninių SF išrašymo priedu patvirtinimas](media/e-invoicing-services-get-started-confirmation-connection-e-invoicing-services.png)

5. Uždarykite dialogo langą.

> [!NOTE]
> Po kiekvieno pateikimo veiksmų centras nurodo pateiktų dokumentų skaičių.
>
> ![Veiksmų centro pranešimai](media/e-invoicing-services-get-started-view-action-center-messages.png)

### <a name="submission-by-batch"></a>Pateikimas pagal paketą

Užuot pateikę dokumentus neautomatiniu būdu, galite automatizuoti pateikimo procesą ir vykdyti jį fone pagal sukonfigūruotą paketinio vykdymo dažnumą.

1. Dialogo lango **Pateikti elektroninius dokumentus** „FastTab” **Paleisti fone** nustatykite parinktį **Paketinis vykdymas** į **Taip**.
2. Skirtuke **Pasikartojimas** konfigūruokite paketinio vykdymo dažnumą.

![Pateikimo pagal paketą nustatymas](media/e-invoicing-services-get-started-set-up-submission-batch.png)

### <a name="view-all-submission-logs"></a>Visų pateikimo žurnalų peržiūra

1. Eikite į **Organizacijos administravimas \> Laikotarpio \> Elektroniniai dokumentai \> Elektroninio dokumento pateikimo žurnalas**.
2. Lauke **Dokumento tipas** pasirinkite dokumento tipą, pagal kurį filtruosite.

    ![Dokumento tipo pasirinkimas norint peržiūrėti pateikimo žurnalus](media/e-invoicing-services-get-started-select-document-type-for-viewing-submission-log.png)

    > [!IMPORTANT]
    > Stulpelyje **Pateikimo būsena** rodoma reikšmė nurodo būseną, kuri susijusi su pateikimo proceso baigimu. Ji nurodo, ar veiksmų srautas, sukonfigūruotas RCS, buvo vykdomas iki pabaigos, neatsižvelgiant į tai, ar elektroninis dokumentas buvo patvirtintas ar atmestas. Stulpelyje **Pateikimo būsena** esanti reikšmė neatspindi pateikto dokumento būsenos. Pateikto dokumento būseną (t. y., ar dokumentas buvo patvirtintas, ar atmestas) galite peržiūrėti pateikimo žurnalo informacijos „FastTab” **Apdorojimo veiksmų žurnalas** , kaip aprašyta toliau.

3. Veiksmų srityje pasirinkite **Užklausos \> Pateikimo informacija**.
4. Peržiūrėkite pateikimo žurnalo informaciją.

    ![Pateikimo žurnalo informacija](media/e-invoicing-services-get-started-view-submission-log-form.png)

Rezultatai, rodomi pateikimo žurnale, priklauso nuo to, kaip el. SF išrašymo funkcija buvo nustatyta RCS. Tačiau, neatsižvelgiant į nustatymą, pateikimo žurnale visuomet yra trys toliau pateikti „FastTab”.

- **Apdorojimo veiksmai** – šis „FastTab” nurodo veiksmų, sukonfigūruotų funkcijos versijoje, nustatytoje RCS, vykdymo žurnalą. Stulpelyje **Būsena** nurodoma, ar veiksmas sėkmingai įvykdytas.
- **Veiksmų failai** – šis „FastTab” nurodo tarpinius failus, sugeneruotus veiksmų vykdymo metu. Galite pasirinkti **Peržiūrėti** , norėdami atsisiųsti failą ir peržiūrėti jo turinį.
- **Apdorojimo veiksmų žurnalas** – šis „FastTab” nurodo ryšio tarp elektroninių SF išrašymo priedo ir tikslinės žiniatinklio tarnybos rezultatus. Taip pat rodoma, ką pateikė žiniatinklio tarnybos apdorojimas.

## <a name="related-topics"></a>Susijusios temos

- [Elektroninių SF išrašymo priedo apžvalga](e-invoicing-service-overview.md)
- [Darbo su Brazilijos elektroninių SF išrašymo priedu pradžia](e-invoicing-bra-get-started.md)
- [Darbo su Meksikos elektroninių SF išrašymo priedu pradžia](e-invoicing-mex-get-started.md)
- [Darbo su Italijos elektroninių SF išrašymo priedu pradžia](e-invoicing-ita-get-started.md)
- [Elektroninių SF išrašymo priedo nustatymas](e-invoicing-setup.md)
