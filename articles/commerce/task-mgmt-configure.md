---
title: Užduočių valdymo konfigūravimas
description: Šiame straipsnyje aprašoma, kaip konfigūruoti užduočių valdymo funkcijas dalyje Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.search.industry: ''
ms.openlocfilehash: cc2d75f52b183559de344982c8e4208000af786e
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746068"
---
# <a name="configure-task-management"></a>Užduočių valdymo konfigūravimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip konfigūruoti užduočių valdymo funkcijas dalyje Microsoft Dynamics 365 Commerce.

Prieš „Dynamics 365 Commerce” vadybininkams ir darbuotojams pradedant naudotis „Commerce“ užduočių valdymo funkcijomis, reikia sukonfigūruoti užduočių valdymą. Konfigūruojant atliekami tokie veiksmai: teisių suteikimas vadybininkams ir darbuotojams, teisių paskirstymas elektroninio kasos aparato (EKA) klientams, EKA pranešimų nustatymas ir plytelės **Užduotys** konfigūravimas EKA programos pagrindiniame puslapyje.

## <a name="configure-permissions-for-store-managers"></a>Parduotuvių vadybininkų teisių konfigūravimas

Kiekvienas konkrečioje parduotuvėje dirbantis darbuotojas gali peržiūrėti visas šiai parduotuvei priskirtas užduotis. Jis taip pat gali naujinti jam priskirtų užduočių būsenas. Tačiau tokie asmenys, kaip parduotuvės vadybininkai, privalo turėti užduočių valdymo teises, kad galėtų valdyti parduotuvei priskirtas užduotis ir kurti vienos paskirties užduotis.

Norėdami konfigūruoti parduotuvių vadybininkų užduočių valdymo teises, atlikite toliau pateikiamus veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Darbuotojai \> Teisių grupės**.
1. Pasirinkite konkrečią teisių grupę (pvz., **Vadybininkas**), tada pasirinkite **Redaguoti**.
1. „FastTab“ skirtuke **Teisės** parinktyje **Leisti užduočių valdymą** nustatykite **Taip**.
1. „FastTab“ skirtuke **Pranešimai** įtraukite operaciją **Užduočių valdymas** ir lauke **Rodyti užsakymą** įveskite vertę. Pavyzdžiui, įveskite **2**, jei operacijoje **Užsakymo įvykdymas** jau yra lauko **Rodyti užsakymą** reikšmė **1**.
    
> [!NOTE]
> Jei ne vadybininkai privalo turėti EKA užduočių valdymo teisių, galite suteikti teisę atskiram asmeniui. Arba galite sukurti naują ne vadybininkams skirtą leidimų grupę ir parinktyje **Leisti užduočių valdymą** nustatyti **Taip**.

Toliau pateiktame paveikslėlyje vaizduojama, kaip konfigūruoti parduotuvių vadybininkų užduočių valdymo teises.

![Parduotuvių vadybininkų užduočių valdymo teisių konfigūravimas.](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a>Darbuotojų teisių konfigūravimas

Darbuotojai privalo turėti teises, kad galėtų kurti užduočių sąrašus, valdyti priskyrimo kriterijus ir konfigūruoti užduočių sąrašo pasikartojimą. Norėdami konfigūruoti šias teises, turite priskirti darbuotojams vaidmenį **Mažmeninės prekybos užduočių vadovas**.

Norėdami konfigūruoti darbuotojo teises, atlikite tolesnius veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Darbuotojai \> Vartotojai**.
1. Pasirinkite darbuotoją.
1. „FastTab“ skirtuke **Vartotojo vaidmenys** pasirinkite **Priskirti vaidmenis**.
1. Dialogo lange **Priskirti vaidmenis vartotojui** pasirinkite vaidmenį **Mažmeninės prekybos užduočių vadovas**, tada pasirinkite **Gerai**.

## <a name="distribute-permissions-to-pos-clients"></a>Teisių EKA klientams paskirstymas

Prieš darbuotojams pradedant naudotis EKA klientais, šių klientų teisės turi būti paskirstytos ir sinchronizuotos.

Norėdami paskirstyti teises EKA klientams, atlikite toliau pateikiamus veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**.
1. Pasirinkite paskirstymo grafiką **1060** (**Darbuotojai**), tada pasirinkite **Vykdyti dabar**.
1. Pasirinkite paskirstymo grafiką **1070** (**Kanalo konfigūracija**), tada pasirinkite **Vykdyti dabar**.

## <a name="configure-pos-notifications-for-tasks"></a>Užduotims skirtų EKA pranešimų konfigūravimas

Užduočių valdymas turi būti sukonfigūruotas taip, kad pranešimai būtų pasiekiami EKA programoje.

Norėdami konfigūruoti EKA pranešimus užduotims, atlikite tolesnius veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA \> EKA operacijos**.
1. Raskite operaciją **1400** (**Užduočių valdymas**) ir pažymėkite žymės langelį **Įjungti pranešimus**.

Toliau pateiktame paveikslėlyje rodoma operacija **Užduočių valdymas** puslapyje **EKA operacijos**.

![Užduočių valdymo operacija EKA operacijų puslapyje.](media/HQ-POS-Tasks-Notifications.png)

Norėdami gauti daugiau informacijos apie EKA pranešimų konfigūravimą, [žr. el. kasos orderio (EKA) straipsnyje Rodyti užsakymų pranešimus](notifications-pos.md).

> [!NOTE]
> Kai įrašysite pakeitimus, bus rodomas šis perspėjimo pranešimas: **Mygtukyno konstruktoriuje operacijos parametras nebus įgalintas operacijos ID, lygus arba mažesnis nei 4000. Jei kuriate pasirinktinę operaciją ir norite perduoti parametrą iš mygtukyno dizainerio, naudokite operacijos ID, didesnį nei 4000.** Pasirinkti Uždaryti **,** kad būtų uždarytas dialogas.


## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a>Plytelės Užduotys EKA programos pagrindiniame puslapyje konfigūravimas

Prieš konfigūruodami plytelę **Užduotys** EKA programos pagrindiniame puslapyje, žr. [Elektroninio kasos aparato (EKA) ekrano maketai](pos-screen-layouts.md), kad sužinotumėte, kaip konfigūruoti ir įtraukti naujų mygtukų į EKA ekrano maketą.

Norėdami konfigūruoti plytelę **Užduotys** EKA programos pagrindiniame puslapyje, atlikite tolesnius veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA \> Ekrano maketai**.
1. Pasirinkite ekrano maketą, maketo dydį ir mygtukyną.
1. „FastTab“ skirtuke **Mygtukynas** pasirinkite **Dizaineris**, kad redaguotumėte pasirinktą mygtukyną.
1. Įtraukite plytelę **Užduotys** į atitinkamą pagrindinio ekrano skyrių.

Toliau pateikiamoje iliustracijoje rodomas plytelės **Užduotys** EKA pagrindiniame puslapyje pavyzdys.

![Plytelė Užduotys EKA pagrindiniame puslapyje.](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Užduočių valdymo apžvalga](task-mgmt-overview.md)

[Užduočių sąrašų kūrimas ir užduočių įtraukimas](task-mgmt-create-lists.md)

[Užduočių sąrašų priskyrimas parduotuvėms arba darbuotojams](task-mgmt-assign-lists.md)

[Užduočių valdymas EKA programoje](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
