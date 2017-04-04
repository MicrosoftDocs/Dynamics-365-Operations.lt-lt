---
title: "Nustatyti dėl optimalios kombinacijos tarp persidengiančių nuolaidos"
description: "Kai nuolaidos sutampa, turite nustatyti persidengiančių nuolaidų, kurios gamins mažiausia sandorio suma ar didžiausia bendra nuolaida derinys. Kai nuolaidos dydis priklauso nuo, perkamų produktų kainą, pavyzdžiui, bendra &quot;pirkti 1, gausite 1 X procentų&quot; (BOGO) mažmeninės prekybos nuolaidos, šis procesas tampa kombinatorinė optimizavimo problema."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.region: global
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 31e5104045ed5b8fbfa3677a7f5702d551de4231
ms.lasthandoff: 03/31/2017


---

# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a>Nustatyti dėl optimalios kombinacijos tarp persidengiančių nuolaidos

Kai nuolaidos sutampa, turite nustatyti persidengiančių nuolaidų, kurios gamins mažiausia sandorio suma ar didžiausia bendra nuolaida derinys. Kai nuolaidos dydis priklauso nuo, perkamų produktų kainą, pavyzdžiui, bendra "pirkti 1, gausite 1 X procentų" (BOGO) mažmeninės prekybos nuolaidos, šis procesas tampa kombinatorinė optimizavimo problema.

Šis straipsnis taikomas Microsoft Dynamics AX 2012 R3 su KB 3105973 (išleista 2015 m. lapkričio 2 d.) arba vėliau, ir iki 2016 m. vasario išleidimo, Microsoft Dynamics AX. Norėdami nustatyti derinys persidengiančių nuolaidos taikomos laiku ir toliau teikti diskontavimas funkcijų, kuri yra prieinama Microsoft Dynamics AX for Retail, įdiegėme metodą taikyti persidengiančių nuolaidas. Mes vadiname šį naują metodą **ribinės vertės reitingas**. Ribinė vertė reitingas yra naudojamas, kai laikas, kurio reikia siekiant įvertinti galimų kombinacijų persidengiančių nuolaidų viršija ribinę vertę, kuri yra konfigurowalne ir **mažmeninė parametrai** puslapis Dynamics AX. Ribinės vertės reitingavimo metodas, vertė skaičiuojama kiekvieną persidengiančių nuolaida naudojant nuolaidos vertė bendro naudojimo produktų. Kad sutapo tada taikomos nuolaidos nuo didžiausios santykinis mažiausia santykinė vertė. Daugiau informacijos apie naują, skyriuje "Ribinė vertė", šiame straipsnyje. Ribinė vertė reitingas nėra naudojamas, kai produkto nuolaidos suma neturės įtakos kitą produktą su sandoriu. Pavyzdžiui, šis metodas nenaudojamas dvi paprastas nuolaidos, arba paprastas nuolaida ir vieno produkto kiekio nuolaida.

## <a name="discount-examples"></a>Nuolaida pavyzdžiai
Dynamics AX, galite sukurti neribotą skaičių mažmeninės prekybos nuolaidų sudaryti bendrą produktų. Vis dėlto nes neribojamas, efektyvumo problemų gali atsirasti, kai bandote apskaičiuoti nuolaidas, kurie turėtų būti naudojami įvairių produktų. Toliau pateikiami pavyzdžiai iliustruoja Ši problema išsamiau. 1 pavyzdyje, mes pradedame dviejų prekių ir dviejų persidengiančių nuolaidą. Tada 2 pavyzdyje, mes parodysime, kaip problemos vystosi, pridedant daugiau prekių.

### <a name="example-1-two-products-and-two-discounts"></a>1 pavyzdys: Dviejų prekių ir dviejų nuolaidą

