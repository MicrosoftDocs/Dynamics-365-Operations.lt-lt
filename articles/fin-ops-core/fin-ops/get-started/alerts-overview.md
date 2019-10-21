---
title: Įspėjimų apžvalga
description: Šioje temoje pateikiama bendra informacija apie įspėjimus. Įspėjimus galite naudoti, kad būtumėte informuoti apie įvykius, kuriuos norite sekti darbo dienos metu.
author: tjvass
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: a42e836c0b72798de3375c169e45b121debd55ec
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191275"
---
# <a name="alerts-overview"></a>Įspėjimų apžvalga

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a>Apie įspėjimus
Įspėjimai sistemoje sudaro pranešimo apie svarbius įvykius sistemą. Įspėjimus galite naudoti, kad būtumėte informuoti apie įvykius, kuriuos norite sekti darbo dienos metu. Galite lengvai kurti savo įspėjimų taisyklių rinkinį, kad jums būtų pranešama apie pavėluotus pristatymus, panaikintus užsakymus, pasikeitusias kainas ar kitus įvykius, į kuriuos reikia reaguoti.

Įmonės išteklių planavimui (ERP) būdingi keletas atvejų, kuriais galima naudoti įspėjimų funkciją. Štai keletas pavyzdžių.

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a>1 atvejis: naujų pardavimo užsakymų įspėjimo taisyklės kūrimas

1. Atidaryti puslapį **Visi pardavimo užsakymai**.
2. Veiksmų srityje, skirtuke **Parinktys**, grupėje **Bendrinti** pasirinkite **Kurti pasirinktinį įspėjimą**.
3. Dialogo lange **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane, kai** lauke **Įvykis** pasirinkite **Įrašas sukurtas**.

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a>2 atvejis: pristatymo datos nukėlimo įspėjimo taisyklės kūrimas

1. Atidaryti puslapį **Visi pirkimo užsakymai**.
2. Pasirinkite pirkimo užsakymo ID, kad pasiektumėte pirkimo užsakymo informaciją.
3. Išplėskite „FastTab“ **Pirkimo užsakymo antraštė**.
4. Veiksmų srityje, skirtuke **Parinktys**, grupėje **Bendrinti** pasirinkite **Kurti pasirinktinį įspėjimą**.
5. Dialogo lange **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane, kai** lauke **Laukas** pasirinkite **Pristatymo data**.
6. Lauke **Įvyks** pasirinkite **buvo atidėtas**.
    
Uždarius dialogo langą **Įspėjimo taisyklės kūrimas** taisyklė rodoma puslapyje **Įspėjimų taisyklių tvarkymas**. Puslapyje **Įspėjimų taisyklių tvarkymas** galite naujinti esamas įspėjimų taisykles. Pavyzdžiui, galite modifikuoti įvykių paleidiklius, atnaujinti įvykių pranešimus ir galiojimo datas. Norėdami atidaryti puslapį **Įspėjimų taisyklių tvarkymas**, naudokite mygtuką **Įspėti mane**, esantį veiksmų srities skirtuke **Parinktys**.

## <a name="what-occurs-when-an-alert-rule-is-created"></a>Kas įvyksta sukūrus įspėjimo taisyklę?

Kai kuriate įspėjimo taisykles, iš anksto numatytą įvykį susiejate su tam tikru lauku. Pavyzdžiui, ateina lauke nurodyta diena arba pasikeičia lauko turinys. Taip pat galite susieti įvykį su konkretaus puslapio įrašais. Pavyzdžiui, įrašas sukuriamas arba įrašas panaikinamas.

Kai įvyksta pasirinktas įvykis, susijęs su lauku arba puslapio įrašu, jums siunčiamas įspėjimas. Pavyzdžiui, sukuriate taisyklę ir susiejate konkrečios pirkimo užsakymo eilutės lauką **Pristatymo data** su įvykiu **praėjo prieš tiek laiko**. Nustatote penkių dienų laiko intervalą. Tokiu atveju įspėjimas siunčiamas praėjus 5 dienoms po tos pirkimo užsakymo eilutės pristatymo datos.

Be to, įspėjimo taisykles galite patobulinti nustatydami sąlygas. Pavyzdžiui, jus galima įspėti apie sukurtus naujus konkrečių tiekėjų kodų pirkimo užsakymus.

## <a name="preparing-for-an-alert"></a>Pasirengimas nustatyti įspėjimą

Prieš nustatydami įspėjimo taisyklę nuspręskite, kada ar kokiais atvejais norite gauti įspėjimus. Kai žinote, apie kokį įvykį norite būti įspėti, raskite puslapį, kuriame pateikiami duomenys, esantys to įvykio priežastimi. Įvykis gali būti tam tikra atėjusi diena arba atliktas konkretus pakeitimas. Todėl turite rasti puslapį, kuriame nurodyta data arba vietą, kurioje rodomas pasikeitęs laukas arba sukurtas naujas įrašas. Turėdami šią informaciją, galite kurti įspėjimo taisyklę.

## <a name="components-of-an-alert-rule"></a>Įspėjimo taisyklės komponentai

Įspėjimo taisyklę sudaro penki komponentai

- **Įvykis** – įvykis, kuris suaktyvina įspėjimo taisyklę, gali būti atėjusi tam tikra diena arba konkretus įvykęs pasikeitimas. Įvykiai nustatomi dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Siųsti el. pašto įspėjimus apie užduočių būsenų pasikeitimus**.
- **Sąlyga** – dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane dėl** galite pasirinkti sąlygos apimtį, kad valdytumėte, kada jus įspėti apie įvykius. Taisyklę galite taikyti tik esamam įrašui arba visiems puslapyje matomiems įrašams. Jei taisyklė bus taikoma visuose juridiniuose subjektuose, galite nustatyti parametro **Visoje organizacijoje** parinktį **Taip**.
- **Taisyklės galiojimo pabaiga** – dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane iki** galite nurodyti, kiek laiko įspėjimo taisyklė turėtų būti aktyvi.
- **Turinys** – dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti mane nurodant** galite nurodyti pranešimo temą ir tekstą, kurios bus naudojamos įspėjimų pranešimuose.
- **Vartotojas** – dialogo lango **Įspėjimo taisyklės kūrimas** „FastTab“ **Įspėti ką** galite nurodyti, kuris vartotojas turėtų gauti įspėjimo gauti įspėjimų pranešimus. Pagal numatytuosius parametrus pasirinktas jūsų vartotojo ID.

    > [!NOTE]
    > Šią parinktį gali naudoti tik organizacijos administratoriai.

## <a name="email-notifications-from-alerts"></a>Įspėjimų el. paštu siunčiami pranešimai

Įspėjimų el. paštu siunčiami pranešimai dar neįgalinti. Ši funkcija bus įgalinta būsimame naujinime.

## <a name="videos"></a>Vaizdo įrašai

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a>Kaip naudoti įspėjimus filtruojamiems duomenis stebėti

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3DWZ3]

Vaizdo įrašas [Kaip naudoti įspėjimus filtruojamiems duomenis stebėti](https://youtu.be/ZYKMcv6kl9s) (pateiktas pirmiau) yra įtrauktas į [„Finance and Operations” grojaraštį](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) „YouTube”.

### <a name="alert-rule-options"></a>Įspėjimo taisyklės parinktys

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3E4PV]

Vaizdo įrašas [Įspėjimo taisyklės parinktys](https://youtu.be/cpzimwOjicM) (pateiktas pirmiau) yra įtrauktas į [„Finance and Operations“ grojaraštį](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) „YouTube”.

