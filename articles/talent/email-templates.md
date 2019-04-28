---
title: El. laiško šablonai
description: Šioje temoje pateikiama informacija apie „Dynamics 365 for Talent - Attract“ galimus sukurti ir naudoti el. laiško šablonus.
author: andreabichsel
manager: AnnBe
ms.date: 10/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: b88ba4386dbf3513d75990acca1c07fa6f0dc9b0
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/19/2019
ms.locfileid: "857065"
---
# <a name="email-templates"></a>El. laiško šablonai
[!include[banner](../includes/banner.md)]

Naudodamiesi el. laiško šablonų biblioteka, administratoriai gali sukurti vienodą visų naudojantis „Microsoft Dynamics 365 for Talent: Attract“ siunčiamų el. laiškų temą ir žymėjimą. Administratoriai taip pat gali kuruoti el. laiško turinio šablonų rinkinį, kuriuo galėtų naudotis kiti vartotojai. Samdos komanda, pasinaudodama šiais šablonais darbo eigoje gali efektyviau siųsti el. laiškus. Kai „Attract“ el. laiškai konfigūruojami taip, kad būtų siunčiami automatiškai, o administratorius, naudodamasis el. laiško šablonų biblioteka, gali tinkinti šių el. laiškų turinį.

> [!NOTE]
> Norėdami naudoti el. laiškų šablonus, jūsų organizacija turi turėti išsamios įdarbinimo informacijos priedą.

## <a name="global-template-configurations"></a>Visuotinės šablono konfigūracijos

Norėdamas sukurti nuoseklius visų visus el. pašto pranešimų ženklus, administratorius pirmiausia turi nustatyti visuotines visų el. laiško šablonų antraštes ir poraštes. Administravimo centro skirtuko **El. laiško šablonų parametrai** skyriuje **Antraštė** administratorius gali įkelti paveikslėlį, kuris bus naudojamas kaip antraštė arba visų el. laiškų reklaminė juosta. Šis paveikslėlis gali būti įmonės logotipas, firminis blankas arba kitas atstovo vaizdas. Rekomenduojamas plotis – nuo 25 iki 800 pikselių, o aukštis – nuo 25 iki 150 pikselių, nes šie matmenys optimalūs naudojantis daugeliu el. pašto klientų, pvz., „Microsoft Outlook“. Paveikslėlis turi būti JPEG, JPG, PNG arba SVG failas, o šio failo dydis turi būti ne mažiau negu 1 megabaitas (MB). Įkėlus paveikslėlį sukuriama ir rodoma antraštės peržiūra. Prireikus antraštės paveikslėlį pašalinti arba pakeisti, administratorius gali naudotis virš peržiūros esančia parinktimi **Šalinti**.

Skyriuje **Poraštė** administratorius gali pateikti nuorodų į bendrovės ryšių privatumo politiką ir į sąlygas. Šios nuorodos įtrauktos į automatiškai sukuriamą poraštę. Tada galima peržiūrėti šią poraštę.

Prieš uždarydami administravimo centro langą, būtinai išsaugokite pakeitimus.

> [!NOTE] 
> Antraštė ir poraštė yra visuotiniai visų el. laiškų parametrai. Todėl jos bus rodomos visuose naudojantis „Attract“ siunčiamuose el. laiškuose. Jei parametrai nesukonfigūruoti, antraštė ir poraštė į el. laiškus neįtraukiamos.

## <a name="email-template-library"></a>El. laiško šablonų biblioteka 

Nustatęs visuotines šablono konfigūracijas, administratorius gali pradėti kurti ir kuruoti visų iš „Attract“ siunčiamų el. laiškų šablonus. El. laiško šablonų biblioteka prieinama tik administratoriams. Norėdami atidaryti biblioteką, pagrindiniame naršymo meniu paspauskite skirtuką **El. laiško šablonai**. Biblioteka kategorizuojama pagal įvairias „Attract“ veiklas, kurias atliekant turi būti siunčiami el. laiškai, pvz., planavimas, vertinimas ir pareigų kūrimas. Administratorius gali pasirinkti bet kurią kategoriją ir peržiūrėti visus su šia veikla susietus el. laiško tipus. Pavyzdžiui, pasirinkus **Planavimas** galima peržiūrėti įvairius vykstant planavimo procesui siunčiamų el. laiškų tipus ir visus galimus kiekvieno tipo el. laiško šablonus. Kiekvienas kategorijos poskyris reiškia el. laiško tipą.

