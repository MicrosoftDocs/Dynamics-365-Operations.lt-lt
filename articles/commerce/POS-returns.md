---
title: Kurti grąžinimus EKA
description: Šiame straipsnyje aprašoma, kaip inicijuoti grynųjų Microsoft Dynamics 365 Commerce pinigų ir (arba) atliekamų operacijų arba klientų užsakymų grąžinimą į programą Point of Sale (EKA).
author: hhainesms
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.20
ms.openlocfilehash: a49e9abd0143d480cc1cafb05be5e995fb3cebdd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857003"
---
# <a name="create-returns-in-pos"></a>Kurti grąžinimus EKA

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip inicijuoti grynųjų Microsoft Dynamics 365 Commerce pinigų ir (arba) atliekamų operacijų arba klientų užsakymų grąžinimus point point sale (EKA) programoje.

> [!NOTE]
> "Commerce 10.0.20" versijoje ir vėliau galima naudoti naują funkciją, kuri **EKA vadinama bendrojo grąžinamo apdorojimo** patirtimi. Ši funkcija teikia nuoseklią ir suvienodintą grąžinimo procesą EKA, nepaisant operacijos tipo (grynųjų pinigų ir perkėlimo operacijos ar kliento užsakymo) ar pradinio kanalo, kuriame buvo sukurtas užsakymas. Rekomenduojame visoms organizacijoms įjungti šią naują funkciją, kad būtų pagerintas bendras grąžinimo apdorojimo EKA patikimumas.
>
> Kai priemonė įjungta, jos išjungti negalima.

## <a name="process-returns-by-using-the-return-transaction-operation"></a>Apdoroti grąžinimus naudojant grąžinimo operacijos operaciją

Rekomenduojame grąžinimo operaciją įtraukti į EKA [ekrano maketą](pos-screen-layouts.md). Leidimuose prieš "Commerce" 10.0.20 versiją, grąžinimo operacijos operacija tinkamai palaiko tik grynųjų pinigų ir carry operacijų grąžinimų apdorojimą. „Commerce“ versija **10.0.20" paleidimo arba vėlesnės versijos įjungus EKA** priemonės bendrojo grąžinimo apdorojimo patirtį, grąžinimo operacijos operacija taip pat palaiko grąžinimų, kilusių iš kliento užsakymų, apdorojimą, pvz., "paėmimas" arba "siųsti į pagrindinį" užsakymą, kuriam jau išrašytos SF.

Grąžinimo operacijos vartotojai gali ieškoti grynųjų pinigų ir carry operacijos arba kliento užsakymo, su kuriuo grįš, įvesdami bet kurį iš nurodytų keturių ieškos kriterijų. Vartotojai gali įvesti šiuos kriterijus naudodami įrenginio klaviatūrą, ekrano klaviatūros ar brūkšninių kodų skaitytuvą.

- Gavimo kvito ID
- Užsakymo numeris
- Kanalo nuorodos ID (taip pat vadinamas užsakymo patvirtinimo ID)
- Sąskaitos faktūros ID

Jei randama operaciją ar užsakymą, kuris atitinka ieškos kriterijus, **rodomas puslapis** Grąžintini produktai. Ten vartotojai gali nurodyti grąžinamas prekes. Jie taip pat gali įvesti grąžinamus kiekius ir priežasčių kodus.

EKA rodo kiekvienos grąžinamų produktų sąrašo užsakymo eilutės informaciją apie pradinį pirkimo kiekį ir visų anksčiau apdorotų grąžinimų kiekius. Grąžinimo kiekis, kurį vartotojas įveda užsakymo eilutėje, turi būti mažesnis arba lygus lauko **Galima grąžinti** vertei.

![Grąžintinas produktų puslapis.](media/returnslist.png)

