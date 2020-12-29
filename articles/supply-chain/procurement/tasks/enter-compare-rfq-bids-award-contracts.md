---
title: RFQ kainos pasiūlymų įvedimas bei lyginimas ir sutarčių pasirinkimas
description: Šioje temoje pasakojama kaip įvesti atsakymus pasiūlymo patvirtinimui (RFQ), skaičiuoti ir lyginti kainų pasiūlymus bei pasirinkti vieno iš tiekėjų sutartį.
author: mkirknel
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchRFQCaseTable, PurchRFQReplyTable, PurchRFQCompare, PurchRFQEditLines, PurchRFQEditLinesParameters, PurchTable, PurchTablePart, PurchRFQCompareLinePrices, PurchRFQCompareRFQ
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae7c43516fc90224439f6f7cfd5fd0a6058e8b39
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434022"
---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>RFQ kainos pasiūlymų įvedimas bei lyginimas ir sutarčių pasirinkimas

[!include [banner](../../includes/banner.md)]

Šioje temoje pasakojama kaip įvesti atsakymus pasiūlymo patvirtinimui (RFQ), skaičiuoti ir lyginti kainų pasiūlymus bei pasirinkti vieno iš tiekėjų sutartį. Šią procedūrą galite naudoti **USMF** demonstracinių duomenų įmonėje.

Prieš pradedant šią procedūrą reikia turėti RFQ su dviem eilutėmis ir išsiųstą bent dviem tiekėjams. Norėdami sukurti šį RFQ, atlikite pasiūlymo [Pasiūlymo patvirtinimo kūrimas](create-request-quotation.md) procedūrą. Šios procedūros negalėsite vykdyti tol, kol taip pat nenustatysite vertinimo kriterijų.

Galite įvesti kainos pasiūlymą kaip tiekėjas arba įsigijimo specialistas. Daugiau informacijos žr. [Tiekėjo bendradarbiavimo nustatymas ir tvarkymas](../set-up-maintain-vendor-collaboration.md).

## <a name="enter-a-reply-as-a-vendor"></a>Įveskite atsakymą kaip teikėjas

1. Ataskaitų srityje pasirinkite **Tiekėjų kainos pasiūlymas**.
2. Sąraše **Nauji kainos pasiūlymo kvietimai** suraskite ką tik išsiųstą RFQ. Pasirinkite RFQ, kad pamatytumėte, ko prašoma.
3. Pasirinkite **RFQ priedai**, norėdami peržiūrėti visus pridėtus priedus.
4. Pasirinkite **Kainos pasiūlymas**, kad laukai būtų redaguojami. Atkreipkite dėmesį, kad laukas **Kainos pasiūlymo eiga** nustatytas į **Atnaujina tiekėjas**.
5. Antraštėje ir eilutėse įveskite vertes ir kainos pasiūlymo atsakymo.
6. Jei prie kainos pasiūlymo reikia įtraukti priedus, pasirinkite **Kainos pasiūlymo priedai.**
7. Norėdami peržiūrėti, ar reikalingi kokie nors dokumentai, pasirinkite spartųjį skirtuką **Kainos pasiūlymo nurodymo elementai**.
8. Norėdami peržiūrėti, ar RFQ buvo pakeistas, pasirinkite spartųjį skirtuką **Pakeitimai** .
9. Pasirinkite spartųjį skirtuką **Klausimynas**. Būtina atsakyti į visus čia pateikiamus klausimynus.
10. Norėdami peržiūrėti išplėstinę informaciją apie eilutę, pasirinkite spartųjį skirtuką **Eilutės informacija**.
11. Pasirinkite **Atkurti iš RFQ**, tik jei jums būtina atkurti vertes, kurios buvo įvestos į pirmines RFQ vertes.
12. Kainos pasiūlymą galima įrašyti bet kuriuo metu ir atlikti papildomą apdorojimą vėliau, jei galiojimo data ir laikas nėra perkelti. Tokiu atveju galite rasti kainos pasiūlymą sąraše **Kainos pasiūlymo eiga**, esančiame darbo srityje **Tiekėjo kainos pasiūlymas**.
13. Kai pasiūlymas parengtas siųsti, pasirinkite **Pateikti**. Jei nenorite pateikti kainos pasiūlymo, pasirinkite **Atmesti**. Pateikti kainos pasiūlymai pasiekiami sąraše **Pateikti kainos pasiūlymai** darbo srityje **Tiekėjo kainos pasiūlymas**.  
14. Pateikę kainos pasiūlymą, galite jį atšaukti bet kuriuo metu prieš pasibaigiant galiojimo datai ir laikui. Atkreipkite dėmesį, kad kai kainos pasiūlymas atšaukiamas, jis nėra laikomas pateiktu. Kai pasiūlymą priima arba atmeta pirkimo padalinys, jis rodomas sąraše **Pasirinkti kainos pasiūlymai** arba **Prarasti kainos pasiūlymai**, esančiame darbo srityje **Tiekėjo kainos pasiūlymas**.  

