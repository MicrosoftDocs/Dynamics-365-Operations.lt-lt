---
title: Mokėjimų priežiūros proceso automatizavimas
description: Šioje temoje aprašomas mokėjimų priežiūros proceso strategijų, kurios automatiškai identifikuoja klientų SF, kurioms reikalingas priminimas el. paštu, mokėjimų veikla ar priminimo laiškas, kuris bus išsiųstas klientui, nustatymo procesas.
author: JodiChristiansen
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
ms.openlocfilehash: 59db852024faf457db7ac145b67619b31555aaf2
ms.sourcegitcommit: 3f6cbf4fcbe0458b1515c98a1276b5d875c7eda7
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/10/2021
ms.locfileid: "7486874"
---
# <a name="collections-process-automation"></a>Surinkimo proceso automatizavimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas mokėjimų priežiūros proceso strategijų, kurios automatiškai identifikuoja klientų SF, kurioms reikalingas priminimas el. paštu, mokėjimų veikla (pvz., telefono skambutis) ar priminimo laiškas, kuris bus išsiųstas klientui, nustatymo procesas. 

Organizacijos dažnai išleidžia daug laiko tirdamos suskirstytų pagal terminus balansų ataskaitas, klientų sąskaitas ir atviras SF, kad sužinotų, su kuriais klientais reikėtų susisiekti dėl atviros SF ar sąskaitos balanso. Šie tyrimai užima laiką, kurį mokėjimų priežiūros agentas galėtų praleisti bendraudamas su klientais, kad būtų surinkti pasibaigusio termino balansai, ar spręsdamas su SF susijusius konfliktus. Mokėjimų priežiūros proceso automatizavimas leidžia nustatyti strategija pagrįstą jūsų mokėjimų priežiūros proceso metodą. Tai padeda nuosekliai taikyti mokėjimų priežiūros veiklas pateikiant tinkintus priminimus el. paštu arba suprogramuotą priminimo laiškų siuntimo procesą. 

## <a name="collections-process-setup"></a>Mokėjimų priežiūros proceso sąranka
Galite naudoti puslapį **Mokėjimų priežiūros proceso sąranka** (**Kredito ir mokėjimų priežiūra > Sąranka > Mokėjimų priežiūros proceso sąranka**), kad būtų sukurtas automatizuotas mokėjimų priežiūros procesas, skirtas veikloms planuoti, el. laiškams siųsti ir klientų priminimo laiškams kurti bei registruoti. Proceso veiksmai yra pagrįsti pagrindine arba seniausia atvira SF. Kiekvienas veiksmas naudoja šią SF, kad nustatytų, kokie konkretaus kliento ryšiai ar veikla turi įvykti.  

Mokėjimų priežiūros komandos paprastai siunčia ankstyvą pranešimą, susijusį su kiekviena neapmokėta SF, kad klientas būtų informuojamas, kai SF reikia sumokėti. **Išankstinio bandymo** pasirinkimą galima nustatyti taip, kad vienas kiekvieno proceso hierarchijos žingsnis būtų įgyvendintas kiekvienai SF, nes SF laikas pasiekia tą veiksmą.

### <a name="process-hierarchy"></a>Proceso hierarchija
Kiekvieną kliento telkinį galima priskirti tik vienai proceso hierarchijai. Šio veiksmo hierarchijos rangas nurodo, kuris procesas bus viršesnis, jei klientas įtrauktas į daugiau nei vieną telkinį, kuriam priskirta proceso hierarchija. Telkinio ID nustato, kurie klientai bus priskirti procesui. Kiekviena nustatyta hierarchija gali būti priskirta tik vienam proceso automatizavimui.

Ramios dienos naudojamos siekiant užtikrinti, kad automatizuotas procesas per dažnai nesusisiektų su klientu. Pavyzdžiui, jei nustatytos dvi ramios dienos, automatizuotas procesas su klientu nesusisieks bent dvi dienas, net jei pradinė pagrindinė SF yra visiškai sudengta. 

Norėdami neįtraukti klientų į proceso automatizavimą, jei klientų skirstymo pagal terminus balansas arba SF suma yra mažesnė nei nustatyta vertė, pasirinkite **Skirstymo pagal terminus balanso suma mažesnė nei** arba **SF suma mažesnė nei** lauke **Neįtraukti į procesą** ir įveskite sumos vertę.

Pažymėkite **Naudoti prognozę**, kad sukurtumėte rinkinių veiklas naudodami Klientų mokėjimo prognozes. Sukurtos veiklos naudos Veiklos šabloną iš **Mokėjimo prognozių**, esančių **Gautinų paskyrų parametrų** puslapio **Mokėjimų proceso automatizavimo** skirtuke. 

