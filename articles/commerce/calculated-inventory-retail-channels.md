---
title: Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas
description: Šioje temoje aprašoma, kaip įmonė gali naudoti „Microsoft Dynamics 365 Commerce“, kad galėtų peržiūrėti įvertintą produktų pasiūlą internetinių ir fizinių parduotuvių kanaluose.
author: hhainesms
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 1b1e0ea264dd74f6583d3b7fd3ecce551c73fbae
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674680"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip įmonė gali naudoti „Microsoft Dynamics 365 Commerce“, kad galėtų peržiūrėti įvertintą produktų pasiūlą internetinių ir fizinių parduotuvių kanaluose.

## <a name="accuracy-of-inventory-availability"></a>Atsargų pasiekiamumo tikslumas

„Commerce“ naudoja keletą serverių ir duomenų bazių, kad būtų užtikrintas išplečiamumas ir efektyvumas. Todėl svarbu suprasti, kad turimos atsargų vertės, teikiamos per elektroninio kasos aparato (EKA) programą, elektroninės prekybos atsargų pasiekiamumo programų sąsajas (API) ir turimų atsargų puslapius „Commerce Headquarters“, realiu laiku negali būti 100 proc. tikslios. Jeigu operacijos, sukurtos interneto ar fizinės parduotuvės kanalo produktams, dar nebuvo sinchronizuotos su štabo serveriu ir duomenų baze, turimų atsargų štabo gali nebūti rodoma tiksli šių produktų realaus laiko atsargų vertė. Ir atvirkščiai, jei sukonfigūravote savo įmonę taip, kad štabo kitos integruotos programos vartotojai galėtų parduoti, gauti, grąžinti ar kitaip koreguoti atsargas iš parduotuvės ar internetinio sandėlio, EKA arba interneto kanalas gali neturėti visos informacijos, kurios reikia norint rodyti tikslią atsargų vertes realiu laiku.

Tačiau svarbu suprasti, kad visi turimi atsargų prieinamumo duomenys, pateikiami per visą darbo dieną, yra laikomi numatoma verte. Todėl, jei bandysite palyginti turimų atsargų informaciją, kurią pateikia programa, su faktinėmis fizinėmis atsargomis lentynose, arba jei bandysite lyginti turimų atsargų vertes, kurios rodomos EKA, su turimais duomenimis, kuriuos galite rasti štabą tame pačiame sandėlyje, vertės gali skirtis. Tokio skirtum per darbo dieną reikia tikėtis ir jis neturėtų būti laikomas problema. Jei norite patikrinti duomenis ir įsitikinti, kad vertės, pateiktos atsargų pasiekiamumo EKA ir štabas, atitinka faktinius fizinius vienetus, kuriuos matote parduotuvėje arba sandėlio lentynose, geriausia, kad tai būtų daroma, kai tos dienos kanalo operacijos nebevykdomos ir visos operacijos buvo tinkamai sinchronizuotos tarp štabo ir kanalo.

## <a name="channel-side-inventory-calculation"></a>Kanalo atsargų skaičiavimas

Kanalo atsargų skaičiavimas yra mechanizmas, kuris „Commerce Headquarters" laiko paskutinių žinomus kanalo atsargų duomenis ir lemia papildomus atsargų pokyčius, atliktus kanalo pusėje, kurios neįtrauktos į tą pradinį kanalą, kad būtų apskaičiuotos beveik realiuoju laiku įvertintos turimos atsargos. 

Šios atsargų pakeitimai šiuo metu yra atsižvelgiama į kanalo atsargų skaičiavimo logiką:

- Atsargos, parduotos parduotuvėse vykdant grynųjų pinigų ir perkėlimo užsakymus
- Atsargos, parduotos per kliento užsakymus parduotuvės arba interneto kanale
- Atsargos grąžintos į parduotuvę
- Atsargos įvykdytos (paėmimas, pakuotė, laivas) iš parduotuvės sandėlio

Norėdami naudoti kanalo atsargų skaičiavimą, turite įgalinti **optimizuoto produkto prieinamumo skaičiavimo** funkciją.

Jei jūsų „Commerce" aplinkoje yra **nuo 10.0.8 iki 10.0.11** atlikite šiuos veiksmus.

