---
title: Rengimasis „Human Resources” įgyvendinimo pradžiai
description: Šiame puslapyje pateikiami nurodymai, kaip pasirengti „Dynamics 365 Human Resources” įgyvendinimui.
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 196d843ce3ccacc203896439b8c66f168c75bdc945c9b2cd5f9bdd46a2cc3ddd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744899"
---
# <a name="prepare-for-human-resources-go-live"></a>Rengimasis „Human Resources” įgyvendinimo pradžiai

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip pasirengti „Dynamics 365 Human Resources” projekto įgyvendinimui naudojant „Microsoft Dynamics Lifecycle Services” (LCS). 

Šiame grafike parodyti įgyvendinimo proceso etapai. 

![Įgyvendinimo procesas.](./media/hr-admin-go-live-prepare-process.png)

Toliau pateiktoje lentelėje pateikiami visi proceso veiksmai, numatoma trukmė ir už veiksmus atsakingi darbuotojai.

| Etapas | Veiksmas | Trukmė / kada | Kas | Pastabos |
| --- | --- | --- | --- |--- |
| 1 | Įgyvendinimo datos naujinimas LCS | Ne vėliau kaip likus 2-3 mėnesiams | Partneris / klientas | Etapų datos turi būti nuolat atnaujinamos. |
| 2 | Kontrolinio sąrašo užbaigimas ir siuntimas | Baigus vartotojo priėmimo testavimą (UAT) | Partneris / klientas | Sekite instrukcijas, pateiktas [„FastTrack” įgyvendinimo įvertinimas](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment). |
| 3 | Projekto įvertinimas („FastTrack”) | „FastTrack” architektas * | Architektas pateikia vertinimą po kontrolinio sąrašo gavimo ir tęsia peržiūrą, kol klausimai paaiškinami ir mažinimo veiksmai užbaigiami, jei jie taikomi. |
| 4 | Projekto seminaras („FastTrack”) | „FastTrack” architektas * | |
| 5 | Duomenų paketų importavimai | Priklauso nuo projekto | Partneris / klientas | Sekite instrukcijas, pateiktas [Duomenų valdymo apžvalga](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).|
| 6 | Gamybos parengimas | Užbaigus visus ankstesnius veiksmus | Partneris / klientas | Partneris / klientas gali perimti gamybos aplinkos valdymą.|
| 7 | Perėjimo veiklos | Priklauso nuo projekto | Partneris / klientas | |
| 8 | Įgyvendinimo pradžia | Priklauso nuo projekto | Klientas | |

> [!IMPORTANT]
> * 3 ir 4 žingsniai yra užbaigti tik tiems klientams, kurie gali naudoti „FastTrack”.

## <a name="completing-the-lcs-methodology"></a>LCS metodikos užbaigimas

Pagrindinis kiekvieno įgyvendinimo projekto etapas yra perėjimas prie gamybos aplinkos. Veiksmo užbaigimo procesą sudaro dvi dalys: 

- Faktinio darbo, pvz., tinkamumo / trūkumų analizės arba vartotojo priėmimo testavimo (UAT), atlikimas. 
- Atitinkamo LCS metodikos veiksmo pažymėjimas kaip baigtas. 

Naudinga užbaigti metodikos veiksmus vykdant įgyvendinimą. Nelaukite iki paskutinės minutės. Klientui naudinga turėti patikimą įgyvendinimą. 

## <a name="uat-for-your-solution"></a>Jūsų sprendimo UAT

UAT etapo metu turite tikrinti visus jūsų įdiegtus verslo procesus ir atliktus tinkinimus įgyvendinimo projekto smėlio dėžės aplinkoje. Norėdami užtikrinti sėkmingą įgyvendinimą, turite atkreipti dėmesį į toliau pateiktą informaciją, baigdami UAT etapą. 