### <a name="process-details"></a>Proceso informacija
Spustelėkite **Naujas**, kad į hierarchiją įtrauktumėte naują proceso informaciją. **Aprašas** yra naudojamas hierarchijos veiksmo paskirčiai arba pavadinimui nustatyti. Pasirinkite **Veiksmo tipą** kad apibrėžtumėte, ar veiksmas sukurs veiklą, išsiųs elektroninį laišką, ar sukurs priminimo laišką. 

- **Verslo dokumentas** apibrėžia šabloną, naudojamą veiksmo tipo kūrimui. Šis dokumentas gali būti veiklos šablonas, elektroninio laiško šablonas arba priminimo laiškas, siunčiamas kiekvienam klientui. Rinkinių proceso automatizavimas sukuria tik priminimo laiškus vienam klientui, nepaisant to, kaip nustatyti kiti rinkinių parametrai.
- **Kai** nurodo proceso veiksmą, kuris įvyks prieš arba po priekinio (seniausio) SF termino datos, ir bus naudojamas kartu su numeriu, rodomu **Su SF terminu susijusios dienos** stulpelyje. 
- Pažymėkite **Anksčiausios sumos** parinktį, kad sukurtumėte veiksmą kiekvienai SF vienu proceso hierarchijos veiksmu. Anksčiausios sumos veiksmai paprastai yra ankstyvas pranešimas, susijęs su kiekviena neapmokėta SF, kad klientas būtų informuojamas, iki kada būtina sumokėti SF. Anksčiausia suma yra galima pažymėti tik vienai hierarchijos veiklai. Pasirinkus elektroninio pašto veiksmo tipą, gavėjas bus naudojamas nustatyti, ar elektroninis laiškas nusiųstas klientui, pardavimo grupei, ar mokėjimų priežiūros agentui. 
- Lauko **Verslo paskirties kontaktas** reikšmė nustatys, kuris tos klieno sąskaitos kontaktas gaus pranešimą.

### <a name="business-document-details"></a>Verslo dokumento informacija
Verslo dokumento informacija skirsis pagal veiksmo tipą, pasirinktą proceso informacijoje. Kai veiksmo tipas yra veikla, bus rodoma veiklos šablono informacija. Šie duomenys apima veiklos šablono pavadinimą, veiklos, kuri bus sukurta, tipą, veiklos paskirtį, numatytą dienų, kurių reikės veiklos užbaigimui, skaičių ir informaciją apie veiklą. Ši veikla bus susieta su pagrindine SF, nurodančia gavėjui apie veiksmą, kurio reikia veiklai užbaigti.

Jei veiksmo tipas yra el. laiškas proceso informacijoje, šiame skyriuje bus du „FastTab”. Pirmasis naudojamas norint nurodyti šablono ID, el. pašto aprašą, numatytąją kalbą, vartotojo vardą, kuris bus priskirtas automatiškai siunčiamiems el. laiškams, ir susijusių siuntėjų el. pašto adresus. Antrasis leis sukurti el. laišką po to, kai reikšmės laukuose **Kalba** ir **Tema** bus išsaugotos pasirinkus **Redaguoti**. Atsidarys langas, kuris leis įkelti HTML turinį. 

> [!Note]
> Jūs galite išsaugoti „Outlook” elektroninį laišką, kuriame yra pranešimo tekstas HTML formatu. Tada galite įkelti pranešimo turinį, kad įgyvendintumėte šabloną. <br> <br> Jei pasirinktas priminimo laiško veiksmo tipas, sąrankos puslapyje nebus verslo dokumento informacijos skyriaus.

Naudokite **Mokėjimų priežiūros procesų retrospektyvos** mygtuką, jei norite peržiūrėti naujausią pasirinkto proceso hierarchijos retrospektyvą. 

Spustelėkite **Priminimų proceso priskyrimo** veiksmą, kad peržiūrėtumėte klientus, priskirtus priminimų procesui. Naudokite **Peržiūrėti kliento priskyrimą**, jei norite peržiūrėti hierarchiją, kuriai priskirtas konkretus klientas. Naudokite **Peržiūrėti kliento priskyrimą**, jei norite peržiūrėti klientus, kurie bus priskirti hierarchijai ją paleidus. Spustelėkite **Rankinis priskyrimas**, kad peržiūrėtumėte klientus, kurie buvo priskirti procesui rankiniu būdu arba pasirinkite klientus, kurie bus priskirti procesui.

Spustelėkite **Proceso simuliacija** veiksmą, kad peržiūrėtumėte veiksmus, kurie bus sukurti, jei šiuo metu bus vykdomas pasirinkto proceso automatizavimas. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
