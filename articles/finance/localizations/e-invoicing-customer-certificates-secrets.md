---
title: Kliento sertifikatai ir slaptos saugos
description: Šioje temoje paaiškinama, kaip nustatyti kliento sertifikatus ir paslapymus išrašant elektronines SF.
author: dkalyuzh
ms.date: 02/07/2022
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
ms.openlocfilehash: 1325cad95e9a6dc470691f5f168439fccaaa78e1
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371955"
---
# <a name="customer-certificates-and-secrets"></a>Kliento sertifikatai ir slaptos saugos

[!include [banner](../includes/banner.md)]

Jei jau turite kodo Microsoft Azure Vault nuorodą Reguliavimo konfigūracijos tarnyba (RCS), galite sukurti nuorodas į rakto Vault sertifikatus ir paslapius. Jei dar neturite rakto Vault nuorodos, informacijos apie tai, [kaip ją sukurti, žr](e-invoicing-service-environments.md) . paslaugų aplinkose.

## <a name="create-certificates-and-secrets"></a>Sertifikatų ir paslapčių kūrimas

Norėdami kurti ir nustatyti sertifikatus ir slaptus atvejus, atlikite šiuos veiksmus.

1. Prisijunkite prie jūsų RCS abonemento.
2. Darbo srities **Globalizacijos funkcijos** dalyje **Aplinka** pasirinkite plytelę **Elektroninių SF išrašymo priedas**.
3. **Aplinkos nustatymo** puslapio veiksmų srityje pasirinkite Aptarnavimo **aplinkos**.
4. **Aptarnavimo aplinkos puslapyje**, veiksmų srityje, pasirinkite rakto **Vault parametrus**.
5. Puslapyje Rakto **Vault parametrai** pasirinkite rakto Vault nuorodą, tada **skyriuje Sertifikatai** pasirinkite **Įtraukti**.
6. Lauke Pavadinimas **įveskite** rakto Vault sertifikato arba slapto pavadinimą. Daugiau informacijos rasite "Azure" [saugyklos sąskaitos kūrimas "Azure" portale](e-invoicing-create-azure-storage-account-azure-portal.md).
7. Lauke **Aprašas** įveskite aprašą.
8. Lauke Tipas **pasirinkite** Sertifikatas **·**, jei nurodote sertifikatą, kuris saugomas rakto saugykloje. Pasirinkite **Slapti**, jei nurodote slaptą, kuris saugomas rakto saugykloje.
9. Pasirinkite **Įrašyti**.

> [!NOTE]
> Kai kuriuose scenarijuose turite naudoti viešus sertifikatus, kurie turi plėtinį .cer failo vardas. Tačiau "Key Vault" nepalaiko šio tipo sertifikatų kaip "Key Vault" importavimo ir saugojimo. Šiuose scenarijuose turite įrašyti .cer failą kaip Base-64 užkoduotą X.509 (. CER) eilutė. Tada rakto Vault slaptoje saugykloje saugokite eilutę, kuri **atsiranda tarp failo eilutės BEGIN CERTIFICATE** **ir END CERTIFICATE** eilutės. Aptarnavimo aplinkoje vis tiek turite sukurti nuorodą į rakto Vault įrašą ir nustatyti lauką **Tipas** kaip **Sertifikatas**.

## <a name="create-a-chain-of-certificates"></a>Sukurti sertifikatų grandinę

Jei jūsų šaliai/regionui konkrečioms SF reikia sertifikatų grandinės, kad būtų galima taikyti skaitmeninius parašus, arba sukurti saugių jungčių lygmens \[SSL\] ryšį su išorinėmis tinklo paslaugomis, sukurkite sertifikatų grandinę, kurioje šie sertifikatai būtų pateikti tokia tvarka:

1. Šakniniai sertifikatai
2. Tarpiniai sertifikatai
3. Galutinių vartotojų sertifikatai

Šakninio sertifikato institucijos (CAS) yra patikimas sertifikatų šaltinis. Tarpiniai CA sertifikatai yra tiltai, kurie susieja galutinio vartotojo sertifikatus su šakniniais CA sertifikatais.

Norėdami sukurti ir nustatyti sertifikatų grandinę, atlikite šiuos veiksmus.

1. **Mygtuko "Vault" parametrų** puslapyje, veiksmų srityje, pasirinkite **Sertifikatų grandinė**.
2. Pasirinkite **Naujas** tam, kad sukurtumėte sertifikatų grandinę.
3. **Lauke Pavadinimas** įveskite sertifikatų grandinės pavadinimą.
4. Lauke **Aprašas** įveskite aprašą.
5. Skyriuje **Sertifikatai** pasirinkite **Įtraukti** kad į grandinę būtų įtrauktas sertifikatas.
6. Norėdami pakeisti **Aukštyn** arba **Žemyn** poziciją sertifikato grandinėje. Sąrašo viršuje išlaikykite CA šakninį sertifikatą ir galutinio vartotojo sertifikatą apačioje.
7. Pasirinkite **Įrašyti**.

RCS galite sukurti tiek pagrindinių saugyklos nuorodų, kiek norite. Nepamirškite, kad saugojimo bendrai naudojamos prieigos parašo (SAS) atpažinimo ženklo secret naudojamas susieti nurodytą aptarnavimo aplinką su rakto Vault nuoroda. Galite nurodyti rakto Vault sertifikatus ir pasamdus, saugomus rakto saugykloje, kurioje taip pat yra saugyklos SAS atpažinimo ženklo, kurį naudojate kurdami aptarnavimo aplinką, slapti.
