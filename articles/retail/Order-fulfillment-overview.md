---
title: "Parduotuvės užsakymų įvykdymo peržiūra"
description: "Šioje temoje pateikiama parduotuvės užsakymų įvykdymo nustatymo apžvalga."
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
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 1ac73b50c6051ba7d3b96ae49cb7e33cf436ba9e
ms.contentlocale: lt-lt
ms.lasthandoff: 03/08/2018

---

# <a name="store-order-fulfillment"></a>Parduotuvės užsakymų įvykdymas

[!INCLUDE [banner](includes/banner.md)]

Daugelis mažmenininkai norėtų optimizuoti užsakymo įvykdymą, suteikdami galimybę parduotuvėms vykdyti užsakymus. Užsakymų įvykdymas parduotuvės lygiu gali palengvinti konkrečios parduotuvės atsargų perpildymo atvejais, taip pat tai gali būti naudinga dėl logistinių tikslų tais atvejais, kai parduotuvė turi papildomų pajėgumų arba yra arčiau kliento, kuriam reikia siųsti prekes. Šiems poreikiams patenkinti elektroniniame kasos aparate galima naudoti bendrąją užsakymų įvykdymo operaciją.

Užsakymams, kurie turi būti įvykdyti konkrečioje parduotuvėje, skirtas specialus parduotuvės sandėlis, nurodytas užsakymo antraštėje arba eilutėje. 

Užsakymo įvykdymo operacija elektroniniame kasos aparate suteikia vieną darbo sritį elektroniniame kasos aparate, kurią galima naudoti užsakymams apdoroti. Tai apima viską nuo užsakymo priėmimo, jo pažymėjimo išsiųstu arba paėmimo parduotuvėje inicijavimo. 

## <a name="access-unified-order-fulfillment-in-the-point-of-sale"></a>Prieiga prie bendrojo užsakymų įvykdymo srities elektroniniame kasos aparate

Užsakymų įvykdymas, [operacijos ID 928](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-operations), gali būti naudojamas norint pasiekti parduotuvės užsakymų įvykdymo darbo sritį elektroniniame kasos aparate. 

Užsakymų įvykdymo operacija neturi savo parengtos naudoti teisės, tačiau ateityje vartotojai galės naudoti teisę **Leisti nuskaityti užsakymą**, kad būtų galima iškviesti operaciją iš elektroninio kasos aparato.

Parduotuvės lygiu galima naudoti konfigūracijos parametrą norint nustatyti, ar užsakymo eilutė turi būti priimta neautomatiškai iš elektroninio kasos aparato. Jei ta konfigūracijos parinktis nenustatyta, užsakymo eilutės bus priimtos pagal numatytuosius parametrus. Jei ši konfigūracijos parinktis įjungta, elektroniniame kasos aparate vartotojai turėsi pasirinkti teisę **Leisti priimti užsakymą**, kad būtų galima priimti užsakymus iš elektroninio kasos aparato.
Užsakymo eilutes taip pat galima atmesti iš elektroninio kasos aparato. Atmetant užsakymo eilutę nurodoma, kad ji nebus vykdoma parduotuvėje, ir užsakymo eilutė grąžinama, kad būtų perskirta kitai parduotuvei arba sandėliui. Užsakymo eilutės atmetimo teisė suteikiama naudojant teisę **Leisti atmesti užsakymą**. 

## <a name="order-fulfillment-operation-parameters"></a>Užsakymų įvykdymo operacijos parametrai

Užsakymo įvykdymas suteikia parengtus naudoti parametrus, kuriuos galima taikyti operacijai, kai jis iškviečiama elektroniniame kasos aparate. Jei parametras **Visi užsakymai** sukonfigūruotas, visi užsakymai rodomi, kai operacija yra naudojama. Parametras **Siųstini užsakymai** rodo tik užsakymus, kuriuos reikia siųsti iš parduotuvės, o **Paimtini užsakymai** rodo užsakymus, kurie bus paimti parduotuvėje. 

## <a name="orders-for-fulfillment"></a>Įvykdytini užsakymai

