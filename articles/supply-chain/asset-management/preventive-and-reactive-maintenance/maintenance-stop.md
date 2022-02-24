---
title: Prižiūrimo turto prastovos veiklos
description: Šioje temoje paaiškinama, kaip prižiūrimo turto prastova naudojama peržiūrėti, kiek reikia pajėgumų norint atlikti priežiūros užduotis, skirtas konkrečiam turtui, nustatytu laikotarpiu.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetMaintenanceStopCopy, EntAssetMaintenanceStopObject, EntAssetObjectProductionStop, EntAssetProductionStopType, EntAssetMaintenanceStop
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 986b2ae4cf7f7819caaf35e009fd4735f35e6928
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017963"
---
# <a name="maintenance-downtime-activities"></a>Prižiūrimo turto prastovos veiklos

[!include [banner](../../includes/banner.md)]

Prižiūrimo turto prastova naudojama peržiūrėti, kiek reikia pajėgumų norint atlikti priežiūros užduotis, skirtas konkrečiam turtui, nustatytu laikotarpiu. Pavyzdžiui, galite sukurti prižiūrimo turto prastovos registravimą 10 gamybos linijai gamybos ceche 29-A gamybos vietoje 02. Prižiūrimo turto prastovos registracija nurodo pradžią ir pabaigą laikotarpio, kada su priežiūros sustabdymu susijęs turtas nėra pasiekiamas gamybai.

**Prižiūrimo turto prastovos veiklos** – tai priežiūros grafiko eilučių ir darbo užsakymo priežiūros užduočių apžvalga, vykdoma susijusiam turtui nurodytu laikotarpiu. Visos eilutės, susijusios su darbo užsakymo priežiūros užduotimis, turi turėti numatomą pradžios datą priežiūros sustabdymo laikotarpiu. Galite gauti naudingos informacijos ir padaryti pakeitimus suplanuotoms priežiūros užduotims:

- Peržiūrėkite privalomuosius gamybos įrangos išjungimo laikotarpius (turtas).  
- Gaukite planuojamos priežiūros (valandomis), sugrupuotos pagal kompetencijas (atsakingų priežiūros darbo grupių arba priežiūros darbuotojų), apžvalgą, pavyzdžiui, elektrikų, kalvių ar kitų priežiūros darbo grupių, būtinų atlikti suplanuotas priežiūros užduotis, pajėgumus.  
- Koreguokite priežiūros grafiko eilutes arba darbo užsakymo priežiūros užduotis, susijusias su turtu, pvz., keiskite numatomus pradžios ir pabaigos laikus eilutėje, arba pasirinkite kitus priežiūros darbuotojus, kad optimizuotumėte priežiūros darbuotojų ir priežiūros darbo grupių darbo eigą.

Pasirinkus turtą prižiūrimo turto prastovos registracijoje, visos atidarytos priežiūros grafiko eilutės ir darbo užsakymo priežiūros užduotys, susijusios su aktyviais darbo užsakymais, įtraukiamos į prižiūrimo turto prastovos registravimą.

## <a name="maintenance-downtime-activities"></a>Prižiūrimo turto prastovos veiklos

Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Prižiūrimo turto prastovos veiklos** > **Visos prižiūrimo turto prastovos veiklos**, kad atidarytumėte prižiūrimo turto prastovos veiklų sąrašą ir matytumėte dalį informacijos, susijusios su veiklomis. Norėdami atidaryti išsamios informacijos rodinį, spustelėkite nuorodą stulpelyje **Prižiūrimo turto prastovos veiklos**. Paveikslėlyje pavaizduotas sąrašo **Prižiūrimo turto prastovos veiklos** pavyzdys.

![1 pav.](media/19-preventive-maintenance.png)


## <a name="create-a-maintenance-downtime-activity"></a>Pradėti prižiūrimo turto prastovos veiklą

1. Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Prižiūrimo turto prastovos veiklos** > **Visos prižiūrimo turto prastovos veiklos** arba **Aktyvios prižiūrimo turto prastovos veiklos**.

2. Spustelėkite **Naujas**.

