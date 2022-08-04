---
title: Konfigūruoti Algalapį su Adyen
description: Šiame straipsnyje aprašoma, kaip konfigūruoti Algalapį su Adyen Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 07/05/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c3f049946c66fcd8560f7c08a4cb2beab0dcd5b2
ms.sourcegitcommit: 3d2c0a39c4f987e9ac71df2f2fa6df0f64f10b2b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2022
ms.locfileid: "9115016"
---
# <a name="configure-google-pay-with-adyen"></a>Konfigūruoti Algalapį su Adyen

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip konfigūruoti Algalapį su Adyen Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce siūlo papildomą integravimą į Lauką Mokėti, kai naudojama Adyen mokėjimo šliuzo paslauga. "Arba Pay" yra skaitmeninis mokėjimo būdas, kuris naudoja "Vz." mokėjimo prekybininko sąskaitą pagal Adyen mokėjimų tarnybą. Kai šis mygtukas sukonfigūruojamas, internetinio užsakymo išregistravimo metu, mygtukas Alga pay galimas kaip galimas pasirinkti mokėjimo būdas. Kai vartotojai palaikomoje **naršyklėje** ar įrenginyje pasirenka Algalapio mokėjimą, jie tiesiai tiesiai per "Alga" paslaugą yra nukreipti į mokėjimą. Tada jis grąžinamas į interneto parduotuvės iš anksto, kad būtų užbaigtas užsakymas.

Kai Cb Pay naudojamas su s express checkout moduliu komercijoje, vartotojo mokėjimo sąskaitos informacija automatiškai užpildoma išregistravimo forma, kad vartotojas būtų lengviau pereiti per tikrinimo procesą. "Commerce" apima mokėjimų siųstų modulių, įgalinančių siųstų čekių elgseną. Mokėjimo siųstas modulis gali būti naudojamas fragmente, kuris įtrauktas į čekio ar krepšelio puslapį. "Dynamics 365" mokėjimo jungtis, skirta "Alga Pay" jungties nuorodai, naudojama kartu su "Dynamics 365" mokėjimo jungtimi Adyen, kad būtų įgalintos ir siųstos, ir įprastos PayPal pasirinktys. "Blok Pay" taip pat galima sukonfigūruoti su Adyen mokėjimo terminalais ir "Commerce point of sale" (EKA) naudoti parduotuvėje.

## <a name="key-terms"></a>Pagrindiniai terminai

| Semestras | Aprašymas |
|---|---|
| Algalapių mokėjimas | Taip pat vadinamas "Alga Pay" mygtuku "Alga Pay" yra mokėjimas, kurį palaiko Adyen jungtis. Tai įgalina klientų patirtį ir integravimą, kuriuos palaiko "Dynamics Paslaugos mokėjimo jungtis". |
| Piniginė | Mokėjimo tipas, į kurį nėra įtrauktos tradicinės mokėjimo charakteristikos, pvz., banko identifikavimo numerio (TALPYKLOS) diapazonas ir galiojimo data, naudojami kredito ir debeto kortelių tipams atskirti. |
| Mokėjimo siųsti modulis | Modulis Dynamics 365 Commerce, kuris palaiko spartesnį tikrinimo elgseną su palaikomais mokėjimo metodais. |

## <a name="prerequisites"></a>Būtinieji komponentai