- Rekomenduojame, kad jūsų UAT procesas prasidėtų su švaria ir šviežia aplinka, kurioje duomenys iš jūsų GOLD konfigūracijos būtų nukopijuoti į aplinką prieš UAT proceso pradžią. Rekomenduojame jums naudoti gamybos aplinką, nes jūsų GOLD aplinka iki jūsų paleidimo į internetą, į kurią taiko aplinka, tampa gamyba.
- Testavimo atvejai apima visą reikalavimų aprėptį. 
- Testuokite naudodami perkeltus duomenis. Tai turėtų apimti tokius duomenis, kaip darbuotojai, užduotys ir pareigos. Taip pat įtraukite pradinius balansus, pvz., atostogų ir neatvykimų kaupimus. Galiausiai įtraukite atidarytas operacijas, pvz., dabartinių išmokų registravimus. Atlikite testavimą naudodami visų tipų duomenis, net jei duomenų rinkiniai nėra baigti. 
- Testuokite naudodami teisingus saugos vaidmenis (numatytuosius ir pasirinktinius vaidmenis), priskirtus vartotojams. 
- Įsitikinkite, kad sprendimas atitinka bet kokius konkrečios įmonės ir konkrečios pramonės šakos reglamentavimo reikalavimus. 
- Dokumentuokite visas funkcijas ir gaukite kliento patvirtinimą bei išsiregistravimą. 

## <a name="mock-go-live"></a>Netikras paleidimas į internetą

Prieš jūsų paleidimą į internetą, turite atlikti netikrą paleidimą siekiant išbandyti žingsnius, kurių reikia nukirpti jūsų ankstesnę sistemą į naują sistemą. Turite atlikti savo netikrą paleidimą smėlio dėžės aplinkoje ir apimti visus žingsnius jūsų pjovimo plane.

- Rekomenduojame jums naudoti gamybos aplinką kaip GOLD konfigūravimo aplinką iki paleidžiant į internetą.
- Įsitikinkite, kad turite stiprų valdymo procesą siekiant apsaugoti gamybos aplinką nuo atsitiktinių transakcijų ar naujinimų prieš paleidimą į internetą.
- Jums pasirengus atlikti UAT ar netikrą paleidimą į internetą, atnaujinkite smėlio dėžės aplinką iš gamybos aplinkos. Dėl daugiau informacijos, žr. [Kopijuoti elementą](hr-admin-setup-copy-instance.md).
- Bandykite kiekvieną savo nupjovimo plano žingsnį smėlio dėžės aplinkoje ir tuomet patvirtinkite smėlio dėžės aplinką atlikdami vietų patikras ar atlikdami testus iš jūsų UAT scenarijų aplinkoje.
  - Bandymai turi apimti visus duomenų perkėlimus, įskaitant transformacija, kurių reikia paleisti į internetą.
  - Procesas turi apimti visų senų sistemų praktikos nupjovimą.
  - Įsitikinkite, kad apėmėte visus integravimo nupjovimo žingsnius ar išorės sistemų žingsnius jūsų netikrame nupjovime.
- Jei radote bet kokių problemų netikrame nupjovime, gali reikėti antro netikro nupjovimo. Dėl to, rekomenduojame suplanuoti du netikrus nupjovimus jūsų projekto plane.

## <a name="fasttrack-go-live-assessment"></a>„FastTrack” įgyvendinimo įvertinimas

Klientai, galintys naudoti „FastTrack” ir dirbantys su „FastTrack” sprendimų architektu, atliks įgyvendinimo apžvalgą su „Microsoft FastTrack”. Daugiau informacijos žr.  [„Microsoft FastTrack“](/dynamics365/fasttrack/). 

Likus aštuonioms savaitėms iki įgyvendinimo pradžios, „FastTrack” komanda paprašys jūsų užpildyti [įgyvendinimo kontrolinį sąrašą](https://go.microsoft.com/fwlink/?linkid=2146013).

Projekto vadovas arba pagrindinis projekto narys turi užbaigti įgyvendinimo kontrolinį sąrašą projekto pasirengimo įgyvendinimo pradžiai etapo metu. Paprastai kontrolinis sąrašas baigiamas likus keturioms – šešioms savaitėms iki siūlomos įgyvendinimo datos, kai UAT baigtas arba beveik baigtas. 

Baigę įgyvendinimo kontrolinį sąrašą, siųskite jį el. paštu jūsų „FastTrack” sprendimų architektui. El. laiške visada įtraukite kliento ir įgyvendinimo partnerio pagrindines suinteresuotąsias šalis. 

Pateikus kontrolinį sąrašą, jūsų „FastTrack” sprendimų architektas peržiūrės projektą ir pateiks įvertinimą, aprašantį galimą riziką, geriausią praktiką ir rekomendacijas sėkmingam projekto įgyvendinimui atlikti. Kai kuriais atvejais sprendimų architektas gali akcentuoti rizikos veiksnius ir prašyti mažinimo plano. 

## <a name="see-also"></a>Taip pat žiūrėkite

[DUK apie įgyvendinimo pradžią](hr-admin-go-live-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