Grąžinimo apdorojimo metu, jei vartotojas turi fizinį produktą ir tas produktas turi brūkšninius kodus, vartotojas gali nuskaityti brūkšninius kodus, kad galėtų užregistruoti grąžinimą. Kiekvienas brūkšninio kodo nuskaitymas padidina vienos prekės grąžinimo kiekį. Tačiau jei brūkšninio kodo žymėje yra įdėtas kiekis, šis kiekis bus **įvestas į lauką** Grąžinimas dabar.

Vartotojai taip pat gali rankiniu būdu pasirinkti **grąžintinas prekes** puslapyje ir tada atnaujinti **Grąžinimas dabar** naudodami dešinės pusės informacijos sritį.

Jei operacijai nurodomas didžiausias galimas **Grąžinimo dabar** kiekis, vartotojas gali EKA programos juostoje pasirinkti pasirinkti visą **Operaciją, kad** būtų nustatytas didžiausias grąžintinas kiekis visose eilutėse.

Kiekvienoje eilutėje, kurios **grąžinimo dabar** kiekis yra, vartotojas turi pasirinkti grąžinimo priežasties kodą, naudodamas informacijos skydą. Grynųjų pinigų ir carry operacijų grąžinimo priežasties kodai sukonfigūruoti kaip informacijos kodai parduotuvės funkcijų šablone. Klientų užsakymų grąžinimo grąžinimo priežasties kodai yra sukonfigūruoti pardavimo **užsakymų grąžinimo** priežasčių kodų „Dynamics 365 Commerce“ puslapyje.

Kai grąžinimo kiekis ir priežasties kodas nustatomas kiekvienai prekei, kurią reikia grąžinti, vartotojas gali pasirinkti grąžinimo operaciją EKA programos juostoje, kad būtų **tęsiamas** apdorojimas. Rodomas EKA operacijų puslapis, kuriame į krepšelį buvo pridėtos ankstesniame puslapyje pasirinktos grąžintinos prekės. Dabar **grąžinti prekių** kiekiai operacijos metu rodomi kaip neigiamo kiekio eilutės, ir apskaičiuojamas bendras grąžinimas.

Vartotojai gali įtraukti eilutes į grąžinimo operaciją, jei jie kuria keitimo užsakymą. Vartotojai taip pat gali įtraukti daugiau ad hoc grąžinamų prekių į grąžinimo operaciją, naudodami grąžinimo produkto operaciją pridėtai teigiamo kiekio **pardavimo eilutei**.

> [!NOTE]
> EKA pateikiama produkto **leidžia grąžinti** bet kokį grąžinimo operacija nepateikia jokių pradinių operacijų patikrinimo ir produktą. Todėl rekomenduojame, kad šią operaciją būtų leidžiama atlikti tik įgaliotiems vartotojams arba, jei ši operacija naudojama, būtų reikalaujama vadybininko nepaisymo.

Jei grąžinimas turi būti išregistruojamas, organizacijos gali konfigūruoti [grąžinimo mokėjimo strategijas](refund_policy_returns.md), kurios riboja mokėjimo metodus, kurie gali būti naudojami grąžinti klientams. Jei pradinė operacija buvo sumokėta naudojant kredito kortelę, atsižvelgiant į mokėjimo procesorių ir sistemos konfigūraciją, vartotojai gali turėti galimybę išduoti grąžinimą [originaliai kortelei](dev-itpro/linked-refunds.md). Tokiu atveju grąžinimas gali būti apdorotas nereikalaujant, kad klientas vėl perbrauktų savo kredito kortelę. Pradinis mokėjimo atpažinimo ženklas naudojamas norint išduoti grąžinimą.

## <a name="other-return-options-in-pos"></a>Kitos grąžinimo parinktys EKA