1. „Commerce“ štabe eikite į **Mažmeninė prekyba ir prekyba** \> **„Commerce“ bendrinti parametrai**.
1. Skirtuke **Atsargos**, dalyje **Produkto pasiekiamumo užduotis**, laukelyje pasirinkite **Naudoti optimizuotą produkto pasiekiamumo užduoties procesą**.

Jei jūsų „Commerce" aplinkoje yra **nuo 10.0.12 ar vėlesnės** atlikite šiuos veiksmus.

1. „Commerce“ štabe eikite į **Darbo aplinka \> Funkcijų valdymas** ir įjunkite **Optimizuoto produkto prieinamumo skaičiavimo** funkciją.
1. Jei jūsų interneto ir parduotuvės kanalai naudoja tuos pačius įvykdymo sandėlius, taip pat turite įgalinti patobulintos el. komercijos kanale **esančių atsargų skaičiavimo logikos** funkciją. Taip, kanalo pusės skaičiavimo logika nagrinės neužregistruotas operacijas, kurios sukuriamos parduotuvės kanale. (Šios operacijos gali būti grynųjų pinigų ir carry operacijos, klientų užsakymai ir grąžinimai.)
1. Vykdykite **1070** (**Kanalo konfigūracija**) užduotį.

Jei „Commerce" aplinka buvo atnaujinta iš ankstesnės nei „Commerce" versija 10.0.8, įjungę funkciją **Optimizuotas produkto pasiekiamumas** funkcija, taip pat turite vykdyti **Pradėti prekybos tvarkaraštį** tam, kad funkcija būtų taikoma. Norėdami vykdyti pradžią, eikite į **Prekyba ir komercija** \> **Būstinės sąranka** \> **Prekybos planuoklė**.

Norint naudoti kanalo atsargų skaičiavimą, kaip būtinąsias sąlygas į kanalo duomenų bazes turi būti siunčiamas periodinis atsargų duomenų vaizdas iš būstinės, kurią sukūrė produkto prieinamumo **užduotis**. Momentinė kopija rodo informaciją, kurią štabus turi apie atsargų pasiekiamumą pagal tam tikrą produktą arba produkto variantą ir sandėlį. Ji apima tik atsargų operacijas, kurios buvo apdorotos ir užregistruotos būstinėje tuo metu, kai buvo paimta momentinė kopija, ir ji gali būti ne 100 procentų tiksli realiuoju laiku dėl pastovaus pardavimo apdorojimo, vykstainio paskirstytuose serveriuose.

- Jei produkto atsargos buvo parduotos parduotuvės sandėlyje naudojant kasos aparatą arba nesinchronizuojamo kliento užsakymo pardavimo EKA programoje režimą, štabas karto neturės informacijos apie susijusią pardavimo atsargų išdavimo operaciją. Štave bus informacijos apie atsargas, parduotas tokio parduotuvės pardavimo būdu, tik po to, kai P užduotis įkels susijusią operaciją iš parduotuvės kanalo duomenų bazės į štabą ir bus sukurtas susijęs pardavimo užsakymas naudojant išrašo registravimą arba duomenų perdavimo mažais kiekiais registravimo procesą. Štabo užsakymo kūrimo procesas sukuria susijusias atsargų operacijas. 
- El. prekybos kanalo užsakymų atveju štabas turi informacijos apie atsargų operacijas tik po to, kai operacijos nusiunčiamos į štabų naudojant P užduotį ir užbaigiamas užsakymų sinchronizavimo procesas.

Norėdami padaryti „Commerce Headquarters“ atsargų momentinę kopiją atlikite šiuos veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> „Retail“ ir „Commerce“ IT \> Produktai ir atsargos \> Produkto pasiekiamumas**.
1. Pasirinkite **Gerai**, jei norite vykdyti užduotį **Produkto pasiekiamumas**. Taip pat galite suplanuoti šią užduotį, kad ji būtų paleista pakete.

Pasibaigus užduoties **Produkto pasiekiamumas** vykdymui, užfiksuoti duomenys turi būti perduoti į el. prekybos kanalo duomenų bazes, kad skaičiuojant turimas atsargas būtų galima atsižvelgti į naujausias štabo momentines kopijas.

