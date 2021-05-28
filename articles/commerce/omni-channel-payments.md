---
title: Integruotų kanalų mokėjimų apžvalga
description: Šioje temoje pateikiama informacija apie „Dynamics 365 Commerce“ integruoto kanalo mokėjimus.
author: rubendel
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 8.1.3
ms.openlocfilehash: 7b99b5f7b5b972d41e0831995bde69e9041369b9
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6028016"
---
# <a name="omni-channel-payments-overview"></a>Integruotų kanalų mokėjimų apžvalga

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie „Dynamics 365 Commerce“ integruoto kanalo mokėjimus. Ji apima išsamų palaikomų scenarijų sąrašą, informaciją apie funkcijas, sąranką bei trikčių diagnostiką ir kai kurių tipiškų problemų aprašymus.

## <a name="key-terms"></a>Pagrindiniai terminai

| Semestras | Aprašas |
|---|---|
| Atpažinimo ženklas | Duomenų seka, kurią kaip nuorodą pateikia mokėjimo procesorius. Atpažinimo ženklai gali nurodyti mokėjimo kortelių numerius, mokėjimų autorizavimą ir ankstesnius mokėjimus. Atpažinimo ženklai yra svarbūs, nes jie padeda apsaugoti konfidencialius duomenis elektroninio kasos aparato (EKA) sistemoje. Kartais jie taip pat vadinami *nuorodomis*. |
| Kortelės atpažinimo ženklas | Atpažinimo ženklas, kurį mokėjimo procesorius pateikia saugoti EKA sistemoje. Kortelės atpažinimo ženklą gali naudoti tik jį gavęs prekybininkas. Kortelių atpažinimo ženklai kartais taip pat vadinami *kortelių nuorodomis*. |
| Autorizavimo („auth“) atpažinimo ženklas | Unikalus ID, kurį mokėjimo procesas pateikia kaip dalį atsakymo, kurį siunčia EKA sistemai po to, kai EKA sistema sukuria autorizavimo užklausą. Autorizavimo atpažinimo ženklą galima naudoti vėliau, jei procesorius iškviečiamas atlikti tokius veiksmus kaip autorizavimo atšaukimas arba anuliavimas. Tačiau dažniausiai jis naudojamas norint fiksuoti lėšas, kai įvykdytas užsakymas arba baigta operacija. Autorizavimo atpažinimo ženklai kartais taip pat vadinami *autorizavimo nuorodomis*. |
| Atpažinimo ženklo fiksavimas | Nuoroda, kurią mokėjimo procesorius pateikia EKA sistemai, kai atsiskaitymas yra baigtas arba užfiksuotas. Tada fiksavimo atpažinimo ženklą galima naudoti norint nurodyti mokėjimo fiksavimą vėlesnėse operacijose, pvz., grąžinimo užklausose. | 
| Kortelės nėra | Frazė, nurodanti mokėjimo operacijas, atliekamas nepateikiant faktinės kortelės. Pavyzdžiui, šios operacijos gali būti vykdomos elektroninės prekybos arba skambučių centro scenarijuose. Atliekant šias operacijas, su mokėjimais susijusi informacija įvedama neautomatiniu būdu el. prekybos svetainėje, skambučių centro sraute arba EKA ar mokėjimo terminale. |
| Kortelė yra | Frazė, nurodanti mokėjimo operacijas, kurias atliekant faktinė kortelė pateikiama naudojama mokėjimo terminale, sujungtame su „Microsoft Dynamics 365“ EKA sistema. |

## <a name="overview"></a>Apžvalga

Paprastai frazė *integruoto kanalo mokėjimai* nurodo galimybę kurti užsakymą viename kanale ir vykdyti jį kitame kanale. Svarbiausia integruoto kanalo ypatybė – mokėjimo informacijos ir likusios užsakymo informacijos išsaugojimas bei mokėjimo informacijos naudojimas, kai užsakymas atšaukiamas arba apdorojamas kitame kanale. Klasikinis pavyzdys yra scenarijus „Pirkimas internetu, atsiėmimas parduotuvėje“. Tokiu atveju mokėjimo informacija yra įtraukiama, kai užsakymas sukuriamas internete. Tada informacija atšaukiama EKA, kad kliento mokėjimo kortelė būtų apmokestinta paėmimo metu. 