Kai kurių tipų el. laiškuose gali būti nurodytas daugiau nei vienas gavėjas. Pavyzdžiui, tie kategorijos **Planavimas** el. laiškai, kurie siunčiami prireikus pokalbių grafiko suvestinės, siunčiami abiems kandidatams ir kalbintojams. Yra du pagrindiniai kiekvieno skyriaus stulpeliai: **Šablono pavadinimas** ir **Gavėjas**. Kiekvienoje skyriaus eilutė skirta vienam vieno tipo el. laiško šablonui. Iš pradžių užrakto simbolis bus rodomas kiekvieno šablono eilutėje. Šis simbolis reiškia, kad šablonas yra standartinis – toks, koks pateikiamas kartu su „Attract“ ir kurio panaikinti negalima. Naudodamasis bet kuriam šablonui skirtu elipsės mygtuku (**...**) administratorius gali nukopijuoti šabloną, nustatyti šabloną kaip numatytąjį arba jį panaikinti. Kai šablonas nustatomas kaip numatytasis, gali būti atliekamas vienas iš dviejų veiksmų. Veiksmą nurodo šablono eilutėje rodomas ženklas arba ženklai.

- **Numatytasis** – šis ženklas reiškia, kad šis šablonas yra numatytasis siunčiamo el. laiško šablonas ir kad informacija bus įrašyta vartotojui siunčiant šio konkretaus tipo el. laišką.
- **Numatytasis** + **Išsiųsta automatiškai** – šis ženklų derinys reiškia, kad tai aktyvus sistemos sukurtų automatiškai siunčiamų el. laiškų šablonas.

Norėdami redaguoti šabloną, pasirinkite eilutę ir atlikite šablono pakeitimus.

> [!NOTE]
> Kiekvienam tam tikro tipo el. laiško gavėjui skirtas numatytasis šablonas. Visi standartiniai „Attract“ šablonai nustatomi kaip numatytieji šablonai, kol administratorius sukuria naują konkretaus tipo el. laiško šabloną ir nustato jį kaip numatytąjį.

## <a name="create-a-template"></a>Kurti šabloną

Norėdami sukurti šabloną, el. laiško šablonų bibliotekos viršutiniame dešiniajame kampe paspauskite **+ Nauja šablonas**. Norėdami pasirinkti el. laiško, kuriam kuriate šabloną, tipą, pasirinkite gavėją, procesą ir įvykį, kuriam vykstant turi būti siunčiamas el. laiškas. Paskui paspauskite **Kurti**.

Atidaromas šablono redagavimo rodinys ir galima nurodyti šablono pavadinimą. Pavyzdžiui, jei šablonas skirtas kandidatams iš JAV universiteto, bet tekstas parašytas prancūzų kalba, galite įvesti pavadinimą **Universitetas\_JAV\_Francais**. Bet kurio šablono pavadinime, temos eilutėje ir tekste gali būti rašoma ir kita (ne tik anglų) kalba.

Šablono lauko **To** redaguoti negalima, kadangi pirmą kartą sukūrę šabloną jau pasirinkote gavėją.

Laiško kopijos (Cc) eilutėje galite nurodyti asmenis, pvz., **Darbdavys** arba **Samdos vadovas**. Siunčiant el. laišką, šie vaidmenys automatiškai pakeičiami atitinkamais vartotojais, atsižvelgiant į pareigų kontekstą.

Temos eilutėje ir tekste palaikomi vietos rezervavimo ženklai. Norėdami įterpti vietos rezervavimo ženklų, įveskite **\#**, o po to išplečiamajame sąraše pasirinkite atitinkamą vietos rezervavimo ženklą. Galimų vietos rezervavimo ženklų sąrašas rodomas dešinėje puslapio pusėje. Siunčiant el. laišką, šie vietos rezervavimo ženklai pakeičiami automatiškai, atsižvelgiant į pareigų ir gavėjo kontekstą. Pavyzdžiui, kandidatams siunčiamo el. laiško šablone yra vietos rezervavimo ženklas \#{Candidate\_Name}. Kai el. laiškas siunčiamas kandidatui, kurio vardas Cameron, tas vietos rezervavimo ženklas pakeičiamas vardu Cameron.

Tekstas redaguojamas raiškiojo teksto rengykle, kuria naudojantis galima keisti teksto stilių ir formatą. Taip pat galima įterpti hipersaitus ir fiksavimo taškus.

Kai sukuriamas konkretaus tipo el. laiško šablonas, šablono eilutėje paspauskite elipsės mygtuką (**...**) ir nustatykite jį kaip numatytąjį šabloną.

## <a name="consume-templates"></a>Šablonų naudojimas

Siųsdama el. laišką samdos komanda gali naudoti administratoriaus sukurtus šablonus. Jei sukurti keli vartotojo siunčiamam el. laiškui skirti šablonai, el. laiško kūrimo darbo eigoje rodomas išplečiamasis sąrašas. Automatiškai naudojamas numatytasis šablonas, bet vartotojas gali pasirinkti kitą šabloną.

> [!NOTE] 
> Jei el. laiškai siunčiami automatiškai, galima sukurti kelis šablonus. Tačiau aktyviu nustatyti galima tik vieną šabloną. Kadangi šį procesą suaktyvina įvykiai, tik administratorius gali nuspręsti, kurį šabloną naudoti, pagal šablonų bibliotekos ženklų kombinaciją **Numatytasis** ir **Išsiųsta automatiškai**.
