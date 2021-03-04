---
title: Vartotojų teisių nustatymas „Attract“
description: Šioje temoje pateikiama informacija apie vaidmenų saugą „Microsoft“ „Dynamics 365 Talent – Attract“.
author: andreabichsel
manager: AnnBe
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: efac512cfa07bb2183f06b8be45f74bef9af0767
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461983"
---
# <a name="set-user-permissions-in-attract"></a>Vartotojų teisių nustatymas „Attract“

[!include [banner](includes/banner.md)]

„Microsoft“ „Dynamics 365 Talent: Attract“ naudojama vaidmenimis pagrįsta sauga. Kitaip tariant, prieiga nėra suteikiama atskiriems vartotojams, o tik saugos vaidmenims, kuriems vartotojai priskirti. Vartotojas, kuris yra priskirtas saugos vaidmeniui, turi prieigą prie teisių, kurios susietos su tuo vaidmeniu, rinkinio.

„Attract“ pateikia penkis pagrindinius vartotojų vaidmenis:

- Administratorius
- Samdos vadovas
- Įdarbintojas
- Kalbintojas
- Tik skaitoma

Administratoriaus vaidmuo yra vienintelis vaidmuo, kuris suteikia teisę įtraukti kitų vartotojų ir pakeisti jų teises.

- **Įtraukti** – Administravimo centre skirtuke **Vartotojo teisės** pasirinkite **Priskirti vaidmenis**, suraskite norimą įtraukti vartotoją ir priskirkite jam teisių.
- **Redaguoti** – Ieškokite vartotojo arba suraskite jį sąraše ir pasirinkite **Redaguoti**, kad pakeistumėte jo teises.
- **Naikinti** – Panaikinus vartotojo teises, vartotojas iš sistemos nepašalinamas. Tačiau apribojama vartotojo prieiga ir teisės programoje „Attract“. Pvz., Hilda buvo priskirta samdos vadovo vaidmeniui ir ji įtraukta į užduotį kaip samdos vadovė. Jei vėliau Hilda pašalinama iš samdos vadovo vaidmens, ji lieka kaip samdos vadovė užduotyje ir prie jos vis dar turi prieigą. Tačiau ji negali sukurti kitų užduočių.

Šiuose skyriuose pateikiami išsamūs kiekvieno vaidmens aprašai. Toliau temoje esančiose lentelėse pateikiama išsamesnės informacijos.

> [!NOTE]
> Kai kurias funkcijas galima naudoti tik kartu su išsamios įdarbinimo informacijos priedu, skirtu „Attract“.

## <a name="administrator"></a>Administratorius

Vartotojai, kurie priskirti administratoriaus vaidmeniui, gali pasiekti ir pakeisti visus „Attract“ duomenis. Administratoriai gali kurti, skaityti, atnaujinti ir panaikinti duomenis. Jie taip pat turi prieigą prie administravimo centro, kur gali konfigūruoti programą „Attract“ ir nustatyti vartotojų informaciją. Rekomenduojame priskirti bent vieną asmenį administratoriaus vaidmeniui. Pagal numatytuosius parametrus „Microsoft Power Apps“ aplinkos administratorius nustatytas kaip administratorius ir programoje „Attract“. Jei prisiregistravote naudoti bandomąją „Attract“ versiją, administratoriaus vaidmuo jums priskirtas automatiškai. Šiuo metu norėdami kurti užduotis vartotojai, turintys administratoriaus vaidmenį, turi turėti ir įdarbintojo arba samdos vadovo vaidmenį.

## <a name="hiring-manager"></a>Samdos vadovas

Vartotojai, kurie priskirti samdos vadovo vaidmeniui, gali kurti užduotis ir atnaujinti anksčiau savo sukurtas užduotis. Samdos vadovai gali atlikti tik tam tikrus veiksmus užduotyje ir programose, susijusiose su ta užduotimi. Tik tie vartotojai, kurie priskirti samdos vadovo vaidmeniui, gali būti įtraukti į samdos komandą kaip samdos vadovai.

