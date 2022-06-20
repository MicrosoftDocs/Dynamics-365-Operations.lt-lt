---
title: Paslaugų aplinkos
description: Šiame straipsnyje pateikiama informacija apie elektroninių SF išrašymo paslaugų aplinkas ir paaiškinama, kaip jas nustatyti.
author: dkalyuzh
ms.date: 02/28/2022
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
ms.openlocfilehash: 8c743c5b2fbc7dcc3ae04fa4d7ca0e65de6c2507
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901253"
---
# <a name="service-environments"></a>Paslaugų aplinkos

[!include [banner](../includes/banner.md)]

Tarnybos aplinkos yra loginiai skaidiniai, kurie sukurti palaikyti globalizavimo priemones ir atitinkamus dokumentus, kurie apdorojami elektroninių SF išrašymo paslaugoje. Saugos slapyme ir skaitmeniniuose sertifikatuose bei prieigos teisės (vaidmenys) turi būti sukonfigūruotos tarnybos aplinkos lygiu.

Galite sukurti tiek aptarnavimo aplinkos, kiek jums reikia. Visos jūsų sukuriamos aptarnavimo aplinkos nepriklauso viena nuo kitos. Rekomenduojame sukurti mažiausiai dvi aptarnavimo aplinkas:

- Viena aplinka, skirta pagrindinei programavimo ir tikrinimo tikslais. Ši aplinka paprastai yra vartotojo priėmimo tikrinimo (UAT) aplinka.
- Viena aplinka gamybos tikslams. Paprastai ši aplinka yra gamybos aplinka.

Šis skaidymo tipas padeda užtikrinti, kad el. SF išrašymo procesai prieš pereidami į gamybą bus patikrinti ir pritaikyti sand. langelyje.

Aptarnavimo aplinkos turi būti sukurtos ir tvarkomos reguliavimo konfigūracijos tarnybos (RCS). Tada, kai jos parengtos, jos turi būti publikuojamos elektroninių SF išrašymo paslaugoje. Publikavimo procesas siunčia tarnybos aplinkos parametrus iš RCS egzemplioriaus į elektroninių SF išrašymo tarnybą.

Jei negalite užbaigti publikavimo proceso, kai sukuriate naują paslaugų aplinką arba pakoreguokite esamą tarnybos aplinką (pvz., Microsoft Azure pridėdami arba pašalindami vartotojus arba pagrindinius Vault slaptus) pakeitimus negalėsite pritaikyti. "Dynamics 365 Finance" arba "Dynamics 365" gali pasiekti tik paskelbtas aplinkas Dynamics 365 Supply Chain Management.

## <a name="service-environment-statuses"></a>Aptarnavimo aplinkos būsenos

Aptarnavimo aplinkas galima valdyti pagal jų būseną. Galite peržiūrėti aplinkos būseną aptarnavimo **aplinkos** puslapyje. Galimos šios būsenos:

- **Nepaskelbta** – aplinka sukurta, bet dar nepaskelbta.
- **Publikuota** – aplinka publikuota elektroninių SF išrašymo tarnybose.
- **Pakeista** – publikuoto aplinkos atributai pakeisti, bet pakeitimai dar nebuvo publikuoti.

## <a name="users"></a>Vartotojai

Kiekviena aptarnavimo aplinka turi pateikti vartotojų, kurie gali prisijungti prie elektroninių SF išrašymo iš finansų arba tiekimo grandinės valdymo, sąrašą.

## <a name="applications"></a>Prašymai

Kai kuriuose scenarijuose programos, ne finansų ar tiekimo grandinės valdymas, gali turėti prisijungti prie elektroninių SF išrašymo tarnybos, kad galėtų pateikti elektroninius dokumentus toliau apdoroti arba nuskaityti informaciją, pvz., dokumento pateikimo būseną. Šiais scenarijais programa turi būti nurodyta programų sąraše. Tokiu būdu ji turės prieigą prie elektroninių SF išrašymo tarnybos. Programa taip pat turi būti užregistruota kaip programa Azure Active Directory programoje (Azure AD), o objekto ID turi būti naudojamas jai identifikuoti. 

Kadangi Microsoft reikalauja aukšto lygio programų, kurios gali prisijungti prie elektroninių SF išrašymo tarnybos, saugos lygio, turite su Microsoft <DGXRegulatoryservicesengineering@service.microsoft.com> susisiekti ir pateikti toliau nurodytą informaciją apie savo programą:

- Azure AD nuomotojo ID
- Microsoft Dynamics Ciklo tarnybų (LCS) aplinkos ID
- Programos ID (kliento ID)
- Objekto ID
- Programos pagrindimas ir aukšto lygio aprašas

Microsoft įvertins užklausą ir užregistruos programą saugos registre, kad užtikrintų jos veiklą su elektroninių SF išrašymu.