Kai **EKA priemonėje įjungta bendrojo grąžinimo apdorojimo** funkcija įjungta, vartotojai gali taip pat naudoti **Rodyti žurnalą**  kad inicijuotų grynųjų pinigų ir carry operacijos arba kliento užsakymo grąžinimą. Tada jie žurnale galės pasirinkti operaciją, o tada **EKA** programos juostoje pasirinkti grąžinimo operaciją. Ši operacija galima tik tada, kai užsakyme yra grąžintimų eilučių. Jis inicijuoja tą patį vartotojo patirtį kaip ir **grąžinimo operacijos** operacija.

Be to, vartotojai **EKA gali** ieškoti ir atšaukti klientų užsakymų naudodami operaciją Atšaukti užsakymą. (Šios operacijos negalima naudoti grynųjų pinigų ir carry operacijoms). Tokiu atveju, kai pasirenkamas kliento užsakymas, EKA programos juostoje naudojama grąžinimo operacija gali būti naudojama kliento **užsakymo** grąžinimui inicijuoti. Ši operacija galima tik tada, kai užsakyme yra grąžintimų eilučių. Jis inicijuoja tą patį vartotojo patirtį kaip ir **grąžinimo operacijos** ar **Rodyti žurnalą** operacija.

## <a name="return-orders-are-posted-to-commerce-headquarters-as-sales-orders"></a>Grąžinimo užsakymai registruojami „Commerce Headquarters" kaip pardavimo užsakymai 

Kai **EKA priemonėje įjungta bendrojo grąžinimo apdorojimo** funkcija, visi EKA sukurti grąžinimai į "Commerce Headquarters" rašomi kaip pardavimo užsakymai, kurių eilutės neigiamos. Leidimuose prieš „Commerce" 10.0.20 versiją vartotojai gali pasirinkti, ar grąžinimo užsakymai turi būti registruojami kaip pardavimo užsakymai, kurių eilutės neigiamos, ar turėtų būti grąžinami užsakymai, kurie kuriami vykdant grąžinamų prekių autorizavimo (RMA) procesą. 

EKA **priemonės bendrojo grąžinimo apdorojimo** proceso metu buvo pasenusi parinktis, naudotin RMA procesą grąžinimams kurti EKA. Kai ši funkcija įjungta, visi grąžinimai bus kuriami kaip pardavimo užsakymai su neigiamomis eilutėmis.

## <a name="offline-return-processing-improvements"></a>Autonominio grąžinimo apdorojimo patobulinimai

Kai grąžinimas apdorojamas EKA, daugeliu atvejų sistema bando iškviesti „Commerce Headquarters" „Real-time Service" (RTS) ir patikrinti dabartinius kiekius, kuriuos galima grąžinti. Šis tikrinimas padeda išvengti apgaulingų scenarijų, kuriuose klientas bando grąžinti tą pačią prekę keliose vietose.

Siekiant tvarkyti situacijas, kai RTS iškvietimo nepavyksta padaryti dėl tinklo arba ryšio problemų, buvo sukurtas procesas, siekiant periodiškai sinchronizuoti grąžinimo kiekio duomenis iš "Commerce Headquarters" į parduotuvės kanalų duomenų bazę. Šis kanalo grąžinimo sekimas padeda užtikrinti, kad galima grąžinti EKA parodytus kiekius **būtų tikslūs,** net jei EKA yra autonominis. Taip pat užtikrinama, kad EKA gali toliau tikrinti kanalo informaciją, kad išvengtų apgaulingų grąžinimų.

Kad grąžinimo neprisijungus procesas būtų naudojamas tinkamai, organizacijos "Commerce Headquarters" turėtų planuoti paketinę užduotį **Naujinti grąžinamus kiekius**, kad ji būtų vykdoma dažnai. Rekomenduojame šią užduotį vykdyti tuo pačiu dažnumu kaip ir P užduotis, kuri iš „Commerce" kanalų vykdo naujas operacijas į „Commerce Headquarters".

