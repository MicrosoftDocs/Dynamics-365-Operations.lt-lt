---
title: "„Operations“ ištekliai"
description: "Operacijų ištekliai atlieka projekto arba gamybos proceso veiklas. Jie gali būti skirtingų tipų ir jų galimybės gali skirtis."
author: sorenva
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c4018632e5e20470948ee59e4bb2a1cab905d829
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="operations-resources"></a>„Operations“ ištekliai

[!INCLUDE [banner](../includes/banner.md)]

Operacijų ištekliai atlieka projekto arba gamybos proceso veiklas. Jie gali būti skirtingų tipų ir jų galimybės gali skirtis. 

<a name="operations-resources"></a>„Operations“ ištekliai
--------------------

Operacijos ištekliai yra mašinos, įrankiai, darbuotojai, patalpos, fizinės vietos arba tiekėjai, vykdantys projekto ar gamybos proceso veiklą. Jie gali būti skirtingų tipų ir jų galimybės gali skirtis.

-   **Tiekėjas** – išorinis išteklius, vykdantis projekto veiklą arba gamybos operacijas. Pavyzdys gali būti subrangovas. Tiekėjų išteklius susiedami su tiekėjo sąskaita, galite generuoti subrangovų pirkimus pagal komplektavimo specifikacijos (KS) eilutes arba gamybos eilutes.
-   **Personalas** – projekto arba gamybos darbuotojas, vykdantis veiklą atskirai arba kaip įrankio ar mašinos operatorius. Jei naudojate personalo valdymo funkcijas, personalą galite susieti su darbuotoju. Planavimo mechanizmas tada išteklius paskirstyti pagal nurodytas atitinkamo darbuotojo kompetencijas.
-   **Mašina** – mašina ar kita gamybos įranga, būtina gamybai vykdyti.
-   **Įrankis** – prietaisas arba įrenginys, paprastai naudojamas kartu su kitu ištekliumi projekto arba gamybos veiklai vykdyti.
-   **Vieta** – tam tikro dydžio fizinė vieta, būtina norint atlikti veiklą. Pavyzdys gali būti surinkimo sritis.
-   **Patalpa** – pastatas statybos arba fiksuota struktūra, būtina norint atlikti veiklą.

## <a name="calendars"></a>Kalendoriai
Kalendorių galima priskirti operacijų ištekliui; jis nurodo to ištekliaus pajėgumą (valandomis). Operacijų išteklių darbo laikas nustatomas pagal kalendorių, priskirtą išteklių grupei, kuriai operacijų išteklius priklauso. Galite nustatyti priskirto kalendoriaus įsigaliojimo datą ir galiojimo pabaigos datą. Tada operacijų ištekliui galite priskirti daugiau nei vieną kalendorių. Tačiau priskirtų kalendorių datos negali persidengti, o operacijų ištekliui vienu metu galima priskirti tik vieną kalendorių. **Note:** jei nėra galiojančių išteklių grupės darbo kalendorių (pvz., jei paskutinio priskirto kalendoriaus arba vienintelio priskirto kalendoriaus galiojimo data pasibaigė), jūs nebegalėsite prieiti prie išteklių grupėms priskirtų operacijų išteklių, skirtų gamybai ir operacijoms planuoti. Taip pat kalendorių galite priskirti išteklių grupei, norėdami nurodyti išteklių grupės ir visų išteklių grupei priskirtų operacijų išteklių darbo laikus. Išteklių grupės pajėgumas apskaičiuojamas kaip visų išteklių grupei priskirtų operacijų išteklių pajėgumų suma. Laikui bėgant išteklių grupei priskirtas kalendorius gali keistis.

## <a name="resource-capabilities"></a>Išteklių galimybės
Pajėgumas yra operacijų ištekliaus gebėjimas atlikti tam tikrą veiklą. Operacijų ištekliui galite priskirti vieną arba daugiau pajėgumų. Tada planavimo mechanizmas išteklius paskirstys derindamas kiekvienos veiklos išteklių poreikius ir turimų operacijų išteklių pajėgumus. Pajėgumus galima priskirti visų tipų operacijų ištekliams (**Įrankis**, **Tiekėjas**, **Mašina**, **Personalas**, **Vieta** arba **Patalpa**). Norėdami operacijų ištekliams pajėgumus priskirti laikinai, nurodykite pajėgumo priskyrimo pradžios ir pabaigos datas. Daugiau informacijos žr. [Išteklių pajėgumai](resource-capabilities.md).