3. Lauke **Prižiūrimo turto prastovos veiklos** įterpkite ID, o lauke **Pavadinimas** – pavadinimą.

4. Įterpkite priežiūros sustabdymo laikotarpį į laukus **Pradžios data / laikas** ir **Pabaigos data / laikas.**.

5. Iš „FastTab“ **Prižiūrimo turto prastovos veiklos** > spustelėkite **Pridėti eilutę**, kad galėtumėte pridėti turtą iškart į prižiūrimo turto prastovos veiklą.

6. Spustelėkite **Įrašyti**, kai būsite pridėję visą turtą. Toliau esančiame paveikslėlyje pavaizduotas prižiūrimo turto prastovos veiklos, susijusios su turtu ir priežiūros užduotimis, pavyzdys.

7. Darbo užsakymo priežiūros užduotys ir atidarytos priežiūros grafiko eilutės, susijusios su pasirinktu turtu, matomu „FastTab“ **Numatomos darbo užsakymo priežiūros užduotys** ir „FastTab“ **Priežiūros grafiko eilutės**. „FastTab“ **Bendra** > grupėje **Darbo užsakymai** > lauke **Priežiūros prognozės valandos** ir „FastTab“ **Bendra** > grupėje **Priežiūros grafikas** > lauke **Priežiūros prognozės valandos** matysite bendrą darbo užsakymo priežiūros užduočių ir priežiūros grafiko eilučių prognozuojamų valandų skaičių.

Paveikslėlyje pavaizduotas informacijos rodinio **Prižiūrimo turto prastovos veiklos** pavyzdys.

![2 pav.](media/20-preventive-maintenance.png)

>[!NOTE]
>Darbo užsakymo priežiūros užduotys ir priežiūros grafiko eilutės, susijusios su pasirinktu turtu, automatiškai atnaujinamos, jei sukurti nauji darbo užsakymai arba priežiūros grafiko eilutės yra sukuriamos po to, kai sukūrėte prižiūrimo turto prastovos veiklą. Pavyzdžiui, jei į susijusį turtą suplanuotumėte priežiūros planus arba priežiūros ciklus per dvi dienas po to, kai buvo sukurta prižiūrimo turto prastovos veikla, naujos priežiūros grafiko eilutės automatiškai įtraukiamos į prižiūrimo turto prastovos veiklą.

8. **Visos prižiūrimo turto prastovos veiklos** > **Prižiūrimo turto prastovos veiklos** > pasirinkite prižiūrimo turto prastovos veiklą iš sąrašo ir spustelėkite **Pajėgumas**, kad būtų galima atidaryti dialogo langą **Skaičiuoti pajėgumą**. Naudokite šį dialogo langą, jei norite peržiūrėti pajėgumą, pvz., datą, turtą, turto tipus ir priežiūros užduočių tipus. Atkreipkite dėmesį, kad datos, rodomos dialogo lange, yra pradžios ir pabaigos datos, pasirinktos iš **Prižiūrimo turto prastovos veiklos**. Šis skaičiavimas apima turtą, susijusį su prižiūrimo turto prastovos veikla.

9. Jei reikia, dialogo lange **Apskaičiuoti pajėgumą** redaguokite pradžios ir pabaigos laikus ir pasirinkite, ar norite į skaičiavimą įterpti darbo užsakymus ir priežiūros grafikus. Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti skaičiuojant pajėgumą. Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra yra kelių lygių, tai visas turtas, skirtas funkcinei vietai ir pasirinktas prižiūrimo turto prastovos veiklai, bus rodomas viršuje, todėl valandas į eilutę galėsite įtraukti iš žemiau esančių funkcinių vietų. Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, pajėgumo eilutes.

10. Norėdami pradėti skaičiavimą, spustelėkite **Gerai**. Bendras valandų skaičius rodomas apžvalgoje **Pajėgumas**. Skirtuke **Pajėgumas** > veiksmų srities grupėse **Grupuoti pagal...** spustelėkite atitinkamus mygtukus, norėdami gauti išsamesnę prognozuojamų valandų paskirstymo apžvalgą. Toliau pateiktame paveikslėlyje pateikiami **Pajėgumo** skaičiavimo rezultatai.