Naudojant Alga algalapį su Adyen komercijoje reikia Banko prekybininko sąskaitos. Informacijos apie tai, kaip nustatyti jūsų Merchant Sąskaitą, [ieškokite "Adyen" dokumentacijoje apie Jav](https://docs.adyen.com/payment-methods/google-pay/) mokėjimo ir Išsiregistravimo [integravimo kontrolinį sąrašą](https://developers.google.com/pay/api/web/guides/test-and-deploy/integration-checklist).

Jūsų Adyen sąskaitoje taip pat turi būti integruotas Arba mokėjimo būdas. Norėdami gauti integravimo saitų instrukcijų, [žr. Adyen Alga pay](https://www.adyen.com/payment-methods/google-pay).

Taip pat turite įjungti patobulintą valdymo Dynamics 365 Commerce priemonės funkciją. Eikite **į darbo sričių \> funkcijų valdymą**, ieškokite patobulintos **patobulintos** pagalbos ir mokėjimo pagerinimų funkcijos, pasirinkite funkciją, tada pasirinkite **Įgalinti**. Įgalinę funkciją paleiskite **1110 paskirstymo grafiką**, kad pakeitimas būtų prieinamas visuose kanaluose.

## <a name="map-the-google-pay-payment-method"></a>Susieti algalapių mokėjimo metodą

Paslaugos mokėjimas yra skaitmeninis mokėjimo būdas. Daugiau informacijos apie tai, kaip nustatyti "Vz." mokėjimo susiejimą, žr. [Paslaugos mokėjimų palaikymą](../wallets.md).

Norėdami susieti "Vz.Pay" mokėjimo būdą su mokėjimo kortelių tipais ir EKA, ir interneto kanalams, atlikite šiuos veiksmus.

1. "Commerce Headquarters" eikite į " **Retail" ir "Commerce \> Channel" mokėjimo \> būdų \> kortelių tipus**.
1. Pasirinkti **Nauja**, jei norite įtraukti Eilutės lauką Algalapis.
1. ID lauke **įveskiteVz**.Pay **·**.
1. Lauke Elektroninio **mokėjimo vardas** įveskite Algalapių **mokėjimas**.
1. Tipo lauke **įveskite Pagal vertę** **.**
1. Lauke Išdavėjas **įveskite** **Paslaugos**.
1. Veiksmų srityje pasirinkite Procesoriaus susiejimas **, kad** atidarytumėte procesoriaus **mokėjimo susiejimo** metodų dialogo langą.
1. Atsiedami **procesoriaus** mokėjimo metodus, pamatysite nesusietų procesoriaus mokėjimo metodų sąrašą, kiekvienas iš jų yra susietas su atitinkama jungtimi. Norėdami susieti nesusietus "Rastos" mokėjimo priemonės procesoriaus mokėjimo būdus su mokėjimo kortelių tipais, kiekvienam mokėjimo priemonės tipui atlikite šiuos veiksmus:

    1. Dalyje **Mokėjimo kortelių tipai** pasirinkite mokėjimo kortelės mokėjimo priemonės tipą.
    1. **Stulpelyje Nesusieti** **procesoriaus mokėjimo būdai pasirinkite "Dynamics 365" mokėjimo jungtį Adyen** jungčiai (skirta naudoti EKA) **ir "Dynamics 365" mokėjimo jungtį "Alga Pay**" jungtis (skirta naudoti interneto kanaluose).
    1. Pasirinkite **Įtraukti**. Pasirinkimai pridedami prie stulpelio **Susieti procesoriaus mokėjimo** būdai.

1. Baigę susieti mokėjimo metodus, pasirinkite **Įrašyti**.
1. Puslapyje Kortelių **tipai** pasirinkite **Įrašyti**.

## <a name="configure-a-commerce-online-store-for-google-pay"></a>Konfigūruoti "Commerce" internetinę saugyklą, kad būtų galima naudoti "Algalapių"

Norėdami konfigūruoti "Commerce" internetinę saugyklą, kad būtų galima naudoti Algalapį, atlikite šiuos veiksmus.

1. "Commerce Headquarters" eikite į mažmeninės **prekybos ir komercijos \> kanalų \> interneto parduotuves**.
1. Pasirinkite svetainės interneto parduotuvės kanalą pasirinkdami kanalo mažmeninės prekybos kanalo **ID** reikšmę.
1. Mokėjimo sąskaitų **"** FastTab", kuris yra jungties **dalyje**, patvirtinkite, **kad "Dynamics 365" mokėjimo jungtis, skirta Adyen jungčiai**, yra įtraukta į sąrašą. Jei jo nėra, vadovaukitės instrukcijomis, [pateikiamomis nustatyti "Dynamics 365" mokėjimo jungtį Adyen](adyen-connector-setup.md), kad ją pridėtų.

    > [!NOTE]
    > Daugeliu atvejų "Dynamics 365" mokėjimo jungtis, skirta Adyen **jungčiai,** turi būti įrašyta kaip pirmoji jūsų kanalo jungtis (pirmoji jungtis taip pat vadinama pirmine jungtis). Po jo turi būti naudojamos kitos jungties, pvz., **"Dynamics 365" mokėjimo jungtis, skirta "PayPal** **" ir "Dynamics 365" mokėjimo jungtis, skirta "Iki"** jungtis.

1. Įtraukę **"Dynamics 365" mokėjimo jungtį, for Adyen** jungtį, pasirinkite Įtraukti, **·** **kad pridėtumėte "Dynamics 365" mokėjimo jungtį, for TSPay** jungtį. Tada nustatykite šias jungties ypatybes.

    | Laukas                  | Aprašymas | Būtinas | Automatiškai nustatyti | Pavyzdžio vertė |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Rinkinio pavadinimas          | "Dynamics 365" mokėjimo jungties, skirtosVzpay, surinkimo pavadinimas. | Taip | Taip | *Dvejetainis pavadinimas* |
    | Tarnybos paskyros ID     | Unikalus prekybininko ypatybės nustatymo identifikatorius. Šis identifikatorius yra antspauduotas mokėjimo operacijose ir identifikuoja prekybininko ypatybes, kurias turi naudoti proceso pabaigos procesai (pvz., SF išrašymas). | Taip | Taip | *GUID* |
    | Jūsų prekybininko ID     | ĮveskiteVz. prekybininko ID, priskirtą jūsų Lauk. Prekybininko sąskaitai. Ši ypatybė būtina gamybos aplinkose, bet ji yra pasirinktinė tikrinimo aplinkose. Norėdami gauti daugiau informacijos, apsilankykite <https://pay.google.com/>. | Taip | Ne | *Skaitinis identifikatorius* |
    | Prekybininko sąskaitos ID    | Įveskite unikalų Adyen prekybininko identifikatorių. Ši vertė pateikiama, kai prisiregistruojate Adyen, kaip [aprašyta Registruotis Adyen](adyen-connector-setup.md#sign-up-with-adyen). | Taip | Ne | *Prekybininko identifikatorius* |
    | Debesies API raktas          | Įvesti Adyen debesies API raktą. Norėdami gauti šį raktą, vadovaukitės instrukcijomis [, kaip gauti API raktą](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key). | Taip | Ne | "abcdefg" |
    | Šliuzo aplinka    | Adyen šliuzo aplinka, prie kurios reikia susieti. Galimos vertės yra Bandymas **ir** Tiesioginis **·**. Šį lauką turėtumėte nustatyti tik gamybos **įrenginiams** ir operacijoms tiesiogiai naudoti. | Taip | Taip | "Live" |
    | Palaikomos valiutos   | Valiutos, kurias turėtų apdoroti jungtis. Dabartiniuose kortelių scenarijuose Adyen gali palaikyti papildomas [valiutas](https://www.adyen.com/pos-payments/dynamic-currency-conversion), naudojant dinaminį valiutos konvertavimą po to, kai operacijos užklausa siunčiama į mokėjimo terminalą. Susisiekite su Adyen palaikyme, kad gautumėte palaikomų valiutų sąrašą. | Taip | Taip | "USD; EUR |
    | Palaikomi mokėjimo priemonių tipai | Mokėjimo priemonių tipai, kuriuos turi apdoroti jungtis. | Taip | Taip | "Turi būti" iš "Turi būti" |

1. Nustatę jungties ypatybes, **vykdykite 1070 (** kanalo konfigūracijos) paskirstymo grafiko užduotį.

## <a name="configure-commerce-pos-for-google-pay"></a>Konfigūruoti "Commerce POS", kad būtų galima naudoti "Algalapių" užmokestį

EKA konfigūracija naudoja **Adyen aparatūros šablono EFT** paslaugos lauko parametrą, kurį naudoja "Dynamics 365" mokėjimo jungtis. Informacijos apie tai, kaip sukonfigūruoti elektroninio lėšų pervedimo (EFT) paslaugą" Dynamics 365 Payment Connector Adyen programoje "Commerce Headquarters", [žr. skyrių "Dynamics 365 POS" aparatūros šablonas](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile).

"Adyen" jungties procesoriaus susiejimas fiksuoja kortelių tipus, kurie buvo naudojami EKA terminale.

### <a name="use-the-payment-express-module-with-google-pay"></a>Naudoti mokėjimo siųstų modulį su Algalapių mokėjimu

"Commerce Payment Express" modulis veikia su palaikymo mokėjimo būdais, kad suteiktų klientams galimybę išsiregistruoti greičiau, naudojant jų mokėjimų tarnybos sąskaitos informaciją per išsiregistravimo procesą. Mokėjimo siųsimo modulis nurodo sukonfigūruotą jungties mygtuką ir grąžina vartotojo pasirinkto užsakymo informaciją (adresą, kontaktinę informaciją ir mokėjimo būdą), kad būtų iš anksto užpildyta tikrinimo forma.

Kai siųstų mokėjimų modulis naudojamas su Algalapių mokėjimu, jei klientai atsidarys mokėjimo sąsąnaudos skyriuje Algalapių **mokėjimų** iframe langas. Tada vartotojai gali prisiregistruoti prie savo Buhalterio sąskaitos, kad galėtų naudoti savo sąskaitos siuntimo adresą, sąskaitų siuntimo adresą, el. pašto adresą ir Jūsų mokėjimo už operacijas mokėjimo būdą.

Kai vartotojai baigia veiksmą lange Algalapis, jie nukreipiami į Komercijos svetainės tikrinimo puslapį, kur čekio forma iš anksto užpildoma "Alga" mokėjimo sąskaitos informacija. Vartotojams grįžus į išregistrimo puslapį iš Lango Į išregistravimas, jie matys šią informaciją:

- Mokėjimo sraute, pirma pristatymo pasirinktis, galima pristatymo adresu, kuris buvo grąžintas, bus iš anksto parinkta klientui.
- Kai naudojamas Algalapis, negrąžinas joks kontaktinio el. pašto adresas. Svečio išregistravimas vartotojams turės įvesti el. pašto adresą į išsiregistravimo puslapio kontaktų skyrių. Prisiregistravę vartotojai turi automatiškai užpildytus kontaktinius duomenis iš savo "Dynamics" kliento sąskaitos (pagrindinis el. pašto adresas, kurį jie naudojo autentifikuoti).

Klientai turi pasirinktį peržiūrėti užsakymus ir pakeisti užsakymo tikrinimo informaciją prieš jiems **pasirinkus Užsakymo** vietą užsakymui užbaigti.

### <a name="configure-google-pay-in-site-builder"></a>Konfigūruoti Algalapį svetainės generatoriuje 

Prieš konfigūrdami savo fragmentus ar puslapius naudodami Algalapių užmokestį, turite užtikrinti, kad jūsų svetainės turinio saugos strategijos nustatytos Komercijos svetainės generatoriuje.

Norėdami užtikrinti, kad jūsų turinio saugos strategijos nustatytos svetainės generatoriuje, atlikite šiuos veiksmus.

1. Savo svetainėje eikite į svetainės **parametrų \> plėtinius**.
1. Skirtuke Turinio saugos strategija pridėkite eilutę, **kuri** skirta antriniams src`*.google.com`, **connect-src**,**rėmų** originalams, **rėmų src**, **img-src**, **scenarijaus-src** **ir stiliaus-src** nurodymams.**·**
1. Baigę pasirinkite Įrašyti ir **publikuoti**.

### <a name="configure-the-payment-express-fragment-with-google-pay-in-site-builder"></a>Konfigūruoti mokėjimo siųstų fragmentų naudojant Algalapių mokėjimų svetainės generatorių

Norėdami nustatyti siųstų mokėjimų fragmentą naudodami interneto parduotuvės Algalapį, atlikite šiuos veiksmus.

1. Svetainės generatoriuje eikite į **fragmentus**.
1. Pasirinkite **Nauja**.
1. Dialogo lange **Naujas fragmentas** pasirinkite konteinerio **modulį**, įveskite fragmento pavadinimą (pvz., **Express Checkout**), tada pasirinkite **Gerai**. 
1. Pasirinkite naujo fragmento numatytąją konteinerio **atminties atminties** talpyklą.
1. Dešinėje pusėje esančioje ypatybės srityje nustatykite konteinerio modulio ypatybes:

    - **Antraštė** – įveskite antraštę, jei norite rodyti s express checkout sekciją savo svetainei (pvz., Express **Checkout**).
    - **Konteinerio maketas** – pasirinkite **srautą**.
    - **Plotis** – pasirinkite užpildymo **konteinerį**.
    - **Rodomi tik** **trys**– pasirinkite Trys, jei norite nurodyti vaikų skaičių, kuris atitinka čekio puslapio s express checkout sekcijos eilutę (pvz., teksto lauką, mokėjimo siųstas "PayPal" ir mokėjimą, siųstas "Pay").
    - **CSS klasės pavadinimas** – įveskite **msc-express-payment-container** (būtina).

    > [!IMPORTANT]
    > - Klasės **CSS pavadinimo reikšmė** turi būti nustatyta kaip **msc-express-payment-container**, kad būtų galima valdyti konteinerio veikimo būdą atliekant išregistravimas. Ši elgsena apima slėpimą, sugretinėjimą ir kitus veiksmus, kurie taikomi siųsto tikrinimo sekcijai tikrinimo srauto metu. Msc-express-payment-container **klasė** veikia su numatytosios operacijos, kurios išleistos su modulių bibliotekos tikrinimo moduliu.
    > - Papildomus stilius galima įtraukti kartu su **CSS klasės pavadinimu**. Jei pritaikote modulio elgseną, kryžminio tikrinimo stiliaus valdiklius, jei naudojate tos pačios modulių bibliotekos užsakytą veikimo būdą tikrinimo modulyje dėl s express checkout veikimo būdo.

1. Numatytame konteinerio **laiko** atminties atminties lape pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite siųsdami **modulį** Mokėjimas ir pasirinkite **Gerai**.
1. **Mokėjimo siųsto** modulio ypatybės **srityje nustatykite iFrame** arba koreguokite vertės aukštį pikseliais (pvz., **60**).
1. Lauke Palaikomų **mokėjimo priemonių** tipai įveskite **KalendoriųPay**. Vertė turi **atitikti** kanalui nustatytą jungtį palaikomų mokėjimo priemonių tipų eilutę ([kaip aprašyta anksčiau šiame straipsnyje skyriuje "Commerce online store for Alga"](#configure-a-commerce-online-store-for-google-pay) sukonfigūruokite).

    > [!NOTE]
    > Norėdami pridėti skubius mokėjimo modulius kitiems mokėjimo metodams, galite **pakartoti** 6–9 veiksmus. Sulygiuoti **palaikomų mokėjimo** priemonių tipų vertę su papildomais sukonfigūruotais mokėjimo tipais (pvz., **Paypal**).

1. Pasirinktinai: galite įtraukti teksto bloko modulį į numatytąjį konteinerio modulį, kad įtraukdami instrukcijas arba informacijos gavimo informaciją. Įtraukę modulį, ypatybės srityje įveskite norimą tekstą raiškiojo **teksto** lauke. Tekstą galite padėti virš arba po mokėjimo skubiais moduliais, pasirinkdami elipsę (**...**) **·** **·** **teksto blokavimo atminties dalyje ir pasirinkdami Perkelti aukštyn arba Perkelti žemyn**.
1. Jei **norite** įrašyti pakeitimus, pasirinkite Įrašyti, tada – **Baigti redaguoti**.
1. Norėdami **publikuoti fragmentą**, pasirinkite Publikuoti.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Įtraukti mokėjimo s express fragmentą į tikrinimo puslapį

Norėdami pridėti siųstų mokėjimų fragmentą į tikrinimo puslapį, atlikite šiuos veiksmus.

1. Svetainės generatoriuje, **eikite į puslapius** ir pasirinkite savo svetainės tikrinimo puslapį.
1. Pasirinkite **Redaguoti**.
1. Pagrindiniame laiko **atminties atminties** lape pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite konteinerio **modulį**, tada pasirinkite **Gerai**.
1. Dešinėje pusėje esančioje ypatybės srityje nustatykite konteinerio modulio ypatybes:

    - **Konteinerio maketas** – pasirinkite **Suspausta**.
    - **Plotis** – pasirinkite užpildymo **konteinerį**.
    - **Parodyta vaikų** – **pasirinkite** Trys, jei norite nurodyti vaikų skaičių, kuris bus tinkamas "Express checkout" puslapio skyriaus eilutėje (pvz., teksto laukas, mokėjimo siųstas "PayPal" ir mokėjimas " Express for Pay").

1. Konteinerio **modulio** laiko atminties dalyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **fragmentą**.
1. Dialogo lange **Pasirinkti fragmentą** pasirinkite siųstas mokėjimo fragmentą, kurį sukūrėte, tada pasirinkite **Gerai**.
1. Jei **norite** įrašyti pakeitimus, pasirinkite Įrašyti, tada – **Baigti redaguoti**.
1. Pasirinkite **Publikuoti** ir publikuokite puslapį.

> [!NOTE]
> Jei tikrinimo puslapyje jau yra konteineris, kuriame yra tikrinimo fragmentas, o jūs norite, kad mokėjimo sąstingio modulis būtų atvaizduotas virš įprasto išregistravimo konteinerio, galite padėti jį virš arba po esamo išregistravimo, pasirinkdami daugtaškį (...) **pagrindinėje laiko atžymoje ir** **pasirinkdami Perkelti aukštyn arba** Žemyn **.** **·**

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Įtraukti mokėjimo s express fragmentą į krepšelio puslapį

Norėdami įtraukti mokėjimo s express fragmentą į krepšelio puslapį, atlikite šiuos veiksmus.

1. Svetainės generatoriuje eikite **į puslapius** ir pasirinkite svetainės krepšelio puslapį.
2. Pasirinkite **Redaguoti**.
3. Struktūros rodinyje išplėskite medžio rodinio pagrindinį **atsk.** atminties laiką ir raskite konteinerį, kuriame yra krepšelio **modulis**.
4. Krepšelio **modulyje** pasirinkite " **Payment Express** " atminties laiką, pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
5. Dialogo lange **Pasirinkti modulius** pasirinkite siųsdami **modulį** Mokėjimas ir pasirinkite **Gerai**.
6. Pasirinkite mokėjimo siųsimo **modulio** laiko atminties lauką. Tada, dešinėje, po Palaikomų mokėjimo priemonių tipais, **ypatybės srityje** įveskite **Iki.** Vertė turi atitikti **kanalui** nustatytą jungtį palaikomų mokėjimo priemonių tipų eilutę ([kaip aprašyta anksčiau šiame straipsnyje skyriuje "Commerce online store for Alga"](#configure-a-commerce-online-store-for-google-pay) sukonfigūruokite).
1. Jei **norite** įrašyti pakeitimus, pasirinkite Įrašyti, tada – **Baigti redaguoti**.
1. Pasirinkite **Publikuoti** ir publikuokite puslapį.

Vartotojai krepšelyje "Payment Express" gali **įtraukti iki trijų palaikomų "Payment Express** " modulių (kitaip tariant, trys galimos palaikomos **mokėjimo parinktys**).

### <a name="set-up-google-pay-as-an-option-in-the-checkout-payment-section"></a>Mokėjimų čekiu skyriaus pasirinktį nustatyti kaip pasirinktį

Galite nustatyti Tik mokėjimų čekio mokėjimo skyriaus pasirinktį, jei funkcija nėra skubus. Čekio formą užpildys vartotojas, o Paslaugos mokėjimo puslapis galėsite tik išregistravimas mokėti Čekiu pagal Čekio mokėjimą. Jei norite perrašyti išsamią užpildyto čekio informaciją, dk sąskaitos informacija nebus naudojama.

> [!NOTE]
> Toliau pateiktoje procedūroje laikoma, kad jūsų svetainė naudoja tikrinimo fragmentą, kuris sukonfigūruotas su paėmimo informacija, siuntimo adresu, pristatymo pasirinktimis, kontaktinė informacija, nebūtinomis sąlygomis ir tikrinimo elementų sekcija. Numatytasis modulio bibliotekos tikrinimo modulis išleidžiamas su tikrinimo skyriaus konteineriu, kuriame yra teksto blokavimas, lojalumo taškai, dovanų kortelė ir mokėjimo moduliai. Daugiau informacijos rasite Mokėjimo [modulyje](../payment-module.md).

Norėdami čekių apmokėjimo puslapio skyriuje Mokėjimo būdas **nustatyti** Čekio mokėjimą kaip reguliarią mokėjimo pasirinktį, atlikite šiuos veiksmus.

1. Svetainės generatoriuje eikite **į** fragmentus ir pasirinkite svetainės tikrinimo fragmentą.
1. Pasirinkite **Redaguoti**.
1. Informacijos laiko **atminties išraše** pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti** modulius pasirinkite mokėjimo **modulį** ir pasirinkite **Gerai**.
1. Mokėjimo modulio **dešinios** ypatybės srityje nustatykite konteinerio modulio ypatybes:

    - **Antraštė** – įveskite antraštę, jeigu norite rodyti s express checkout sekciją savo svetainei (pvz., **Algaus mokėjimas**).
    - **Aukščio vertė iFrame** – pakeiskite vertę į pageidaujamą dizaino aukštį pikseliais (pvz., **75**). 
    - **Palaikomi mokėjimo priemonių** tipai – **įveskite "AlgaPay** ", kad atitiktų "Commerce Headquarters" "Vz." jungties konfigūraciją.
    - **Yra pirminis mokėjimas** – palikite žymės langelį išvalytą. (Ši ypatybė paprastai įgalinamas Adyen tikrinimo modulyje.)
    - **Mokėjimo stiliaus perrašymo** – ši ypatybė nepalaikoma "Vz." mokėjimo konfigūracijoje.
    - **Naudoti jungties ID** – šią ypatybę reikia pasirinkti, jei puslapyje naudojamos kelios mokėjimo jungties.

1. Nustatykite modulį virš kitų mokėjimo modulių arba po kitais mokėjimo moduliais, pasirinkdami elipsę (**...**) **·** **mokėjimo laiko atminties dalyje ir pasirinkdami** Perkelti aukštyn arba **Perkelti žemyn.**
1. Jei **norite** įrašyti pakeitimus, pasirinkite Įrašyti, tada – **Baigti redaguoti**.
1. Pasirinkite **Publikuoti**.

### <a name="modes-of-delivery"></a>Pristatymo būdai

Naudojant siųstų mokėjimo modulį, naudojantį Algalapių mokėjimo modulį, pirma pristatymo pasirinktis, grąžinta pagal pasirinktą siuntimo adresą iš Patams. mokėjimo sąskaitos, bus iš anksto pasirinkta. Vartotojai gali koreguoti siuntimo adresą pagal kitą pasirinktį, jei norite.

Užsakymas, kuriame rodomi pristatymo metodai mokėjimo siųstame **modulyje**, yra sukonfigūruotas kanalo pristatymo būdų puslapyje "Commerce Headquarters". "Commerce Headquarters" eikite į mažmeninės **prekybos ir \> komercijos kanalų \>** **interneto parduotuves ir savo parduotuvei pasirinkite mažmeninės prekybos kanalo ID** reikšmę. Veiksmų srities skirtuke Nustatymas **pasirinkite** Pristatymo **būdai**. Išvardyti pristatymo būdai bus rodomi tame pačiame mokėjimo s express modulio užsakyme. Pasirinkite **Valdyti pristatymo būdus veiksmų** srityje, kad įtraukumėte arba pašalintumėte mažmeninės prekybos kanalo ar produkto pristatymo būdus. Daugiau informacijos apie tai, kaip nustatyti pristatymo būdus, ieškokite [Nustatykite pristatymo būdus](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Tikrinimo modulis taip pat naudoja pristatymo parinkčių modulį, kai pristatymo būdai atvaizduojami išregistravimo metu. Daugiau informacijos rasite pristatymo [pasirinkčių modulyje](../delivery-options-module.md).

Pristatymo būdai rodomi taip, kaip jie įtraukti į **interneto parduotuvės pristatymo** būdų sąrašą.

## <a name="additional-resources"></a>Papildomi ištekliai

[DUK apie mokėjimus](payments-retail.md)

[Pirkimo užbaigimo modulis](../add-checkout-module.md)

[Mokėjimo modulis](../payment-module.md)
