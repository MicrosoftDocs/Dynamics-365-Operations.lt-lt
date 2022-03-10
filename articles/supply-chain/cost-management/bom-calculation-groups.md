---
title: KS skaičiavimo grupės
description: Šiame straipsnyje pateikiama informacija apie komplektavimo specifikacijų (KS) skaičiavimo grupes ir tai, kaip jas nustatyti. Norėdami vykdyti KS skaičiavimą, turite nustatyti skaičiavimo grupes ir priskirti jas atskiroms prekėms arba nustatyti numatytąją skaičiavimo grupę. Tada skaičiuojant KS skaičiavimo grupės skaičiavimo parametrai naudojami kaip numatytosios reikšmės puslapyje KS skaičiavimas.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcGroup, BOMCalcTable, BOMCalcTrans, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94063
ms.assetid: 63e1b7dc-c2c5-41b0-81ed-e3e02d1b39e0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 098a2fc065f6ace992dba1b1ae78756d456eb73a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579861"
---
# <a name="bom-calculations-groups"></a>KS skaičiavimo grupės

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie komplektavimo specifikacijų (KS) skaičiavimo grupes ir tai, kaip jas nustatyti. Norėdami vykdyti KS skaičiavimą, turite nustatyti skaičiavimo grupes ir priskirti jas atskiroms prekėms arba nustatyti numatytąją skaičiavimo grupę. Tada skaičiuojant KS skaičiavimo grupės skaičiavimo parametrai naudojami kaip numatytosios reikšmės puslapyje KS skaičiavimas. 

Puslapyje **Atsargų ir sandėlio valdymo parametrai** reikia nurodyti numatytąją skaičiavimo grupę arba puslapyje **Išleisto produkto informacija** reikia nurodyti konkretaus produkto skaičiavimo grupę. Sistema pirmiausia ieško skaičiavimo grupės nustatymo puslapyje **Išleisto produkto informacija**. Jei skaičiavimo grupės ten neranda, ji ieško puslapyje **Atsargų ir sandėlio valdymo parametrai**. Jei sistema negali rasti skaičiavimo grupės, skaičiavimo metu vartotojui rodomas klaidos pranešimas. Skaičiavimo grupėje nurodytos savikainos modelio, pardavimo kainos modelio ir įspėjimų sąrašo strategijos. Skaičiuojant KS skaičiavimo grupės skaičiavimo parametrai naudojami kaip numatytosios reikšmės puslapyje **KS skaičiavimas**.

## <a name="purposes-of-bom-calculation-groups"></a>KS skaičiavimo grupių paskirtis
KS skaičiavimo grupę prekėms priskirti galima dėl kelių priežasčių.

-   Nustatant lauką **Savikainos modelis** nurodomas nupirkto komponento išlaidų įnašo duomenų šaltinis skaičiuojant planuojamas pagamintos prekės išlaidas. Kai kurie gamintojai skaičiuoja planuojamas išlaidas naudodami nupirktų komponentų pirkimo kainos prekybos sutartis ar kitus pagrindus, pvz., pirkimo kainos įrašus įkainojimo versijoje.
-   Nustatant lauką **Pardavimo kainos modelis** nurodoma, kaip prekės duomenys bus naudojami skaičiuoti siūlomas pardavimo kainas. Galite nurodyti prekės pardavimo kainą arba išlaidų grupę. Kai kurie gamintojai siekia skaičiuoti pagamintų prekių siūlomas pardavimo kainas. Suskaičiuota pardavimo kaina gali atspindėti grąžinamų kainų metode, pagrįstame komponento pardavimo kainos įrašu. Arba suskaičiuota pardavimo kaina gali atspindėti išlaidų ir antkainio metode, pagrįstame komponento išlaidų ir taikomais pelno procentais, susietais su komponento išlaidų grupe.
-   Nustačius lauką **Stabdyti išskleidimą** nurodoma, kad pagaminta prekė turi būti laikoma nupirkta preke, siekiant susumuoti išlaidas, kai skaičiuojama KS. Įprastais atvejais nupirkta preke yra laikoma prekė, kuri kartais yra pagaminta arba dabar perkama pagaminta prekė. Prekė pradžioje bus priskirta kaip pagaminta prekė, kad būtų galima apibūdinti KS ir maršruto informaciją, ir palaikyti prekės gamybos užsakymus. Tačiau vėliavėlė **Stabdyti išskleidimą** neleidžia skaičiuojant išlaidas naudoti prekės KS ir maršruto. Vietoj to KS skaičiavimas naudoja prekės nurodytas išlaidas.

## <a name="calculation-groups"></a>Skaičiavimo grupės
Skaičiavimo grupės nurodomos modulio Savikainos valdymas dalyje **Iš anksto nustatytos savikainos strategijų nustatymas**. Prekėms priskirtos skaičiavimo grupės suteikia galimybę nustatyti, iš kur skaičiuojant nuskaitoma prekių savikaina arba pardavimo kaina, kaip apibūdinta skaičiavimo grupėje. Puslapyje **Skaičiavimo grupės** galite nustatyti savikainos modelį, alternatyvių savikainos modelį, pardavimo modelį ir įspėjimus.

