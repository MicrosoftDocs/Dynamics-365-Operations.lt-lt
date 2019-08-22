---
title: Pareigų prognozavimas
description: Su darbuotojais susijusios išlaidas dažnai sudaro didelę įmonės išlaidų dalį. Pareigų prognozavimas suteikia galimybę tas išlaidas planuoti ir įtraukti į biudžetų planavimą.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPositionForecast
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 64413
ms.assetid: 35e791d2-1905-4808-a579-7f181ddddd91
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e2cee30bd32771931af9307ed041723d06f01b2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842718"
---
# <a name="position-forecasting"></a>Pareigų prognozavimas

[!include [banner](../includes/banner.md)]

Su darbuotojais susijusios išlaidas dažnai sudaro didelę įmonės išlaidų dalį. Pareigų prognozavimas suteikia galimybę tas išlaidas planuoti ir įtraukti į biudžetų planavimą.

## <a name="position-forecasting-in-budget-planning"></a>Pareigų prognozavimas planuojant biudžetą

[![Grafinio vaizdo viršuje](./media/graphic-top.png)](./media/graphic-top.png) 

Prognozuojant pareigas trys pagrindiniai komponentai naudojami tikslioms pareigų išlaidų biudžeto sumoms pateikti. Tada šias sumas galima įtraukti į biudžeto planą biudžetui skaičiuoti. 

Pagrindinis komponentas yra su **prognozuojamos pareigos**, t. y. visi išlaidų duomenys, susiję su viena pozicija. Galite kurti kelias prognozuojamų pareigų versijas, kiekvienai versijai priskirdami kitą biudžeto plano scenarijų. Kelių versijų naudojimas yra populiaresnis biudžeto sudarymo metodas, pagal kurį sąlyginius scenarijus galima palyginti. Visas prognozuojamas pareigas atitinka personalo pareigos.

**Biudžeto išlaidų elementas** yra sąrankos komponentas, kuris nurodo konkrečias su pareigomis susietas išlaidas, pvz., pagrindinį užmokestį, darbdavio mokamą sveikatos draudimo mokestį, išmokas mobiliajam telefonui ir t. t. Biudžeto išlaidų elementas apima išlaidoms naudojamą pagrindinę sąskaitą ir skaičiavimo parinktis. Kiekvieną biudžeto išlaidų elementą galima priskirti kelioms prognozės pareigoms. 

**Kompensacijų grupė** yra pasirinktinis sąrankos komponentas, kuris naudojamas biudžeto išlaidų elementų rinkiniui taikyti ir apskaičiuotoms pareigų, kurių apmokėjimo charakteristikos panašios, sumoms apmokėti. Kompensacijų grupė gali apimti užmokesčio tarifų kompensacijų tinklelį. Priskyrus grupę prognozuojamoms pareigoms, tinklelio lygis ir etapas gali priskirti prognozuojamų pareigų pajamas. Išlaidų elementų rinkinys yra įtraukiamas automatiškai.

### <a name="position-forecasting-processes"></a>Pareigų prognozavimo procesai

[![graphic1b](./media/graphic1b.png)](./media/graphic1b.png) 

Įprasto pareigų prognozavimo proceso metu pirmiausia sukuriami sąrankos komponentai (biudžeto išlaidų elementai ir kompensacijų grupės). Tada prognozuojamos pareigos sugeneruojamos pagal esamas pareigas. Tada galite atlikti koregavimus. Pvz., galite įtraukti arba šalinti pareigas, keisti užmokesčio tarifus ir išmokų išlaidas bei įtraukti atlyginimo didinimus. Galite kurti kelias prognozuojamų pareigų versijas, kad galėtumėte lengviau palyginti skirtingus biudžeto sudarymo scenarijus. Tada prognozuojamas pareigas galite įtraukti į biudžeto planus ir prognozuojamų pareigų išlaidas įtraukti kaip biudžeto plano eilutes.

Papildomas prognozuojamų pareigų versijas galima kurti, kai peržiūrimi biudžeto planai. Šios naujos versijos yra tikslinimų pagrindas.

## <a name="position-forecasting-setup"></a>Pareigų prognozavimo sąranka
[![graphic2](./media/graphic2-1024x327.png)](./media/graphic2.png)

### <a name="budget-cost-elements"></a>Biudžeto išlaidų elementai

Biudžeto išlaidų elementai naudojami prognozuojamų pareigų išlaidų informacijai nurodyti. Ši informacija apima išlaidų tipą, išlaidų skaičiavimo būdą ir tai, ar išlaidos yra paskirstomos kelioms datoms, kai prognozuojamos pareigos yra įtrauktos į biudžeto planą. 