## <a name="enter-a-reply-from-a-vendor-as-a-procurement-professional"></a>Įveskite tiekėjo kaip įsigijimo profesionalo atsakymą

1. Įsitikinkite, kad nustatyta teisė redaguoti tiekėjo kainos pasiūlymus. Eikite į **Įsigijimas ir šaltinio pasirinkimas \> Sąranka \> Įsigijimo ir šaltinio pasirinkimo parametrai**. Skirtuke **Pasiūlymo patvirtinimas** nustatykite parinktį **Pirkėjas gali redaguoti tiekėjų kainos pasiūlymą** į **Taip**.
2. Pasirinkite **Įsigijimas ir šaltinio pasirinkimas \> Pasiūlymų patvirtinimai \> Visi pasiūlymų patvirtinimai**.
3. Pasirinkite RFQ, kurio būsena yra **Išsiųstas** ir pasirinkite saitą ant lauke **Pasiūlymo patvirtinimas**.
4. Pasirinkite **Valdyti atsakymus**. Pasirodžiusiame puslapyje rodomas RFQ kiekvienam į pasiūlymą pakviestam tiekėjui.
5. Pasirinkite RFQ, į kurį neatsakė. ( **Atsakymo eigos** laukas turi būti nustatytas kaip **Nepradėtas**.)
6. Pasirinkite **Redaguoti \> Redaguoti RFQ atsakymą**. Pasirodo puslapis **RFQ atsakymas**. Kaip įsigijimo specialistas nuo šiol galite įvesti atsakymą tiekėjo vardu. Atkreipkite dėmesį, kad laukas **Kainos pasiūlymo eiga** nustatytas į **Atnaujina pirkėjas**.  
7. Įveskite kainos pasiūlymo duomenis. Baigę pasirinkite **Pateikti**.

## <a name="score-the-bids"></a>Kainų pasiūlymų vertinimas

1. Puslapyje **Visi pasiūlymų patvirtinimai** užklausos pasirinkite RFQ atvejį, kurio atsakymus norite gauti.
2. Pasirinkite **Valdyti atsakymus**.
3. Pasirinkite vertinamą atsakymą.
4. Pasirinkite **Antraštė**, kad galėtumėte peržiūrėti pasiūlymo vertinimo balus.
5. Sparčiajame skirtuke **Kainos pasiūlymo vertinimas** įveskite lauko **Rezultatas** skaičių vienam iš įvertinimo kriterijų. Jei ant ant kriterijų užvedate pele, patariama, kokiame intervale turi būti jūsų rezultatas. Šioje demonstracijoje galite įvesti skaičių nuo 1 iki 5 bet kuriam įvertinimo kriterijui.  
6. Pakartokite 5 žingsnį kitam vertinimo kriterijuj.
7. Jei RFQ atvejyje yra tiekėjams išsiųstas klausimynas, tiekėjo atsakymus galite įvesti sparčiajame skirtuke **Klausimynai**.
8. Uždarykite puslapį.
9. Visiems kitiems pasiūlymams kartokite 1 – 8 veiksmus.

## <a name="compare-the-replies"></a>Atsakymų palyginimas

