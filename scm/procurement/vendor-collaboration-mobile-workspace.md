---
title: "Tiekėjo bendradarbiavimas mobiliojo darbo Microsoft Dynamics &quot;365&quot; veiklos programa"
description: "Su tiekėjo bendradarbiavimas mobiliojo ryšio darbo sritį, jūsų pardavėjai gali naujienas apie pirkimo užsakymai, kurie buvo išsiųsti jas patvirtinti ir peržiūrėti informaciją apie naujų ir atnaujintų pirkimo užsakymų ir kontaktai."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 36 - 37
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267074
ms.assetid: fe8e912d-8446-4584-8a24-d8892e9028cd
ms.search.region: global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 9f441508b745d22218316128572c9ec6aeb7207b
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Tiekėjo bendradarbiavimas mobiliojo darbo Microsoft Dynamics "365" veiklos programa

Su tiekėjo bendradarbiavimas mobiliojo ryšio darbo sritį, jūsų pardavėjai gali naujienas apie pirkimo užsakymai, kurie buvo išsiųsti jas patvirtinti ir peržiūrėti informaciją apie naujų ir atnaujintų pirkimo užsakymų ir kontaktai.

<a name="prerequisites"></a>Būtinieji komponentai
-------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Būtinoji sąlyga</th>
<th>aprašymas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Skaityti apie Microsoft Dynamics 365 operacijų mobiliųjų platformų</td>
<td><a href="/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Dinamika 365 operacijų mobiliųjų platformų</a></td>
</tr>
<tr class="even">
<td>Dinamika 365 operacijoms</td>
<td>Įsitikinkite, kad naudojate aplinkoje, kuri yra Microsoft Dynamics 365 operacijų versija 1611 ir "Microsoft Dynamics" operacijų platformos naujinimas 3 (2016 m lapkričio mėn.).</td>
</tr>
<tr class="odd">
<td><span style="color: #000000;">Mobiliojo įrenginio, turinčio Dynamics 365 dėl operacijų taikomąją programą</span></td>
<td><span style="color: #000000;">Atsisiųskite Dynamics 365 operacijų App iš mobiliųjų programėlių parduotuvėje.</span></td>
</tr>
<tr class="even">
<td>Karštosios pataisos KB 3215650</td>
<td>Įdiekite karštąją pataisą norite įgalinti darbo sritys, kurios yra Microsoft Dynamics 365 operacijoms.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000;"><span style="color: #000000;">Karštosios pataisos KB 3216943</span> </span></td>
<td>Įdiekite karštąsias pataisas, kad tiekėjo bendradarbiavimas mobiliojo ryšio darbo sritį.</td>
</tr>
<tr class="even">
<td>Tiekėju vartotojas turi turėti prieigą prie tiekėjo bendradarbiavimo web sąsają Dynamics 365 operacijoms ir nustatyti tiekėjo bendradarbiavimo vartotojas.</td>
<td>Atlikite veiksmus, pateikiamus skyriuje šios temos kurti ir dirbti su tiekėjo bendradarbiavimo web sąsają.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Naudoti tiekėjo bendradarbiavimas dirbant su užsienio tiekėjais</a></li>
<li><a href="manage-vendor-collaboration-users.md">Tiekėjo bendradarbiavimo vartotojų valdymas</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Tiekėjo bendradarbiavimo nustatymas ir tvarkymas</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Naudoti tiekėjo bendradarbiavimas dirbant su Klientai Dynamics 365 operacijoms</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Apžvalga
Tiekėjo bendradarbiavimas mobiliojo darbo srities išlaiko tiekėjai informuojami apie naujus pirkimo užsakymus, kad jie galėtų matyti ir reaguoti į pirkimo užsakymus dinamika 365 operacijų web klientas.  

**Pastaba:** mobiliojo darbo srityje turėtų būti naudojamas kaip priedas prie tiekėjo bendradarbiavimo web sąsaja, tačiau negali pakeisti.  

Tiekėjo bendradarbiavimas mobiliojo ryšio darbo sritį, jūsų tiekėjų matyti naujuose pirkimo užsakymuose, kurie siunčiami patvirtinti. Tai rodo pirkimo užsakymo informaciją, pvz., produktai, kiekiui ir Pageidaujamos gavimo datos. Kainos yra prieinamos, atsižvelgiant į kiekvieno tiekėjo konfigūraciją.  

