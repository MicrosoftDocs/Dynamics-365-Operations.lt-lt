---
title: "Mokėtinų sumų SF gretinimas"
description: "Mokėtinų sumų SF gretinimas yra tiekėjo SF, pirkimo užsakymo ir produkto gavimo kvito informacijos gretinimo procesas."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 27361
ms.assetid: 9f3dace7-05d8-4974-8f85-aca2e224876c
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 93017a6592a02505292075a2905303fabe89a3b0
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="accounts-payable-invoice-matching"></a>Mokėtinų sumų SF gretinimas

[!include[banner](../includes/banner.md)]


Mokėtinų sumų SF gretinimas yra tiekėjo SF, pirkimo užsakymo ir produkto gavimo kvito informacijos gretinimo procesas.

Gretinant dokumentus, skirtumai tarp šių dokumentų vadinami gretinimo neatitikimais. Gretinimo nesutapimai lyginami su nurodytais leistinais nuokrypiais. Jei gretinimo neatitikimas viršija leistino nuokrypio procentą ar sumą, puslapyje Tiekėjo SF ir puslapyje SF istorija ir gretinimo informacija rodomos gretinimo nuokrypio piktogramos. 

Pavyzdžiui, vienoje eilutėje įvedate 1 000 elementų (vieno vieneto kaina 1,00) pirkimo užsakymą. Pirkimo užsakymas patvirtinamas ir pateikiamas tiekėjui. Tiekėjas atsiunčia 1 000 elementų, o jūs įvedate produkto gavimo kvitą, kuriame nurodyta 1 000 elementų (vieno vieneto kaina 1,00). Elementų atsargų išlaidos atnaujinamos šia kaina. 

Gaunama SF už 1 000 elementų, kurioje kiekvienos kaina nurodyta 1,10. Jūsų juridinio subjekto strategija šiai prekių kategorijai leidžia 5 proc. grynosios vieneto kainos nuokrypį. 1,05 kaina būtų priimtina, bet 1,10 – ne. Įvedant SF informaciją, identifikuojamas kainų gretinimo nesutapimas ir galite SF įrašyti, kol nesutapimas bus išspręstas.

Galite naudoti toliau nurodytų tipų Mokėtinų sumų SF gretinimą.

-   SF bendrųjų sumų gretinimas – gretinti SF bendrąsias sumas su pirkimo užsakymo bendrosiomis sumomis. Šis SF gretinimo tipas apima mažiausiai informacijos, todėl šią parinktį galite naudoti norėdami nustatyti valdiklius, kurie minimizuotų darbuotojų laiką, kurio reikia peržiūrėti SF gretinimo informacijai.
-   Dvišalis gretinimas – gretinti SF kainos informaciją su pirkimo užsakymo kainos informacija.
-   Trišalis gretinimas – gretinti SF kainos informaciją su pirkimo užsakymo kainos informacija. Taip pat SF kiekio informaciją gretinkite su pasirinktų SF produktų gavimo kvitų kiekio informacija.
-   Išlaidų gretinimas – SF išlaidų informaciją (sumas) gretinkite su pirkimo užsakymo išlaidų informacija (sumomis).

> [!NOTE]
> Kitas SF tikrinimo formas galima atlikti naudojant tiekėjo SF strategijas. 

Dvišalio gretinimo ir trišalio gretinimo metu kainos informacija visada gretinama pagal vieneto kainą. Taip pat galite šias gretinimo strategijas sukonfigūruoti taip, kad kainos informacija būtų gretinama pagal bendrą kainą.
-   Grynosios vieneto kainos gretinimas – kainos informaciją dvišalio gretinimo ar trišalio gretinimo metu gretinkite lygindami kiekvienos SF eilutės grynąją prekės kainą su atitinkama pirkimo užsakymo grynąja prekės kaina. Grynoji vieneto kaina nustatoma pagal šią formulę: Grynoji eilutės suma / Eilutės kiekis
-   Kainų sumų gretinimas – kainos informaciją dvišalio gretinimo ar trišalio gretinimo metu gretinkite lygindami kiekvienos SF eilutės grynąją sumą (kainų sumą) su atitinkama pirkimo užsakymo grynąja suma. Grynoji suma nustatoma pagal šią formulę: (Vieneto kaina \* Eilutės kiekis) + Eilutės išlaidos – Eilutės nuolaidos

