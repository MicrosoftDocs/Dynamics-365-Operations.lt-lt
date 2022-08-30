---
title: Įplaukų pripažinimo perskirstymas
description: Šiame straipsnyje pateikiama informacija apie perskirstymą, kuris įgalina organizacijas perskaičiuoti įplaukų vertes, kai keičiamos pardavimo sutarties sąlygos. Joje pateikiamos nuorodos į kitas temas, kurios apibūdina, kaip atpažinti įplaukas įvairiuose scenarijuose.
author: bking
ms.date: 09/09/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: bking
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6c7e2149058ebbff85cbc2ac86dac3231fbcc41d
ms.sourcegitcommit: 1909d18a74cef85aad020a6a7473281e451f58c7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348160"
---
# <a name="revenue-recognition-reallocation"></a>Įplaukų pripažinimo perskirstymas

[!include [banner](../includes/banner.md)]

Perskirstymas įgalina organizacijas perskaičiuoti įplaukų vertes, kai keičiamos pardavimo sutarties sąlygos. Įplaukų pripažinimo tikslu pardavimo užsakymo dokumentai laikomi sutartimi.

Organizacija turi pati nustatyti, ar būtinas perskirstymas. Naujos eilutės įtraukimas į pardavimo užsakymą arba kliento naujo pardavimo užsakymo įtraukimas gali netapti sutarties pakeitimo priežastimi. Toliau pateikti scenarijai gali reikalauti perskirstymo:

- Klientas įtraukė prekių į pardavimo užsakymą arba pašalino prekių iš pardavimo užsakymo po to, kai užsakymui buvo pilnai arba dalinai išrašyta SF.
- Į tą pačią suderėtą sutartį buvo įvesti keli pardavimo užsakymai, kurių būsena patvirtinta arba išrašytos SF.
- Klientas grąžino arba gavo prekės kreditą po to, kai pradiniam pardavimo užsakymui buvo pilnai arba dalinai išrašyta SF.

Perskirstymo procesui taikomi keli svarbūs apribojimai:

- Procesas gali būti vykdomas tik vieną kartą. Todėl svarbu jį vykdyti tik užbaigus visus keitimus.

    - Šis apribojimas pašalintas iš 10.0.17 ir vėlesnių versijų leidimų.

- Negalima paleisti proceso projekto pardavimo užsakymams.

    - Šis apribojimas pašalintas iš 10.0.17 ir vėlesnių versijų leidimų.

- Jei įtraukti keli pardavimo užsakymai, jie turi būti skirti tai pačiai kliento sąskaitai.
- Visi perskirstomi pardavimo užsakymai turi būti pateikti ta pačia operacijos valiuta.
- Paleidus procesą negalima jo atšaukti ar anuliuoti.

    - Šis apribojimas pašalintas iš 10.0.17 ir vėlesnių versijų leidimų.

- Galima atlikti tik pardavimo užsakymų arba projekto pardavimo užsakymų perskirstymą. Negalima atlikti pardavimo užsakymų ir projekto pardavimo užsakymų derinio perskirstymo.

    - Šis apribojimas pašalintas iš 10.0.17 ir vėlesnių versijų leidimų.

## <a name="set-up-reallocation"></a>Perskirstymo nustatymas

Perskirstymo procesui daro įtaką vienas parametras.

Perskirstymą galima atlikti pardavimo užsakymui, kuriam išrašyta dalinė arba visa SF, visi ankstesni SF apskaitos įrašai turi būti pataisyti naudojant naujas, perskirstytas įplaukų vertes. Šis koregavimas atliekamas atšaukiant pradinės SF apskaitos įrašą ir registruojant naują apskaitos įrašą, pagrįstą perskirstytų įplaukų vertėmis.

