---
title: Optimalaus persidengiančių nuolaidų derinio nustatymas
description: Kai nuolaidos persidengia, turite nustatyti persidengiančių nuolaidų derinį, kurį naudojant bus sukuriama mažiausia bendroji operacijos suma arba didžiausia bendroji nuolaidos suma. Kai nuolaidos suma kinta priklausomai nuo įsigytų produktų kainos, pavyzdžiui, kaip dažnai pasitaikančiu mažmeninės prekybos nuolaidų atveju „Pirkdami 1 gaukite 1 X procentų nuolaidą“ (BOGO), šis procesas tampa kombinacinio optimizavimo problema.
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount,
audience: Application User, IT Pro
ms.reviewer: josaw
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.region: global
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 747c67812b0a357c35778c82531e9db7e99e510b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972712"
---
# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a>Optimalaus persidengiančių nuolaidų derinio nustatymas

[!include [banner](includes/banner.md)]

Kai nuolaidos persidengia, turite nustatyti persidengiančių nuolaidų derinį, kurį naudojant bus sukuriama mažiausia bendroji operacijos suma arba didžiausia bendroji nuolaidos suma. Kai nuolaidos suma kinta priklausomai nuo įsigytų produktų kainos, pavyzdžiui, kaip dažnai pasitaikančiu mažmeninės prekybos nuolaidų atveju „Pirkdami 1 gaukite 1 X procentų nuolaidą“ (BOGO), šis procesas tampa kombinacinio optimizavimo problema.

Šis straipsnis taikomas programai „Microsoft Dynamics AX 2012 R3“ su „KB 3105973“ (išleista 2015 m. lapkričio 2 d.) arba naujesnei versijai ir „Dynamics 365 Commerce“. Norėdami nustatyti, kad nuolaidų persidengimo derinys būtų taikomas reikiamu laiku, pristatėme persidengiančių nuolaidų taikymo metodą. Šį metodą vadiname **ribos vertės vertinimas**. Ribos vertės vertinimas naudojamas tada, kai laikas, reikalingas norint įvertinti galimus persidengiančių nuolaidų derinius, viršija ribinę reikšmę, kurią galima sukonfigūruoti puslapyje **„Commerce“ parametrai**. Taikant ribos vertės vertinimo metodą apskaičiuojama kiekvienos persidengiančios nuolaidos vertė taikant nuolaidos vertę bendrai naudojamiems produktams. Persidengiančios nuolaidos taikomos nuo didžiausios santykinės vertės iki mažiausios santykinės vertės. Išsamią informaciją apie naują metodą rasite toliau šiame straipsnyje pateiktame skyriuje „Ribos vertė“. Ribos vertės vertinimas nenaudojamas, kai produkto nuolaidos sumoms neturi įtakos kitas operacijos produktas. Pavyzdžiui, šis metodas nenaudojamas dviems paprastoms nuolaidoms arba paprastai nuolaidai ir vieno produkto kiekio nuolaidai.

## <a name="discount-examples"></a>Nuolaidų pavyzdžiai

Bendram produktų rinkiniui galite sukurti neribotą nuolaidų skaičių. Tačiau, kadangi nėra apribojimo, bandant apskaičiuoti nuolaidas, kurios turėtų būti naudojamos įvairiems produktams, gali atsirasti našumo trikčių. Toliau pateikiamuose pavyzdžiuose ši problema pavaizduota išsamiau. 1 pavyzdyje pradedame su dviem produktais ir dviem persidengiančiomis nuolaidomis. 2 pavyzdyje rodoma, kaip problema didėja įtraukiant daugiau produktų.

### <a name="example-1-two-products-and-two-discounts"></a>1 pavyzdys: du produktai ir dvi nuolaidos

Šiame pavyzdyje norint, kad būtų taikoma kiekviena nuolaida, reikia dviejų produktų ir nuolaidų negalima sujungti. Šio pavyzdžio nuolaidos yra nuolaidos **Geriausia kaina**. Abiems produktams gali būti taikomos abi nuolaidos. Toliau nurodomos dvi nuolaidos.

![Dviejų geriausių kainos nuolaidų pavyzdys](./media/overlapping-discount-combo-01.jpg)

Kuri iš šių dviejų produktų nuolaidų bus geresnė, priklauso nuo abiejų produktų kainos. Kai abiejų produktų kaina lygi arba beveik lygi, geriau naudoti 1 nuolaidą. Kai vieno produkto kaina žymiai mažesnė negu kito produkto kaina, geriau naudoti 2 nuolaidą. Toliau pateikiama šių dviejų nuolaidų vertinimo viena kitos atžvilgiu matematinė taisyklė.

![Nuolaidų įvertinimo taisyklė](./media/overlapping-discount-combo-02.jpg)

