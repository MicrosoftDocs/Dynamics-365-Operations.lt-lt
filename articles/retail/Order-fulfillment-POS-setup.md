---
title: "Parduotuvės užsakymų įvykdymo nustatymas"
description: "Šioje temoje pateikiama apžvalga, kaip nustatyti parduotuvės užsakymų įvykdymą."
author: rubencdelgado
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: rubencdelgado
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: c8c2e56a1f65d28991dca3e1da4159efe81f2bf3
ms.contentlocale: lt-lt
ms.lasthandoff: 01/04/2019

---


# <a name="set-up-order-fulfillment-for-stores"></a>Parduotuvės užsakymų įvykdymo nustatymas

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Peržiūra

Daugelis mažmenininkai norėtų optimizuoti užsakymo įvykdymą, suteikdami galimybę parduotuvėms vykdyti užsakymus. Užsakymų įvykdymas parduotuvės lygiu gali palengvinti konkrečios parduotuvės atsargų perpildymo atvejais, taip pat tai gali būti naudinga dėl logistinių tikslų tais atvejais, kai parduotuvė turi papildomų pajėgumų arba yra arčiau kliento, kuriam reikia siųsti prekes. Šiems poreikiams patenkinti elektroniniame kasos aparate galima naudoti bendrąją užsakymų įvykdymo operaciją.

Užsakymams, kurie turi būti įvykdyti konkrečioje parduotuvėje, skirtas specialus parduotuvės sandėlis, nurodytas užsakymo antraštėje arba eilutėje.

Užsakymo įvykdymo operacija elektroniniame kasos aparate suteikia vieną darbo sritį elektroniniame kasos aparate, kurią galima naudoti užsakymams apdoroti. Tai apima viską nuo užsakymo priėmimo, jo pažymėjimo išsiųstu arba paėmimo parduotuvėje inicijavimo.

## <a name="set-up-the-order-fulfillment-operation"></a>Užsakymų įvykdymo operacijos nustatymas

Užsakymų įvykdymas, [operacijos ID 928](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-operations), gali būti naudojamas norint pasiekti parduotuvės užsakymų įvykdymo darbo sritį elektroniniame kasos aparate.

Vykdykite veiksmus, aprašytus skyriuje [Operacijos įtraukimas į mygtukyną](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts), norėdami nurodyti, kurį parametrą naudoti iškviečiant užsakymų įvykdymo funkciją elektroniniame kasos aparate. Pagal numatytuosius parametrus nurodžius užsakymų įvykdymo operacijas pasirenkamas parametras **Visi užsakymai**. Sukonfigūravus naudojant šį parametrą, operacija pateiks visas užsakymo eilutes, kurias reikia įvykdyti dabartinėje parduotuvėje. Taip pat naudoti parinktį **Siųstini užsakymai**, kurią galima priskirti mygtukui ir naudoti, kai vartotojas nori pamatyti tik užsakymus, kurie bus siunčiami iš parduotuvės. Galiausiai galima naudoti parametrą **Paimtini užsakymai**. Iškvietus elektroniniame kasos aparate, šis parametras pateikia tik užsakymus, kurie bus paimti iš parduotuvės. Skirtingus parametrus galima priskirti skirtingiems mygtukams, norint suteikti vartotojui įvairių būdų, kaip peržiūrėti užsakymo įvykdymą.

### <a name="enable-users-to-access-order-fulfillment-at-the-point-of-sale"></a>Suteikite vartotojams prieigą prie užsakymų įvykdymo elektroniniame kasos aparate

Užsakymų įvykdymo operacija neturi savo parengtos naudoti teisės, tačiau ateityje vartotojams gali reikėti teisės **Leisti nuskaityti užsakymą**, kad būtų galima iškviesti operaciją iš elektroninio kasos aparato.