Norėdami sinchronizuoti momentinės kopijos duomenis iš būstinės į savo kanalų duomenų bazes, atlikite šiuos veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**.
1. Paleiskite užduotį **1130** (**Produkto pasiekiamumas**), norėdami sinchronizuoti momentinės kopijos, kurią užduotis **Produkto pasiekiamumas** sukūrė iš štabą, duomenis su kanalų duomenų bazėmis.

## <a name="inventory-availability-apis-for-e-commerce"></a>Atsargų prieinamumo API el. prekybai

„Commerce" pateikia toliau nurodytus el. komercijos scenarijų API, siekiant pateikti užklausą dėl produkto atsargų prieinamumo:

- **GetEstimatedAvailability – naudokite šią API, norėdami pateikti užklausą dėl produkto arba produkto varianto interneto kanalo sandėlyje ar sandėliuose, kurie susieti su interneto kanalo** įvykdymo grupe.
- **GetEstimatedProductWarehouseAvailability** – naudokite šią API, norėdami užklausti, kiek prekės produkto ar jo varianto yra konkrečiame sandėlyje.

> [!NOTE]
> Šie APIs pakeičia **GetProductAvailabilities** ir **GetAvailableInventoryNearby** API „Commerce“ versijoje 10.0.7 ir ankstesnėse.

Abi API vidiniai naudoja kanalo pusės skaičiavimo logiką ir grąžina įvertintą faktiškai turimą kiekį, bendrą turimus kiekius, **matavimo** **vienetą** **(UoM)** **ir** pageidaujamo produkto bei sandėlio atsargų lygį. Grąžinamos gali būti rodomos jūsų elektroninės prekybos svetainėje, jei norite, arba jos gali būti naudojamos kitoms verslo logikoms suaktyvinti elektroninės prekybos svetainėje. Pavyzdžiui, galite neleisti pirkti produktų, kurių atsargų lygis „nėra atsargose".

Nors kitos „Commerce“ serveryje esančios API gali patekti tiesiai į štabo, kad galėtų gauti turimų produktų atsargų kiekius, nerekomenduojame jų naudoti elektroninės prekybos aplinkoje dėl galimų našumo problemų ir susijusio poveikio, kurį šios dažnos užklausos gali turėti jūsų štabo serveriuose. Be to, kartu su kanalo skaičiavimu du pirmiau nurodyti API gali pateikti tikslesnį produkto prieinamumo įvertinimą, atsižvelgdami į kanaluose sukurtas operacijas, kurių būstinė dar nežinoma.

Norėdami nurodyti, kaip produktų kiekis turi būti grąžintas API išeiga, atlikite šiuos veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Parametrai \> Prekybos parametrai**.
1. Pasirinkite skirtuką Atsargos ir tada el. komercijos „FastTab" atsargų prieinamumo API sukonfigūruokite kiekio vertę **API** **išeigos** **parametre**.
1. Vykdykite paskirstymo grafiko užduotį **1070** (**Kanalo konfigūracija**), kad sinchronizuotumėte naujausius nustatymus kanaluose.

**API išeigos** parametrų kiekis pateikia tris pasirinktis:

- **Grąžinti atsargų kiekį** - faktinis turimas ir bendras turimas pageidaujamo produkto kiekis grąžinamas į API išeigą.
- **Grąžinamų atsargų kiekio, atimamo atsargų buferį, buferis** – API išeiga grąžintas kiekis koreguojamas atėmus atsargų buferio vertę. Daugiau informacijos apie atsargų buferį ieškokite Konfigūruoti [atsargų buferius ir atsargų lygius](inventory-buffers-levels.md).
- **Negrąžinti atsargų kiekio** – API išeigai grąžinamas tik atsargų lygis. Daugiau informacijos apie atsargų lygius ieškokite Konfigūruoti [atsargų buferius ir atsargų lygius](inventory-buffers-levels.md).

API parametrą `QuantityUnitTypeValue` galite naudoti vieneto tipui, kuriuo API turėtų būti naudojamas grąžinamas kiekis, nurodyti. Šis parametras palaiko **atsargų vienetą** (numatytąjį), **pirkimo vienetą ir pardavimo** **vieneto** pasirinktis. Grąžintas kiekis apvalinamas iki nustatyto atitinkamos matavimo vieneto (mat. vnt.) valdymo vieneto tikslumo.