Paprastai SF gretinimo skaičiavimai automatiškai atliekami jums Tiekėjo SF puslapyje redaguojant tiekėjo SF. Taip pat SF gretinimas gali būti atliekamas pagal poreikį. Juridinio subjekto SF gretinimą pagal poreikį kontroliuoja parinktis Automatiškai atnaujinti SF antraštės būseną į, esanti Mokėtinų sumų parametrų puslapio SF tikrinimo skirtuke. SF gretinimas taip pat gali būti atliekamas kaip SF peržiūros proceso dalis. SF gretinimo rezultatus galite peržiūrėti tiekėjo SF puslapyje ir susijusiuose SF gretinimo puslapiuose.

## <a name="invoice-totals-matching"></a> Sąskaitos faktūros sumų gretinimas
Galite naudoti SF bendrųjų sumų gretinimą, kad užtikrintumėte, jog bendrosios SF sumos nenukryptų nuo numatytų sumų didesniu nei priimtinu nuokrypiu. SF bendrųjų sumų gretinimo informacijos puslapyje lyginamos šešios sumos, kaip parodyta toliau pateiktoje lentelėje. Jei leistinas SF bendrųjų sumų gretinimo nuokrypis yra 20 proc., 100 proc. bendrosios nuolaidos sumos nuokrypio procentas laikomas gretinimo neatitikimu.

| Laukas Iš viso    | Faktinė SF bendroji suma | Numatoma SF bendroji suma | Nukrypimo procentas | Gretinimo būsena |
|----------------|----------------------|------------------------|---------------------|--------------|
| Likutis        | 495,00               | 495,00                 | 0 proc.                  | Įvykdyta sėkmingai       |
| Bendra nuolaida | 0,00                 | 9,90                   | 100 %                | Nepavyko       |
| Mokesčiai        | 64,90                | 64,90                  | 0 proc.                  | Įvykdyta sėkmingai       |
| PVM      | 139,98               | 137,50                 | 2 %                  | Įvykdyta sėkmingai       |
| Apvalinimas      | 0,00                 | 0,00                   | 0 proc.                  | Įvykdyta sėkmingai       |
| Iš viso su PVM | 699,88               | 687,50                 | 2 %                  | Įvykdyta sėkmingai       |

Juridinio subjekto SF bendrųjų sumų gretinimą kontroliuoja jungiklis Gretinti sąskaitos faktūros sumas, esantis Mokėtinų sumų parametrų puslapyje. Gretinamos numatomos SF sumos ir faktinės SF sumos. Numatomos SF sumos skaičiuojamos pagal kainas, išlaidas ir PVM informaciją iš pirkimo užsakymo ir SF kiekių.

## <a name="two-way-price-totals-matching"></a> Dvišalis kainų bendrųjų sumų gretinimas
Naudokite dvišalį gretinimą, kad užtikrintumėte, jog nuokrypis tarp pirkimo užsakymo ir SF kainos informacijos yra leistinas. Kiekvienos SF eilutės ir visų laukiančių bei anksčiau užregistruotų SF eilučių grynosios sumos kainos informaciją galite palyginti su atitinkamos pirkimo užsakymo eilutės grynąja suma. Tai vadinama kainų bendrųjų sumų gretinimu. 

Kainų bendrųjų sumų gretinimas gali būti paremtas procentu, suma arba procentu ir suma. 

Jei nurodytas pirkimo kainos sumos nuokrypio procentas, lyginami penki laukai, kaip parodyta toliau pateiktoje lentelėje. Kadangi pirkimo kainos sumos nuokrypio procentas yra 10 proc., 50 proc. kainos sumos nuokrypio procentas reiškia gretinimo neatitikimą.

