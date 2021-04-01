---
title: Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas
description: Šioje temoje aprašomos parinktys, kurias galima naudoti, kad būtų rodomos parduotuvės ir interneto kanalų turimos atsargos.
author: hhainesms
manager: annbe
ms.date: 08/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: ff60ef23c7e19e3f2f97d56fd416e0018a0c324d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213263"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip įmonė gali naudoti „Microsoft Dynamics 365 Commerce“, kad galėtų peržiūrėti įvertintą produktų pasiūlą internetinių ir fizinių parduotuvių kanaluose.

## <a name="accuracy-of-calculation"></a>Apskaičiavimo tikslumas

„Commerce“ naudoja keletą serverių ir duomenų bazių, kad būtų užtikrintas išplečiamumas ir efektyvumas. Todėl svarbu suprasti, kad turimos atsargų vertės, teikiamos per elektroninio kasos aparato (EKA) programą, elektroninės prekybos atsargų pasiekiamumo programų sąsajas (API) ir turimų atsargų puslapius „Commerce Headquarters“, realiu laiku negali būti 100 proc. tikslios. Jeigu operacijos, sukurtos interneto ar fizinės parduotuvės kanalo produktams, dar nebuvo sinchronizuotos su „Commerce Headquarters“ serveriu ir duomenų baze, turimų atsargų puslapiuose „Commerce Headquarters“ gali nebūti rodoma tiksli šių produktų realaus laiko atsargų vertė. Ir atvirkščiai, jei sukonfigūravote savo įmonę taip, kad „Commerce Headquarters“ ar kitos integruotos programos vartotojai galėtų parduoti, gauti, grąžinti ar kitaip koreguoti atsargas iš parduotuvės ar internetinio sandėlio, EKA arba interneto kanalas gali neturėti visos informacijos, kurios reikia norint rodyti tikslią atsargų vertę realiu laiku.

Šioje temoje paaiškinami duomenų sinchronizavimo procesai, kuriuos galima dažnai paleisti, norint mažinti duomenų tarp programų ar kanalų vėlavimą. Tačiau svarbu suprasti, kad visi turimi atsargų prieinamumo duomenys, pateikiami per visą darbo dieną, yra laikomi numatoma verte. Todėl, jei bandysite palyginti turimų atsargų informaciją, kurią pateikia programa, su faktinėmis fizinėmis atsargomis lentynose, arba jei bandysite lyginti turimų atsargų vertes, kurios rodomos EKA, su turimais duomenimis, kuriuos galite rasti „Commerce Headquarters“ tame pačiame sandėlyje, vertės gali skirtis. Tokio skirtum per darbo dieną reikia tikėtis ir jis neturėtų būti laikomas problema. Jei norite patikrinti duomenis ir įsitikinti, kad vertės, pateiktos atsargų pasiekiamumo API ir „Commerce Headquarters“, atitinka faktinius fizinius vienetus, kuriuos matote parduotuvėje arba sandėlio lentynose, geriausia, kad tai būtų daroma, kai tos dienos kanalo operacijos nebevykdomos ir visos operacijos buvo tinkamai sinchronizuotos tarp „Commerce Headquarters“ ir kanalo.

## <a name="use-inventory-lookup-apis-for-e-commerce-inventory-availability-requests"></a>Naudokite atsargų peržvalgos API elektroninės prekybos atsargų turimumo užklausoms

Galite naudoti šias API, kad būtų rodoma, kirk yra produkto atsargų, kai jūsų klientai apsiperka el. prekybos svetainėje.

- **Gautiapskaičiuotąprieinamumą** – Naudokite šią API tam, kad gautumėte atsargų prieinamumą prekei el. prekybos kanalo sandėlyje ir visuose sandėliuose, kurie yra susieti su el. prekybos kanalo įgyvendinimo grupių konfigūravimu. Ši API taip pat gali būti naudojama sandėliams, esantiems konkrečioje ieškos srityje arba konkrečiu spinduliu, remiantis ilgumos ir platumos duomenimis.
- **GetEstimatedProductWarehouseAvailability** – naudokite šią API, norėdami užklausti, kiek prekės atsargų yra konkrečiame sandėlyje. Pavyzdžiui, galite naudoti ją, kad būtų rodomas atsargų pasiekiamumas scenarijuose, į kuriuos įtrauktas užsakymo paėmimas.

> [!NOTE]
> Šios API pakeičia **GetProductAvailabilities** ir **GetAvailableInventoryNearby** API, esančias „Dynamics 365 Retail“ 10.0.7 ir ankstesnėse versijose.