### <a name="cost-price-model"></a>Savikainos modelis

Lauke **Savikainos modelis** galima pasirinkti keturias parinktis.

-   **Prekės savikaina** – savikaina nuskaitoma iš lentelės **Išleistas produktas** arba prekės dimensijų derinys naudojamas kaip savikaina.
-   **Prekės pirkimo kaina** – pirkimo kaina nuskaitoma iš lauko **Savikaina**, kuris yra puslapio **Išleistų produktų sąrašas** lauke **Pirkimas**.
-   **Prekybos sutartys** – galite konfigūruoti prekybos sutartis, skirtas konkretiems prekių ir tiekėjų deriniams arba konkrečioms teritorijoms. Tada, kai čia pasirenkate parinktį **Prekybos sutartys**, bus naudojama sukurta pirkimo kainos prekybos sutartis ir prekė bei teritorija.
-   **Atsargų kaina** – dabartinė prekės atsargų reikšmė naudojama siekiant apskaičiuoti vieneto savikainą KS skaičiavimo metu. Vieneto savikaina apskaičiuojama tik tada, jei užregistruotas kiekis ir faktinis kiekis yra didesni nei 0 (nulis).

### <a name="alternative-cost-price"></a>Alternatyvi savikaina

Lauke **Alternatyvi savikaina** galimos tos pačios parinktys kaip lauke **Savikainos modelis**. Tačiau šis laukas naudojamas tik tada, kai kainos negalima rasti pirminiame savikainos modelyje.

### <a name="sales-price-model"></a>Pardavimo kainos modelis

Lauko **Pardavimo kainos** reikšmę galima apskaičiuoti dviem būdais.

-   **Išlaidų grupė** – pasirinkus šią parinktį, pardavimo kaina apskaičiuojama pagal išlaidų grupės savikainos ir pelno parametro procentinę vertę.
-   **Prekės pardavimo kaina** – pasirinkus šią parinktį, naudojama pardavimo kaina, nurodyta lentelės Išleistas produktas „FastTab“ lauke **Pardavimas**.

### <a name="stop-explosion"></a>Stabdyti išskleidimą

Žymės langelis **Stabdyti išskleidimą** naudojamas siekiant nurodyti, kada pagaminta prekė turi būti laikoma nupirkta preke. Paprastai žymės langelio **Stabdyti išskleidimą** žymėjimas yra panaikinamas. Norėdami nurodyti, kad skaičiuojant KS pagaminta prekė turi būti laikoma nupirktu komponentu (o ne pagamintu komponentu), pažymėkite šį žymės langelį. Atsižvelgiant į teritoriją, prekės savikaina vis dar gali būti skaičiuojama naudojant KS skaičiavimus. Sustabdomas suplanuotų pirkimo užsakymų ir gamybos užsakymų išskleidimas KS, kurios komponentai yra susieti su skaičiavimo grupe, kurios žymės langelis **Stabdyti išskleidimą** yra pažymėtas. Bendrojo planavimo metu sugeneruojami suplanuoti užsakymai pačioje KS, o ne prekėse, įtrauktose į KS. Iš esmės pažymėję šį žymės langelį nurodote, kad savikaina nebus įtraukta į šios skaičiavimo grupės prekių KS skaičiavimą.

### <a name="warnings"></a>Įspėjimai

„FastTab“ **Įspėjimai** pasirenkamos parinktys, skirtos bet kokiems įspėjimų pranešimams, kurie turėtų būti rodomi vartotojams, kai jie atlieka KS skaičiavimą. 

Pavyzdžiui, jei pasirenkate žymės langelį **Nėra KS**, vartotojui rodomas įspėjimas, jei jokia aktyvi vieno iš komponentų arba pirminės prekės (kuriai vykdomas KS skaičiavimas) KS versija nerasta. Kai pasirenkate žymės langelį **Nėra maršruto**, vartotojui rodomas įspėjimas, jei nėra jokios aktyvios maršruto versijos. Jei maršrutuose ir operacijose naudojate išteklių, galite sistemai nurodyti ieškoti tų išteklių. Tada, jei ištekliaus nerandama visose aktyvaus maršruto eilutėse, vartotojui rodomas įspėjimas. 

Taip pat galite tikrinti ir ieškoti suvartojimo. Vartojimas yra kiekis konkrečiame maršrute. Paprastai tai yra laikas, kurio reikia, kad būtų galima atlikti konkrečią gamybos proceso operaciją. Galite patikrinti, ar prekė neturi savikainos. Jei nėra jokios aktyvios prekės savikainos, į KS skaičiavimą savikaina neįtraukiama. 