| Gretinimo būsena | SF grynoji suma | Numatoma grynoji suma | Nesugretinta pirkimo kainos suma (nuokrypio procentas) | Nesugretintas pirkimo kainos sumos procentas (nuokrypio procentas) | Pirkimo kainos viso leistino nuokrypio procentas |
|--------------|--------------------|---------------------|--------------------------------------------------|-----------------------------------------------------------------|----------------------------------------|
| Įvykdyta sėkmingai       | 105,00             | 100,00              | 5,00                                             | 5 %                                                              | 10 %                                    |
| Nepavyko       | 150,00             | 100,00              | 50,00                                            | 50 %                                                             | 10 %                                    |

Jei nurodyta pirkimo kainos sumos nuokrypio suma, lyginami penki laukai, kaip parodyta toliau pateiktoje lentelėje. Kadangi pirkimo kainos sumos nuokrypio suma yra 100,00, 105,00 kainos sumos nuokrypio suma reiškia gretinimo neatitikimą.

| Gretinimo būsena | SF grynoji suma | Numatoma grynoji suma | Nesugretinta pirkimo kainos suma (nuokrypio procentas) | Nesugretinta visa pirkimo kaina, išreikšta apskaitos valiuta (nuokrypio suma) | Pirkimo kainos visas leistinas nuokrypis |
|--------------|--------------------|---------------------|--------------------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| Įvykdyta sėkmingai       | 150,00             | 100,00              | 50,00                                            | 50,00                                                                   | 100,00                         |
| Nepavyko       | 205,00             | 100,00              | 105,00                                           | 105,00                                                                  | 100,00                         |

Jei kainų bendrųjų sumų gretinimas nustatytas su procentiniu nuokrypiu ir nuokrypio suma, kartais vadinama neviršytina suma, vertinant, ar eilutėje yra gretinimo neatitikimas, atsižvelgiama į abu nuokrypius. Jei procentas arba suma viršija leistiną nuokrypį, kaip parodyta toliau pateiktos lentelės eilutėse 150,00 ir 205,00, eilutėje yra gretinimo neatitikimas.

| Gretinimo būsena | SF grynoji suma | Numatoma grynoji suma | Nesugretintas pirkimo kainos sumos procentas (nuokrypio procentas) | Pirkimo kainos viso leistino nuokrypio procentas | Nesugretinta visa pirkimo kaina, išreikšta apskaitos valiuta (nuokrypio suma) | Pirkimo kainos visas leistinas nuokrypis |
|--------------|--------------------|---------------------|-----------------------------------------------------------------|----------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| Įvykdyta sėkmingai       | 105,00             | 100,00              | 5 %                                                              | 10 %                                    | 5,00                                                                    | 100,00                         |
| Nepavyko       | 150,00             | 100,00              | 50 %                                                             | 10 %                                    | 50,00                                                                   | 100,00                         |
| Nepavyko       | 205,00             | 100,00              | 105 proc.                                                            | 10 %                                    | 105,00                                                                  | 100,00                         |

Juridinio subjekto dvišalis gretinimas kontroliuojamas puslapio Mokėtinų sumų parametrai lauke Eilučių atitikimo strategija. Atsižvelgdami į pasirinktį lauke Leisti nepaisyti atitikimo strategijos, konkretaus tiekėjo, prekės, arba prekės ir tiekėjo dvipusį gretinimą galite pasirinkti puslapyje Gretinimo strategija, o konkretaus pirkimo užsakymo – Pirkimo užsakymo puslapyje.

Juridinio subjekto kainų bendrųjų sumų gretinimas kontroliuojamas lauke Gretinti kainų sumas, esančiame Mokėtinų sumų parametrų puslapyje. Tame puslapyje taip pat nurodoma pirkimo kainų sumų leistino nuokrypo procentinė dalis ir leistino nuokrypio suma (neviršytina suma).