Kai vartotojas įeina, kaip tiekėjų, jie matys pirkimo pavedimai atsiliepė į, arba pirkimo pavedimai, kurie vis dar laukia pirkėjo veiksmų. Pardavėjas gali pasiūlė kitą pristatymo dieną, dar nesuderinta su klientu, pirkimo užsakymą, kad šiuo metu laukiama pirkėjo veiksmų. Pardavėjas taip pat pateikiamas pirkimo užsakymų, kuriuose yra patvirtintos, bet dar nepristatytos.  

Reaguoti į pirkimo užsakymą, tiekėjas turi naudoti tiekėjo bendradarbiavimo web sąsaja, kuri yra prieinama Dynamics 365 operacijų žiniatinklio kliento. Tai taip pat, jeigu pardavėjas gaus daugiau informacijos apie užsakymą, pvz., dokumento priedus, pristatymo adresą per liniją, ir mokesčiai, kurie yra susiję su tiekėjo.  

Specialūs saugos vaidmenį, pardavėjas matyti kuris kontaktas, asmenys yra įsiregistravę tiekėjo sąskaitą. Su tą patį saugos vaidmenį, bet kokį vartotojo prašymą, pateikimo būseną galite peržiūrėti pardavėjo.  

Kurti naujus ryšius ir naujas vartotojo prašymui pateikti, turi būti daroma tiekėjo bendradarbiavimo sąsają, kuri yra prieinama Dynamics 365 operacijų žiniatinklio kliento.  

Su mobiliojo ryšio darbo sritį, jūsų tiekėjas gali:

-   Rodyti naujuose pirkimo užsakymuose, siunčiamas į pardavėją.
-   Peržiūrėti pirkimo užsakymų kad pardavėjas reagavo į ir laukia pirkėjo veiksmų.
-   Peržiūrėti pirkimo užsakymus, kurie yra patvirtinti valstybės ir visiškai nepasiekė.
-   Rodyti kontaktinio asmens informaciją, kuri yra registruota tiekėjo sąskaitos (reikalingas papildomas saugos vaidmenį).
-   Peržiūrėti informaciją ir vykdykite vartotojo prašymą suporuoti su tiekėju (reikalingas papildomas saugos vaidmenį) statusą.

## <a name="get-started"></a>Darbo pradžia
Pradžia mobiliajame įrenginyje:

1.  Jūsų mobiliųjų įrenginių programėlę parduotuvėje, atsisiųskite ir įdiekite Microsoft Dynamics 365 veiklos programą.
2.  Paleiskite programėlę į savo įrenginį.
3.  Įveskite savo dinamika 365 URL.
4.  Įveskite prisijungti prie kompanijos. Pavyzdžiui, įveskite **USMF**.
5.  Pirmą kartą, kai prisijungsite, bus rodomas raginimas įvesti vartotojo vardą ir slaptažodį savo Microsoft Dynamics "365" veiklos sąskaita. 

Po to, kai įeinate į programą, nėra darbo sričių yra matomi. Norėdami peržiūrėti savo mobiliesiems darbo sričių, pirmiausia turi publikuoti norimą darbo srities dinamika 365 operacijų programos. Jums reikia sistemos administracijos leidimo skelbti darbo sritį.

1.  Paleisti Dynamics 365 operacijoms.
2.  Eikite į **sistemos administravimo**&gt;**nustatymo**&gt;**sistemos parametrai**.
3.  Pasirinkite **tvarkyti mobiliųjų įrenginių programėlę**.
4.  Pasirinkite darbo sritį **tiekėjo bendradarbiavimas** skelbti apie mobiliųjų platformų.
5.  Pasirinkite **skelbti darbo srities**.
6.  Atnaujinkite įrenginio paskelbtų darbo sritis.
7.  Pasirinkite į **tiekėjo bendradarbiavimas** darbo srities. Jūs šį puslapį.

