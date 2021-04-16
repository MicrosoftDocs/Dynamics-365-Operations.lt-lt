---
title: Mokėjimų priežiūros proceso automatizavimas
description: Šioje temoje aprašomas mokėjimų priežiūros proceso strategijų, kurios automatiškai identifikuoja klientų SF, kurioms reikalingas priminimas el. paštu, mokėjimų veikla ar priminimo laiškas, kuris bus išsiųstas klientui, nustatymo procesas.
author: panolte
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ce83b8e66abece2c40ca0a7ca3bf67894b97c287
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827631"
---
# <a name="collections-process-automation"></a>Surinkimo proceso automatizavimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas mokėjimų priežiūros proceso strategijų, kurios automatiškai identifikuoja klientų SF, kurioms reikalingas priminimas el. paštu, mokėjimų veikla (pvz., telefono skambutis) ar priminimo laiškas, kuris bus išsiųstas klientui, nustatymo procesas. 

Organizacijos išleidžia daug laiko tirdamos suskirstytų pagal terminus balansų ataskaitas, klientų sąskaitas ir atviras SF, kad sužinotų, su kuriais klientais reikėtų susisiekti dėl atviros SF ar sąskaitos balanso. Šie tyrimai užima laiką, kurį mokėjimų priežiūros agentas galėtų praleisti bendraudamas su klientais, kad būtų surinkti pasibaigusio termino balansai, ar spręsdamas su SF susijusius konfliktus. Mokėjimų priežiūros proceso automatizavimas leidžia nustatyti strategija pagrįstą jūsų mokėjimų priežiūros proceso metodą. Tai padeda nuosekliai taikyti mokėjimų priežiūros veiklas pateikiant tinkintus priminimus el. paštu arba suprogramuotą priminimo laiškų siuntimo procesą. 

## <a name="collections-process-setup"></a>Mokėjimų priežiūros proceso sąranka
Galite naudoti puslapį **Mokėjimų priežiūros proceso sąranka** (**Kredito ir mokėjimų priežiūra > Sąranka > Mokėjimų priežiūros proceso sąranka**), kad būtų sukurtas automatizuotas mokėjimų priežiūros procesas, skirtas veikloms planuoti, el. laiškams siųsti ir klientų priminimo laiškams kurti bei registruoti. Proceso veiksmai yra pagrįsti pagrindine arba seniausia atvira SF. Kiekvienas veiksmas naudoja šią SF, kad nustatytų, kokie konkretaus kliento ryšiai ar veikla turi įvykti.  

Mokėjimų priežiūros komandos paprastai siunčia ankstyvą pranešimą, susijusį su kiekviena neapmokėta SF, kad klientas būtų informuojamas, kai SF reikia sumokėti. **Išankstinio bandymo** pasirinkimą galima nustatyti taip, kad vienas kiekvieno proceso hierarchijos žingsnis būtų įgyvendintas kiekvienai SF, nes SF laikas pasiekia tą veiksmą.

### <a name="process-hierarchy"></a>Proceso hierarchija
Kiekvieną kliento telkinį galima priskirti tik vienai proceso hierarchijai. Šio veiksmo hierarchijos rangas nurodo, kuris procesas bus viršesnis, jei klientas įtrauktas į daugiau nei vieną telkinį, kuriam priskirta proceso hierarchija. Telkinio ID nustato, kurie klientai bus priskirti procesui. 

Ramios dienos naudojamos siekiant užtikrinti, kad automatizuotas procesas su klientu nesusisiektų per dažnai.  Pavyzdžiui, jei nustatytos dvi ramios dienos, automatizuotas procesas su klientu nesusisieks bent dvi dienas, net jei pradinė pagrindinė SF yra visiškai sudengta. 

Norėdami pašalinti klientus iš proceso automatizavimo, jei sąskaitos balansas arba SF balansas yra mažesnis už nustatytą vertę, nustatykite lauką **Pašalinti iš proceso** į **Taip** ir įveskite sumos vertę.

