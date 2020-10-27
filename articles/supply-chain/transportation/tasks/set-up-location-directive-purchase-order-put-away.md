---
title: Pirkimo užsakymo atidėjimo vietos nurodymo nustatymas
description: Šioje temoje paaiškinta, kaip nustatyti paprastą vietos nurodymą.
author: ShylaThompson
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c14fb92103fdd3c32ebc287a74a5dc4f4882b0e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981950"
---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Pirkimo užsakymo atidėjimo vietos nurodymo nustatymas

[!include [banner](../../includes/banner.md)]

Šioje temoje paaiškinta, kaip nustatyti paprastą vietos nurodymą. Parodytame pavyzdyje sukuriamas atidėjimo vietos nustatymas, kuris turi būti naudojamas nustatant prekių, gautų pirkimo užsakymui, talpinimo vietą. Šį užduoties vedlį galite paleisti su minėtais duomenimis naudodami demonstracinių duomenų įmonės USMF. Išankstinės sąlygos: turite sukurti perdavimo kodą. Atlikdami šią procedūrą mes naudojame perdavimo kodą, vadinamą Pakartotinis žymėjimas. Jei savo duomenyse kuriate vietos nurodymą, turite nustatyti išplėstinį sandėlio ir prekių sandėlio valdymą. Ši procedūra skirta sandėlio vadovui.

1. Naršymo srityje eikite į **Moduliai > Sandėlio valdymas > Sąranka > Vietos nurodymai**.
2. Lauke **Darbo užsakymo tipas** pasirinkite **Pirkimo užsakymai**.

## <a name="create-a-location-directive-header"></a>Vietos nurodymo antraštės kūrimas
1. Pasirinkite **Naujas**.
2. Lauke **Sekos skaičius** įveskite skaičių. Tai seka, kuria apdorojamas pasirinkto darbo tipo vietos nurodymas. Seką, jei reikia, galite modifikuoti.  
3. Lauke **Pavadinimas** įveskite reikšmę. Tai unikalus šio nurodymo identifikatorius.  
4. Lauke **Darbo tipas** pasirinkite **Padėjimas**. Pasirinkite norimo atlikti darbo tipą. **Padėjimas** yra vienintelė palaikoma reikšmė, kai nurodymo darbo užsakymo tipas yra Pirkimo užsakymas.  
5. Lauke **Vieta** įveskite reikšmę.
6. Lauke **Sandėlis** įveskite reikšmę. Krypties kodą palikite tuščią.  Krypčių kodai naudojami norint susieti darbo užsakymo eilutę, kurios tipas Padėjimas, su konkrečiu nurodymu. Pirkimo užsakymų paskutinės darbo užsakymo eilutės, kurios tipas Padėjimas, vieta nustatoma prieš nustatant darbo šabloną. Todėl neįmanoma prijungti paskutinės darbo šablono eilutės prie konkretaus nurodymo.   
7. Lauke **Perdavimo kodas** įveskite reikšmę. Perdavimo kodas riboja vietos nurodymo naudojimą, todėl vietos nurodymas naudojamas tik tada, jei registruojant prekę naudojantis mobiliuoju įrenginiu sandėlio darbuotojas įveda šią konkrečią vertę.  
8. Pasirinkite **Įrašyti**.

## <a name="edit-the-query-for-directive"></a>Nurodymo užklausos redagavimas
1. Pasirinkite **Redaguoti užklausą**. Šio nurodymo naudojimas ribojamas ir jį leidžiama naudoti tik prekėms, kurios registruotos jūsų nurodytame sandėlyje ir su jūsų nurodytu perdavimo kodu. Naudodami užklausą galite įtraukti kitų apribojimų.  
2. Pasirinkite **Gerai**.