Konkretūs laukai nustato biudžeto išlaidų elemento elgseną. Kiekvienam biudžeto išlaidų elementui priskiriamas biudžeto išlaidų tipas **Pajamos**, **Išmoka**, **Mokesčiai** arba **Kita**. Biudžeto išlaidų tipai dažniausiai naudojami sumoms apskaičiuoti. Lauko **Prognozuojamų pareigų perrašymas** reikšmė nurodo, ar prognozuojamose pareigose galima modifikuoti elemento sumas. Laukas **Paskirstymo metodas** naudojamas, kai prognozuojamos pareigos yra įtrauktos į biudžeto planą. Išlaidų sumą galite išskaidyti į atskiras biudžeto plano eilutes, kurių datos skiriasi; tai galite atlikti kas mėnesį, ketvirtį, savaitę arba dvi savaites. Pasirinkus pradžios datą, išlaidos kaip viena suma yra priskiriamos nustatytai prognozuojamų pareigų pradžios datai. 

Skaičiuojant biudžeto išlaidų elemento išlaidų sumą naudojamos įsigaliojimo datos, kad tas pats išlaidų elementas galėtų būti naudojamas skirtingais laikotarpiais. Kiekvienam laikotarpiui priskiriama viena pagrindinė sąskaita ir procentas arba metinė suma, kuri nurodo išlaidų sumą. Biudžeto išlaidų elementas gali naudoti kitų išlaidų elementų procentą arba metinės sumos procentą, bet ne abu. Taip pat galite nurodyti metinę ribą. 

Jei išlaidų elementas yra pagrįstas procentu, turite nurodyti biudžeto išlaidų elementus, kurie skaičiuojant yra naudojami kaip pagrindas.

**Pavyzdys** 

Jūratės organizacija teikia 5 proc. darbuotojo pagrindinio atlygio mokymo išmoką. Jūratė nori kurti šios savikainos biudžeto išlaidų elementą. Ji sukuria naują biudžeto išlaidų elementą ir priskiria biudžeto išlaidų tipą **Išmoka**.

Jūratė nenori, kad vadovai keistų išmokos sumą. Todėl lauke **Prognozuojamų pareigų perrašymas** ji pasirenka **Neleisti keisti išlaidų**. Organizacija nori, kad šios išlaidos būtų tolygiai paskirstytos kiekvienam mėnesiui. Todėl lauke **Paskirstymo metodas** Jūratė pasirenka **Kas ketvirtį**. 

Tada Jūratė įtraukia išlaidų skaičiavimo eilutę, nustato datas ir pagrindinę sąskaitą bei kaip procentą įveda **5,00**. Jos organizacija šiai išmokai per metus gali skirti 5 000 JAV dolerių. Todėl Jūratė įveda šią sumą kaip metinę ribą. 

Galiausiai Jūratė įtraukia visus uždarbio išlaidų elementus, kurie yra naudojami kaip pagrindinio užmokesčio skaičiavimo pagrindas. Dabar jos biudžeto išlaidų elementas yra parengtas naudoti.

### <a name="compensation-groups"></a>Kompensacijų grupės

Naudojant kompensacijų grupes galima grupuoti prognozuojamas pareigas, kurių kompensacijų atributai yra panašūs. Taip pat jas galima naudoti siekiant nustatyti prognozuojamų pareigų pajamas ir kasmetinius padidinimus bei priskirti bendrųjų biudžeto išlaidų elementų rinkinį. 

Pagrindinė kompensacijų grupių funkcija yra biudžeto išlaidų elementų rinkinį priskirti prognozuojamoms pareigoms. Todėl kompensacijų grupes galima naudoti siekiant įtraukti bendrąsias išlaidas, pavyzdžiui, išmokų planus ir mokesčius. Prognozuojamas pareigas kuriantis vadovas neprivalo žinoti visų išlaidų elementų, kuriuos reikia įtraukti. Išlaidų elementus galima įtraukti, kai pasirenkama kompensacijų grupė. Elementai įtraukiami į kompensacijų grupės sąranką skirtuke **Biudžeto išlaidų elementai**. 

