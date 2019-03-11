---
title: Pardavimo grąžinimai
description: Šioje temoje pateikiama informacija apie grąžinimo užsakymų procesą. Ji apima informaciją apie klientų grąžinimus ir jų poveikį įkainojimui ir turimų atsargų kiekiui.
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3dfeb393698431b1bbb0eb5069cc0930dc122374
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "362699"
---
# <a name="sales-returns"></a>Pardavimo grąžinimai

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie grąžinimo užsakymų procesą. Ji apima informaciją apie klientų grąžinimus ir jų poveikį įkainojimui ir turimų atsargų kiekiui.

Klientai gali grąžinti prekes dėl įvairių priežasčių. Pvz., prekė gali turėti defektų arba gali neatitikti kliento lūkesčių. Grąžinimo užsakymo procesas prasideda, kai klientas pakeikia prašymą gražinti prekę. Po to, kai gaunamas kliento prašymas, „Microsoft Dynamics 365 for Finance and Operations“ sukuriamas grąžinimo užsakymas.

## <a name="return-order-process"></a>Grąžinimo užsakymo procesas
Toliau esančiame paveikslėlyje pateikiama grąžinimo užsakymo proceso apžvalga.  

[![Grąžinimo užsakymo procesas](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

Yra dviejų tipų grąžinimo užsakymo procesai: fizinis grąžinimas ir tik kreditas.

-   **Fizinis grąžinimas** – grąžinimo užsakymas įgalioja fizinį produktų grąžinimą.
-   **Tik kreditas** – grąžinimo užsakymas įgalioja kliento kreditą, bet nėra būtina klientui fiziškai grąžinti produktus.

### <a name="physical-return-order-process"></a>Fizinio grąžinimo užsakymo procesas

1.  **Kurti grąžinimo užsakymą.** Formaliai dokumentuokite kliento įgaliojimą grąžinti turinčius defektų arba nepageidaujamus produktus. Pagal grąžinimo užsakymą nėra reikalaujama, kad įmonė priimtų grąžintus produktus arba klientui suteiktų kreditą. Jei grąžinimas priimtas, galite įgalioti išsiųsti prekės pakaitalą dar nesugrąžinus prekės su defektu.
2.  **Atvykti į sandėlį apžiūrėti.** Užpildykite pradinio tikrinimo ir patvirtinimo pagal grąžinimo užsakymą dokumentą. Grąžinimo užsakymas palaiko grąžintų prekių sulaikymą papildomai apžiūrai ir kokybės kontrolei.
3.  **Nustatykite perdavimą.** Užbaikite patikrinimo procesą ir nuspręskite, ką reikia daryti su grąžinamais produktais. Kaip šio veiksmo dalį, nuspręskite, ar kredituosite klientą, atmesite produkto grąžinimą, ar priimsite produkto grąžinimą, nurašysite produktą ir tada klientui nusiųsite pakeitimo produktą.
4.  **Generuoti važtaraštį.** Generuokite važtaraštį ir vykdykite perdavimo sprendimą, kurį priėmėte 3 veiksme. Užbaikite logistikos procesus.
5.  **Generuokite sąskaitą faktūrą.** Uždarykite grąžinimo užsakymą.

### <a name="credit-only-process"></a>Tik kredito procesas

1.  **Kurti grąžinimo užsakymą.** Formaliai dokumentuokite kliento įgaliojimą gauti kreditą negrąžinanant produktų su defektais arba nepageidaujamų produktų. **Tik kreditas** perdavimo kodas įgalioja sprendimą kredituoti klientą be fizinio grąžinimo.
2.  **Generuokite sąskaitą faktūrą.** Sugeneruokite kredito pažymą, tada uždarykite grąžinimo užsakymą.

## <a name="return-material-authorization"></a>Grąžinamų medžiagų autorizavimas
Grąžinamų medžiagų autorizavimo (RMA) apribojimas pagrįstas pardavimo užsakymo funkcija. RMA registruojamas kaip grąžinimo užsakymas, kuris sukurtas kaip pardavimo užsakymas, su juo gali būti susietas kitas pardavimo užsakymas, vadinamas pakeitimo užsakymu. Abu pardavimo užsakymai susieti su pradinio RMA numeriu.

-   **Grąžinimo užsakymas** – norėdami užregistruoti RMA, sukurkite pardavimo užsakymą, kuris yra pardavimo užsakymas su priskirtu tipu **Grąžintas užsakymas.** Visi atliekami RMA informacijos pakeitimai automatiškai atnaujinami pardavimo užsakyme. Kol grąžinimo užsakymo būsena yra **Atidaryta**, jis nebus rodomas pardavimo užsakymų sąraše. RMA naudojamas tvarkyti grąžintų prekių pristatymą ir gavimą, be to, įgalioti tik kredito perdavimo veiksmą (žr. skyrių **Perdavimo kodas ir perdavimo veiksmai**). Visus kitus tolesnius procesus reikia tvarkyti pardavimo užsakyme.
-   **Pakeitimo tvarka** – kai pakeitimo užsakymą reikia išsiųsti klientui, RMA gali apimti ir antrą susietą pardavimo užsakymą. Galite rankiniu būdu sukurti RMA pakeitimo užsakymą skubiai siuntai palaikyti. Kitu atveju, pakeitimo užsakymą galima sukurti automatiškai, baigus pristatymą, patikrinimą ir gavimą RMA eilutės prekės, turinčios perdavimo kodą, kuris nurodo pakeitimą. Pakeitimo užsakymas turi tą pačią funkciją, kuri susieta su pardavimo užsakymu. Pvz., galite jį naudoti pasirinktam produktui konfigūruoti kaip pakeitimo prekę, sukurti gamybos užsakymą grąžintai prekei pataisyti, sukurti tiesioginio pristatymo pirkimo užsakymą, norėdami pakeitimą išsiųsti iš tiekėjo, arba kitiems tikslams palaikyti.

## <a name="create-a-return-order"></a>Grąžinimo užsakymo kūrimas
Grąžinimo užsakymo procesas prasideda, kai klientas susisiekia su jūsų organizacija norėdamas grąžinti produktą su defektu arba nenorimą produktą ir / arba gauti kreditą. Po to, kai jūsų organizacija priims grąžinimą, jis dokumentuojamas grąžinimo užsakymu. Šis grąžinimo užsakymas tampa grąžinto produkto vidinio apdorojimo centrine ašimi. Toliau pateikiamoje iliustracijoje pavaizduota grąžinimo užsakymo kūrimo procedūra.  

[![Grąžinimo užsakymo kūrimo procedūra](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>Grąžinimo užsakymo antraštės kūrimas

Kuriant grąžinimo užsakymą, jame turi būti toliau pateikiamoje lentelėje nurodyta informacija.

| Laukas              | aprašymas                                              | Komentarai                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kliento kodas   | Nuoroda į kliento lentelę                       | Turite pateikti esamą kliento sąskaitą.                                                                                                                                                                                                                                                                                                  |
| Pristatymo adresas   | Adresas, kuriuo prekė grąžinta.                 | Pagal numatytuosius nustatymus naudojamas organizacijos adresas. Jei antraštėje pasirenkamas konkretus sandėlis, pristatymo adresas pakeičiamas į sandėlio pristatymo adresą. Šį adresą galite pakeisti puslapyje **Grąžinimo užsakymų informacija**.                                                                                                  |
| Svetainė / sandėlis     | Svetainė arba sandėlis, gaunantis grąžinamą produktą | Grąžinimo užsakymo pristatymo adresas nustatomas pagal svetainės arba sandėlio pristatymo adresą.                                                                                                                                                                                                                                 |
| RMA numeris         | Grąžinimo užsakymui priskirtas ID              | RMA numeris naudojamas kaip alternatyvusis raktas grąžinimo užsakymo proceso metu. Priskirtas RMA numeris yra pagrįstas RMA numeracija, kuri nustatyta puslapyje **Gautinų sumų parametrai**.                                                                                                                              |
| Galutinis terminas           | Paskutinė data, kai prekė gali būti grąžinta               | Numatytoji vertė apskaičiuojama kaip dabartinė data plius galiojimo laikotarpis. Pvz., jei grąžinimas galioja tik 90 dienų nuo datos, kada sukurtas grąžinimo užsakymas, o jis buvo sukurtas gegužės 1 d., vertė šiame lauke yra **Liepos 30 d.**. Galiojimo laikas nustatomas puslapyje **Gautinų sumų parametrai**. |
| Grąžinimo priežasties kodas | Kliento priežastis, dėl kurios grąžina produktą          | Priežasties kodas pasirenkamas iš vartotojo nustatytų priežasties kodų sąrašo. Lauką galima bet kada atnaujinti.                                                                                                                                                                                                                                    |

### <a name="create-return-order-lines"></a>Grąžinimo užsakymo eilučių kūrimas

Užbaigę grąžinimo antraštę, galite kurti grąžinimo eilutes pagal vieną iš šių metodų:

-   Rankiniu būdu įveskite prekės informaciją, kiekį ir kitą informaciją kiekvienoje grąžinimo eilutėje.
-   Grąžinimo eilutę kurkite naudodami funkciją **Rasti pardavimo užsakymą**. Rekomenduojame naudoti šią funkciją, kai kursite grąžinimo užsakymą. Funkcija **Rasti pardavimo užsakymą** sukuria nuorodą iš grąžinimo eilutės į pardavimo užsakymo eilutę, kuriai išrašyta SF, ir iš pardavimo eilutės nuskaito eilutės informaciją, pvz., prekės numeris, kiekis, kaina, nuolaida ir savikainos vertes. Nuoroda padeda užtikrinti, kad kai produktas grąžinamas įmonei, jis įvertintas tokia pat savikaina, kokia ir buvo parduotas. Nuoroda taip pat patvirtinama, kad grąžinimo užsakymų nesukuriama tiek, kad kiekis viršytų sąskaitoje faktūroje nurodytą kiekį.

>[Pastaba!] Grąžinimo eilutės, turinčios nuorodą į pardavimo užsakymą, tvarkomos kaip pardavimo pataisos arba atšaukimai. Išsamesnės informacijos žr. skyriuje „Registravimas į didžiąją knygą“ toliau šioje temoje.

### <a name="charges"></a>Išlaidos

Mokėjimus ir mokesčius galima įtraukti į grąžinimo užsakymą vienu ar daugiau iš toliau nurodytų metodų:

-   Mokesčius galite rankiniu būdu įtraukti į grąžinimo užsakymo antraštę, grąžinimo užsakymo eilutę arba į abi.
-   Išlaidas galima automatiškai įtraukti į grąžinimo užsakymo antraštę kaip grąžinimo priežasties kodo funkciją.
-   Mokesčius galima automatiškai įtraukti į grąžinimo užsakymo eilutę pagal eilutės perdavimo kodą.

Išlaidos įtraukiamos automatiškai po to, kai grąžinimo priežasties kodas ar perdavimo kodas priskiriamas eilutei. Jei priežasties kodas keičiamas vėliau, esamas išlaidų įrašas nebus pašalintas, bet naują išlaidų įrašą galima įtraukti pagal naują priežasties kodą. Įtraukiant mokesčius į grąžinimo užsakymo eilutes, eilutės išlaidos, apskaičiuotos procentine išraiška, arba jei užsakymo vertė tampa neigiama, kai eilutė ar eilutės užsakymas yra neigiamas skaičius, nebent procentinė išraiška taip pat yra neigiamas skaičius. Neigiamos vertės mokestis reiškia klientui suteiktą kreditą.

### <a name="return-reason-codes"></a>Grąžinimo priežasčių kodai

Grąžinimams taikant priežasties kodus, galima padėti supaprastinti grąžinimo modelių analizę. Priežasties kodai pateikia informacijos apie tai, kodėl klientas nori grąžinti prekes. Kai kurios organizacijos turi daug priežasčių kodų. Tokios organizacijos gali grupuoti priežasties kodus į priežasties kodų grupes, siekiant gauti geresnę apžvalgą ir sukaupti ataskaitas.

### <a name="disposition-codes-and-disposition-actions"></a>Perdavimo kodai ir perdavimo veiksmai

Svarbus grąžinimo užsakymo proceso veiksmas yra perkėlimo kodo priskyrimas į grąžinimo užsakymo eilutę kaip pristatymo registravimo dalį. Perdavimo kodas nustato šią informaciją:

-   **Finansinės įžvalgos** – ar klientas turi būti kredituojamas už grąžintas prekes, ir ar turėtų į grąžinimo užsakymo eilutę būti įtraukti kokie nors mokesčiai?
-   **Grąžintos prekės perdavimas** – ar gali prekė vėl būti įtraukta į atsargas, ar ji turi būti nurašyta, ar ji turėtų būti grąžinta klientui?
-   **Grąžintos prekės logistika** – ar pakaitalas turi būti išduotas klientui?

Be to, kad reikia nustatyti, kaip grąžintos prekės turi būti likviduotos, grąžinimo eilutei gali būti taikomi mokesčiai pagal perdavimo kodus. Jie gali būti naudojami ir grąžinimams sugrupuoti statistinės analizės tikslais. Perdavimo kodai nustatomi kaip grąžinimo užsakymų nustatymo dalis. Tačiau kiekvienas perdavimo kodas turi nurodyti vieną iš įtaisytųjų perdavimo veiksmų. Šioje lentelėje pateikti įtaisytieji perdavimo kodai ir jų veiksmai. **Svarbu:** jei prekė neturi būti grąžinta, bet klientas vis tiek turi būti kredituojamas, grąžinimo eilutei priskirkite perdavimo kodą **Tik kreditas**.

<table>
<thead>
<tr class="header">
<th>Perdavimo kodas</th>
<th>Finansinės įžvalgos</th>
<th>Įžvalgos dėl logistikos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tik kreditas</td>
<td><ul>
<li>Klientui suteikiamas kreditas siekia pardavimo kainą, atėmus mokesčius ar išlaidas.</li>
<li>Prekės nurašymo nuostolis užregistruojamas didžiojoje knygoje.</li>
</ul></td>
<td>Prekė neturi būti grąžinta. Perdavimo veiksmas naudojamas šiais atvejais:
<ul>
<li>Tarp šalių yra pakankamas pasitikėjimas.</li>
<li>Prekės su defektu grąžinimo savikaina yra draudžiamoji.</li>
<li>Prekių negalima grąžinti atgal į atsargas. Dėl kitų sąlygų, fizinio grąžinimo nereikalaujama.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kreditas</td>
<td><ul>
<li>Klientui suteikiamas kreditas siekia pardavimo kainą, atėmus mokesčius ar išlaidas.</li>
<li>Atsargų vertė padidinama pagal grąžintos prekės savikainą.</li>
</ul></td>
<td>Prekė grąžinama ir įtraukiama atgal į atsargas.</td>
</tr>
<tr class="odd">
<td>Keitimas ir kreditas</td>
<td><ul>
<li>Klientui suteikiamas kreditas siekia pardavimo kainą, atėmus mokesčius ar išlaidas.</li>
<li>Atsargų vertė padidinama pagal grąžintos prekės savikainą.</li>
<li>Pakeitimui sukuriamas atskiras pardavimo užsakymas, kuris tvarkomas atskirai.</li>
</ul></td>
<td>Prekė grąžinama ir įtraukiama atgal į atsargas.</td>
</tr>
<tr class="even">
<td>Keitimas ir nurašymas</td>
<td><ul>
<li>Klientui suteikiamas kreditas siekia pardavimo kainą, atėmus mokesčius ar išlaidas.</li>
<li>Prekės nurašymo nuostolis užregistruojamas didžiojoje knygoje.</li>
<li>Pakeitimui sukuriamas atskiras pardavimo užsakymas, kuris tvarkomas atskirai.</li>
</ul></td>
<td>Prekė grąžinama ir nurašoma.</td>
</tr>
<tr class="odd">
<td>Grąžinti klientui</td>
<td>Nėra, išskyrus mokesčius ar išlaidas.</td>
<td>Prekė grąžinta, bet po patikrinimo išsiųsta atgal klientui. Perdavimo veiksmas gali būti naudojamas, jei prėkė buvo sąmoningai sugadinta, arba jei buvo anuliuota garantija.</td>
</tr>
<tr class="even">
<td>Nurašyta</td>
<td><ul>
<li>Klientui suteikiamas kreditas siekia pardavimo kainą, atėmus mokesčius ar išlaidas.</li>
<li>Prekės nurašymo nuostolis užregistruojamas didžiojoje knygoje.</li>
</ul></td>
<td>Prekė grąžinama arba nurašoma.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>Gavimas sandėlyje patikrinimui atlikti
Prieš fiziškai gaunant grąžinamas prekes į sandėlį užregistravus važtaraštį, prekės turi būti užregistruotos pristačius ir, pasirinktinai, patikrintos. Toliau esančiame paveikslėlyje pateikiama pristatymo proceso apžvalga. Tolesniuose skyriuose aprašytas kiekvienas veiksmas, parodytas iliustracijoje.  

[![Gavimo procesas](./media/salesreturn03.png)](./media/salesreturn03.png)  

Šis procesas turi kelis variantus, kurie šioje temoje neaptariami. Toliau pateikiamos kai kurie iš šių variantų.

-   Nenaudokite sąrašo **Gavimo apžvalga** Gavimo žurnalui sukurti. Gavimo žurnalą sukurkite rankiniu būdu. Grąžinimo užsakymuose kaip nuoroda bus **Pardavimo užsakymas**.
-   Jei naudojate Sandėlio valdymą, sugeneruokite padėklų transportavimą. Padėklų transportavimo metu grąžinimo eilutės būsena bus **Gauta**.
-   Grąžintos prekės gavimą registruokite tiesiogiai iš grąžinimo užsakymo eilutės naudodami funkciją **Registravimas**.

Gavimo proceso metu grąžinimai integruojami su bendruoju sandėlio gavimo procesu. Gavimo procesastaip pat palaiko sulaikymo užsakymų kūrimą grąžinamoms prekėms, kurias reikia atskirai patikrinti.

### <a name="identify-products-in-the-arrival-overview-list"></a>Produktų identifikavimas Gavimo apžvalgos sąraše

Puslapyje **Gavimo apžvalga** pateikiamas visų suplanuotų įeinančių gavimų sąrašas. 
>[Pastaba!] Gavimus iš grąžinimo užsakymų reikia apdoroti atskirai nuo kitų tipų gavimo operacijų. Po to, kai identifikuosite gaunamą paketą puslapyje **Gavimo apžvalga** (pvz., naudojant lydintį RMA dokumentą), veiksmų srityje spustelėję **Pradėti gavimą** kurkite ir inicijuokite gavimo žurnalą, kuris sutampa su gavimu.

### <a name="edit-the-arrival-journal"></a>Gavimo žurnalo redagavimas

Nustatydami parinktį **Sulaikymo valdymas** į **Taip**, grąžinimo eilutei galite kurti sulaikymo užsakymą. Jei eilutė išsiųsta sulaikyti dėl patikrinimo, galite nurodyti perdavimo kodą. 
 
Jei nustatysite prekės atsargų modelio grupės parinkties **Sulaikymo valdymas** reikšmę **Taip**, parinktis **Sulaikymo valdymas** puslapyje **Žurnalo eilutės** bus pažymėta gavimo žurnalo eilutei ir jos nebebus galima keisti. Jei eilutė siunčiama sulaikyti, turite nurodyti atitinkamą sulaikymo sandėlį. 

Jei gavimo eilutė nesiunčiama patikrinti, sandėlio gavimo klerkas turi nurdyti perdavimo kodą tiesiogiai į gavimo žurnalo eilutę, tada užregistruoti gavimo žurnalą. Jei tas pats perdavimo kodas neturėtų būti priskirtas visam grąžinimo eilutės kiekiui, arba visas eilutės kiekis nebuvo gautas, turite skaidyti eilutę. Suskaidę gavimo žurnalo eilutę, kartu suskaidote ir grąžinimo eilutę (**SalesLine**) ir sukuriate naują partijos ID. Eilutę suskaidyti galite sumažinę gavimo žurnalo eilutės kiekį. Kai žurnalas užregistruotas, sukuriama nauja grąžinimo eilutė, kurios likusio kiekio būsena yra **Numatoma**. Be to, eilutę suskaidyti galite spustelėję **Funkcijos** &gt; **Skaidyti**.

### <a name="process-the-quarantine-order"></a>Sulaikymo užsakymo apdorojimas

Jei grąžinti produktai siunčiami į sulaikymo sandėlį patikrinti, visas kitas papildomas apdorojimas užbaigiamas sulaikymo tvarka. Kiekvienai gavimo eilutei sukuriamas vienas sulaikymo užsakymas. Perkėlimo kodas nurodo patikrinimo proceso rezultatą. 

Galite suskaidyti sulaikomą užsakymą, kaip ir galite suskaidyti gavimo žurnalą Jei suskaidysite sulaikymo užsakymą, sukelsite atitinkamą grąžinimo eilutės suskaidymą. Įvedę perkėlimo kodą, užbaikite sulaikymo užsakymą naudodami funkciją **Baigti** arba funkciją **Skelbti baigtu**. Jei pasirinksite **Skelbti baigtu**, paskirtame sandėlyje bus sukurtas naujas gavimas. Šį gavimą tada galite apdoroti naudodami puslapį **Gavimo apžvalga**. 

Jei gavimas sukurtas pagal sulaikymo užsakymą, negalėsite pakeisti perdavimo kodo, kuris priskirtas patikrinimo metu. Jei sulaikymo užsakymą užbaigsite naudodami funkciją **Baigti**, partija užregistruojama automatiškai. Kartais prekė gali būti atsiunčiama atgal iš sulaikymo į Siuntimo ir gavimo skyrių. Pvz., sulaikymo inspektorius gali nežinoti, kur atsargose laikyti prekę. Tokiu atveju atitinkamą važtaraštį reikia atnaujinti, kad būtų tinkamai registruotas ir veiktų pagal perdavimo kodą, kuris nurodytas dėl sulaikymo. 

Kkrąžinimo eilutė užregistruota, klientui galima nusiųsti gavimo patvirtinimą. Ataskaita **Grąžinimo patvirtinimas** atspindi grąžinimo užsakymo dokumentą. Ataskaita **Grąžinimo patvirtinimas** nėra įtraukiama į žurnalą ar kitaip registruojama sistemoje, tai nėra būtinas grąžinimo užsakymo proceso veiksmas.

## <a name="replace-a-product"></a>Produkto keitimas
Yra du produkto keitimo valdymo mėtodai:

-   **Išankstinis pakeitimas** – produktas keičiamas dar prieš gaunant grąžinamą produktą iš kliento.
-   **Pakeitimas pagal perdavimo kodą** – automatiškai kurkite naują pakeitimo užsakymo eilutę.

### <a name="up-front-replacement"></a>Išankstinis pakeitimas

Išankstinio pakeitimo atveju, pakaitalas gali būti pristatytas klientui dar prieš grąžinant prekę. Šis metodas naudingas, jei, pvz., prekė yra automobilio detalė, kurios negalima nuimti, kol atsarginė detalė bus pasiekiama šiai pakeisti, arba, jei tiesiog norite, kad klientas pakaitalą gautų kaip įmanoma greičiau. Išankstinis pakeitimo užsakymas yra atskiras pardavimo užsakymas. Antraštės informacija inicijuojama iš kliento, o eilutės informacija inicijuojama iš grąžinimo užsakymo. Pakeitimo užsakymą galite redaguoti, apdoroti ir panaikinti atskirai nuo grąžinimo užsakymo. Panaikinę pakeitimo užsakymą, gausite pranešimą, kad užsakymas sukurtas kaip pakeitimo užsakymas. Šioje iliustracijoje parodytas išankstinio pakeitimo užsakymo procesas.  

![Išankstinio pakeitimo procesas](./media/SalesReturn04.png)

Grąžinimo užsakymas apima nuorodą į pakeitimo užsakymą. Jei išankstinio pakeitimo užsakymas sukurtas grąžinimo užsakymui prieš grąžinant prekę su defektu, negalėsite pasirinkti pakeitimo perdavimo kodų po to, kai prekė su defektu bus grąžinta.

### <a name="replacement-by-disposition-code"></a>Pakeitimas pagal perdavimo kodą

Jei klientui išsiųsite pakaitalą ir perdavimo veiksmą **Pakeisti ir nurašyti** arba **Pakeisti ir kredituoti** naudojate grąžinimo užsakyme, naudokite procesą, kuris parodytas toliau pateikiamoje iliustracijoje.  

![Pakeitimo procesas, kai naudojamas perdavimo kodas](./media/SalesReturn05.png)

Pakaitalas bus pristatytas naudojant atskirą pardavimo užsakymą – pakeitimo pardavimo užsakymą. Šis pardavimo užsakymas sukuriamas, kai sugeneruojamas grąžinimo užsakymo važtaraštis. Užsakymo antraštėje naudojama informacija iš kliento, kuris nurodytas grąžinimo užsakymo antraštėje. Eilutės informacija surenkama iš puslapyje **Prekės pakaitalas** įvestos informacijos. Turi būti užpildytos puslapio **Prekės pakaitalas** eilutės, susijusios su perdavimo veiksmais, kurios prasideda žodžiu „pakeisti“. Tačiau, nei prekės pakaitalo kiekis, nei tapatybė nėra patikrinta ar apribota. Šis veikimo būdas leidžia atvejus, kai klientas nori tos pačios prekės tik kitokia konfigūracija ar dydžiu, ir tuos atvejus, kai klientas nori visai kitokios prekės. Pagal numatytuosius nustatymus, identiška prekė įvedama puslapyje **Prekės pakaitalas**. Tačiau galite pasirinkti kitokią prekę, jei tokia funkcija yra nustatyta. 

>[Pastaba!] Sukūrus pakeitimo pardavimo užsakymą galima jį redaguoti ir panaikinti.

## <a name="generate-a-packing-slip"></a>Važtaraščio generavimas
Prieš tai, kai grąžintos prekės bus gautos į atsargas, turite atnaujinti užsakymo, kuriam tos prekės priklauso, važtaraštį. Kaip sąskaitos faktūros atnaujinimo procesas yra finansinės operacijos atnaujinimas, važtaraščio atnaujinimas yra fizinis atsargų įrašo atnaujinimas. Kitaip tariant, jo metu atliekami atsargų pakeitimai. Grąžinimo atvejais važtaraščio atnaujinimo metu atliekami tie žingsniai, kurie priskirti perdavimo veiksmui. Generuojant važtaraštį atliekami toliau nurodyti įvykiai:

-   Sandėlyje naudojant standartinį procesą atliekamas faktinis gavimas. Didžiosios knygos registravimai sugeneruojami, jei atitinkamai nustatyti atsargų modelio grupės (**Registruoti faktines atsargas**) ir gautinų sumų parametrai (**Registruoti važtaraštį DK**).
-   Prekės su pažymėtu perdavimo veiksmu, kuriame nurodytas žodis „nurašymas“, yra nurašomos, o atsargų nuostolis užregistruojamas į didžiąją knygą.
-   Prekės su pažymėtu perdavimo veiksmu **Grąžinti klientui** gaunamos ir pristatomos klientui. Šios prekės atsargoms neturi grynojo poveikio.
-   Sukuriamas pakeitimo pardavimo užsakymas. Šis pardavimo užsakymas pagrįstas informacija iš puslapio **Prekės pakaitalas**.

Galite sugeneruoti tik tų eilučių važtaraštį, kurių grąžinimo būsena yra **Registruota**, ir tik viso eilutėje nurodyto kiekio. Jei kelių grąžinimo užsakymo eilučių būsena yra **Registruota**, galite sugeneruoti tų eilučių poaibio važtaraštį, puslapyje **Registruoti važtaraštį** panaikinę kitas eilutes. 

Daliniai grąžinimai apibrėžiami pagal grąžinimo užsakymo eilutes, o ne grąžinimo užsakymo siuntas. Tai yra, jei jūs gaunate visą kiekį, nurodytą vienoje grąžinimo užsakymo eilutėje, bet negaunate nieko iš kiekio, nurodyto kitose grąžinimo užsakymo eilutėse, šis pristatymas nėra dalinis. Tačiau, jei grąžinimo užsakymo eilutėje reikia 10 vienetų, kad prekė būtų grąžinta, bet gavote tik keturis vienetus, tuomet pristatymas yra dalinis pristatymas. Jei gautos ne visos numatomos grąžinamos prekės, galite atidėti siuntą ir palaukti, kol bus gautas likęs grąžinamas kiekis. Kitu atveju, galite jas registruoti ir užregistruoti dalinį kiekį. Važtaraščio registravimo proceso metu galite važtaraščio nuorodos numerį, esantį kliento siuntimo dokumentuose, susieti su užsakymo eilutėmis. Šis susiejimas pasirinktis ir naudojamas tik kaip nuoroda. Joks operacijos atnaujinimas nesukuriamas. 

Apskritai, važtaraščio procesą galite praleisti ir eiti tiesiogiai į SF išrašymą. Tokiu atveju, tuos veiksmus, kuriuos būtumėte atlikę generuodami važtaraštį, galėsite atlikti išrašydami SF.

## <a name="generate-an-invoice"></a>Kurti SF
Puslapyje **Grąžinimo užsakymas** pateikiama informacija ir veiksmai, kurie reikalingi specialiems grąžinimo užsakymo logistikos aspektams tvarkyti, turite naudoti puslapį **Pardavimo užsakymas** SF išrašymo procesui užbaigti. Tada jūsų organizacija gali išrašyti grąžinimo užsakymų ir pardavimo užsakymų sąskaitas faktūras tuo pačiu metu, tas pats asmuo gali užbaigti šį procesą reikiamu būdu. Norėdami grąžinimo užsakymą peržiūrėti puslapyje **Pardavimo užsakymas** spustelėję pardavimo užsakymo numerio saitą atidarykite susietą pardavimo užsakymą. Grąžinimo užsakymą rasite ir puslapyje **Visi pardavimo užsakymai**. Grąžinimo užsakymai yra pardavimo užsakymai, kurių užsakymo tipas yra **Grąžintas užsakymas**.

### <a name="credit-correction"></a>Kredito koregavimas

SF išrašymo proceso metu patvirtinkite, kad papildomos išlaidos yra teisingos. Norint, kad didžiosios knygos registravimai taptų taisymais („Storno“), galbūt registruodami SF / kredito pažymą norėsite naudoti parinktį **Kredito koregavimas**, esančią skirtuke **Kita**, puslapyje **SF registravimas**. 
>[Pastaba!] Pagal numatytuosius nustatymus, parinktis **Kredito koregavimas** suaktyvinama, jei puslapyje **Gautinų sumų parametrai** įgalinta parinktis **Kredito pažyma kaip pataisymas**. Tačiau rekomenduojame neregistruoti grąžinimų su „Storno“.

## <a name="create-intercompany-return-orders"></a>Vidinės įmonės grąžinimo užsakymų kūrimas
Grąžinimo užsakymus galima užbaigti tarp dviejų vidinių jūsų organizacijos įmonių. Palaikomi toliau nurodyti scenarijai:

-   Paprasti vidinės įmonės grąžinimai tarp dviejų įmonių, dalyvaujančių vidinės įmonės ryšyje
-   Vidinės įmonės grandinė, kuri sukuriama, kai kliento grąžinimo užsakymas sukuriamas parduodančioje įmonėje
-   Vidinės įmonės grandinė, kuri sukuriama, kai tiekėjo grąžinimo užsakymas sukuriamas perkančioje įmonėje
-   Tiesioginio pristatymo siuntų grąžinimas tarp išorinio kliento ir dviejų įmonių, kurios dalyvauja vidinės įmonės ryšyje

### <a name="setup"></a>Sąranka

Toliau pateikiamoje iliustracijoje: minimalus nustatymas, kurio reikia dviems įmonėms norint dalyvauti vidinės įmonės ryšyje pasinaudoti vidinės įmonės prekyba.  

![Minimalus nustatymas](./media/SalesReturn06.png)

Toliau pateikiamame pavyzdyje „CompBuy“ yra perkanti įmonė, o „CompSell“ yra parduodanti įmonė. Paprastai parduodanti įmonė siunčia prekes arba perkančiai įmonei, arba, tiesioginio pristatymo siuntų scenarijuose, tiesiogiai galutiniam klientui. Įmonėje „CompBuy“ tiekėjas IC\_„CompSell“ nustatytas kaip vidinės įmonės galinis punktas, kuris susietas su įmone „CompSell“. Tuo pat metu, įmonėje „CompSell“ klientas IC\_„CompBuy“ nustatytas kaip vidinės įmonės galinis punktas, kuris susietas su įmone „CompBuy“. Atitinkamos veiksmų strategijos informacija ir vertės susiejimai turi būti nustatyti abiejose įmonėse. Tiesioginio pristatymo siuntų scenarijuje vidinės įmonės grąžinimo užsakymas, kuris yra ir vidinės įmonės pardavimo užsakymas, sukuriamas parduodančioje įmonėje. Vidinės įmonės grąžinimo užsakymo RMA numerį galima paimti iš RMA skaičių sekos „CompSell“, arba jį galima nukopijuoti iš RMA numerio, kuris priskirtas originaliam grąžinimo užsakymui „CompBuy“. Šiuos veiksmus nustato RMA skaičių sekos nustatymai „CompBuy“ veiksmų strategijoje **„PurchaseRequisition“**. Jei RMA numeris sinchronizuotas, turėtumėte planuoti sumažinti skaičių prieštaravimo riziką, jei šios dvi įmonės naudos tą pačią skaičių seką.

### <a name="simple-intercompany-returns"></a>Paprasti vidinės įmonės grąžinimai

Šis scenarijus apima dvi tos pačios organizacijos įmones kaip parodytatoliau pateikiamoje iliustracijoje.  

![Paprasti vidinės įmonės grąžinimai](./media/SalesReturn07.png)

Užsakymo grandinę galima sukurti, kai tiekėjo grąžinimo užsakymas sukuriamas perkančioje įmonėje arba kliento grąžinimo užsakymas atkuriamas parduodančioje įmonėje. „Finance and Operations“ sukuria atitinkamą užsakymą kitoje įmonėje ir užtikrina, kad antraštė ir eilutės informacija tiekėjo grąžinimo užsakyme atspindėtų kliento grąžinimo užsakymo parametrus. Sukurtame grąžinimo užsakyme gali būti arba nebūti nuoroda (**Rasti pardavimo užsakymą**) į esamą kliento sąskaitą faktūrą. Šių dviejų užsakymų važtaraščius ir sąskaitas galima apdoroti atskirai. Pvz., nereikia generuoti tiekėjo grąžinimo užsakymo važtaraščio prieš generuojant kliento grąžinimo užsakymo važtaraštį.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Tiesioginio pristatymo siuntų grąžinimai tarp trijų šalių

Šį scenarijų galima sukurti, jei ankstesnis **Tiesioginis pristatymas** tipo pardavimas užbaigtas, ir jei SF pagal klientą egzistuoja įmonėje, kuri sąveikauja su klientu. Toliau pateikiamoje iliustracijoje įmonė „CompBuy“ anksčiau yra klientui „Extern“ pardavusi ir išrašiusi SF produktams. Jei produktai buvo išsiųsti tiesiogiai iš įmonės „CompSell“ klientui vidinės įmonės užsakymo grandinę.  

![Tiesioginio pristatymo siuntų grąžinimai tarp trijų šalių](./media/SalesReturn08.png)

Jei klientas „Extern“ nori grąžinti produktus, klientui sukuriamas grąžinimo užsakymas (RMA02) įmonėje „CompBuy“. norint sukurti vidinės įmonės grandinę, grąžinimo užsakymas turi būti pažymėtas tiesioginiam pristatymui. Kai naudojate **Rasti pardavimo užsakymą** funkciją norėdami paimti kliento SF grąžinti, sukuriama vidinės įmonės užsakymo grandinė, sudaryta iš šio dokumento:

-   **Originalus grąžinimo užsakymas:** RMA02 (įmonė „CompBuy)“
-   **Pirkimo užsakymas:** PO02 (įmonė „CompBuy“)
-   **Originalus grąžinimo užsakymas:** RMA\_00032 (įmonė „CompSell“)

Po to, kai sukurta tiesioginio pristatymo vidinės įmonės grandinė, visas faktinis grąžinimų tvarkymas ir apdorojimas turi vykti vidinės įmonės grąžinimo užsakymo kontekste, RMA\_00032 įmonėje „CompSell“. Produktų negali gauti įmonė „CompBuy“. Kai perdavimo kodas priskiriamas vidinės įmonės grąžinimo užsakymui, jis sinchronizuojamas su originaliu grąžinimo užsakymu, kad būtų leidžiama tinkamai išrašyti originalaus užsakymo SF.

## <a name="post-to-the-ledger"></a>Registruoti didžiojoje knygoje
Didžiosios knygos registravimams, kurie sugeneruojami, kai išrašoma grąžinimo užsakymo SF, įtakos turi keli svarbūs nustatymai ir parametrai:

-   **Grąžinimo savikaina** – atsargų modeliams ne parametras **Standartinė savikaina**, o **Grąžinimo savikaina** nustato prekės savikainą, kai ji priimama atgal į atsargas arba nurašoma. Norint tinkamai apskaičiuoti atsargų vertinimą, svarbu tinkamai nustatyti parametrą **Grąžinimo savikaina**. Jei naudojate funkciją **Rasti pardavimo užsakymą** grąžinimo užsakymo eilutei, turinčiai nuorodą į kliento sąskaitą faktūrą, sukurti, vertė **Grąžinimo savikaina** yra lygi parduotos prekės savikainai. Kitu atveju, savikainos vertė gaunama iš prekės nustatymo arba gali būti įvesta rankiniu būdu.
-   **Kredito koregavimas / „Storno“** – parametras **Kredito koregavimas** puslapyje **SF registravimas** nustato, ar registravimai turi būti įrašyti kaip teigiami (DR / CR) įrašai ar kaip koregavimo, neigiami įrašai.

Tolesniuose pavyzdžiuose grąžinimo savikaina pateikiama kaip **Atsargų savikaina**.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>1 pavyzdys: grąžinimo užsakymas nenurodo į kliento sąskaitą faktūrą

Grąžinimo užsakymas nenurodo į kliento sąskaitą faktūrą. Grąžinta prekė kredituojama. Generuojant grąžinimo užsakymo sąskaitą faktūrą arba kredito pažymą, nepasirinktas parametras **Kredito koregavimas**.  

![Grąžinimo užsakymas nenurodo į kliento sąskaitą faktūrą](./media/SalesReturn09.png)  

>[Pastaba!] Pagrindinė prekės kaina naudojama kaip numatytoji parametro **Grąžinimo savikaina** vertė. Numatytoji kaina skiriasi nuo savikainos atsargų išdavimo metu. Todėl implikuojama, kad patirtas nuostolis yra 3. Be to, grąžinimo užsakymas neapima nuolaidos, kuri buvo suteikta klientui pardavimo užsakyme. Todėl susidaro kredito perviršis.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>2 pavyzdys: grąžinimo užsakymui pasirinktas kredito koregavimas

2 pavyzdys yra tas pat 1 pavyzdys, bet parametras **Kredito koregavimas** pasirenkamas, kai sugeneruota grąžinimo užsakymo sąskaita faktūra.  

![Grąžinimo užsakymas, kai pasirinktas kredito koregavimas ](./media/SalesReturn10.png)  

>[Pastaba!] Didžiosios knygos registravimai įvesti kaip neigiami pataisymai.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>3 pavyzdys: grąžinimo užsakymo eilutė sukurta naudojant funkciją Rasti pardavimo užsakymą

Šiame pavyzdyje grąžinimo užsakymo eilutė sukurta naudojant funkciją **Rasti pardavimo užsakymą**. Kuriant sąskaitą faktūrą, nepasirinktas parametras **Kredito koregavimas**.  

![Grąžinimo užsakymo eilutė, kuri sukurta naudojant funkciją Rasti pardavimo užsakymą ](./media/SalesReturn11.png)  

>[Pastaba!] **Nuolaida** ir **Grąžinimo savikaina** nustatytos tinkamai. Todėl įvyksta kliento sąskaitos faktūros tikslus atšaukimas.



