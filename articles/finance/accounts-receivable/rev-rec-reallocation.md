---
title: Įplaukų pripažinimo perskirstymas
description: Šioje temoje pateikiama informacija apie perskirstymą, kuris įgalina organizacijas perskaičiuoti įplaukų vertes, kai keičiamos pardavimo sutarties sąlygos. Joje pateikiamos nuorodos į kitas temas, kurios apibūdina, kaip atpažinti įplaukas įvairiuose scenarijuose.
author: kweekley
manager: aolson
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a7c57ac5f3fc8d9a0e0b57ba5d7a3e2924bbd4c6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995643"
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
- Negalima paleisti proceso projekto pardavimo užsakymams.
- Jei įtraukti keli pardavimo užsakymai, jie turi būti skirti tai pačiai kliento sąskaitai.
- Visi perskirstomi pardavimo užsakymai turi būti pateikti ta pačia operacijos valiuta.
- Paleidus procesą negalima jo atšaukti ar anuliuoti.

## <a name="set-up-reallocation"></a>Perskirstymo nustatymas

Perskirstymo procesui daro įtaką vienas parametras.

Perskirstymą galima atlikti pardavimo užsakymui, kuriam išrašyta dalinė arba visa SF, visi ankstesni SF apskaitos įrašai turi būti pataisyti naudojant naujas, perskirstytas įplaukų vertes. Šis koregavimas atliekamas atšaukiant pradinės SF apskaitos įrašą ir registruojant naują apskaitos įrašą, pagrįstą perskirstytų įplaukų vertėmis.

