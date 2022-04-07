---
title: Mobiliojo įrenginio vartotojų paskyros
description: Šioje temoje aprašoma, kaip nustatyti ir valdyti vartotojų sąskaitas, kurios leidžia darbuotojams prisijungti ir naudoti sandėlio programą.
author: Mirzaab
ms.date: 09/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-09-15
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c4cb36160e692cc12140b57037d2c9739f7b2ebd
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462676"
---
# <a name="mobile-device-user-accounts"></a>Mobiliojo įrenginio vartotojų paskyros

[!include [banner](../includes/banner.md)]

Kiekvieną kartą, kai darbuotojas pradeda naudoti sandėlio programą, jis turi prisiregistruoti naudodamas vartotojo vardą ir slaptažodį. Bet kokį sandėlio programos vartotojų skaičių galima susieti su kiekvienu sistemos darbuotoju, o sandėliai paprastai yra susieti su kiekvienu iš tų sandėlio programų vartotojų. Norint nustatyti numatytuosius parametrus ir kitus parametrus, susijusius su sandėlio programa, taip pat konfigūr nustatomos įvairios kiekvieno darbuotojo pasirinktys.

## <a name="set-up-the-required-worker-and-employee-records"></a>Nustatyti reikiamus darbuotojo ir darbuotojo įrašus

Prieš nustatydamas sandėlio programos vartotojus, kiekvienas darbuotojas jau turi būti kaip „Supply Chain Management“ darbuotojas arba darbuotojas **personalo** modulyje.

## <a name="set-up-mobile-device-user-accounts"></a><a name="set-wma-users"></a>Mobiliojo įrenginio vartotojų paskyrų nustatymas

Kai personalo dalyje nustatyti reikiami darbuotojai, kiekvienam iš jų galite priskirti sandėlio programų vartotojus ir nustatyti kitas parinktis, darančių įtaką tai, kaip jie gali naudoti programą.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Darbuotojai**.
1. Norėdami redaguoti esamą darbuotoją, pasirinkite jį sąrašo srityje. Norėdami įtraukti naują įrašą, rinkitės **Nauja** veiksmų juostoje.
1. Jei nustatote naują darbuotoją, atlikite šiuos veiksmus:

    1. **Darbuotojo** laukelyje pasirinkite paskirties vartotoją darbuotojų sąraše.
    1. Pasirinkite **Pasirinkti**.
    1. Veiksmų srityje pasirinkite **Įrašyti**.

1. Numatytasis profilis gali būti naudojamas nurodyti sandėlio darbuotojui pakavimo stotyje reikiamą procesą. Taip pat galima naudoti numatytąjį profilį, norint išsaugoti pageidaujamus darbuotojo profilio parametrus. „FastTab“ **Profilis** nustatykite toliau pateikiamus laukus:

    - **Konteinerio pakavimo strategija** – pasirinkite konteinerio pakavimo strategiją, kuri nustato, kaip pakavimo vietos konteineriai turi būti apdorojami. Čia pasirinkta konteinerio pakavimo strategija bus iš anksto pasirinkta darbuotojui, kai jis atidarys pakavimo stotį. Daugiau informacijos rasite toliau pateikiamame žurnalo skelbime: [patobulintos pakavimo funkcijos](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611),
    - **Pakavimo šablono ID** – pasirinkite pakavimo šablono ID, kuris apibrėžia naudojamus pakavimo strategiją ir konteinerio parametrus. Jei pasirinktas pakavimo šablono ID yra susietas su konteinerio pakavimo strategija, šiame puslapyje negalėsite keisti **konteinerio pakavimo strategijos** parametro.

1. **Numatytoje pakavimo stoties** „FastTab" nustatykite šiuos laukus, norėdami nustatyti numatytąją pakavimo stotį, kuri taikoma darbuotojui prisijungiant. Darbuotojas gali pasirinkti kitą pakavimo stotį, jei būtina.

    - **Vieta** – pasirinkite stotis, kurioje yra numatytoji pakavimo stotis.
    - **Sandėlis** – pasirinkite sandėlį, kuriame yra numatytoji pakavimo stotis.
    - **Vieta** – pasirinkite numatytosios pakavimo stoties vietą.

