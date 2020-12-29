---
title: Rengimasis „Human Resources” įgyvendinimo pradžiai
description: Šiame puslapyje pateikiami nurodymai, kaip pasirengti „Dynamics 365 Human Resources” įgyvendinimui.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 59d7274c3b40e78209d90960c4514321b736876a
ms.sourcegitcommit: b40d6ce45aeb07724fc41d1a41923970b007fbcf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/14/2020
ms.locfileid: "4419795"
---
# <a name="prepare-for-human-resources-go-live"></a>Rengimasis „Human Resources” įgyvendinimo pradžiai

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip pasirengti „Dynamics 365 Human Resources” projekto įgyvendinimui naudojant „Microsoft Dynamics Lifecycle Services” (LCS). 

Šiame grafike parodyti įgyvendinimo proceso etapai. 

![Įgyvendinimo procesas](./media/hr-admin-go-live-prepare-process.png)

Toliau pateiktoje lentelėje pateikiami visi proceso veiksmai, numatoma trukmė ir už veiksmus atsakingi darbuotojai.

| Etapas | Veiksmas | Trukmė / kada | Kas | Pastabos |
| --- | --- | --- | --- |--- |
| 1 | Įgyvendinimo datos naujinimas LCS | Ne vėliau kaip likus 2-3 mėnesiams | Partneris / klientas | Etapų datos turi būti nuolat atnaujinamos. |
| 2 | Kontrolinio sąrašo užbaigimas ir siuntimas | Baigus vartotojo priėmimo testavimą (UAT) | Partneris / klientas | Sekite instrukcijas, pateiktas [„FastTrack” įgyvendinimo įvertinimas](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment). |
| 3 | Projekto įvertinimas („FastTrack”) | „FastTrack” architektas * | Architektas pateikia vertinimą po kontrolinio sąrašo gavimo ir tęsia peržiūrą, kol klausimai paaiškinami ir mažinimo veiksmai užbaigiami, jei jie taikomi. |
| 4 | Projekto seminaras („FastTrack”) | „FastTrack” architektas * | |
| 5 | Duomenų paketų importavimai | Priklauso nuo projekto | Partneris / klientas | Sekite instrukcijas, pateiktas [Duomenų valdymo apžvalga](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages).|
| 6 | Gamybos parengimas | Užbaigus visus ankstesnius veiksmus | Partneris / klientas | Partneris / klientas gali perimti gamybos aplinkos valdymą.|
| 7 | Perėjimo veiklos | Priklauso nuo projekto | Partneris / klientas | |
| 8 | Įgyvendinimo pradžia | Priklauso nuo projekto | Klientas | |

> [!IMPORTANT]
> * 3 ir 4 žingsniai yra užbaigti tik tiems klientams, kurie gali naudoti „FastTrack”.

## <a name="completing-the-lcs-methodology"></a>LCS metodikos užbaigimas

Pagrindinis kiekvieno įgyvendinimo projekto etapas yra perėjimas prie gamybos aplinkos. 

