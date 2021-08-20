---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. kovo 10 d.)
description: Šiame straipsnyje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2020 m. kovo 10 d.
author: andreabichsel
ms.date: 03/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-03-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 311c907cdb91a1ad87c7dac45c273810fea5cfd53dce3013dda870c1932b3a25
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736093"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-10-2020"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. kovo 10 d.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šiame straipsnyje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources“ funkcijos. Pakeitimai taikomi 8.1.2985 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo LCS palaikymo numerius informaciniais tikslais.

## <a name="cant-access-skill-gap-analysis-report-394460"></a>Nepavyksta pasiekti įgūdžių trūkumų analizės ataskaitos (394460)

Dynamics 365 Human Resources nepalaiko šios ataskaitos. Meniu elementas, skirtas SSRS ataskaitai atspausdinti, yra pašalintas.

## <a name="incorrect-message-accessing-the-getting-started-page-417950"></a>Netinkamas pranešimas jungiantis prie darbo pradžios puslapio (417950)

Atlikus šį pakeitimą, sauga paslepia šį meniu elementą, jei neturite prieigos prie formos.

## <a name="streamlined-task-maintenance-for-employees-380538"></a>Supaprastinta darbuotojų užduočių priežiūra (380538)

Darbuotojo užduoties priežiūros formoje pateikiamos visos darbuotojo užduotys, susijusios su įtraukimu į kolektyvą, atleidimu, perėjimais ir verslo procesais. Galite panaikinti, iš naujo priskirti ar atnaujinti užduočių būseną.

Pavyzdys: Benjamin Martin yra išmokos administratorius. Atliekant darbuotojo įleidimą į kolektyvą, užduotys sukuriamos Benjaminui, kad būtų galima peržiūrėti naujo darbuotojo išmokų pasirinkimą. Rodomos Benjamino užduotys, kurias jis yra atlikęs, ir būsimos užduotys, kurias jis turi atlikti. Benjaminas nusprendė palikti įmonę, todėl jo užduotys turi būti arba iš naujo priskirtos, arba pašalintos. Užduoties priežiūros forma (formos **Darbuotojas** veiksmų srityje) leidžia visas Benjamino užduotis iš naujo priskirti kitam darbuotojui arba pašalinti.  

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>Dataverse sprendimas dabar galimas su šiais pakeitimais:

| aprašymas | Pakeitimas |
| --- | --- |
| Objekto **Užduotis / pareigos** keitimai | <ul><li>Pridėta **Kompensacijos sritis**</li>|
| Objektas **Pareigų dimensija** pridėtas | <ul><li>Pridėta **Finansinės dimensijos**</li>
| Objekto **Darbininkas** keitimai | <ul><li>Pridėta **Pavadinimų seka**</li><li>Pridėta **Dirba iš namų**</li><li>Pridėta **Kalba**</li><li>Pridėta **Paaukštinimo data**</li><li>Pridėta **Jubiliejaus data**</li><li>Pridėta **Pradinio įdarbinimo data**</li></ul> |
| Objekto **Įdarbinimas** keitimai | <ul><li>Pridėta **Finansinės dimensijos**</li><li>Pridėta **Atleidimo priežastis**</li><li>**Perėjimo data** pervardyta į **Atleidimo data**</li><li>Pridėta **Bandomojo laikotarpio data**</li></ul> |
| Objekto **Darbininko adresas** keitimai | <ul><li>Pridėta **Gatvė**</li><li>**1 adreso eilutė**, **2 adreso eilutė** ir **3 adreso eilutė** pažymėtos kaip nebenaudojamos</li></ul> |
| Nauji kintamosios atlyginimo dalies sąrankos objektai | <ul><li>**Kompensacijų kitimo plano tipas**</li><li>**Kompensacijų kitimo planas**</li><li>**Kintamosios atlyginimo dalies paskirstymo taisyklės**</li><li>**Kompensacijų kitimo plano lygis**</li></ul> |
| Naujas objektas **Darbuotojo įdarbinimo kalendorius** | <ul><li>Pridėta **Darbo kalendoriaus objektas**</li></ul> |
| Naujas objektas **Algalapio pareigų informacija** | <ul><li>Pridėta **Algalapio pareigų informacija**</li></ul> |
| Naujas subjektas **Pavadinimas** | <ul><li>**Pavadinimas** pridėtas</li></ul> Naujas objektas **Pavadinimas** įtrauktas į Dataverse, bet šiuo metu nėra nurodomas iš objektų **Pareigos** arba **Darbas**. |