Parduotuvės lygiu galima naudoti konfigūracijos parametrą norint nustatyti, ar užsakymo eilutė turi būti priimta neautomatiškai iš elektroninio kasos aparato. Jei ta konfigūracijos parinktis nenustatyta, užsakymo eilutės bus priimtos pagal numatytuosius parametrus. Jei ši konfigūracijos parinktis įjungta, elektroniniame kasos aparate vartotojams reikės teisės **Leisti priimti užsakymą**, kad būtų galima priimti užsakymus iš elektroninio kasos aparato.

### <a name="enable-manual-order-acceptance"></a>Neautomatinio užsakymų priėmimo įjungimas

Pagal numatytuosius parametrus užsakymo eilutės, priskirtos parduotuvei, yra pažymėtos kaip **Priimta**. Tai reiškia, kad manoma, jog jos bus įvykdytos iš priskirtos parduotuvės ir daugiau nebebus priskirtos niekam. Tam tikrais atvejais mažmenininkai gali norėti neautomatiškai priimti užsakymus, kol jų dar negalima įvykdyti. Pavyzdžiui, jei parduotuvėje trūksta darbuotojų užsakymams įvykdyti, parduotuvės vadovas priims tik tiek apdorotinų užsakymų, kiek, jo manymu, jų galima tinkamai apdoroti per tam tikrą dieną. Kol užsakymas nepatvirtintas, tarnybinis biuras gali jį iš naujo priskirti kitai parduotuvei. Tokiu būdu užsakymų priėmimas taip pat suteikia galimybę nurodyti, kad užsakymą patvirtino parduotuvė ir jis bus įvykdytas.

Paėmimo parduotuvėje užsakymo eilutės pažymėtos kaip **Laukiama** ir jos nėra priimamos.

Norėdami įjungti neautomatinį užsakymo eilučių priėmimą, pasirinkite **Mažmeninė prekyba** \> **Kanalai** \> **Mažmeninės prekybos parduotuvės** \> **Visos mažmeninės prekybos parduotuvės**. Pasirinkite parduotuvę ir spustelėkite parduotuvės ID, norėdami peržiūrėti parduotuvės informaciją. Spustelėkite **Redaguoti**. „FastTab“ **Bendra** raskite paantraštę**Užsakymo įvykdymas** ir pakeiskite parametro **Neautomatinis priėmimas** iš parinkties **Ne** į **Taip**.

### <a name="enable-reject-order-line-capability"></a>Užsakymo eilutės atmetimo galimybės įjungimas

Užsakymo eilutes taip pat galima atmesti iš elektroninio kasos aparato. Atmetant užsakymo eilutę nurodoma, kad ji nebus vykdoma parduotuvėje, ir užsakymo eilutė grąžinama, kad būtų perskirta kitai parduotuvei arba sandėliui. Užsakymo eilutės atmetimo teisė suteikiama per teisę **Leisti atmesti užsakymą** EKA teisių grupėje, susietoje su darbuotoju. Mažmenininkai gali įgalioti savo darbuotojus, atmetančius eilutę, pateikti atmetimo priežastį. Tai galima padaryti naudojant tipo **Informacijos kodo veikla** **užsakymo įvykdymo** informacijos kodus ir priskiriant informacijos kodą veiksmui **Atmesti užsakymo eilutę** funkcijų šablone, susietame su kanalu.

> [!NOTE]
> Tik tipo **Informacijos kodo veikla** **užsakymo įvykdymo** informacijos kodus galima priskirti veiksmui **Atmesti užsakymo eilutę**.

### <a name="synchronize-changes-to-the-channel-database"></a>Pakeitimų sinchronizavimas su kanalų duomenų baze

Priskyrus operaciją mygtukynui, priskyrus reikiamas teises ir sukonfigūravus kanalą, keitimus reikia sinchronizuoti su kanalo duomenų baze. Norėdami tai padaryti, pasirinkite **Mažmeninė prekyba** \> **Mažmeninės prekybos IT** \> **Paskirstymo grafikas**. Pasirinkite grafiką 1090 – registrai, kad sinchronizuotumėte mygtukyno keitimus, tada spustelėkite **Vykdyti dabar**. Tada sinchronizuokite teisių keitimus pasirinkdami 1060 – personalas ir spustelėkite **Vykdyti dabar**. Tada sinchronizuokite kanalo keitimus pasirinkdami 1070 – kanalo konfigūracija ir spustelėkite **Vykdyti dabar**. Galiausiai sinchronizuokite naujai sukurtą atšaukimo priežasties informacijos kodą pasirinkdami 1110 – visuotinė konfigūracija ir spustelėkite **Vykdyti dabar**.