[![tiekėjas-bendradarbiavimas-programėlė](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Kontaktai
Ir **kontaktais** puslapis leidžia matyti visus ryšius, kurie buvo nustatyti tiekėjo sąskaitos. Tai rodo kontaktinio asmens vardą, elektroninio pašto ir naudotojų pseudonimas, jei įmanoma. Jis taip pat rodo, ar kontaktinis asmuo vartotojo sąskaita yra aktyvi. Kai pasirenkate adresato, kontaktinius duomenis, pvz., kurioje juridinių asmenų asmuo yra kontaktą, ir kontaktinė informacija telefono numerį arba el. pašto adresą.

## <a name="user-requests"></a>Vartotojų užklausos
Su **vartotojo užklausas** puslapis leidžia matyti visus vartotojas prašo, kad pateikė per tiekėjo bendradarbiavimo web sąsają ir sekti būseną. Pasirinkus vartotojo prašymą, galite pamatyti, kas buvo prašyta, pridėti ar nukenksmina vartotojas, keisti saugumo, ir pamatyti, kurie saugos vaidmenų buvo prašoma pateikti vartotojo.

## <a name="purchase-orders-ready-for-review"></a>Parengta Peržiūrėti pirkimo užsakymus
Į **pirkimo užsakymus paruošta apžvalga** puslapis leidžia jums pamatyti, visi pirkimo užsakymai, buvo išsiųsti klientui ir nebuvo atsakyta. Galite peržiūrėti pasirinktą informaciją apie užsakymą, pavyzdžiui, produktams, kurių buvo paprašyta ir kada pristatyti. Informaciją apie kainas galima tik, jei tai sukonfig┼½ruota tiekėjui.  

Jūs galite pamatyti, ar pirkimo užsakymą turi pastabų arba priedus. Neatidarinėkite, jums reikia naudoti tiekėjo bendradarbiavimas žiniatinklio kliente. Pasirinkite **pirkimo užsakymo eilutę** Norėdami pamatyti visas eilutes su detalėmis. Atkreipkite dėmesį, kad kiekvienai eilutei, indikatorius parodys, ar yra pastabos ar priedus arba jei yra pristatymo adresą, kuris yra kitoks, nei kas turi būti rodoma antraštės.  

Reaguoti į pirkimo užsakymą, turite naudoti tiekėjo bendradarbiavimas žiniatinklio klientą.

## <a name="awaiting-customer-action"></a>Laukiama kliento veiksmo
Į **laukia klientų veiksmų** puslapis leidžia jums ieškoti pirkimo užsakymų, kad jūs arba kas nors iš jūsų įmonės, kurie taip pat turi prieigą prie tiekėjo bendradarbiavimas, atsakė į. Pirkimo užsakymai yra matomos šiame sąraše tik jei klientas turi atlikti vieną iš šių veiksmų pirkimo užsakyme.

-   Atmetus pirkimo užsakymas, klientui būtų arba būtina atnaujinti išsiųsti užsakymą ir siųsti dar kartą arba atšaukti užsakymą ir persiųsti. Kai pirkimo užsakymas išsiųstas dar kartą, jis dings iš to **laukia klientų veiksmų** puslapis.
-   Jei pirkimo užsakymą buvo priimtas su pakeitimais, klientas turi atnaujinti pradinį užsakymą ir siųsti peržiūrai, arba atnaujinti pagal pakeitimus ir patvirtinti jį iš karto. Abiem atvejais pirkimo užsakymą dings iš to **laukia klientų veiksmų** puslapis.
-   Jei pirkimo užsakymą buvo priimtas, ir pasirodo kad **laukia klientų veiksmų** puslapyje, tai yra, nes pirkimo užsakymas nebus automatiškai patvirtinta kai priėmimo buvo padaryta. Jis laukia pirkimo agentui pakeisti užsakymą į patvirtinta. Paprastai pirkimo užsakymą, kad būtų laikoma kaip tarp kliento ir tiekėjo susitarimą kaip tik pardavėjas priima užsakymą. Juda pirkimo užsakymas patvirtintas valstybei būtų sutvarkyti.

Pasirinkus pirkimo užsakymas, papildoma informacija atrodo apie atsakymą. Jūs galite pamatyti eilutės informaciją ir atsako už kiekvieną eilutę. Eilutės būsena parodo, kuri šių atsakymų buvo suteikta.

-   Priimta
-   Atmestas
-   Priimta su pakeitimais
-   Pakeisti/pakeisti
-   Padalinti į grafiką/tvarkaraščio eilutės

Atkreipkite dėmesį, kad indikatorius parodo **pristatymas**= taip/ne, kuris yra naudojamas nurodyti, kad eilutės nebus pristatytas. Gali būti, kad linija buvo atmestas, arba rūšies tais atvejais, kai nėra tikėtina, kad pristatyti esančių originaliose eilutėse, ar linija, kuri buvo padalyta į kelis tvarkaraščio eilutės ir pradinėje eilutėje nėra tikėtina, kad pristatyti prašymą gavimo tvarka.  

Užsakymo eilutės atsakymo bet kokie pakeitimai rodomi, išskyrus įkelta pastabas ir priedus, kuriuos matote naudojant tiekėjo bendradarbiavimo web sąsają.

## <a name="open-confirmed-orders"></a>Atviri patvirtinti užsakymai
Pirkimo užsakymas patvirtinamas pirkėjo, t. y. pirkimo užsakymą pasikeičia į patvirtintas valstybės, jis pasirodys atidaryti patvirtinta tvarka. Jis liks sąraše tol, kol jis yra įregistruotas kaip gautos.