Kompensacijų grupės taip pat gali nustatyti prognozuojamų pareigų pajamų tarifus. Norėdami skaičiuoti prognozuojamų pareigų pajamas, turite nustatyti grupę, kad ji valandinį arba metinį atlyginimą naudotų kaip skaičiavimo pagrindą. Skirtuke **Kompensacijų koeficientų lentelės** pateiktas darbo užmokesčio tarifų kompensacijų tinklelis nustato pajamas, kurios bus įtrauktos į prognozuojamas pareigas, pagal priskirtą lygį ir etapą. Šie tinkleliai gali būti pagrįsti esamais personalo kompensacijų tinkleliais. Taip pat galite kurti naujus biudžeto planavimo kompensacijų tinklelius. 

Kompensacijų koeficientų lentelėse pateiktos įsigaliojimo ir galiojimo datos suteikia galimybę darbo užmokesčio tarifus keisti bet kurią dieną. Ši funkcija yra naudinga, kai derybų vienetas sutaria dėl visuotino padidėjimo biudžeto ciklo viduryje. Šiuo atveju pakeičiate esamos lentelės galiojimo pabaigos datą į datą, kuri yra viena diena ankstesnė negu tarifo keitimas, ir įtraukiate naują tarifų lentelę, kuri pradedama nuo naujos datos. Kai sukuriate naują tarifų lentelę, jeigu pasirenkate **Kurti naują kompensacijų tinklelį naudojant esamą tinklelį**, galite pasirinkti esamą žmogiškųjų išteklių tarifų lentelę. Sukurtos tarifų lentelės parinktis **Masinis keitimas** suteikia galimybę visiems tinklelio tarifams taikyti procentinį arba standartinės sumos padidėjimą ar sumažėjimą. 

Kompensacijų grupės laukai **Padidinimo grafikas** ir **Padidinimo data** yra naudojami, kai turite kurti darbo užmokesčio didinimus, nes pasikeičia pareigų etapas. Metinio darbo užmokesčio padidėjimas yra įprastas scenarijus. Padidinimo grafikas nurodo, ar nustatant etapo didinimą naudojama pareigų metinių data, ar viena bendroji data. Padidinimo grafikas taikomas visoms kompensacijų grupės prognozuojamoms pareigoms. 

Kompensacijų grupėje pasirinktas pajamų išlaidų elementas yra naudojamas, kai grupėje kuriate prognozuojamų pareigų pajamas, įskaitant jų pagrindinį užmokestį ir bet kokio etapo didinimą. Laukas **Pastoviosios atlyginimo dalies planas** kompensacijų grupę su personalo pastoviosios atlyginimo dalies planu. Šis saitas gali darbuotojo pastoviosios atlyginimo dalies informaciją priskirti prognozuojamoms pareigoms, o dėl to gali būti tiksliau planuojamas biudžetas. Atminkite, kad kompensacijų grupės kompensacijų tinklelio struktūra (lygiai ir etapai) turi atitikti pastoviosios atlyginimo dalies plano struktūrą. Kitu atveju sistema negali kompensacijų grupės tinkamai susieti su pastoviosios atlyginimo dalies planu.

## <a name="creating-forecast-positions"></a>Prognozuojamų pareigų kūrimas
[![graphic3](./media/graphic3-1024x327.png)](./media/graphic3.png)

### <a name="creating-forecast-positions-for-existing-positions"></a>Esamų pareigų prognozuojamų pareigų kūrimas

Norėdami biudžetą planuoti kuo tiksliau, prognozuojamas pareigas galite kurti naudodami informaciją iš esamų pareigų „Microsoft Dynamics 365 for Finance and Operations“, nesvarbu, ar pareigos yra šiuo metu užpildytos, ar ne. 

Funkcijoje **Įtraukti esamas pareigas** rodomos visos organizacijos pareigos. Nustatydami **Nuo** datą, galite keisti pareigų sąrašą, kad jame būtų rodomos tam tikros praeities arba (labiau tikėtina)ateities datos buvusios pareigos. Pasirinkite biudžeto planavimo procesą ir biudžeto plano scenarijų, sąraše pasirinkite pareigas ir spustelėkite **Gerai**, kad sukurtumėte pasirinktų pareigų prognozuojamas pareigas. Atkreipkite dėmesį, kad kiekvienoms esamoms pareigoms biudžeto planavimo procese ir scenarijuje galite kurti tik vienas prognozuojamas pareigas. Tačiau galite kurti papildomas versijas, priskirdami kitus biudžeto plano scenarijus. 

Jei biudžeto išlaidų elementai priskirti personalo pareigoms, tie biudžeto išlaidų elementai taip pat priskiriami prognozuojamoms pareigoms ir jie naudos numatytąsias sumas. Prognozuojamų pareigų lauke **Priskirtas darbuotojas** nustatomas pareigoms priskirto darbuotojo vardas, jei darbuotojas buvo priskirtas. Šis laukas yra paprastas teksto laukas. Tiesioginis saitas nesukuriamas. 