Abi šios API teikia duomenis iš „Commerce Server“ ir nurodo tam tikro produkto ar produkto varianto ir sandėlio turimų atsargų įvertinimą. Nors kitos „Commerce“ serveryje esančios API gali patekti tiesiai į „Commerce Headquarters“, kad galėtų gauti turimų produktų atsargų kiekius, nerekomenduojame jų naudoti elektroninės prekybos aplinkoje dėl galimų našumo problemų ir susijusio poveikio, kurį šios dažnos užklausos gali turėti jūsų „Commerce Headquarters“ serveriuose. Be to, jei turimos atsargos skaičiuojamos per „Commerce“ serverį, labai tikėtina, kad skaičiuojant bus įtrauktos atsargos, kurios buvo parduotos pastarųjų el. prekybos operacijų metu, kurios dar nesinchronizuotos su „Commerce Headquarters“. Nors „Commerce Headquarters“ gali nebūti informacijos apie šias operacijas, „Commerce“ serveryje ir kanalo duomenų bazėje duomenys yra. Todėl į duomenys bus atsižvelgta ir jie padės tiksliau įvertinti turimas produkto atsargas.

### <a name="get-started-with-e-commerce-calculated-inventory-availability"></a>Pradėkite naudoti el. prekybos apskaičiuotą atsargų pasiekiamumą

Prieš jums naudojant abi anksčiau paminėtas API programas, turite išjungti realaus laiko paslaugų skambučius atsargų paieškai iš POS programos, pirmiausia turite įjungti **Optimizuoto produkto prieinamumo skaičiavimo** funkciją per **Funkcijų valdymo** darbo sritį komercijos štabe.

Kad API galėtų tiksliai apskaičiuoti prekės atsargų pasiekiamumą, „Commerce Headquarters“ turi būti padaryta momentinė turimų atsargų kopija ir nusiųsta į kanalo duomenų bazę, kurią naudoja el. prekybos „Commerce Scale Unit“. Momentinė kopija rodo informaciją, kurią „Commerce Headquarters“ turi apie atsargų pasiekiamumą pagal tam tikrą produktą arba produkto variantą ir sandėlį. Joje gali būti ir atsargų koregavimai arba perkėlimai, kuriuos sukėlė atsargų gavimai, siuntimai arba kiti procesai, atlikti „Commerce Headquarters“ ir žinomi el. prekybos kanalui tik dėl sinchronizavimo proceso.

Duomenų bazės momentinė kopija, kurią sukuria užduotis **Produkto pasiekiamumas**, apskaičiuoja tik tas atsargų operacijas, kurios buvo apdorotos ir užregistruotos „Commerce Headquarters“ tuo metu, kai buvo padaryta momentinė kopija. Jei produkto atsargos buvo parduotos parduotuvės sandėlyje naudojant kasos aparatą arba nesinchronizuojamo kliento užsakymo pardavimo EKA programoje režimą, „Commerce Headquarters“ iš karto neturės informacijos apie susijusią pardavimo atsargų išdavimo operaciją. Jame bus informacijos apie atsargas, parduotas tokio parduotuvės pardavimo būdu, tik po to, kai P užduotis įkels susijusią operaciją iš parduotuvės kanalo duomenų bazės į „Commerce Headquarters“ ir bus sukurtas susijęs pardavimo užsakymas naudojant išrašo registravimą arba duomenų perdavimo mažais kiekiais registravimo procesą. „Commerce Headquarters“ užsakymo kūrimo procesas sukuria susijusias atsargų operacijas. El. prekybos kanalo užsakymų atveju „Commerce Headquarters“ turi informacijos apie atsargų operacijas tik po to, kai operacijos nusiunčiamos į „Commerce Headquarters“ naudojant P užduotį ir užbaigiamas užsakymų sinchronizavimo procesas. Todėl svarbu, kad jūs suprastumėte, jog atsargų momentinės kopijos reikšmė, kuri pateikiama užduotyje **Produkto pasiekiamumas**, negali būti 100 procentų tiksli realiu laiku, nes nuolatinis pardavimas vyksta per įvairius serverius.

Norėdami padaryti „Commerce Headquarters“ atsargų momentinę kopiją atlikite šiuos veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> „Retail“ ir „Commerce“ IT \> Produktai ir atsargos \> Produkto pasiekiamumas**.
1. Pasirinkite **Gerai**, jei norite vykdyti užduotį **Produkto pasiekiamumas**. Taip pat galite suplanuoti šią užduotį, kad ji būtų paleista pakete.

