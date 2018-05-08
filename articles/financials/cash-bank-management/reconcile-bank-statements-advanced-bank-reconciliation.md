---
title: "Banko išrašų derinimas naudojant išplėstinį banko banko derinimą"
description: "Pažangaus banko suderinimo funkcija suteikia galimybę importuoti elektroninius banko išrašus ir automatiškai juos suderinti su banko operacijomis programoje „Microsoft Dynamics 365 for Finance and Operations“. Šioje temoje paaiškinamas derinimo procesas."
author: saraschi2
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationWorksheet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 98243
ms.assetid: 9df13adf-aa9d-4f6b-bde6-25a214611692
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ed3a1fae6ca30b9411fde47e7ef8a08150d7d748
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="reconcile-bank-statements-by-using-advanced-bank-reconciliation"></a>Banko išrašų derinimas naudojant išplėstinį banko banko derinimą

[!include [banner](../includes/banner.md)]

Pažangaus banko suderinimo funkcija suteikia galimybę importuoti elektroninius banko išrašus ir automatiškai juos suderinti su banko operacijomis programoje „Microsoft Dynamics 365 for Finance and Operations“. Šioje temoje paaiškinamas derinimo procesas.  

<a name="import-an-electronic-bank-statement"></a>Elektroninio banko išrašo importavimas
-----------------------------------

Banko išrašai importuojami puslapyje **Banko išrašai** naudojant veiksmą **Importuoti išrašą**. Banko išraše banko sąskaita nurodoma naudojant reikšmių, nustatytų banko sąskaitos informacijoje, derinį. Šios reikšmės apima banko pavadinimą, banko sąskaitos numerį, banko kodą, Tarptautinės organizacijos, teikiančios finansinių pranešimų perdavimo paslaugas (SWIFT) kodą ir tarptautinį banko sąskaitos numerį (IBAN). 

Galite nusiųsti banko išrašą, kuriame yra informacija apie vieną ar kelias sąskaitas. Jei yra kelios sąskaitos, sąskaitos gali būti skirtingų juridinių subjektų.

-   Norėdami importuoti vieną vienos sąskaitos banko išrašą, nustatykite parinktį **Importuoti kelių banko sąskaitų išrašą visuose juridiniuose subjekuose** į **Ne** ir pasirinkite banko sąskaitą, susietą su išrašu. Spustelėkite **Naršyti**, kad pasirinktumėte susietą banko išrašo failą, o tada spustelėkite **Nusiųsti**.
-   Norėdami importuoti vieną kelių sąskaitų banko išrašo failą, nustatykite parinktį **Importuoti kelių banko sąskaitų išrašą visuose juridiniuose subjekuose** į **Taip**. Spustelėkite **Naršyti**, kad pasirinktumėte susietą banko išrašo failą, o tada spustelėkite **Nusiųsti**.

Jei kurių nors elektroninio failo įrašų negalima susieti su banko sąskaita naudojant identifikavimo laukus, jie nebus importuojami. Tačiau kiti failo įrašai gali būti importuojami. Tada vartotojas gauna pranešimą, kuriame teigiama, kad tam tikrų banko sąskaitų banko išrašų importuoti nepavyko. Atkreipkite dėmesį, kad norėdamas importuoti juridinio subjekto banko sąskaitas banko išrašo failą importuojantis vartotojas turi turėti prieigą prie to juridinio subjekto. 

Norėdami vienu veiksmu į „Finance and Operations“ nusiųsti kelis išrašų failus, galite naudoti „zip“ failą. Norėdami importuoti kelis kelių sąskaitų banko išrašo failus, sujunkite visus banko išrašo failus į vieną „zip“ failą. Dialogo lange **Importuoti banko išrašus** nustatykite parinktį **Importuoti kelių banko sąskaitų išrašą visuose juridiniuose subjekuose** į **Taip**. Spustelėkite **Naršyti**, kad pasirinktumėte banko išrašo failų „zip“ failą, o tada spustelėkite **Nusiųsti**. Importavimo procesas atpažįsta „zip“ failą ir įkelia kiekvieną į jį įtrauktą išrašą, nepriklausomai nuo to, koks yra banko sąskaitos juridinis subjektas. 

Galima naudoti parinktį **Suderinti importavus**. Kai nustatote šios parinkties nuostatą **Taip**, sistema automatiškai patvirtina banko išrašą, sukuria naują banko derinimą ir darbalapį bei vykdo numatytąją gretinimo taisyklę, nustatytą nusiunčiant banko išrašą. Ši funkcija automatizuoja procesą iki to momento, kai operacijas reikia gretinti neautomatiniu būdu.