**GetEstimatedAvailability** API siūlo šiuos įvesties parametrus, kurie palaiko skirtingus užklausų scenarijus:

- `DefaultWarehouseOnly` – naudoti šį parametrą norint pateikti užklausą dėl produkto atsargų interneto kanalo numatytame sandėlyje. 
- `FilterByChannelFulfillmentGroup` ir `SearchArea` – naudoti šiuos du parametrus norint pateikti užklausą dėl produkto atsargų iš visų paėmimo vietų, esančių tam tikroje ieškos srityje, pagal `longitude` ir `latitude`, `radius`. 
- `FilterByChannelFulfillmentGroup` ir `DeliveryModeTypeFilterValue` – naudoti šiuos du parametrus norint pateikti užklausą dėl konkrečių sandėlių, kurie susieti su interneto kanalo įvykdymo grupe produkto atsargomis ir kurie sukonfigūruoti palaikyti tam tikrus pristatymo būdus. Parametras `DeliveryModeTypeFilterValue`palaiko **visas** (numatytąsias), **siuntimo ir** **paėmimo** pasirinktis. Pavyzdžiui, scenarijuje, kai užsakymas tinkle gali būti įvykdytas iš kelių siuntimo sandėlių, galite naudoti šiuos du parametrus, norėdami pateikti užklausą dėl produkto atsargų prieinamumo visuose siuntimo sandėliuose. API šiuo atveju grąžina kiekvieno siuntimo sandėlio turimo produkto kiekį ir atsargų lygį, pridėjus sudėtinį kiekį ir agreguotas visų siuntimo sandėlių, esančių užklausos aprėnyje, atsargų lygį.
 
„Commerce buy box", parduotuvės išrinkiklis, pageidavimų sąrašas, krepšelis ir krepšelio piktogramų moduliai naudoja anksčiau paminėtos API ir parametrus, kad būtų rodomi atsargų lygio pranešimai el. komercijos svetainėje. „Commerce" svetainės generatoriuje pateikiami įvairūs atsargų parametrai, leidžiantys valdyti reklamavimo ir pirkimo elgseną. Daugiau informacijos žr. [Atsargų parametrų taikymas](inventory-settings.md).

## <a name="pos-inventory-lookup-with-channel-side-calculation"></a>EKA atsargų peržvalga naudojant kanalo skaičiavimą

„Commerce“ leidime 10.0.9 ir ankstesnėse versijose EKA operacija **Atsargų peržvalga** naudojo paslaugos realiu laiku iškvietą į štabe, kad gautų pasirinkto produkto atsargų informaciją tiek iš dabartinės vartotojo parduotuvės, tiek iš visų kitų parduotuvių, kurios sukonfigūruotos vykdymo grupėje kaip parduotuvės kanalo konfigūracijos dalis. Naudojant „Commerce“ leidime 10.0.10" ir vėliau galima išjungti „Commerce“ leidime 10.0.10 ir vėliau galima išjungti „Commerce“ leidime 10.0.10 paslaugos iškleidimą į būstines ir vietoj to naudoti kanalo skaičiavimą „Commerce" serveryje, kad nustatytumėte turimas atsargas, kurios faktiškai galimos parduotuvei ir bet kokioms kitoms vietų, apibrėžtų įvykdymo grupėje. Ši kanalo apskaičiuotų atsargų konfigūracija taip pat naudinga vietose, kur interneto ryšys yra nepatikimas, nes jums nereikia būti prisijungus prie interneto, kad galėtumėte gauti atsargų peržvalgas iš štabo.

Kai kanalo skaičiavimas tinkamai sukonfigūruotas ir valdomas, jis gali teikti patikimesnį dabartinių parduotuvės atsargų įvertinimą, nes jis naudoja transakcijų duomenis, kurie yra komercijos kanalo duomenų bazėje, tačiau apie kuriuos štabas dar gali neturėti informacijos. Pvz., jei naudojate esamą atsargų peržvalgų EKA paslaugos realiu laiku iškvietą, štabas tikriausiai dar nebus informacijos apie produkto pardavimą už grynuosius pinigus, kuris ką tik buvo įvykdytas. Todėl produkto turimų atsargų vertė, kurią pateikia štabas, veikiausiai viršys faktines parduotuvės turimas atsargas pagal vieną vienetą. Tačiau, jei naudojate kanalo skaičiavimą, pardavimas už grynuosius pinigus gali būti įtrauktas į skaičiavimą ir atimtas iš turimų atsargų vertės, kuri rodoma. Nors vertės, kurias teikia ir kanalų skaičiavimas, ir paslaugos realiu laiku iškvieta yra tik turimų atsargų įvertinimas, vertė, kurią pateikia kanalo skaičiavimas, yra daug labiau tikėtina, kad yra tiksli dabartinėje parduotuvėje.

