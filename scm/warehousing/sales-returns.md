---
title: "Pardavimo grąžinimai"
description: "Šioje temoje pateikta informacija apie grąžinimo užsakymų procesą. Tai apima informaciją apie pirkėjo deklaracijas bei jų poveikį įkainojimo ir turimų atsargų kiekius."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3d02a15387231160f5b8a237aa11008b91ef1223
ms.openlocfilehash: b265a20a271230de5dba6df93900a24aad642885
ms.lasthandoff: 03/31/2017


---

# <a name="sales-returns"></a>Pardavimo grąžinimai

Šioje temoje pateikta informacija apie grąžinimo užsakymų procesą. Tai apima informaciją apie pirkėjo deklaracijas bei jų poveikį įkainojimo ir turimų atsargų kiekius.

Klientai gali grąžinti prekes dėl įvairių priežasčių. Pvz., prekės gali būti su defektais, arba ji neatitinka kliento lūkesčių. Grąžinimo procesas prasideda, kai klientui išduoda prašymo dėl prekių grąžinimo. Po kliento prašymo gavimo, grąžinimo užsakymas sukurtas Microsoft Dynamics 365 operacijoms.

## <a name="return-order-process"></a>Grąžinimo užsakymo procesas
Šioje iliustracijoje apžvelgiami grąžinimo užsakymo procesas.  