Pasibaigus užduoties **Produkto pasiekiamumas** vykdymui, užfiksuoti duomenys turi būti perduoti į el. prekybos kanalo duomenų bazes, kad skaičiuojant turimas atsargas būtų galima atsižvelgti į naujausias „Commerce Headquarters“ atsargų momentines kopijas.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**.
1. Paleiskite užduotį **1130** (**Produkto pasiekiamumas**), norėdami sinchronizuoti momentinės kopijos, kurią užduotis **Produkto pasiekiamumas** sukūrė iš „Commerce Headquarters“, duomenis su kanalų duomenų bazėmis.

Kai atsargų prieinamumo reikalauja **Gautiapskaičiuotąprieinamumą** arba **Gautiapskaičiuotųprekiųsandėlioprieinamumą** API, skaičiavimas yra vykdomas tam, kad būtų gaunamas geriausias prekių atsargų apskaičiavimas. Skaičiuojant remiamasi visais elektroninės prekybos klientų užsakymais, kurie yra kanalo duomenų bazėje, bet neįtraukti į momentinės kopijos duomenis, kuriuos pateikė 1130 užduotis. Ši logika vykdoma stebint paskutinę įvykdytą atsargų operaciją iš „Commerce Headquarters“ ir lyginant ją su operacijomis kanalo duomenų bazėje. Ji teikia kanalo skaičiavimo logikos atskaitos vertę, kad būtų galima papildomus atsargų perkėlimus, kurie buvo atlikti kliento užsakymo pardavimo operacijose elektroninės prekybos kanalo duomenų bazėje, įtraukti į atsargų vertę, kurią pateikia API.

Kanalo skaičiavimo logika pateikia įvertintą faktinę atsargų vertę ir bendrą galimą pageidaujamo produkto ir sandėlio vertę. Vertės gali būti rodomos jūsų elektroninės prekybos svetainėje, jei norite, arba jos gali būti naudojamos kitoms verslo logikoms suaktyvinti elektroninės prekybos svetainėje. Pavyzdžiui, galite rodyti pranešimą, kad atsargose nėra, o ne faktinį turimą kiekį, kurį apskaičiavo API.

Skaičiavimo logika, kurią kanalo elektroninės prekybos API naudoja atsargų vertei apskaičiuoti, gali įvertinti atsargas tik pagal kliento užsakymus, kurie buvo sukurti kanalo duomenų bazėje, tačiau dar nebuvo sinchronizuoti ir užregistruoti „Commerce Headquarters“. Jeigu jūsų kanalo duomenų bazėje taip pat yra pardavimo už grynuosius pinigus operacijų duomenys iš tam tikrų parduotuvės sandėlių, pardavimai už grynuosius pinigus šiuose sandėliuose nėra įtraukiami į kanalo el. prekybos skaičiavimą.

## <a name="configure-the-inventory-lookup-operation-in-the-pos-channel"></a>Konfigūruokite atsargų peržvalgos operaciją EKA kanale

„Retail“ 10.0.9 ir ankstesnėse versijose EKA operacija **Atsargų peržvalga** naudojo paslaugos realiu laiku iškvietą į „Commerce Headquarters“, kad gautų pasirinkto produkto atsargų informaciją tiek iš dabartinės vartotojo parduotuvės, tiek iš visų kitų parduotuvių, kurios sukonfigūruotos vykdymo grupėje kaip parduotuvės kanalo konfigūracijos dalis. „Commerce“ 10.0.10 ir naujesnėse versijose galima išjungti paslaugos realiu laiku iškvietimus į „Commerce Headquarters“. Vietoj jų galite naudoti kanalo skaičiavimą „Commerce“ serveryje, kad nustatytumėte turimas atsargas, kurios yra faktiškai prieinamos parduotuvei ir bet kuriai kitai vietai, kuri nurodyta vykdymo grupėje. Ši kanalo apskaičiuotų atsargų konfigūracija taip pat naudinga vietose, kur interneto ryšys yra nepatikimas, nes jums nereikia būti prisijungus prie interneto, kad galėtumėte gauti atsargų peržvalgas iš „Commerce Headquarters“.