Norėdami konfigūruoti EKA **Atsargų peržvalgos** operaciją „Commerce” štabe, kad galėtumėte naudoti kanalo pusės apskaičiavimo logiką ir išjungti realaus laiko paslaugų skambučius, pirmiausia turite įjungti **Optimizuoto produkto prieinamumo skaičiavimo** funkciją per **Funkcijų valdymo** darbo sritį „Commerce” štabe, o tada atlikti šiuos veiksmus.

1. Eikite į **Mažmeninį prekyba ir komercija \> Kanalo sąranka \> EKA sąranka \> EKA profiliai \> Funkcionalumo profiliai**.
1. Pasirinkite funkcijų šabloną.
1. „FastTab“ **Funkcijos**, skyriuje **Atsargų pasiekiamumo skaičiavimas**, pakeiskite lauko **Atsargų pasiekiamumo skaičiavimo būdas** vertę iš **Paslauga realiu laiku** į **Kanalas**. Pagal numatytuosius parametrus visi funkcijų profiliai naudoja paslaugos realiu laiku iškvietimus. Todėl, jei norite naudoti kanalo skaičiavimo logiką, turite pakeisti šio lauko vertę. Atlikus šį pakeitimą bus paveiktos visos mažmeninės prekybos parduotuvės, kurios yra susijusios su pasirinktu funkcijų šablonu.

Tada turite sinchronizuoti kanalų keitimus naudodami paskirstymo grafiko procesą štabe ir atlikdami tolesnius veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**.
1. Vykdykite **1070** (**Kanalo konfigūracija**) užduotį.

Baigus konfigūruoti, informacijoje, kuri pateikiama apie faktiškai turimas atsargas, nebenaudojama paslaugos realiu laiku iškvieta, kai EKA programos vartotojas naudoja operaciją **Atsargų peržvalga** (standartiniai ir matricos rodiniai). Vietoje to duomenys apie tos parduotuvės ir visų vykdymo grupės parduotuvių faktiškai turimas atsargas apskaičiuojami pagal paskutinę žinomą momentinę kopiją, kuri buvo pristatyta į kanalo duomenų bazę iš „Commerce Headquarters“. Momentinės kopijos vertę detalizuoja kanalo skaičiavimas, kad būtų pakoreguota faktiškai turimų atsargų vertė remiantis pasirinkto produkto papildomomis pardavimo arba grąžinimo operacijomis, kurios yra kanalo duomenų bazėje, tačiau kurios nebuvo įtrauktos į paskutinę sinchronizuotą momentinę kopiją iš 1130 užduoties. Jeigu kanalo duomenų bazėje nėra operacijų duomenų iš sandėlių ar parduotuvių, esančių vykdymo grupėje, joje nėra jokių papildomų operacijų, kurias būtų galima įtraukti perskaičiuojant vertę. Todėl geriausias šių sandėlių ar parduotuvių turimų atsargų įvertinimas yra paskutinės žinomos „Commerce Headquarters“ momentinės kopijos duomenys.

EKA **Užsakymo vykdymas** ekranai taip pat įvertina kanalo skaičiavimą, kad parodytų turimas prekių atsargas, kai pasirenkama užsakymo vykdymo eilutė, o vartotojas peržiūri skydelį **Informacija**, skirtą pasirinktai prekei.

## <a name="optimize-your-inventory-data"></a>Optimizuokite atsargų duomenis

Norint užtikrinti, kad atsargos būtų įvertintos kuo tiksliau, svarbu naudoti šias „Commerce“ paketines užduotis ir dažnai jas paleisti:

- **P-užduotis** – P užduotis yra puslapyje **Paskirstymo grafikai** ir turi būti vykdoma dažnai. Ši užduotis pateikia el. prekybos užsakymus, asinchroninius kliento užsakymus, kuriuos sukūrė EKA, ir grynųjų pinigų užsakymus, kuriuos EKA sukūrė iš kanalo duomenų bazių, į „Commerce Headquarters“, kad juos būtų galima apdoroti vėliau. Kol šie duomenys sinchronizuojami iš kanalo į „Commerce Headquarters", „Commerce Headquarters" neturi informacijos apie produktų, esančių sandėliuose, kurie susiję su šiomis operacijomis, atsargų koregavimus.
- **Sinchronizuoti užsakymus** – ši užduotis apdoroja neapdorotus operacijų duomenis „Commerce Headquarters“, kuriuos P užduotis teikia ir konvertuoja el. prekybos bei asinchronines kliento užsakymų operacijas į „Commerce Headquarters“ pardavimo užsakymus. Kol bus apdorota ši užduotis ir sukurti pardavimo užsakymai, nebus sukurtos jokios atsargų operacijos. Todėl „Commerce Headquarters“ turimose atsargose neatsispindės operacijos.
- **Atlikti operacijų išrašų paketinį skaičiavimą** – grynųjų pinigų operacijų, kurios sukurtos parduotuvėje, atveju duomenų perdavimo mažais kiekiais registravimo procesas užtikrina, kad su pardavimu susiję atsargų procesai bus veiksmingai atnaujinami. Norėdami pasiekti efektyviausią užsakymų už grynuosius pinigus atsargų operacijų apdorojimą įsitikinkite, kad sukonfigūravote savo sistemą naudoti [duomenų perdavimo mažais kiekiais registravimas](./trickle-feed.md).
- **Atlikti operacijų išrašų paketinį registravimą** – ši užduotis taip pat reikalinga duomenų perdavimo mažais kiekiais registravimui. Po jos eina užduotis **Atlikti operacijų išrašų paketinį skaičiavimą**. Ši užduotis sistemingai registruoja apskaičiuotas sumas, kad „Commerce Headquarters“ būtų sukurti pardavimo už grynuosius pinigus pardavimo užsakymai ir „Commerce Headquarters“ tiksliau atspindėtų parduotuvės atsargas.
- **Produkto pasiekiamumas** – šia užduotimi sukuriama atsargų, esančių „Commerce Headquarters“, momentinė kopija.
- **1130 (produkto pasiekiamumas)** – ši užduotis randama puslapyje **Paskirstymo grafikai** ir turi būti vykdoma iškart po užduoties **Produkto pasiekiamumas**. Ši užduotis perkelia atsargų momentinės kopijos duomenis iš „Commerce Headquarters“ į kanalų duomenų bazes.

> [!NOTE]
> - Bendrai, geriausia praktika būtų vykdyti produkto **prieinamumą** ir **1130** darbus pagal valandas ir suplanuoti P-darbo sinchronizavimo užsakymus bei sumažinti su srauto talpinimu susijusius darbus tuo pačiu ar didesniu dažnumu.
> - Dėl našumo priežasčių, kai kanalo atsargų pasiekiamumo skaičiavimai naudojami atsargų pasiekiamumo užklausai įvykdyti naudojant el. prekybos API arba naują EKA kanalo atsargų logiką, skaičiuojant naudojama talpykla, kad būtų nustatyta, ar praėjo pakankamai laiko, kad būtų protinga skaičiavimo logiką vykdyti dar kartą. Numatytoji talpykla nustatyta kaip 60 sekundžių. Pavyzdžiui, jūs įjungėte kanalo skaičiavimą savo parduotuvei ir peržiūrėjote turimas produkto atsargas puslapyje **Atsargų peržvalga**. Jei tada vienas produkto vienetas parduodamas, puslapyje **Atsargų peržvalga** nebus rodomos sumažėjusios atsargos, kol talpykla nebus išvalyta. Po to, kai vartotojai užregistruos operacijas EKA, turi praeiti 60 sekundžių, kad būtų matomas turimų atsargų sumažėjimas.

Jei pagal jūsų verslo scenarijų reikia trumpesnio talpyklos laiko, pagalbos kreipkitės į savo produktų palaikymo tarnybos atstovą.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