Siekiant padėti užtikrinti, kad gamybos aplinka būtų naudojama atliekant įgyvendinimo operacijas, „Microsoft” konfigūruoja gamybos egzempliorių tik tada, kai įgyvendinimas artėja prie etapo **Vykdymas** ir kai reikiamos LCS metodikos veiklos yra užbaigtos. Daugiau informacijos apie jūsų prenumeratos aplinkas žr.  [„Dynamics 365” licencijavimo vadovas](https://go.microsoft.com/fwlink/?LinkId=866544). 

Klientai turi užbaigti LCS metodikos etapus **Analizė**, **Kūrimas ir vystymas** ir **Testavimas** prieš atsirandant užklausos dėl gamybos aplinkos pateikimo mygtukui  **Konfigūruoti** . Norėdami baigti LCS etapą, pirmiausia turite užbaigti kiekvieną reikalingą to etapo veiksmą. Kai visi etapo veiksmai baigti, galite užbaigti visą etapą. Vėliau, jei reikia atlikti keitimus, galite bet kada iš naujo atidaryti etapą. Daugiau informacijos žr.  [„Lifecycle Services (LCS)“, skirtas „Finance and Operations“ programų klientams](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs). 

Veiksmo užbaigimo procesą sudaro dvi dalys: 

- Faktinio darbo, pvz., tinkamumo / trūkumų analizės arba vartotojo priėmimo testavimo (UAT), atlikimas. 
- Atitinkamo LCS metodikos veiksmo pažymėjimas kaip baigtas. 

Naudinga užbaigti metodikos veiksmus vykdant įgyvendinimą. Nelaukite iki paskutinės minutės. Negalima tiesiog spustelėti visų veiksmų, kad gamybos aplinka būtų gauta. Klientui naudinga turėti patikimą įgyvendinimą. 

## <a name="uat-for-your-solution"></a>Jūsų sprendimo UAT

UAT etapo metu turite tikrinti visus jūsų įdiegtus verslo procesus ir atliktus tinkinimus įgyvendinimo projekto smėlio dėžės aplinkoje. Norėdami užtikrinti sėkmingą įgyvendinimą, turite atkreipti dėmesį į toliau pateiktą informaciją, baigdami UAT etapą. 

- Testavimo atvejai apima visą reikalavimų aprėptį. 
- Testuokite naudodami perkeltus duomenis. Šiuose duomenyse turi būti pagrindiniai duomenys, pvz., darbuotojai, užduotys ir pareigos. Taip pat įtraukite pradinius balansus, pvz., atostogų ir neatvykimų kaupimus. Galiausiai įtraukite atidarytas operacijas, pvz., dabartinių išmokų registravimus. Atlikite testavimą naudodami visų tipų duomenis, net jei duomenų rinkiniai nėra baigti. 
- Testuokite naudodami teisingus saugos vaidmenis (numatytuosius ir pasirinktinius vaidmenis), priskirtus vartotojams. 
- Įsitikinkite, kad sprendimas atitinka bet kokius konkrečios įmonės ir konkrečios pramonės šakos reglamentavimo reikalavimus. 
- Dokumentuokite visas funkcijas ir gaukite kliento patvirtinimą bei išsiregistravimą. 

## <a name="fasttrack-go-live-assessment"></a>„FastTrack” įgyvendinimo įvertinimas

Klientai, galintys naudoti „FastTrack” ir dirbantys su „FastTrack” sprendimų architektu, atliks įgyvendinimo apžvalgą su „Microsoft FastTrack”. Daugiau informacijos žr.  [„Microsoft FastTrack“](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview). 

Likus aštuonioms savaitėms iki įgyvendinimo pradžios, „FastTrack” komanda paprašys jūsų užpildyti [įgyvendinimo kontrolinį sąrašą](https://go.microsoft.com/fwlink/?linkid=2146013).

Projekto vadovas arba pagrindinis projekto narys turi užbaigti įgyvendinimo kontrolinį sąrašą projekto pasirengimo įgyvendinimo pradžiai etapo metu. Paprastai kontrolinis sąrašas baigiamas likus keturioms – šešioms savaitėms iki siūlomos įgyvendinimo datos, kai UAT baigtas arba beveik baigtas. 

Baigę įgyvendinimo kontrolinį sąrašą, siųskite jį el. paštu jūsų „FastTrack” sprendimų architektui. El. laiške visada įtraukite kliento ir įgyvendinimo partnerio pagrindines suinteresuotąsias šalis. 

Pateikus kontrolinį sąrašą, jūsų „FastTrack” sprendimų architektas peržiūrės projektą ir pateiks įvertinimą, aprašantį galimą riziką, geriausią praktiką ir rekomendacijas sėkmingam projekto įgyvendinimui atlikti. Kai kuriais atvejais sprendimų architektas gali akcentuoti rizikos veiksnius ir prašyti mažinimo plano. 

## <a name="see-also"></a>Taip pat žiūrėkite

[DUK apie įgyvendinimo pradžią](hr-admin-go-live-faq.md)