## <a name="number-sequences"></a>Numeracijos

Jei jūsų scenarijams reikia numeracijų (pavyzdžiui, failų pavadinimuose), galite naudoti numeracijas, kurios nustatytos konkrečiai aplinkai, bet kurios gali būti naudojamos globalizavimo priemonėse arba konkrečios globalizavimo funkcijose. Nu nustačius numeraciją, ją galima naudoti kintamiesiems ir pardavimo galimybių apdorojimui. Norėdami sekti jo naudojimą, **numeracijos** puslapyje ieškokite naudojimo parametro **Dabartinės** **vertės**.

### <a name="working-with-number-sequences"></a>Darbas su numeracijomis
**Numeracijų puslapyje**: 

- Pasirinkti **Naujas**, jei norite kurti numeraciją. Tada įveskite pavadinimą ir aprašymą. 
- Jei **numeraciją** norite panaikinti, jei ji nebenaudojama, pasirinkite Naikinti.
- Jums nereikia veiksmų srityje pasirinkti **Publikuoti**, kad būtų publikuoti numeracijos pakeitimai. Atnaujinimas atliekamas automatiškai.

## <a name="create-a-key-vault-reference"></a>Kurti kodo Vault nuorodą

1. Prisijunkite prie jūsų RCS abonemento.
2. Darbo srities **Globalizacijos funkcijos** dalyje **Aplinka** pasirinkite plytelę **Elektroninių SF išrašymo priedas**.
3. **Aplinkos nustatymo** puslapio veiksmų srityje pasirinkite Aptarnavimo **aplinkos**.
4. **Aptarnavimo aplinkos puslapyje**, veiksmų srityje, pasirinkite rakto **Vault parametrus**.
5. **Rakto Vault parametrų puslapyje pasirinkite** Naujas **, kad** sukurtumėte rakto Vault nuorodą.
6. **Lauke Pavadinimas** įveskite rakto Vault nuorodos pavadinimą.
7. Lauke **Aprašas** įveskite aprašą.
8. Lauke Rakto **Vault URI** iš rakto saugyklos (`https://<your key vault>.vault.azure.net/`) įklijuokite rakto Vault URI. Norėdami gauti daugiau informacijos, " [Azure" rakto "Azure" portale sukurkite "Azure" raktą](e-invoicing-create-azure-key-vault-azure-portal.md).
9. Pasirinkite **Įrašyti**.
    
## <a name="create-a-secret-for-the-storage-account-secret-token"></a>Kurti saugyklos sąskaitos slapto atpažinimo ženklo slaptą slaptažodį

1. Puslapyje Rakto **Vault parametrai** pasirinkite rakto Vault nuorodą, kurią sukūrėte ankstesnėje procedūroje, **tada** skyriuje Sertifikatai pasirinkite **Įtraukti**.
2. **Pavadinimas** laukelyje įveskite tą patį talpyklos paskyros pavadinimą. Šis pavadinimas turi sutapti su rakto Vault slapto ženklo, kuriame yra saugyklos bendrinamos prieigos parašo (SAS) atpažinimo ženklo, pavadinimu. Daugiau informacijos rasite "Azure" [saugyklos sąskaitos kūrimas "Azure" portale](e-invoicing-create-azure-storage-account-azure-portal.md). 
3. Lauke **Aprašas** įveskite aprašą.
4. Lauke **Tipas** pasirinkite **Raktas**.
5. Pasirinkite **Įrašyti**.
    
## <a name="create-a-service-environment"></a>Aptarnavimo aplinkos kūrimas

1. Puslapyje Aptarnavimo **aplinkos pasirinkite** Naujas, kad **sukurtumėte** aptarnavimo aplinką.
2. Lauke Pavadinimas **įveskite** elektroninių SF išrašymo aplinkos pavadinimą.
3. Lauke **Aprašas** įveskite aprašą.
4. **Talpyklos SAS atpažinimo rakto** lauke pasirinkite slaptos saugyklos paskyros, kuri turi būti naudojama, jei norima autentifikuoti prieigą prie saugyklos sąskaitos, pavadinimą.
5. Skyriuje Vartotojai **pasirinkite** Įtraukti, kad **įtrauktumėte** vartotoją, kuriam leidžiama pateikti elektronines SF per aplinką ir prisijungti prie saugojimo sąskaitos.
6. Lauke **Vartotojo ID** įveskite vartotojo pravardę. 
7. Lauke **El. paštas** įveskite vartotojo el. pašto adresą.
8. Pasirinkite **Įrašyti**.
9. Veiksmų srityje pasirinkite Publikuoti, kad **publikuodami** aplinką elektroninių SF išrašymo paslaugoje. Patikrinkite, ar lauko Būsena **reikšmė pakeista į Publikuota** **.**
