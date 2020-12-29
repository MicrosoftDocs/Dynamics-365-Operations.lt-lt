---
title: Užduočių planavimas
description: Šiame straipsnyje pateikiama informacija apie užduočių planavimą, kuris yra išsamesnė planavimo forma nei operacijų planavimas. Galite naudoti užduočių planavimo procesą atskiroms užduotims arba darbo užsakymams suplanuoti bei gamybos aplinkai valdyti.
author: ChristianRytt
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19431
ms.assetid: aef37341-91d8-4263-80eb-35d9584be156
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bff966a68001d479b8631e13caa18c9ec8d2bf4c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433821"
---
# <a name="job-scheduling"></a>Užduočių planavimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie užduočių planavimą, kuris yra išsamesnė planavimo forma nei operacijų planavimas. Galite naudoti užduočių planavimo procesą atskiroms užduotims arba darbo užsakymams suplanuoti bei gamybos aplinkai valdyti.

Galite naudoti užduočių planavimo procesą atskiroms užduotims arba darbo užsakymams suplanuoti bei gamybos aplinkai valdyti. Vykdant užduočių planavimo procesą kiekviena operacija padalinama į atskiras užduotis. Tada šios užduotys priskiriamos operacijų ištekliams, kuriuos naudojant šios užduotys bus atliekamos. Be to, vykdydami užduočių planavimo procesą galėsite sinchronizuoti visas pasirinktoje užduotyje nurodytas užduotis. Galite nurodyti užduoties pradžios arba pabaigos datą ir laiką, tada atlikti planavimo procesą. Nurodytas laikas gali būti pradžios arba pabaigos laikas – tai priklauso nuo planavimo krypties. Ši funkcija naudinga, kai, pavyzdžiui, užduotį vienu metu galima atlikti tik viename įrenginyje arba kai norima optimizuoti užduotį, kuri atliekama naudojant visus išteklius.

## <a name="tasks-in-the-job-scheduling-process"></a>Užduočių planavimo proceso užduotys
Vykdant užduočių planavimo procesą atliekamos toliau nurodytos užduotys.

-   Operacijos išskaidomos į užduotis.
-   Užduotys suplanuojamos pagal išteklių datas ir laiką, nurodytą susijusioje operacijoje.
-   Apskaičiuojamas kiekvienos užduoties pradžios ir pabaigos laikas. Naudodami riboto pajėgumo parinktį galite užtikrinti, kad nebūtų sutampančių laikotarpių.
-   Nustatykite, kuriems išteklių grupės ištekliams taikyti užduotį. Šiai užduočiai atlikti reikia nurodyti operacijos išteklių grupę. Vykdant užduočių planavimo procesą ištekliai arba išteklių grupės pasirenkamos pagal trumpiausią gamybos laiką bei taip pat yra atsižvelgiama į visus ankstesnius išteklių rezervavimus.
-   Operacijos išskaidomos į užduotis. Užduotys pagal datą ir laiką suplanuojamos remiantis gamybos maršrute nurodytu užsakymu. Nustatant operaciją nurodomos užduotys, į kurias bus išskaidyta vykdant planavimo procesą. Naudojant operacijai priskirtą maršrutų grupę valdoma, ar bus generuojamos užduotys. Užduotis generuojama tik tuomet, jei turi konkrečią trukmę. Pavyzdžiui, transportavimo laiko užduotis generuojama, jei pasirinktoje operacijoje buvo nurodytas transportavimo laikas.

## <a name="scheduling-direction"></a>Planavimo kryptis
Užduotis galite suplanuoti pirmyn arba atgal.

-   **Pirmyn** – naudokite planavimo kryptį Pirmyn, kad gamybos užduotis būtų pradedama kaip įmanoma anksčiau. Vykdant gamybos procesą gamybos užduotis perkeliama link proceso pradžios, todėl ši kryptis dar vadinama stūmimo metodu. Gamybos užduotis suplanuojama, kad prasidėtų ir pasibaigtų kaip įmanoma anksčiau.
-   **Atgal** – naudokite planavimo kryptį Atgal, kad gamybos užduotis būtų pradedama kaip įmanoma vėliau. Ši kryptis taikoma pagal gamybos proceso užbaigimo datą, todėl ji dar vadinama traukimo metodu. Taikant planavimo kryptį Atgal skaičiuojama atgal iki vėliausios galimos datos, kada galima pradėti gamybos užduotį nepraleidžiant jos tikslinio termino.

## <a name="finite-capacity"></a>Ribotas pajėgumas
Galite suplanuoti užduotis naudodami riboto pajėgumo metodą. Jį naudojant suplanuotas pajėgumas negali būti didesnis už prieinamą išteklių pajėgumą. Galimas laikas apibrėžiamas kaip intervalas, kai išteklius yra prieinamas, o pajėgumas nėra rezervuotas niekur kitur. Vykdant planavimo pagal ribotą pajėgumą procesą užtikrinama, kad esant tam tikrai datai nepersidengs operacijos pradžios ir pabaigos laikai. Atsižvelgiama į jau rezervuotus išteklių pajėgumus bei pradžios ir pabaigos laikų persidengimus. Naudojant riboto pajėgumo metodą nustatoma būtinai prieinama išteklių pajėgumo apimtis, kad būtų optimaliai naudojami šie ištekliai. Ši nustatyta apimtis suderinama su apskaičiuotu trumpiausiu galimu gamybos laiku tarp operacijų.