## <a name="recruiter-role"></a>Įdarbintojo vaidmuo

Vartotojai, kurie priskirti įdarbintojo vaidmeniui, turi visas skaitymo, kūrimo, atnaujinimo ir naikinimo teises užduotyse, kurias jie sukūrė. Jie taip pat turi visas kūrimo, skaitymo, atnaujinimo ir naikinimo teises programose, susijusiose su jų turimomis užduotimis. Tik tie vartotojai, kurie priskirti įdarbintojo vaidmeniui, gali būti įtraukti į samdos komandą kaip įdarbintojai.

## <a name="interviewer"></a>Interviu ėmėjas

Bet kuris vartotojas, kuris turi organizacijoje „Microsoft Azure Active Directory“ („Azure AD“) paskyrą, gali būti įtrauktas į samdos komandą kaip kalbintojas. Vartotojai, kurie priskirti kalbintojo vaidmeniui, gali peržiūrėti užduoties informaciją ir pretendento duomenis tų užduočių, kurių samdos komandose jie yra. Šių užduočių mastu kalbintojai gali pateikti įdarbinimo rekomendacijų ir atsiliepimų apie kandidatus. Tačiau jie negali atnaujinti užduoties informacijos arba pretendento duomenų.

## <a name="read-only"></a>Tik skaitoma

Vartotojai, kurie priskirti vaidmeniui Tik skaityti, turi tik skaitymo prieigą prie visų duomenų „Attract“ aplinkoje. Tačiau jie negali kurti ar redaguoti jokių duomenų.

## <a name="find-out-which-roles-you-have"></a>Sužinokite, kokie vaidmenys jums priskirti

1.  Viršutiniame dešiniajame „Attract“ puslapio kampe spustelėkite klaustuką (**?**).

2.  Spustelėkite **Apie**.

    Pasirodžiusiame lange pamatysite, kokie „Attract“ vaidmenys jums priskirti.

    ![Peržiūrėkite, kokio tipo „Attract“ licenciją turite](media/attract-license-types.png)
    
## <a name="delegated-roles"></a>Perduoti vaidmenys

Įdarbintojai ir samdos vadovai užduočiai, kurios samdos komandoje jie yra, gali deleguoti vieną ar daugiau asmenų vietoj savęs. Tačiau jie negali paskirti kitų samdos komandoje esančių žmonių atstovų.

Perėmėjai turi tas pačias teises kaip ir asmuo, kuris jiems tas teises perdavė. Pvz., jei samdos vadovė užduočiai paskiria perėmėją už save, perėmėjas užduotyje turės tas pačias teises, kokias turėjo ta samdos vadovė. Perėmėjai kitų perėmėjų iš samdos komandos pašalinti negali. Jie taip pat negali pašalinti žmonių, kurie juos paskyrė kaip perėmėjus.

## <a name="job-details-and-actions"></a>Užduoties informacija ir veiksmai

Vartotojai, turintys įdarbintojo ar samdos vadovo vaidmenį, gali kurti užduotis. Toliau išvardytos teisės, kurios taikomos užduoties informacijai, ir veiksmai, kuriuos galima atlikti užduotyje.

