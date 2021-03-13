---
title: Turto valdymo parametrai
description: Turto valdymo srityje būtina nustatyti bendruosius parametrus, susijusius su turtu, darbo užsakymais ir darbo užsakymų planavimu.
author: josaw1
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e4b76ba90ab03cd35e72eff8acc89f780659fa5
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020659"
---
# <a name="asset-management-parameters"></a>Turto valdymo parametrai

[!include [banner](../../includes/banner.md)]

Turto valdymo srityje būtina nustatyti bendruosius parametrus, susijusius su turtu, darbo užsakymais ir darbo užsakymų planavimu. Šioje temoje aiškinama, kaip juos nustatyti. Pasirinkite **Turto valdymas** > **Sąranka** > **Turto valdymo parametrai**, kad atidarytumėte puslapį.

> [!NOTE]
> Jei norite nustatyti sistemą, kuri apima demonstracinius turto valdymo funkcijų tikrinimo duomenis, žr. [Demonstracinės aplinkos diegimas](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).

## <a name="the-assets-tab"></a>Skirtukas Turtas

Skirtuke **Turtas** pateikiami šie parametrai:

- **Numatytoji funkcinė vieta** yra standartinė funkcinė vieta, kuri kuriant naują turtą automatiškai pasirenkama turtui.  
- Lauke **Standartinis kalendorius** pasirinkite kalendorių, kuris bus naudojamas skaičiuojant turto KPI, jei turtui nepasirinktas joks išteklius.  
- Lauke **Rodinys** pasirinkite standartinį rodinį, rodomą, kai atidaromas **Turto rodinys**(**Turto valdymas** > **Bendra** > **Turtas** > **Turto rodinys**).
- **Numatytasis užklausos tipas** yra standartinis priežiūros užklausos tipas, kuris automatiškai pasirenkamas kuriant naują užklausą.  
- Užduočių tipų prognozės saugomos projekte, pasirinktame lauke **Prognozės projektas**. Kiekvienam užduoties tipui prognozės projekte automatiškai sukuriama nauja veikla. Užduoties tipo prognozės išsaugomos prognozės projekte.  
- Lauke **Modelis** pasirinkite prognozės modelį, naudojamą užduoties tipui ir darbo užsakymo prognozėms.

## <a name="the-work-orders-tab"></a>Skirtukas Darbo užsakymai

Skirtuke **Darbo užsakymai** pateikiami šie parametrai:

