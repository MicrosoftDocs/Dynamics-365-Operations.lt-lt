---
title: "Optimalaus persidengiančių nuolaidų derinio nustatymas"
description: "Kai nuolaidos persidengia, turite nustatyti persidengiančių nuolaidų derinį, kurį naudojant bus sukuriama mažiausia bendroji operacijos suma arba didžiausia bendroji nuolaidos suma. Kai nuolaidos suma kinta priklausomai nuo įsigytų produktų kainos, pavyzdžiui, kaip dažnai pasitaikančiu mažmeninės prekybos nuolaidų atveju „Pirkdami 1 gaukite 1 X procentų nuolaidą“ (BOGO), šis procesas tampa kombinacinio optimizavimo problema."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.region: global
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 598f479c4bba0df289af49076fb0cb7053ee96c1
ms.contentlocale: lt-lt
ms.lasthandoff: 04/26/2017


---

# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a>Optimalaus persidengiančių nuolaidų derinio nustatymas

[!include[banner](includes/banner.md)]


Kai nuolaidos persidengia, turite nustatyti persidengiančių nuolaidų derinį, kurį naudojant bus sukuriama mažiausia bendroji operacijos suma arba didžiausia bendroji nuolaidos suma. Kai nuolaidos suma kinta priklausomai nuo įsigytų produktų kainos, pavyzdžiui, kaip dažnai pasitaikančiu mažmeninės prekybos nuolaidų atveju „Pirkdami 1 gaukite 1 X procentų nuolaidą“ (BOGO), šis procesas tampa kombinacinio optimizavimo problema.

Šis straipsnis taikomas programai „Microsoft Dynamics AX 2012 R3“ su „KB 3105973“ (išleista 2015 m. lapkričio 2 d.) arba vėlesnei versijai ir 2016 m. vasario mėn. išleistai „Microsoft Dynamics AX“ versijai. Norėdami nustatyti, kad nuolaidų persidengimo derinys būtų taikomas tam tikru laiku ir kad toliau būtų taikoma didelių nuolaidų funkcija, kuria galima naudotis naudojantis programa „Microsoft Dynamics AX for Retail“, mes siūlome persidengiančių nuolaidų taikymo metodą. Šį metodą vadiname **ribos vertės vertinimas**. Ribos vertės vertinimas naudojamas, kai laiko, kurio reikia norint įvertinti galimus persidengiančių nuolaidų derinius, vertė viršija slenkstinę vertę, kuri konfigūruojama „Dynamics AX“ puslapyje **Mažmeninės prekybos parametrai**. Taikant ribos vertės vertinimo metodą apskaičiuojama kiekvienos persidengiančios nuolaidos vertė taikant nuolaidos vertę bendrai naudojamiems produktams. Persidengiančios nuolaidos taikomos nuo didžiausios santykinės vertės iki mažiausios santykinės vertės. Išsamią informaciją apie naują metodą rasite toliau šiame straipsnyje pateiktame skyriuje „Ribos vertė“. Ribos vertės vertinimas nenaudojamas, kai produkto nuolaidos sumoms neturi įtakos kitas operacijos produktas. Pavyzdžiui, šis metodas nenaudojamas dviems paprastoms nuolaidoms arba paprastai nuolaidai ir vieno produkto kiekio nuolaidai.

## <a name="discount-examples"></a>Nuolaidų pavyzdžiai
Naudodami „Dynamics AX“ galite sukurti neribotą skaičių bendrajam produktų rinkiniui taikomų mažmeninės prekybos nuolaidų. Tačiau, kadangi nėra apribojimo, bandant apskaičiuoti nuolaidas, kurios turėtų būti naudojamos įvairiems produktams, gali atsirasti našumo trikčių. Toliau pateikiamuose pavyzdžiuose ši problema pavaizduota išsamiau. 1 pavyzdyje pradedame su dviem produktais ir dviem persidengiančiomis nuolaidomis. 2 pavyzdyje rodoma, kaip problema didėja įtraukiant daugiau produktų.

### <a name="example-1-two-products-and-two-discounts"></a>1 pavyzdys: du produktai ir dvi nuolaidos