| Duomenys arba veiksmas    | Įdarbintojas | Samdos vadovas | Kalbintojas |
|-------------------|-----------|----------------|-------------|
| Darbo informacija       | Kurti, skaityti, atnaujinti ir panaikinti užduotis, kurių samdos komandoms vartotojas priklauso | Kurti, skaityti, atnaujinti ir panaikinti užduotis, kurių samdos komandoms vartotojas priklauso | Tik skaitoma |
| Samdos komanda       | Kurti, skaityti, atnaujinti ir panaikinti užduotis, kurių samdos komandoms vartotojas priklauso | Kurti, skaityti, atnaujinti ir panaikinti užduotis, kurių samdos komandoms vartotojas priklauso | Tik skaitoma |
| Užduočių registravimas       | Kurti, skaityti, atnaujinti ir panaikinti užduotis, kurių samdos komandoms vartotojas priklauso | Tik skaitoma | Tik skaitoma |
| Procesas           | Kurti, skaityti, atnaujinti ir panaikinti užduotis, kurių samdos komandoms vartotojas priklauso | Kurti, skaityti, atnaujinti ir panaikinti užduotis, kurių samdos komandoms vartotojas priklauso | Tik skaitoma |
| Įtraukti pretendentų    | Įtraukti pretendentus į užduotis, kurių samdos komandoms vartotojas priklauso | Įtraukti pretendentus į užduotis, kurių samdos komandoms vartotojas priklauso | Neleidžiama |
| Įtraukti kandidatų     | Įtraukti kandidatus į užduotis, kurių samdos komandoms vartotojas priklauso | Konfigūracijos parinktimi, esančia [potencialaus kliento veiklos nustatymas](./activities-attract.md#prospect-activity), valdoma kalbintojo teisė įtraukti ir peržiūrėti potencialius klientus. | Neleidžiama |
| Aktyvinti užduotį      | Aktyvinti užduotis, kurių samdos komandoms vartotojas priklauso | Aktyvinti užduotis, kurių samdos komandoms vartotojas priklauso | Neleidžiama |
| Uždaryti užduotį         | Uždaryti užduotis, kurių samdos komandoms vartotojas priklauso | Neleidžiama | Neleidžiama |
| Naikinti užduotį        | Panaikinti užduotis, kurių samdos komandoms vartotojas priklauso | Tik tada, jei nėra įtraukta nė vieno pretendento į tą užduotį | Neleidžiama |
| Panaikinti pretendentus | Panaikinti pretendentus, jei vartotojas priklauso samdos komandai | Neleidžiama | Neleidžiama |

## <a name="application-details-and-actions"></a>Prašymų informacija ir veiksmai

Toliau išvardytos teisės, kurios taikomos užduočiai būdingiems pretendentų duomenims, ir veiksmai, kuriuos galima atlikti su pretendentais.

| Duomenys arba veiksmas          | Įdarbintojas | Samdos vadovas | Kalbintojas |
|-------------------------|-----------|----------------|-------------|
| Prašymo dokumentai   | Kurti, skaityti, atnaujinti ir panaikinti užduotis, kurių samdos komandoms vartotojas priklauso | Kurti, skaityti, atnaujinti ir panaikinti užduotis, kurių samdos komandoms vartotojas priklauso | Tik skaitoma |
| Prašymo pastabos       | Kurti, skaityti, atnaujinti ir panaikinti užduotis, kurių samdos komandoms vartotojas priklauso | Kurti, skaityti, atnaujinti ir panaikinti užduotis, kurių samdos komandoms vartotojas priklauso | Tik skaityti|
| Prašymo veikla    | Peržiūrėti, jei vartotojas priklauso samdos komandai | Peržiūrėti, jei vartotojas priklauso samdos komandai | Tik skaitoma |
| Nuomonė apie prašymą    | Įtraukti ir peržiūrėti visas nuomones, jei vartotojas priklauso nuomos komandai | Įtraukti ir peržiūrėti visas nuomones, jei vartotojas priklauso nuomos komandai | Gali įtraukti nuomonę\*\* |
| Atmesti prašymą      | Gali atmesti, jei vartotojas priklauso samdos komandai | Neleidžiama | Neleidžiama |
| Perkelti į kitą etapą           | Gali atmesti, jei vartotojas priklauso samdos komandai | Gali perduoti toliau, jei vartotojas priklauso samdos komandai | Neleidžiama |
| Pradėti pasiūlymo valdymą | Gali pradėti pasiūlymo valdymą | Galima naudoti konfigūracijos parinktį pasiūlymo veikloje. | Neleidžiama |


\*\*Konfigūracijos parinktimi, esančia [nuomonės veiklos sąrankoje](./activities-attract.md), galima valdyti kalbintojų galimybę matyti vienas kito nuomonę.


## <a name="process-templates"></a>Proceso šablonai

Šios teisės taikomos samdos procesų šablonams. Komandos narių galimybė kurti ir redaguoti šablonus sukonfigūruota administravimo centro dalyje **Šablonų valdymas** . Jei šablono valdymas įjungtas, įdarbintojai ir samdos vadovai gali kurti ir redaguoti savo procesų šablonus. Jei šablonų valdymas yra išjungtas, tik administratoriai gali kurti ir redaguoti procesų šablonus. Toliau pateikiama lentelėje, kai laikoma, kad šablonų valdymas, įjungtas.

| Duomenys              | Įdarbintojas                                           | Samdos vadovas                                      | Kalbintojas |
|-------------------|-----------------------------------------------------|-----------------------------------------------------|-------------|
| Proceso šablonai | Visos teisės į šablonus, kuriuos vartotojas sukuria | Visos teisės į šablonus, kuriuos vartotojas sukuria | Nėra prieigos   |

## <a name="email-and-email-templates"></a>El. paštas ir el. pašto šablonai

Toliau išvardytos teisės, kurios taikomos el. pašto šablonams, ir veiksmai, kuriuos galima atlikti el. pašte. Tik administratoriai gali kurti ir redaguoti el. pašto šablonus.

| Duomenys arba veiksmas     | Įdarbintojas          | Samdos vadovas     | Kalbintojas |
|--------------------|--------------------|--------------------|-------------|
| El. laiško šablonai    | Tik skaityti leidžianti prieiga   | Tik skaityti leidžianti prieiga   | Nėra prieigos   |
| Siųsti el. laišką         | Siuntimas per veiklą  | Siuntimas per veiklą  | Nėra prieigos   |
| Redaguoti el. laiško turinį | Redaguoti el. laiško turinį | Redaguoti el. laiško turinį | Nėra prieigos   |

## <a name="talent-pools"></a>Talentų telkiniai

Šios teisės taikomos talentų telkiniams. Talentų telkiniai yra matomi tik tiems asmenims, kurie juos sukūrė, išskyrus atvejus, kai tie asmenys pasirenka juos bendrinti. Kandidatų iešką galima naudoti kandidatams, kurie neįtraukti į įvardytą telkinį, ieškoti.

| Duomenys arba veiksmas   | Įdarbintojas                                       | Samdos vadovas                                  | Kalbintojas |
|------------------|-------------------------------------------------|-------------------------------------------------|-------------|
| Įvardytas telkinys       | Visos teisės į telkinius, kuriuos vartotojas sukuria | Visos teisės į telkinius, kuriuos vartotojas sukuria | Nėra prieigos   |
| Bendrinti telkinį       | Tik telkiniai, kuriuos sukūrė vartotojas                | Tik telkiniai, kuriuos sukūrė vartotojas                | Nėra prieigos   |
| Kandidatų ieška | Visos ieškos galimybes                        | Visos ieškos galimybes                        | Nėra prieigos   |

## <a name="candidates"></a>Kandidatai

Kandidatai yra žmonės, kurie buvo įtraukti į talentų telkinį, bet nėra susieti su užduotimi.

| Duomenys                        | Įdarbintojas                        | Samdos vadovas                   | Kalbintojas |
|-----------------------------|----------------------------------|----------------------------------|-------------|
| Profilis – kandidato informacija | Kurti, skaityti, atnaujinti ir panaikinti | Kurti, skaityti, atnaujinti ir panaikinti | Nėra prieigos   |
| Dokumentai                   | Kurti, skaityti, atnaujinti ir panaikinti | Kurti, skaityti, atnaujinti ir panaikinti | Nėra prieigos   |


[!INCLUDE[footer-include](../includes/footer-banner.md)]