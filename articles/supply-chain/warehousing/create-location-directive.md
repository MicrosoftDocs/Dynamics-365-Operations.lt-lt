---
title: Vietos nurodymo kūrimas
description: Ši tema paaiškina, kaip sukurti vietos nurodymus. Vietos nurodymai yra vartotojui draugiškos taisyklės padedančios identifikuoti paėmimo ir padėjimo vietas inventoriaus judėjime.
author: Mirzaab
manager: tfehr
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSLocDirHint, WHSLocDirTableUOM, WHSLocDirFailure
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-28
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 4f634b7f526fd198b394af6d3870c43ee560813e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016775"
---
# <a name="create-location-directives"></a>Vietos nurodymo kūrimas

[!include [banner](../includes/banner.md)]

Ši tema paaiškina, kaip sukurti vietos nurodymus. Vietos nurodymai yra vartotojui draugiškos taisyklės padedančios identifikuoti paėmimo ir padėjimo vietas inventoriaus judėjime. Pavyzdžiui, prekybos užsakymo perlaidai, vietos nurodymas nulemia vietą, kurioje prekės bus paimamos ir vietą, kur paimtos prekės bus padėtos.

> [!NOTE]
> Ši tema taikoma **Sandėlio valdymo** modulio funkcijoms. Ji netaikoma funkcijoms [Atsargų valdymo](../inventory/inventory-home-page.md) moduliui.

Galite naudoti vietos nurodymus tam, kad atliktumėte šias užduotis:

