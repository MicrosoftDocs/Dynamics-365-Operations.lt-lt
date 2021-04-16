---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ 2020 m. rugsėjo 26 d.
description: Šioje temoje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2020 m. rugsėjo 26 d.
author: jcart1106
ms.date: 09/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0bb0d01536106306dd456f4f3474611fa29530e2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800074"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-26-2020"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ 2020 m. rugsėjo 26 d.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje aprašomos naujos, pasikeitusios ar netrukus pasirodysiančios „Dynamics 365 Human Resources“ funkcijos. Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Daugiau informacijos apie naujas funkcijas ir jų numatomas bendro pasiekiamumo datas žr. [„Dynamics 365 Human Resources” 2020 m. 2-os leidimo bangos apžvalga](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šiame leidime

Šiame leidime yra toliau pateiktos naujos funkcijos ir klaidų ištaisymai. Pakeitimai taikomi 8.1.3589-hf.3 komponavimo versijai.

### <a name="new-features"></a>Naujos funkcijos

Šiame leidime bendrai prieinama toliau pateikta funkcija.

- **Dabar pasiekiamas 10.0.13 versijos platformos naujinimas**: daugiau informacijos apie naujinimą žr. [„Finance and Operations” programų 10.0.13 versijos platformos naujinimai (2020 m. spalio mėn.)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-13).

### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

> [!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Gali būti šios temos naujinimų siekiant įtraukti klaidų ištaisymus, įtrauktus į komponavimo versiją publikavus šią temą.

| Problemos numeris | Problema | Aprašas |
| --- | --- | --- |
| 469495 | Numatytųjų finansinių dimensijų tinklelio ir dialogo lango naujinimai | Finansinių dimensijų tinklelis ir dialogo langas atnaujinti visoje „Human Resources”. |
| 474887 | Atostogų užklausos darbo elementas atidaro netinkamą neautomatinio sprendimo saitą | Kai darbo eigos konfigūracijoje yra neautomatinis sprendimas, pereinant iš **Man priskirti darbo elementai** į atostogų užklausą atidaromas neteisingas saitas, rodantis tuščią formą arba atostogų užklausą, kurią sukūrė dabartinis vartotojas, o ne jam priskirtą neautomatinio sprendimo užklausą. |
| 474962 | Atostogų ir neatvykimų parametrų objekte yra laukų su nesuderinamomis žymomis | Atostogų ir neatvykimų parametrų objekto žymos atnaujintos, kad būtų aiškesnės. |
| 481401 | Kaupimo apdorojimas pakimba, kai kaupimo datos pagrindas yra po kaupimo pradžios datos ir mėnesio pabaigoje | Kaupimo apdorojimas atnaujintas, kad nebūtų delsos, jei kaupimo datos pagrindas yra po kaupimo pradžios datos ir mėnesio pabaigoje. |
| 447167 | Baigiančių galioti įrašų sąrašuose yra neaktyvių darbuotojų | **Personalo valdymo** skirtuke **Baigiantys galioti įrašai** yra neaktyvių darbuotojų. Dabar jame yra tik aktyvūs darbuotojai. |
| 486840 | Sąraše **Man priskirti darbo elementai** atidaromas netinkamas atostogų prašymas | Pasirinkus atostogų prašymą iš sąrašo **Man priskirti darbo elementai**, daugiau neatidaromas naujausias dabartiniam vartotojui priskirtas atostogų prašymas. |
| 506868 | „Dataverse” objekto **Pareigos** laukas **Pavadinimas** nenustatytas | Laukas **Pavadinimas**, esantis objektuose **Darbas** ir **Pareigos**, buvo rodomas kaip nenustatytas. Dabar laukas **Pavadinimas** rodomas. |
| 430359 | Nepavyksta pasiekti atleidimo kontrolinio sąrašo užduočių, kai priskirti vadovo ir darbuotojo vaidmenys | Darbuotojai, kurių atleidimo data ateityje, negalėjo pasiekti jų kontrolinio sąrašo užduočių, jei jie buvo tik darbuotojo ar vadovo vaidmens vartotojai. Dabar tik darbuotojo ar vadovo vaidmens vartotojai, kurių atleidimo data ateityje, gali pasiekti atleidimo užduotis. |
| 458102 | Sukurtas naujas darbuotojas neatsiranda objekte **Darbuotojo algalapio informacija** | Nauji darbuotojai įtraukiami į darbuotojo algalapio informacijos objektą neatidarant tų darbuotojų algalapių informacijos prieš eksportuojant objektą. |

## <a name="in-preview"></a>Peržiūros režimu

Toliau pateiktos naujos funkcijos yra peržiūrimos. Daugiau informacijos apie funkcijų įjungimą ir išjungimą žr. [Funkcijų valdymas](hr-admin-manage-features.md).

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| „Human Resources“ programa, esanti „Microsoft Teams” | [Darbuotojo atostogos ir neatvykimai „Microsoft Teams”](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [„Human Resources“ programa „Teams“](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Atostogų prašymų valdymas „Teams“](hr-teams-leave-app.md) |
| Patobulintos darbo eigos užklausos ir patvirtinimai | [Organizacijos ir personalo valdymo darbo eigos patobulinimai](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigūracijos parinktis, skirta sąrašui Man priskirti darbo elementai perkelti](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |

## <a name="coming-soon"></a>Jau greitai

Toliau pateikta nauja funkcija bus įtraukta į būsimą leidimą.

- [Pasirinktiniai saitai vadovų savitarnoje](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service)

Norėdami gauti visą planuojamų funkcijų ir jų suplanuotų leidimų sąrašą, žr. [„Dynamics 365 Human Resources” 2019 m. 2-os leidimo bangos apžvalga](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Papildomi ištekliai

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)
[„Dynamics 365 Human Resources“ 2020 m. 2 leidimo bangos apžvalga](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)
[Atnaujinimo procesas](hr-admin-setup-update-process.md)
[Funkcijų valdymas](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]