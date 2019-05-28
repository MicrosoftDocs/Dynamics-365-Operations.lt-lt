---
title: Nustatyti pirkimo užsakymo atidėjimo vietos nurodymą.
description: Ši procedūra nurodo, kaip nustatyti paprastą vietos nurodymą.
author: ShylaThompson
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ca4b3c2598a268c065011daff31296521faa918
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551865"
---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Nustatyti pirkimo užsakymo atidėjimo vietos nurodymą.

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra nurodo, kaip nustatyti paprastą vietos nurodymą. Pateiktame pavyzdyje sukuriamas vietos nurodymas, kuris bus naudojamas norint nustatyti, kur padėti gautas pirkimo užsakymo prekes. Šį užduoties vedlį galite paleisti su minėtais duomenimis naudodami demonstracinių duomenų įmonės USMF. Išankstinės sąlygos: turite sukurti perdavimo kodą. Atlikdami šią procedūrą mes naudojame perdavimo kodą, vadinamą Pakartotinis žymėjimas. Jei kuriate savo duomenų vietos nurodymą, turite nustatyti patobulintą savo sandėlio ir prekių valdymą.  Ši procedūra skirta sandėlio vadovui.

1. Pasirinkite Sandėlio valdymas > Nustatymai > Vietos nurodymai.
2. Lauke Darbo užsakymo tipas pasirinkite „Pirkimo užsakymai“.

## <a name="create-a-location-directive-header"></a>Vietos nurodymo antraštės kūrimas
1. Spustelėkite Naujas.
2. Lauke Sekos numeris įveskite skaičių.
    * Tai seka, kuria apdorojamas pasirinkto darbo tipo vietos nurodymas. Seką, jei reikia, galite modifikuoti.  
3. Lauke Pavadinimas surinkite reikšmę.
    * Tai unikalus šio nurodymo identifikatorius.  
4. Lauke Darbo tipas pasirinkite „Padėjimas“.
    * Pasirinkite norimo atlikti darbo tipą. Norėdami pateikti darbo užsakymo nurodymą, įveskite Pirkimo užsakymas, o vienintelė palaikoma vertė yra Padėti.  
5. Lauke Teritorija surinkite reikšmę.
6. Lauke Sandėlis surinkite reikšmę.
    * Krypties kodą palikite tuščią.  Krypčių kodai naudojami norint susieti darbo užsakymo eilutę, kurios tipas Padėjimas, su konkrečiu nurodymu. Pirkimo užsakymų paskutinės darbo užsakymo eilutės, kurios tipas Padėjimas, vieta nustatoma prieš nustatant darbo šabloną. Todėl neįmanoma prijungti paskutinės darbo šablono eilutės prie konkretaus nurodymo.   
7. Lauke „Perdavimo kodas“ įveskite reikšmę.
    * Perdavimo kodas riboja vietos nurodymo naudojimą, todėl vietos nurodymas naudojamas tik tada, jei registruojant prekę naudojantis mobiliuoju įrenginiu sandėlio darbuotojas įveda šią konkrečią vertę.  
8. Spustelėkite Įrašyti.

## <a name="edit-the-query-for-directive"></a>Nurodymo užklausos redagavimas
1. Spustelėkite Redaguoti užklausą.
    * Šio nurodymo naudojimas ribojamas ir jį leidžiama naudoti tik prekėms, kurios registruotos jūsų nurodytame sandėlyje ir su jūsų nurodytu perdavimo kodu. Naudodami užklausą galite įtraukti kitų apribojimų.  
2. Spustelėkite GERAI.

## <a name="add-directive-lines"></a>Nurodymo eilučių įtraukimas
1. Spustelėkite Naujas.
    * Tai seka, kuria apdorojamos pasirinkto darbo tipo vietos nurodymo eilutės. Seką, jei reikia, galite modifikuoti.  
2. Lauke Pradinis kiekis įveskite skaičių.
    * Tai yra mažiausias kiekis, kuriam ši nurodymo eilutė yra taikoma.  