1. Naudodami **vartotojų** „FastTab" galite sukurti bet kokį sandėlio programos vartotojų abonementų skaičių pasirinktam darbuotojui. Kiekviena sąskaita yra susieta su konkrečiu sandėliu ar sandėliu. Naudokite įrankių juostą, norėdami pridėti arba pašalinti vartotojo abonementus, iš naujo nustatyti pasirinktos sąskaitos slaptažodį arba priskirti sandėlius pasirinktam abonementui. Kiekvienai vartotojo paskyrai, nustatykite toliau pateiktus laukus.

    - **Vartotojo ID** – Įveskite unikalų identifikavimo numerį.
    - **Vartotojo vardas** – Įveskite vardą identifikavimo numeriui.
    - **Numatytasis sandėlis** – nustatyti numatytąjį sandėlį, kuriame paprastai dirba darbuotojas. Norėdami priskirti papildomus sandėlius, galite naudoti įrankių juostą, o darbuotojas gali pereiti tarp sandėlių naudodamas mobiliojo įrenginio meniu elemento netiesioginę **sandėlio netiesioginę** veiklą.
    - **Meniu pavadinimas** – pasirinkite šakninį meniu, kuris bus darbuotojo pradinis puslapis. Galimybė nustatyti kiekvieno darbuotojo šakninį meniu yra naudinga, nes ji leidžia valdyti meniu struktūrą, kurią gali naudoti kiekvienas darbuotojas. Pavyzdžiui, meniu darbuotojams, kurie aktyvūs tik siuntimo srityje, gali būti atliekamas užduotims, susijusioms su tos srities siuntimo operacijomis.
    - **Neaktyvus** – pasirinktas žymės langelis nurodo, kad vartotojo abonementas neaktyvus. Vartotojo abonementas automatiškai neaktyvus, jei darbuotojas penkis kartus į sandėlio programos eilutę įveda klaidingą slaptažodį. Nepaisant to, galite rankinių būdu rinktis šį žymimą laukelį. Atžymėti žymės langelį, kad vartotojas vėl būtų aktyvus.