## <a name="use-order-fulfillment-at-the-point-of-sale"></a>Užsakymo įvykdymo naudojimas elektroniniame kasos aparate

Atidarykite elektroninį kasos aparatą ir pasirinkite užsakymo įvykdymo operaciją. Atsižvelgiant į konfigūraciją, bus rodomos visos eilutės, paėmimo užsakymo eilutės arba siuntimo užsakymo eilutės.

### <a name="order-fulfillment-view"></a>Užsakymų įvykdymo rodinys

Užsakymo įvykdymo rodinyje išvardijamos parduotuvėje įvykdytinos užsakymo eilutės ir pateikiami toliau nurodyti stulpeliai.

- Užsakymo numeris
- Produkto numeris
- aprašymas
- Užsakytas kiekis
- Pageidaujama pristatymo data
- Kliento vardas
- Įvykdymo būsena

Konkrečios užsakymo eilutės papildomą informaciją galima peržiūrėti pasirinkus užsakymo eilutę ir tada atidarius iškeliamąjį meniu, esantį žemiau prisiregistravusio vartotojo / pamainos informacijos, kuri rodoma elektroninio kasos aparato antraštėje. Šiame meniu yra 2 skirtukai: vienas skirtas eilutės informacijai, o kitas – užsakymo informacijai. Eilutės informacijos skirtuke pateikiama toliau nurodyta informacija.

- Užsakytas kiekis
- Likęs kiekis, kurį reikia išsiųsti / paimti
- Paimtas kiekis
- Supakuotas kiekis
- Kiekis, kurio SF išrašyta (jau paimtas arba išsiųstas kiekis)
- Pristatymo būdas
- Pristatymo adresas

Informacijos iškeliamajame meniu taip pat yra skirtukas, kuriame pateikiama daugiau užsakymo lygio informacijos, įskaitant toliau nurodytąją.

- Kliento vardas
- Kliento ID
- Užsakymo numeris
- Užsakymo suma
- Užsakymo balansas

Užsakymo įvykdymo rodinio apačioje yra veiksmų sritis. Joje yra visi veiksmai, kuriuos galima taikyti užsakymo eilutei. Jei veiksmo negalima atlikti atsižvelgiant į eilutės būseną, tas veiksmas nebus pateiktas.

Pagal numatytuosius parametrus užsakymų būsena bus **Priimta**. Užsakymo būseną galima peržiūrėti kaip užsakymo eilučių sąrašo stulpelį. Jei parinktis **Neautomatinis priėmimas** sukonfigūruota kanalo lygiu, visos siųstinos eilutės bus rodomos kaip **Laukiama** ir prieš įvykdant jas reikia priimti. Paėmimo parduotuvėje užsakymų būsena yra **Laukiama** pagal numatytuosius parametrus ir jų nereikia priimti.

### <a name="order-fulfillment-line-actions"></a>Užsakymo įvykdymo eilutės veiksmai