Atnaujinimo kiekių užduotis apskaičiuoja kiekį, kurį galima grąžinti **visiems pardavimo užsakymams,** kurie randami „Commerce Headquarters". Tada užduoties apskaičiuojami duomenys turi būti siunčiami į kanalo duomenų bazes, kad būtų galima atnaujinti parduotuvės kanalus. Šiuo **tikslu naudojama** grąžinimo kiekių (1200) paskirstymo užduotis. Dėl to, kad "Commerce Headquarters" sinchronizuojami duomenys apie grąžintimą kiekį, jei grąžinimas apdorojamas EKA, bet negalima atlikti RTS iškvietimo, EKA gali naudoti grąžinimo kanale informaciją, kad galėtų patikrinti kiekį, kurį galima pateikti į nurodytą **pardavimo eilutę**.

Kai RTS skambučių atlikti negalima, o EKA grąžinimo patvirtinimui naudoja kanalo duomenis, perspėjimo pranešimas informuoja vartotojus, kad jie kuria grąžinimą ne tinkle. Todėl jie žino, kad **galimas grąžinimo** rodomas EKA, gali būti nebegalioja arba nebėra tikslus, atsižvelgiant į tai, kada paskutinį kartą **buvo apdorota grąžinimo** kiekių atnaujinimo užduotis ir sinchronizuojama su kanalu.

Pavyzdžiui, klientas neseniai apdorojo užsakymo eilutės grąžinimą kitame kanale, bet šie duomenys dar nebuvo sinchronizuoti su kanalo duomenų bazėmis naudojant užduotį **Attnaujinti grąžinimo kiekius**. Tada klientas eina į kitą parduotuvę ir bando vėl grąžinti tą pačią prekę. Tokiu atveju, jei parduotuvė negali iškviesti RTS į "Commerce Headquarters", kad būtų gauti realiuoju laiku grąžinami duomenys, EKA leis prekę grąžinti dar kartą. Tačiau vartotojas įspėjamas, kad informacija, naudojama grąžinimui patikrinti, gali būti nepateisinta. Pranešimas, kurį gauna vartotojas, yra tik įspėjamasis pranešimas. Tai neleidžia vartotojui tęsti grąžinimo proceso.

Jei kanalo informacija dėl kokių nors priežasčių nėra naujausia ir vykdomas grąžinimas ne tinkle, kai grąžinama daugiau nei faktinis turimas kiekis, gali būti sugeneruojama klaida, kai vykdomas išrašo registravimas, kad **būtų sukurta operacija** „Commerce Headquarters".

> [!NOTE]
> Kai EKA **priemonėje įjungta bendrojo grąžinimo apdorojimo** funkcija, galimos naujos pasirenkamos priemonės, kurios palaiko eilutėmis išdėstyti produktų grąžinimų tikrinimą. Daugiau informacijos ieškokite Grąžinimo [serijos numerio kontroliuojami produktai, esantys Point of Sale (EKA)](POS-serial-returns.md).

## <a name="version-details"></a>Versijos informacija

Toliau pateiktame sąraše pateikiami mažiausi įvairių komponentų versijos reikalavimai.
- "Commerce Headquarters": 10.0.20 versija
- "Commerce Scale Unit" (CSU): 9.30 versija
- Point of sale (EKA): 9.30 versija

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Įjungti tinkamą mokesčių skaičiavimą, kai grąžinamas dalinis kiekis

Šia funkcija užtikrinama, kad užsakymą grąžinus naudojant kelias sąskaitas faktūras, galiausiai mokesčiai bus lygūs pirminei mokėtinai mokesčių sumai.

1. Funkcijų valdymo **darbo srityje ieškokite** Įgalinti tinkamą mokesčių **skaičiavimą, jei grąžinimai atlikti su daliniu kiekiu**.
1. Pasirinkite įgalinti **tinkamą mokesčių skaičiavimą, kai grąžinimai turi dalinio** kiekio funkciją, tada pasirinkite **Įgalinti**.