Šiame pavyzdyje du produktai būtini kiekvieno nuolaidą ir nuolaidos negali būti derinama. Nuolaidos šiame pavyzdyje yra **geriausia kaina** nuolaidos. Abu produktai gali būti tiek nuolaidas. Čia pateikiami dviejų nuolaidą. [![Sutapimo nuolaida Kombi 01](./media/overlapping-discount-combo-01.jpg)](./media/overlapping-discount-combo-01.jpg) bet dviejų produktų iš šių dviejų nuolaidą geriau priklauso nuo šių dviejų produktų kainos. Kai abiejų produktų kainos yra beveik vienodos, nuolaida 1 yra geriau. Kai vienos prekės kaina yra žymiai mažesnė nei kitos prekės kaina, nuolaida 2 yra geriau. Čia yra matematinės taisyklė įvertinti šių dviejų nuolaidos tarpusavyje: [![Overlapping nuolaida Kombi 02](./media/overlapping-discount-combo-02.jpg)](./media/overlapping-discount-combo-02.jpg) dėmesį, kad kai prekės 1 kaina yra lygi dviem trečdaliams 2 prekės kaina, dviejų nuolaidą yra vienodas. Šiame pavyzdyje, veiksmingas nuolaidos procentą nuolaidos 1 svyruoja nuo kelių procentų (kai šių dviejų produktų kainos toli vienas nuo kito) ne daugiau kaip 25 procentus (kai du produktai turi tą pačią kainą). Veiksmingas nuolaidos procentą nuolaidos 2 yra fiksuota. Tai visada 20 procentų. Kadangi veiksminga nuolaidos procentą nuolaidos 1 diapazoną, kuriame gali būti daugiau nei arba mažiau nei nuolaida 2, geriausias nuolaida priklauso nuo šių dviejų produktų, kurie turi būti diskontuojamos kainas. Šiame pavyzdyje apskaičiuoti yra užbaigti greitai, nes tik du nuolaidos yra taikomos tik du produktus. Yra tik du galimų derinių: vieną paraišką 2 nuolaida nuolaida 1 arba vienas taikymo. Šiuo metu jokių kombinacijų apskaičiuoti. Kiekvienai nuolaidai vertė yra apskaičiuojama taikant abu produktai, ir naudoja geriausias nuolaida.

### <a name="example-2-four-products-and-two-discounts"></a>2 pavyzdys: Keturių produktų ir du nuolaidos

Be to, mes naudojame keturių produktų ir pačios dviejų nuolaidą. Visų keturių produktų gauti tiek nuolaidas. Šiuo metu dvylika galimų kombinacijų. Galų gale, du nuolaidos bus pritaikytos operacijai – vienas iš trijų derinių: dvi paraiškas nuolaida 1, dvi paraiškas nuolaida 2 ar vieną taikymo 1 ir viena nuolaida nuolaida 2 taikymo. Norėdami parodyti galimus derinius, mes pažvelgti į du trys keturių produktų, kurie turi skirtingas kainas:

-   Visi keturi produktai turi tą pačią kainą, $15.00. Šiuo atveju nuolaida geriausią yra dvi paraiškas nuolaida 1. Du produktai bus pilna kaina, ir du bus 50 procentų išjungti. Diskontuota bendra operacijos išjungtas nediskontuoti bendra $60 $45 (15 + 15 + 7,50 + 7,50), kuris yra $15 (25 proc.). Nuolaida 2 yra tik $12 (20 proc.).
-   Du produktai yra $20 kiekvienos, vienas produktas yra $15, ir vienas produktas yra $5. Šiuo atveju nuolaida geriausią yra viena paraiška nuolaida 1 2 ir vienas nuolaidų taikymo. Šiose lentelėse parodoma nuolaidas.

Skaityti lenteles, naudokite vieną iš eilės ir vieno produkto iš stulpelio. Pvz., nuolaida 1 lentelės, kai jūs derinti du $20 produktai, išlipti $10. Nuolaida 2 lentelės, kai jūs derinti $15 produktas ir $5 produktas, išlipti $4. [![Sutapimo nuolaida Kombi 03](./media/overlapping-discount-combo-03.jpg)](./media/overlapping-discount-combo-03.jpg) pirmą kartą, mes rasti didžiausias nuolaida, kuri yra prieinama iš bet kurios dvi produktų naudojant arba nuolaida. Dvi lentelės rodo visiems deriniams šių dviejų prekių nuolaidos suma. Spalvotomis dalimis lentelių atstovauti arba atvejais, kai produktas yra suporuotas su savimi, mes negalime padaryti, arba atvirkštinio suporavus du produktus, kurie susidaro tokia pati nuolaidos suma ir galima nekreipti dėmesio. Pažvelgus į lenteles, pamatysite, kad nuolaida 1 dviejų $20 punktų yra didžiausia nuolaida, kuri yra skirta arba nuolaida visų keturių produktų. (Šią nuolaidą yra pažymėtas žaliai pirmoje lentelėje.) Tai palieka tik $15 produktas ir $5 produktas. Vėl žiūri į dvi lenteles, galite pamatyti, kad šių dviejų produktų, nuolaida 1 suteikia $2.50 nuolaida, kadangi 2 nuolaida $4 nuolaida. Todėl, mes pasirinkite nuolaida 2. Todėl bendra nuolaida yra $14. Kad ši diskusija būtų lengviau vizualizuoti, čia yra dvi papildomos lentelės, tai rodo veiksmingą nuolaidos procentą visų galimų dviejų produktų deriniams abi nuolaida 1 ir nuolaida 2. Tik pusė derinių sąrašas yra įtrauktas, nes šių dviejų nuolaidos, kai dvi prekės išleidžiamos į nuolaida tvarka nesvarbi. Didžiausią veiksmingą nuolaidą (25 proc.) yra pažymėtas žaliai, o mažiausia veiksminga nuolaida (10 proc.) yra paryškinta raudona spalva. [![Sutapimo nuolaida Kombi 04](./media/overlapping-discount-combo-04.jpg)](./media/overlapping-discount-combo-04.jpg)**Pastaba:** kai kainos skiriasi, o dvi ar daugiau nuolaidų konkuruoti, vienintelis būdas garantuoti geriausią nuolaidos yra įvertinti tiek nuolaidas ir palyginti juos.