Kiekviena organizacija turi nuspręsti, ar taisymas turi atnaujinti tik DK, ar taip pat turi atnaujinti gautinas sumas. Priimtas sprendimas nulemia atitinkamą parinkties **Perskirstant registruoti SF taisymus į Gautinas sumas** parametrą skirtuke **Įplaukų pripažinimas** puslapyje **Didžiosios knygos parametrai** (**Įplaukų pripažinimas \> Sąranka \> Didžiosios knygos parametrai**). Atitinkamas parametras priklauso nuo konkretaus scenarijaus. Jei norite daugiau informacijos apie galimus scenarijus, naudokite nuorodas, esančias toliau šiame straipsnyje pateiktame skyriuje [Perskirstymo scenarijai](#scenarios-for-reallocation).

[![Įplaukų pripažinimo skirtukas puslapyje Didžiosios knygos parametrai.](./media/01_RevRecScenarios.png)](./media/01_RevRecScenarios.png)

Jei parinktis **Perskirstant registruoti SF taisymus į Gautinas sumas** nustatyta į **Taip**, perskirstymo procesas pateikia tokį rezultatą:

- Kredito dokumentas sukuriamas gautinose sumose, kad būtų galima atšaukti SF, kurią būtina koreguoti.

    - Kredito dokumentas pakartotinai naudoja pradinės SF numerį, tačiau prie jo pridedama „-1“.
    - Kredito dokumentas automatiškai sudengiamas pagal pradinę SF. Jei pradinė SF jau buvo sudengta su kitu kredito dokumentu ar mokėjimu, šis sudengimas automatiškai atšaukiamas.
    - Kredito dokumentas užregistruojamas DK, kad būtų galima atšaukti apskaitos įrašą, kuris buvo užregistruotas pradinėje SF. Tačiau atsargų ir parduotų prekių savikainos (PPK) operacijų įrašai nėra atšaukiami.

- Gautinose sumose sukuriama nauja SF, pagrįsta nauja, perskirstytos kainos suma.

    - Nauja SF pakartotinai naudoja pradinės SF numerį, tačiau prie jo pridedama „-2“.
    - Nauja SF automatiškai sudengiama pagal bet kurį kredito dokumentą ar mokėjimus, kurie anksčiau buvo sudengti su pradine SF.
    - Nauja SF užregistruojama DK naudojant naujas perskirstytas įplaukų vertės sumas. Ji nėra užregistruojama atsargų ir PPK sąskaitose, nes šie įrašai išlaikomi pradinės SF apskaitos įraše.

Jei parinktis **Perskirstant registruoti SF taisymus į Gautinas sumas** nustatyta į **Ne**, perskirstymo procesas pateikia tokį rezultatą:

- Atšaukiamas apskaitos įrašas registruojamas tik DK. Visa apskaita iš pradinės SF atšaukiama, išskyrus atsargų ir PPK sąskaitų įrašus.
- Naujas apskaitos įrašas registruojamas tik DK pagal naujas, perskirstytas įplaukų vertes. Ji nėra užregistruojama atsargų ir PPK sąskaitose, nes šie įrašai išlaikomi pradinės SF apskaitos įraše.
- Puslapyje **Kliento operacijos** SF nėra paveikiama ar pakeičiama, tačiau vis tiek atspindi pradinį apskaitos įrašą. Nėra nuorodos į atšaukimą ar naujus apskaitos įrašus.

Kaip minėta, galima atnaujinti tik DK arba atnaujinti ir DK, ir gautinas sumas. Abu būdai turi teigiamų ir neigiamų savybių. Siekiant nustatyti, kurią pasirinktį naudoti, rekomenduojame įvertinti savo organizacijos reikalavimus. Jei atnaujinsite ir DK, ir gautinas sumas, naujoje SF bus rodomi teisingi apskaitos įrašai, kuriuos galima peržiūrėti dokumente, esančiame puslapyje **Kliento operacijos**. Be to, sudengimo proceso metu bus naudojami atnaujinti apskaitos įrašai, kad būtų galima registruoti mokėjimo nuolaidas ir pelną ar nuostolius. Kita vertus, kredito dokumentas ir nauja SF bus rodomi kliento išrašuose ir skirstymo pagal terminus ataskaitose, kaip ir kituose kredito dokumentuose ir kliento SF. Tų dokumentų aprašyme nurodoma, kad jie buvo sukurti taikant apskaitos korekciją.

## <a name="run-the-reallocation-process"></a>Perskirstymo proceso vykdymas

Norėdami pradėti perskirstymo procesą, pasirinkite **Perskirstyti vertę naujose užsakymo eilutėse** bet kuriame pardavimo užsakyme, kurį būtina perskirstyti. Arba eikite į **Įplaukų pripažinimas \> Periodinės užduotys \> Perskirstyti vertę naujose užsakymo eilutėse**, tada įveskite atitinkamus filtrus, pvz., kliento sąskaitą.

[![Puslapis Perskirstyti vertę naujose užsakymo eilutėse.](./media/02_RevRecScenarios.png)](./media/02_RevRecScenarios.png)

Viršutinis tinklelis puslapyje **Perskirstyti vertę naujose užsakymo eilutėse** pavadintas **Pardavimas**. Jame pateikiami kliento pardavimo užsakymai. Pasirinkite pardavimo užsakymus, kuriuos būtina perskirstyti. Jei pardavimo užsakymas turi perskirstymo ID, vadinasi jį jau pažymėjo perskirstymui kitas vartotojas. Jei vienas ar daugiau pardavimo užsakymų buvo perskirstyti anksčiau ir turi būti įtraukti į kitą perskirstymą, pirmiausia reikia anuliuoti tų pardavimo užsakymų paskirstymą. Tada jį galima įtraukti į naują perskirstymą. Norėdami gauti išsamesnės informacijos, žr. toliau pateikiamus straipsnio skyrius [Perskirstymo anuliavimas](#undo-a-reallocation) ir [Perskirstymas kelis kartus](#reallocate-multiple-times).

Apatinis puslapio tinklelis pavadintas **Eilutės**. Tinklelyje **Pardavimas** pasirinkus vieną ar daugiau pardavimo užsakymų, tinklelyje **Eilutės** rodomos pardavimo užsakymo eilutės. Pasirinkite pardavimo užsakymo eilutes, kurias būtina perskirstyti. Jei pasirinkote tik vieną pardavimo užsakymą, būtina perskirstyti to paties pardavimo užsakymo eilutes. Tokia situacija gali susiklostyti, kai vienai pardavimo užsakymo eilutei anksčiau buvo išrašyta SF, tada buvo pridėta nauja eilutė, arba esama eilutė buvo pašalinta ar atšaukta. Jei eilutė buvo pašalinta, ji nebus rodoma tinklelyje. Todėl jos pasirinkti negalima. Tačiau į ją vis tiek bus atsižvelgiama paleidus perskirstymo procesą.

Pasirinkę reikiamas pardavimo užsakymo eilutes naudokite veiksmų srities mygtukus, kaip aprašyta čia:

- **Atnaujinti perskirstymą** – skaičiuoti naujas pasirinktų pardavimo užsakymo eilučių įplaukų vertės sumas. Jei eilutė buvo pašalinta ar atšaukta, perskirstymas bus atliekamas tik pasirinktoms esamoms eilutėms. Tolesnėje iliustracijoje pateiktas pardavimo užsakymo eilučių prieš atnaujinant perskirstymą pavyzdys.

    [![Pardavimo užsakymo eilutės prieš atnaujinant perskirstymą.](./media/03_RevRecScenarios.png)](./media/03_RevRecScenarios.png)

    Naujos įplaukų vertės sumos rodomos tinklelio **Eilutės** stulpelyje **Perskirstyta suma**. Šiuo metu perskirstymas yra apdorotas, bet dar nėra apskaičiuotas. Tolesnėje iliustracijoje pateiktas pardavimo užsakymo eilučių atnaujinus perskirstymą pavyzdys.

    [![Pardavimo užsakymo eilutės atnaujinus perskirstymą.](./media/04_RevRecScenarios.png)](./media/04_RevRecScenarios.png)

- **Apdoroti** – apdoroti arba registruoti perskirstytas įplaukų vertes. Pasirinkus šį mygtuką nėra galimybių atšaukti perskirstymą. Jei nepasirinkote **Atnaujinti perskirstymą** prieš pasirinkdami **Apdoroti**, perskirstymas bus vykdomas automatiškai.

    - Jei pardavimo užsakymo eilutei nebuvo išrašyta SF, įplaukų vertės sumos atnaujinamos bet kuriame pardavimo užsakyme, kuris buvo pasirinktas perskirstymui.
    - Jei SF išrašyta vienai ar daugiau pardavimo užsakymo eilučių, registruojami korekciniai apskaitos įrašai ir pataisome visa įplaukų grafiko informacija, sukurta pardavimo užsakymo eilutei, kuriai išrašyta SF.

- **Numatomas kvitas** – rodoma apskaitos įrašų, sukurtų bet kurioms pardavimo užsakymo eilutėms, kurioms buvo išrašyta SF, peržiūra. Jei SF nebuvo išrašyta, nerodoma jokia informacija. Jei nepasirinkote **Atnaujinti perskirstymą** prieš pasirinkdami **Numatomas kvitas**, perskirstymas bus vykdomas automatiškai.
- **Įplaukų perskirstymas** – atidaromas puslapis, kuriame rodomas visų pasirinktų eilučių įplaukų vertės paskirstymas. Šiame puslapyje negalima pakeisti jokios informacijos. Joje pateikiamos eilutės sumos, naudotos perskirstymui.

    [![Eilutės sumos, naudotos perskirstymui.](./media/05_RevRecScenarios.png)](./media/05_RevRecScenarios.png)

- **Iš naujo nustatyti pasirinkto kliento duomenis** – jei perskirstymo procesas buvo pradėtas, tačiau nebuvo baigtas, perskirstymo lentelėje išvalykite tik pasirinkto kliento duomenis. Pavyzdžiui, perskirstymui pažymite kelias pardavimo užsakymo eilutes, paliekate puslapį atidarytą nepasirinkę **Apdoroti**, tada baigiasi puslapio skirtasis laikas. Tokiu atveju pardavimo užsakymo eilutės liks pažymėtos ir nebus pasiekiamos kitam vartotojui, kad būtų galima baigti perskirstymo procesą. Atidarytas puslapis net gali būti tuščias. Tokiu atveju naudojant mygtuką **Iš naujo nustatyti pasirinkto kliento duomenis** galima išvalyti neapdorotus pardavimo užsakymus, kad kitas vartotojas galėtų baigti perskirstymo procesą.

## <a name="undo-a-reallocation"></a>Perskirstymo anuliavimas

Perskirstymas anuliuojamas paleidus kitą anuliavimą. Perskirstymas atliekama iš naujo ir vartotojas pasirenka skirtingas pardavimo užsakymo eilutes, kurias reikia įtraukti į antrąjį perskirstymo procesą.

Jei perskirstymas buvo atliktas dviejuose ar daugiau atskirų pardavimo užsakymų, jį galima anuliuoti pasirinkus **Perskirstyti kainą naujose užsakymo eilutėse** iš bet kurio pardavimo užsakymo, įtraukto perskirstyme. Perskirstymo anuliuoti negalima nuėjus į **Įplaukų pripažinimas \> Periodinės užduotys \> Perskirstyti kainą naujose užsakymo eilutėse**, nes šiuo būdu atidarytame puslapyje rodomi tik pardavimo užsakymai, kuriuose nėra perskirstymo ID. Perskirstymo ID priskiriamas po to, kai dokumentas yra perskirstytas.

Puslapyje **Perskirstyti kainą naujose užsakymo eilutėse** atžymėkite bet kokius pardavimo užsakymus, kurie neturi būti įtraukti į sutartį. Norėdami apdoroti perskirstymą, naudokite atitinkamus veiksmų srities mygtukus, pvz., **Naujinti perskirstymą** ir **Apdoroti**. Jei visi pardavimo užsakymai, išskyrus aktyvų pardavimo užsakymą, nepažymėti, perskirstymo ID bus pašalintas apdorojus keitimą.

Jei perskirstymas atliktas įtraukiant naują eilutę į pardavimo užsakymą, kuriam pilnai arba dalinai išrašyta SF, perskirstymas gali būti anuliuotas šalinant tą eilutę iš pardavimo užsakymo ir dar kartą paleidžiant paskirstymą. Pardavimo užsakymo eilutę reikia pašalinti, nes yra manoma, kad visos pardavimo užsakymo eilutės yra tos pačios sutarties dalis. Negalite atžymėti pardavimo užsakymo eilutės, kol esate puslapyje **Perskirstyti kainą naujose užsakymo eilutėse**.

## <a name="reallocate-multiple-times"></a>Perskirstymas kelis kartus

Jei sutartyje atlikti keli pakeitimai, galima atlikti kelis to paties pardavimo užsakymo perskirstymus. Kiekvienas perskirstymas suaktyvina perskirstymo ID priskyrimą pardavimo užsakymui arba pardavimo užsakymų grupei, kad būtų sugrupuoti keitimai. Jei atliekami keli perskirstymai, kiekvienas papildomas perskirstymas naudoja tą patį perskirstymo ID kaip ir pirmasis perskirstymas.

Pavyzdžiui, įvedamas pardavimo užsakymas 00045, kuris turi kelias eilutes. Išrašius visą pardavimo užsakymo SF, prie jo pridedama nauja pardavimo užsakymo eilutė. Tada perskirstymas paleidžiamas atidarius puslapį **Perskirstyti kainą naujose užsakymo eilutėse** iš pardavimo užsakymo 00045 arba nuėjus į **Įplaukų pripažinimas \> Periodinės užduotys \> Perskirstyti kainą naujose užsakymo eilutėse**. Perskirstymo ID **Reall000001** priskiriamas pardavimo užsakymui.

Antras pirkimo užsakymas, 00052, sukuriamas tai pačiai sutarčiai. Perskirstymą galima paleisti dar kartą atidarius puslapį **Perskirstyti kainą naujose užsakymo eilutėse** iš pardavimo užsakymo 00045, bet ne iš pardavimo užsakymo 00052. Jei puslapį **Perskirstyti kainą naujose užsakymo eilutėse** atidarysite iš pirkimo užsakymo 00052, pirkimo užsakymas 00045 nebus rodomas, nes jam buvo priskirtas perskirstymo ID. Puslapyje rodomi tik pardavimo užsakymai, kurie neturi perskirstymo ID.

Yra du būdai, kaip atlikti antrą perskirstymą. Galite anuliuoti pardavimo užsakymo 00045 perskirstymą. Tokiu atveju perskirstymo ID pašalinamas ir perskirstymą galite atlikti iš pardavimo užsakymo 00045 arba pardavimo užsakymo 00052. Arba galite atidaryti puslapį **Perskirstyti kainą naujose užsakymo eilutėse** iš pardavimo užsakymo 00045 ir įtraukti naują pardavimo užsakymą. Kai perskirstymas yra apdorotas, perskirstymo ID **Reall000001** bus priskirtas tiek pardavimo užsakymui 00045, tiek pardavimo užsakymui 00052.

## <a name="scenarios-for-reallocation"></a>Perskirstymo scenarijai

Įvairūs įplaukų pripažinimo scenarijai aptariami toliau nurodytose temose:

- [Įplaukų pripažinimo perskirstymas – 1 scenarijus](rev-rec-reallocation-scenario-1.md) – įvedami du pardavimo užsakymai, tačiau jie yra tik patvirtinti. Tas pats scenarijus duoda panašius rezultatus, jei daugiau nei dviejų pardavimo užsakymų būsena yra Patvirtinta.
- [Įplaukų pripažinimo perskirstymas – 2 scenarijus](rev-rec-reallocation-scenario-2.md) – įvedami du pardavimo užsakymai, tada klientas įtraukia prekę į sutartį po to, kai SF išrašoma pirmam pardavimo užsakymui.
- [Įplaukų pripažinimo perskirstymas – 3 scenarijus](rev-rec-reallocation-scenario-3.md) – į esamą pardavimo užsakymą, kuriam išrašyta SF, įtraukiama nauja eilutė.
- [Įplaukų pripažinimo perskirstymas – 4 scenarijus](rev-rec-reallocation-scenario-4.md) – iš esamo pardavimo užsakymo, kuriam išrašyta dalinė SF, pašalinama eilutė.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