## <a name="process-details"></a>Proceso informacija
**Aprašas** naudojamas hierarchijos veiksmo paskirčiai arba pavadinimui nustatyti.

**Veiksmo tipas** apibrėžia, ar veiksmas sukurs veiklą, išsiųs el. laišką, ar sukurs priminimo laišką.

**Verslo dokumentas** apibrėžia šabloną, naudojamą kuriant veiksmo tipą.  Tai gali būti veiklos šablonas, el. laiško šablonas arba priminimo laiškas kiekvienam klientui. 

Veiksmų tipai gali būti kuriami prieš arba po SF apmokėjimo termino, remiantis parametru, kuris rodomas stulpelyje **Dienos, susijusios su SF apmokėjimo terminu**.

Pasirinkus el. pašto veiksmo tipą, gavėjas bus naudojamas nustatyti, ar tai klientas, pardavimo grupė, ar mokėjimų priežiūros agentas. Lauko **Verslo paskirties kontaktas** reikšmė nustatys, kuris tos klieno sąskaitos kontaktas gaus pranešimą.

## <a name="business-document-details"></a>Verslo dokumento informacija
Verslo dokumento informacija skirsis pagal veiksmo tipą, pasirinktą proceso informacijoje.  Kai veiksmo tipas yra veikla, bus rodoma veiklos šablono informacija.  Šie duomenys apima veiklos šablono pavadinimą, veiklos, kuri bus sukurta, tipą, veiklos paskirtį, numatytą dienų, kurių reikės veiklos užbaigimui, skaičių ir informaciją apie veiklą.  Ši veikla bus susieta su pagrindine SF, nurodančia gavėjui apie veiksmą, kurio reikia veiklai užbaigti.

Jei veiksmo tipas yra el. laiškas proceso informacijoje, šiame skyriuje bus du „FastTab”.  Pirmasis naudojamas norint nurodyti šablono ID, el. pašto aprašą, numatytąją kalbą, vartotojo vardą, kuris bus priskirtas automatiškai siunčiamiems el. laiškams, ir susijusių siuntėjų el. pašto adresus. Antrasis leis sukurti el. laišką po to, kai reikšmės laukuose **Kalba** ir **Tema** bus išsaugotos pasirinkus **Redaguoti**.  Atsidarys langas, kuris leis įkelti HTML turinį. Taip pat galite įvesti pranešimą, sukuriamą rankiniu būdu apatiniame kairiajame lango lauke.  

> [!Note]
> „Outlook” el. laišką galima įrašyti naudojant norimą pranešimo tekstą HTML formatu. Tada galima įkelti, kad šablonas būtų įgyvendintas. <br> <br> Jei pasirinktas priminimo laiško veiksmo tipas, sąrankos formoje nebus verslo dokumento informacijos skyriaus.


## <a name="fasttab-reference"></a>„FastTab” nuoroda
Toliau pateiktose lentelėse pateikiamas puslapių ir laukų, iš kurių galima pasiekti nurodytus „FastTab”, sąrašas ir to skirtuko informacijos aprašas. 

### <a name="process-hierarchy"></a>Proceso hierarchija

