---
title: Priežiūros ciklai
description: Šioje temoje aprašomi priežiūros ciklai skiltyje Turto valdymas.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRoundTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: af0461588971342b62104fce9b5bfa25e329d7c9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252995"
---
# <a name="maintenance-rounds"></a>Priežiūros ciklai

[!include [banner](../../includes/banner.md)]

 

Skiltyje **Turto valdymas** galite sukurti priežiūros ciklus įvairiam turtui, kuriam būtina atlikti panašias užduotis reguliariais intervalais. Pavyzdžiui, sutepimo darbai arba saugos tikrinimo darbai, kurie turi būti atliekami keletui mašinų tais pačiais intervalais. Pirmas žingsnis – sukurti priežiūros ciklą, apimantį turtą, kuriam reikalinga tokia pati priežiūros užduoties forma. Kitame žingsnyje planuokite priežiūros ciklus. Kai įvykdysite priežiūros ciklų grafiką, galėsite matyti visus užduoties įrašus, susijusius su ciklu, skiltyse **Visi priežiūros grafikai** ir **Atidaryti priežiūros grafiko eilutes**.

>[!NOTE]
>Priežiūros ciklai taip pat gali būti nustatyti funkcinėms vietoms, kuriose priežiūra atliekama funkcinėje vietoje įdiegtam turtui, kai sukuriamas pasikartojantis darbo užsakymas. Daugiau informacijos apie priežiūros ciklų arba funkcinių vietų sąranką žr. [Kurti funkcines vietas](../functional-locations/create-functional-locations.md).

## <a name="set-up-a-maintenance-round"></a>Kaip nustatyti priežiūros ciklą

1. Spustelėkite **Turto valdymas** > **Sąranka** > **Prevencinė priežiūra** > **Priežiūros ciklai**.

2. Spustelėkite **Naujas**, kad sukurtumėte naują priežiūros ciklą.

3. Įterpkite ID lauke **Priežiūros ciklas** ir priežiūros ciklo pavadinimą lauke **Pavadinimas**.

4. Lauke **Pradžios data** pažymėkite ciklo pradžios datą.

5. Laukuose **Baigti per dienas** ir **Baigti per valandas** galite įterpti numatomą pabaigos datą dienomis arba valandomis. Numatoma pabaigos data apskaičiuojama atitinkamai kaip ir pradžios data, kuri apskaičiuojama kuriant priežiūros grafiko eilutes. Pavyzdžiui, galite įterpti „7“ į lauką **Baigti per dienas**, kad nurodytumėte, jog susijęs darbas turi būti atliktas per savaitę nuo pradžios datos.

6. Pasirinkite Taip perjungiklyje **Sukurti automatiškai**, jei darbo užsakymai, kurie kuriami iš priežiūros ciklo, turi būti sukurti automatiškai iš priežiūros grafiko eilučių.

7. Lauke **Darbo užsakymo tipas** pasirinkite darbo užsakymo tipą, naudotiną darbo užsakymams, sukurtiems iš priežiūros ciklo.

8. Lauke **Aptarnavimo lygis** pasirinkite darbo užsakymo aptarnavimo lygį, naudotiną darbo užsakymams, sukurtiems iš priežiūros ciklo.

9. „FastTab“ **Turto eilutės** spustelėkite **Įtraukti**, kad įtrauktumėte turtą į priežiūros ciklą.

10. Eilutės numeris automatiškai įterpiamas į lauką **Eilutės numeris**, nurodant turto eilės tvarką priežiūros cikle.

11. Pasirinkite turtą lauke **Turtas**.

12. Pasirinkite priežiūros užduoties tipą turtui lauke **Priežiūros užduoties tipas**.

13. Jei reikia, pasirinkite **Priežiūros užduoties tipo variantas** ir **Prekybos šaka**, susijusius su priežiūros užduoties tipu.

14. Pažymėkite pasikartojimą (diena, savaitė ir t. t.) lauke **Laikotarpio tipas**.

15. Lauke **Laikotarpio dažnumas** įveskite priežiūros ciklo pasikartojimų skaičių. Pavyzdžiui: jei lauke **Laikotarpio tipas** pasirinkote „Diena“ ir įvedėte į lauką skaičių „7“, naujos priežiūros ciklo eilutės sukuriamos kartą per savaitę kuriant prevencinės priežiūros grafikus.

16. Pasirinkite pradžios datą įtrauktinam į priežiūros ciklą turtui lauke **Pradžios data**. Ši data gali skirtis nuo pradžios datos, nurodytos priežiūros cikle.

17. Pakartokite 9–16 veiksmus norėdami į priežiūros ciklą įtraukti daugiau turto.

18. „FastTab“ **Funkcinės vietos eilutės** pasirinkite **Įtraukti**, kad įtrauktumėte funkcinę vietą į priežiūros ciklą. Žr. ankstesnį susijusių laukų aprašą. Tie patys laukai yra pasiekiami kuriant turto eilutę, tačiau, jei reikia, taip pat galite funkcinei vietai parinkti **Gamintojas** ir **Modelis** reikšmes. Jei pasirinksite tik funkcinę vietą eilutėje, bet nustatysite reikšmes **Turto tipas**, **Gamintojas**, **Modelis**, **Priežiūros darbo tipą**, **Priežiūros darbo tipo variantas** ir **Prekybos šaka**, visas, susijęs su funkcine vieta, turtas bus įtrauktas į priežiūros ciklą kuriant priežiūros grafiką.