- Ateinančių prekių atidėjimas.
- Prekių paėmimas ir stadijos išorės perlaidoms.
- Žaliavų gamybai paėmimas ir atidėjimas.
- Vietų papildymas.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš tai, kai galite sukurti vietos nurodymus, privalote atlikti šiuos žingsnius tam, kad įsitikintumėte, kad išankstinės sąlygos yra sukurtos.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlis \> Sandėliai**.
1. Sandėlio sukūrimas.
1. „FastTab“ **Sandėlis** įsitikinkite nustatykite **Sandėlio valdymo procesų naudojimo** parinktį į *Taip*.
1. Sukurkite vietas, vietos tipus, vietos profilius ir vietos formatus. Dėl isamesnės informacijos, žr. [Konfigūruokite vietas WMS įjungtame sandėlyje](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).
1. Sukurkite vietas, sritis ir srities grupes. Dėl isamesnės informacijos, žr. [Sandėlio nustatymas](https://docs.microsoft.com/dynamics365/commerce/channels-setup-warehouse) ir [Konfigūruokite vietas WMS sandėlio įjungime](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).

## <a name="setup"></a>Sąranka

### <a name="create-location-directives"></a>Vietos nurodymo kūrimas

Tam, kad sukurtumėte vietos nurodymus, atlikite šiuos žingsnius.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.
1. Juostos sąraše, nustatykite **Darbo tvarkos tipas** laukelį atsargų perlaidos tipui, kuriam kuriate vietos nurodymą.
1. Veiksmų juostoje pasirinkite **Naujas** tam, kad sukurtumėte vietos nurodymą.
1. Naujos vietos nurodymui, nustatykite laukelius kaip aprašyta tolesnėje lentelėje.

    | Laukas | aprašymas |
    |---|---|
    | Sekos numeris | Įveskite papunktį, kuris rodo vietos nurodymo sektos padėtį. Sekos padėtys nusprendžia, kada kiekvienas vietos nurodymas yra apdorojamas pasirinkto darbo vietos tipui. |
    | Pavadinimas / vardas ir (arba) pavardė | Įveskite vietos nurodymo pavadinimą. | 
    | Darbo tipas | Pasirinkite turimą atlikti darbo tipą. Verčių sąrašas priklau nuo atsargų perlaidos tipo, kurį pasirenkate **Darbo tvarkos tipo** laukelyje. Tolesnės vertės gali būti:<ul><li>**Padėjimas** – Vietos nurodymas bandys surasti geriausią padėjimo vietą ar nustatyti atsargas, kurios patenka į sistemą per gavimo, gamybos ar atsargų keitimus. Vietos nurodymas taip pat naudojamas nustatyti padėjimo į etapą vietą ar galutinę pristatymo iki durų vietą išorės sraute.</li><li>**Paėmimas** – Vietos nurodymas bandys surasti geriausias vietas iš fizinių atsargų rezervo (darbo sukūrimas). Paėmimas gali būti užbaigtas (paėmimo darbo eilutė gali būti uždaryta) net jei darbas nėra užbaigtas. Vartotojas gali užbaigti fizinį paėmimą. Sistemoje, šis veiksmas yra paėmimo žingsnis. Vartotojas tuomet gali atšaukti darbą iš mobilaus prietaiso ir užbaigti darbą vėliau (pavyzdžiui, padėti). Nepaisant to, darbo antraštė yra uždaroma pirmiausiai, kai galutinis padėjimas yra baigtas.</li><li>**Skaičiavimas** , **Keitimai** , **Tinkinimas** , **Atsargos statuso keitimas** , **Licencijos numerio kūrimas** , **Spausdinimas** , **Statuso keitimas** ir **Pakavimas į lizdinius licencijų numerius** – Šių verčių negalima naudoti jokiuose vietos nurodymo nustatymuose.</li></ul> |
    | Vieta | Pasirinkite vietą, kurioje darbas turi būti užbaigtas. |
    | Sandėlis | Pasirinkite sandėlio vietą, kurioje darbas turi būti užbaigtas. |
    | Krypties kodas | Pasirinkite nurodymo kodą, kuris turi valdyti vietos nurodymo pasirinkimą, susijusį su darbo šablono padėjimo eilutėmis, kurioms yra priskirtas šis kodas. **Nurodymo kodo** puslapyje galite sukurti naujus kodus, kurie gali būti naudojami sujungti darbo šabloną su vietos nurodymu. Galite taip pat naudoti puslapį siekiant užmegzti ryšį tarp bet kurių darbo šablono eilučių ir vietos nurodymo (tokio kaip pristatymo iki durų ar etapo vietos). Dėl išsamesnės informacijos, kaip konfigūruoti nurodymo kodą su darbo šablonu, žr. [Valdyti sandėlio darbą naudojant darbo šablonus ir vietos nurodymus](control-warehouse-location-directives.md).<p>Jei nurodymo kodas yra nustatytas tada, kai darbas turi būti sukurtas, sistema ieškos vietos nurodymų pagal nurodymo kodą, o ne pagal seką. Tokiu būdu, galite būti tikslesni dėl vietos šablono, kuris yra naudojamas konkrečiame žingsnyje darbo šablone, tokiame kaip žingsnio etapo medžiagose.</p> |
    | Perdavimo kodas | Pasirinkite išdėstymo kodą, kad nukreiptumėte gautų prekių atidėjimą į vietą. (Dėl išsamesnės informacijos, žr. [Nustatyti išdėstymos kodus](tasks/set-up-dispositions-codes.md).) Šis laukelis prieinamas tik tada, kai **Darbo tvarkos tipo** laukelis yra nustatytas į *Prekybos užsakymai* , *Grąžinimo užsakymai* ar *Užbaigtų prekių atidėjimas*. |
    | Keli SKU | Nustatykite šią parinktį į *Taip* tam, kad naudotumėte daugelį sandėlio laikymo objektų vietoje. Pavyzdžiui, ši parinktis turi būti nustatyta į *Taip* pristatymui iki durų.<p>Jei **Daugelis SKU** parinktis yra nustatyta į *Taip* , padėjimo vieta bus nurodyta darbe (kaip tikėtasi). Nepaisant to, padėjimo vietą galima valdyti kelių prekių paėmimu tik, jei darbas apima skirtingus SKU, kurie turi būti paimti ir padėti, ne jei darbas apima tik vieną SKU, kuris turi būti padėtas.</p><p>Jei **Daugelis SKU** parinktis yra nustatyta į *Ne* , padėjimo vieta bus nurodyta tik jei padėjimas turi vieną iš SKU tipų.</p><p>Tam, kad būtų naudojamos abi prieigos, turite nurodyti dvi linijas su ta pačia struktūra ir nustatymais ir nustatyti **Daugelis SKU** parinktį į *Taip* vienai iš šių eilučių ir *Ne* kitai. Kitaip tariant, du identiškos vietos nurodymai yra būtini padėjimo veiksmams net jei neturite atskyrimo tarp vieno ir kelių SKU darbo ID. Privalote taip pat nustatyti vietos nurodymą paėmimui, jei turite užsakymą su daugiau nei viena preke.</p><p>**Pastaba:** Jei nustatote **Daugelis SKU** parinktį į *Taip* *Padėjimo* vietos nurodymo darbo tipui, sistema visuomet pasirinks pirmąją vietos nurodymo eilutę nepriklausomai nuo kitų apribojimų sukurtų eilutėms.</p> |

1. Pasirenkamas: Veiksmų juostoje pasirinkite **Redaguoti užklausą** tam, kad pasirinktumėte vietas arba nurodykite apribojimus taikomus tada, kai pasirenkate konkretų vietos nurodymą.
1. **Eilutės** „FastTab“, sukurkite vieną ar kelias eilutes tam, kad nurodytumėte padalinius ir nustatytumėte kiekio vietą ir jį rezervuotumėte sandėlyje.
1. Kiekvienoje naujoje eilutėje, nustatykite tolesnėje lentelėje aprašytus laukelius.

    | Laukas | aprašymas |
    |---|---|
    | Sekos numeris | Įveskite papunktį, kuris rodo vietos nurodymo sektos padėtį. Sekos padėtys nusprendžia, kada kiekvienas vietos nurodymas yra apdorojamas pasirinkto darbo vietos tipui. |
    | Pradinis kiekis | Nurodykite pradžios kiekio intervalą, kai vidurinio tinklelio seka turi būti pasirenkama. Nurodykite matavimo vieneto kiekį, kuris yra pasirinktas **Vieneto** laukelyje. |
    | Kiekis Iki | Nurodykite pabaigos kiekio intervalą, kai vidurinio tinklelio seka turi būti pasirenkama. Nurodykite matavimo vieneto kiekį, kuris yra pasirinktas **Vieneto** laukelyje. |
    | Vienetas | Pasirinkite matavimo vienetą prekėms.<p>Galite nurodyti mažiausią kiekį ir didžiausią kiekį, kuriam turi būti taikomas nurodymas. Galite taip pat nurodyti, kad nurodymas turi būti naudojamas konkrečiam atsargų vienetui. **Vieneto** laukelis yra naudojamas tik kiekio apskaičiavimui.</p><p>Tam, kad nustatytumėte, ar vietos nurodymo eilutės yra taikomos, sistema apskaičiuoja kiekius naudodama **Vieneto** vertę, kuri yra nurodyta eilutėje. Kas kartą, kai patenkama į nurodymo eilutę, sistema bandys paversti užklausos vienetą į vienetą, kuris yra nurodytas eilutėje. Jei vieneto pavertimas neegzistuoja, sistema pereis prie kitos eilutės.</p> |
    | Sandėliavimo kiekis | Laukelis galioja tik tada, kai bandote padėti ir nustatyti sandėlio kiekį. Kitaip tariant, jis galioja tik *Padėjimo* darbui. Pasirinkite metodą, kuris yra naudojamas apskaičiuoti, ar kiekis yra nustatytame intervale **Iš kiekio** ir **Į kiekį** laukelius. Jei vietos nurodymas yra vidaus perlaidai, pasirinkite vieną iš tolesnių parinkčių:<ul><li>**Licencijos numerio kiekis** ─ Tam, kad apskaičiuotumėte, ar kiekis yra galutinio kiekio intervale, naudokite gautą kiekį licencijos numeryje.</li><li>**Panaudotas kiekis** ─ Tam, kad apskaičiuotumėte, ar kiekis yra galutinio kiekio intervale, naudokite kiekį, kuris yra apjungtas perlaidoje. Pavyzdžiui, sandėlyje, jei galite gauti 1000 kiekį ir suskirstyti jį į 10 licencijos numerių, kiekvienas numeris turi 100 kiekį, kurį galite naudoti kaip 1000 prekių vietoje licencijos numerio 100 kiekio.</li><li>**Likęs kiekis** ─ Tam, kad apskaičiuotumėte, ar kiekis yra galutinio kiekio intervale, naudokite kiekį, kuris turi būti gautas įsigijimo užsakymo eilutėje, kuri šiuo metu yra registruojama.</li><li>**Laukiamas kiekis** ─ Tam, kad apskaičiuotumėte, ar kiekis yra galutinio kiekio intervale, naudokite bendrą įsigijimo užsakymo eilutės kiekį nepriklausomai nuo gauto kiekio.</li></ul> |

1. Pasirenkamas: **Eilutės** „FastTab“, galite nustatyti tolesnius papildomus laukelius.

    | Laukas | aprašymas |
    |---|---|
    | Riboti pagal vienetą | Pasirinkite šį žymimą laukelį tam, kad apribotumėte matavimo vienetus, kurie yra laikomi galiojančiais atrankos kriterijais vietos nurodymo eilutėms. Kai matavimo vienetai buvo nurodyti, tik prekės, kuriose vienetas atitinka mažiausiai vieną vienetą, nustatytą vieneto sekos grupei, bus laikomas galiojančiu eilutės pasirinkime.<p>Pavyzdžiui, vienetas yra apribotas padėklų ir prekė yra susieta su vieneto sekos grupe, kuri apima *padėklų* vienetą. Šiuo atveju, prekės yra laikomos galiojančia parinktimi vietos nurodymui.</p><p>Nepaisant to, **Apribotas vieneto** žymimas laukelis nekontroliuoja vieneto ar vienetų, kurie yra taikomi darbo eilutėms. Vieneto apribojimas taikomas tik vienetams, kurie yra prieinami per vieneto sekos grupę.</p><p>Pavyzdžiui, vienetas yra apribotas padėklų ir prekė yra susieta su vieneto sekos grupe, kuri apima tiek *padėklus* , tiek ir *vnt.* vienetus. Matavimo vienetas buvo nustatytas, kai 1 padėklas = 100 vnt. ir vietos nurodymas naudojamas **Apribotas vieneto** funkcijos tik padėklams. Taip pat, buvo nustatytas darbo šablonas, kuris apriboja darbo antraštės kūrimą iki 50 vnt. Šiuo atveju, bus sukurtos 50 vnt. darbo eilutės.</p><p>Matavimo vieneto apribojimo nustatymui, atlikite šiuos žingsnius </p><ol><li>**Eilutės** „FastTab“ pasirinkite **Apriboti pagal vienetą**. Šis mygtukas yra prieinamas tik tuomet, kai pasirenkate **Apriboti pagal vienetą** žymimą laukelį eilutei ir tuomet pasirenkate **Įrašyti**.</li><li>**Vieneto** laukelyje pasirinkite matavimo vienetą tam, kad apribotumėte paėmimo ir padėjimo procesus.</li></ol> |
    | Apvalinti iki vieneto | Pasirinkite šią parinktį tam, kad nurodytumėte, jog žaliavos paėmimas būtų apvalinamas iki kelių tvarkymo vienetų, kurie yra nurodyti **Apriboti pagal vienetą** laukelyje. Šis laukelis taikomas tik žaliavų paėmimui ir *Paėmimo* tipo vietos nurodymui. |
    | Sandėliavimo pakavimo kiekis | Pasirinkite šį žymimą laukelį, jei pakavimo vieneto kiekis yra nurodytas **Prelybos užsakymas** puslapyje. Jei pasirenkate šį žymimą laukelį, pasirenkamos tik vietos turinčios šį pakavimo vieneto kiekį. |
    | Leisti skaidyti | Pasirinkite šį žymimą laukelį tam, kad atskirtumėte kiekius daugelyje vietų. |
    | Skubaus papildymo šablonas | Sukurkite ryšį tam, kad papildytumėte šabloną taip, kad papildymas prasidėtų nedelsiant, jei prekės nėra priskirtos. Jei paliekate šį laukelį tuščią, prekės papildymas neprasidės, kol visos vietos nurodymo eilutės nebus apdorotos.<p>Šis laukelis yra prieinamas pasirinktiems darbo tvarkos tipams, kai papildymas yra leidžiamas, tokiems kaip  *Prekybos užsakymams* ir *Žaliavos medžiagos paėmimui*.</p> |

1. **Vietos nurodymo veiksmai** „FastTab“, pasirinkite **Naujas** tam, kad pasirinktumėte vietą ar vietų intervalą.
1. **Sekos numeris** laukelis rodo seką, kurioje pasirinktam darbo tipui bus apdorojamas vietos nurodymas. Galite keisti seką. Nepaisant to, būkite atsargūs su sekos numeriais vietos nurodymo veiksmams, nes vietos nurodymo veiksmai visuomet bus vykdomi šia seka.
1. **Pavadinimas** laukelyje įveskite vietos nurodymo veiksmo pavadinimą. Būkite konkretūs taip, kad būtų aišku, koks tai veiksmas.
1. Pasirenkamas: Pasirinkite **Redaguoti užklausą** tam, kad keistumėte sandėlio vietas ir kitus kriterijus.
1. Pasirenkamas: Galite nustatyti tolesnius papildomus laukelius vietos nurodymui.

    | Laukas | aprašymas |
    |---|---|
    | Fiksuotos vietos naudojimas | Pasirinkite, į kurias vietas reiktų atsižvelgti vietos nurodyme:<ul><li>**Fiksuotos ir nefiksuotos vietos** – Bus atsižvelgta į vietos nurodymą visose vietose.</li><li>**Tik fiksuotos vietos produktui** – Vietos nurodymas atsižvelgs tik į fiksuotas vietas produktams.</li><li>**Tik fiksuotos vietos produkto variantui** – Vietos nurodymas atsižvelgs tik į fiksuotas vietas produkto variantams.</li></ul> |
    | Leisti neigiamas atsargas | Pasirinkite šį žymimą laukelį tam, kad leistumėte neigiamas atsargas nurodytoje sandėlio vietoje. |
    | Paketas įjungtas | Pasirinkite šį žymimą laukelį tam, kad naudotumėte pakuotės strategijas prekėms, kurios yra įjungtos paketams. Jei šis žymimas laukelis yra pasirinkitas ir **Strategijos** laukelis yra nustatytas į *Jokio* , sistema judės prie kito veiksmo eilutės. |
    | Strategija | Pasirinkite strategiją, kurią vietos nurodymas turėtų naudoti:<ul><li>**Jokia** – Bus nenaudojama jokia strategija.</li><li>**Atitikimo pakavimo kiekis** – Ši strategija tikrina, ar paėmimo vieta turi konkretų pakavimo kiekį. Ši strategija galioja tik, jei **Darbo tipo** laukelis yra nustatytas į *Paimti*.</li><li>**Konsoliduoti** – Ši strategija konsoliduoja prekes konkrečioje vietoje, kai panašios prekės jau yra prieinamos. Ši strategija galioja tik, jei **Darbo tipo** laukelis yra nustatytas į *Padėti*. Įprastuose padėjimo nustatymui, sistema bando konsoliduoti pirmojoje veiksmo eilutėje ir tuomet antrojoje veiksmo eilutėje ji bando padėti be konsolidavimo. Prekių konsolidavimas paverčia pastarąjį paėmimą efektyvesniu.</li><li>**FEFO paketo rezervavimas** – Ši strategija yra naudojama, kai atsargos yra aptinkamos naudojant paketo pabaigos datą ir jų priskyrimą paketų rezervavimui. Pirmoji galiojimo pabaiga, pirmoji išeigos (FEFO) paketo rezervavimo strategija taip pat naudojama, kai atsargos nustatomos naudojant paketo geriausio iki datą kartu su galiojimo pabaigos data. Galite naudoti šią strategiją tik pakete įjungtoms prekėms. Ši strategija galioja tik, jei **Darbo tipo** laukelis yra nustatytas į *Paimti*. Jums pasirinkus šią strategiją, panaikinate visas taikomas rūšiavimo užklausas paketui.</li><li>**Apvalinimas iki pilno LP** – Ši strategija suapvalina atsargų kiekį taip, kad jis atitinka licencijos numerio kiekį priskirtą prekėms, kurios turi būti supakuotos. Ši strategija gali būti naudojama tik vietos nurodymo tipo papildymui ir jei **Darbo tipo** laukelis yra nustatytas į *Paimti*.</li><li>**Tuščia vieta be jokio ateinančio darbo** – Ši strategija naudojama aptikti tuščias vietas. Vieta laikoma tuščia, jei ji neturi jokių fizinių atsargų ir jokio tikimosi ateinančio darbo. Ši strategija galioja tik, jei **Darbo tipo** laukelis yra nustatytas į *Padėti*.</li></ul> |

## <a name="example-of-the-use-of-location-directives"></a>Vietos nurodymų naudojimo pavyzdys

Šiame pavyzdyje svarstomas pirkimo užsakymo procesas, kai vietos nurodymas turi sandėlyje rasti laisvos vietos atsargų prekėms, kurios buvo ką tik užregistruotos gavimo rampoje. Pirmiausia reikia sandėlyje rasti laisvos vietos, konsoliduojant esamas atsargas. Jei konsoliduoti negalima, tada reikia rasti tuščią vietą.

Pagal šį scenarijų turite nustatyti du vietos nurodymo veiksmus. Pirmasis sekos veiksmas turi naudoti strategiją **Konsoliduoti** , o antrasis – strategiją **Tuščia vieta, kurioje negaunama darbo**. Jei nenustatysite trečio veiksmo, skirto perpildos scenarijui tvarkyti, kai sandėlyje nėra vietos, galimi du rezultatai: darbą galima kurti net jei nėra nurodytų vietų arba darbo kūrimo procesas gali nepavykti. Rezultatas nustatomas pagal sąranką puslapyje **Vietos nurodymo klaidos** , kuriame galite nuspręsti, ar norite kiekvienam darbo užsakymų tipui nustatyti parinktį **Stabdyti darbą esant vietos nurodymo klaidai**.

## <a name="next-step"></a>Kitas veiksmas

Kai sukūrėte vietos nurodymus, galite susieti visus nurodymo kodus su darbo šablono kodu darbo sukūrimui. Dėl išsamesnės informacijos, žr. [Sandėlio darbo kontroliavimas naudojant darbo šablonus ir vietos nurodymus](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/control-warehouse-location-directives).

## <a name="technical-information-for-system-admins"></a>Techninė informacija sistemos administratoriams

Jei neturite prieigos prie puslapių, kurie yra naudojamo šios užduoties užbaigimui, susisiekite su sistemos administratoriumi ir pateikite informaciją rodomą tolesnėje lentelėje.

| Kategorija | Būtinoji sąlyga |
|---|---|
| Configuration Keys | Eikite į **Sistemos administravimas \> Sąranka \> Licencijos konfigūracija**. Išplėskite **Prekybos** licencijos raktą ir tuomet pasirinkite **Sandėlio ir gabenimo valdymo** konfigūravimo raktą. |