Užsakymų įvykdymo operacija rodo tik užsakymus, kurie paimti arba išsiųsti iš dabartinės parduotuvės. Kitose parduotuvėse įvykdytini užsakymai nepateikiami naudojant užsakymų įvykdymo operaciją. 

## <a name="line-selection"></a>Eilutės pasirinkimas

Eilutes galima pasirinkti naudojant veiksmų srities funkciją **Pasirinkti**. Kai funkcija **Pasirinkti** įjungta, galima pasirinkti kelias eilutes apdoroti. Pasirinktas eilutes galite išvalyti, tą pačią eilutę spustelėdami dar kartą. 

## <a name="line-details"></a>Eilutės informacija

Eilutės informacija galima rodyti naudojant informacijos iškeliamąjį meniu. Naudojant šį meniu, pateikiami trys skirtukai, kuriuose rodoma papildoma informacija apie pasirinktą eilutę. Pirmajame skirtuke **Eilutės informacija** rodoma informacija apie pačią eilutę, pvz., užsakytą ir likusį kiekį. Pateikiama papildoma informacija, įskaitant paimtą kiekį, supakuotą kiekį ir kiekį, už kurį SF išrašytos, taip pat pristatymo būdą ir pristatymo adresą. Skirtuke **Užsakymo informacija** pateikiama užsakymo antraštės informacija, įskaitant klientą, kliento ID, užsakymo numerį, bendrą užsakymo sumą ir likutį. Skirtuke **Atsargos** parodyta pasirinktos eilutės informacija apie faktinį turimą atsargų kiekį, rezervuotas atsargas ir užsakytas atsargas.

Pasirinkus kelias eilutes, užsakymo eilutės iškeliamasis meniu rodys tik tai, kad pasirinktos kelios eilutės. Norėdami rodyti vienos eilutės informaciją, išvalykite eilutes, kol liks tik viena eilutė. 

## <a name="pending-order-lines"></a>Laukiančios pardavimo eilutės

Bendrasis užsakymų įvykdymas apima galimybę neautomatiškai priimti užsakymus. Pagal numatytuosius parametrus parduotuvėje įvykdytini užsakymai jau yra priimti. Tačiau, jei atsižvelgiant į verslo procesus reikia, kad darbuotojas priimtų užsakymus parduotuvės lygiu, galima įjungti neautomatinį priėmimą mažmeninės prekybos parduotuvės lygiu. Norėdami įjungti užsakymų priėmimą, pasirinkite **Mažmeninė prekyba** > **Kanalai** > **Mažmeninės prekybos parduotuvės** > **Visos mažmeninės prekybos parduotuvės**. Atidarykite norimą parduotuvę ir skirtuke **Bendra** raskite paantraštę **Užsakymų įvykdymas**. Šioje paantraštėje yra parinktis **Neautomatinis priėmimas**, pagal numatytuosius parametrus nustatyta į parametrą **Ne**. Nustatant šią parinktį į parametrą **Taip** ir sinchronizuojant kanalų duomenų bazės keitimus, užsakymo eilutėms galima taikyti priėmimo procesą.

Darbuotojai, kuriems priskirta teisė **Leisti priimti užsakymą**, gali atidaryti užsakymų įvykdymą ir pasirinkti priimtinas eilutes. Kai eilutės priimtos, jų būsena pasikeičia iš **Laukiama** į **Priimta** ir galima tęsti likusį užsakymo įvykdymo procesą. Kai įjungta parinktis **Neautomatinis priėmimas**, užsakymai nebus apdoroti, kol jie nebus priimti. 

Parduotuvėje paimtinų užsakymų būsena niekada nebūna **Laukiama**. Taip yra todėl, kad būtų išvengta atvejų, kai klientas atvyksta į parduotuvę ir užsakymo eilutės negalima apdoroti, nes nėra darbuotojo, turinčio atitinkamą teisę.

## <a name="accepted-order-lines"></a>Priimtos užsakymo eilutės

Užsakymams, kurių eilučių būsena **Priimta**, galima taikyti likusį užsakymo įvykdymo procesą elektroniniame kasos aparate. Priėmus užsakymą visus likusius veiksmus galima taikyti užsakymo eilutei. 