Visus scenarijus, aprašytus šioje temoje, galima įgyvendinti naudojant standartinį mokėjimų programinės įrangos kūrimo rinkinį (SDK), kuris pateikiamas kartu su „Commerce“. [„Dynamics 365“ mokėjimo jungtis, skirta „Adyen“](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3), pateikia parengtą naudoti kiekvieno čia aprašyto scenarijaus įdiegtį. 

### <a name="prerequisites"></a>Būtinieji komponentai

Kiekvienam šioje temoje aprašytam scenarijui reikalinga mokėjimo jungtis, palaikanti integruoto kanalo mokėjimus. Parengta naudoti „Adyen“ jungtis taip pat gali būti naudojama, nes ji palaiko scenarijus, kurie galimi naudojant mokėjimų SDK. Norėdami daugiau informacijos apie tai, kaip nustatyti mokėjimų jungtis, ir apie „Retail“ SDK bendrai rasite apsilankę [pagrindiniame „Retail“, skirtos IT profesionalams ir kūrėjams, puslapyje](/dynamics365/unified-operations/retail/dev-itpro/dev-retail-home-page#payment-connectors).

#### <a name="supported-versions"></a>Palaikomos versijos

Šioje temoje aprašytos integruoto kanalo galimybės išleistos kaip „Microsoft Dynamics 365 for Retail“ 8.1.3 versijos dalis. 

#### <a name="card-present-and-card-not-present-connectors"></a>Tipo „Kortelė yra“ ir „kortelės nėra“ jungtys

Mokėjimų SDK priklauso nuo dviejų mokėjimo programų kūrimo sąsajų (API) rinkinių. Pirmas API rinkinys pavadintas **iPaymentProcessor**. Jis naudojamas taikant tipo „kortelės nėra“ jungtis, kurias galima naudoti skambučių centruose ir su „Microsoft Dynamics“ elektroninės prekybos platforma. Norėdami daugiau informacijos apie sąsają **iPaymentProcessor** žr. mokėjimus apimančią dokumentaciją [Mokėjimo jungties ir mokėjimo įrenginio diegimas](https://download.microsoft.com/download/e/2/7/e2735c65-1e66-4b8d-8a3c-e6ef3a319137/The%20Guide%20to%20Implementing%20Payment%20Connector%20and%20Payment%20Device_update.pdf). 

Antras API rinkinys pavadintas **iNamedRequestHandler**. Jis palaiko tipo „kortelė yra“ mokėjimo integravimo, naudojančio mokėjimo terminalą, diegimą. Norėdami gauti daugiau informacijos apie sąsają **„iNamedRequestHandler”** sąsają, žr. [Mokėjimų integravimo į mokėjimo terminalą kūrimas](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension). 

### <a name="setup-and-configuration"></a>Nustatymas ir konfigūracija

Būtini toliau nurodyti komponentai ir nustatymo veiksmai.

- **„eCommerce“ integracija:** norint, kad būtų palaikomi scenarijai, kai užsakymas pateikiamas internetinėje parduotuvėje, reikalinga integracija su „Commerce“. Norėdami daugiau informacijos apie „Retail e-Commerce“ SDK, žr. [„e-Commerce“ platformos programinės įrangos kūrimo rinkinys (SDK)](/dynamics365/unified-operations/retail/dev-itpro/ecommerce-platform-sdk). Demonstracinėje aplinkoje nuorodos parduotuvė palaiko integruoto mokėjimo scenarijus. 
- **Mokėjimų internetu konfigūracija:** internetinio kanalo sąranka turi apimti mokėjimo jungtį, kuri buvo atnaujinta, kad palaikytų integruoto kanalo mokėjimus. Taip pat galima naudoti parengtą naudoti mokėjimo jungtį. Informacijos apie tai, kaip konfigūruoti „Adyen“ mokėjimo jungtį, skirtą internetinėms parduotuvėms, žr. [„Adyen“ mokėjimo jungtis](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#e-commerce). Reikia ne tik atlikti šioje temoje aprašytus „eCommerce“ sąrankos veiksmus, bet ir „Adyen“ jungties parametruose nustatyti parametro **Leisti įrašyti informaciją Galima įrašyti informaciją apie elektroninėje prekyboje** vertę **True**. 
- **Daugiakanalių mokėjimų konfigūracija:** operacijų skyriuje eikite į **„Retail and Commerce“ \> Būstinės sąranka \> Parametrai \> Bendrai naudojami „Commerce“ parametrai**. Tada skirtuke **Integruotas kanalas** nustatykite parinkties **Naudoti integruoto kanalo mokėjimus** vertę **Taip**. Prekybos versijose 10.0.12 ir naujesnėse šie parametrai yra **Funkcijų valdymo** darbo srityje. Pasirinkite **Vieno kanalo mokėjimai** funkciją ir paspauskite **Įjungti dabar**. 
- **Mokėjimo paslaugos:** skambučių centras naudoja numatytąją mokėjimo jungtį puslapyje **Mokėjimo paslaugos**, kad apdorotų mokėjimus. Siekiant palaikyti tokius scenarijus „Pirkimas skambučių centre, atsiėmimas parduotuvėje“, ši numatytoji mokėjimo jungtis turi būti „Adyen“ mokėjimo jungtis arba mokėjimo jungtis, kuri atitinka integruoto kanalo mokėjimų vykdymo reikalavimus.
- **EFT paslauga:** mokėjimo terminale atliekami mokėjimai turi būti nustatyti aparatinės įrangos profilio „FastTab“**EFT paslauga**. „Adyen“ jungtis iš karto palaiko integruoto kanalo mokėjimus. Kitos mokėjimo jungtys, palaikančios sąsają **iNamedRequestHandler**, taip pat gali būti naudojamos, jei jos palaiko integruoto kanalo mokėjimus.
- **Mokėjimo jungties pasiekiamumas:** kai užsakymas atšaukiamas, į mokėjimo priemonės eilutes, kurios buvo atšauktos kartu su užsakymu, įtraukiamas mokėjimo jungties, kuri buvo naudojama kuriant su tuo užsakymu susijusius autorizavimus, pavadinimas. Kai užsakymas įvykdomas, mokėjimų SDK bando naudoti tą pačią jungtį, kuri buvo naudojama pradiniam autorizavimui sukurti. Todėl jungtį, kurios prekybininko ypatybės sutampa, turi pavykti fiksuoti. 
- **Kortelių tipai:** kad integruoto kanalo scenarijai veiktų tinkamai, kiekvieno kanalo priemonių tipų sąranka turi būti tokia pati ir ją turi būti galima naudoti integruotame kanale. Ši sąranka apima apmokėjimo būdo ID ir kortelės tipo ID. Pvz., jei internetinės parduotuvės sąrankoje priemonės tipo **Kortelės** ID yra **2** , mažmeninės parduotuvės sąrankoje jos ID turi būti toks pat. Tas pats reikalavimas taikomas kortelės tipo ID. Jei internetinėje parduotuvėje kortelės numeris **12** nustatytas kaip **VISA**, mažmeninės prekybos parduotuvėje turi būti nustatytas toks pat ID. 
- „ Retail Modern POS“ „Windows“ ar „Android“ su įdiegta kompiuterinės įrangos stotimi -arba-
- Modernus POS iOS ar debesies POS su sujungta bendrinta kompiuterinės įrangos stotimi. 

### <a name="basic-principle-supporting-omni-channel-payments"></a>Pagrindinis principas, palaikantis integruoto kanalo mokėjimus

Mokėjimo jungtys ir mokėjimo procesoriai naudoja atpažinimo ženklus (arba nuorodas), kad nurodytų su kortelių mokėjimais susijusias sąveikas. Pavyzdžiui, kai pateikiama mokėjimo autorizavimo užklausa, pateikiama nuoroda į tą autorizavimą. Todėl autorizavimą galima nurodyti vėliau, kai vykdymo metu fiksuojamos lėšos. Šis autorizavimas yra unikalus prekybininkui, mokėjimo surinkėjui ir procesoriui. 

Jei internete sukurtas užsakymas paimamas parduotuvėje, reikia nuskaityti ir naudoti tą pačią to užsakymo mokėjimo informaciją. Kai pradinė informacija pateikiama kaip užklausos dalis siekiant fiksuoti mokėjimą pagal pradinį autorizavimą, mokėjimo procesorius galės apdoroti užklausą ir užfiksuoti apmokėjimą. 

Norint tinkamai nurodyti internetinį užsakymą, taip pat turi būti pasiekiama tipo „kortelės nėra“ mokėjimo jungtis, kuri palaiko tą patį procesorių. Tokiu būdu EKA sistemoje gali būti vienas procesorius, skirtas tipo „kortelė yra“ mokėjimams, tačiau ji taip pat gali turėti prieigą prie kitų mokėjimo jungčių, kad galėtų įvykdyti užsakymus, kurie sukuriami kituose kanaluose naudojant skirtingus mokėjimo procesorius. 

## <a name="supported-scenarios"></a>Palaikomi scenarijai

Palaikomi toliau nurodyti integruoto kanalo mokėjimo scenarijai.

- Pirkimas internetu, atsiėmimas parduotuvėje
- Pirkimas skambučių centre, atsiėmimas parduotuvėje
- Pirkimas A parduotuvėje, atsiėmimas B parduotuvėje
- Pirkimas A parduotuvėje, siuntimas klientui

    > [!NOTE]
    > Skambučio centre esantys mokėjimai, kuriuos susieti su „įprasta“ mokėjimo funkcija, turi būti pažymėti kaip **Išankstinis mokėjimas** = **Taip**, kad būtų atspindėta suma, kuri turi būti sumokėta, kai atšaukiamas užsakymas EKA. Ne išankstinio mokėjimo „įprasto“ tipo mokėjimai yra neatpažįstami, kai atšaukiamas mokėjimas EKA. 

Taip pat palaikomi šių scenarijų variantai. Pavyzdžiui, internetiniame užsakyme gali būti ir eilučių, kurios bus išsiųstos klientui, ir eilučių, kurios bus paimtos parduotuvėje. Visos užsakymo vykdymo parinktys palaikomos naudojant integruoto kanalo mokėjimus. 

Tolesniuose skyriuose aprašomi kiekvieno scenarijaus veiksmai ir rodoma, kaip vykdyti scenarijų naudojant demonstracinius duomenis. 

### <a name="buy-online-pick-up-in-store"></a>Pirkimas internetu, atsiėmimas parduotuvėje

Prieš pradėdami įsitikinkite, kad įvykdytos toliau nurodytos būtinosios sąlygos.

- Turite nuorodos parduotuvę, kurioje sukonfigūruota „Adyen“ jungtis.
- **Daugiakanalių mokėjimų** parinktis, esanti puslapyje **Bendrai naudojami „Commerce“ parametrai**, nustatoma į **Tiesa**. Paskutinėse versijose šie parametrai perkelti į **Funkcijos valdymas** darbo sritį, kurioje galite pasirinkti **Vieno kanalo mokėjimai** funkciją ir paspausti **Įjungti dabar**. 
- „Adyen“ mokėjimo jungtis sukonfigūruota ;Houston: EKA registre.
- „ Retail Modern POS“ „Windows“ ar „Android“ su įdiegta kompiuterinės įrangos stotimi -arba-
- Modernus POS iOS ar debesies POS su sujungta bendrinta kompiuterinės įrangos stotimi. 

Norėdami vykdyti scenarijų atlikite toliau nurodytus veiksmus.

1. Nuorodos parduotuvėje sukurkite parduotuvėje paimamą užsakymą. Įsitikinkite, kad pasirinkote parduotuvę **Houston**. 
2. Atlikite atsiskaitymo veiksmus ir sumokėkite naudodami tikrinimo kredito kortelės numerį. Tikrinimo kredito kortelių numerius galite rasti puslapyje [„Adyen“ tikrinimo kortelių numeriai](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description).
3. „Commerce“ naudokite paketinę užduotį **Sinchronizuoti užsakymus** ir paskirstymo grafiką **P-001**, kad galėtumėte sukurti užsakymus operacijų skyriuje.
4. EKA darbo pradžios puslapyje pasirinkite operaciją **Paimtini užsakymai**, kad peržiūrėtumėte parduotuvėje paimtinus užsakymus. 
5. Pasirinkite vieną ar kelias eilutes iš užsakymo, kuris buvo sukurtas nuorodos parduotuvėje, tada pasirinkite **Paimti**.

    Užsakymas nuskaitomas iš operacijų biuro. 

6. Kai užsakymo eilutės informacija nuskaitoma iš operacijų biuro ir aptinkama kortelė, kurią galima naudoti integruotame kanale, pranešama apie galimą mokėjimo būdą.
7. Pasirinkite **Naudoti galimą mokėjimo būdą**, kad atliktumėte operaciją naudodami kortelės informaciją, kuri buvo įvesta nuorodos parduotuvėje.

    Užsakymo eilutės įkeliamos į operacijos puslapį, o balansas yra 0 (nulis). 

8. Pasirinkite skirtuką **Mokėjimai**, kad peržiūrėtumėte priemonės eilutę, kuri buvo nuskaityta iš internetinio užsakymo. 
9. Pasirinkite bet kokį mokėjimo būdą, kad atliktumėte operaciją. 

### <a name="buy-in-call-center-pick-up-in-store"></a>Pirkimas skambučių centre, atsiėmimas parduotuvėje

1. „Commerce“, puslapyje **Klientų aptarnavimas**, ieškos juostoje įveskite **Karen Berg**, tada pasirinkite **Ieškoti**. 
3. Ieškos rezultatuose pasirinkite **Karen Berg**.
4. Kai Karen bus įkelta į puslapį **Klientų aptarnavimas**, pasirinkite **Naujas pardavimo užsakymas**.
5. Naujame pardavimo užsakymo puslapyje pasirinkite **Antraštė**, kad peržiūrėtumėte užsakymo antraštę. 
6. Puslapyje **Užsakymo antraštė** nustatykite vietą į **Centrinė**, o sandėlį – į **Houston**.
7. Skirtuke **Pristatymas** nustatykite kliento paėmimo lauką **Pristatymo būdas** į vertę **60**.
8. Pasirinkite **Eilutės**, tada į užsakymą įtraukite vieną ar daugiau eilučių. 
9. Pasirinkite **Baigti**, kad prasidėtų užsakymo vykdymo užbaigimo eiga.
10. Slinkite žemyn į mokėjimų skiltį, pasirinkite **Įtraukti**, tada pasirinkite eilutę, kurioje nustatytas mokėjimo būdo tipas **Kortelės**. 
11. Norėdami įtraukti mokėjimą kortele, pasirinkite pliuso ženklą (**+**). 
12. Įveskite tikrinimo kredito kortelės numerio informaciją, kuri nurodyta puslapyje [„Adyen“ tikrinimo kortelių numeriai](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description), tada pasirinkite **OK**.

    > [!NOTE]
    > Jei įvesto numerio kortelės prekės ženklas skiriasi nuo prekės ženklo, pasirinkto inicijuojant mokėjimą, mokėjimas vis tiek bus įvykdytas. Tačiau jis bus užregistruotas paskyrose, susietose su kortelės prekės ženklu, kurį pasirinkote atlikdami 10 veiksmą.

12. Dar kartą pasirinkite **OK**, kad uždarytumėte dialogo langą **Užsakymo įvykdymo mokėjimai**.
13. Puslapyje **Pardavimo užsakymo suvestinė** pasirinkite **Pateikti**.
14. EKA darbo pradžios puslapyje pasirinkite operaciją **Paimtini užsakymai**, kad peržiūrėtumėte parduotuvėje paimtinus užsakymus. 
15. Pasirinkite vieną ar kelias eilutes iš užsakymo, kuris buvo sukurtas nuorodos parduotuvėje, tada pasirinkite **Paimti**.

    Užsakymas nuskaitomas iš operacijų biuro. 

16. Kai užsakymo eilutės informacija nuskaitoma iš operacijų biuro ir aptinkama kortelė, kurią galima naudoti integruotame kanale, pranešama apie galimą mokėjimo būdą.
17. Pasirinkite **Naudoti galimą mokėjimo būdą**, kad atliktumėte operaciją naudodami kortelės informaciją, kuri buvo įvesta nuorodos parduotuvėje.

    Užsakymo eilutės įkeliamos į operacijos puslapį, o balansas yra 0 (nulis).

18. Pasirinkite skirtuką **Mokėjimai**, kad peržiūrėtumėte priemonės eilutę, kuri buvo nuskaityta iš internetinio užsakymo. 
19. Pasirinkite bet kokį mokėjimo būdą, kad atliktumėte operaciją. 

### <a name="buy-in-store-a-pick-up-in-store-b"></a>Pirkimas A parduotuvėje, atsiėmimas B parduotuvėje

1. Paleiskite parduotuvės „Houston“ EKA.
2. Puslapyje **Operacija** įtraukite Karen Berg į operaciją naudodami skaitmenų klaviatūrą, kad įvestumėte **2001.**
3. Į operaciją įtraukite vieną ar daugiau eilučių.
4. Pasirinkite **Užsakymai**, kad peržiūrėtumėte užsakymo parinktis.
5. Pasirinkite **Paimti viską**, tada, kai jus paragins, pasirinkite **Kliento užsakymas**.
6. Ieškos juostoje įveskite **Seattle**, tada pasirinkite paėmimo parduotuvę **Seattle**. 
7. Pasirinkite **OK**, kad esamą datą patvirtintumėte kaip paėmimo datą.
9. Pasirinkite **Mokėti kortele,** kad inicijuotumėte mokėjimą.
10. Naudodami kortelę įmokėkite mokėtiną depozito sumą. 
11. Užbaikite depozito mokėjimą mokėjimo terminale. 
12. Sumokėję depozitą pasirinkite parinktį naudoti tą pačią kortelę vykdymo metu ir palaukite, kol užsakymas bus įvykdytas. 
13. Paleiskite parduotuvės „Seattle“ EKA.
14. EKA darbo pradžios puslapyje pasirinkite operaciją **Paimtini užsakymai**, kad peržiūrėtumėte parduotuvėje paimtinus užsakymus. 
15. Pasirinkite vieną ar kelias eilutes iš užsakymo, kuris buvo sukurtas nuorodos parduotuvėje, tada pasirinkite **Paimti**.

    Užsakymas nuskaitomas iš operacijų biuro. 

16. Kai užsakymo eilutės informacija nuskaitoma iš operacijų biuro ir aptinkama kortelė, kurią galima naudoti integruotame kanale, pranešama apie galimą mokėjimo būdą.
17. Pasirinkite **Naudoti galimą mokėjimo būdą**, kad atliktumėte operaciją naudodami kortelės informaciją, kuri buvo įvesta nuorodos parduotuvėje.

    Užsakymo eilutės įkeliamos į operacijos puslapį, o balansas yra 0 (nulis).

18. Pasirinkite skirtuką **Mokėjimai**, kad peržiūrėtumėte priemonės eilutę, kuri buvo nuskaityta iš internetinio užsakymo. 
19. Pasirinkite bet kokį mokėjimo būdą, kad atliktumėte operaciją. 

### <a name="buy-in-store-a-ship-to-customer"></a>Pirkimas A parduotuvėje, siuntimas klientui

1. Paleiskite parduotuvės „Houston“ EKA.
2. Puslapyje **Operacija** įtraukite Karen Berg į operaciją naudodami skaitmenų klaviatūrą, kad įvestumėte **2001.**
3. Į operaciją įtraukite vieną ar daugiau eilučių.
4. Pasirinkite **Užsakymai**, kad peržiūrėtumėte užsakymo parinktis.
5. Pasirinkite **Siųsti viską**, tada, kai jus paragins, pasirinkite **Kliento užsakymas**.
6. Siuntimo metodo puslapyje pasirinkite **Standartinis pristatymas per naktį**, o tada pasirinkite **Gerai**, kad patvirtintumėte šios dienos datą, kaip siuntimo datą. 
7. Pasirinkite **OK**, kad esamą datą patvirtintumėte kaip paėmimo datą.
8. Pasirinkite **Mokėti kortele,** kad inicijuotumėte mokėjimą.
9. Naudodami kortelę įmokėkite mokėtiną depozito sumą. 
10. Užbaikite depozito mokėjimą mokėjimo terminale. 
11. Sumokėję depozitą pasirinkite parinktį naudoti tą pačią kortelę vykdymo metu ir palaukite, kol užsakymas bus įvykdytas.

Kai užsakymas paimamas, supakuojamas ir operacijų biure išrašoma jo SF, EKA pateikta mokėjimo informacija bus naudojama prekių, gabenamų klientui, lėšoms fiksuoti. 

## <a name="scenario-details"></a>Išsami scenarijaus informacija

Be pagrindinių scenarijų, kurie čia aprašyti, atlikti keli mokėjimų SDK patobulinimai, kad būtų palaikomi integruoto kanalo mokėjimai. 

### <a name="pos"></a>EKA

#### <a name="single-swipedip-for-customer-orders"></a>Vienkartinis perbraukimas kortele / kortelės įstatymas kliento užsakymuose

Prieš įdiegiant integruoto kanalo mokėjimų funkciją, kai kliento užsakymai, apimantys depozitus, buvo kuriame EKA, klientams reikėjo perbraukti kortele (arba ją įstatyti) du kartus: vieną kartą – norint sumokėti depozitą, o kitą kartą – norint sukurti kortelės atpažinimo ženklą, kuris toliau bus naudojamas vykdant užsakymą. Kai integruoto kanalo atpažinimo ženklų funkcija įjungta, klientai turi perbraukti kortele tik vieną kartą, kad sumokėtų depozitą ir patvirtintų mokėtiną sumą už prekių užsakymą, kuris bus įvykdytas vėliau. Vykdymo metu fiksuojamos patvirtintos lėšos. Prieš integruoto kanalo atpažinimo ženklų funkcijos įtraukimą buvo kuriamas tik pasikartojantis kortelių atpažinimo ženklas, skirtas toliau vykdyti užsakymą. Todėl laukiančio vykdymo lėšos nebūdavo patvirtinamos; kadangi tos lėšos nebuvo sulaikomos šiuo konkrečiu tikslu, buvo mažiau tikėtina, kad bus užfiksuotos vėliau.

> [!NOTE]
> Vienkartinis perbraukimas kortele nepalaikomas „Retail 8.1.3 versijoje. 8.1.3 versijoje kliento užsakymai naudoja tą patį srautą, kuris buvo naudojamas prieš integruoto kanalo atpažinimo ženklų funkcijos įtraukimą. 

### <a name="cards-that-cant-issue-recurring-card-tokens"></a>Kortelės, kurios negali išduoti pasikartojančių kortelių atpažinimo ženklų

Kai kurių kortų negalima naudoti atliekant integruoto kanalo mokėjimus, nes jos nepalaiko pasikartojančių kortelių atpažinimo ženklų išdavimo. Kai užsakymas sukuriamas EKA, jei depozitas sumokamas naudojant kortelę, kuri nepalaiko pasikartojančių kortelių atpažinimo ženklų, naudojamas ankstesnis kortelės atpažinimo ženklų srautas. Todėl klientas, norintis pateikti mokėjimą, kuris bus toliau naudojamas vykdant užsakymą, turi pateikti antrą kortelę. Jei antra kortelė nepalaiko pasikartojančių kortelių atpažinimo ženklų, atpažinimo ženklo veiksmas bus atmestas ir kasininkas bus paragintas paprašyti kliento pateikti kitą kortelę. 

### <a name="using-a-different-card"></a>Kitos kortelės naudojimas

Klientas, kuris atvyksta į parduotuvę paimti užsakymo, gali naudoti kitą kortelę. Kai užsakymo paėmimo metu kasininkas gauna paraginimą **Naudoti galimą mokėjimo būdą**, kasininkas gali paklausti, ar klientas nori naudoti tą pačią kortelę. Jei klientas prarado kortelę, kuri buvo naudojama kuriant užsakymą, ir nori apmokėti užsakymą naudodamas kitą kortelę, kasininkas gali pasirinkti **Naudoti kitą mokėjimo būdą**. Jei klientas vėliau grįžta paimti daugiau to paties užsakymo prekių ir pradinės kortelės autorizacija vis dar galioja, kasininkas gali dar kartą paklausti, ar klientas nori naudoti šią kortelę.

### <a name="invalid-authorizations"></a>Negaliojančios autorizacijos

Jei kortelė, naudota kuriant užsakymą, nebegalioja, kai produktai pasirenkami paimti, mokėjimo fiksavimo užklausa nepavyks. Tada EKA mokėjimo jungtis bandys sukurti naują autorizaciją ir fiksuoti naudodama tą pačią kortelės informaciją. Jei nauja autorizacija arba fiksavimas nepavyksta, kasininkui bus pranešta, kad mokėjimo nepavyko apdoroti. Tada kasininkas turi gauti naują kliento mokėjimą. 

### <a name="multiple-available-payments"></a>Keli galimi mokėjimai

Kai paimamas užsakymas, kuriame yra kelios mokėjimo priemonės ir kelios eilutės, pirmiausia kasininkas gauna raginimą **Naudoti galimą mokėjimo būdą**. Jei galima naudoti kelias korteles, kai kasininkas pasirenka **Naudoti galimą mokėjimo būdą**, esamos kortelės mokėjimo priemonių eilutės bus fiksuojamos tol, kol sumokėtas balansas už tuo metu paimamas prekes. Kasininkas negalės pasirinkti kortelės, kuri turėtų būti naudojama paimamoms prekėms apmokėti. 

## <a name="related-topics"></a>Susijusios temos

- [DUK apie mokėjimus](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
- [„Dynamics 365“ mokėjimo jungtis, skirta sprendimui „Adyen“](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3)
- [Sukonfigūruokite „BOPIS“ „Dynamics 365 Commerce“ vertinamoje aplinkoje](./cpe-bopis.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]