## <a name="two-way-net-unit-price-matching"></a> Dvišalis grynųjų vieneto kainų gretinimas
Naudokite dvišalį gretinimą, kad užtikrintumėte, jog nuokrypis tarp pirkimo užsakymo ir SF kainos informacijos yra leistinas. Galite palyginti kiekvienos SF prekės grynosios vieneto kainos informaciją. Tai vadinama grynųjų vieneto kainų gretinimu. 

SF gretinimo informacijos puslapyje lyginamos devynių eilučių sumos, kaip parodyta toliau pateiktoje lentelėje. Jei leistinas grynųjų vieneto kainų gretinimo nuokrypis yra 10 proc., 22,61 proc. grynosios vieneto kainos nuokrypis laikomas gretinimo neatitikimu.

| Eilutės laukas                    | SF vertė | Pirkimo užsakymo vertė | Nukrypimo procentas | Gretinimo būsena |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Vnt. kaina                    | 55,40         | 55,38                | 0 proc.                  | Įvykdyta sėkmingai       |
| Kainos vienetas                    | 1,00          | 1,00                 | 0 proc.                  | Įvykdyta sėkmingai       |
| Pirkimo išlaidos          | 50,00         | 0,00                 | 100 %                | Nepavyko       |
| Nuolaida                      | 0,00          | 0,00                 | 0 proc.                  | Įvykdyta sėkmingai       |
| Nuolaidos procentas              | 0,00          | 0,00                 | 0 proc.                  | Įvykdyta sėkmingai       |
| Kelių eilučių nuolaida            | 0,00          | 0,00                 | 0 proc.                  | Įvykdyta sėkmingai       |
| Kelių eilučių nuolaidos procentas | 0,00          | 0,00                 | 0 proc.                  | Įvykdyta sėkmingai       |
| Grynoji suma                    | 271,60        | 221,52               | 22.61 proc.              | Nepavyko       |
| Grynoji vieneto kaina                | 67,9000       | 55,3800              | 22.61 proc.              | Nepavyko       |

Juridinio subjekto dvišalis gretinimas kontroliuojamas puslapio Mokėtinų sumų parametrai lauke Eilučių atitikimo strategija. Atsižvelgdami į pasirinktį lauke Leisti nepaisyti atitikimo strategijos, konkretaus tiekėjo, prekės, arba prekės ir tiekėjo dvipusį gretinimą galite pasirinkti puslapyje Gretinimo strategija, o konkretaus pirkimo užsakymo – Pirkimo užsakymo puslapyje. 

Juridinio subjekto grynųjų vieneto kainų gretinimas kontroliuojamas lauke Įgalinti SF gretinimo tikrinimą, esančiame Mokėtinų sumų parametrų puslapyje. Puslapyje Leistini kainų nuokrypiai galima konfigūruoti prekių, prekių grupių, tiekėjų, tiekėjų grupių, prekių ir tiekėjų derinių arba juridinio subjekto grynųjų vieneto kainų leistino nuokrypio procentus.

## <a name="two-way-price-totals-matching-and-net-unit-price-matching"></a> Dvišalis kainų bendrųjų sumų gretinimas ir grynųjų vieneto kainų gretinimas
Kainų bendrųjų sumų gretinimą ir grynųjų vieneto kainų gretinimą galite naudoti kartu. Šiame pavyzdyje laikoma, kad yra toliau pateikta konfigūracija.

-   Prekės USB atmintukas grynosios vieneto kainos leistinas nuokrypis yra 10 proc.
-   Juridinio subjekto kainų bendrųjų sumų gretinimo leistinas nuokrypis yra 15 proc. arba 500,00.

Pirkimo užsakyme yra toliau nurodyta eilutė.

| Prekės numeris | Kiekis | Vnt. kaina | Grynoji suma |
|-------------|----------|------------|------------|
| USB atmintukas   | 1000    | 10,00      | 10.000,00  |

Įvedamos trys SF, kaip parodyta toliau pateiktoje lentelėje. 3 SF yra SF gretinimo nesutapimas, nes 1 880,00 nuokrypis viršija 500,00 pirkimo kainų sumų leistino nuokrypio sumą. Gretinant kainų bendrąsias sumas, SF grynoji suma apima visas anksčiau užregistruotas sąskaitas faktūras bei SF, su kuria šiuo metu dirbate.