Šiame pavyzdyje norint, kad būtų taikoma kiekviena nuolaida, reikia dviejų produktų ir nuolaidų negalima sujungti. Šio pavyzdžio nuolaidos yra nuolaidos **Geriausia kaina**. Abiems produktams gali būti taikomos abi nuolaidos. Toliau nurodomos dvi nuolaidos. [![Persidengianti nuolaida, 01 pasirinktinis įvedimas](./media/overlapping-discount-combo-01.jpg)](./media/overlapping-discount-combo-01.jpg) Kuri iš šių dviejų produktų nuolaidų bus geresnė, priklauso nuo abiejų produktų kainos. Kai abiejų produktų kaina lygi arba beveik lygi, geriau naudoti 1 nuolaidą. Kai vieno produkto kaina žymiai mažesnė negu kito produkto kaina, geriau naudoti 2 nuolaidą. Toliau nurodoma matematinė taisyklė, kaip vertinti šias dvi nuolaidas viena kitos atžvilgiu. [![Persidengianti nuolaida, 02 pasirinktinis įvedimas](./media/overlapping-discount-combo-02.jpg)](./media/overlapping-discount-combo-02.jpg) Atkreipkite dėmesį, kad kai 1 produkto kaina lygi dviems trečiosioms 2 produkto kainos, dvi nuolaidos yra lygios. Šiame pavyzdyje 1 nuolaidos įsigaliojimo procentinė dalis kinta nuo kelių procentų (kai dviejų produktų kainos itin skiriasi viena nuo kitos) iki maksimalios 25 procentų procentinės dalies (kai dviejų produktų kaina vienoda). 2 nuolaidos įsigaliojimo procentinė dalis yra fiksuota. Ji visada lygi 20 procentų. Kadangi 1 nuolaidos įsigaliojimo procentinės dalies intervalas gali būti didesnis arba mažesnis už 2 nuolaidą, geriausia nuolaida priklauso nuo dviejų produktų kainos, kuriems turi būti taikoma nuolaida. Šiame pavyzdyje skaičiavimas atliekamas greitai, nes taikomos tik dvi nuolaidos ir tik dviems produktams. Galimi du deriniai: vieną kartą taikoma 1 nuolaida arba vieną kartą taikoma 2 nuolaida. Nėra derinių, kuriuos reikėtų apskaičiuoti. Kiekvienos nuolaidos vertė apskaičiuojama naudojant abu produktus ir naudojama didžiausia nuolaida.

### <a name="example-2-four-products-and-two-discounts"></a>2 pavyzdys: keturi produktai ir dvi nuolaidos

Toliau bus naudojami keturi produktai ir tos pačios dvi nuolaidos. Visiems keturiems produktams gali būti taikomos abi nuolaidos. Yra dvylika galimų derinių. Galiausiai dvi nuolaidos bus taikomos vienu iš šių trijų derinių: du kartus taikoma 1 nuolaida, du kartus taikoma 2 nuolaida arba vieną kartą taikoma 1 nuolaida ir vieną kartą taikoma 2 nuolaida. Norėdami pavaizduoti galimus derinius peržiūrėsime du skirtingus iš keturių skirtingų kainų produktų sudarytus rinkinius.

-   Visų produktų kaina vienoda – 15,00 dol. Šiuo atveju geriausias nuolaidų derinys yra du kartus taikoma 1 nuolaida. Du produktai bus parduodami be nuolaidos, o du – su 50 proc. nuolaida. Bendra operacijos nuolaidos suma yra 45 dol. (15 + 15 + 7,50 + 7,50), o tai yra 15 dol. (25 procentų) nuolaida nuo bendros 60 dol. siekiančios sumos be nuolaidos. 2 nuolaida yra tik 12 dol. (20 procentų).
-   Du produktai kainuoja po 20 dol., vienas produktas kainuoja 15 dol. ir vienas produktas – 5 dol. Šiuo atveju geriausias nuolaidų derinys yra vieną kartą taikoma 2 nuolaida ir vieną kartą taikoma 1 nuolaida. Šios nuolaidos pavaizduotos toliau pateiktose lentelėse.

Norėdami perskaityti šias lenteles, naudokite vieną produktą iš eilutės ir vieną produktą iš stulpelio. Pavyzdžiui, 1 nuolaidos lentelėje sujungę du 20 dol. vertės produktus gaunate 10 dol. nuolaidą. 2 nuolaidos lentelėje sujungę 15 dol. ir 5 dol. vertės produktus gaunate 4 dol. nuolaidą. [![Persidengianti nuolaida, 03 pasirinktinis įvedimas](./media/overlapping-discount-combo-03.jpg)](./media/overlapping-discount-combo-03.jpg) Pirmiausia randame didžiausią galimą nuolaidą, kuri gali būti pritaikyta bet kuriems dviems produktams naudojant bet kurią nuolaidą. Dviejose lentelėse nurodomos visų galimų derinių iš dviejų produktų nuolaidos sumos. Pilkos spalvos lentelių dalyse nurodomi atvejai, kai produktas susiejamas pats su savimi, ko padaryti mes negalime, arba kai du produktai siejami atvirkštiniu būdu ir gaunama ta pati nuolaidos suma, kurios galima nepaisyti. Žiūrėdami į lenteles galite pamatyti, kad 1 nuolaida, kuri taikoma dviems 20 dol. vertės prekėms, yra didžiausia nuolaida, kuri gali būti taikoma bet kuriam iš keturių produktų. (Ši nuolaida pirmoje lentelėje paryškinama žalia spalva.) Taigi lieka tik 15 dol. vertės produktas ir 5 dol. vertės produktas. Dar kartą pažvelgę į dvi lenteles galite pamatyti, kad šiems dviems produktams 1 nuolaida suteikia 2,50 dol. nuolaidą, o 2 nuolaida suteikia 4 dol. nuolaidą. Nodėl mes pasirenkame 2 nuolaidą. Bendra nuolaida sudaro 14 dol. Siekiant, kad būtų lengviau įsivaizduoti tai, kas pasakyta anksčiau, pateikiamos dvi papildomos lentelės, kuriose nurodomos visų galimų derinių iš dviejų produktų 1 ir 2 nuolaidos įsigaliojimo procentinės dalys. Įtraukiama tik pusė derinių sąrašo, nes išdėstymo tvarka, pagal kurią dviems produktams pritaikomos šios dvi nuolaidos, yra nesvarbi. Didžiausia nuolaidos įsigaliojimo procentinė dalis (25 procentai) paryškinama žalia spalva, o mažiausia nuolaidos įsigaliojimo procentinė dalis (10 procentų) paryškinama raudona spalva. [![Persidengianti nuolaida, 04 pasirinktinis įvedimas](./media/overlapping-discount-combo-04.jpg)](./media/overlapping-discount-combo-04.jpg) **Pastaba.** Kai kainos skiriasi ir konkuruoja dvi nuolaidos, vienintelis būdas užtikrinti geriausią nuolaidų derinį yra įvertinti abi nuolaidas ir jas palyginti.