## <a name="resource-groups"></a>Išteklių grupės
Išteklių grupė yra operacijų išteklių rinkinys, nurodantis, kaip detaliai norite planuoti išteklius, kai naudojate operacijų planavimo metodą. Todėl išteklių grupės paprastai atitinka fizinį darbo elementų išdėstymą, ant gamybos cecho grindų apibrėžtą geltonomis linijomis. Išteklių grupė apibrėžia grupei priskirtų operacijų išteklių teritoriją, gamybos vienetą ir sandėlio kontekstą. Kai operacijų išteklių priskiriate išteklių grupei, išteklių galite planuoti teritorijoje, kurioje yra išteklių grupė. Jūsų sukurtų operacijų išteklių išteklių grupei priskirti nereikia. Tačiau operacijų išteklius turi būti priskirtas išteklių grupei, norint planuoti jo darbą. Operacijų ištekliai išteklių grupėms gali būti priskirti ribotą laiką. Taip pat operacijų išteklių galite priskirti kelioms išteklių grupėms ir bendrai išteklių naudoti visose teritorijose. Tačiau įsigaliojimo datos ir galiojimo pabaigos datos persidengti negali. Kitaip tariant, negalite operacijų išteklių tuo pačiu metu priskirti kelioms išteklių grupėms. Išteklių grupės priskyrimų pakeitimai galioja tik naujiems išteklių paskirstymams. Užduočių, operacijų ir projekto valandų prognozių, kurios jau yra suplanuotos, pajėgumo rezervavimams pakeitimai įtakos neturės. **Pastaba:** kai tipo **Tiekėjas** operacijų išteklius priskiriate išteklių grupei, visi tai išteklių grupei priskirti operacijų ištekliai turi būti tipo **Tiekėjas** ir turi būti susieti su ta pačia tiekėjo sąskaita.

## <a name="production-units"></a>Gamybos vienetai
Gamybos vienetas yra administracinis vienetas, kuris yra išteklių grupių rinkinys. Gamybos vienetą gali sudaryti kelios išteklių grupės, bet išteklių grupė gali būti priskirta tik vienam gamybos vienetui. Gamybos vienetas atspindi faktinį gamybos išteklių išdėstymą, bet nedaro įtakos operacijoms arba jų apdorojimui. Turite susieti gamybos vienetą ir teritoriją. Gamybos vienetui taip pat galite priskirti paėmimo sandėlį ir saugojimo sandėlį. Gamybos vienetą galima naudoti norint konsoliduoti ir filtruoti su gamyba susijusius duomenis. Pvz., gamybos cecho vadybininkas gali peržiūrėti tam tikro gamybos vieneto neišnaudotą darbo krūvį ir turimus pajėgumus. Galima pakeisti išteklių grupei priskirtą gamybos vienetą. Taip pat galima gamybos vienetą panaikinti. Tačiau šie pakeitimai gamybos vienetui atliekami tik naujiems užsakymams, kurie sukurti po bendrojo planavimo. Jeigu gamybos vieneto pakeitimą norite pritaikyti esamiems užsakymams, tai reikia atlikti neautomatiniu būdu.

## <a name="resource-scheduling"></a>Išteklių planavimas
Operacijos ištekliai yra priskiriami veikloms, kai suplanuojamas projektas arba gamyba. Galima naudoti du planavimo metodus: operacijų planavimą ir užduočių planavimą. Kai naudojate operacijų planavimo metodą, kiekviena operacijos arba projekto veikla yra suplanuojama išteklių grupėje, kurioje yra operacijų ištekliai, atitinkantys nurodytus operacijos išteklių reikalavimus. Jei operacijai atlikti reikalingas konkretus operacijų išteklius, planavimas rezervuoja tik konkretaus grupės operacijų ištekliaus pajėgumą. Užduočių planavimas yra išsamesnis planavimo būdas nei operacijų planavimas. Jis kiekvieną operaciją padalina į atskiras užduotis. Tada šios užduotys priskiriamos operacijų ištekliams, kuriuos naudojant šios užduotys bus atliekamos. Planavimas rezervuoja pajėgumą išteklių grupėse pagal operacijų laiką, nurodytą gamybos maršruto arba projekto veiklose. Jei pajėgumas yra ribotas, grafikas priklauso nuo operacijos išteklių, reikalingų veiklai atlikti, prieinamumo. Naudojant operacijų planavimo metodą, išteklių grupės pajėgumas yra galimų tos grupės operacijų išteklių pajėgumų suma. Esami operacijų išteklių pajėgumų rezervavimai laikomi neprieinamu pajėgumu. Jei nėra pakankamai pajėgumų gamybai vykdyti, gamybos užsakymus galima atidėti arba net sustabdyti. Puslapyje **Ištekliai** galite nurodyti kelias ypatybes, valdančias pajėgumų rezervavimo procesą.