1. Veiksmų srities skirtuke **Bendra** pasirinkite **Palyginti atsakymus**.
2. Lauke **Reitingas** įveskite skaičių.  
    - Šiame puslapyje rodomi kainų pasiūlymai su antrašte ir eilutės informacija bei bendras rezultatas antraštės lygyje. Eilutes galite palyginti jas rūšiuodami tinklelyje, kad palyginamos eilutės būtų viena šalia kitos. Tai pat įtraukta ši informacija:
    - **Kiekis** – tiekėjo siūlomas kiekis. Kiekis gali skirtis nuo RFQ nurodyto kiekio.
    - **Grynoji suma** – atėmus visas nuolaidas tiekėjo siūloma kaina už eilutėje nurodytas prekes.
    - **Nuokrypis** – dienų skaičius, kuriuo kainos pasiūlymo antraštėje arba eilutėje nurodyta pristatymo data skiriasi nuo pageidaujamos RFQ eilutėje nurodytos pristatymo datos. Galite įvesti kiekvieno kainos pasiūlymo reitingą.  
3. Pasirinkite kito norimo reitinguoti kainos pasiūlymo antraštės eilutę.
4. Lauke **Reitingas** įveskite skaičių.
5. Pasirinkite **Įrašyti**.

## <a name="reject-a-bid"></a>Kainos pasiūlymo atmetimas

1. Pasirinkite norimo atmesti kainos pasiūlymo antraštės eilutę. Vienu metu vieną kainos pasiūlymą ar vieno kainos pasiūlymo eilutes galite tik priimti, atmesti arba grąžinti.
2. Pažymėkite žymės langelį **Žymėti**.  
    - Jei kainos pasiūlymo antraštėje pažymėsite žymės langelį **Žymėti**, taip pat bus pažymėtos visos eilutės. Norėdami atmesti arba priimti tik kai kurias kainos pasiūlymo eilutes, galite pažymėti tik tas eilutes. Be to, kai kuriose RFQ eilutėse galite priimti vieno tiekėjo kainos pasiūlymą, o kitas RFQ eilutes galite skirti kitam tiekėjui. Tačiau vienu metu turite atlikti vieną kainos pasiūlymą.  
    - Jei yra pakaitinių eilučių, galite priimti pradinę pasiūlymo eilutę arba jos pakaitą, bet ne abu.  
3. Pasirinkite **Atmesti**.
4. Pasirinkite **Parametrai**, tada lauke **Atmetimo priežastis** įveskite arba pasirinkite savo pasiūlymo atmetimo priežastį. Priežastis saugoma atsakyme.  
5. Pasirinkite **Gerai**.
6. Pasirinkite **Gerai**.

## <a name="accept-a-bid"></a>Kainos pasiūlymo priėmimas

1. Pasirinkite kainos pasiūlymą, kurį norite priimti ir spustelėkite lauke **Pasiūlymo patvirtinimas** esantį saitą. Jei esate puslapyje **Palyginti pasiūlymo patvirtinimo atsakymus**, paryškintas siūlomas kainos pasiūlymas yra pasiūlymas, į kurį sistema atsižvelgs atliekant priėmimo veiksmą. Vienu metu galite priimti eilutes iš vieno kainos pasiūlymo.  
2. Veiksmų srityje pasirinkite **Atsakymas**.
3. Pasirinkite **Patvirtinti**. Jei pažymėjote tik konkrečias eilutes, į priėmimo veiksmą bus įtrauktos tik tos eilutės. Jei norite priimti visas kainos pasiūlymo eilutes, tada eilučių žymėti nereikia.  
4. Pasirinkite **Parametrai**, tada lauke **Priėmimo priežastis** įveskite arba pasirinkite savo pasiūlymo priėmimo priežastį. Priežastis saugoma kainos pasiūlyme.  
5. Pasirinkite **Gerai**.
6. Pasirinkite **Gerai**. Pasirinkus **Gerai**, pagal eilutes, įtrauktas į RFQ priėmimą, sugeneruojamas pirkimo užsakymas. Jei yra kitų neapdorotų (priimtų, atmestų ar grąžintų) kainos pasiūlymų, sistema jus paragins likusius kainos pasiūlymus atmesti.  

## <a name="view-the-purchase-order-that-is-generated"></a>Sugeneruojama pirkimo užsakymo peržiūra

Veiksmų srities skirtuke **Bendra** pasirinkite **Pirkimo užsakymas**. Pasirodžiusiame puslapyje galite peržiūrėti pirkimo užsakymą, kuris buvo sugeneruotas, kai priėmėte kainos pasiūlymą.