Pvz., priimtą užsakymo eilutę galima pasirinkti ir tada paimti tiesiogiai, nevykdant paėmimo ir pakavimo procesų.

## <a name="line-actions"></a>Eilutės veiksmai

### <a name="pick"></a>Paimti

Veiksmų kategorija **Paėmimas** skirta užsakymo eilučių paėmimo iš lentynų procesui. Paėmimo veiksmą galima taikyti tik užsakymo eilutėms, kurios buvo priimtos anksčiau. 

**Veiksmas: paėmimas**

- Rodoma EKA būsena: Paėmimas
- Rodoma tarnybinio biuro būsena: Be keitimų

Priėmus užsakymą, eilutes galima pasirinkti ir priskirti joms žymę **Paėmimas**. Priskyrus eilutei žymę **Paėmimas** nurodoma, kad eilutės paėmimo darbas jau atliekamas. Taip dviems darbuotojams neleidžia vienu metu bandyti paimti tas pačias užsakymo eilutes.  

**Veiksmas: Spausdinti išrinkimo dokumentą**

- Rodoma būsena: Paėmimas
- Rodoma tarnybinio biuro būsena: Be keitimų

Išrinkimo dokumentus galima spausdinti elektroniniame kasos aparate ir padėti darbuotojams, vykdantiems paėmimo procesą. Atspausdintą išrinkimo dokumentą darbuotojas, atliekantis paėmimą, gali nešiotis su savimi, kai produktai paimami, ir pažymėti juos kaip paimtus išrinkimo dokumente. 

Išrinkimo dokumento formatas yra konfigūruotas „Dynamics 365 for Retail“ ir įtrauktas į kvito šabloną. Daugiau informacijos, kaip nustatyti kvitų šablonus, žr. [Kvitų šablonai ir spausdinimas](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/receipt-templates-printing).

Jei pasirenkamos eilutės ir išspausdinamas tų eilučių išrinkimo dokumentas, jos yra automatiškai atnaujinamos priskiriant būseną **Paėmimas**. 

**Veiksmas: Pažymėti kaip paimtą**

- Rodoma būsena: Paimta arba iš dalies paimta
- Rodoma tarnybinio biuro būsena: Paimta arba iš dalies paimta

Atliktus faktinį paėmimo procesą, eilutes galima pažymėti kaip **Paimta**. Pasirenkant eilutę ir pažymint ją kaip **Paimta** atliekamas realiojo laiko iškvietimas atnaujinti užsakymo eilutę „Dynamics 365 for Retail“. Kai eilutė pažymėta kaip **Paimta** elektroniniame kasos aparate, tarnybiniame biure rodoma būsena taip pat atnaujinama į **Paimta** ir atsargų operacijos nurodo, kad nurodytas kiekis buvo sumažintas.

Apdorojant užsakymus per tam tikrą laikotarpį galima apdoroti tam tikros eilutės dalinius kiekius. Jei pasirenkama eilutė ir atliekamas veiksmas **Pažymėti kaip paimta**, o kiekis yra didesnis nei vienas, vartotojas paraginamas nurodyti kiekį. Likęs paimtinas kiekis yra užpildomas automatiškai. Jei nurodomas mažesnis nei likęs kiekis, nustatoma eilutės būsena **Iš dalies paimta**. Atnaujinus užsakymo eilutę tarnybiniame biure, ji taip pat nurodo iš dalies paimtą būseną, o vartotojo įvestas kiekis naudojamas atsargoms atnaujinti. 

Jei užsakymo eilutė paimama per klaidą, užsakymo eilutės paėmimo atsisakymo procesas turi būti atliktas tarnybiniame biure. Šiuo metu paėmimo atsisakymo veiksmo negalima naudoti elektroniniame kasos aparate. 

Užsakymų eilutes iš skirtingų užsakymų galima pasirinkti ir priskirti žymę **Paėmimas**, išspausdintą tame pačiame išrinkimo dokumente, arba pažymėti kaip **Paimta**. 

### <a name="pack"></a>Pakuoti

Užsakymo eilutes galima supakuoti bet kada po to, kai užsakymo eilutė priimta. 

**Veiksmas: Spausdinti važtaraštį**

