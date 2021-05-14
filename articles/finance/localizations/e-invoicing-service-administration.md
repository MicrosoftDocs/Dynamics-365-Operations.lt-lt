---
title: Elektroninių SF išrašymo administravimo komponentai
description: Šioje temoje pateikta informacija apie kompnentus, kurie susiję su elektroninių sąskaitų priedų administravimu.
author: gionoder
ms.date: 04/29/2021
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
ms.openlocfilehash: 3ac4a03d75898680b5655421f3024dc6f666464c
ms.sourcegitcommit: 54d3ec0c006bfa9d2b849590205be08551c4e0f0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/30/2021
ms.locfileid: "5963196"
---
# <a name="electronic-invoicing-administration-components"></a>Elektroninių SF išrašymo administravimo komponentai

[!include [banner](../includes/banner.md)]


Šioje temoje pateikta informacija apie kompnentus, kurie susiję su elektroninių sąskaitų priedų administravimu. Taip pat pateikiama informacija apie tai, kaip konfigūruoti elektroninių SF išrašymo papildomą paslaugą.

## <a name="azure"></a>Azure

Naudokite „Microsoft Azure“ norėdami sukurti rakto saugyklos ir saugyklos sąskaitos slaptus duomenis. Tada konfigūruojant elektroninės SF išrašymo priedą naudokite paslapius.

## <a name="lifecycle-services"></a>Lifecycle Services

Naudokite „Microsoft Dynamics Lifecycle Services“ LCS tam, kad įgalintumėte mikroservices priedą LCS diegimo projektui.

