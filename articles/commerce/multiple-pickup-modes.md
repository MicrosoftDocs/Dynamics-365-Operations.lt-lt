---
title: Įjungti keletą paėmimo pristatymo režimų kliento užsakymams
description: Šioje temoje paaiškinamos „Microsoft Dynamics 365 Commerce“ funkcijos leidžiančios jums sukurti kliento užsakymus paėmimui parduotuvėje.
author: hhainesms
ms.date: 06/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: a8fec96eb644cccea3566a32f3eb2ac3c699faa412be2bb9cdb2690d34999542
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745361"
---
# <a name="enable-multiple-pickup-delivery-modes-for-customer-orders"></a>Įjungti keletą paėmimo pristatymo režimų kliento užsakymams

[!include [banner](includes/banner.md)]


„Microsoft Dynamics 365 Commerce“ versijoje 10.0.16 ir vėlesnėse, organizacijos gali nustatyti keletą pristatymo režimų, kuriuos pardavėjai ar pardavimo agentai gali pasirinkti jiems sukuriant užsakymą, kuris bus atsiimtas parduotuvėje. Tokiu būdu, organizacijos gali suteikti keletą atsiėmimo parinkčių jų prekybininkams. Pavyzdžiui, daugelis mažmenininkų dabar siūlo prekybininkams pasirinkimą atsiimti parduotuvėse arba atsiimti per langelį užsakymus. „Commerce“ palaiko šių skirtingų paėmimo pristatymo režimų konfigūravimą. Vartotojai gali pasinaudoti jais kurdami kliento užsakymus bet kuriame palaikomame „Commerce“ kanale (e-komercija, skambučių centras ar parduotuvę).

## <a name="enable-and-configure-pickup-delivery-modes"></a>Įjungti ir konfigūruoti atsiėmimo pristatymo būdus

Norėdami naudoti šias funkcijas, įjunkite **Palaikymas keletui atsiėmimo pristatymo režimų** funkciją  **Funkcijų valdymo** darbo srityje „Commerce“ štabe. Jums įjungus funkciją, reikės atlikti papildomą konfigūravimą.

„Commerce“ versjoje 10.0.15 ir ankstesnėse, organizacijos gali nustatyti tik vieną pristatymo būdą kaip skirtą atsiėmimo pristatymo būdą. Ši sąvoka yra užbaigta **„Commerce“ parametrų** puslapyje. Versijoje 10.0.16 ir vėlesnėse, jums įjungus **Palaikyti keletą atsiėmimo pristatymo būdų** funkciją, pristatymo būdas, kuris buvo anksčiau nustatytas atsiėmimo pristatymo būdui **„Commerce“ parametrų** puslapyje yra automatiškai nukopijuojamas į naują konfigūravimą paėmimui pristatymo režimams.

![Paėmimo pristatymo režimai „Commerce“ parametrų puslapyje.](media/multiplepickupparameter.png)

Jums įjungus **Palaikymo keletui paėmimo pristatymo būdų** funkciją galite nurodyti keletą paėmimo pristatymo būdų **Pristatymo paėmimo būdo** tinklelyje **Pristatymo būdai** „FastTab“ skirtuke **TInkinti užsakymai** puslapyje **„Commerce“ parametrai**.

**Pristatymo atlikimo būdas** ir **Elektroninio pristatymo būdo** laukeliai bei **Rodyti tik vežėjo būdo parinktis siunčiamiems užsakymams** parinktis, buvo perkelta į šį „FastTab“.