1. „FastTab“ **Darbas**, nustatykite tolesnes vertes:

    - **Leisti nepaisyti paėmimo vietos** – nustatykite šią parinktį kaip *Taip* jei norite leisti darbuotojui nepaisyti paėmimo veiksmų vietos. Ši galimybė gali būti naudinga, jei faktinės atsargos neatitinka sistemos siūlomos vietos.
    - **Leisti nepaisyti padėjimo vietos** – nustatykite šią parinktį kaip *Taip* jei norite leisti darbuotojui nepaisyti padėjimo veiksmų vietos. Ši galimybė gali būti naudinga, jei siūloma padėjimo vieta šiuo metu yra pilna arba jos nėra, arba jei išdėstymo vietos pakeistos.
    - **Leisti paimti pardavimus** – nustatykite šią parinktį kaip *Taip* jei norite leisti darbuotojui per daug paimti, kai išrinkti pardavimo užsakymai. Dėl daugiau informacijos, žr. [Per didelis pardavimo užsakymų ir perkėlimo užsakymų paėmimas](over-picking-for-sales-and-transfer-orders.md).
    - **Leisti perdavimo užsakymą per didelį paėmimą** – nustatykite šią parinktį kaip *Taip* jei norite leisti darbuotojui per daug perleisti užsakymus, kai išrinkti pardavimo užsakymai. Dėl daugiau informacijos, žr. [Per didelis pardavimo užsakymų ir perkėlimo užsakymų paėmimas](over-picking-for-sales-and-transfer-orders.md).
    - **Leisti perkelti atsargas su susijusiu darbu** – nustatykite šią pasirinktį kaip *Taip* kad darbuotojas galėtų perkelti atsargas, kurios jau rezervuotos arba jau susietos su kitu darbu. Dėl daugiau informacijos, žr. [Atsargų perkėlimas su susietu darbu modulyje „Warehouse management“](move-inventory-associated-work.md).
    - **Leisti rankinį prekių realią vietą** – nustatykite šią pasirinktį kaip *Taip* norėdami trumpo paėmimo metu darbuotojui įgalinti rankinį realų paskirstymas. Prekių realų paskirstymas vedlys padės darbuotojams paimti atsargas iš kitos vietos. Nors automatinis realų paskirstymas galimas visiems darbuotojams, rankinis realus vietos nustatymas reikalingas darbuotojui. Galimybė valdyti kiekvieno darbuotojo tikroją vietą rankiniu būdu gali padėti, nes taip galima valdyti kiekvieno darbuotojo matomumą, kai, pvz., prekių paėmimas iš sulaikymo ar buferio srities ribojamas patikimiems darbuotojams. Norėdami gauti daugiau informacijos, žr. toliau nurodytą žurnalo skelbimą: automatinis [ir rankinis prekių reallocation trumpalaikio paėmimo metu](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/11/07/automatic-and-manual-item-reallocation-during-the-short-picking-dynamics-365-for-operations-1611/).
    - **Yra ciklų skaičiavimo prižiūrėtojas** – nustatykite šią pasirinktį kaip *Taip* jei norite darbuotoją padaryti ciklų skaičiavimo prižiūrėtojui. Tokiu atveju visi ciklai, kuriuos darbuotojas atlieka sandėlio programoje, bus nedelsiant patvirtinti. **Maksimali procentinė riba**, **maksimali kiekio riba**, ir **maksimalios vertės limito** aukai nėra skirti darbuotojams, kurių ši pasirinktis nustatyta kaip *Taip*.
    - **Maksimali procentinė riba** – Įveskite didžiausią procentinę ribą, kuria ciklų skaičius gali skirtis nuo numatyto kiekio nereikalaujant patvirtinimo iš ciklų skaičiavimo prižiūrėtojo.
    - **Maksimali kiekio riba** – įveskite bendrą kiekį, kurį įvestas kiekis gali skirtis nuo numatomo kiekio (vienetais), nepareikalaudami patvirtinimo ciklo skaičiavimo prižiūrėtojo.
    - **Maksimali vertės riba** – Įveskite didžiausią sumą, kuria atsargų kaina gali skirtis nuo numatytosios kainos nereikalaujant patvirtinimo iš ciklų skaičiavimo prižiūrėtojo.

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Jei įtraukiėte naują vartotojo paskyrą, **Slaptažodžio nustatymas** teksto laukelis, kuriame galit sukurti paprastą slaptažodį, kurį vartotojas galės naudoti prisijungdamas prie mobilios programos. Įveskite paprastą slaptažodį du kartus, tada, norėdami tęsti, pasirinkite **Įrašyti slaptažodį**.

## <a name="set-the-language-number-formats-and-time-zone-for-each-warehouse-app-user"></a>Kiekvieno sandėlio programos vartotojo kalbos, skaičių formatų ir laiko juostos nustatymas