> [!NOTE]
> Mikropaslaugos LCS priedo įdiegimui reikalingas bent 2 pakopos virtualusis įrenginys. Daugiau informacijos apie aplinkų planavimą ieškokite skyriuje [Aplinkos planavimas](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
 

## <a name="regulatory-configuration-services"></a>„Regulatory Configuration Services“ (RCS)

„Dynamics 365 Regulatory Configuration Services“ (RCS) yra sąsaja, naudojama elektroninio SF išrašymo priedams konfigūruoti. Tokie ištekliai kaip aplinkos ir elektroninių SF išrašymo priemonės kuriamos, prižiūrimos ir laikomos RCS. Kai ištekliai parengti, jie publikuojami elektroninių SF išrašymo papildomų paslaugų svetainėje.

Norėdami sužinoti RCS prisijungimą, žr. skyrių [„Regulatory Services”](https://marketing.configure.global.dynamics.com/).

Daugiau informacijos apie RCS žr. [„Regulatory Configuration Services“ (RCS) – globalizacijos funkcijos](rcs-globalization-feature.md)

### <a name="integration-with-electronic-invoicing"></a>Integravimas su elektroninių SF priedu 

Prieš konfigūruojant elektronines SF naudojant RCS, būtina sukonfigūruoti RCS, kad būtų leidžiama susisiekti su elektroninių SF išrašymo papildymu. Šią konfigūraciją užbaikite skirtuko **Elektroninės sąskaitos faktūros priedai** **Elektroninės ataskaitos parametrai** puslapyje.

#### <a name="service-endpoint"></a>Paslaugos galinis punktas

Elektroninių SF išrašymo priedas yra keliuose „Azure” duomenų centro regionuose. Toliau esančioje lentelėje pateikiamas pasiekiamumo sąrašas pagal regioną.

| „Azure" duomenų centro geografija |
|----------------------------|
| Rytų JAV                    |
| Vakarų JAV                    |
| Šiaurės ES                   |
| Vakarų ES                    |

### <a name="service-environments"></a>Paslaugų aplinkos

Aptarnavimo aplinkos yra loginiai skaidiniai, kurie sukurti elektroninių SF išrašymo funkcijų vykdymui elektroninio SF išrašymo papildinyje palaikyti. Saugos slapyme ir skaitmeniniuose sertifikatuose, ir pereigimas (t. y. prieigos teisės) turi būti konfigūruojamas tarnybos aplinkos lygiu.

Klientai gali sukurti tiek aptarnavimo aplinkos, kiek tik norite. Visos kliento sukuriamos aptarnavimo aplinkos yra nepriklausomos vienas nuo kito.

Aptarnavimo aplinkos turi būti sukurtos ir tvarkomos RCS. Kai paslaugų aplinkos parengti, jie turi būti publikuoti elektroninių SF išrašymo papildomų paslaugų svetainėje.

#### <a name="service-environment-status"></a>Paslaugų aplinkos būsena

Aptarnavimo aplinkas galima valdyti naudojant būseną. Galimos parinktys yra šios:

- **Nepaskelbta** – aplinka sukurta, bet dar nepaskelbta.
- **Publikuota** – aplinka publikuota elektroninio SF išrašymo prieduose.
- **Pakeista** – publikuoto aplinkos atributai pakeisti, bet pakeitimai dar nebuvo publikuoti.

#### <a name="customer-secrets"></a>Kliento raktai

Elektroninių SF išrašymo priedo paslauga yra atsakinga už visų jūsų verslo duomenų saugojimą „Azure” ištekliuose, kurie priklauso jūsų įmonei. Siekiant užtikrinti, kad paslauga veiktų tinkamai ir kad visus verslo duomenis, kurių reikia elektroninių SF išrašymo priedui ir kuriuos jis sugeneravo, galėtų pasiekti tik priedas, turite sukurti du pagrindinius toliau pateiktus „Azure” išteklius:

- „Azure” saugyklos abonementas („Blob“ saugykla) saugos elektronines SF
- „Azure Key Vault”, kuri laikys sertifikatus ir suvienodintą saugyklos paskyros išteklių identifikatorių (URI)


Paskirti „Key Vault“ ištekliai ir kliento talpyklos paskyra turi būti priskirti tik elektroninių SF išrašymo priedo naudojimui . Daugiau informacijos žr. [Kurti „Azure” saugyklos paskyrą ir „Key Vault“ raktą](e-invoicing-create-azure-storage-account-key-vault.md).

Norėdami stebėti „Key Vault" apsaugą ir gauti įspėjimus, sukonfigūruokite „Azure Monitor for Key Vault". Įjungus „Key Vault" registravimą, galima stebėti, kaip, kada ir kas turi prieigą prie „Key Vault". Norėdami gauti daugiau informacijos, [žr. „Azure Key Vault" stebėjimą ir įspėjimą](/azure/key-vault/general/alert) bei kaip įgalinti [„Key Vault"](/azure/key-vault/general/howto-logging?tabs=azure-cli) registravimą.

Geriausia, jei norite periodiškai pasukti paslapius. Daugiau informacijos ieškokite [Raktų dokumentacijoje](/azure/key-vault/secrets/).

#### <a name="users"></a>Vartotojai

Kiekviena aptarnavimo aplinka turi pateikti vartotojų, kurie gali prisijungti „Dynamics 365 Finance“ prie elektroninių „Dynamics 365 Supply Chain Management“ SF išrašymo priedo ir prie jo prisijungti, sąrašą.

#### <a name="publication"></a>Publikavimas

Paslaugų aplinkos turi būti publikuotos elektroninių SF išrašymo priede prieš jų naudojimą. „Finance and Supply Chain Management“ gali pasiekti tik paskelbtas aplinkas. Be to, paslaugų aplinka turi būti publikuota prieš tai, kai visi atributų naujinimai įsigalios elektroninių SF išrašymo paslaugai.

### <a name="connected-applications"></a>Prijungtos programos

Susijusios programos yra „Finance and Supply Chain Management“ egzemplioriai, kuriuos jūs galite norėti pasiekti naudodami RCS. Be programos URL ir jo nuomininko, susijusioje programoje yra kredencialai, kurie leidžia RCS prisijungti prie aplinkos.

Naudodami susijusias programas galite konfigūruoti dalį elektroninių SF išrašymo priemonės „Finance and Supply Chain Management“, kad būtų veikia visa elektroninių SF išrašymo priemonė.

## <a name="finance-and-supply-chain-management"></a>„Finance and Supply Chain Management“

### <a name="integration-with-electronic-invoicing"></a>Integravimas su elektroninių SF priedu

Prieš naudojant „Finance and Supply Chain Management“ elektroninėms SF išduoti naudojant elektroninių SF išrašymo priedą, priedas turi būti sukonfigūruotas taip, kad leistų ryšį su tarnyba.

#### <a name="electronic-invoicing-integration-feature"></a>Elektroninių SF išrašymo priedo funkcijos integravimas

Norėdami įgalinti „Finance and Supply Chain Management“ ir elektroninio SF išrašymo priedo ryšį, turite įjungti integravimo priemonę **Elektroninio SF išrašymo priedo integravimas** funkciją **Funkcijų valdymas** darbo srityje.

#### <a name="service-endpoint"></a>Paslaugos galinis punktas

Paslaugos galinis punktas yra URL, kuriame yra elektroninio SF išrašymo priedas. Prieš elektroninių sąskaitų išleidimą, paslaugos galinis taškas turi būti konfigūruotas „Finance and Supply Chain Management“ siekiant leisti komunikaciją su paslaugomis.

Norėdami konfigūruoti paslaugų galinį tašką, eikite į **Organizacijos administravimas \> Nustatymai \> Elektroninio dokumento parametras** ir tada **Pateikimo tarnybos** skirtukas, laukelyje **Elektroninės sąskaitos priedo URL** laukelis ir įveskite URL kaip aprašyta lentelėje skyriuje **Paslaugos galinis taškas**.

#### <a name="environments"></a>Aplinkos

Aplinkos pavadinimas, įvestas „Finance and Supply Chain Management“ remiasi aplinkos, kuri sukurta RCS ir paskelbta elektroninio SF išrašymo prieduose, pavadinimu.

Aplinka turi būti konfigūruojama **Pateikimo paslaugų** skirtuke **Elektroninio dokumento parametro** puslapyje taip, kad kiekvienoje užklausoje išduoti elektronines SF būtų aplinka, kur elektroninio SF išrašymo priedas gali nustatyti, kuri elektroninių SF išrašymo funkcija turi apdoroti užklausą.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių sąskaitų konfigūravimas RCS](e-invoicing-configuration-rcs.md)
- [Išduoti elektronines sąskaitas „Finance and Supply Chain Management”](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