- **Numatytasis darbo užsakymo tipas** apibrėžia standartinius parametrus kuriant darbo užsakymą.  
- **Prevencinis darbo užsakymo tipas** apibrėžia darbo užsakymo tipą, naudojamą kuriant darbo užsakymus iš priežiūros planų. Jei šis laukas paliekamas tuščias, naudojamas lauke **Numatytasis darbo užsakymo tipas** esantis darbo užsakymo tipas.  
- Lauke **Susijęs darbo užsakymo šablonas** nurodomas maksimalus darbo užsakymų, kurie gali būti susieti su darbo užsakymu, skaičius. Pavyzdžiui, ## leidžia naudoti iki 99 susietų darbo užsakymų. Jei apibrėžiate šabloną, kaip aprašyta čia, susiję darbo užsakymai bus sunumeruoti [darbo užsakymo, su kuriuo susietas darbo užsakymas, ID]-01, -02, -03 ir t. t. Jei šiame lauke neapibrėžiate šablono, susijęs darbo užsakymas gaus kitą nuoseklų darbo užsakymo ID.  
- Mygtuke **Kopijuoti gedimus** pasirinkite **Taip**, jei norite automatiškai nukopijuoti klaidas, užregistruotas darbo užsakymuose, į susijusias priežiūros užklausas. 
- Lauke **Lygis** galite apibrėžti funkcinės vietos lygį, kuris automatiškai įterpiamas į darbo užsakymą, jei visos susijusios darbo užsakymo užduotys nurodo tą pačią funkcinę vieta. Jei darbo užsakymo užduotys ne visos susijusios su ta pačia funkcine vieta apibrėžtame lygyje, darbo užsakymo laukas **Funkcinė vieta** paliekamas tuščias. Pavyzdžiui, jei šiame lauke įterpiate skaičių „1“, jis nurodo aukščiausią funkcinės vietos struktūros lygį. Jei šiame lauke įterpiate skaičių „0“, vadinasi nesate apibrėžę konkretaus funkcinės vietos lygio, o tik tai, kad visos darbo užsakymo užduotys turi būti susietos su ta pačia funkcine vieta, kurioje ta funkcinė vieta turi būti pridėta prie darbo užsakymo.  
- Žurnalai, naudojami registruojant suvartojimą darbo užsakyme, gali būti pasirinkti FastTab **Bendra** laukuose **Valanda**, **Prekė** ir **Išlaidos**.  
- Lauke **Produkto kalbos šaltinis** pasirinkite, kuri kalba bus naudojama produktų pavadinimams turto valdymo ataskaitose. Galite pasirinkti įmonės paskyroje nustatytą kalbą arba šiuo metu nustatytą prisiregistravusio vartotojo kalbą.  
- Mygtuke **Naujinimas realiuoju laiku** pasirinkite **Taip**, jeigu norite automatiškai naujinti užduoties tipo numatytųjų parametrų keitimus, priežiūros planus ir priežiūros ciklus.
  - Jei pasirinksite **Ne**, užduoties tipo numatytųjų parametrų keitimai, priežiūros planai ir priežiūros ciklai nebus automatiškai atnaujinami turto valdyme.
  - Mygtuke pasirinkite **Ne**, jei yra didelis sinchronizuojamų duomenų kiekis, pvz., nustatoma daug turto ar funkcinių vietų priežiūros planuose ar priežiūros cikluose, arba yra didelis priežiūros planų ar ciklų skaičius.  
  - Jei atliekate užduoties tipo numatytųjų parametrų ar priežiūros planų arba priežiūros ciklų keitimų ir naujinimui realiu laiku pasirinkote **Ne**, gali būti nerodomas įspėjimas, jeigu keitimai daro įtaką:
    - funkcinėms vietoms, nustatytoms priežiūros planuose ir cikluose  
    - objektams, nustatytiems priežiūros planuose ir cikluose  
    - priežiūros planų nustatymui  
    - priežiūros ciklų nustatymui  
- „FastTab“ **Kategorija** galima apibrėžti numatytąsias kategorijas, susijusias su vartojimu darbo užsakymuose.  

## <a name="the-work-order-scheduling-tab"></a>Skirtukas Darbo užsakymo planavimas

Skirtuke **Darbo užsakymo planavimas** pateikiami šie parametrai **Bendra** „FastTab”:

- **Grafiko laiko ribos** apibrėžia laikotarpį dienomis, apskaičiuotą pagal numatomą darbo užsakymo pradžios datą, kai buvo suplanuotos darbo užsakymo užduotys.  
- **Bendrasis planas** susijęs su ištekliais modulyje **Organizacijos administravimas**. Jei šiame lauke pasirinksite bendrąjį planą, galėsite peržiūrėti pajėgumo rezervavimus, susijusius su darbo užsakymais **Pajėgumų užsakymuose** (**Organizacijos administravimas** > **Ištekliai** > **Ištekliai** > pasirinkite išteklių > skirtukas **Išteklių** > mygtukas **Pajėgumų rezervavimai**). Jei šį lauką paliksite tuščią, galėsite peržiūrėti pajėgumą, susijusį su darbo užsakymais **Pajėgumų užsakymai** (**Organizacijos administravimas** \>**Ištekliai** \>**Ištekliai** \> pasirinkite išteklių \> skirtukas **Išteklių** mygtukas \> **Pajėgumas**).  