- Rodoma būsena: Supakuota arba iš dalies supakuota
- Rodoma tarnybinio biuro būsena: Pristatyta arba iš dalies pristatyta

Šiuo veiksmu eilutės pažymimos kaip supakuotos arba iš dalies supakuotos ir išspausdinamas važtaraštis. Važtaraštį galima išspausdinti norint patikrinti produktus, kurie buvo supakuoti kartu. Važtaraščio formatas yra konfigūruotas „Dynamics 365 for Retail“ ir įtrauktas į kvito šabloną. Daugiau informacijos, kaip nustatyti kvitų šablonus, žr. [Kvitų šablonai ir spausdinimas](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/receipt-templates-printing).

**Veiksmas: Pažymėti kaip supakuotą**

- Rodoma būsena: Supakuota arba iš dalies supakuota
- Rodoma tarnybinio biuro būsena: Pristatyta arba iš dalies pristatyta

Veiksmą **Pažymėti kaip supakuotą** galima naudoti norit nurodyti, kad eilutės supakuotos neatspausdinus važtaraščio. Atlikus bet kurį iš veiksmų **Spausdinti važtaraštį** ir **Pažymėti kaip supakuotą**, tarnybiniame biure bus sugeneruotos atsargų operacijos. Supakavus eilutes elektroniniame kasos aparate, tarnybiniame biure bus sugeneruoti važtaraščių žurnalai. 

Jei užsakymo eilutė supakuojama per klaidą, važtaraščių žurnalą reikia pataisyti tarnybiniame biure. 

Vienu metu galima pakuoti tik užsakymo eilutes, kurios priklauso tam pačiam užsakymui ir kurių pristatymo būdas toks pats.

Šiuo metu pasirinktis pažymėti parduotuvės paėmimo eilutes kaip **Supakuota** yra išjungta. Ši funkcija bus įtraukta į būsimą leidimą. Važtaraščio kūrimo procesas bus patobulintas, suteikiant galimybę įtraukti trečiosios šalies siuntimo informaciją į važtaraščio procesą.

### <a name="pick-up"></a>Paimti

Parduotuvėje paimtinus užsakymus galima tiesiogiai paimti, kai jie nuskaitomi elektroniniame kasos aparate. Parduotuvėje paimtinų užsakymų negalima priimti. 

**Veiksmas: Paimti**

- Rodoma būsena: SF išrašyta arba SF išrašyta iš dalies
- Rodoma tarnybinio biuro būsena: SF išrašyta arba SF išrašyta iš dalies

Pasirinkus eilutę paimti naudojant bendrąjį užsakymų įvykdymą, visas užsakymas įkeliamas į elektroninį kasos aparatą ir pažymimas visas pasirinktos eilutės kiekis. Kitos užsakymo eilutes taip pat įkeliamos į elektroninio kasos aparato operacijos rodinį, bet kiekis pažymimas kaip nulis. 

Įkėlus paimtinas eilutes į operacijos rodinį, operaciją galima apmokėti įprastai. 

Eilutės, kurių SF visiškai išrašyta paėmimo metu, nebebus rodomos bendrajame užsakymų apdorojime. Eilutės, kurios buvo iš dalies paimtos, bus toliau rodomos bendrajame užsakymų įvykdyme, kol jos bus visiškai paimtos. 

Jei eilutė paimama per klaidą, reikia ištaisyti klaidą ir atšaukti paėmimą.  

Vienu metu galima paimti tik užsakymo eilutes, kurios priklauso tam pačiam užsakymui ir kurių pristatymo būdas toks pats. 

### <a name="shipping"></a>Siuntimas

Užsakymo eilutėms, kurias reikia išsiųsti iš parduotuvės, galima taikyti bendrąjį užsakymų įvykdymą naudojant veiksmą **Siųsti**. Jei neautomatinis užsakymo eilutės priėmimas sukonfigūruotas kanalo lygiu, užsakymus reikia priimti prieš siunčiant. Priėmus užsakymo eilutę ir jos būseną pakeitus į **Laukiama** arba kitą būseną, eilutes galima siųsti. 

**Veiksmas: Siųsti**