Taip pat galite patikrinti ir patvirtinti savikainos terminą. Pavyzdžiui, įveskite **60** norėdami nurodyti, kad vieneto savikaina turi būti perkainota po 60 dienų. Jei pasiekiama ši riba, sistema generuoja įspėjimą. Pvz., prekės savikaina įvesta šių metų sausio mėn. Jei dabar yra rugpjūčio mėn. (t. y. praėjo daugiau kaip 60 dienų po to, kai buvo įvesta savikainą), vykdant KS skaičiavimą vartotojui rodomas įspėjimas. Lauke **Minimali kontribucijos marža** galite įvesti procentą. Ši reikšmė nurodo, kokia yra minimali leistina kontribucijos marža. Jei konkretaus komponento kontribucijos marža per maža, vartotojui rodomas įspėjimas. Todėl šis laukas padeda užtikrinti, kad išlaidos ir papildomos laikymo išlaidos, reikalingos jūsų prekėms, nebus pernelyg sumažintos.

### <a name="default-setup-in-inventory-and-warehouse-management-parameters"></a>Numatytasis modulio Atsargų ir sandėlio valdymas parametrų nustatymas

Kadangi skaičiavimams vykdyti reikalingos skaičiavimo grupės, atsargų valdymo parametruose turite nustatyti numatytąją skaičiavimo grupę. Šis nustatymas suteikia galimybę įmonėms naudoti standartinį visų prekių išlaidų grupės ir pelno nustatymą. Tada, jei konkrečiai prekei nustatyti specialūs skaičiavimo reikalavimai, tai prekei vartotojas gali priskirti kitą skaičiavimo grupę. Paprastai nustatomos KS sudėtinių prekių, o KS prekių skaičiavimo grupės. Tačiau, jei rodomi įspėjimo pranešimai, galima taikyti skaičiavimo grupes. Prekėms priskirta skaičiavimo grupė pakeičia numatytąją reikšmę, kuri nustatyta atsargų valdymo parametruose. 

Numatytąjį parametrą galite nustatyti pasirinkdami **Išlaidų valdymas** &gt; **Atsargų apskaitos strategijų nustatymas** &gt; **Parametrai** &gt; **Atsargų apskaita** &gt; **Skaičiavimo grupė**. Nustatydami numatytąją konfigūracijos grupę, taip pat galite konfigūruoti įspėjimo sąlygas, kad KS skaičiavimo proceso metu vartotojai būtų įspėti, jei dėl pasirinktų komponentų gali kilti skaičiavimo klaidų.

### <a name="view-warning-messages-on-the-complete-page"></a>Įspėjimus pranešimų peržiūra puslapyje Baigta

KS skaičiavimas generuoja įspėjimo pranešimus. Galite peržiūrėti pasirinktos prekės įspėjimus. Pvz., modulyje Pardavimas ir rinkodara sukurkite naują prekės D0001 pardavimo užsakymą. Tada pardavimo užsakymo eilutės meniu **Naujinti eilutę** spustelėkite **Skaičiuoti remiantis KS / formule**, kad peržiūrėtumėte skaičiavimo informaciją ir įspėjimus. KS skaičiavimo rezultatus taip pat galite peržiūrėti puslapyje **Baigta**. Dvi perspėjimo sąlygos taikomos tik pagamintoms prekėms, o keturios perspėjimo sąlygos taikomos bet kuriai prekei.
-   Nustatyti, kada pagaminta prekė neturi aktyvios KS.
-   Nustatyti, kada pagaminta prekė neturi aktyvaus maršruto.
-   Nustatyti, kai prekei KS eilutėje taikomas kiekis, lygus 0 (nuliui).
-   Nustatyti, kai prekei KS eilutėje taikomos išlaidos, lygios 0 (nuliui), arba kai ji neturi išlaidų įrašo.
-   Nustatyti, kai prekė KS eilutėje turi išlaidas, kurių galiojimo laikas pasibaigęs. Perspėjime atspindimas skaičiavimo datos ir dienų, nurodytų kaip maksimalus kainos terminas, palyginimas.
-   Nustatyti, kai prekės KS eilutėje pelningumo procentai yra mažesni nei jūs pageidaujate.

Galite nustatyti kelias KS skaičiavimo grupės, priklausomai nuo to, kiek skirtingų įspėjimo pranešimų norite. Pavyzdžiui, gali pakakti vienos KS skaičiavimo grupės, taikant perspėjimo sąlygas dėl aktyvios KS, kai tiek komponento kiekis, tiek komponento išlaidos lygūs 0 (nuliui). Perspėjimo sąlygos, susietos su KS skaičiavimo grupe, gali būti perrašomos inicijuojant KS skaičiavimą. Taip pat galima įspėjimo sąlygų pridėti arba pašalinti. Pavyzdžiui, galite pašalinti aktyvaus maršruto perspėjimo sąlygą, kai į esamą situaciją nėra įtraukti maršruto duomenys. **Pastaba.** Modulyje Laikas ir buvimas darbe teikiamas puslapis **Skaičiavimo grupės**, bet tas nesusijęs su KS skaičiavimo grupėmis. Taikant modulį Laikas ir buvimas darbe, darbuotojus galima priskirti skaičiavimo grupėms, kurios atspindi su tuo pačiu prižiūrėtoju arba vadovu susijusių darbuotojų grupavimą. Darbuotojų registracijų skaičiavimą galima atlikti automatiškai arba neautomatiniu būdu jį gali atlikti prižiūrėtojas ar vadovas.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]