Kai darbuotojas prisijungia prie „Warehouse Management“ „mobile app“, kalba, numerių formatai ir laiko juostos keitimas, kad atitiktų darbuotojo nuostatas. Darbuotojo, pasirinkto 3 žingsnyje Nustatyti mobiliojo įrenginio vartotojo abonementus, [sąskaitos parametrai](#set-wma-users) apibrėžia naudojamus parametrus. Jei kiekvienam vartotojui reikia atskirų parametrų, naudokite skirtingas darbuotojų sąskaitas. Toliau pateiktoje procedūroje rodoma, kaip pakeisti kiekvieno sandėlio programos vartotojo kalbą, numerių formatus ir laiko juostą.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Darbuotojai**.
1. Raskite darbuotojo, kurį norite nustatyti, vardą. Įsitikinkite, kad darbuotojas turi visus reikiamus sandėlio programos vartotojų abonementus, kurie išvardyti **vartotojų** „FastTab". Sukurkite naują darbuotoją ir (arba) įtraukite sandėlio programos vartotojų abonementus, kaip reikia, atlikite veiksmus, nurodytus skyriuje [Nustatyti mobiliojo įrenginio vartotojų](#set-wma-users) sąskaitas.
1. Eikite į **Sistemos administravimas \> Vartotojai \> Vartotojai**.
1. Pasirinkite vartotojo abonementą, kuriame **asmens** stulpelyje rodomas darbuotojo, kurį suradote 2 žingsniu, vardas.

    > [!IMPORTANT]
    > **Vartotojo ID** reikšmės, išvardytos puslapyje **Vartotojai** puslapyje *nėra* susijusios su vertėmis, kurios rodomos darbuotojo puslapio, kurį atidarėte 1 žingsniu **Vartotojai** „FastTab“ **Darbuotojo** puslapyje.

1. Veiksmų srityje pasirinkite **Vartotojo parinktys**.
1. Skirtuke **Ypatybės** nustatykite toliau pateiktus laukus.

    - **Kalba** – pasirinkite kalbą, kurią darbuotojas pageidauja. Šiame lauke taip pat valdomas numerių formatas, rodomas sandėlio programoje.
    - **Datos, laiko ir numerio formatas** – pasirinkite datos ir laiko formatą, kurį pageidauja darbuotojas. Sandėlio programa vietoj šio parametro naudoja numerio formatą, **susietą su pasirinkta** kalbos lauko kalba.
    - **Laiko juosta** – pasirinkite laiko juostą, kurioje dirba darbuotojas. Šis laukas turi įtakos visų registracijų, kurias darbuotojas atlieka naudodamas programą, laiko antspaudui.

> [!NOTE]
> Kai kuriais atvejais, sandėlio programai nepavyko rasti konkrečių darbuotojo parametrų, kurie nustato kalbą, numerių formatus ir laiko juostą. Galioja šios taisyklės:
>
> - Jei programa neprijungta prie „Supply Chain Management“ aplinkos (pvz., pirmą kartą įdiegus programą), naudojama vietinio įrenginio kalba. Kai pasikeičia įrenginio kalba, pasikeičia ir programos kalba. Daugiau informacijos apie vietinio įrenginio kalbos konfigūravimą ieškokite įrenginio ir (arba) operacinės sistemos dokumentuose.
> - Jei programa prijungta prie „Supply Chain Management“ aplinkos, bet nepasirinktas prisiregistravęs darbuotojas, kalba, numerių formatai ir laiko juosta parenkami remiantis sąskaita, kuri susieta su kliento ID, kurį įrenginys naudoja jungtis prie „Supply Chain Management“. Dėl išsamesnės informacijos, žr. [Vartotojo paskyros kūrimas ir konfigūravimas programoje „Supply Chain Management“](install-configure-warehouse-management-app.md#user-azure-ad).

> [!TIP]
> Jei pastebite, kad rodomi netinkami registracijų, kurios buvo pagamintos naudojant sandėlio programėlę, laiko juostą, nustatytą vartotojo sąskaitai, prie kurios darbuotojai prisiregistruodami naudoja „Supply Chain Management“ ir (arba) autentifikuoti, turite ją koreguoti. Kaip anksčiau buvo nurodyta, laiko juostos parametras gali būti nustatytas iš vartotojo abonemento, kuris naudojamas prisijungti prie sandėlio programos, kaip nustatyta **Darbuotojas** puslapyje. Arba, jei vartotojo abonementas nustatytas **Darbuotojas** puslapyje, laiko juosta gaunama iš vartotojo abonemento, kuris susietas su kliento ID, kuris naudojamas autentifikuoti, kaip nustatyta **[Azure Active Directory programose](install-configure-warehouse-management-app.md)** puslapyje.