3. Lauke Galutinis kiekis įveskite skaičių.
4. Lauke „Vienetas“ įveskite reikšmę.
    * Vienetas, kuriuo išreikštas Pradinis kiekis ir Galutinis kiekis. Jei šis laukas paliekamas tuščias, naudojamas prekės atsargų vienetas.  
5. Lauke Rasti kiekį pasirinkite parinktį.
    * Nėra arba numerio lentelės kiekis: kiekvienoje numerio lentelėje užregistruotas kiekis. Vienetais išskirstytas kiekis: visas užregistruotas kiekis. Likęs kiekis: registruotinas kiekis, nurodytas pirkimo užsakymo eilutėje. Numatomas kiekis: bendras kiekis, nurodytas pirkimo užsakymo eilutėje.  
6. Pažymėkite arba atžymėkite žymės langelį Riboti pagal vienetą.
    * Jei pasirinksite šią pasirinktį ir puslapyje Riboti pagal vienetą nurodysite vienetą, į vietą bus galima perkelti tik tas prekes, kurių matavimo vienetas atitinka nurodytą vienetą. Pavyzdžiui, jei matavimo vienetas yra PL (padėklai), į nurodytą vietą galima perkelti tik padėkluose esančias prekes.  
7. Pažymėkite arba atžymėkite žymės langelį Leisti skaidyti.
    * Taip nurodymas gali išskaidyti kiekį keliose vietose.  
8. Spustelėkite Įrašyti.

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>Nurodymo eilutės apribojimas konkrečiu vienetu
1. Spustelėkite Riboti pagal vienetą.
    * Šis mygtukas galimas tik tada, kai pažymėję žymės langelį Riboti pagal vienetą paspaudžiate Įrašyti.  
2. Lauke „Vienetas“ įveskite reikšmę.
3. Uždarykite puslapį.

## <a name="add-a-location-directive-action-line"></a>Vietos nurodymo veiksmo eilutės įtraukimas
1. Spustelėkite Naujas.
    * Tai seka, kuria apdorojamos pasirinkto darbo tipo vietos nurodymo veiksmo eilutės. Seką, jei reikia, galite modifikuoti.  
2. Lauke Pavadinimas surinkite reikšmę.
    * Tai unikalus šio nurodymo veiksmo identifikatorius.  
3. Lauke Fiksuotos vietos naudojimas pasirinkite parinktį.
    * Fiksuotos ir nefiksuotos vietos: visos nefiksuotos vietos galioja kaip ir produkto fiksuota vieta – užklausoje nurodytu diapazonu.  Tik produkto fiksuota vieta: galioja produkto fiksuotos vietos ir visiems produkto variantams priskiramas tas pats fiksuotų vietų rinkinys. Tik produkto variantų fiksuota vieta: galioja tik kiekvienam produkto variantui nurodytos fiksuotos vietos.  
4. Lauke Strategija pasirinkite parinktį.
    * Darbo užsakymai, kurių tipas Pirkimo užsakymas palaiko šias strategijas: Nėra: prekė perkeliama į pirmą rastą vietą. Konsolidavimas: prekė perkeliama į vietą, kurioje jau yra panašių prekių. Tuščia vieta, kurioje negaunama darbo: prekė perkeliama į pirmą rastą tuščią vietą. Vieta laikoma tuščia, jei joje nėra jokių fizinių atsargų ir jokio planuojamo darbo.  
5. Spustelėkite Įrašyti.

## <a name="edit-the-query-for-directive-action-line"></a>Nurodymo veiksmo eilutės užklausos redagavimas
1. Spustelėkite Redaguoti užklausą.
2. Spustelėkite Pridėti.
3. Lauke Laukas įveskite „vietos šablono ID“.
    * Šiame pavyzdyje mes apribosime galimas vietas naudodami vietos šablono ID.  
4. Lauke Kriterijai surinkite reikšmę.
5. Spustelėkite GERAI.
    * Jūs galite įtraukti tiek nurodymo eilučių ir nurodymo veiksmų, kad aprėptumėte visus galimus sandėlio scenarijus.  

