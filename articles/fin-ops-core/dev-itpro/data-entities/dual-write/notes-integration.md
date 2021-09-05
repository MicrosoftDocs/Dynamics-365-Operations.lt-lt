---
title: Pastabų integravimas
description: Šioje temoje aprašomas pastabų duomenų integravimas dvigubo rašymo funkcijoje.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e850b44479d36c16db3c993e196cd6bfdbc52ee7
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416606"
---
# <a name="note-integration"></a>Pastabų integravimas

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Verslo procesų metu „Microsoft Dynamics 365” vartotojai dažnai renka informaciją apie savo klientus. Ši informacija įrašoma kaip veiklos ir pastabos. Šioje temoje aprašomas pastabų duomenų integravimas dvigubo rašymo funkcijoje.

Kliento informaciją galima klasifikuoti toliau pateiktais būdais.

+ **Veiksminga informacija, kurią „Dynamics 365“ vartotojas valdo kliento vardu** – Pavyzdžiui, „Contoso“ („Dynamics 365“ vartotojas) veda žaidimų šou. Vienas Iš „Contoso“ klientų (klientas) nori dalyvauti žaidimų šou. Klientas paprašo „Contoso“ darbuotojo rezervuoti jam vietą žaidimų šou. Rezervavimas įvyksta „Contoso“ įvykių dalyvio kalendoriuje.
+ **Veiksminga „Dynamics 365” vartotojo informacija** – pvz., klientas, perkantis „Surface” vienetą, įveda specialias instrukcijas, nurodančias, kad prieš pristatant įrenginį reikia supakuoti kaip dovaną. Šios instrukcijos yra veiksmingos informacijos, kurią turi valdyti „Contoso“ darbuotojas, atsakingas už pakavimą.
+ **Neveiksminga informacija** – pvz., klientas lankosi „Contoso“ parduotuvėje ir pokalbio su parduotuvės atstovu metu išreiškia susidomėjimą *„Halo“* žaidimais bei žaidimų priedais. Parduotuvės atstovas pasižymi šios informacijos pastabą. Tada produktų rekomendacijų mechanizmas ją naudoja, kad klientui pateiktų rekomendacijas.

Apskritai, veiksminga informacija fiksuojama kaip *veiklos* „Finance and Operations” bei klientų įtraukimo programose. Neveiksminga informacija fiksuojama kaip *pastabos* „Finance and Operations” programose arba kaip *komentarai* klientų įtraukimo programose.

> [!TIP]
> Nors pastabos skirtos neveiksmingai informacijai, programos netrukdys jomis naudotis saugant ir valdant veiksmingą informaciją, jei norite jas naudoti tokiu būdu.

„Microsoft” šiuo metu leidžia pastabų integravimo funkcijas. (Veiklos integravimo funkcijos bus išleistos vėliau.) Pastabų integravimą galima naudoti dirbant su klientais, tiekėjais, pardavimo užsakymais ir pirkimo užsakymais.

## <a name="create-a-note-in-a-customer-engagement-app"></a>Pastabos kūrimas klientų įtraukimo programoje

Norėdami sukurti pastabą klientų įtraukimo programoje ir tada sinchronizuoti ją su „Finance and Operations” programa, atlikite šiuos veiksmus.

1. Klientų įtraukimo programoje atidarykite kliento abonemento įrašą.
2. Srityje **Laiko juosta** pasirinkite pliuso ženklą (**+**), tada, norėdami sukurti pastabą, pasirinkite **Pastaba**.

    ![Pastabos kūrimas klientų įtraukimo programoje.](media/notes-ce-1.png)

3. Įveskite pavadinimą ir aprašymą, tada pasirinkite **Įtraukti pastabą**.

    ![Pavadinimo ir aprašymo įvedimas.](media/notes-ce-2.png)

    Nauja pastaba įtraukiama į kliento laiko juostą.

    ![Nauja pastaba kliento laiko juostoje.](media/notes-ce-3.png)

4. Prisijunkite prie „Finance and Operations” programos ir atidarykite tą patį kliento įrašą. Atkreipkite dėmesį, kad viršutiniame dešiniajame kampe esantis mygtukas **Priedai** (sąvaržėlės simbolis) nurodo, kad įrašas turi priedą.

    ![Pranešimas apie priedą.](media/notes-ce-4.png)