-   **Pajėgumas** – nurodykite operacijų išteklių pajėgumą per valandą pajėgumo matavimo vienetais.
-   **Paketo pajėgumai** – nurodykite didžiausią vienetų, kuriuos vykdymo metu operacijų išteklius gali apdoroti, skaičių.
-   **Efektyvumo procentas** – nurodykite efektyvumą, kurio tikitės iš operacijų ištekliaus. Efektyvumo procentas reguliuoja operacijų ištekliaus našumą ir veikia ištekliui rezervuotą laiką. Atitinkamai pakoreguojamas operacijų, naudojančių operacijų išteklių, vykdymo laikas. Skaičiuojant naudojama toliau nurodyta formulė: planavimo laikas = laikas x 100 ÷ efektyvumo procentinė reikšmė. *Laiką* sudaro apdorojimo laikas ir nustatymo laikas.
-   **Operacijų planavimo procentas** – nurodykite maksimalų operacijos ištekliaus pajėgumo procentą, kurį norite naudoti planuodami operacijas. Nurodyta vertė turi būti mažesnė nei 100 procentų, kad planuojant užduotis būtų galima lanksčiai naudoti pajėgumą.
-   **Ribotas pajėgumas** – jei operacijos išteklius turėtų būti planuojamas pagal faktinį turimą pajėgumą ir jei reikia atsižvelgti į esamų pajėgumų rezervavimus, šią parinktį nustatykite į **Taip**. Jei ši parinktis nustatyta į **Ne**, daroma prielaida, kad operacijos ištekliaus pajėgumas yra neribotas, todėl šis išteklius gali būti perpildytas.
-   **Ribota ypatybė** – nustatykite šią parinktį į **Taip**, jei operacijos išteklius turėtų būti planuojamas pagal faktinį turimą pajėgumą, atsižvelgiant į reikiamas darbo laiko planavimo ypatybes.
-   **Išskirtinis** – nustatykite šią parinktį į **Taip**, jei nenorite, kad atliekant kitą užduotį arba operaciją operacijų ištekliaus nebūtų galima naudoti, kol nebus baigta dabartinė gamyba. Šiuo atveju operacijų ištekliaus negalima naudoti net jei yra ištekliaus apdorojimo laiko spragų.
-   **Ribotosios spartos ištekliai** – operacijų išteklių nurodykite kaip ribotosios spartos išteklių. Ribotosios spartos ištekliai planuojami naudojant ribotą pajėgumą, kai puslapyje **Bendrieji planai** pasirenkamos parinktys **Ribotas pajėgumas** ir **Ribotosios spartos planavimas**.

Norėdami tuo pačiu metu suplanuoti keletą operacijų išteklių, pvz., gamybos operacijai atlikti, turite nurodyti įvairių išteklių reikalavimus naudodami pirmines ir antrines operacijas. Tada taip pat galite rezervuoti kelis skirtingų pajėgumų operacijų išteklius. Suplanuotas pirminės operacijos operacijų išteklius nustato veiklos trukmę.

## <a name="lean-work-cells"></a>„Lean“ darbo elementai
Galite nurodyti, kad išteklių grupė yra „lean“ darbo elementas. Tada išteklių grupė gali būti gamybos eigos dalis. Nustatydami išteklių grupę kaip „lean“ darbo elementą, jūs taip pat neleisite išteklių grupę ir priskirtus operacijų išteklius paskirstyti gamybos užsakymo arba projekto valandų prognozės operacijoms. Reikia nurodyti kiekvienos išteklių grupės, kuri veikia kaip „lean“ darbo elementas, toliau pateiktą informaciją.

-   **Kalendorius** – darbo elemento, kurio ypatybė turi būti standartinė darbo diena, darbo kalendorius.
-   **Įvesties sandėlis ir vieta** – numatytoji vieta, kurioje paimamos veiklai skirtos medžiagos.
-   **Išeigos sandėlis ir vieta** – numatytoji vieta, kurioje padedama visa darbo elemento išeiga.
-   **Apdorojimo laiko išlaidų kategorija** – ši darbo elemento kategorija turi būti nurodyta, jei įkainojant sekamas tiesioginis darbas.

Kai išteklių grupė yra naudojama kaip „lean“ darbo elementas, darbo elemento pajėgumas yra tiesiogiai nurodytas išteklių grupėje. Todėl operacijų išteklių išteklių grupei priskirti nereikia. Tik kai darbo elementą valdo subrangovas, darbo elementui turi būti priskirti tipo **Tiekėjas** operacijų ištekliai. Jei operacijos išteklių priskiriate išteklių grupei, kuri pažymėta kaip darbo elementas, tai neturės įtakos darbo elemento pajėgumui.

## <a name="costing-resources"></a>Įkainojimo ištekliai
Kai nustatote veiklą, pvz., maršruto operaciją arba projekto valandų prognozę, galite nurodyti konkretaus operacijų ištekliaus arba išteklių grupės reikalavimą. Tačiau taip pat galite nurodyti konkretaus tipo, pajėgumo arba kompetencijos operacijų ištekliaus reikalavimą. Dėl šios priežasties faktinis išteklių priskyrimas nėra atliekamas tol, kol nesuplanuota veikla ir nerezervuotas pajėgumas. Todėl maršruto operacijoje galite nurodyti, kad įvertinimas ir KS skaičiavimas turi būti paremtas konkrečiu operacijų ištekliumi. Šis operacijų išteklius yra vadinamas įkainojimo ištekliumi. Taip pat išlaidų kategorijas ir operacijų laiką galite perkelti iš įkainojimo ištekliaus į veiklą. Suplanavus operaciją, įvertinimas ir KS skaičiavimas yra atliekami naudojant faktiškai suplanuotą operacijų išteklių.