## <a name="finite-materials"></a>Ribotos medžiagos
Vykdant užduočių planavimo pagal ribotas medžiagas procesą užtikrinama, kad prasidėjus operacijai reikalingos medžiagos bus prieinamos. Prekių padengimo taisyklėse apibrėžiamos šios ribos. Vykdant planavimo procesą poreikio išskleidimo metodas naudojamas sudedamųjų prekių prieinamumo laikui nustatyti. Jei suplanuosite nenustatę ribotų medžiagų metodo, sistemoje bus laikoma, kad prireikus visos medžiagos yra prieinamos.

## <a name="finite-properties"></a>Ribotos ypatybės
Vykdant užduočių planavimo procesą pagal specialių ypatybių metodą būtinai turi būti nurodytos gamybos maršruto operacijų ypatybės. Šios ypatybės turi būti įvykdytos, kad būtų rezervuotas pajėgumas.

## <a name="references"></a>Nuorodos
Vykdant užduočių planavimo procesą suplanuojamos visos esamoje gamybos užduotyje nurodomos gamybos užduotys. Pagrindinės gamybos užduotis negali būti pradėta, kol nebus atliktos susijusios tarpinės gamybos užduotys, tad jei gamybos užduotyje nurodyta viena ar kelios tarpinės gamybos užduotys, jos turi būti suplanuotos tuo pačiu laiku kaip pagrindinė gamybos užduotis.

## <a name="schedule-resources"></a>Planuoti išteklius
Naudojant planavimo mechanizmą tikrinami išteklių deriniai, siekiant nustatyti reikalavimus galinčius atitikti derinius. Pasirinkimo kriterijus galite nurodyti pasirinkę kurią nors toliau pateiktą puslapio **Planavimo parametrai** lauko **Pirminių išteklių pasirinkimas** reikšmę.

-   **Trukmė** – naudojant planavimo mechanizmą pasirenkami ištekliai, kurių gamybos laikas trumpiausias. **Pastaba.** Vykdant planavimo pagal trukmę procesą gali sumažėti našumas, jei toje pačioje išteklių grupėje bus daug išteklių bei bus naudojamos antrinės operacijos. Vienoje operacijoje galite suplanuoti daugiausia 32 išteklius. Jei viršysite šį kiekį, bus pateikiamas sistemos pranešimas, o vykdant užduočių planavimo procesą geriausi alternatyvūs ištekliai nebus surasti.
-   **Prioritetas** – naudojant planavimo mechanizmą pasirenkami didžiausio prioriteto ištekliai, jei bent dvejų išteklių pajėgumai ir lygmenys bus identiški. Išteklių, kurių skaitinė vertė šiame lauke nurodyta mažiausia, prioritetas yra didžiausias.

Paleidus užduočių planavimo procesą sistemoje ištekliai suplanuojami pagal išteklių parametruose nustatytus apribojimus. Naudodami kalendoriaus parametrus galite valdyti išteklių pajėgumą. Vykdant planavimo procesą sistemoje apskaičiuojamos išteklių apkrovos. **Pastaba.** Jei vykdant gamybos procesą naudojama operacijų planavimo funkcija, įvykdę šią funkciją galite paleisti užduočių planavimo procesą. Jei nenaudojate operacijų planavimo funkcijos, užduočių planavimo procesą galite vykdyti atskirai.

## <a name="maximum-capacities-for-resources-per-job-order"></a>Maksimalūs užduoties užsakymo išteklių pajėgumai
Vykdant užduočių planavimo procesą ištekliai priskiriami užduotims. Galite nustatyti maksimalius užduoties užsakymo išteklių pajėgumus. Pavyzdžiui, galite nustatyti, kad sistemoje apdorojant gamybos užsakymą būtų suplanuojama naudoti ne daugiau nei 50 procentų viso pajėgumo apimties. Taikydami šį nustatymą, užduočių planavimo lygmeniu galėsite geriau valdyti išteklių planavimo užduotį. Be to, jį taikant galima išvengti problemų, kai pajėgumo nepakanka gamybos užduotims vienu metu atlikti.

## <a name="resource-efficiency"></a>Išteklių efektyvumas
Atliekant užduočių planavimo procesą atsižvelgiama į nurodytas išteklių efektyvumo procentines reikšmes. Taikant efektyvumo procentines reikšmes sumažinamas arba padidinamas rezervuotas išteklių laikas. Be to, padidinamas arba sumažinamas ir gamybos laikas. Skaičiuojant naudojama toliau nurodyta formulė: Planavimo laikas = laikas x 100 ÷ efektyvumo procentinė reikšmė Į šios formulės reikšmę *Laikas* įtraukiami apdorojimo ir nustatymo laikai.



