---
title: Turto valdymo parametrai
description: Turto valdymo srityje būtina nustatyti bendruosius parametrus, susijusius su turtu, darbo užsakymais ir darbo užsakymų planavimu.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3ccbb7eed643abf613f8b75ae78854246d20f6d
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569883"
---
# <a name="asset-management-parameters"></a>Turto valdymo parametrai

[!include [banner](../../includes/banner.md)]

 

Turto valdymo srityje būtina nustatyti bendruosius parametrus, susijusius su turtu, darbo užsakymais ir darbo užsakymų planavimu. Šioje temoje aiškinama, kaip juos nustatyti. Pasirinkite **Turto valdymas** > **Sąranka** > **Turto valdymo parametrai**, kad atidarytumėte formą.

Mygtukas **Kurti duomenų vedlį** gali būti naudojamas siekiant automatiškai kurti sąrankos duomenis tikrinimo ar demonstracinės versijos tikslais įmonėje naudojant Dynamics 365 Supply Chain Management. Informacijos, kaip naudoti vedlį, ieškokite techninėje dokumentacijoje „Tikrinimo duomenų nustatymas naudojant turto valdymą“.

**Turto** nuoroda

- **Numatytoji funkcinė vieta** yra standartinė funkcinė vieta, kuri kuriant naują turtą automatiškai pasirenkama turtui.  
- Lauke **Standartinis kalendorius** pasirinkite kalendorių, kuris bus naudojamas skaičiuojant turto KPI, jei turtui nepasirinktas joks išteklius.  
- Lauke **Rodinys** pasirinkite standartinį rodinį, rodomą atidarius formą **Turto rodinys**(**Turto valdymas** > **Bendra** > **Turtas** > **Turto rodinys**).
- **Numatytasis užklausos tipas** yra standartinis priežiūros užklausos tipas, kuris automatiškai pasirenkamas kuriant naują užklausą.  
- Jei norite kurti su turtu susijusius projektus, projekto ryšius, susijusius su **Pagrindinio projekto**, **Projekto hierarchijos** pasirinkimu ir galimybe **Automatiškai kurti projektus**, nustatykite **Turto valdymo parametrus**.  
- Lauke **Darbo užsakymo projekto šablonas** galite nustatyti darbo užsakymams ir antriniam turtui leistinų antrinių projektų skaičių. Darbo užsakymo šablonas naudojamas nustatyti, kiek darbo užsakymų galima sukurti turtui ir naudoti susijusiame darbo užsakymo užduoties projekte. Darbo užsakymo šablonas nustatytas lauke **Susijusio darbo užsakymo šablonas** srityje **Turto valdymo parametrai** (**Turto valdymas** > **Sąranka** > **Turto valdymo parametrai** > **Darbo užsakymai**).  
>[!NOTE]
>Susijusio darbo užsakymo šablono formatas yra maišos ženklų (#) skaičius, priklausomai nuo maksimalaus darbo užsakymų, kuriuos tikitės sukurti turtui, skaičiaus. Pavyzdys: ## leidžia sukurti iki 99 antrinių projektų.  
- Užduočių tipų prognozės saugomos projekte, pasirinktame lauke **Prognozės projektas**. Kiekvienam užduoties tipui prognozės projekte automatiškai sukuriama nauja veikla. Užduoties tipo prognozės išsaugomos prognozės projekte.  
- Lauke **Modelis** pasirinkite prognozės modelį, naudojamą užduoties tipui ir darbo užsakymo prognozėms.  


**Darbo užsakymų** saitas

- **Numatytasis darbo užsakymo tipas** apibrėžia standartinius parametrus kuriant darbo užsakymą.  
- **Prevencinis darbo užsakymo tipas** apibrėžia darbo užsakymo tipą, naudojamą kuriant darbo užsakymus iš priežiūros planų. Jei šis laukas paliekamas tuščias, naudojamas lauke **Numatytasis darbo užsakymo tipas** esantis darbo užsakymo tipas.  
- Lauke **Susijęs darbo užsakymo šablonas** nurodomas maksimalus darbo užsakymų, kurie gali būti susieti su darbo užsakymu, skaičius. Pavyzdys: pavyzdys: ## leidžia naudoti iki 99 susietų darbo užsakymų. Jei apibrėžiate šabloną, kaip aprašyta čia, susiję darbo užsakymai bus sunumeruoti [darbo užsakymo, su kuriuo susietas darbo užsakymas, ID]-01, -02, -03 ir t. t. Jei šiame lauke neapibrėžiate šablono, susijęs darbo užsakymas gaus kitą nuoseklų darbo užsakymo ID.  
- Perjungimo mygtuke **Kopijuoti gedimus** pasirinkite Taip, jei norite automatiškai nukopijuoti klaidas, užregistruotas darbo užsakymuose, į susijusias priežiūros užklausas.  
- Lauke **Lygis** galite apibrėžti funkcinės vietos lygį, kuris automatiškai įterpiamas į darbo užsakymą, jei visos susijusios darbo užsakymo užduotys nurodo tą pačią funkcinę vieta. Jei darbo užsakymo užduotys ne visos susijusios su ta pačia funkcine vieta apibrėžtame lygyje, darbo užsakymo laukas **Funkcinė vieta** paliekamas tuščias. Pavyzdys: jei šiame lauke įterpiate skaičių „1“, jis nurodo aukščiausią funkcinės vietos struktūros lygį. Jei šiame lauke įterpiate skaičių „0“, vadinasi nesate apibrėžę konkretaus funkcinės vietos lygio, o tik tai, kad visos darbo užsakymo užduotys turi būti susietos su ta pačia funkcine vieta, kurioje ta funkcinė vieta turi būti pridėta prie darbo užsakymo.  
- Žurnalai, naudojami registruojant suvartojimą darbo užsakyme, gali būti pasirinkti FastTab **Bendra** laukuose **Valanda**, **Prekė** ir **Išlaidos**.  
- Lauke **Produkto kalbos šaltinis** pasirinkite, kuri kalba bus naudojama produktų pavadinimams turto valdymo ataskaitose. Galite pasirinkti įmonės paskyroje nustatytą kalbą arba šiuo metu nustatytą prisiregistravusio vartotojo kalbą.  
- Perjungimo mygtuke **Naujinimas realiuoju laiku** pasirinkite „Taip“, jeigu norite automatiškai naujinti užduoties tipo numatytųjų nustatymų keitimus, priežiūros planus ir priežiūros ciklus.
> - Jei pasirinksite „Ne“, užduoties tipo numatytųjų parametrų pakeitimai, priežiūros planai ir priežiūros ciklai nebus automatiškai atnaujinami turto valdyme  
> - Perjungimo mygtuke pasirinkite „Ne“, jei yra didelis sinchronizuojamų duomenų kiekis, pvz., nustatoma daug turto ar funkcinių vietų priežiūros planuose ar priežiūros cikluose, arba yra didelis priežiūros planų ar ciklų skaičius.  
> - Jei atliekate užduoties tipo numatytųjų parametrų ar priežiūros planų arba priežiūros ciklų keitimų ir naujinimui realiu laiku pasirinkote „Ne“, gali būti nerodomas įspėjimas, jeigu keitimai daro įtaką:
>   - funkcinėms vietoms, nustatytoms priežiūros planuose ir cikluose  
>   - objektams, nustatytiems priežiūros planuose ir cikluose  
>   - priežiūros planų nustatymui  
>   - priežiūros ciklų nustatymui  
- „FastTab“ **Kategorija** galima apibrėžti numatytąsias kategorijas, susijusias su vartojimu darbo užsakymuose.  


**Darbo užsakymo planavimo** saitas

- **Grafiko laiko ribos** apibrėžia laikotarpį dienomis, apskaičiuotą pagal numatomą darbo užsakymo pradžios datą, kai buvo suplanuotos darbo užsakymo užduotys.  
- **Bendrasis planas** susijęs su ištekliais modulyje **Organizacijos administravimas**. Jei šiame lauke pasirinksite bendrąjį planą, galėsite peržiūrėti pajėgumo rezervavimus, susijusius su darbo užsakymais **Pajėgumų užsakymuose** (**Organizacijos administravimas** > **Ištekliai** > **Ištekliai** > pasirinkite išteklių > skirtukas **Išteklių** > mygtukas **Pajėgumų rezervavimai**). Jei šį lauką paliksite tuščią, galėsite peržiūrėti pajėgumą, susijusį su darbo užsakymais **Pajėgumų užsakymai** (**Organizacijos administravimas** \>**Ištekliai** \>**Ištekliai** \> pasirinkite išteklių \> skirtukas **Išteklių** mygtukas \> **Pajėgumas**).  

>[!NOTE]
>Pasirinkimas, susijęs su bendrojo plano naudojimu modulyje **Turto valdymas** ir susijusi forma, naudojama siekiant gauti pajėgumų rezervavimo arba pajėgumo apžvalgą, yra standartinėje sąrankoje. Atsižvelgiant į sąranką lauke **Pagrindinis planas**, galėsite pasiekti pajėgumo informaciją modulio **Organizacijos administravimas** dalyje **Pajėgumų rezervavimas** arba **Pajėgumas**. Negalima sukurti sąrankos, kurioje pajėgumų rezervavimai būtų rodomi abiejuose rodiniuose.  

Toliau pateiktame ženklelių sąraše aprašyti visis laukai, susiję su vertinimo rezultatais, kurie naudojami apskaičiuoti darbo užsakymo prioritetą planuojant darbo užsakymą.

- **Prioritetas** – vertinimo balas, apskaičiuotas kartu su vertinimo rezultatu laukuose **Kritiškumas** ir **Pradžios data**. Skaičius šiame lauke yra padalintas iš skaičiaus, esančio darbo užsakymo lauke **Prioritetas**. Pavyzdys: jei šiame lauke įterpiama reikšmė „5,00“, o darbo užsakymo prioritetas yra „20“, prioriteto vertinimo balas yra 0,25.  
- **Kritiškumas** – vertinimo balas, apskaičiuotas kartu su vertinimo rezultatu laukuose **Prioritetas** ir **Pradžios data**. Skaičius šiame lauke yra dauginamas iš skaičiaus, esančio darbo užsakymo lauke **Kritiškumas**. Pavyzdys: jei šiame lauke įterpiama reikšmė „10,00“, o darbo užsakymo kritiškumas yra „5“, kritiškumo vertinimo balas yra 50.  
- **Pradžios data** – vertinimo balas, apskaičiuotas kartu su vertinimo rezultatu laukuose **Prioritetas** ir **Kritiškumas**. Šis laukas rodo dienos balą kaip neigiamą reikšmę ir yra lyginamas su arbo užsakymo lauku **Numatoma pradžia**. Pavyzdys: jei šiame lauke įterpiama reikšmė „10,00“, o numatoma darbo užsakymo pradžios data yra trys dienos nuo dabar, įvertinimo rezultatas yra minus 30,00. Pridėjus 0,25 ir 50 iš pavyzdžių laukuose **Prioritetas** ir **Kritiškumas**, gaunama bendra reikšmė plius 20,25. Šis skaičius lyginamas su visais kitais darbo užsakymo įvertinimo balais darbo užsakymų tvarkaraščiuose, o tada pirmiausia planuojami aukščiausią įvertinimą gavę elementai.  
- **Atsakingas darbuotojas** – vertinimo balas, apskaičiuojamas kartu su įvertinimo balo reikšmėmis **Atsakingų darbuotojų grupė**, **Pageidaujamas darbuotojas**, **Pageidaujama darbuotojų grupė**, **Turto vieta** ir **Pradžios data**. Jei šiame lauke įterpiama reikšmė „50,00“ ir darbo užsakyme pasirinktas atsakingas darbuotojas, darbo užsakymo planavimo metu darbuotojas gauna 50 taškų atliekant bendrąjį darbuotojo skaičiavimą.  
- **Atsakingų darbuotojų grupė** – vertinimo balas, apskaičiuojamas kartu su įvertinimo balo reikšmėmis **Atsakingų darbuotojų grupė**, **Pageidaujamas darbuotojas**, **Pageidaujama darbuotojų grupė**, **Turto vieta** ir **Pradžios data**. Jei šiame lauke įterpiama reikšmė „50,00“ ir darbo užsakyme pasirinktas atsakingas darbuotojas, darbo užsakymo planavimo metu darbuotojas gauna 50 taškų atliekant bendrąjį darbuotojo skaičiavimą.  
- **Apriboti iki atsakingų** – Taip/Ne perjungimo mygtukas riboja darbo užsakymų tvarkaraščiams prieinamų darbuotojų skaičių. Pasirinkite „Ne“, jei norite apskaičiuoti visų darbuotojų įvertinimą, neatsižvelgiant į tai, kad jie nustatyti kaip atsakingi darbuotojai ar atsakingų darbuotojų grupės dalis. Pasirinkite „Taip“, jei norite apskaičiuoti įvertinimą darbuotojų, kurie darbo užsakyme nustatyti kaip atsakingi darbuotojai ir (arba) įtraukti į darbo užsakyme pasirinktą atsakingų darbuotojų grupę.  
- **Pageidaujamas darbuotojas** – vertinimo balas, apskaičiuojamas kartu su įvertinimo balo reikšmėmis **Atsakingų darbuotojų grupė**, **Pageidaujamas darbuotojas**, **Pageidaujama darbuotojų grupė**, **Turto vieta** ir **Pradžios data**. Keturi įvertinimo balai apskaičiuojami ir sudedami, kad būtų pateiktas rezultatas, naudojamas pasirenkant, kuris darbuotojas turėtų būti priskirtas darbo užsakymui darbo užsakymo planavimo metu. Jei šiame lauke įterpiama reikšmė „10,00“ ir darbo užsakyme pasirinktas kaip pageidaujamas darbuotojas, darbo užsakymo planavimo metu tas darbuotojas gauna 10 taškų atliekant bendrąjį darbuotojo skaičiavimą.  
- **Pageidaujamų darbuotojų grupė** – vertinimo balas, apskaičiuojamas kartu su įvertinimo balo reikšmėmis **Atsakingų darbuotojų grupė**, **Pageidaujamas darbuotojas**, **Pageidaujama darbuotojų grupė**, **Turto vieta** ir **Pradžios data**. Jei šiame lauke įterpiama reikšmė „10,00“ ir darbuotojas darbo užsakyme priskirtas pageidaujamų darbuotojų grupei, darbo užsakymo planavimo metu tas darbuotojas gauna 10 taškų atliekant bendrąjį darbuotojo skaičiavimą.  
- **Apriboti iki pageidaujamų** – Taip/Ne perjungimo mygtukas riboja darbo užsakymų tvarkaraščiams prieinamų darbuotojų skaičių. Pasirinkite „Ne“, jei norite apskaičiuoti visų darbuotojų įvertinimą, neatsižvelgiant į tai, kad jie nustatyti kaip pageidaujami darbuotojai ar pageidaujamų darbuotojų grupės dalis. Pasirinkite „Taip“, jei norite apskaičiuoti įvertinimą tik darbuotojų, kurie yra nustatyti kaip pageidaujami darbuotojai ir (arba) įtraukti į pageidaujamų darbuotojų grupę.  
- **Vieta** – vertinimo balas, apskaičiuojamas kartu su įvertinimo balo reikšmėmis **Atsakingų darbuotojų grupė**, **Pageidaujamas darbuotojas**, **Pageidaujama darbuotojų grupė**, **Turto vieta** ir **Pradžios data**. Jei šiame lauke įterpiama reikšmė „3 000,00“, skaičiuojant darbuotojas gauna 3 000 taškų, jei darbuotojas yra toje pačioje gamykloje ar objekte kaip ir turtas, kuriam planuojama užduotis.  

  - Jei įmonė naudoja funkcines vietas, darbuotojai gauna visą balą, jei jie yra funkcinėje vietoje, susijusioje su turtu. Jei turto funkcinė vieta turi pirminį turtą, toje funkcinėje vietoje esantys darbuotojai gauna 1/2 balo. Jei ta vieta taip pat turi pirminę vietą, tos vietos darbuotojai gauna 1/3 balo. Jei ta vieta taip pat turi pirminę vietą, tos vietos darbuotojai gauna 1/4 balo ir t. t.  
  - Jei įmonė naudoja turto buvimo vietą, ko mes nerekomenduojame, skaičiuojant vietos vertinimą naudojama vieta, sritis ir zona. Darbuotojai gauna visą balą, jei jie yra su turtu susietoje vietoje, srityje ir zonoje. Jei darbuotojo vieta sutampa tik su vieta ir sritimi, darbuotojo įvertinimo balas yra 2/3 nuo viso balo. Jei darbuotojo vieta sutampa tik su vieta, darbuotojo įvertinimo balas yra 1/3 nuo viso balo.  

- **Apriboti iki vietos** – Taip/Ne perjungimo mygtukas riboja darbo užsakymų tvarkaraščiams prieinamų darbuotojų skaičių. Pasirinkite „Ne“, jei norite apskaičiuoti balą visiems darbuotojams visose funkcinėse vietose. Pasirinkite „Taip“, jei norite apskaičiuoti tik su darbo užsakymo funkcine vieta susietų darbuotojų balą.

>[!NOTE]
>Pateikti trys perjungimo mygtukai „Apriboti iki...“, skirti paspartinti darbo užsakymo planavimą apribojant darbuotojams skaičiuojamų vertinimų skaičių.

**Darbuotojo pradžios data** – vertinimo balas, apskaičiuojamas kartu su įvertinimo balo reikšmėmis **Atsakingų darbuotojų grupė**, **Pageidaujamas darbuotojas**, **Pageidaujama darbuotojų grupė**, **Turto vieta** ir **Pradžios data**. Šis laukas rodo dienos balą kaip neigiamą reikšmę ir yra lyginamas su arbo užsakymo lauku **Numatoma pradžia**. Jei šiame lauke įterpiama reikšmė „10,00“, o numatoma darbo užsakymo pradžios data yra rytoj, įvertinimo rezultatas yra minus 10,00.

  - Darant prielaidą, kad joks atsakingas darbuotojas ir atsakinga darbuotojų grupė nebuvo parinkti planuojamam darbo užsakymui – sudėjus ir atėmus vertinimo rezultatų reikšmes pavyzdžio laukuose **Pageidaujamas darbuotojas**, **Pageidaujamų darbuotojų grupė**, **Turto vieta** ir **Pradžios data**, gaunate bendrą 3 010,00 įvertinimą. Tai reiškia aukštą balą darbuotojui, kuris jau pasirinktas kaip pageidaujamas darbuotojas ir įtrauktas į pageidaujamų darbuotojų grupė darbo užsakymą, darbuotojas taip pat yra toje pačioje vietoje, kaip turtas, kuriam būtina planuoti užduotį. Visa tai reiškia, kad yra didelė tikimybė, jog atitinkamas darbuotojas bus pasirinktas atlikti darbą planuojant darbo užsakymą.  
  - Jei į vieną iš aštuonių anksčiau nurodytų laukų įterpiama reikšmė „0,00“, rezultato balas nebus naudojamas atliekant darbo užsakymo planavimą.  


**Dokumentų tipų** saitas

Pasirinkite dokumentų tipus, kurie turėtų būti pasiekiami kaip spausdinimo priedai, susiję su darbo užsakymo ataskaita. Tai atliekama spustelėjus dokumento tipą dalyje **Pasiekiama** ir spustelėjus mygtuką ![rodyklė pirmyn](media/15-setup-for-objects.png). Jei norite pašalinti pasirinktą dokumento tipą, pasirinkite dokumento tipą dalyje **Pasirinkta**, tada spustelėkite mygtuką ![rodyklė atgal](media/16-setup-for-objects.png).



**Numeravimo sekų** saitas

Šioje dalyje pasirinkite reikiamas numeravimo sekas. Turtui taikomos dvi numeravimo sekos: viena skirta neautomatiniu būdu sukurtam turtui, o kita – turtui, sukurtam laukiant turto.
