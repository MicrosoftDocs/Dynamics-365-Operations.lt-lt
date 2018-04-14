---
title: "Mažmeninės prekybos išrašai"
description: "Šioje temoje aprašoma, kaip kuriami ir registruojami išrašai."
author: ashishmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: ddceadb797af98f85670df72a335b2714fe2f01e
ms.contentlocale: lt-lt
ms.lasthandoff: 03/08/2018

---

# <a name="retail-statements"></a>Mažmeninės prekybos išrašai

[!INCLUDE [banner](includes/banner.md)]

„Microsoft Dynamics 365 for Retail“ išrašo registravimo procesas naudojamas kaip operacijos, vykdomos „Cloud point of sale“ (POS) arba „Modern POS“ (MPOS). Išrašo registravimo procesas naudoja paskirstymo grafiką, kad EKA operacijų rinkinį perkeltų į būstinės (HQ) klientą. Puslapiuose **Mažmeninės prekybos parametrai** ir **Parduotuvės** nurodyti parametrai naudojami norint pasirinkti operacijas, įtraukiamas į atskiras išrašus.  

Išrašų registravimo procesas parodytas toliau pateiktame paveikslėlyje. Šiame procese operacijos, įrašytos EKA, perduodamos į klientą naudojant duomenų apsikeitimo valdymą. Kai klientas gauna operacijas, galite kurti, skaičiuoti ir registruoti parduotuvės operacijos išrašą. 

[![Išrašų registravimo procesas](./media/retail-statements.png)](./media/retail-statements.png)

## <a name="creating-and-posting-statements"></a>Išrašų kūrimas ir registravimas
Galite kurti išrašą neautomatiniu būdu arba naudodami paketinius vykdymus, jūsų nustatytus reguliariai veikti visą dieną. Abiem atvejais išrašai kuriami ir registruojami atliekant toliau nurodytus veiksmus.

###  <a name="create-the-statement"></a>Išrašo kūrimas
Šiame veiksme identifikuojama parduotuvė, kuriai neautomatiniu būdu kuriamas išrašas. Jei konfigūruojate paketinį vykdymą, galite automatiškai kurti išrašus visoms parduotuvėms pagal jūsų nustatytą grafiką. 

### <a name="calculate-the-statement"></a>Išrašo skaičiavimas
Šiame veiksme pasirenkamos operacijos eilutės pagal kriterijus, apibrėžtus ir kiekvienai parduotuvei priskirtus puslapiuose **Mažmeninės prekybos parametrai** ir **Parduotuvės**. Šiuose puslapiuose galima apibrėžti kriterijus ir nurodyti, kaip skaičiuojamos operacijos. Jei norite peržiūrėti į išrašą įtrauktų operacijų sąrašą prieš skaičiuodami išrašą, naudokite puslapį **Operacijos**. 

Išrašo skaičiavime kaip apskaičiuota suma naudojamos mokėjimo priemonių deklaracijos iš registrų. Arba galite įvesti apskaičiuotą sumą neautomatiniu būdu. Išraše nurodomas skirtumas tarp operacijų pardavimo sumos ir faktinės apskaičiuotos sumos visuose mokėjimo būduose. Išrašas registruojamas tik jei šis skirtumas yra mažesnis nei maksimalus registravimo skirtumas, nustatytas parduotuvei. 

> [!NOTE]
> Išrašo skaičiavimo procese naudojama bendroji numeracija.

Kai skaičiuojate išrašą, skaičiavimas apima šias užduotis:

- Pažymėkite operacijas, kurios nebuvo įtrauktos į ankstesnio išrašo skaičiavimą, ir priskirkite pasirinktam datų intervalui. 
- Apskaičiuokite visas sumas, kurios buvo sumokėtos pasirinktose operacijose. Rezultatai rodomi išrašo eilutėse priklausomai nuo išrašo metodo.

  - Jei išrašo metodas yra **Iš viso**, eilutė sukuriama kiekvienam mokėjimo būdui pasirinktose operacijose. 
  - Jei išrašo metodas yra **Personalas**, eilutė sukuriama kiekvienam mokėjimo būdui operacijose, kurias atliko pasirinktas personalo narys. 
  - Jei išrašo metodas yra **EKA terminalas**, eilutė sukuriama kiekvienam mokėjimo būdui operacijose, kurios buvo atliktos pasirinktame registre. 
  - Jei išrašo metodas yra **Pamaina**, eilutė sukuriama kiekvienam mokėjimo būdui operacijose, kurios buvo atliktos pamainos metu.

Jei puslapyje **Parduotuvės** pažymėtas žymės langelis **Skaidyti pagal išrašo metodą**, sukuriamas atskiras išrašas pagal reikšmę, pasirinktą lauke **Išrašo metodas**.

Jei jūsų parduotuvės darbo valandos tęsiasi ir po vidurnakčio, galite sukonfigūruoti išrašų registravimą pagal darbo dienos pabaigą, o ne pagal kalendorinės dienos pabaigą. 

Puslapio **Parduotuvės** „FastTab“ **Išrašas / uždarymas** lauke **Darbo dienos pabaiga** įveskite laiką, kurį turi būti registruojama paskutinė operacija, kad ji būtų įtraukta į darbo dienos išrašą. Pažymėkite žymės langelį **Registruoti kaip darbo dieną**, jei norite registruoti operacijas tą pačią darbo dieną. Užregistravus išrašą, operacijos, įrašytos tą pačią darbo dieną, gali būti įtrauktos į tą patį pardavimo užsakymą, net jei kai kurios operacijos vykdomos prieš vidurnaktį, o kitos operacijos – po vidurnakčio. 

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a>Pavyzdys: darbo dienos, trunkančios dvi kalendorines dienas, išrašo registravimas 

Parduotuvė dirba nuo 8:00 val. iki 3:00 val., o parduotuvės konfigūracijoje pažymėtas žymės langelis **Registruoti kaip darbo dieną**. Parduotuvė registruoja operacijas nuo gegužės 31 d. 8:00 val. iki vidurnakčio. Be to, parduotuvė registruoja operacijas nuo birželio 1 d. 12:01 val. iki 3:00 val. 

Kai parduotuvė registruoja savo išrašą baigdama darbo dieną, generuojamas pardavimo užsakymas apima visas operacijas, įrašytas darbo valandomis nuo 8:00 val. iki 3:00 val., net jei operacijos įvyko dvi skirtingas dienas, gegužės 31 d. ir birželio 1 d. 

Jei ta pati parduotuvė konfigūruojama nepažymėjus žymės langelio **Registruoti kaip darbo dieną**, kai parduotuvė registruoja savo darbo dienos išrašą, generuojami atskiri pardavimo užsakymai. Vienas pardavimo užsakymas apima operacijas, įrašytas gegužės 31 d. darbo valandomis nuo 8:00 val. iki vidurnakčio, o antras – operacijas, įrašytas birželio 1 d. darbo valandomis nuo 12:01 val. iki 3:00 val.
 
> [!NOTE]
> Prieš kurdami išrašus turite uždaryti pamainas išrašo laikotarpiu. 

### <a name="post-the-statement"></a>Išrašo registravimas
Kai registruojate išrašą, išraše sukuriami mažmeninės prekybos pardavimo užsakymai ir sąskaitos faktūros.

- Atsiskaitymo grynaisiais operacijos kaupiamos viename pardavimo užsakyme, o sąskaita faktūra išrašoma numatytajam klientui, kuris yra priskirtas parduotuvei. 
- Mažmeninė prekyba, kurios klientas buvo įtrauktas į „Microsoft Dynamics 365 for Retail POS“ operaciją, generuoja atskirus pardavimo užsakymus ir sąskaitas faktūras, po vieną kiekvienam unikaliam klientui. 

Išrašo mokėjimams automatiškai sukuriami mokėjimų žurnalai, o EKA parduotuvėje atnaujinamos atsargos.