|     Puslapis                                                  |     Laukas                         |     Aprašas                           |
| --------------------------------------------------------  |-------------------------------    |---------------------------------------    |
|     Mokėjimų priežiūros proceso sąranka <br> Proceso automatizavimas       |                                   |     Kurkite ir tvarkykite mokėjimų priežiūros procesus, pagrįstus klientų telkinių priskyrimais.                                                                                                                             |
|     Mokėjimų priežiūros proceso sąranka <br> Proceso automatizavimas       |     Hierarchija                     |     Apibrėžia proceso automatizavimo prioritetą, kad būtų galima priskirti klientą, jei jis priklauso keliems telkiniams.                                                                                                   |
|     Mokėjimų priežiūros proceso sąranka <br> Proceso automatizavimas       |     Telkinio ID                       |     Užklausos, apibrėžiančios klientų įrašų grupę.                                                                                                                                                        |
|     Mokėjimų priežiūros proceso sąranka <br> Proceso automatizavimas       |     Ramios dienos                    |     Apribokite, kaip dažnai gali būti atliktas proceso veiksmas. Pavyzdžiui, jei nustatytos dvi ramios dienos, kitas proceso veiksmas nebus vykdomas bent dvi dienas, jei keičiasi pagrindinė SF.     |
|     Mokėjimų priežiūros proceso sąranka <br> Proceso automatizavimas       |     Pašalinti iš proceso        |     Pasirinkus **Kliento skirstymo pagal terminus balansas mažesnis nei** arba **SF suma mažesnė nei**, klientas bus pašalintas iš proceso automatizavimo, jei nesilaikoma verčių kriterijų.                                   |

### <a name="process-details"></a>Proceso informacija
|     Puslapis                                                  |     Laukas                                         |      Aprašas                  |
|--------------------------------------------------------   |-----------------------------------------------    |----------------------------   |
|     Mokėjimų priežiūros proceso sąranka <br> Proceso automatizavimas       |                                                   |     Apibrėžkite veiksmus, kurių buvo imtasi pagal pagrindinę SF.                                                                                                |
|                                                           |     Aprašas                                   |     Laisvos formos teksto laukas, naudojamas norint suteikti veiksmui pavadinimą ir (arba) aprašą.                                                                           |
|                                                           |     Veiksmo tipas                                   |     Veiklos, el. pašto ar priminimo laiškas, kuris bus sukurtas proceso veiksmo metu.                                                                     |
|                                                           |     Verslo dokumentas                           |     Apibrėžia veiklą arba el. laiško šabloną, kuris naudojamas proceso veiksmo metu.                                                                        |
|                                                           |     Kada                                          |     Nurodo, ar proceso veiksmas bus vykdomas prieš arba po pagrindinės SF apmokėjimo termino, ir nurodo lauką **Dienos, susijusios su SF apmokėjimo terminu**.        |
|                                                           |     Dienos, susijusios su sąskaitos faktūros termino data        |     Kartu su lauku **Kada** nurodo proceso veiksmo laiką.                                                                          |
|                                                           |     Išankstinis priminimas                                   |     Šis pasirinkimas leidžia nustatyti vieną kiekvienos SF proceso hierarchijos veiksmą ir jį vykdyti pagal kiekvieną SF, jai pasiekus laiko kriterijus.                                                |
|                                                           |     Gavėjas                                     |     Nurodo, ar el. laiškas bus išsiųstas klientui, pardavimo grupei ar mokėjimų priežiūros agentui.                                                   |
|                                                           |     Verslo paskirties kontaktas                    |     Nurodo, kuris gavėjo el. pašto adresas naudojamas el. pašto pranešimams.                                                                                 |

### <a name="business-process-activity-template-details"></a>Verslo procesų veiklos šablono informacija 
|     Puslapis                                                  |     Laukas                     |      Aprašas                  |
|--------------------------------------------------------   |----------------------------   |-------------------------  |
|     Mokėjimų priežiūros proceso sąranka <br> Proceso automatizavimas       |                               |     Sąrankos proceso skyrius, nurodantis veiklos šablono informaciją.                                                                      |
|     Mokėjimų priežiūros proceso sąranka <br> Proceso automatizavimas       |     Veiklos šablonas       |     Nurodo tipą, paskirtį, dienų, kurių reikia atlikimui, skaičių ir pateikia informaciją apie veiklą, kuri bus sukurta veiklos proceso veiksmo metu.       |