>[!NOTE]
>Pasirinkimas, susijęs su bendrojo plano naudojimu modulyje **Turto valdymas** ir susijusi forma, naudojama siekiant gauti pajėgumų rezervavimo arba pajėgumo apžvalgą, yra standartinėje sąrankoje. Atsižvelgiant į sąranką lauke **Pagrindinis planas**, galėsite pasiekti pajėgumo informaciją modulio **Organizacijos administravimas** dalyje **Pajėgumų rezervavimas** arba **Pajėgumas**. Negalima sukurti sąrankos, kurioje pajėgumų rezervavimai būtų rodomi abiejuose rodiniuose.  

Toliau pateiktame sąraše aprašyti visis laukai, susiję su vertinimo rezultatais, kurie naudojami apskaičiuoti darbo užsakymo prioritetą planuojant darbo užsakymą.

- **Prioritetas** – vertinimo balas, apskaičiuotas kartu su vertinimo rezultatu laukuose **Kritiškumas** ir **Pradžios data**. Skaičius šiame lauke yra padalintas iš skaičiaus, esančio darbo užsakymo lauke **Prioritetas**. Pavyzdžiui, jei šiame lauke įterpiama reikšmė „5,00“, o darbo užsakymo prioritetas yra „20“, prioriteto vertinimo balas yra 0,25.  
- **Kritiškumas** – vertinimo balas, apskaičiuotas kartu su vertinimo rezultatu laukuose **Prioritetas** ir **Pradžios data**. Skaičius šiame lauke yra dauginamas iš skaičiaus, esančio darbo užsakymo lauke **Kritiškumas**. Pavyzdžiui, jei šiame lauke įterpiama reikšmė „10,00“, o darbo užsakymo kritiškumas yra „5“, kritiškumo vertinimo balas yra 50.  
- **Pradžios data** – vertinimo balas, apskaičiuotas kartu su vertinimo rezultatu laukuose **Prioritetas** ir **Kritiškumas**. Šis laukas rodo dienos balą kaip neigiamą reikšmę ir yra lyginamas su arbo užsakymo lauku **Numatoma pradžia**. Pavyzdžiui, jei šiame lauke įterpiama reikšmė „10,00“, o numatoma darbo užsakymo pradžios data yra trys dienos nuo dabar, įvertinimo rezultatas yra minus 30,00. Pridėjus 0,25 ir 50 iš pavyzdžių laukuose **Prioritetas** ir **Kritiškumas**, gaunama bendra reikšmė plius 20,25. Šis skaičius lyginamas su visais kitais darbo užsakymo įvertinimo balais darbo užsakymų tvarkaraščiuose, o tada pirmiausia planuojami aukščiausią įvertinimą gavę elementai.  
- **Atsakingas darbuotojas** – vertinimo balas, apskaičiuojamas kartu su įvertinimo balo reikšmėmis **Atsakingų darbuotojų grupė**, **Pageidaujamas darbuotojas**, **Pageidaujama darbuotojų grupė**, **Turto vieta** ir **Pradžios data**. Jei šiame lauke įterpiama reikšmė „50,00“ ir darbo užsakyme pasirinktas atsakingas darbuotojas, darbo užsakymo planavimo metu darbuotojas gauna 50 taškų atliekant bendrąjį darbuotojo skaičiavimą.  
- **Atsakingų darbuotojų grupė** – vertinimo balas, apskaičiuojamas kartu su įvertinimo balo reikšmėmis **Atsakingas darbuotojas**, **Pageidaujamas darbuotojas**, **Pageidaujama darbuotojų grupė**, **Turto vieta** ir **Pradžios data**. Jei šiame lauke įterpiama reikšmė „50,00“ ir darbo užsakyme pasirinktas atsakingas darbuotojas, darbo užsakymo planavimo metu darbuotojas gauna 50 taškų atliekant bendrąjį darbuotojo skaičiavimą.  
- **Apriboti iki atsakingų** – tai riboja darbo užsakymų planavimui prieinamų darbuotojų skaičių. Pasirinkite **Ne**, jei norite apskaičiuoti visų darbuotojų įvertinimą, neatsižvelgiant į tai, ar jie nustatyti kaip atsakingi darbuotojai ar atsakingų darbuotojų grupės dalis. Pasirinkite **Taip**, jei norite apskaičiuoti įvertinimą darbuotojų, kurie darbo užsakyme nustatyti kaip atsakingi darbuotojai ir (arba) įtraukti į darbo užsakyme pasirinktą atsakingų darbuotojų grupę.  
- **Pageidaujamas darbuotojas** – vertinimo balas, apskaičiuojamas kartu su įvertinimo balo reikšmėmis **Atsakingas darbuotojas**, **Pageidaujamas darbuotojas**, **Pageidaujama darbuotojų grupė**, **Turto vieta** ir **Pradžios data**. Keturi įvertinimo balai apskaičiuojami ir sudedami, kad būtų pateiktas rezultatas, naudojamas pasirenkant, kuris darbuotojas turėtų būti priskirtas darbo užsakymui darbo užsakymo planavimo metu. Jei šiame lauke įterpiama reikšmė „10,00“ ir darbo užsakyme pasirinktas kaip pageidaujamas darbuotojas, darbo užsakymo planavimo metu tas darbuotojas gauna 10 taškų atliekant bendrąjį darbuotojo skaičiavimą.  
- **Pageidaujamų darbuotojų grupė** – vertinimo balas, apskaičiuojamas kartu su įvertinimo balo reikšmėmis **Atsakingas darbuotojas**, **Pageidaujamas darbuotojas**, **Pageidaujama darbuotojų grupė**, **Turto vieta** ir **Pradžios data**. Jei šiame lauke įterpiama reikšmė „10,00“ ir darbuotojas darbo užsakyme priskirtas pageidaujamų darbuotojų grupei, darbo užsakymo planavimo metu tas darbuotojas gauna 10 taškų atliekant bendrąjį darbuotojo skaičiavimą.  
- **Apriboti iki pageidajamų** – tai riboja darbo užsakymų planavimui prieinamų darbuotojų skaičių. Pasirinkite **Ne**, jei norite apskaičiuoti visų darbuotojų įvertinimą, neatsižvelgiant į tai, ar jie nustatyti kaip pageidaujami darbuotojai ar pageidaujamų darbuotojų grupės dalis. Pasirinkite **Taip**, jei norite apskaičiuoti įvertinimą tik darbuotojų, kurie yra nustatyti kaip pageidaujami darbuotojai ir (arba) įtraukti į pageidaujamų darbuotojų grupę.  
- **Vieta** – vertinimo balas, apskaičiuojamas kartu su įvertinimo balo reikšmėmis **Atsakingas darbuotojas**, **Pageidaujamas darbuotojas**, **Pageidaujama darbuotojų grupė**, **Turto vieta** ir **Pradžios data**. Jei šiame lauke įterpiama reikšmė „3 000,00“, skaičiuojant darbuotojas gauna 3 000 taškų, jei darbuotojas yra toje pačioje gamykloje ar objekte kaip ir turtas, kuriam planuojama užduotis.  
  - Jei įmonė naudoja funkcines vietas, darbuotojai gauna visą balą, jei jie yra funkcinėje vietoje, susijusioje su turtu. Jei turto funkcinė vieta turi pirminį turtą, toje funkcinėje vietoje esantys darbuotojai gauna 1/2 balo. Jei ta vieta taip pat turi pirminę vietą, tos vietos darbuotojai gauna 1/3 balo. Jei ta vieta taip pat turi pirminę vietą, tos vietos darbuotojai gauna 1/4 balo ir t. t.  
  - Jei įmonė naudoja turto buvimo vietą, ko mes nerekomenduojame, skaičiuojant vietos vertinimą naudojama vieta, sritis ir zona. Darbuotojai gauna visą balą, jei jie yra su turtu susietoje vietoje, srityje ir zonoje. Jei darbuotojo vieta sutampa tik su vieta ir sritimi, darbuotojo įvertinimo balas yra 2/3 nuo viso balo. Jei darbuotojo vieta sutampa tik su vieta, darbuotojo įvertinimo balas yra 1/3 nuo viso balo.  