## <a name="validate-the-bank-statement"></a>Banko išrašo tvirtinimas
Norėdami patvirtinti išrašą, puslapyje **Banko išrašai** spustelėkite **Tvirtinti**. Prieš derinant banko išrašus, juos reikia patvirtinti. Jei importavimo metu nustatote parinkties **Suderinti importavus** nuostatą **Taip**, šis veiksmas atliekamas automatiškai. 

Banko išrašo tvirtinimo metu tikrinama toliau pateikta informacija.

-   Ar banko išrašas atitinka pasirinktą banko sąskaitą.
-   Ar banko išrašo valiuta atitinka banko sąskaitos valiutą.
-   Ar išrašo pradinis balansas lygus ankstesnio banko sąskaitos išrašo pabaigos balansui.
-   Ar data nesutampa su tos pačios banko sąskaitos kito banko išrašo data.
-   Ar banko sąskaitos išrašo datose nėra tarpų.
-   Ar išrašo eilučių datos patenka į diapazoną tarp banko išrašo pradžios datos ir pabaigos datos.
-   Ar pradinio balanso suma ir bendra eilučių suma lygios pabaigos balansui.

Kai tikrinimas baigtas, banko išrašo būsena atnaujinama kaip **Patvirtinta**. Prieš derinant banko išrašą, jį reikia patvirtinti.

## <a name="reconcile-the-bank-statement"></a>Banko išrašo derinimas
Importavę elektroninį banko išrašą ir išrašą patvirtinę, puslapyje **Banko išrašai** galite suderinti banko išrašą, naudodami puslapius **Banko derinimas** ir **Banko derinimo darbalapis**. 

Puslapyje **Banko derinimas** spustelėkite **Naujas**, kad sukurtumėte naują derinimą, o tada pasirinkite importuoto išrašo banko sąskaitą. Banko sąskaita gali būti susieta tik su vienu atviru banko derinimu. Nutraukimo data nustato banko išrašo operacijas ir „Operations“ banko operacijas, įtrauktas į derinimo darbalapį. Pagal numatytuosius parametrus dabartinė sistemos data yra naudojama kaip nutraukimo data, bet derinimo datą galite keisti. Likusi antraštės informacija automatiškai nuskaitoma iš išrašo. Jei importavimo metu nustatote parinkties **Suderinti importavus** nuostatą **Taip**, šis veiksmas atliekamas automatiškai. 

Puslapyje **Banko derinimas** spustelėkite **Darbalapis**, kad atidarytumėte puslapį **Banko derinimo darbalapis**. Jei nustatote parinkties **Suderinti importavus** nuostatą **Taip**, derinant numatytasis gretinimo taisyklių rinkinys taikomas automatiškai. Norėdami gretinimo taisykles vykdyti neautomatiškai, spustelėkite **Vykdyti gretinimo taisykles**, pasirinkite greitinimo taisyklių rinkinius arba gretinimo taisykles, kurias norite taikyti banko operacijoms. Jei norite apdoroti daug operacijų, šį veiksmą galite atlikti kaip paketinio vykdymo procesą. 

Puslapyje **Banko suderinimo darbalapis** rodomi keturi tinkleliai, kuriuose pateikiamos operacijos. Dviejuose viršutiniuose tinkleliuose rodomos banko išrašo ir „Operations“ operacijos, kurios dar nebuvo sugretintos. Dviejuose apatiniuose tinkleliuose rodomos sugretintos operacijos. Skirtuke **Banko išrašo operacijos informacija** rodoma informacija apie nesugretintą bako išrašo operaciją, pasirinktą viršutiniame tinklelyje. 

Gretinti arba derinti banko išrašo operacijas galima trimis būdais.

-   Derinti operacijas su „Operations“ banko operacijomis.
-   Derinti operacijas su atšaukimo banko išrašo operacija.
-   Pažymėti operacijas kaip **Nauja**, kad jas vėliau būtų galima registruoti kaip banko operacijas sprendime „Finance and Operations“.

Norėdami patys gretinti operacijas, pasirinkite operacijas tinklelyje **Banko išrašo operacijos**, pasirinkite atitinkamas operacijas tinklelyje **„Operations“ banko operacijos**, o tada spustelėkite **Gretinti**. Pasirinktos operacijos perkeliamos iš viršutinių nesugretintų operacijų tinklelių į apatinius sugretintų operacijų tinklelius. Be to, atnaujinamos bendrosios sugretintos ir nesugretintos sumos. Galite derinti vieną su viena operacija, kelias su viena operacija arba kelias su keliomis operacijomis. Gretinant privaloma laikytis leidžiamų datų nuokrypių ir operacijos tipo susiejimo taisyklių. Šios taisyklės nustatomos puslapyje **Grynųjų pinigų ir banko valdymo parametrai**.