Pasirinkus biudžeto išlaidų elementą, prognozuojamoms pareigoms priskiriama pastoviosios atlyginimo dalies metinė suma naudojant pasirinktą išlaidų elementą, jei priskirtas darbuotojas turi pastoviosios atlyginimo dalies planą. Jei darbuotojas neturi pastoviosios atlyginimo dalies plano arba jei darbuotojas nepriskirtas, naudojama numatytoji biudžeto išlaidų elemento suma. 

Kai parinktis **Priskirti kompensacijų grupę** nustatyta į **Taip**, jei pareigoms priskirtas darbuotojas turi etapais pagrįstą pastoviosios atlyginimo dalies planą, kuris yra susietas su kompensacijų grupę (kaip aprašyta aukščiau), prognozuojamoms pareigoms priskiriami darbuotojo lygis ir etapas bei kompensacijų grupė. Pajamų biudžeto išlaidų elementas iš kompensacijų grupės yra įtraukiamas į prognozuojamas pareigas ir naudojamas kompensacijos grupės lygio ir etapo darbo užmokesčio tarifas. 

Parinkties **Priskirti kompensacijų grupę** nustatymui teikiama pirmenybė, lyginant su parinkties **Biudžeto išlaidų elemento priskyrimas** nustatymu. Šiuos du parametrus galima naudoti vienu metu. 

[![graphic4](./media/graphic4.png)](./media/graphic4.png) 

Kitas pasirinkimas – priskirti jubiliejaus datą. Tada priskirto darbuotojo pasirinkta data (koreguota pradžios data, darbuotojo pradžios data, įdarbinimo pradžios data arba paaukštinimo data) yra nustatoma kaip prognozuojamų pareigų metinių data ir naudojama informacijai teikti bei darbo užmokesčio didinimams generuoti.

### <a name="creating-new-forecast-positions"></a>Naujų prognozuojamų pareigų kūrimas

Naujas prognozuojamas pareigas galima kurti dviem būdais: kopijuoti esamas prognozuojamas pareigas ir kurti visiškai naujas prognozuojamas pareigas. 

Pasirinkę prognozuojamas pareigas, pasirinkite **Kopijuoti pasirinktas prognozuojamas pareigas**, kad sukurtumėte naujas prognozuojamas pareigas, kurių prognozavimo būsena yra **Pasiūlyta**. Šios prognozuojamos pareigos turi visus tuos pačius duomenis, kaip prognozuojamos pareigos, išskyrus priskirtą darbuotoją ir bet kokias biudžeto išlaidų elementų pastabas. Atkreipkite dėmesį, kad sukuriamos atitinkamos naujos personalo pareigos. Šių pareigų aprašas yra **Sukurta pagal prognozę**. 

Taip pat galite kurti visiškai naujas prognozuojamas pareigas. Pasirinkite esamą užduotį ir biudžeto planavimo procesą bei biudžeto plano scenarijų. Tada galite įtraukti kitą norimą informaciją. Įsidėmėkite: tuo pačiu metu sukuriamos ir naujos personalo pareigos.

## <a name="working-with-forecast-positions"></a>Darbas su prognozuojamomis pareigomis
[![graphic5](./media/graphic5-1024x327.png)](./media/graphic5.png)

### <a name="multiple-versions-of-a-forecast-position"></a>Kelios prognozuojamų pareigų versijos

Galite modifikuoti prognozuojamas pareigas ir taikyti žinomus biudžeto ciklo keitimus arba modeliuoti siūlomus keitimus. Paprastai kuriamas pagrindinis prognozuojamų pareigų rinkinys ir tų prognozuojamų pareigų kopijos, o tada tos kopijos naudojamos skirtingiems keitimų rinkiniams modeliuoti. Kopijos priskiriamos kitam biudžeto plano scenarijui, bet (bent jau tol, kol neįsigalioja keitimai) jos yra identiškos prognozuojamoms pareigoms, pagal kurias kopijos yra sukurtos. Originalų ir kopijų personalo pareigos yra tos pačios. 

Tai suteikia funkcija **Kopijuoti į scenarijų**. Atkreipkite dėmesį, kad kiekviename biudžeto plano scenarijuje gali būti tik vienos personalo pareigų prognozuojamos pareigos.

### <a name="modifying-forecast-positions"></a>Prognozuojamų pareigų modifikavimas