## <a name="total-possible-combinations"></a>Visos galimos kombinacijos
Šiame skyriuje tęsiamas ankstesniame skyriuje pateikto pavyzdžio aprašymas. Įtrauksime daugiau produktų ir kitą nuolaidą ir paziuresime, kiek turi būti apskaičiuojama ir palyginama derinių. Toliau pateiktoje lentelėje nurodomas galimų nuolaidų derinių skaičius, kai didėja produkto kiekis. Lentelėje pavaizduota, kas įvyksta, kai yra dvi persidengiančios nuolaidos, kaip nurodyta ankstesniame pavyzdyje, ir kai yra trys persidengiančios nuolaidos. Turimų įvertinti galimų nuolaidų derinių skaičius greitai tampa toks, kurio apskaičiuoti ir pakankamai greitai palyginti, kad būtų tinkamas mažmeninės prekybos operacijoms, negali net spartus kompiuteris. [![Persidengianti nuolaida, 05 pasirinktinis įvedimas](./media/overlapping-discount-combo-05.jpg)](./media/overlapping-discount-combo-05.jpg) Kai taikomos didesnės nuolaidos arba daugiau persidengiančių nuolaidų, bendras galimų nuolaidų derinių skaičius greitai pasiekia milijoną, o laikas, kurio reikia norint įvertinti ir pasirinkti geriausią derinį, greitai tampa pastebimas. Atlikti kai kurie mažmeninės prekybos kainų variklio optimizavimo veiksmai, kad būtų sumažintas bendras turimų įvertinti derinių skaičius. Tačiau kadangi persidengiančių nuolaidų skaičius ir operacijos kiekiai yra riboti, kiekvieną kartą esant persidengiančių nuolaidų turės būti įvertinamas didelis derinių skaičius. Ši problema sprendžiama taikant ribos vertės vertinimo metodą.

## <a name="marginal-value-method"></a>Ribos vertės metodas
Norint išspręsti proporcingai didėjančio turimų įvertinti derinių skaičiaus problemą, galima naudoti optimizavimą, kurį naudojant apskaičiuojama kiekvieno bendrai naudojamo produkto, priklausančio produktų rinkiniui, kuriems gali būti taikomos dvi ar daugiau nuolaidų, nuolaidos vertė. Ši vertė vadinama bendrai naudojamų produktų nuolaidos **ribos vertė**. Ribos vertė yra bendros produkto nuolaidos sumos padidėjimo vidurkis, kai bendrai naudojami produktai įtraukiami į kiekvieną nuolaidą. Ribos vertė apskaičiuojama iš bendros nuolaidos sumos (DTotal) atimant nuolaidos sumą be bendrai naudojamų produktų (DMinus\\ Shared) ir padalinant skirtumą iš bendrai naudojamų produktų (ProductsShared) skaičiaus. [![Persidengianti nuolaida, 06 pasirinktinis įvedimas](./media/overlapping-discount-combo-06.jpg)](./media/overlapping-discount-combo-06.jpg) Apskaičiavus kiekvienos bendrai naudojamų produktų rinkinio nuolaidos ribos vertę bendrai naudojamiems produktams nuolaidos taikomos mažėjančia tvarka nuo didžiausios ribos vertės iki mažiausios ribos vertės. Taikant šį metodą visos likusios nuolaidos galimybės nėra lyginamos kiekvieną kartą pritaikius vieną nuolaidos atvejį. Persidengiančios nuolaidos lyginamos vieną kartą, o po to taikomos iš eilės. Nėra atliekama jokių papildomų palyginimų. Puslapio **Mažmeninės prekybos parametrai** skirtuke **Nuolaida** galite sukonfigūruoti, kad ribinė vertė būtų įjungiama pagal ribos vertės metodą. Įvairiose mažmeninės prekybos rinkose laikas, kuris tinkamas apskaičiuoti bendrąją nuolaidos sumą, skiriasi. Tačiau šis laikas paprastai patenka į intervalą nuo dešimčių milisekundžių iki vienos sekundės.