> [!NOTE]
> Kai 1 produkto kaina yra lygi dviem trečdaliams 2 produkto kainos, nuolaidos yra vienodos. Šiame pavyzdyje 1 nuolaidos įsigaliojimo procentinė dalis kinta nuo kelių procentų (kai dviejų produktų kainos itin skiriasi viena nuo kitos) iki maksimalios 25 procentų procentinės dalies (kai dviejų produktų kaina vienoda). 2 nuolaidos įsigaliojimo procentinė dalis yra fiksuota. Ji visada lygi 20 procentų. Kadangi 1 nuolaidos įsigaliojimo procentinės dalies intervalas gali būti didesnis arba mažesnis už 2 nuolaidą, geriausia nuolaida priklauso nuo dviejų produktų kainos, kuriems turi būti taikoma nuolaida. Šiame pavyzdyje skaičiavimas atliekamas greitai, nes taikomos tik dvi nuolaidos ir tik dviems produktams. Galimi du deriniai: vieną kartą taikoma 1 nuolaida arba vieną kartą taikoma 2 nuolaida. Nėra derinių, kuriuos reikėtų apskaičiuoti. Kiekvienos nuolaidos vertė apskaičiuojama naudojant abu produktus ir naudojama didžiausia nuolaida.

### <a name="example-2-four-products-and-two-discounts"></a>2 pavyzdys: keturi produktai ir dvi nuolaidos

Toliau bus naudojami keturi produktai ir tos pačios dvi nuolaidos. Visiems keturiems produktams gali būti taikomos abi nuolaidos. Yra dvylika galimų derinių. Galiausiai dvi nuolaidos bus taikomos vienu iš šių trijų derinių: du kartus taikoma 1 nuolaida, du kartus taikoma 2 nuolaida arba vieną kartą taikoma 1 nuolaida ir vieną kartą taikoma 2 nuolaida. Norėdami pavaizduoti galimus derinius peržiūrėsime du skirtingus iš keturių skirtingų kainų produktų sudarytus rinkinius.

- Visų produktų kaina vienoda – 15,00 dol. Šiuo atveju geriausias nuolaidų derinys yra du kartus taikoma 1 nuolaida. Du produktai bus parduodami be nuolaidos, o du – su 50 proc. nuolaida. Bendra operacijos nuolaidos suma yra 45 dol. (15 + 15 + 7,50 + 7,50), o tai yra 15 dol. (25 procentų) nuolaida nuo bendros 60 dol. siekiančios sumos be nuolaidos. 2 nuolaida yra tik 12 dol. (20 procentų).
- Du produktai kainuoja po 20 dol., vienas produktas kainuoja 15 dol. ir vienas produktas – 5 dol. Šiuo atveju geriausias nuolaidų derinys yra vieną kartą taikoma 2 nuolaida ir vieną kartą taikoma 1 nuolaida. Šios nuolaidos pavaizduotos toliau pateiktose lentelėse.

Norėdami perskaityti šias lenteles, naudokite vieną produktą iš eilutės ir vieną produktą iš stulpelio. Pavyzdžiui, 1 nuolaidos lentelėje sujungę du 20 dol. vertės produktus gaunate 10 dol. nuolaidą. 2 nuolaidos lentelėje sujungę 15 dol. ir 5 dol. vertės produktus gaunate 4 dol. nuolaidą.

![Pavyzdys, naudojantis keturis produktus, kuriems taikomos dvi tos pačios nuolaidos](./media/overlapping-discount-combo-03.jpg)

Pirmiausia randame didžiausią galimą nuolaidą, kuri gali būti pritaikyta bet kuriems dviem produktams naudojant bet kurią nuolaidą. Dviejose lentelėse nurodomos visų galimų derinių iš dviejų produktų nuolaidos sumos. Pilkos spalvos lentelių dalyse nurodomi atvejai, kai produktas susiejamas pats su savimi, ko padaryti mes negalime, arba kai du produktai siejami atvirkštiniu būdu ir gaunama ta pati nuolaidos suma, kurios galima nepaisyti. Žiūrėdami į lenteles galite pamatyti, kad 1 nuolaida, kuri taikoma dviems 20 dol. vertės prekėms, yra didžiausia nuolaida, kuri gali būti taikoma bet kuriam iš keturių produktų. (Ši nuolaida pirmoje lentelėje paryškinama žalia spalva.) Taigi lieka tik 15 dol. vertės produktas ir 5 dol. vertės produktas. Dar kartą pažvelgę į dvi lenteles galite pamatyti, kad šiems dviems produktams 1 nuolaida suteikia 2,50 dol. nuolaidą, o 2 nuolaida suteikia 4 dol. nuolaidą. Nodėl mes pasirenkame 2 nuolaidą. Bendra nuolaida sudaro 14 dol. Siekiant, kad būtų lengviau įsivaizduoti tai, kas pasakyta anksčiau, pateikiamos dvi papildomos lentelės, kuriose nurodomos visų galimų derinių iš dviejų produktų 1 ir 2 nuolaidos įsigaliojimo procentinės dalys. Įtraukiama tik pusė derinių sąrašo, nes išdėstymo tvarka, pagal kurią dviems produktams pritaikomos šios dvi nuolaidos, yra nesvarbi. Didžiausia nuolaidos įsigaliojimo procentinė dalis (25 procentai) paryškinama žalia spalva, o mažiausia nuolaidos įsigaliojimo procentinė dalis (10 procentų) paryškinama raudona spalva.