Prognozuojamų pareigų keitimai taikomi tik toms prognozuojamoms pareigoms. Keitimai neturi įtakos personalo pareigų įrašams. Be to, dauguma keitimų yra taikomi tik redaguojamoms prognozuojamoms pareigoms. Kitaip tariant, keitimai yra taikomi priskirtiems biudžeto planavimo procesui ir biudžeto plano scenarijui. Išimtis yra laukų, kuriuos pareigos bendrai naudoja keliuose procesuose ir scenarijuose, keitimai. Šie laukai apima laukus skirtukuose **Bendra** ir **Finansinės dimensijos**. Pakeitus šiuos laukus, naujos reikšmės taikomos pareigoms visuose biudžeto planavimo scenarijuose. Todėl šie laukai suteikia galimybę greitai atnaujinti visas versijas.

#### <a name="budget-cost-elements"></a>Biudžeto išlaidų elementai

Biudžeto išlaidų elementai pateikia pagrindinę informaciją apie biudžeto planus: biudžeto sumą ir pagrindinę sąskaitos. Biudžeto suma yra į biudžeto planą siunčiama suma, kai į planą įtrauktos prognozuojamos pareigos. Biudžeto suma yra apskaičiuojama ir jos negalima tiesiogiai keisti. Ši suma yra metinė suma arba apskaičiuotas metinės sumos pagrindo elementų procentas (kaip nurodyta biudžeto išlaidų elemento sąrankoje). Tada suma yra išskaidoma pagal elemento datų intervalo dienų skaičių (pradžios data, pabaigos data) ir pagal prognozuojamų pareigų lauko **Viso etato ekvivalentas** (FTE) reikšmę. 

Pvz., biudžeto išlaidų elemento eilutė, kurios pradžios data yra 2017 m. sausio 1 d., pabaigos data – 2017 m. birželio 30 d., metinė suma – 100 000, of FTE reikšmė yra **0,50**, apskaičiuojama kaip 100 000 x (181 dienų ÷ 365 dienų) x 0,50 = 24 794,52. 

Biudžeto išlaidų elemento eilutes reikia perskaičiuoti, kai pasikeičia prognozuojamų pareigų FTE reikšmė. Taip pat eilutes reikia perskaičiuoti, kai pakeičiamos aktyvinimo arba galiojimo datos. Šių datų keitimai gali lemti biudžeto išlaidų elemento pradžios ir pabaigos datų naujinimą, nes jos turi patekti į prognozuojamų pareigų datų intervalą. Kai reikia perskaičiuoti, mygtukas **Perskaičiuoti** tampa galimas naudoti ir rodomas pranešimas „Reikia apskaičiuoti“. Perskaičiuoti taip pat reikia, jei įtraukėte arba pašalinote biudžeto išlaidų elementą.

**Pavyzdys** 

Organizacija svarsto du būdus, kaip sumažinti buhalterio pareigų išlaidas. Vienas būdas yra baigti pareigų dalį metuose. Kitas būdas yra keisti pareigas į pusės etato visus metus. Benas sukūrė esamų buhalterio pareigų prognozuojamas pareigas pagal pagrindinį scenarijų. Jis kopijuoja šias pagrindines prognozuojamas pareigas į A scenarijų, nustato pabaigos datą į gegužės 31 d. ir perskaičiuoja. Tada Benas kopijuoja pagrindines prognozuojamas pareigas į B scenarijaus, pakeičia FTE reikšmę į **0,50** ir perskaičiuoja. Dabar Benas turi tris versijas, kurių kiekvienos bendrosios išlaidų sumos yra suderintos su jo parinktimis.

#### <a name="assigning-a-compensation-group"></a>Kompensacijų grupės priskyrimas

Kai kompensacijų grupę pirmą kartą priskiriate prognozuojamoms pareigoms, įtraukiami kompensacijų grupės numatytieji biudžeto išlaidų elementai. Jei išlaidų elementai jau priskirti prognozuojamoms pareigoms, tie išlaidų elementai lieka. Jei kompensacijų grupė jau priskirta ir yra keičiama, esami biudžeto išlaidų elementai yra pašalinami ir pakeičiami elementų rinkiniu iš kompensacijų grupės. 

Kai pasirenkate kompensacijos lygį ir etapą, įtraukiamas pajamų biudžeto išlaidų elementas (kaip apibrėžta kompensacijų grupėje). Metinė suma apskaičiuojama naudojant pasirinkto lygio ir etapo tarifą bei kompensacijų grupės valandas per metus (arba, jei tai metinis atlyginimas, visą lygio ir etapo sumą). Primename, kad ši suma išskaidoma pagal išlaidų elemento eilutės datų intervalą ir prognozuojamų pareigų FTE reikšmę.