- Rodoma būsena: SF išrašyta arba SF išrašyta iš dalies
- Rodoma tarnybinio biuro būsena: SF išrašyta arba SF išrašyta iš dalies

Eilučių, išsiųstų iš bendrojo užsakymų įvykdymo, SF išrašoma tarnybiniame biure, panašiai, kaip užsakymo SF išrašoma tiesiogiai iš tarnybinio biuro. Eilutės, siunčiamos iš bendrojo užsakymų įvykdymo, nėra įkeliamos į operacijos rodinį, be to, eilučių siuntimo metu mokėjimas neatliekamas. 

Užsakymo eilutės, kurios buvo visiškai išsiųstos, nebebus rodomi bendrajame užsakymų įvykdyme. Iš dalies išsiųstos eilutės bus toliau rodomos bendrajame užsakymų įvykdyme, kol jos bus visiškai išsiųstos. 

Vienu metu galima siųsti tik to paties užsakymo eilutes. Jei to paties užsakymo eilučių pristatymo būdai skiriasi, jas vis tiek galima pasirinkti siųsti vienu metu. 

### <a name="reject"></a>Atmesti

Eilutes arba dalines eilutes galima atmesti. Tai suteikia galimybę jas iš naujo priskirti tarnybiniam biurui arba kitai parduotuvei ar sandėliui. Eilutes galima atmesti tik jei jos dar nebuvo paimtos arba supakuotos. Norėdami atmesti eilutę, kuri jau buvo paimta arba supakuota, tarnybiniame biure reikia atmesti tos eilutės paėmimą arba supakavimą. 

**Veiksmas: Atmesti**

- Rodoma būsena: Atmesta
- Rodoma tarnybinio biuro būsena: Be keitimų 

Atmestas užsakymo eilutes galima peržiūrėti darbo srityje **Pardavimo užsakymo apdorojimas ir užklausa**. Išvalykite asmens filtrą darbo srityje, norėdami peržiūrėti visas atmestas užsakymo eilutes visose parduotuvėse. Skirtuke **Atmestos užsakymo eilutės**, dalyje **Užsakymai ir parankiniai**, rodoma užsakymo eilučių informaciją. Be to, vartotojai gali spustelėti mygtuką **Atmesti užsakymo eilutės**, pateiktą dalyje **Suvestinė**, kad atidarytų į pardavimo užsakymo rodinį. Jame rodomi visi užsakymai, kurių viena ar daugiau užsakymo eilučių atmestos. Jei įjungtas paskirstytas užsakymų valdymas (DOM), tada šie atmesti užsakymai bus automatiškai iš naujo priskirti atitinkamoms parduotuvėms įvykdyti, tačiau šias užsakymų eilutes taip pat galima priskirti iš naujo neautomatiškai. Norėdami tai padaryti, pasirinkite eilutę, kurios **Įvykdymo būsena** nustatyta kaip **Atmesta**, ir pagal poreikį pakeiskite vietovę / sandėlį. Spustelėkite išplečiamąjį meniu **Atnaujinti eilutę** ir spustelėkite **Iš naujo nustatyti įvykdymo būseną**, kad pakeistumėte įvykdymo būseną iš **Atmesta** į **Priimta** arba **Laukiama**, priklausomai nuo užsakymo įvykdymo nustatymo. Iš naujo nustačius įvykdymo būseną, parduotuvės darbuotojai galės peržiūrėti užsakymo eilutes EKA.

## <a name="line-quantity-tracking"></a>Eilutės kiekio sekimas

Vieną užsakymo eilutę, kurios kiekis yra didesnis už vieną, galima apdoroti per tam tikrą laiką, todėl užsakymo eilučių antrinės būsenos gali skirtis. Pavyzdžiui, jei gamintojas vykdo projektą, kuriame reikia 500 lentų, bet vykdydamas projektą gamintojas vienu metu paims arba pristatys tik po kelias lentas, tuo pačiu metu gali būtų kiekių, kurie yra paimami, pakuojami ir siunčiami. 