19. „FastTab“ **Telkiniai** spustelėkite **Įtraukti**, kad įtrauktumėte darbo užsakymo telkinį, įtrauktiną į priežiūros ciklą. Keletas darbo užsakymų telkinių gali būti prijungti prie priežiūros ciklo.

20. Įrašykite sąranką.

>[!NOTE]
>Laukai **Turtas** ir **Eilutės** yra grupėje **Išsami informacija**, kuri yra „FastTab“ **Antraštė**, ir nurodo bendrą turto ir eilučių, susijusių su pasirinktu priežiūros ciklu, skaičių.

Toliau pateiktame paveikslėlyje parodytas priežiūros ciklo, kuriame yra trys turto vienetai, pavyzdys.

![1 pav.](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a>Planuoti priežiūros ciklus

Nustatę priežiūros ciklą, vykdykite grafiko užduotį, kuria planuojamos visos užduotys, susijusios su priežiūros ciklu.

1. Spustelėkite mygtukus **Turto valdymas** > **Periodiškai** > **Prevencinė priežiūra** > **Planuoti priežiūros ciklus** arba **Turto valdymas** > **Bendrieji dalykai** > **Priežiūros grafikas** > **Visi priežiūros grafikai**, arba **Atidaryti priežiūros grafiko eilutes**, arba **Atidaryti priežiūros grafiko telkinius** > pasirinkite sąraše priežiūros grafiko eilutę > **Priežiūros ciklai**.

2. Lauke **Laikotarpis** pasirinkite laikotarpio tipą, naudotiną planuojamai užduočiai.

3. Lauke **Laikotarpio dažnumas** įveskite laikotarpių, kuriuos norite įtraukti, skaičių. Grafiko pradžia atitinka dabartinę datą.

4. Pasirinkite Taip perjungiklyje **Sukurti automatiškai**, jei darbo užsakymas turi būti sukurtas automatiškai priežiūros ciklo pagrindu.

>[!NOTE]
>Jei šiame perjungiklyje nustatyta Taip ir perjungiklyje **Kurti automatiškai** taip pat nustatyta Taip priežiūros ciklui formoje **Priežiūros ciklai**, darbo užsakymai kuriami pagal priežiūros ciklo eilutes, o priežiūros grafiko eilutės kuriamos, turinčios būseną „Darbo užsakymas sukurtas“. Jei tik vienas iš perjungiklių **Kurti automatiškai** nustatytas į Taip, išplečiamajame sąraše arba skiltyje **Priežiūros ciklai**, bus sukuriamos vien būseną Sukurta turinčios priežiūros grafiko eilutės. Tokiu atveju nesukuriama jokių darbo užsakymų.

5. Jei reikia, grafiko užduočiai galite pasirinkti konkrečius ciklus arba kitą pradžios datą. Spustelėkite **Filtruoti** ir pridėkite reikiamų ciklų.

6. Spustelėkite **Gerai**.

7. Dabar galite matyti priežiūros ciklų užduotis, pasirinkus **Turto valdymas** > **Bendrieji dalykai** > **Priežiūros grafikas** > **Visi priežiūros grafikai** arba **Atidaryti priežiūros grafiko eilutes**. Jei suplanuoti ciklai susieti su darbo užsakymų telkiniu, taip pat galite matyti priežiūros grafiko eilutes, pasirinkus **Atidaryti priežiūros grafikų telkinius**. Sukurtos iš ciklo priežiūros grafiko eilutės turi pirminės reikšmės tipą „Priežiūros ciklai“.

Toliau esančiuose dviejuose paveikslėliuose pavaizduota grafiko užduotis dialogo lange **Planuoti priežiūros ciklus** ir priežiūros grafiko eilutes, sukurtos naudojant **Visas priežiūros tvarkaraščius** pagal grafiko užduotį.

![2 pav.](media/14-preventive-maintenance.png)

![3 pav.](media/15-preventive-maintenance.png)

- Kai neautomatiniu būdu sukuriami darbo užsakymai turtui, kuriam taikoma tiekėjo garantija, rodomas dialogo langas, kad vartotojas žinotų apie garantiją. Darbo užsakymo kūrimas vėliau gali būti atšauktas. Garantinis čekis neįtraukiamas automatiškai sukurtuose darbo užsakymuose.  
- Galite nustatyti paketinę užduotį, esančią „FastTab“ **Vykdyti fone**, kad grafiko ciklai būtų vykdomi reguliariais intervalais.  
- Jei ciklas yra įtrauktas į kelis darbo užsakymų telkinius (žr. [Darbo užsakymų telkiniai](../work-orders/work-order-pools.md)), kiekviename įrašo telkinyje pasirinkus **Atidaryti priežiūros grafiko telkinius** rodomas vienas įrašas. Taip siekiama optimizuoti darbo užsakymų telkinių filtravimo parinktis.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]