| Prekės numeris          | Kiekis | Vnt. kaina | Grynoji suma | Kainos gretinimas | Kainos sumos gretinimas |
|----------------------|----------|------------|------------|-------------|-------------------|
| 1 SF: USB atmintukas | 800      | 10,80      | 8 640,00   | Įvykdyta sėkmingai      | Įvykdyta sėkmingai            |
| 2 SF: USB atmintukas | 100      | 10,80      | 1 080,00   | Įvykdyta sėkmingai      | Įvykdyta sėkmingai            |
| 3 SF: USB atmintukas | 200      | 10,80      | 2 160,00   | Įvykdyta sėkmingai      | Nepavyko            |
| Bendroji suma                |          |            | 11 880,00  |             |                   |

## <a name="three-way-matching"></a>Tripusis atitikimas

Naudokite trišalį gretinimą, norėdami užtikrinti, kad nuokrypis tarp pirkimo užsakymo ir SF kainos informacijos būtų priimtinas bei užtikrinti, kad SF kiekis atitiktų atitinkamų produkto gavimo kvitų kiekį.

SF gretinimo informacijos puslapyje lyginamos tos pačios eilučių sumos, kaip ir atliekant dvišalį gretinimą. Be to, SF kiekis gretinamas su gautų produktų gavimo kvitų kiekiais. Jei SF kiekis skiriasi nuo sugretinto produkto gavimo kvito kiekio, yra kiekio gretinimo klaida.

| Eilutės laukas                    | SF vertė | Pirkimo užsakymo vertė | Nukrypimo procentas | Gretinimo būsena |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Vnt. kaina                    | 55,40         | 55,38                | 0 proc.                  | Įvykdyta sėkmingai       |
| Kainos vienetas                    | 1,00          | 1,00                 | 0 proc.                  | Įvykdyta sėkmingai       |
| Pirkimo išlaidos          | 50,00         | 0,00                 | 100 %                | Nepavyko       |
| Nuolaida                      | 0,00          | 0,00                 | 0 proc.                  | Įvykdyta sėkmingai       |
| Nuolaidos procentas              | 0,00          | 0,00                 | 0 proc.                  | Įvykdyta sėkmingai       |
| Kelių eilučių nuolaida            | 0,00          | 0,00                 | 0 proc.                  | Įvykdyta sėkmingai       |
| Kelių eilučių nuolaidos procentas | 0,00          | 0,00                 | 0 proc.                  | Įvykdyta sėkmingai       |
| Grynoji suma                    | 271,60        | 221,52               | 22.61 proc.              | Nepavyko       |
| Grynoji vieneto kaina                | 67,9000       | 55,3800              | 22.61 proc.              | Nepavyko       |

| Eilutės laukas                     | SF vertė | Gretinimo būsena |
|--------------------------------|---------------|--------------|
| SF kiekis               | 4,00          |              |
| Sugretintų gavimo dokumentų suma | 0,00          | Nepavyko       |

Juridinio subjekto trišalis gretinimas kontroliuojamas puslapio Mokėtinų sumų parametrai lauke Eilučių atitikimo strategija. Atsižvelgdami į pasirinktį lauke Leisti nepaisyti atitikimo strategijos, konkretaus tiekėjo, prekės, arba prekės ir tiekėjo trišalį gretinimą galite pasirinkti puslapyje Gretinimo strategija, o konkretaus pirkimo užsakymo – Pirkimo užsakymo puslapyje.

## <a name="charges-matching"></a> Išlaidų gretinimas
Galite naudoti išlaidų gretinimą, kad užtikrintumėte, jog išlaidų sumos nenukryptų nuo numatytų sumų didesniu nei priimtinu nuokrypiu. Kiekvieno išlaidų kodo, taikomo SF ir pirkimo užsakymui, bendrosios sumos lyginamos puslapyje Išlaidų verčių palyginimas – sąskaita faktūra: kaip parodyta toliau pateiktoje lentelėje. Jei leistinas išlaidų kodo nuokrypis yra 25 proc., 99 999 999 999,99 proc. Licencijos išlaidų kodo nuokrypio procentas laikomas gretinimo neatitikimu.