5. Pasirinkite mygtuką **Priedai**, kad atidarytumėte puslapį **Priedai**. Turėtumėte rasti pastabą, kurią sukūrėte klientų įtraukimo programoje.

    ![Pastaba iš „Customer Engagement” programos.](media/notes-ce-5.png)

Visi pastabos atnaujinimai sinchronizuojami tarp „Finance and Operations” programos ir klientų įtraukimo programos.

## <a name="create-a-note-in-a-finance-and-operations-app"></a>Pastabos kūrimas „Finance and Operations” programoje

Taip pat galite sukurti pastabą „Finance and Operations” programoje ir ji bus sinchronizuojama su klientų įtraukimo programa.

Norėdami sukurti pastabą „Finance and Operations” programoje ir tada sinchronizuoti ją su klientų įtraukimo programa, atlikite šiuos veiksmus.

1. Programos „Finance and Operations” puslapyje **Priedai** pasirinkite **Naujas** \> **Pastaba**.

    ![Pastabos kūrimas „Finance and Operations” programoje.](media/notes-fo-1.png)

2. Įveskite pavadinimą ir trumpą instrukcijų rinkinį, tada pasirinkite **Įrašyti**.

    ![Pavadinimo ir instrukcijų įvedimas.](media/notes-fo-2.png)

3. Atnaujinkite įrašą klientų įtraukimo programoje. Naują pastabą turėtumėte rasti laiko juostoje.

    ![Nauja pastaba „Customer Engagement” programos laiko juostoje.](media/notes-fo-3.png)

Pastabą galite klasifikuoti kaip vidinę arba išorinę.

- Programos „Finance and Operations” puslapyje **Priedai** atidarykite pastabą, tada lauke **Apribojimas** pasirinkite **Vidinis** arba **Išorinis**.

    ![Laukas Apribojimas.](media/notes-fo-4.png)

Taip pat galite sukurti URL.

1. Programos „Finance and Operations” puslapyje **Priedai** pasirinkite **Naujas** \> **URL**.
2. Įveskite pavadinimą ir URL.
3. Lauke **Apribojimas** pasirinkite **Vidinis** arba **Išorinis**.

    ![URL kūrimas „Finance and Operations” programoje.](media/notes-fo-5.png)

4. Pasirinkite **Įrašyti**.

    Kadangi klientų įtraukimo programų URL tipo nėra, URL integruotas su dvigubu rašymu kaip pastaba.

    ![URL kaip pastaba „Customer Engagement” programoje.](media/notes-ce-6.png)

> [!NOTE]
> Failų priedai nepalaikomi.

## <a name="templates"></a>Šablonai

Pastabų integravimą sudaro lentelių schemų, veikiančių kartu interaktyviai naudojant duomenis (kaip parodyta tolesnėje lentelėje) rinkinys.

| „Finance and Operations“ programa | „Customer engagement“ programa | aprašymas |
|----------------------------|-------------------------|-------------|
| [Kliento priedai](mapping-reference.md#230) | Komentarai | Įmonės, naudojančios paprastąjį tekstą ir URL, kad fiksuotų konkrečių klientų informaciją (organizacijų ir asmenų). |
| [Tiekėjo dokumentų priedai](mapping-reference.md#231) | Komentarai | Įmonės, naudojančios paprastąjį tekstą ir URL, kad fiksuotų konkrečių tiekėjų informaciją (organizacijų ir asmenų). |
| [Pardavimo užsakymo antraštės dokumento priedai](mapping-reference.md#229) | Komentarai | Įmonės, naudojančios paprastąjį tekstą ir URL, kad fiksuotų konkrečių pardavimo užsakymų informaciją. |
| [Pirkimo užsakymo antraštės dokumento priedai](mapping-reference.md#232) | Komentarai | Įmonės, naudojančios paprastąjį tekstą ir URL, kad fiksuotų konkrečių pirkimo užsakymų informaciją. |

## <a name="limitations"></a>Apribojimai

Įdiegę pastabų sprendimą, jo pašalinti negalite. 

Daugiau informacijos žr. [Dvigubo rašymo susiejimo nuoroda](mapping-reference.md)