- **Redaguoti** – jei užsakymo būsena yra laukiama, ją galima koreguoti elektroniniame kasos aparate. Užsakymų, kurie jau buvo iš dalies paimti, supakuoti arba kurių SF buvo išrašyta, negalima redaguoti iš užsakymo įvykdymo rodinio.
- **Priimti** – jei parinktis **Neautomatinis priėmimas** sukonfigūruota kanalo lygiu, eilutės pirmiausia turi būti priimtos, kad jos galėtų pereiti užsakymo įvykdymo proceso etapus.
- **Paimti** – paėmimo parinktis suteikia galimybę atlikti kelis veiksmus. Pirma, **Paėmimas** atnaujina užsakymo eilutės būseną, todėl kiti parduotuvės darbuotojai nemėgintų paimti tos pačios eilutės. Antra, veiksmu **Spausdinti išrinkimo dokumentą** išspausdinamas pasirinktos eilutės arba eilučių išrinkimo dokumentas ir taip pat atnaujinama jų būsena į **Paėmimas**. Išrinkimo dokumento formatai valdomi kaip kvitų formatų dalis. Daugiau informacijos, kaip nustatyti kvitų formatus, žr. [Kvitų šablonai ir spausdinimas](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing). Galiausiai veiksmas **Pažymėti kaip paimtą** nurodo, kad eilutė yra paimta. Veiksmas **Pažymėti kaip paimtą** inicijuoja atitinkamas atsargų operacijas tarnybiniame biure. Paėmimo veiksmus galima vienu metu taikyti kelios užsakymo eilutėms iš kelių užsakymų ir naudojant visus pristatymo būdus.
- **Atmesti** – eilutes arba dalines eilutes galima atmesti. Tai suteikia galimybę jas iš naujo priskirti tarnybiniam biurui arba kitai parduotuvei ar sandėliui. Eilutes galima atmesti tik jei jos dar nebuvo paimtos arba supakuotos. Norėdami atmesti eilutę, kuri jau buvo paimta arba supakuota, tarnybiniame biure reikia atmesti tos eilutės paėmimą arba supakavimą.
- **Pakavimas** – pakavimo parinktis suteikia galimybę atlikti du veiksmus: veiksmu **Spausdinti važtaraštį** bus pasirinktų eilučių išspausdintas važtaraštis, o veiksmu **Pažymėti kaip supakuotas** tarnybiniame biure eilutės bus pažymėtos kaip supakuotos ir eilutes bus pažymėtos kaip pristatytos. Vienu metu galima pakuoti tik užsakymo eilutes, kurios priklauso tam pačiam užsakymui ir kurių pristatymo būdas toks pats. Važtaraščio formatai valdomi kaip kvitų formatų dalis. Daugiau informacijos, kaip nustatyti kvitų formatus, žr. [Kvitų šablonai ir spausdinimas](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing).
- **Siųsti** – siuntimo veiksmu pasirinktos eilutės tarnybiniame biure bus pažymėtos kaip **Pristatyta**. Visiškai išsiuntus eilutę, ji nebebus rodoma užsakymo įvykdymo rodinyje.
- **Paėmimas** – paėmimo veiksmu eilutės įtraukiamos į paėmimo operacijos rodinį. Jei yra kitų užsakymo eilučių, kurios šiuo metu nėra paimamos, jos bus įtrauktos į operacijos rodinį nurodant nulinį kiekį. Visiškai paėmus eilutę, ji nebebus rodoma užsakymo įvykdymo rodinyje.

### <a name="order-fulfillment-filtering"></a>Užsakymų įvykdymo filtravimas

Užsakymų įvykdymas elektroniniame kasos aparate apima filtravimą, kad vartotojai galėtų lengvai rasti, ko reikia. Filtrus galima keisti ekrano **Elektroninis kasos aparatas** apačioje esančioje veiksmų srityje. Pagal numatytuosius parametrus taikomas filtras **Pristatymo tipas**, atsižvelgiant į tai, kaip nustatyta operacija. Jei nustatytas operacijos parametras **Visi užsakymai**, tada tas filtras taikomas atidarant užsakymų įvykdymo funkciją. Tas pats taikoma parametrams **Paėmimas parduotuvėje** ir **Siųsti iš parduotuvės**. Toliau nurodyti kiti filtrai, kuriuos galima taikyti užsakymų įvykdymo rodiniui.

- Kliento numeris
- Kliento vardas
- Kliento el. paštas
- Užsakymo numeris
- Pristatymo būdas
- Gavimo numeris
- Kanalo nuorodos ID
- Pradinis parduotuvės numeris
- Eilutės būsena
- Sukūrimo data
- Pristatymo data
- Gavimo data