Kai kanalo skaičiavimas tinkamai sukonfigūruotas ir valdomas, jis gali teikti patikimesnį dabartinių parduotuvės atsargų įvertinimą, nes jis naudoja transakcijų duomenis, kurie yra komercijos kanalo duomenų bazėje, tačiau apie kuriuos „Commerce Headquarters“ dar gali neturėti informacijos. Pvz., jei naudojate esamą atsargų peržvalgų EKA paslaugos realiu laiku iškvietą, „Commerce Headquarters“ tikriausiai dar nebus informacijos apie produkto pardavimą už grynuosius pinigus, kuris ką tik buvo įvykdytas. Todėl produkto turimų atsargų vertė, kurią pateikia „Commerce Headquarters“, veikiausiai viršys faktines parduotuvės turimas atsargas pagal vieną vienetą. Tačiau, jei naudojate kanalo skaičiavimą, pardavimas už grynuosius pinigus gali būti įtrauktas į skaičiavimą ir atimtas iš turimų atsargų vertės, kuri rodoma. Nors vertės, kurias teikia ir kanalų skaičiavimas, ir paslaugos realiu laiku iškvieta yra tik turimų atsargų įvertinimas, vertė, kurią pateikia kanalo skaičiavimas, yra daug labiau tikėtina, kad yra tiksli dabartinėje parduotuvėje.

### <a name="get-started-with-pos-channel-side-calculated-inventory-availability"></a>Pradėkite naudoti EKA kanalo apskaičiuotą atsargų pasiekiamumą

Siekiant naudoti kanalo pusės apskaičiavimo logiką ir išjungti realaus laiko paslaugų skambučius atsargų paieškai iš POS programos, pirmiausia turite įjungti **Optimizuoto produkto prieinamumo skaičiavimo** funkciją per **Funkcijų valdymo** darbo sritį komercijos štabe. Be funkcijos įjungimo, turite atlikti **funkcijų šablono** pakeitimus.

Norėdami pakeisti **funkcijų profilį**, atlikite toliau nurodytus veiksmus.

1. Eikite į **„Retail and Commerce“\> Kanalo sąranka \> EKA sąranka \> EKA profiliai \> Funkcionalumo profiliai**.
1. Pasirinkite funkcijų šabloną.
1. „FastTab“ **Funkcijos**, skyriuje **Atsargų pasiekiamumo skaičiavimas**, pakeiskite lauko **Atsargų pasiekiamumo skaičiavimo būdas** vertę iš **Paslauga realiu laiku** į **Kanalas**. Pagal numatytuosius parametrus visi funkcijų profiliai naudoja paslaugos realiu laiku iškvietimus. Todėl, jei norite naudoti kanalo skaičiavimo logiką, turite pakeisti šio lauko vertę. Atlikus šį pakeitimą bus paveiktos visos mažmeninės prekybos parduotuvės, kurios yra susijusios su pasirinktu funkcijų šablonu.

Tada turite sinchronizuoti kanalo keitimus naudodami paskirstymo grafiko procesą ir atlikdami tolesnius veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**.
1. Vykdykite **1070** (**Kanalo konfigūracija**) užduotį.

Baigus konfigūruoti, informacijoje, kuri pateikiama apie faktiškai turimas atsargas, nebenaudojama paslaugos realiu laiku iškvieta, kai EKA programos vartotojas naudoja operaciją **Atsargų peržvalga** (standartiniai ir matricos rodiniai). Vietoje to duomenys apie tos parduotuvės ir visų vykdymo grupės parduotuvių faktiškai turimas atsargas apskaičiuojami pagal paskutinę žinomą momentinę kopiją, kuri buvo pristatyta į kanalo duomenų bazę iš „Commerce Headquarters“. Momentinės kopijos vertę detalizuoja kanalo skaičiavimas, kad būtų pakoreguota faktiškai turimų atsargų vertė remiantis pasirinkto produkto papildomomis pardavimo arba grąžinimo operacijomis, kurios yra kanalo duomenų bazėje, tačiau kurios nebuvo įtrauktos į paskutinę sinchronizuotą momentinę kopiją iš 1130 užduoties. Jeigu kanalo duomenų bazėje nėra operacijų duomenų iš sandėlių ar parduotuvių, esančių vykdymo grupėje, joje nėra jokių papildomų operacijų, kurias būtų galima įtraukti perskaičiuojant vertę. Todėl geriausias šių sandėlių ar parduotuvių turimų atsargų įvertinimas yra paskutinės žinomos „Commerce Headquarters“ momentinės kopijos duomenys.

EKA **Užsakymo vykdymas** ekranai taip pat įvertina kanalo skaičiavimą, kad parodytų turimas prekių atsargas, kai pasirenkama užsakymo vykdymo eilutė, o vartotojas peržiūri skydelį **Informacija**, skirtą pasirinktai prekei.

## <a name="optimize-your-inventory-data"></a>Optimizuokite atsargų duomenis

Norint užtikrinti, kad atsargos būtų įvertintos kuo tiksliau, svarbu naudoti šias „Commerce“ paketines užduotis ir dažnai jas paleisti:

- **P-job** – P užduotis yra puslapyje **Paskirstymo grafikai** ir turi būti vykdoma dažnai. Ši užduotis pateikia el. prekybos užsakymus, asinchroninius kliento užsakymus, kuriuos sukūrė EKA, ir grynųjų pinigų užsakymus, kuriuos EKA sukūrė iš kanalo duomenų bazių, į „Commerce Headquarters“, kad juos būtų galima apdoroti vėliau. Kol šie duomenys sinchronizuojami iš kanalo į „Commerce Headquarters", „Commerce Headquarters" neturi informacijos apie produktų, esančių sandėliuose, kurie susiję su šiomis operacijomis, atsargų koregavimus.
- **Sinchronizuoti užsakymus** – ši užduotis apdoroja neapdorotus operacijų duomenis „Commerce Headquarters“, kuriuos P užduotis teikia ir konvertuoja el. prekybos bei asinchronines kliento užsakymų operacijas į „Commerce Headquarters“ pardavimo užsakymus. Kol bus apdorota ši užduotis ir sukurti pardavimo užsakymai, nebus sukurtos jokios atsargų operacijos. Todėl „Commerce Headquarters“ turimose atsargose neatsispindės operacijos.
- **Atlikti operacijų išrašų paketinį skaičiavimą** – grynųjų pinigų operacijų, kurios sukurtos parduotuvėje, atveju duomenų perdavimo mažais kiekiais registravimo procesas užtikrina, kad su pardavimu susiję atsargų procesai bus veiksmingai atnaujinami. Norėdami pasiekti efektyviausią užsakymų už grynuosius pinigus atsargų operacijų apdorojimą įsitikinkite, kad sukonfigūravote savo sistemą naudoti [duomenų perdavimo mažais kiekiais registravimas](https://docs.microsoft.com/dynamics365/commerce/trickle-feed).
- **Atlikti operacijų išrašų paketinį registravimą** – ši užduotis taip pat reikalinga duomenų perdavimo mažais kiekiais registravimui. Po jos eina užduotis **Atlikti operacijų išrašų paketinį skaičiavimą**. Ši užduotis sistemingai registruoja apskaičiuotas sumas, kad „Commerce Headquarters“ būtų sukurti pardavimo už grynuosius pinigus pardavimo užsakymai ir „Commerce Headquarters“ tiksliau atspindėtų parduotuvės atsargas.
- **Produkto pasiekiamumas** – šia užduotimi sukuriama atsargų, esančių „Commerce Headquarters“, momentinė kopija.
- **1130 (produkto pasiekiamumas)** – ši užduotis randama puslapyje **Paskirstymo grafikai** ir turi būti vykdoma iškart po užduoties **Produkto pasiekiamumas**. Ši užduotis perkelia atsargų momentinės kopijos duomenis iš „Commerce Headquarters“ į kanalų duomenų bazes.

Jums nerekomenduojama naudoti tų darbų paketų per dažnai (kas keletą minučių). Dažni vykdymai perpildys komercijos štabus ir gali potencialiai pabloginti veikimą. Bendrai, geriausia praktika būtų vykdyti produkto prieinamumą ir 1130 darbus pagal valandas ir suplanuoti P-darbo sinchronizavimo užsakymus bei sumažinti su srauto talpinimu susijusius darbus tuo pačiu ar didesniu dažnumu.

> [!NOTE]
> Dėl našumo priežasčių, kai kanalo atsargų pasiekiamumo skaičiavimai naudojami atsargų pasiekiamumo užklausai įvykdyti naudojant el. prekybos API arba naują EKA kanalo atsargų logiką, skaičiuojant naudojama talpykla, kad būtų nustatyta, ar praėjo pakankamai laiko, kad būtų protinga skaičiavimo logiką vykdyti dar kartą. Numatytoji talpykla nustatyta kaip 60 sekundžių. Pavyzdžiui, jūs įjungėte kanalo skaičiavimą savo parduotuvei ir peržiūrėjote turimas produkto atsargas puslapyje **Atsargų peržvalga**. Jei tada vienas produkto vienetas parduodamas, puslapyje **Atsargų peržvalga** nebus rodomos sumažėjusios atsargos, kol talpykla nebus išvalyta. Po to, kai vartotojai užregistruos operacijas EKA, turi praeiti 60 sekundžių, kad būtų matomas turimų atsargų sumažėjimas.

Jei pagal jūsų verslo scenarijų reikia trumpesnio talpyklos laiko, pagalbos kreipkitės į savo produktų palaikymo tarnybos atstovą.


[!INCLUDE[footer-include](../includes/footer-banner.md)]