Prieš tai, kai sukonfigūruosite paėmimo pristatymo būdus, turite nustatyti pristatymo būdus. Puslapyje **Pristatymo būdai** „Commerce“ štabe įtraukite pristatymo būdus, kurie turi būti laikomi atsiėmimo pristatymo būdais. Įsitikinkite, kad konfigūravimas baigtas. Pavyzdžiui, jei tam tikroms parduotuvėms siūlote šį pristatymo būdą kaip pristatymo pasirinktį, turite sukurti naują pristatymo būdą šiam tikslui. Šį pristatymo būdą galite sukurti naudodami aprašymą „curbside pickup". Tada galite būti užtikrinti, kad "curbside pick" pristatymo būdas yra susietas su visais „Commerce" kanalais, kurie gali jį pasiūlyti, įskaitant interneto parduotuves, kurios gali suteikti šią parinktį, ir atskirus parduotuvės kanalus, kurie pasiūlys šį vykdymo metodą. Pristatymo būdai taip pat turi būti susieti su produktais. Šiame pavyzdyje, jei yra tam tikrų produktų, kurių negalima įvykdyti naudojant „curbside paėmimą", turite užtikrinti, kad tos prekės būtų neįtrauktos. Pabaigus naujų pristatymo būtų įtraukimą, vykdykite **Apdoroti pristatymo būdus** darbą, kad sukurtumėte ryšius tarp pristatymo būdų, kanalų ir prekių. Kai darbas yra baigtas, atverkite **Paskirstymo grafikas** puslapį „Commerce“ štabe ir vykdykite **1120** paskirstymo darbą siekiant užtikrinti, kad atitinkamas „Commerce“ kanalo duomenų bazės yra atnaujintos su jūsų nauju pristatymo būdo konfigūravimu.

![Pristatymo būdo pavyzdys konfigūruoti atsiėmimą per langelį.](media/pickupmodes.png)

Po to, kai nustatysite papildomus atsiėmimo pristatymo būdus, įtrauktie juos į **Atsiėmimo pristatymo būdo** tinklelį puslapyje **„Commerce“ parametrai**. Tuomet vykdykite atitinkamus paskirstymo darbus siekiant naujinti atitinkamas „Commerce“ kanalo duomenų bazes su konfigūravimo keitimu.

> [!NOTE]
> Kartu su esančiu atsiėmimo pristatymu būdu, kuris nukopijuotas į **Atsiėmimo pristatymo būdo** tinkelį jums įjungus **Palaikymas keletui atsiėmimo pristatymo būdų** funkciją, kiekvienam papildomam atsiėmimo pristatymo būdo konfigūravimui, kuriį sukūrėte, turite konfigūruoti naujus pristatymo būdus. Jums įtraukus pristatymo būdus į **Atsiėmimo pristatymo būdo** tinklelį, „Commerce“ patvirtina, ar bet kurios atviros pardavimo eilutės jau juos naudoja. Jei randamos kokios nors atviros pardavimo užsakymo eilutės, gausite klaidos pranešimą. Pristatymo būdai nėra laikomi atsiėmimo pristatymo būdais, kol visos atviros užsakymo eilutės, juos naudojančios, bus užvertos (arba įtrauktos į sąskaitą ar panaikintos).

> [!IMPORTANT]
> Jums nustačius daugiau nei vieną atsiėmimo pristatymo būdą **„Commerce“ parametrų** puslapyje, **Palaikymas keletui atsiėmimo pristatymo būdų** funkcija tampa privaloma ir nebegali būti išjungta. Jei privalote išjungti šią funkciją, pašalinkite visus ir palikite tik vieną atsiėmimo pristatymo būdą iš **Atsiėmimo pristatymo būdo** tinklelio. Kai tik vienas atsiėmimo pristatymo būdas yra nustatytas, funkcija nebėra laikoma privaloma ir gali būti išjungta.

### <a name="e-commerce-site-configurations"></a>E-komercijos saito konfigūravimai

Kai **Palaikymas keletui atsiėmimo pristatymo būdų** funkcija yra įjungta, tolesni moduliai e-komercijos puslapiuose rodo naujus atsiėmimo pristatymo būdus, kaip konfigūruota:

- Pirkimo laukelis
- Parduotuvės išrinkiklis
- Krepšelis
- Paėmimo informacija
- Užsakymo patvirtinimas
- Užsakymo informacija

Nereikia jokių papildomų žingsnių e-komercijos puslapiuose tam, kad paėmimo pristatymo režimai būtų prieniami.

## <a name="work-with-multiple-pickup-delivery-modes"></a>Darbas su keletu paėmimo pristatymo režimų