#### <a name="generating-increases"></a>Didėjimo generavimas

Prognozuojamų pareigų kasmetinius didinimus (vieną per kalendorinius metus) galima kurti automatiškai, jei toms pareigoms priskirta etapais pagrįsta kompensacijų grupė. Spustelėkite **Generuoti didinimą**, norėdami įtraukti paskesnio aukščiausio etapo pajamų biudžeto išlaidų elementą. Naujo pajamų biudžeto išlaidų elemento pradžios data yra suplanuota padidinimo data, pateikiama prognozuojamose pareigose. Ši data nustatoma iš kompensacijų grupės vienu iš dviejų būdų. Jei kompensacijų grupės didinimo grafikas nustatytas kaip **Įprasta data**, didinimo data yra nurodyta kompensacijų grupėje. Jei didinimo grafikas nustatytas kaip **Metinių data**, naudojamas prognozuojamų pareigų metinių datos laukas, o biudžeto ciklas nurodo metus. Jei biudžeto cikle yra keli kalendoriniai metai, įtraukiami keli didinimai. 

Dabartinių pajamų biudžeto išlaidų elemento pabaigos data yra atnaujinama į dieną prieš didinimo datą. Kai generuojami didinimai, automatiškai naudojamas perskaičiavimo procesas. Todėl patiems perskaičiuoti nereikia. 

Jei spustelėsite **Generuoti didinimą** antrą kartą, procesas bus paleistas dar kartą, bet papildomų įrašų įtraukta nebus. Sukuriamas tik vienas didinimas per kalendorinius metus.

#### <a name="changes-from-other-pages"></a>Pakeitimai iš kitų puslapių

Prognozuojamų pareigų naujinimai taip pat gali būti inicijuoti kitose srityse, pvz., biudžeto išlaidų elemento ir kompensacijų grupės sąrankos puslapiuose. Taip pat galite modifikuoti prognozuojamas pareigas, vykdydami masinio naujinimo procesą. 

Sąrankos puslapyje **Biudžeto išlaidų elementas** galima naudoti dvi parinktis: **Įtraukti į pareigas** ir **Naujinti pareigas**. Naudojant parinktį **Įtraukti į pareigas**, biudžeto išlaidų elementas yra įtraukiamas į pasirinktas prognozuojamas pareigas. Jei elementas prognozuojamoms pareigoms jau priskirtas, tos prognozuojamos pareigos yra praleidžiamos. Naudojant parinktį **Naujinti pareigas**, taikomos dabartinės pasirinktų prognozuojamų pareigų reikšmės (pagrindinė sąskaita, procentas, metinė suma ir t.t.). 

Kiekvienas procesas turi panašų puslapį, kuriame galima pasirinkti prognozuojamas pareigas. Puslapyje **Įtraukti į pareigas** rodomos visos prognozuojamos pareigos, kurias galima pasirinkti, o puslapyje **Naujinti pareigas** rodomos tik tos prognozuojamos pareigos, kurioms biudžeto išlaidų elementas jau priskirtas. (Todėl naudodami puslapį **Naujinti pareigas** galite sužinoti, kurioms prognozuojamoms pareigoms išlaidų elementas jau priskirtas.) Perkelkite prognozuojamas pareigas iš viršutinio tinklelio į apatinį tinklelį, kad įtrauktumėte jas į naujinimą. 

Atkreipkite dėmesį, kad skirtuko **Išlaidų skaičiavimas** funkcija **Keisti datas** iš karto pakeičia biudžeto išlaidų elemento pradžios ir pabaigos datas prognozuojamose pareigose. Nėra galimų naudoti parinkčių. 

Puslapio **Kompensacijų grupė** funkcija **Naujinti pareigų tarifus** dabartinius kompensacijos tarifų lentelės tarifus taiko grupei priskirtoms prognozuojamoms pareigoms. Tarifai atnaujinami ir įtraukiamos papildomos išlaidų elemento eilutės, skirtos kiekvienai naujai tarifų lentelės eilutei (atsižvelgiant į datas). Tačiau biudžeto išlaidų elementai ir didinimo datos nėra naujinamos. Galite pasirinkti, kurį biudžeto planavimo procesą ir biudžeto plano scenarijų naujinti. Todėl vieną scenarijų galite atnaujinti, o kitų nekeisti, kad galėtumėte juos palyginti. 