> [!NOTE] 
> 99 999 999 999,99 nuokrypio procentas reiškia, kad pagal pirkimo užsakymą numatoma suma lygi nuliui, o SF faktinė suma yra teigiama. 

| Išlaidų gretinimo būsena | SF išlaidų kodas | Faktinė visa apskaičiuota vertė | Numatoma visa apskaičiuota vertė | Nukrypimo suma | Nukrypimo procentas | Leistino nuokrypio procentas |
|----------------------|----------------------|-------------------------------|---------------------------------|-----------------|---------------------|----------------------|
| Nepavyko               | Licencija              | 25                            | 0                               | 25              | 99 999 999 999,99 proc.  | 25 %                  |
| Įvykdyta sėkmingai               | Transportavimas              | 200                           | 200                             | 0               | 0 proc.                  | 25 %                  |
| Nepavyko               | Vykdyti             | 4                             | 2                               | 2               | 100 %                | 25 %                  |

Juridinio subjekto išlaidų gretinimą kontroliuoja jungiklis Gretinti išlaidas, esantis Mokėtinų sumų parametrų puslapyje. Išlaidų leistino nuokrypio procentus galite nustatyti Leistinų išlaidų nuokrypių puslapyje.

> [!NOTE]
> Išlaidų gretinimas atliekamas tik tų išlaidų kodų, kurie pasirinkti jungikliu Palyginti pirkimo užsakymo ir SF vertes, esančiu Išlaidų kodo puslapyje.

## <a name="related-functionality"></a> Susijusios funkcijos
Tiekėjo SF dažnai yra pagrįstos produktų gavimo kvitais, kuriuose nurodomos faktinės siuntos, o ne pirkimo užsakymais. Kartais SF sumos nesutampa su pirkimo užsakymo sumomis, o kartais siuntų kiekiai nesutampa su SF nurodytais kiekiais. Padėti tvarkyti šią informaciją galite toliau nurodytais būdais.
-   Kurti tiekėjo SF pagal produktų gavimo kvitus. SF produktų gavimo kvitai pasiūlomi automatiškai, ir galima pasirinkti, kurį produkto gavimo kvitą naudoti. Jei reikia, iš keleto pirkimo užsakymų taip pat galima pasirinkti tam tikras produkto gavimo kvito eilučių prekes.
-   Peržiūrėti ir patvirtinti, ar nėra SF kiekio ir produkto gavimo kvite nurodyto gauto kiekio skirtumų. Jeigu yra skirtumas, SF galima išsaugoti ir vėliau sugretinti su kitu produkto gavimo kvitu arba pakeisti SF kiekį, kad sutaptų su gautu kiekiu.
-   Įvesti SF sumas, kurios nebuvo įtrauktos į originalų pirkimo užsakymą, kad SF informacija sutaptų su SF, kuri gauta iš tiekėjo, informacija. Galima palyginti pirkimo užsakymų išlaidas su SF išlaidomis. Jei būtina, išlaidas galima įtraukti į SF ir paskirstyti SF eilutėms.
-   Peržiūrėti ir patvirtinti SF grynosios prekės kainos ir pirkimo užsakymo grynosios prekės kainos gretinimo nesutapimus. Galite nustatyti juridinio subjekto, tiekėjų ir prekių leistino kainų nuokrypio procentus. Jeigu tiekėjo SF eilutės kaina viršija priimtiną kainos nuokrypį, galima išsaugoti SF, kol ji bus patvirtinta registruoti arba kol iš tiekėjo bus gautas pataisymas.

Daugiau informacijos žr. [Trišalės atitikimo strategijos](three-way-matching-policies.md) ir [Nustatyti mokėtinų sumų SF sugretinimo patvirtinimą](tasks/set-up-accounts-payable-invoice-matching-validation.md). 