Kai daugelis pasiėmimo pristatymo režimų yra prieiname kanale, papildoma patirtis suteikiama klientams, kai jie apsiperka atsiimamais produktais. 

- E-komercijos kanaluose, prekybininkai gali pasirinkti bet kurį galiojantį prieinamą atsiėmimo režimą. Pavyzdžiui, mažmenininkas nustato du atsiėmimo pristatymo režimus (atsiėmimą parduotuvėje ar per langelį), abu jie sukonfigūruojami **Atsiėmimo pristatymo režimo** tinklelyje ir abu galioja užsakymo įgyvendinimo kanale ir produktui, kurį šiuo metu pirkėjas įsigyja. Šiuo atveju, pirkėjas gali pasirinkti jam tinkamą atsiėmimo pristatymo režimą. Pasirinktas atsiėmimo pristatymo režimas tuomet tampa pristatymo būdu, kuris susietas su pardavimo užsakymo eilute, kai užsakymas sukuriamas „Commerce“ štabe.

    ![Atsiėmimo parinkties pasirinkimas e-komercijoje.](media/pickupecommerce.png)

- Parduotuvių kanaluose, jei kliento užsakymas atsiėmimui sukuriamas per pardavimo taško (POS) programą, su pardavimo susijęs asmuo skatinamas pasirinkti tarp esamo atsiėmimo pristatymo būdo, jei jie buvo sukonfigūruoti. Jei galioja tik vienas atsiėmimo pristatymo būdas kanalui ir prekei, prekybinikas nėra skatinamas jį pasirinkti. Vietoje to, esamas atsiėmimo pristatymo būdas automatiškai taikomas užsakymo eilutėms.

    ![Atsiėmimo parinkties pasirinkimas POS programoje.](media/pickuppos.png)

- Skambučių centro kanaluose, vartotojams sukūrus atsiėmimo užsakymus jie gali rankiniu būdu pasirinkti bet kurį atsiėmimo pristatymo būdą, kuris susietas su skambučių centro kanalu. Sistema tada patvirtina, ar pasirinktas atsiėmimo pristatymo būdas gali būti naudojamas kai prekė yra susieta su užsakymu. Pasirinkus atsiėmimo pristatymo būdą skambučių centro kanaluose, pardavimo užsakymo eilutės turi būti susietos su galiojančiu parduotuvės sandėliu. Jei ne parduotuvės sandėlis yra nustatytas skambučių centro pardavimo eilutėje, atsiėmimo pristatymo būdas negali būti nustatytas pardavimo eilutėje.
- Prekybininkas gali naudoti **Užsakymo atšaukimo** ar **Užsakymo įgyvendinimo** veiksmą POS programoje, kad gautų užsakymų sąrašą ar užsakymo eilutės atsiėmimui. Jei prekybininkas naudoja iš anksto nusatytą paieškos filtrą, kad surastų visus užsakymus, kurie bus atsiimti iš esamos parduotuvės, užklausos yra keičiamos siekiant užtikrinti, kad paieškos rezultatai apima visus galiojančius užsakymus, kurie naudos atsiėmimo pristatymo būdą. POS naudotojai gali taip pat naudoti esančius filtrus, kad susiaurintų užsakymų sąrašą iki konkretaus atsiėmimo pristatymo būdo. Pavyzdžiui, jie gali rodyti tik užsakymus atsiėmimui per langelį.

    ![Filtruokite atsiėmimo pristatymo būdus taikomus atšauktų užsakymų sąrašui.](media/pickuprecallorder.png)

## <a name="considerations-for-distributed-order-management"></a>Pasvarstymai dėl pristatyto užsakymo valdymo

[Pristatyto užsakymo valdymas (DOM)](./dom.md) funkcijos „Commerce“ ignoruoja visas pardavimo eilutes, kurios buvo sužymėtos atsiėmimui parduotuvėje. Šios funkcijos buvo atnaujintos siekiant užtikrinti, kad prekybos eilutės, susietos su konfigūruotu atsiėmimo pristatymo būdu apietų DOM logiką ir nebūtų iš naujo priskiriamos naujam įgyvendinimo sandėliui.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