Bet kuriuo metu pasirinkus eilutę, likusi eilutės suma bus papildyta automatiškai, manant, kad likęs kiekis apdorojamas. Naudojant pirmiau pateiktą pavyzdį, jei 200 lentų jau yra paimtos ir lentų eilutė pasirenkama paimti, likęs kiekis (300) bus automatiškai papildytas. Tas pats galioja, jei SF jau išrašyta už 200 lentų. Tokiu atveju tik likęs kiekis bus papildytas automatiškai. 

Pasitelkiant tą patį pirmiau nurodytą pavyzdį, jei 200 lentų pažymėtos kaip supakuotos ir pasirenkamas siuntimas, visa suma (500) bus papildyta. Jei siunčiamos tik 200 lentų, sistema manys, kad anksčiau supakuotos lentos yra siunčiamos ir supakuotas kiekis bus sumažintas. Jei siunčiama 201 lenta, supakuotų lentų skaičius yra pirmiausia sumažinamas, o likusi viena lenta atimama iš likusio kiekio. 

## <a name="line-statuses"></a>Eilučių būsenos

Naudojamos kelios užsakymo eilučių būsenos elektroniniame kasos aparate, norint nurodyti užsakymo eilutės būseną. Būsenos elektroniniame kasos aparate ne visada atitinka tarnybiniame biure nurodytas būsenas. Užsakymo eilučių būsenas galima peržiūrėti elektroniniame kasos aparate naudojant užsakymų įvykdymo operacijas. Tarnybiniame biure užsakymo eilutes galima peržiūrėti užsakymo informacijoje. Užsakymo informaciją galima pasiekti pasirinkus **Mažmeninė prekyba** > **Klientai** > **Visi kliento užsakymai**. Pasirinkite **Užsakymo ID**, kad peržiūrėtumėte užsakymo informaciją. Užsakymo informacijoje pasirinkite skirtuką **Pardavimo užsakymas**, tada pasirinkite parinktį **Išsami būsena**, pateiktą paantraštėje **Rodinys**. 

**Laukiama** – peržiūrint elektroniniame kasos aparate užsakymo eilučių, kurios priskirtos parduotuvei, bet dar nėra priimtos, būsena yra **Laukiama**. Eilučių, laukiančių priėmimo elektroniniame kasos aparate, tarnybiniame biure rodoma būsena bus **Užsakymas apdorojamas**.

**Priimtina** – peržiūrint elektroniniame kasos aparate užsakymo eilučių, kurios buvo neautomatiškai arba automatiškai patvirtintos, būsena yra **Priimta**. Eilučių, kurių būsena **Priimta**, tarnybiniame biure rodoma būsena yra **Užsakymas apdorojamas**.

**Paėmimas** – eilučių, kurios šiuo metu paimamos parduotuvės lygiu, būsena yra **Paėmimas**. Tų pačių eilučių, peržiūrimų tarnybiniame biure, rodoma būsena yra **Užsakymas apdorojamas**.

**Paimta** ir **Iš dalies paimta** – eilučių, kurios buvo paimtos arba iš dalies paimtos, elektroniniame kasos aparate rodoma būsena yra **Paimta** arba **Iš dalies paimta**. Tų pačių eilučių, peržiūrimų tarnybiniame biure, rodoma būsena taip pat yra **Paimta** arba **Iš dalies paimta**.

**Supakuota** ir **Iš dalies supakuota** – eilučių, kurios buvo supakuotos arba iš dalies supakuotos, elektroniniame kasos aparate rodoma būsena yra **Supakuota** arba **Iš dalies supakuota**. Tų pačių eilučių, peržiūrimų tarnybiniame biure, rodoma būsena taip pat yra **Pristatyta** arba **Iš dalies pristatyta**.

**Iš dalies išrašyta SF** – eilučių, kurios buvo iš dalies paimtos arba iš dalies išsiųstos, elektroniniame kasos aparate ir tarnybiniame biure rodoma būsena yra **Iš dalies išrašyta SF**.

**SF išrašyta** – eilutės, kurių SF visiškai išrašyta, elektroniniame kasos aparate nebebus rodomos kaip vykdytinos. Tarnybiniame biure tų eilučių rodoma būsena yra **SF išrašyta**.

## <a name="order-fulfillment-filtering"></a>Užsakymų įvykdymo filtravimas

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