Kiekviena organizacija turi nuspręsti, ar taisymas turi atnaujinti tik DK, ar taip pat turi atnaujinti gautinas sumas. Priimtas sprendimas nulemia atitinkamą parinkties **Perskirstant registruoti SF taisymus į Gautinas sumas** parametrą skirtuke **Įplaukų pripažinimas** puslapyje **Didžiosios knygos parametrai** (**Įplaukų pripažinimas \> Sąranka \> Didžiosios knygos parametrai**). Atitinkamas parametras priklauso nuo konkretaus scenarijaus. Jei norite daugiau informacijos apie galimus scenarijus, naudokite nuorodas, esančias toliau šioje temoje pateiktame skyriuje [Perskirstymo scenarijai](#scenarios-for-reallocation).

[![Įplaukų pripažinimo skirtukas puslapyje Didžiosios knygos parametrai](./media/01_RevRecScenarios.png)](./media/01_RevRecScenarios.png)

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

[![Puslapis Perskirstyti vertę naujose užsakymo eilutėse](./media/02_RevRecScenarios.png)](./media/02_RevRecScenarios.png)

Viršutinis tinklelis puslapyje **Perskirstyti vertę naujose užsakymo eilutėse** pavadintas **Pardavimas**. Jame pateikiami kliento pardavimo užsakymai. Pasirinkite pardavimo užsakymus, kuriuos būtina perskirstyti. Negalima pasirinkti projekto pardavimo užsakymų, nes negalima perskirstyti projekto pardavimo užsakymų. Taip pat negalima pasirinkti pardavimo užsakymų, kurie jau turi perskirstymo ID, nes ne projekto pardavimo užsakymus galima perskirstyti tik vieną kartą. Jei pardavimo užsakymas turi perskirstymo ID, vadinasi jį jau pažymėjo perskirstymui kitas vartotojas.

Apatinis puslapio tinklelis pavadintas **Eilutės**. Tinklelyje **Pardavimas** pasirinkus vieną ar daugiau pardavimo užsakymų, tinklelyje **Eilutės** rodomos pardavimo užsakymo eilutės. Pasirinkite pardavimo užsakymo eilutes, kurias būtina perskirstyti. Jei pasirinkote tik vieną pardavimo užsakymą, būtina perskirstyti to paties pardavimo užsakymo eilutes. Tokia situacija gali susiklostyti, kai vienai pardavimo užsakymo eilutei anksčiau buvo išrašyta SF, tada buvo pridėta nauja eilutė, arba esama eilutė buvo pašalinta ar atšaukta. Jei eilutė buvo pašalinta, ji nebus rodoma tinklelyje. Todėl jos pasirinkti negalima. Tačiau į ją vis tiek bus atsižvelgiama paleidus perskirstymo procesą.

Pasirinkę reikiamas pardavimo užsakymo eilutes naudokite veiksmų srities mygtukus, kaip aprašyta čia:

- **Atnaujinti perskirstymą** – skaičiuoti naujas pasirinktų pardavimo užsakymo eilučių įplaukų vertės sumas. Jei eilutė buvo pašalinta ar atšaukta, perskirstymas bus atliekamas tik pasirinktoms esamoms eilutėms. Tolesnėje iliustracijoje pateiktas pardavimo užsakymo eilučių prieš atnaujinant perskirstymą pavyzdys.

    [![Pardavimo užsakymo eilutės prieš atnaujinant perskirstymą](./media/03_RevRecScenarios.png)](./media/03_RevRecScenarios.png)

    Naujos įplaukų vertės sumos rodomos tinklelio **Eilutės** stulpelyje **Perskirstyta suma**. Šiuo metu perskirstymas yra apdorotas, bet dar nėra apskaičiuotas. Tolesnėje iliustracijoje pateiktas pardavimo užsakymo eilučių atnaujinus perskirstymą pavyzdys.

    [![Pardavimo užsakymo eilutės atnaujinus perskirstymą](./media/04_RevRecScenarios.png)](./media/04_RevRecScenarios.png)

- **Apdoroti** – apdoroti arba registruoti perskirstytas įplaukų vertes. Pasirinkus šį mygtuką nėra galimybių atšaukti perskirstymą. Jei nepasirinkote **Atnaujinti perskirstymą** prieš pasirinkdami **Apdoroti**, perskirstymas bus vykdomas automatiškai.

    - Jei pardavimo užsakymo eilutei nebuvo išrašyta SF, įplaukų vertės sumos atnaujinamos bet kuriame pardavimo užsakyme, kuris buvo pasirinktas perskirstymui.
    - Jei SF išrašyta vienai ar daugiau pardavimo užsakymo eilučių, registruojami korekciniai apskaitos įrašai ir pataisome visa įplaukų grafiko informacija, sukurta pardavimo užsakymo eilutei, kuriai išrašyta SF.

- **Numatomas kvitas** – rodoma apskaitos įrašų, sukurtų bet kurioms pardavimo užsakymo eilutėms, kurioms buvo išrašyta SF, peržiūra. Jei SF nebuvo išrašyta, nerodoma jokia informacija. Jei nepasirinkote **Atnaujinti perskirstymą** prieš pasirinkdami **Numatomas kvitas**, perskirstymas bus vykdomas automatiškai.
- **Įplaukų perskirstymas** – atidaromas puslapis, kuriame rodomas visų pasirinktų eilučių įplaukų vertės paskirstymas. Šiame puslapyje negalima pakeisti jokios informacijos. Joje pateikiamos eilutės sumos, naudotos perskirstymui.

    [![Eilutės sumos, naudotos perskirstymui](./media/05_RevRecScenarios.png)](./media/05_RevRecScenarios.png)

- **Iš naujo nustatyti pasirinkto kliento duomenis** – jei perskirstymo procesas buvo pradėtas, tačiau nebuvo baigtas, perskirstymo lentelėje išvalykite tik pasirinkto kliento duomenis. Pavyzdžiui, perskirstymui pažymite kelias pardavimo užsakymo eilutes, paliekate puslapį atidarytą nepasirinkę **Apdoroti**, tada baigiasi puslapio skirtasis laikas. Tokiu atveju pardavimo užsakymo eilutės liks pažymėtos ir nebus pasiekiamos kitam vartotojui, kad būtų galima baigti perskirstymo procesą. Atidarytas puslapis net gali būti tuščias. Tokiu atveju naudojant mygtuką **Iš naujo nustatyti pasirinkto kliento duomenis** galima išvalyti neapdorotus pardavimo užsakymus, kad kitas vartotojas galėtų baigti perskirstymo procesą.

## <a name="scenarios-for-reallocation"></a>Perskirstymo scenarijai

Įvairūs įplaukų pripažinimo scenarijai aptariami toliau nurodytose temose:

- [Įplaukų pripažinimo perskirstymas – 1 scenarijus](rev-rec-reallocation-scenario-1.md) – įvedami du pardavimo užsakymai, tačiau jie yra tik patvirtinti. Tas pats scenarijus duoda panašius rezultatus, jei daugiau nei dviejų pardavimo užsakymų būsena yra Patvirtinta.
- [Įplaukų pripažinimo perskirstymas – 2 scenarijus](rev-rec-reallocation-scenario-2.md) – įvedami du pardavimo užsakymai, tada klientas įtraukia prekę į sutartį po to, kai SF išrašoma pirmam pardavimo užsakymui.
- [Įplaukų pripažinimo perskirstymas – 3 scenarijus](rev-rec-reallocation-scenario-3.md) – į esamą pardavimo užsakymą, kuriam išrašyta SF, įtraukiama nauja eilutė.
- [Įplaukų pripažinimo perskirstymas – 4 scenarijus](rev-rec-reallocation-scenario-4.md) – iš esamo pardavimo užsakymo, kuriam išrašyta dalinė SF, pašalinama eilutė.