### <a name="business-document-email-template-details"></a>Verslo dokumento el. laiško šablono išsami informacija 
|     Puslapis                                                  |     Laukas     |      Aprašas                  |
|--------------------------------------------------------   |-------------- |-----------------------------  |
|     Mokėjimų priežiūros proceso sąranka <br> Proceso automatizavimas       |               |     Nurodo el. pašto aprašą, numatytąją kalbą, siuntėjo vardą ir el. pašto adresą, kuris bus sukurtas el. pašto proceso veiksmo metu.        |


### <a name="collections-history"></a>Mokėjimų retrospektyva 
|     Puslapis                              |     Laukas     |      Aprašas                                                          |
|------------------------------------   |-------------- |---------------------------------------------------------------------  |
|     Mokėjimų priežiūros proceso sąranka       |               |     Peržiūrėkite naujausią pasirinktos proceso hierarchijos retrospektyvą.       |

### <a name="collection-process-assignment"></a>Mokėjimų priežiūros proceso priskyrimas
|     Puslapis                              |     Laukas     |      Aprašas                                                  |
|------------------------------------   |-------------- |-----------------------------------------------------------    |
|     Mokėjimų priežiūros proceso sąranka       |               |     Peržiūrėkite klientus, priskirtus mokėjimų priežiūros procesui.  
|     Priskyrimas rankiniu būdu               |               |     Peržiūrėkite klientus, kurie buvo priskirti procesui rankiniu būdu arba pasirinkite klientus, kurie bus priskirti procesui. |
|     Peržiūrėti proceso priskyrimą      |               |     Peržiūrėkite klientus, kurie bus priskirti vykdomai strategijai.   |
|     Peržiūrėti kliento priskyrimą     |               |     Peržiūrėkite strategiją, kuriai priskirtas konkretus klientas.    |
 
 ### <a name="process-simulation"></a>Proceso imitavimas
|     Puslapis                              |     Laukas     |      aprašymas                                                  |
|------------------------------------   |-------------- |-----------------------------------------------------------    |
|    Proceso imitavimas                 |               |     Peržiūrėkite veiksmus, kurie bus sukurti, jei šiuo metu bus vykdomas pasirinkto proceso automatizavimas. |

### <a name="parameters"></a>Parametrai
|     Puslapis                                                                  |     Laukas                                             |      aprašymas                              |
|-------------------------------------------------------------------------- |------------------------------------------------------ |-------------------------------------  |
|     Gautinų sumų parametrai > Mokėjimų priežiūros proceso automatizavimas     |     Procentas klientų vienai paketinei užduočiai          |     Parametras, skirtas nustatyti paketinių užduočių skaičių viename automatizavimo procese.                                          |
|     Gautinų sumų parametrai > Mokėjimų priežiūros proceso automatizavimas     |     Registruoti priminimo laiškus automatiškai           |     Priminimo laiškų veiksmų tipai užregistruos laišką automatizavimo metu.                                      |
|     Gautinų sumų parametrai > Mokėjimų priežiūros proceso automatizavimas     |     Automatizavimo veiklų kūrimas                |     Kurkite ir uždarykite ne veiklų veiksmo tipų veiklas, kad būtų galima peržiūrėti visus automatizuotus veiksmus, atliktus sąskaitoje.        |
|     Gautinų sumų parametrai > Mokėjimų priežiūros proceso automatizavimas     |     Dienų, kiek truks mokėjimų priežiūros proceso automatizavimas, skaičius     |     Apibrėžia dienų, kiek saugoma mokėjimų priežiūros retrospektyva, skaičių.                                                       |
|     Gautinų sumų parametrai > Mokėjimų priežiūros proceso automatizavimas     |     Neįtraukti sąskaitos faktūros suaktyvinus paskutinį proceso veiksmą    |     SF, kuri pasiekia paskutinį mokėjimų priežiūros proceso veiksmą, nebus naudojama kuriant būsimus procesų automatizavimo veiksmų tipus. Kita seniausia SF nustatys kitą proceso automatizavimo veiksmą, kad būtų užtikrinti tolesni mokėjimų priežiūros proceso automatizavimo veiksmai.                                                        |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