Derinant gali atsirasti skirtumų centais. Galite gretinti vieną banko išrašo operaciją ir vieną „Operations“ banko operaciją, kurių sumos skiriasi centais, jei skirtumai centais neviršija banko sąskaitos lauke **Leistinas skirtumas centais** nustatytos leistino nuokrypio sumos. Suma rodoma „Operations“ banko operacijos lauke **Koregavimo suma**. Kai banko suderinimas pažymėtas kaip suderintas, naudojant susieto tipo banko operacijoje nurodytą pagrindinę sąskaitą automatiškai įkeliami pataisymai. Pataisymai nepalaikomi naudojant dokumentų tipus **Čekis** ir **Depozitas**. 

Banko išrašo operacijų atšaukimai yra sugretinami naudojant derinimo darbalapį. Galima suderinti dvi išrašo eilutes, jei sumos yra priešingos ir jei iš operacijų yra pažymėta kaip atšaukimas. Taip pat galite nustatyti veiksmo **Išvalyti atšaukimo išrašo eilutes** gretinimo taisyklę.

Atšauktas „Operations“ banko operacijas reikia suderinti naudojant puslapį **„Operations“ banko operacijos**. Galite suderinti dvi „Operations“ banko operacijas tarpusavyje, jei dokumentų banko sąskaita, dokumento tipas ir mokėjimo nuoroda sutampa ir jei dokumentų sumos yra priešingos. Taip pat galite suderinti vieną atšauktą čekį, kad tos operacijos nebūtų rodomos derinimo darbalapyje. 

Jei yra naujų banko inicijuotų operacijų, pvz., palūkanų, mokesčių ir išlaidų, kurių dar nėra sprendime „Finance and Operations“, galite jas įtraukti į žurnalą, kuris yra susietas su pasirinktu banko išrašo derinimu. Pasirinkite banko išrašo operaciją nesugretintų operacijų tinklelyje **Banko išrašo operacijos**, o tada spustelėkite **Pažymėti kaip naują**. Operacijos būsena nustatoma kaip **Nauja** ir operacija yra perkeliama į sugretintų operacijų tinklelį **Banko išrašo operacijos**. Operacijos, kurių būsena pažymėta kaip **Nauja**, registruojamos vėliau puslapyje **Banko išrašas**. 

Netinkamai sugretintų operacijų gretinimą galima atšaukti. Pasirinkite suderintą banko išrašo operaciją ir tada spustelėkite **Atšaukti gretinimą**. Visos susijusios operacijos yra perkeliamos į viršutinį nesugretintų operacijų tinklelį ir atnaujinamos bendrosios sugretintos ir nesugretintos sumos. 

Baigę derinimo procesą, darbalapį Banko derinimas turite pažymėti kaip suderintą.  Šis procesas automatiškai registruos koregavimo sumas naudodamas puslapyje **Banko operacijos tipas** nustatytas sąskaitas.  Išrašo banko derinimą pažymėti kaip suderintą galima bet kuriuo metu, net jei yra dar nesugretintų banko išrašo eilučių.  Nesugretintos operacijos bus automatiškai perkeltos į kitą derinimo darbalapį kaip nesugretintos banko išrašo operacijos, kurias reikia suderinti.  Atkreipkite dėmesį, kad, banko išrašo suderinimą pažymėjus kaip suderintą, jo atšaukti negalima.  Suderinimo nebebus galima redaguoti ir nebegalėsite jo naujinti.

## <a name="post-new-transactions-that-are-associated-with-the-reconciliation"></a>Naujų operacijų, susietų su derinimu, registravimas
Banko išrašo operacijos, kurių būseną derinimo darbalapyje pažymėjote kaip **Nauja**, yra užregistruojamos puslapyje **Banko išrašas**. Puslapyje **Banko išrašas** pasirinkite išrašo ID, kad peržiūrėtumėte išrašo informaciją. Meniu **Apskaita** galite naudoti parinktis **Peržiūrėti paskirstymus** ir **Peržiūrėti apskaitą**, kad peržiūrėtumėte naujų operacijų ir susietų DK įrašų informaciją. Pasirinkite parinktį **Registruoti**, kad DK užregistruotumėte banko išrašo eilutes, kurių būsena pažymėta kaip **Nauja**. Atkreipkite dėmesį, kad banko išrašą galima užregistruoti tik vieną kartą.