Pasirinkdami prognozuojamas pareigas ir spustelėdami parinktį **Masinis atnaujinimas**, tuo pačiu metu galite įtraukti arba keisti daugiau nei vienas prognozuojamas pareigas. Galima naudoti daug parinkčių. Viena skirtuko **Finansinės dimensijos** parinktis šiek tiek skiriasi nuo kitų ir yra susijusi su biudžeto išlaidų elementais. Biudžeto išlaidų elementus galite įtraukti nustatydami parinktį **Numatytieji biudžeto parametrai** į **Taip**. Jei nepasirinkti jokie biudžeto išlaidų elementai, o parinktis **Numatytieji biudžeto parametrai** nustatyta į **Taip**, pašalinami visi šiuo metu priskirti biudžeto išlaidų elementai. 

Perskaičiavimo procesas automatiškai taikomas visoms prognozuojamoms pareigoms, kurios buvo pakeistos.

## <a name="bringing-forecast-positions-into-budget-plans"></a>Prognozuojamų pareigų perdavimas į biudžeto planus

[![graphic6](./media/graphic6-1024x327.png)](./media/graphic6.png)

Prognozuojamų pareigų kūrimo ir modifikavimo paskirtis – įtraukti jas į biudžeto planus, kad biudžeto planuose būtų pateikiamos tiksliausios biudžeto sumos. Yra du prognozuojamų pareigų įtraukimo į biudžeto planus būdai. Galite naudoti biudžeto plano generavimo procesą arba parinkimo procesą.

### <a name="generating-a-budget-plan-from-forecast-positions"></a>Biudžeto plano generavimas pagal prognozuojamas pareigas

Funkcija **Generuoti biudžeto planą pagal prognozuojamas pareigas** sukuria arba atnaujina biudžeto planus, kad juose būtų prognozuojamų pareigų biudžeto sumos ir FTE skaičiavimai. Prognozuojamų pareigų biudžeto sumos tampa biudžeto plano eilučių sumomis ir yra sujungiamos pagal finansinių dimensijų reikšmes ir įsigaliojimo datą. Generavimo proceso metu biudžeto plano eilutei priskiriama šaltinio prognozės pozicija. Norėdami pareigas peržiūrėti, galite į biudžeto plano maketą įtraukdami prognozuojamas pareigas kaip eilutę arba naudoti užklausą **Biudžeto plano eilutės**. Norėdami šį paskirstymą praleisti, nustatykite parinktį **Įtraukti pareigas į biudžeto plano eilutę** į **Ne**. 

Galite pasirinkti biudžeto plano FTE scenarijų įtraukti FTE skaičių į biudžeto planą. Galite pasirinkti tik kiekio tipo scenarijus, įtrauktus į tikslinio biudžeto plano maketą. Kai pasirinkate FTE scenarijų, taip pat turite nurodyti FTE pagrindinę sąskaitą. Ši sąskaita naudojama kuriant kiekio biudžeto plano eilutes. 

Šaltinyje pasirinkti biudžeto planavimo procesas ir biudžeto plano scenarijus nustato paskirties scenarijaus biudžeto planavimo procesą ir scenarijų. Kadangi šie atributai yra priskiriami prognozuojamoms pareigoms, jie turi atitikti biudžeto planą. Todėl paskirties vietoje atributų redaguoti negalima. 

Galima naudoti tris kitų generavimo procesų parinktis, pateiktas toliau.

-   **Kurti naują biudžeto planą** – sukuriamas naujas planas, kurio atributai pasirenkami sekcijoje **Paskirties vieta**.
-   **Pakeisti esamą biudžeto plano scenarijų** – panaikinami visi pasirinkto biudžeto plano scenarijaus paskirties biudžeto plano duomenys ir sukuriamos naujos eilutės, kuriose pateikiami pasirinktų prognozuojamų pareigų duomenys.
-   **Atnaujinti esamą biudžeto plano scenarijų ir įtraukti naujų duomenų** – atnaujinamos esamos paskirties plano eilutes, kurios atitinka šaltinio eilutes, ir sukuriamos naujos eilutės naujiems duomenims įtraukti. Gretinimas yra pagrįstas DK sąskaita, data, biudžeto klase ir kitomis reikšmėmis, pvz., prognozuojamomis pareigomis. Visos eilutės, kurių pozicijos numeris atitinka šaltinio pozicijos numerį, yra pakeičiamos naujomis eilutėmis iš šaltinio.

### <a name="selecting-forecast-positions"></a>Prognozuojamų pareigų pasirinkimas