## <a name="set-up-return-locations-for-retail-stores"></a>Parduotuvių grąžinimo vietų nustatymas

"Commerce" leidžia nustatyti grąžinimo vietas pagal mažmeninės prekybos informacijos kodus ir pardavimo ir rinkodaros priežasčių kodus. Kai klientai grąžina pirkimą, kasininkas dažnai nurodo grąžinimo priežastį. Galite nurodyti, kad grąžinti produktai būtų priskirti skirtingoms grąžinimo atsargoms vietai, remiantis informacijos kodais ir priežasčių kodais, kuriuos kasininkas pasirenka EKA kasos aparate.

Pavyzdžiui, klientas grąžina produktą su trūkumais, o kasininkas apdoroja grąžinimo operaciją. Kai "Retail POS" rodo grąžinimo informacijos kodą, kasininkas pasirenka grąžinimo su trūkumais tarpinį kodą. Tada grąžintas produktas automatiškai priskiriamas konkrečiai grąžinimo vietai.

Grąžinimo vieta gali būti sandėlis, vieta sandėlyje ar netgi konkretus padėklas, priklausomai nuo jūsų organizacijos nustatytų atsargų vietų. Kiekvieną grąžinimo vietą galite susieti su vienu ar daugiau mažmeninės prekybos informacijos kodų ir pardavimo ir rinkodaros priežasčių kodų.

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš tai, kai galėsite nustatyti grąžinimo vietas, turite nustatyti šiuos elementus:

- **Mažmeninės prekybos informacijos** kodai – paragina kasos aparatu, kurie nustatomi "Retail" **modulyje**. Daugiau informacijos rasite informacijos [kodų nustatymas](/dynamicsax-2012/appuser-itpro/setting-up-info-codes).
- **Pardavimo ir rinkodaros priežasčių kodai** – paragina EKA kasos aparate, kurie nustatomi pardavimo **ir rinkodaros modulyje**. Daugiau informacijos rasite Priežasčių [kodų nustatymas](/dynamicsax-2012/appuser-itpro/set-up-return-reason-codes).
- **Atsargų vietos** – vietos, kuriose laikomos atsargos. Daugiau informacijos rasite [Atsargų vietų nustatymas](/dynamicsax-2012/appuser-itpro/about-locations).
    
### <a name="set-up-return-locations"></a>Nustatyti grąžinimo vietas

Norėdami nustatyti grąžinimo vietas, atlikite šiuos veiksmus.

1. Eikite į **"Retail" ir "Commerce \> Channel" \> nustatymo sandėlius** ir pasirinkite sandėlį.
1. Mažmeninės **prekybos** "FastTab" lauke Numatytoji grąžinimo vieta pasirinkite atsargų vietą, **kuri** bus naudojama grąžinimams, kai informacijos kodai ar priežasčių kodai nėra susieti su grąžinimo vieta.
1. Numatytojo **grąžinimo padėklo** lauke pasirinkite padėklą, naudotiį grąžinimams, kurių informacijos kodai arba priežasčių kodai nėra susieti su grąžinimo vietas.
1. Eikite į **"Retail" ir "Commerce \> Inventor management \> Return" vietas**.
1. Pasirinkite **Naujas,** jei norite sukurti grąžinimo vietos strategiją.
1. Įveskite unikalų grąžinimo vietos pavadinimą ir aprašą.

    > [!NOTE]
    > Jei nustatyta grąžinimo vietų numeracija, pavadinimas įvedamas automatiškai.