![Nuolaidos įsigaliojimo procentas, skirtas visiems abiejų nuolaidų dviejų produktų deriniams](./media/overlapping-discount-combo-04.jpg)

> [!NOTE]
> Kai kainos skiriasi ir konkuruoja dvi ar daugiau nuolaidų, vienintelis būdas užtikrinti geriausią nuolaidų derinį yra įvertinti abi nuolaidas ir jas palyginti.

## <a name="total-possible-combinations"></a>Visos galimos kombinacijos

Šiame skyriuje tęsiamas ankstesniame skyriuje pateikto pavyzdžio aprašymas. Įtrauksime daugiau produktų ir kitą nuolaidą ir paziuresime, kiek turi būti apskaičiuojama ir palyginama derinių. Toliau pateiktoje lentelėje nurodomas galimų nuolaidų derinių skaičius, kai didėja produkto kiekis. Lentelėje pavaizduota, kas įvyksta, kai yra dvi persidengiančios nuolaidos, kaip nurodyta ankstesniame pavyzdyje, ir kai yra trys persidengiančios nuolaidos. Turimų įvertinti galimų nuolaidų derinių skaičius greitai tampa toks, kurio apskaičiuoti ir pakankamai greitai palyginti, kad būtų tinkamas mažmeninės prekybos operacijoms, negali net spartus kompiuteris.

![Galimų nuolaidų derinių skaičius, kai didėja produkto kiekis](./media/overlapping-discount-combo-05.jpg)

Kai taikomos didesnės nuolaidos arba daugiau persidengiančių nuolaidų, bendras galimų nuolaidų derinių skaičius greitai pasiekia milijoną, o laikas, kurio reikia norint įvertinti ir pasirinkti geriausią derinį, greitai tampa pastebimas. Kainų mechanizme buvo atliktas optimizavimas tam, kad būtų sumažintas bendras derinių, kuriuos reikia įvertinti, skaičius. Tačiau kadangi persidengiančių nuolaidų skaičius ir operacijos kiekiai yra riboti, kiekvieną kartą esant persidengiančių nuolaidų turės būti įvertinamas didelis derinių skaičius. Ši problema sprendžiama taikant ribos vertės vertinimo metodą.

## <a name="marginal-value-method"></a>Ribos vertės metodas

Norint išspręsti proporcingai didėjančio turimų įvertinti derinių skaičiaus problemą, galima naudoti optimizavimą, kurį naudojant apskaičiuojama kiekvieno bendrai naudojamo produkto, priklausančio produktų rinkiniui, kuriems gali būti taikomos dvi ar daugiau nuolaidų, nuolaidos vertė. Ši vertė vadinama bendrai naudojamų produktų nuolaidos **ribos vertė**. Ribos vertė yra bendros produkto nuolaidos sumos padidėjimo vidurkis, kai bendrai naudojami produktai įtraukiami į kiekvieną nuolaidą. Ribos vertė apskaičiuojama iš bendros nuolaidos sumos (DTotal) atimant nuolaidos sumą be bendrai naudojamų produktų (DMinus\\ Shared) ir padalinant skirtumą iš bendrai naudojamų produktų (ProductsShared) skaičiaus.

![Ribinės vertės apskaičiavimo formulė](./media/overlapping-discount-combo-06.jpg)

Apskaičiavus kiekvienos bendrai naudojamų produktų rinkinio nuolaidos ribinę vertę, bendrai naudojamiems produktams nuolaidos taikomos mažėjančia tvarka nuo didžiausios ribinės vertės iki mažiausios ribinės vertės. Taikant šį metodą visos likusios nuolaidos galimybės nėra lyginamos kiekvieną kartą pritaikius vieną nuolaidos atvejį. Persidengiančios nuolaidos lyginamos vieną kartą, o po to taikomos iš eilės. Nėra atliekama jokių papildomų palyginimų. Galite sukonfigūruoti ribinę reikšmę, kad pereitumėte prie ribinės vertės metodo, esančio puslapyje **„Commerce“ parametrai**, skirtuke **Nuolaida**. Įvairiose mažmeninės prekybos rinkose laikas, kuris tinkamas apskaičiuoti bendrąją nuolaidos sumą, skiriasi. Tačiau šis laikas paprastai patenka į intervalą nuo dešimčių milisekundžių iki vienos sekundės.


[!INCLUDE[footer-include](../includes/footer-banner.md)]