Taip pat galite prognozuojamų pareigų biudžeto sumas įtraukti tiesiai į biudžeto planą. Naudokite virš biudžeto plano eilučių pateiktą funkciją **Įtraukti pareigas**, norėdami pasirinkti įtrauktinas prognozuojamas pareigas. 

Kaip šaltinį galima pasirinktis tik tuos biudžeto plano scenarijus, kurie yra įtraukti į plano maketą. Skirtuke **Paskirties vieta** galima nurodyti, kad į FTE scenarijų ir pagrindinę sąskaitą galima įtraukti FTE skaičiavimus, bet tai nėra būtina. 

Šio parinkimo proceso elgsena yra panaši į generavimo proceso parinkties **Atnaujinti esamą biudžeto plano scenarijų ir įtraukti naujų duomenų** elgsena. Visos esamos biudžeto plano eilutės, į kurias įtraukiamos prognozuojamos pareigos, yra pašalinamos ir pakeičiamos naujomis eilutėmis, pagrįstomis dabartine prognozuojamų pareigų būsena.

#### <a name="date-options"></a>Datos parinktys

Generavimo ir parinkimo procesų biudžeto išlaidų elemento eilutės pradžios data nurodo atitinkamos biudžeto plano eilutės įsigaliojimo datą. Biudžeto išlaidų elemento sąranka puslapio laukas **Paskirstymo metodas** nurodo paskirstymo metodą.

-   **Pradžios data** – biudžeto išlaidų elemento pradžios data naudojama kaip biudžeto plano eilutės įsigaliojimo data.
-   **Kas mėnesį** – biudžeto suma yra lygiai padalijama iš datų intervalo mėnesių skaičiaus, siekiant nustatyti įprastą mėnesio sumą, kuri priskiriama kiekvieno mėnesio pirmą dieną. Jei pirmasis laikotarpis yra dalinis mėnesis, to mėnesio suma yra padalijama iš to mėnesio dienų, kurias išlaidos yra aktyvios, skaičiaus, o rezultatas yra priskiriamas pradžios datai. Paskutinio mėnesio suma yra visos biudžeto sumos ir visų kitų mėnesių sumos skirtumas. Todėl apvalinimas gali turėti įtakos paskutinio mėnesio sumai.
-   **Kas ketvirtį** – šis metodas yra toks pats, kaip **Kas mėnesį**, bet skaičiavimai atliekami trijų mėnesių laikotarpiams.
-   **Kas savaitę** – šio metodo logika yra tokia pati, kaip metodų **Kas mėnesį** ir **Kas ketvirtį**. Biudžeto suma yra lygiai padalijama iš datų intervalo savaičių skaičiaus, siekiant nustatyti įprastą savaitės sumą, kuri priskiriama kiekvienos savaitės pirmą dieną. Jei pirmasis laikotarpis yra dalinė savaitė, tos savaitės suma yra padalijama iš tos savaitės dienų, kurias išlaidos yra aktyvios, skaičiaus, o rezultatas yra priskiriamas pradžios datai. Paskutinės savaitės suma yra visos biudžeto sumos ir visų kitų savaičių sumos skirtumas. Todėl apvalinimas gali turėti įtakos paskutinės savaitės sumai.
-   **Kas dvi savaites** – šis metodas yra toks pats, kaip **Kas savaitę**, bet skaičiavimai atliekami dviejų savaičių laikotarpiams.

#### <a name="changing-budget-plan-lines-that-have-forecast-positions"></a>Biudžeto plano eilučių, turinčių prognozuojamas pareigas, keitimas

Biudžeto plano eilutėse rodomas biudžeto sumų šaltinis (prognozuojamų pareigų numeris), bet jos nėra susietos. Todėl prognozuojamų pareigų keitimai nėra rodomi biudžeto plano eilutėje, o biudžeto plano eilutės keitimai yra rodomi prognozuojamose pareigose. Jei pakeičiate prognozuojamas pareigas ir norite naujinimus įtraukti į biudžeto planą, turite dar kartą perduoti prognozuojamas pareigas į planą. Tačiau atminkite, kad šio proceso metu pašalinamos visos eilutės, kurioms tos prognozuojamos pareigos yra priskirtos. Todėl pašalinami visi atlikti tų eilučių pakeitimai. 

Norėdami pamatyti, į kuriuos biudžeto planus prognozuojamos pareigos buvo įtrauktos, galite generuoti ataskaitą **Prognozuojamos pareigos pagal biudžeto planą**. Taip pat galite prognozuojamose pareigose atidaryti „FactBox“ **Susieti biudžeto planai** ir peržiūrėti planus.