![3 pav.](media/21-preventive-maintenance.png)

11. Sužinoję pajėgumą, jei norite pakoreguoti darbo užsakymo priežiūros užduotis arba priežiūros grafiko eilutes, grįžkite į išsamų rodinį **Prižiūrimo turto prastovos veiklos** ir pasirinkite eilutes, kurias norite koreguoti „FastTab“ **Atsiradusios darbo užsakymo priežiūros užduotys** ir „FastTab“ **Priežiūros grafiko eilutės**.

12. Spustelėkite mygtuką **Koreguoti** ir atnaujinkite numatomas pradžios / pabaigos datas, aptarnavimo lygį arba atsakingus priežiūros darbuotojus, paskirtus pasirinktoms darbo užsakymo priežiūros užduotims arba priežiūros grafiko eilutėse.

13. Spustelėkite **Gerai**, kai atliksite reikiamus koregavimus. 

>[!NOTE]
>Darbo užsakymo priežiūros užduotys ir priežiūros grafiko eilutės, kurios neįtrauktos į prižiūrimo turto prastovos laikotarpį po to, kai atlikote koregavimus, automatiškai pašalinami iš **Prižiūrimo turto prastovos veiklos**.

14. **Visos prižiūrimo turto prastovos veiklos** > **Prižiūrimo turto prastovos veiklos** > pasirinkite prižiūrimo turto prastovos veiklą iš sąrašo ir spustelėkite **Elemento prognozė**, kad būtų galima atidaryti dialogo lange **Skaičiuoti elemento prognozę**. Naudokite šį dialogo langą apskaičiuoti prekių (atsarginių dalių ir kitų būtinų elementų) prognozes ir jas sugrupuoti, kad būtų galima peržiūrėti, pvz., pagal datą, turtą, turto tipą ir priežiūros užduoties tipą. Atkreipkite dėmesį, kad datos, rodomos dialogo lange, yra pradžios ir pabaigos datos, pasirinktos iš **Prižiūrimo turto prastovos veiklos**. Šis skaičiavimas apima atsargines dalis ir prekes, susijusias su turtu, pasirinktu prižiūrimo turto prastovos veikloje.

15. Jei reikia, dialogo lange **Apskaičiuoti elemento prognozę** redaguokite pradžios ir pabaigos laikus ir pasirinkite, ar norite į skaičiavimą įterpti darbo užsakymus ir priežiūros grafikus. Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti skaičiuojant pajėgumą. Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra yra kelių lygių, tai visas turtas, skirtas funkcinei vietai ir pasirinktas prižiūrimo turto prastovos veiklai, bus rodomas viršuje, todėl valandas į eilutę galėsite įtraukti iš žemiau esančių funkcinių vietų. Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, pajėgumo eilutes.

16. Norėdami pradėti skaičiavimą, spustelėkite **Gerai**. Bendras elemento prognozių skaičius, rodomas apžvalgoje **Elemento prognozė**. Skirtuke **Elemento prognozė** > veiksmų srities grupėse **Grupuoti pagal...** spustelėkite atitinkamus mygtukus, norėdami gauti išsamesnę prognozuojamų elementų paskirstymo apžvalgą. Toliau esančiame paveikslėlyje pavaizduoti **Elemento prognozė** rezultatai.

![4 pav.](media/22-preventive-maintenance.png)

- Galite kopijuoti turtą iš vienos prižiūrimo turto prastovos veiklos į kitą. Iš **Visos prižiūrimo turto prastovos veiklos** pasirinkite mygtuką **Kopijuoti prižiūrimo turto prastovos veiklą** ir pasirinkite atrankos kriterijus laukuose **Iš prižiūrimo turto prastovos veiklų** ir **Prižiūrimo turto prastovos veiklos**, tada spustelėkite **Gerai**.
- **Visos prižiūrimo turto prastovos veiklos** spustelėkite mygtuką **Priežiūros grafiko eilutės** arba mygtuką **Aktyvūs darbo užsakymai**, kad būtų atidaryti susiję sąrašai ir galėtumėte peržiūrėti eilutes, susijusias su pasirinkta prižiūrimo turto prastovos veikla.