## <a name="total-possible-combinations"></a>Iš viso galimų kombinacijų
Šiame skyriuje toliau pavyzdį iš ankstesnio skyriaus. Mes pridėti daugiau produktų ir kita nuolaida, ir pamatyti, kiek deriniai turi būti apskaičiuoti ir palyginti. Šioje lentelėje skaičius galimas nuolaidų kombinacijas kaip produkto kiekis didėja. Lentelėje parodyta, kas atsitinka ir tada, kai dviejų persidengiančių nuolaidos, kaip ir ankstesniame pavyzdyje, kai yra trys sutampa nuolaidos. Galimas nuolaidų kombinacijas, kurie turi būti įvertinti greitai viršija net greitą kompiuterį galite apskaičiuoti ir palyginti greitai pakankamai priimtina mažmeninės prekybos operacijų. [![Sutapimo nuolaida Kombi 05](./media/overlapping-discount-combo-05.jpg)](./media/overlapping-discount-combo-05.jpg) kada net didesnius kiekius ar daugiau sutampančių taikome nuolaidas, bendras skaičius galimas nuolaidų kombinacijas greitai eina į milijonais ir laiką, kurio reikia siekiant įvertinti ir pasirinkti geriausią galimą greitai tampa pastebimas. Kai kurių patobulinimų buvo padaryta mažmeninės kainos variklio sumažinti skaičių derinių, kurie turi būti įvertinti. Vis dėlto nes numeris sutampa nuolaidas ir kiekius pagal sandorį ne tik, daug kombinacijų visada turi įvertinti kiekvieną kartą, kai yra persidengiančių nuolaidas. Ši problema yra klausimas, kuris vertės reitingavimo metodas.

## <a name="marginal-value-method"></a>Ribinės vertės metodas
Norėdami išspręsti šią problemą, proporcingai vis daugiau derinių, kurie turi būti įvertinti, optimizavimo egzistuoja, kad apskaičiuoja bendra kiekvienos produktų, kurie gali būti taikomi du ar daugiau nuolaidų rinkinį nuolaida produkto vertę. Minime šią vertę, kaip ir **ribinė vertė** nuolaidos bendro naudojimo produktų. Ribinė vertė yra bendros nuolaidos sumą padidinti produkto vidutinė, kai bendro naudojimo produktai yra įtraukti į kiekvienai nuolaidai. Ribinė vertė apskaičiuojama imant nuolaidos sumą, bendrą produktų bendros nuolaidos suma (DTotal), (DMinus\\ bendro naudojimo), ir šis skirtumas dalijant bendrą produktų (ProductsShared) skaičius. [![Sutapimo nuolaida Kombi 06](./media/overlapping-discount-combo-06.jpg)](./media/overlapping-discount-combo-06.jpg) po to, kai apskaičiuojama kiekvienai nuolaidai dėl bendros produktų vertės, nuolaidos taikomos bendros produktams tvarka, išsamiai, nuo didžiausios vertės iki mažiausios ribinės vertės. Taikant šį metodą, visas likusias nuolaida galimybes nėra palyginti kiekvieną kartą pritaikius nuolaidą vieno egzemplioriaus. Vietoj to, persidengiančių nuolaidos yra palyginti vieną kartą ir tada taikoma tvarka. Jokių papildomų palyginimai yra daroma. Galite konfigūruoti slenksčio vertės metodo įjungti į **nuolaida** skirtuke, **mažmeninė parametrai** puslapis. Priimtiną laiką apskaičiuoti bendrą nuolaidą skiriasi mažmeninės prekybos sektoriuose. Tačiau šį kartą paprastai patenka į dešimtis milisekundžių į vieną sekundę, diapazonas.