## <a name="add-directive-lines"></a>Nurodymo eilučių įtraukimas
1. Pasirinkite **Naujas**. Tai seka, kuria apdorojamos pasirinkto darbo tipo vietos nurodymo eilutės. Seką, jei reikia, galite modifikuoti.  
2. Lauke **Pradinis kiekis** įveskite skaičių. Tai yra mažiausias kiekis, kuriam ši nurodymo eilutė yra taikoma.  
3. Lauke **Galutinis kiekis** įveskite skaičių.
4. Lauke **Vienetas** įveskite reikšmę. Vienetas, kuriuo išreikštas Pradinis kiekis ir Galutinis kiekis. Jei šis laukas paliekamas tuščias, naudojamas prekės atsargų vienetas.  
5. Lauke **Sandėliavimo kiekis** pasirinkite parinktį.
    - Nėra arba numerio lentelės kiekis: kiekvienoje numerio lentelėje užregistruotas kiekis.  
    - Numerio lentelių grupavimas: visos užregistruotos lentelės.  
    - Likęs kiekis: registruotinas kiekis, nurodytas pirkimo užsakymo eilutėje.  
    - Numatomas kiekis: bendras kiekis, nurodytas pirkimo užsakymo eilutėje.  
6. Pažymėkite arba atžymėkite žymės langelį **Riboti pagal vienetą**. Jei pažymėsite šią parinktį, o puslapyje **Riboti pagal vienetą** nurodysite vienetą, į vietą galima bus galima perkelti tik prekes su tuo matavimo vienetu. Pavyzdžiui, jei matavimo vienetas yra PL (padėklai), į nurodytą vietą galima perkelti tik padėkluose esančias prekes.  
7. Pažymėkite arba atžymėkite žymės langelį **Leisti išskaidyti**. Taip nurodymas gali išskaidyti kiekį keliose vietose.  
8. Pasirinkite **Įrašyti**.

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>Nurodymo eilutės apribojimas konkrečiu vienetu
1. Pasirinkite **Riboti pagal vienetą**. Šis mygtukas bus pasiekiamas tik tada, kai pažymėję žymės langelį **Riboti pagal vienetą** spustelėsite **Įrašyti**.  
2. Lauke **Vienetas** įveskite reikšmę.
3. Uždarykite puslapį.

## <a name="add-a-location-directive-action-line"></a>Vietos nurodymo veiksmo eilutės įtraukimas
1. Pasirinkite **Naujas**. Tai seka, kuria apdorojamos pasirinkto darbo tipo vietos nurodymo veiksmo eilutės. Seką, jei reikia, galite modifikuoti.  
2. Lauke **Pavadinimas** įveskite reikšmę. Tai unikalus šio nurodymo veiksmo identifikatorius.  
3. Lauke **Fiksuotos vietos naudojimas** pasirinkite parinktį.
    - Fiksuotos ir nefiksuotos vietos: galioja visos nefiksuotos vietos, taip pat ir paties produkto fiksuota vieta, užklausoje nurodytame diapazone.  
    - Tik produkto fiksuota vieta: galioja produkto fiksuotos vietos ir visiems produkto variantams priskiramas tas pats fiksuotų vietų rinkinys.  
    - Tik produkto variantų fiksuota vieta: galioja tik kiekvienam produkto variantui nurodytos fiksuotos vietos.  
4. Lauke **Strategija** pasirinkite parinktį. Darbo užsakymai, kurių tipas yra Pirkimo užsakymas, palaiko toliau nurodytas strategijas. 
    - Nėra: prekė dedama į tuščią vietą.  
    - Konsolidavimas: prekė perkeliama į vietą, kurioje jau yra panašių prekių.  
    - Tuščia vieta be prekių: prekė dedama į tuščią vietą. Vieta laikoma tuščia, jei joje nėra jokių fizinių atsargų ir jokio planuojamo darbo.  
5. Pasirinkite **Įrašyti**.

## <a name="edit-the-query-for-directive-action-line"></a>Nurodymo veiksmo eilutės užklausos redagavimas
1. Pasirinkite **Redaguoti užklausą**.
2. Pasirinkite **Įtraukti**.
3. Lauke **Laukas** įveskite `location profile ID`. Šiame pavyzdyje apribosime galimas vietas, naudodamiesi vietos profilio ID.  
4. Lauke **Kriterijai** įveskite reikšmę.
5. Pasirinkite **Gerai**. Jūs galite įtraukti tiek nurodymo eilučių ir nurodymo veiksmų, kad aprėptumėte visus galimus sandėlio scenarijus.  