- **Apriboti iki vietos** – tai riboja darbo užsakymų planavimui prieinamų darbuotojų skaičių. Pasirinkite **Ne**, jei norite apskaičiuoti balą visiems darbuotojams visose funkcinėse vietose. Pasirinkite **Taip**, jei norite apskaičiuoti tik su darbo užsakymo funkcine vieta susietų darbuotojų balą.

>[!NOTE]
>Pateikti trys laukai „Apriboti iki...“, skirti paspartinti darbo užsakymo planavimą apribojant darbuotojams skaičiuojamų vertinimų skaičių.

**Darbuotojo pradžios data** – vertinimo balas, apskaičiuojamas kartu su įvertinimo balo reikšmėmis **Atsakingas darbuotojas**, **Pageidaujamas darbuotojas**, **Pageidaujama darbuotojų grupė**, **Turto vieta** ir **Pradžios data**. Šis laukas rodo dienos balą kaip neigiamą reikšmę ir yra lyginamas su arbo užsakymo lauku **Numatoma pradžia**. Jei šiame lauke įterpiama reikšmė „10,00“, o numatoma darbo užsakymo pradžios data yra rytoj, įvertinimo rezultatas yra minus 10,00.

  - Darant prielaidą, kad joks atsakingas darbuotojas ir atsakinga darbuotojų grupė nebuvo parinkti planuojamam darbo užsakymui – sudėjus ir atėmus vertinimo rezultatų reikšmes pavyzdžio laukuose **Pageidaujamas darbuotojas**, **Pageidaujamų darbuotojų grupė**, **Turto vieta** ir **Pradžios data**, gaunate bendrą 3 010,00 įvertinimą. Tai reiškia aukštą balą darbuotojui, kuris jau pasirinktas kaip pageidaujamas darbuotojas ir įtrauktas į pageidaujamų darbuotojų grupė darbo užsakymą, darbuotojas taip pat yra toje pačioje vietoje, kaip turtas, kuriam būtina planuoti užduotį. Tai reiškia, kad yra didelė tikimybė, jog atitinkamas darbuotojas bus pasirinktas atlikti darbą planuojant darbo užsakymą.  
  - Jei į vieną iš aštuonių anksčiau nurodytų laukų įterpiama reikšmė „0,00“, rezultato balas nebus naudojamas atliekant darbo užsakymo planavimą.  

## <a name="the-document-types-tab"></a>Skirtukas Dokumentų tipai

Pasirinkite dokumentų tipus, kurie turėtų būti pasiekiami kaip spausdinimo priedai, susiję su darbo užsakymo ataskaita. Tai atliekama pasirinkus dokumento tipą dalyje **Pasiekiama** ir pasirinkus ![rodyklę pirmyn](media/15-setup-for-objects.png). Jei norite pašalinti pasirinktą dokumento tipą, pasirinkite dokumento tipą dalyje **Pasirinkta**, tada pasirinkite ![rodyklę atgal](media/16-setup-for-objects.png).

## <a name="the-number-sequences-tab"></a>Skirtukas Numeravimas

Šioje dalyje pasirinkite reikiamas numeravimo sekas. Turtui taikomos dvi numeravimo sekos: viena skirta neautomatiniu būdu sukurtam turtui, o kita – turtui, sukurtam laukiant turto.