[![salesreturns01](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

Yra dviejų tipų grąžinimo užsakymo procesą: fizinės grįžti ir kredito tik.

-   **Fizinis grąžinimas** – įsakymo grąžinti vaiką leidžia fizinis produktų grąžinimas.
-   **Kredito tik** – įsakymo grąžinti vaiką leidžia klientui kreditą, bet nereikalauja, kad vartotojas fiziškai Gr±¾inkite gaminius.

### <a name="physical-return-order-process"></a>Fizinės grąžinimo užsakymo procesas

1.  **Grąžinimo užsakymo kūrimas.** Oficialiai dokumento leidimas klientui grąžinti jokių defektų ar nepageidaujamas produktų. Įsakymo grąžinti vaiką nereikalauja, kad įmonė priimti atgal grąžinta prekę ar suteikti kreditą klientui. Jei grąžinimas yra priimtinas, jūs galite leisti keičiamai prekei siunčiami prieš defektų turinčios prekės buvo grąžintos.
2.  **Atvykti į sandėlį patikrinimui.** Užbaigti pradinio patikrinimo ir patvirtinimo prieš dokumento grąžinimo užsakymas. Įsakymo grąžinti vaiką taip pat palaiko grąžinamas prekes, karantinas dėl papildomos inspekcijos ir kokybės kontrolės.
3.  **Nustato disponavimo.** Baigti per patikrinimą, ir nuspręsti, kas turėtų būti daroma su grąžinta prekė. Vykdant šį veiksmą, nuspręsti, ar jums bus kredito klientas, atmesti prekių grąžinimas, ar priimti prekių grąžinimas, laužas produktas, o tada siųsti pakaitinį produktą klientui.
4.  **Kurti važtaraštį.** Kurti važtaraštį, ir įsipareigoti likvidavimo sprendimą, kad pasirinkote atlikdami 3 veiksmą. Užbaikite logistikos procesus.
5.  **Sukurti sąskaitą-faktūrą.** Uždarykite įsakymo grąžinti vaiką.

### <a name="credit-only-process"></a>Kredito tik proceso

1.  **Grąžinimo užsakymo kūrimas.** Oficialiai dokumento leidimo naudoti klientui gauti kreditą be Grą indami gaminius su trūkumais arba nepageidautina. Ir **kredito tik** perdavimo kodo įgalioja sprendimą turi kredito klientas be fizinės grąža.
2.  **Sukurti sąskaitą-faktūrą.** Kurti kredito pažymą, ir tada uždarykite įsakymo grąžinti vaiką.

## <a name="return-material-authorization"></a>Medžiagų leidimo grįžti
Grąžinimo medžiagų autorizavimo (RMA) perdirbimo remiasi pardavimo užsakymo funkcija. RMA yra registruotas kaip grąžinimo tvarka, kuri yra sukurta kaip pardavimo užsakymą, ir gali turėti kitas pardavimo užsakymo, susijusią su ja, vadinama keitimo užsakymą. Abu pardavimo užsakymų susieti su kilmės RMA numerį.

-   **Grąžinimo užsakymui** – užsiregistruoti dėl RMA, galite sukurti grąžinimo užsakymas, kuris yra pardavimo užsakymą, kuriame turi priskirtą tipą, **grąžinti užsakymą.** Visi pakeitimai, kuriuos atliekate RMA informacija automatiškai atnaujinama pardavimo užsakymo. Kol grąžinimo užsakymas, kurio būsena yra reikalingas **atviras**, jis nebus rodomas pardavimo užsakymų, sąrašas. Naudojate RMA elgtis atvykimo ir grąžintų prekių gavimą, taip pat leisti kredito tik likvidavimo veiksmų (žr. skyrių **disponavimo kodus ir disponavimo veiksmai**). Visus kitus tolesnius procesus turi būti tvarkomos pagal pardavimo užsakymą.
-   **Pakeitimo užsakymo** -kai pakeitimo tvarka turi būti vežamos į klientas, RMA numerį galima įtraukti antrojo susijusios pardavimo užsakymo. Galite rankiniu būdu sukurti pakeitimo įsakymo RMA nedelsiant siuntą. Kita vertus, dėl pakeitimo užsakymo gali būti automatiškai kuriamos po atvykimo, tikrinimo ir priėmimo būtų užpildyti RMA eilutės elemento, kuris turi disponavimo kodą, nurodantį pakeitimo. Keitimo užsakymą turi tas pačias funkcijas, kuris yra susietas su pardavimo užsakymą. Pavyzdžiui, galite naudoti jį sukonfigūruoti pasirinktinius produktą kaip keičiamai prekei, kurti gamybos užsakymą remonto grąžintų prekių, sukurti tiesioginio pristatymo pirkimo užsakymą siųsti pakeitimo iš tiekėjo ar remti kitais tikslais.

## <a name="create-a-return-order"></a>Grąžinimo užsakymo kūrimas
Grąžinimo užsakymo procesas prasideda, kai klientas susisiekia su jūsų organizacijos grįžti su defektais ar nepageidaujamo produkto ir (arba) pervesti. Po to, kai jūsų organizacija sutinka grąžinti, grąžinti parduotame grąžinimo užsakymas. Šis grąžinimo užsakymas tampa grąžintos prekės vidaus gamybos centru. Toliau pateiktame paveikslėlyje pavaizduotas sukurti per nustatytą tvarką.  

[![Tvarkos, kuriant grąžinimo užsakymas](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>Kurti antraštę įsakymo grąžinti vaiką

Kai grąžinimo užsakymas, toliau lentelėje pateikiama informacija turi būti pateikiama.

| Laukas              | aprašymas                                              | Komentarai                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kliento kodas   | Nuoroda į lentelę Klientai                       | Turite pateikti esamą kliento paskyrą.                                                                                                                                                                                                                                                                                                  |
| Pristatymo adresas   | Adresas, kad prekės būtų grąžintas                 | Pagal numatytuosius parametrus, organizacijos adresas yra naudojamas. Pasirinkus konkretų sandėlį antraštę, pristatymo adresas pakeičiamas į pristatymo adresą sandėlyje. Galite pakeisti šį adresą į **grąžinimo užsakymo duomenys** puslapis.                                                                                                  |
| Vieta/sandėlis     | Svetainės ar sandėlį, gauna grąžintas produktas | Grąžinimo užsakymo pristatymo adresas yra nustatomas pagal pristatymo adresą svetainės ar sandėlio.                                                                                                                                                                                                                                 |
| RMA numeris         | ID, priskirtas grąžinimo užsakymas              | RMA numeris yra naudojamas kaip alternatyvus raktas per visą grąžinimo užsakymo procesą. RMA numerį, kuris yra paskirtas remiantis RMA numeraciją, kuri nustatyta ant to **sudaro gautinų sumų parametrai** puslapis.                                                                                                                              |
| Galutinis terminas           | Elementas gali būti grąžintas datą               | Numatytoji reikšmė apskaičiuojama kaip dabartinę datą ir galiojimo laikotarpį. Pavyzdžiui, jei grįžti galioja tik 90 dienų nuo dienos, kai grąžinimo užsakymas yra sukurta, ir grąžinimo užsakymu buvo sukurtas gegužės 1 d., vertė lauke yra **30-liepos**. Galiojimo laikotarpis yra nustatytas į **sudaro gautinų sumų parametrai** puslapis. |
| Grąžinimo priežasties kodas | Kliento priežastis, dėl gaminio grąžinimu          | Priežasties kodas pasirenkamas vartotojo apibrėžiamų priežasties kodų sąrašas. Šiame lauke galite atnaujinti bet kuriuo metu.                                                                                                                                                                                                                                    |

### <a name="create-return-order-lines"></a>Grąžinimo užsakymų eilučių kūrimas

Baigus grąžinimo antraštę, galite sukurti grąžinamąjį vamzdyną iš naujo naudodami vieną iš šių metodų:

-   Rankiniu būdu įvesti prekės detales, kiekiu ir kita informacija už kiekvieną grįžimo linijos.
-   Sukurti grąžinimo eilutę naudodami, **rasti pardavimo užsakymo** funkcija. Mes rekomenduojame šią funkciją kuriant grąžinimo užsakymas. Į **rasti pardavimo užsakymo** funkcija nustato nuo grįžimo linijos nuoroda į išrašyta SF pardavimo užsakymo eilutės, ir perrašo eilutės informacija pvz., prekės numeris, kiekis, kaina, nuolaida ir savikainas iš pardavimų eilutės. Nuoroda padeda užtikrinti, kad, kai produktas yra grąžinamas bendrovei, ji paklusdavo paties vieneto kaina kad ji buvo parduota. Nuoroda taip pat patvirtina kad grąžinimo užsakymai nekuriami kiekis, kuris viršija kiekį, kuris buvo parduotas sąskaitoje-faktūroje.

**Pastaba:** grąžinamąjį vamzdyną, kurie turi nuorodą į pardavimo užsakymą elgtis kaip pataisymus arba atstatymas ir pardavimas. Norėdami gauti daugiau informacijos, peržiūrėkite skyrelį "DK įrašas", šioje temoje.

### <a name="charges"></a>Išlaidos

Mokesčius ir rinkliavas, galima paminėti į grąžinimo užsakymą per vieną ar daugiau iš toliau nurodytų būdų:

-   Galite rankiniu būdu pridėti mokesčių grąžinimo užsakymo antraštėje, grąžinimo užsakymo eilutę arba abu.
-   Mokesčius galima automatiškai įtraukti į grąžinimo užsakymo antraštėje, priklausomai nuo grąžinimo priežasties kodas.
-   Mokesčiai automatiškai įtraukiami į grąžinimo užsakymų linija, remiantis perdavimo kodo eilutės.

Mokesčiai automatiškai įtraukiami po grąžinimo priežasties kodą arba perdavimo kodo priskiriamas prie linijos. Jei priežasties kodas pakeistas vėliau, esamą įkrovos įrašą, nebus pašalinti, o naujas mokestis įrašas gali būti pridėtas, remiantis nauja priežasties kodas. Jei norite pridėti mokesčių grąžinimo užsakymų eilučių, mokesčių, kurie apskaičiuojami procentais eilutę ar užsakymo vertės tampa neigiamas, kai linija arba linijos užsakymas yra neigiamas, nebent procentinis dydis taip pat yra neigiamas skaičius. Mokestis, kuris turi neigiamą vertę sudaro kredito klientui.

### <a name="return-reason-codes"></a>Grąžinimo priežasčių kodai

Taikant grąžinimo priežasties kodus, galite padėti lengviau analizuoti grąžinimo modelius. Priežasčių kodus suteikti informacijos apie Kodėl pirkėjas nori grąžinti prekes. Kai kurios organizacijos turi daug priežasčių kodus. Šios organizacijos gali grupės priežasčių kodus į priežasties kodas grupes, geriau peržvelgti ir sukauptą ataskaitų.

### <a name="disposition-codes-and-disposition-actions"></a>Disponavimo kodus ir disponavimo veiksmai

Svarbus žingsnis grąžinimo užsakymo procesas yra perdavimo kodo grąžinimo užsakymo eilutę priskyrimo atvykimo registravimo dalis. Disponavimo kodas nurodo šią informaciją:

-   **Finansinis poveikis** -turėtų būti įskaitytos į klientų už grąžintas prekes, ir bet kokius mokesčius galima pridurti prie grąžinimo užsakymo eilutės?
-   **Grąžinama prekė iš** -prekės gali būti pridedami prie atsargų, turėtų būti sunaikintas, ar jis turėtų būti grąžintas į kliento?
-   **Grąžintų prekių logistika** – keičiamai prekei išduodamos klientui?

Ne tik nustatyti, kaip grąžintos prekės yra realizuojami, disponavimo kodai gali sukelti mokesčiai taikytinas grįžimo linijos. Taip pat jais galima grupuoti grąžina statistinei analizei. Disponavimo kodai apibrėžiami kaip grąžinimo užsakymus sąrankos dalis. Tačiau kiekvieno perdavimo kodo turi nurodyti vieną iš įtaisytųjų likvidavimo veiksmų. Žemiau pateiktoje lentelėje integruotas disponavimo kodus ir jų veiksmus. **Svarbu:** jei prekę grąžinti nereikia, bet vis dar turėtų būti įskaitytos į klientų, priskirti prie **kredito tik** perdavimo kodo į grįžimo linijos.

<table>
<thead>
<tr class="header">
<th>Perdavimo kodas</th>
<th>Įgyvendinimo poveikis finansams</th>
<th>Logistikos poveikis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tik kreditas</td>
<td><ul>
<li>Klientas yra kredituojamas pardavimo kaina atėmus visus mokesčių ar privalomųjų mokėjimų.</li>
<li>Nuostolis iš pašalinti iš apyvartos prekės registruojamos DK.</li>
</ul></td>
<td>Prekę grąžinti nereikia. Šis polinkis veiksmų vartojamas šiais atvejais:
<ul>
<li>Nėra pakankamai pasitikėjimo tarp šalių.</li>
<li>Defektų turinčios prekės grąžinimo išlaidos yra pernelyg didelės.</li>
<li>Elementus negalima leisti atgal į inventorių. Dėl kitų sąlygų, fizinės grąža nėra būtina.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kreditas</td>
<td><ul>
<li>Klientas yra kredituojamas pardavimo kaina atėmus visus mokesčių ar privalomųjų mokėjimų.</li>
<li>Atsargų vertė didinama už grąžintas prekes.</li>
</ul></td>
<td>Prekė grąžinama ir dedama atgal į inventorių.</td>
</tr>
<tr class="odd">
<td>Keitimas ir kreditas</td>
<td><ul>
<li>Klientas yra kredituojamas pardavimo kaina atėmus visus mokesčių ar privalomųjų mokėjimų.</li>
<li>Atsargų vertė didinama už grąžintas prekes.</li>
<li>Atskira pardavimo užsakymą už keitimą yra sukurtas ir tvarkomas atskirai.</li>
</ul></td>
<td>Prekė grąžinama ir dedama atgal į inventorių.</td>
</tr>
<tr class="even">
<td>Keitimas ir nurašymas</td>
<td><ul>
<li>Kredituojama pirkėjo pardavimo kainai, atėmus bet kokį mokesčių ar rinkliavų.</li>
<li>Nuostolis iš pašalinti iš apyvartos prekės registruojamos DK.</li>
<li>Atskira pardavimo užsakymą už keitimą yra sukurtas ir tvarkomas atskirai.</li>
</ul></td>
<td>Prekės yra grąžinama ir nurašytas į atliekas.</td>
</tr>
<tr class="odd">
<td>Grąžinti klientui</td>
<td>Niekas, išskyrus bet kokį mokesčių ar rinkliavų.</td>
<td>Prekė grąžinama bet siunčiamas atgal į kliento po patikrinimo. Šis polinkis veiksmų gali būti naudojami, jei prekė buvo sąmoningai sugadinta arba jei buvo anuliuotas garantija.</td>
</tr>
<tr class="even">
<td>Nurašyta</td>
<td><ul>
<li>Klientas yra kredituojamas pardavimo kaina atėmus visus mokesčių ar privalomųjų mokėjimų.</li>
<li>Nuostolis iš pašalinti iš apyvartos prekės registruojamos DK.</li>
</ul></td>
<td>Prekės grąžintos arba į metalo laužą.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>Atvežimo į sandėlį patikrinimui
Kad galėtumėte fiziškai gauti grąžintas prekes į atsargas registruojant važtaraštį, elementus turi pereiti per atvykimo registracijos bei bagažo skyriaus patikrinimas neprivalomas. Šioje iliustracijoje apžvelgiami atvykimo procesą. Kad ir aprašyti kiekvieną žingsnį, kuris yra pavaizduota paveiksle.  

[![Atvykimo procesą](./media/salesreturn03.png)](./media/salesreturn03.png)  

Šį procesą sudaro keletas kitų sąlygų keitimų, kurie nėra įtraukti į šią temą. Štai keletas iš šių variantų:

-   Nenaudokite su **gavimų apžvalga** sΰraπas sukurti atvykimo leidinyje. Vietoj to, rankiniu būdu sukurti atvykimo žurnalą. Grąžinti užsakymų turės **pardavimų užsakymų** į priekį.
-   Jei naudojate sandėlio valdymą, generuoja padėklų transportą. Grąžinimo linija turės būsena **Arrived** padėklų transportavimo metu.
-   Registruotis atvykstant grąžintas prekes tiesiai iš grąžinimo užsakymų eilutės, naudojant į **registracijos** funkcija.

Atvykimo metu, grąža yra integruoti į bendrojo proceso sandėlio atvykusiems. Atvykimo procesą taip pat palaiko sulaikymo užsakymus už grąžinamas prekes, kad turi būti atliktas atskiras kontrolės sukūrimas.

### <a name="identify-products-in-the-arrival-overview-list"></a>Nustatyti produktų sąraše atvykimo apžvalga

Į **gavimų apžvalga** puslapis išvardyti visų planuojamų gaunamus atvykusiųjų. **Pastaba:** prekyboje nuo grąžinimo užsakymai turi būti tvarkomi atskirai nuo kitų rūšių atvykimo operacijas. Po to, kai jau nustatėte gaunamo paketo į **gavimų apžvalga** puslapyje (pvz., naudojant RMA lydraštis), į veiksmų sritį, spustelėkite **pradėti atvykimo** sukurti ir inicijuoti gavimo žurnalą, kuris atitinka atvykimo.

### <a name="edit-the-arrival-journal"></a>Redaguoti atvykimo žurnalą

Nustatydami, **karantino valdymo** į **taip**, galite sukurti sulaikymo užsakymas, grąžinimo linijos. Jei linija buvo išsiųstas į karantino inspekcijos, jūs negalite nurodyti perdavimo kodo. **Pastaba:** jei nustatysite į **karantino valdymo** į **taip** – prekės atsargų modelių grupę, į **karantino valdymo** parinktį į **žurnalo eilutes** puslapis bus pažymėtas kaip žurnalo eilutėje ir negali būti pakeistas. Jei eilutė yra siunčiama karantino, nurodykite tinkamą sulaikymo sandėlį. Jei atvykimo linija nėra siunčiami patikrinimui, sandėlio atvykimo sekretorius turi nurodyti perdavimo kodo tiesiai ant žurnalo eilutėje, po to atvykimo žurnalą. Jei tą patį disponavimo kodą būti paskirtas visam kiekiui, grįžimo linijos, arba visas kiekis linijos negavo, jūs suskaidote linija. Kai išskaidote atvykimo žurnalo eilutę, jūs taip pat padalinti grįžimo linijos (**SalesLine**) ir sukurti naują partijos ID. Galite perskirti linija iš žurnalo eilutėje kiekio sumažinimo. Kai žurnalas užregistruojamas, naują grąžinimo linijos atsiras, kurio būsena **numatoma**, likęs kiekis. Taip pat galite padalinti į eilutę spustelėdami **funkcijos**&gt;**Split**.

### <a name="process-the-quarantine-order"></a>Sulaikyto užsakymo procesas

Jei grąžinta prekė yra siunčiama patikrinimui sulaikymo sandėlyje, bet koks papildomas tvarkymas bus baigtas sulaikymo užsakymas. Vienas sukurtas kiekvienai atvykimo eilutei, kuri yra siunčiama karantino. Disponavimo kodas nurodo patikrinimo proceso rezultatas. Galite perskirti sulaikymo užsakymas, lygiai taip pat jūs galite padalinti atvykimo žurnalą. Jeigu jūs suskaidote sulaikymo užsakymą, jūs sukelti atitinkamas split grįžimo linijos. Įvedę perdavimo kodo, baigti sulaikymo užsakymą naudodami, **galo** funkcija arba **paskelbtos baigtomis** funkcija. Jei pasirinksite **paskelbti baigtu**, naujokė yra sukurta paskirtoji sandėlyje. Tada galite apdoroti šio atvykimo naudojant į **gavimų apžvalga** puslapis. Jei atvykimo yra kilęs iš sulaikymo užsakymas, disponavimo kodą, kuris yra priskirtas patikrinimo metu keisti negalima. Jei žaidžiate sulaikymo užsakymą naudodami, **pabaigos** funkcija, kad daug bus automatiškai įregistruotas. Kartais prekė gali būti siunčiama atgal iš karantino siuntimo ir gavimo skyrius. Pvz., sulaikymo inspektoriui galite nežinoti kur saugoti prekę atsargose. Tokiu atveju atitinkamas važtaraštis turi būti atnaujinta teisingai užsiregistruoti ir dėl disponavimo kodą, kuris nurodomas dėl karantino. Gavimo patvirtinimą galima siųsti klientui užregistruojant grąžinimo linijos. Į **grąžinimo patvirtinimo** ataskaita panaši į nustatytą dokumentą. Į **grąžinimo patvirtinimo** ataskaita nėra įtrauktas į žurnalą ar kitaip užregistruoti sistemoje, ir tai nėra būtinas žingsnis grąžinimo užsakymo procese.

## <a name="replace-a-product"></a>Pakeisti produkto
Valdymo produktų pakeitimas dviem būdais:

-   **Išankstinis pakeitimas** – pakeisti produktą prieš grąžintas produktas yra gautas iš pirkėjo.
-   **Perdavimo kodo gali pakeisti** -automatiškai sukurti naują pakeitimo užsakymo eilutę.

### <a name="up-front-replacement"></a>Išankstinis pakeitimas

– Išankstinis pakeitimas, keičiamai prekei gali būti pristatomi klientui, kol elementas bus grąžintas. Šis metodas yra naudingas, jei, pvz., elementas yra mašinos dalis, kuri negali būti pašalinta, nebent atsarginėmis dalimis užimti savo vietą, arba jei jūs tiesiog norite klientui galimybę turėti pakaitos produktas kuo greičiau. Išankstinis pakeitimas tvarka yra nepriklausomi pardavimo tvarka. Antraštės informacija yra inicijuota iš kliento, ir eilutės informacija yra rengiami nuo įsakymo grąžinti vaiką. Galite redaguoti, tvarkyti ir naikinti pakeitimo tvarka, neatsižvelgiant į įsakymo grąžinti vaiką. Panaikinus keitimo užsakymą, galite gauti pranešimą, kad tokia tvarka buvo sukurta kaip keitimo užsakymą. Toliau pateiktame paveikslėlyje pavaizduotas procesas išankstinis pakeitimas.  

[![Išankstinis pakeitimas procesas](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)  

Grąžinimo užsakymas yra nuoroda į keitimo užsakymą. Jei užsakymą išankstinis pakeitimas yra sukurta per nustatytą prieš defektų turinčios prekės yra grąžinama, negalite pasirinkti disponavimo kodų pakeitimas po to, kai buvo grąžintas defektų turinčios prekės.

### <a name="replacement-by-disposition-code"></a>Perdavimo kodo pakeitimas

Jei pristatote keičiamai prekei klientui, ir naudoti su **pakeisti ir laužo** ar **pakeisti ir kredito** likvidavimo veiksmų dėl įsakymo grąžinti vaiką, naudokite procesą, parodyta šioje iliustracijoje.  

[![Kai naudojamas perdavimo kodo keitimo procedūra](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)  

Keičiamai prekei bus pristatyti naudojant nepriklausomi pardavimo užsakymo, keitimo pardavimų užsakymo. Šiam pardavimo užsakymui yra sukurtas, kai sukuriamas grąžinimo užsakymo važtaraštį. Užsakymo antraštėje naudoja informaciją iš kliento, kuris nurodomas grąžinimo užsakymo antraštėje. Eilutės informacija renkama informacija, įvedama į **pakaitalas** puslapis. Į **pakaitalas** puslapis turi būti nurodytas linijas, disponavimo veiksmai, kurie prasidės žodžiu "pakeisti." Vis dėlto nei kiekio, nei keičiamai prekei tapatybė yra patvirtinti arba apribojamas. Šią problemą leidžia tais atvejais, kai klientas nori tą pačią prekę, bet ir kitą konfigūraciją ar dydis, o taip pat atvejus kai klientai nori visiškai kitą elementą. Pagal numatytuosius nustatymus tapačios prekės būtų įrašytas į **pakaitalas** puslapis. Tačiau, galite pasirinkti kitą elementą, sąlyga, kad būtų nustatyta funkcija. **Pastaba:** galite redaguoti ir panaikinti keitimo pardavimų užsakymo, kai yra sukuriama.

## <a name="generate-a-packing-slip"></a>Kurti važtaraštį
Prieš grąžinamas prekes gausite į inventorių, turite atnaujinti tvarką, pagal kurią prekės priklauso važtaraštį. Kaip SF atnaujinimo procesas yra atnaujinti finansinės operacijos, pakavimo važtaraščio atnaujinimo procesas yra fizinių atsargų įrašo atnaujinimo. Kitaip tariant, šį procesą padaro pakeitimus į atsargas. Tais atvejais, kai grąžinimas, disponavimo veiksmus priskirtus veiksmus būtų įgyvendintos per pakavimo savikainomis. Kai kuriate važtaraštį, atsiranda šie įvykiai:

-   Sandėlyje, standartinė procesas yra naudojamas atlikti faktinio gavimo. DK registravimus sugeneruojami, jei atsargų modelio grupės (**registruoti faktines atsargas**) ir esantį Accounts receivable parameters (**pagal važtaraštį DK. Post**) yra nustatyti tinkamai.
-   Prekės pažymėtos su likvidavimo veiksmų, kuriame yra žodis "scrap" nurašomos, o atsargų nuostolis registruojamas į DK.
-   Elementus, kurie buvo pažymėti su į **grąžinimas klientui** likvidavimo veiksmų gaunamos ir pristatomos klientui. Šie elementai turi įtakos atsargų.
-   Keitimo pardavimų užsakymo yra sukurta. Šiam pardavimo užsakymui remiasi informacija apie su **pakaitalas** puslapis.

Jūs galite kurti važtaraštį tik eilutes, kurių grąžinimo būsena **registruotu**, ir tik visą kiekį grąžinimo linijoje. Jei keli grąžinimo užsakymo eilutes su **registruotu** būsenos, galite generuoti važtaraščio eilutes poaibį panaikindami eilutes iš į **paštu pagal važtaraštį** puslapis. Dalinio grąžinimo yra apibrλώtos grąžinimo užsakymo eilutes, ne pagal grąžinimo užsakymo siuntimus. Todėl, jei gaunate visas kiekis, nurodytos grąžinimo užsakymo eilutėje, bet gaunate nieko iš kitos eilutės grąžinimo užsakymas, pristatymas ne dalinį pristatymą. Tačiau, jei grąžinimo užsakymų linija reikalauja grąžinti 10 prekės vienetų, bet gaunate tik keturi vienetai, pristatymas yra dalinis pristatymas. Jei ne visi numatomą grąžintų prekių atgabenimo, galite anuliuoti siuntą ir laukti, kol grąžintas kiekis atvykti poilsio. Taip pat galite registruotis ir registruoti dalinį kiekį. Važtaraščių registravimo proceso dalis, pakuotės lapelis nuorodos numeris iš kliento siuntimo dokumentuose galite susieti su užsakymo eilutes. Ši asociacija yra neprivaloma ir tik nuorodai. Jis neturi sukurti sandorio naujinimų. Apskritai, galite praleisti pakavimo slydimo procesą ir pereiti tiesiai į SF. Šiuo atveju, žingsnių, kad jums būtų atlikti per pakavimo slydimo kartos atliekamos per SF išrašymas.

## <a name="generate-an-invoice"></a>Kurti SF
Nors į **grąžinimo užsakymui** puslapyje yra informacija ir veiksmai, kurių reikia norint tvarkyti ypatingus logistikos aspektus, grąžinimo užsakymas, turite naudoti su **pardavimų užsakymų** puslapyje, kad baigti SF išrašymo procesą. Jūsų organizacija gali tada SF grąžinimo ir pardavimo užsakymuose vienu metu, ir tas pats asmuo gali atlikti sąskaitų faktūrų išrašymo procesą, kaip to reikalauja. Norėdami peržiūrėti grąžinimo užsakymą iš to **pardavimų užsakymų** spustelėkite nuorodą, Norėdami atidaryti susijusią pardavimo užsakymo pardavimo užsakymo numerį. Jūs taip pat galite rasti įsakymo grąžinti vaiką į **visus pardavimo užsakymus** puslapis. Grąžinimo užsakymai pardavimo užsakymų, kurių užsakymo tipą, **grąžintas užsakymas**.

### <a name="credit-correction"></a>Kredito koregavimas

Sąskaitų faktūrų išrašymo proceso dalis, patikrinkite, ar teisingi jokių papildomų išlaidų. Sukelti DK registravimų tapti pataisos (Storno), apsvarstykite galimybę naudoti į **kredito koregavimas** parinktį į **kiti** skirtuke, **registruojant SF** puslapio, kai registruojate SF/kredito pažymos. **Pastaba:** pagal numatytuosius nustatymus į **kredito koregavimas** parinktis įjungta, jei į **kredito pažymą kaip korekcija** parinktį su **sudaro gautinų sumų parametrai** puslapis buvo įgalintas. Tačiau mes rekomenduojame, kad jūs ne rašyti grįžta su Storno.

## <a name="create-intercompany-return-orders"></a>Kurti vidinės įmonės užsakymus, grąžinimo
Grąžinimo užsakymai gali būti baigtas dviejų bendrovių jūsų organizacijoje. Palaikomi šie scenarijai:

-   Paprastos vidinės įmonės grąžina tarp dviejų įmonių, kurios dalyvauja tarpusavio ryšys
-   Vidinės įmonės grandinėje, kuri yra nustatyta, kada parduodanti įmonė sukurta per pirkėjo nustatytą
-   Vidinės įmonės grandinėje, kuri yra nustatyta, kada tiekėjo grąžinimo užsakymas sukurtas įmonei
-   Tiesiogiai pristatyti siuntą grąžina tarp užsienio klientus ir dviejų bendrovių, kurios dalyvauja tarpusavio ryšys

### <a name="setup"></a>Sąranka

Šioje iliustracijoje minimalų nustatymą, reikalingas dviem bendrovėms dalyvauti tarpusavio ryšį ir pasinaudoti, naudojamas vidinės įmonės prekyboje.  

[![Minimum setup](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)  

Tokią situaciją, CompBuy yra perkančioji bendrovė, ir CompSell yra pardavimo įmonė. Paprastai, parduodanti įmonė pristatoma prekes įmonei arba, tiesiogiai pristatyti siuntą scenarijuose, galų gale užsakovui. – CompBuy, tiekėjo IC\_CompSell yra apibrėžiamas kaip vidinės įmonės galinio punkto, kuris yra susietas su kompanija CompSell. Be to, į CompSell, klientas IC\_CompBuy yra apibrėžiamas kaip vidinės įmonės galinio punkto, kuris yra susietas su kompanija CompBuy. Abi bendrovės turi būti apibrėžta atitinkamų veiksmų strategijos detales ir verčių atvaizdžiai. Tiesiogiai pristatyti siuntą scenarijų, vidinės įmonės grąžinimo užsakymas, kuris taip pat yra vidinės įmonės pardavimo užsakymą, sukuriamas pardavimo įmonė. Vidinės įmonės grąžinimo užsakymo RMA numeris gali būti įlaipinami RMA numeracijos, CompSell, arba kad gali būti nukopijuota nuo RMA numeris, priskirtas grąžinimo užsakyme, CompBuy. RMA numeris parametrus, **PurchaseRequisition** politikos veiksmų CompBuy nustatyti šių veiksmų. Jei sinchronizuojama RMA numerį, turite suplanuoti mažinti riziką skaičių susidūrimai, jei dvi įmonės naudoja ta pati numeracija.

### <a name="simple-intercompany-returns"></a>Paprastos vidinės grąžos

Šis scenarijus apima dvi bendrovės tos pačios organizacijos, kaip parodyta šioje iliustracijoje.  

[![Paprastos vidinės grąžos](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)  

Užsakymo grandinė gali būti nustatytas, kai tiekėjo grąžinimo užsakymas, įmonei arba per pirkėjo nustatytą sukuriamas pardavimo įmonė. Dinamika 365 operacijoms sukuria atitinkamo užsakymo kitoje įmonėje ir užtikrina, kad antraštės ir eilučių informacija apie tiekėjo grąžinimo tvarka atspindi kliento parametrus grąžinimo užsakymui. Grąžinimo tvarką, pagal kurią nustatoma gali įtrauktumėte arba neįtrauktumėte nuoroda (**rasti pardavimo užsakymo**) – esamų kliento SF. Važtaraščių ir sąskaitų-faktūrų du užsakymai gali būti tvarkomi atskirai. Pavyzdžiui, jūs neturite sukurti tiekėjo grąžinimo užsakymo važtaraštį, prieš jums sukurti kliento grąžinimo užsakymo važtaraštį.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Tiesiogiai pristatyti siuntą grąžina tarp trijų šalių

Šį scenarijų galima nustatyti jei ankstesnį pardavimo ir **tiesioginio pristatymo** tipo yra baigtas, ir jei SF prieš klientas yra įmonė, kuri sąveikauja su klientu. Šioje iliustracijoje, bendrovė CompBuy anksčiau pardavė ir SF produktus klientui Extern. Gaminiai buvo išsiųsti tiesiogiai iš kompanijos CompSell klientui per vidinės įmonės užsakymo grandinę.  

[![Tiesiogiai pristatyti siuntą grąžina tarp trijų šalių](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)  

Jei klientas Extern nori grįžti produktus, grąžinimo užsakymas (RMA02) yra sukurta kliento įmonėje CompBuy. Norėdami nustatyti vidinės įmonės grandinėje, grąžinimo užsakyme turi būti pažymėta tiesioginis pristatymas. Naudojant to **rasti pardavimo užsakymo** funkcija pasirinkti kliento SF sugrįžti, sukuriamas vidinės įmonės užsakymo grandinę, kurią sudaro šie dokumentai:

-   **Originalus įsakymo grąžinti vaiką:** RMA02 (įmonė CompBuy)
-   **Pirkimo užsakymas:** PO02 (įmonė CompBuy)
-   **Vidinės įmonės grąžinimo užsakymas:** RMA\_00032 (įmonė CompSell)

Po to, kai sukuriamas vidinės įmonės tiesioginio pristatymo grandinės, fizinio tvarkymo ir perdirbimo grąžos turi atsirasti vidinės įmonės grąžinimo užsakymas, RMA kontekste\_00032 įmonės CompSell. Produktai nepristatomi įmonės CompBuy. Kai perdavimo kodo priskiriamas vidinės įmonės įsakymo grąžinti vaiką, jis sinchronizuojamas su originalus grąžinimo užsakymą, kad būtų galima tinkamai sąskaitas faktūras už pradinį užsakymą.

## <a name="post-to-the-ledger"></a>Registruojant DK.
Knygos registravimai, kurie yra generuojami, kai grąžinimo užsakymui išrašius SF yra veikiami kelis svarbius parametrus ir parametrus:

-   **Grąžinimo savikaina** – už atsargų modelių, išskyrus **Normatyvinė savikaina**, kad **grąžinimo savikaina** parametro priklauso prekės savikainą, kai jis turi priimti atgal į atsargų arba nurašytas į atliekas. Apskaičiuoti tinkamą vertinimo aprašą, svarbu, kad jūs nustatote į **grąžinimo savikaina** parametras teisingai. Jei naudojate, **rasti pardavimo užsakymo** funkcija sukurti nuorodą į pardavimo SF, grąžinimo užsakymas liniją su **grąžinimo savikaina** reikšmė yra lygi savikainai, prekės, kuri yra parduodama. Priešingu atveju savikainos vertę ateina iš prekių nustatymą arba galite įvesti rankiniu būdu.
-   **Kredito koregavimas/Storno** – **kredito korekcija** parametras su **registruojant SF** puslapis nustato, ar darbai turėtų būti įrašytas kaip teigiamas (DR/CR) įrašus arba ištaisyti, neigiamas įrašus.

Pateikiamuose pavyzdžiuose grąžinimo savikaina yra atstovaujama kaip **Inv. savikaina**.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>1 pavyzdys: Įsakymo grąžinti vaiką nėra nurodyti pardavimo SF

Įsakymo grąžinti vaiką nėra informacijos iš kliento sąskaitos-faktūros. Grąžinama Prekė yra kredituojama. Ir **kredito korekcija** parametras nėra pasirinkta, kai sugeneruojamas grąžinimo užsakymo SF arba kredito pažymos,.  

[![Patvirtinto įsakymo grąžinti vaiką nėra informacijos klientų invoic](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)  

**Pastaba:** kapitonas prekės kaina yra naudojama kaip numatytoji reikšmė, **grąžinimo savikaina** parametras. Numatytoji kaina skiriasi nuo savikainos atsargų išdavimo metu. Todėl prielaida, kad buvo patirtos nuostolių 3. Be to, grąžinimo užsakyme nėra nuolaida, kuri buvo pateikta pirkėjui pardavimo užsakymo. Todėl atsiranda pernelyg didelio kredito.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>2 pavyzdys: Kreditų pataisymai pasirinkta grąžinimo užsakymas

2 pavyzdys yra tas pats, kaip pvz 1, bet ir **kredito korekcija** pasirinktas parametras sukuria grąžinimo užsakymo SF.  

[![Įsakymo grąžinti vaiką, jei pasirinktas kredito koregavimas](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)  

**Pastaba:** DK registravimų įrašomos kaip neigiami koregavimai.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>3 pavyzdys: Grąžinimo užsakymų linija yra sukurta naudojant funkciją rasti pardavimo užsakymas

Šiame pavyzdyje grąžinimo užsakymų linija yra sukurta naudojant į **rasti pardavimo užsakymo** funkcija. Ir **kredito korekcija** parametras nėra pasirinkta kuriant SF.  

[![Grąžinimo užsakymo eilutės, kurios yra sukurtos naudojant rasti pardavimo užsakymo](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)  

**Pastaba:****nuolaida** ir **grąžinimo savikaina** yra teisingi. Todėl tiksli pardavimo SF panaikinimas įvyksta.