1. Bendrajame **"** FastTab" nustatykite parinktį **Spausdinti etiketes** kaip **Taip**, norėdami išspausdinti visų produktų, priskirtų grąžinimo vietų, etiketes.
1. Nustatykite **pasirinktį Blokuoti** atsargas kaip **Taip,** jei norite grąžinti produktus iš numatytosios grąžinimo vietos į atsargas ir neleisti jų parduoti.
1. Norėdami susieti konkrečius mažmeninės prekybos informacijos kodus ir antrinius kodus su grąžinimo vieta, atlikite šiuos veiksmus:

    1. Mažmeninės prekybos **informacijos kodų "** FastTab" pasirinkite **Įtraukti**.
    1. **Informacijos kodo lauke** pasirinkite grąžinimo informacijos kodą.
    1. **Lauke Antrinis** kodas pasirinkite grąžinimo priežasties antrinius kodus. Aprašymo **lauke** rodomas pasirinkto antrinio kodo aprašymas.
    1. Lauke Parduotuvė **pasirinkite** parduotuvę, kurioje naudojamas informacijos kodas.
    1. Norėdami nurodyti **grąžinimo vietą**, **naudokite** laukus **Sandėlis**, Vieta ir Padėklo ID. Pavyzdžiui, norėdami nurodyti vietą parduotuvėje, pasirinkite parduotuvę **lauke Parduotuvė**, o lauke **Vieta**.
    1. Pažymėkite žymės **langelį Blokuoti atsargas**, kad grąžinti produktai nebūtų atsargose ir nebūtų parduoti.

1. Norėdami susieti konkrečius pardavimo ir rinkodaros priežasčių kodus su grąžinimo vietas, atlikite šiuos veiksmus:

    1. Pardavimo ir **rinkodaros priežasčių koduose "** FastTab" pasirinkite **Įtraukti**.
    1. **Lauke Priežasties kodas** pasirinkite grąžinimo priežasties kodą. **Lauke** Aprašymas rodomas pasirinkto priežasties kodo aprašymas.
    1. Lauke Parduotuvė **pasirinkite** parduotuvę, kurioje naudojamas priežasties kodas.
    1. Norėdami nurodyti **grąžinimo vietą**, **naudokite** laukus **Sandėlis**, Vieta ir Padėklo ID. Pavyzdžiui, norėdami nurodyti padėklą vietoje sandėlyje, pasirinkite sandėlį, **sandėlį,** **vietą lauke Vieta, o padėklą – lauke** Padėklo ID **.**
    1. Pažymėkite žymės **langelį Blokuoti atsargas**, kad grąžinti produktai nebūtų atsargose ir nebūtų parduoti.

    > [!NOTE]
    > Jei prekei naudojama grąžinimo vietos strategija, bet grąžinimo priežastis, **kurią kasininkas pasirenka, neatitinka jokio kodo, nurodyto "Retail** **·**" informacijos koduose arba pardavimo ir rinkodaros priežasčių koduose "FastTab", prekė siunčiama į numatytąją **grąžinimo** vietą, kuri nurodyta sandėlio puslapyje. Be to, žymės **·** **langelio** Blokuoti atsargas parametras, esantis puslapio Grąžinimo vietų bendra **FastTab**, nustato, ar grąžinta prekė turi būti užblokuota atsargos.

1. Eikite į " **Retail" ir "Commerce \> Commerce" produktų hierarchiją**.
1. Skirtuko Valdyti **atsargų kategorijos ypatybes** "FastTab" lauke **Grąžinimo** vieta pasirinkite grąžinimo vietą. Kadangi tai pačiai parduotuvei galima nustatyti kelias grąžinimo vietos strategijas, čia jūsų naudojama reikšmė lemia naudojamą grąžinimo vietos strategiją.

## <a name="additional-resources"></a>Papildomi ištekliai

[Grąžinti serijos numeriais kontroliuojamus produktus naudojant prekybos vietos EKA](POS-serial-returns.md)

[Susietas anksčiau patvirtintų ir patvirtintų operacijų grąžinimas](dev-itpro/linked-refunds.md)

[Kanalo prekių ir pinigų grąžinimų strategijos kūrimas ir naujinimas](refund_policy_returns.md)

[EKA vartotojo sąsajos vaizdinio elemento konfigūracijos](pos-screen-layouts.md)