> [!NOTE]
> Abiejų pareigų ir įdarbinimo finansinės dimensijos suteikia vienos krypties integraciją, skirtą atnaujinimams iš „Human Resources“ į Dataverse. Finansinių dimensijų atnaujinimai dabar nesinchronizuojami iš Dataverse į „Human Resources“.

Per artimiausias kelias savaites šie objektų pakeitimai bus galimi visose aplinkose. Norėdami rankiniu būdu įdiegti naujausią Dataverse sprendimą, skirtą „Human Resources“:

1.  Eikite į [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com).

2.  Pasirinkite **Aplinkos**.

3.  Raskite aplinką, kurią norite atnaujinti. Aplinka turėtų atitikti „Human Resources“ formoje **Apie** esančios sekcijos **Dataverse informacija** reikšmę **Aplinkos pavadinimas**.

4.  Pasirinkite aplinką, kad peržiūrėtumėte detalią aplinkos informaciją.

5.  Veiksmo juostos viršuje pasirinkite **Valdyti sprendimus**. Atsidarys naujas naršyklės langas ir pereisite į **„Dynamics 365“ administravimo centrą** savo aplinkos kontekste.

6.  Sąraše **Sprendimas** pasirinkite **Dynamics 365 Human Resources fiksavimas**.

7.  Pasirinkite **Atnaujinti**, kad pritaikytumėte naujausią sprendimą.

## <a name="in-preview"></a>Peržiūros režimu

Šios peržiūros funkcijos bus pasiekiamos nuo 2020 m. vasario 3 d.

- **Atostogų ir neatvykimų peržiūros funkcijos** – daugiau informacijos žr. skyrių [Atostogų ir neatvykimų peržiūros funkcijos](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Išmokų valdymo peržiūros funkcija** – norėdami gauti daugiau informacijos, įskaitant žinomas problemas, žr. skyrių [Išmokų valdymo peržiūra](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Jau greitai

### <a name="platform-update-33"></a>Platformos „update 33“

- Viso puslapio programos (peržiūra) – ši peržiūros funkcija, kuriai reikia įjungti įrašytų rodinių funkciją, leidžia įtraukti Power Apps ir trečiųjų šalių programas prietaisų skydelyje kaip viso puslapio patirtį.

- Įrašyti rodiniai (peržiūra) – ši peržiūros funkcija įjungia įrašytus rodinius, o tai labai patobulina personalizavimo posistemį. Ši funkcija suteikia vartotojams galimybę viename puslapyje turėti kelis įvardytuosius individualizavimo rinkinius. Taip pat galite publikuoti saugos vaidmenų rodinius.

- Optimizuota „yra viena iš“ filtravimo patirtis – šia funkcija įjungiama optimizuota „yra viena iš“ filtravimo patirtis, kurią pasitelkus yra lengviau įvesti kelias filtrų vertes, suteikiama paprastesnė priemonė atskiroms arba visoms filtrų vertėms pašalinti ir glaudesnis bei intuityvesnis filtro verčių vizualizavimas.

- Rekomenduojami laukai – vartotojams dažnai reikia pridėti laukus prie tinklelio ar puslapio. Tai gali būti sudėtinga su tiek daug galimų laukų. Vietoje to, kad paieška būtų atliekama dideliame sąraše, ši funkcija leidžia sistemai nustatyti rekomenduojamus laukus, atsižvelgiant į tai, kuriuos kitus vartotojus dažniausiai pridedate panašiose situacijose.

- „Priklijuojamieji“ numatytieji veiksmai tinkleliuose – šia funkcija užtikrinama, kad numatytasis veiksmas tinklelyje būtų susietas su konkrečiu stulpeliu tinklelyje, nepriklausomai nuo to, ar tas stulpelis yra perkeltas ar paslėptas.

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]