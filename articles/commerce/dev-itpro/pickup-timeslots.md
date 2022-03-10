---
title: Kurti ir naujinti laiko vietas kliento atsiėmimui
description: Šioje temoje aprašoma, kaip kurti, konfigūruoti ir naujinti kliento paėmimo laikų vietas „Commerce“ štabe.
author: anupamar-ms
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.15 update
ms.openlocfilehash: a9ee1356bfcaeee881c28cf0361b34b2c65acbc7a3b57347fa2581a8a935da42
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713426"
---
# <a name="create-and-update-time-slots-for-customer-pickup"></a>Kurti ir naujinti laiko vietas kliento atsiėmimui

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašoma, kaip kurti, konfigūruoti ir naujinti kliento paėmimo laikų vietas „Commerce“ štabe.

Laiko vietos funkcija suteikia mažmeniniams prekybininkams būdą nustatyti laiko vietas prekėms, kurios paėmimo pristatymo būdas yra įjungtas. Laiko vietos leidžia mažmeniniams prekybininkams nustatyti dienas ir laikus, kai užsakymai gali būti paimami iš parduotuvės. Mažmeniniai prekeiviai taip pat gali nustatyti užsakymų skaičius, kurie gali būti paimti per tam tikrą laikotarpį. Tokiu būdu, mažmeniniai prekeiviai gali apriboti užsakymų skaičių, kurį galima atsiimti per tam skirtą dieną ir tam skirtu laiku. Rezultatai yra geros kokybės patirtis jų klientams.

> [!NOTE]
> Laiko vietos funkcija yra prieinama „Microsoft Dynamics 365 Commerce“ versija 10.0.15 ir vėlesnė.

Tolesnis paveikslėlis rodo laiko vietos pavyzdžio pasirinkimą e-komercijos išregistravimo metu.

![Laiko vietos pasirinkimo pavyzdys e-komercijos išsiregistravimo metu.](../dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="time-slot-properties"></a>Laiko vietos ypatybės

Laiko vieta yra konkretus intervalas, kai klientas gali pasirinkti, ar atsiimti užsakymą iš konkrečios parduotuvės ar vietos. Laiko vietos valdymo funkcija yra prieinama tik kai kliento atsiėmimo pristatymo būdas sukonfigūruotas „Dynamics 365 Commerce“.

Laiko vieta yra nustatyta naudojant tolesnes ypatybes:

- **Pristatymo būdas** – Nurodykite pristatymo atsiėmimo būdą, kai taikoma laiko vieta.
- **Mažiausia dienų** ir **Daugiausia dienų** – Nurodo anksčiausias ir vėliausias datas, kurias galima pasirinkti pasiėmimo metu pagal datą, kai užsakymas yra padarytas. 

    **Mažiausia dienų** ypatybė užtikrina, kad yra pakankamai laiko mažmeniniam prekeiviui siekiant apdoroti užsakymą prieš tai, kai jis yra parengtas atsiėmimui. Ypatybė **Daugiausia dienų** užtikrina, kad vartotojas negalėtų pasirinkti datos, kuri yra toli ateityje. Pavyzdžiui, jei minimali vertė yra nustatyta į **1**, o užsakymas yra padarytas rugsėjo 20 dieną, anksčiausią dieną, kai užsakymas bus prieinamas atsiėmimui kitą galiojančią dieną (rugsėjo 21 d.). Panašiu būdu, maksimalios vertės nustatymui, galite nustatyti maksimalų dienų skaičių, per kurį galima atsiimti užsakymą. Kai minimalios ir maksimalios vertės yra nustatytos, svetainės vartotojai gali matyti ar pasirinkti tik konkretų dienų rinkinį jų išsiregistravimo patirtyje.

    Galite nustatyti minimalią vertę iki dešimtainės, kuri yra mažesnė nei 1. Pavyzdžiui, jei atsiėmimas yra prieinamas keturias valandas po to, kai užsakymas yra padarytas, nustatykite minimalią vertę į **0,17** (= 4 ÷ 24, suapvalinta iki dviejų dešimtainių vietų). Nepaisant to, jei nustatote minimalią vertę iki dešimtainės vertės, kuri didesnė nei 1, ji visuomet apvalinama iki artimiausio sveiko skaičiaus. Pavyzdžiui, vertė **1,2** bus suapvalinta iki **2**. Panašiai, jei nustatote maksimalią vertę iki dešimtainės vertės, ji yra visuomet apvalinama iki artimiausio sveiko skaičiaus. 

- **Pradžios data** ir **Pabaigos data** – Nurodykite pradžios ir pabaigos datas laiko vietai. Kas kartą kai laiko vietos įrašas turi pradžios ir pabaigos datą. Dėl to, galite būti lankstūs ir įtraukti kitą laiko vietą per metus (pavyzdžiui, paėmimui per atostogų valandas). Jei laiko vietos pradžios ir datos yra keičiamos padarius užsakymą, pakeitimai nebus taikomi tam užsakymui. Jums nustačius pradžios ir pabaigos datas, turite apgalvoti parduotuvės užsidarymo datas (pavyzdžiui, Kalėdų dieną) ir įsitikinti, kad laiko vietos nėra nustatytos tomis dienomis.
- **Aktyvios valandos atsiėmimui** – Nurodykite laikotarpį, kai atsiėmimas yra leidžiamas. Pavyzdžiui, paėmimo laikai gali būti nuo 14:00 iki 17:00 kas dieną. Ši ypatybė leidžia atsiėmimo laikus, kurie priklauso nuo parduotuvės valandų. Dėl to, pardavėjas gali konfigūruoti atsiėmimo laikus, kurie atitinka jo konkrečius įmonės reikalavimus. Jums nustačius veikiančias atsiėmimo valandas, privalote apgalvoti parduotuvės valandas ir užtikrinti, kad atsiėmimo laikai nėra nustatyti laiku, kai parduotuvė yra uždaryta.

    > [!NOTE]
    > Atsiėmimo parduotuvėje valandos turi būti nustatytos parduotuvę atitinkančioje laiko zonoje.

- **Laiko vietos intervalas** – Nurodykite laiką, kuris gali būti priskirtas kiekvienai laiko vietai. Pavyzdžiui, kiekvienos laiko vietos trukmė gali būti didėjanti 15, 30 minučių ar viena valanda. Jei laiko vietos vertė yra 0, laiko vieta yra prieinama per visą laiką nuo pradžios iki pabaigos laiko.
- **Vietos vienam intervalui** – Nurodykite klientų ar užsakymų skaičių, kuris gali būti aptarnautas atsiėmimo metu per kiekvieną laiko intervalą. Pavyzdžiui, įveskite **1**, **2**, **3** ar bet kokį kitą sveiką skaičių.
- **Aktyvios dienos** – Nurodykite savaitės dienas, kai atsiėmimo laiko vieta yra veikianti. Ši ypatybė leidžia prekeiviui nustatyti dienas, kai jis nori palaikyti atsiėmimo užsakymus.
- **Mažmeniniai kanalai** – Nurodykite mažmeninius kanalus. Visos laiko vietos gali būti susietos su viena ar keliomis mažmenos parduotuvėmis. Priklausomai nuo kiekvienos parduotuvės darbo valandų, vienas ar daugiau laiko vietų gali būti sukurti ir susieti su kanalu. 

<!-- ![HQ Timeslot overview.](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

Tik vienas laiko vietos šablonas gali būti konfigūruojamas kanalui. Šie kanalai apima fizines parduotuves, skambučių centrus, mobiliuosius įrenginius ir el. prekybos svetaines.

## <a name="configure-the-time-slot-feature-in-commerce-headquarters"></a>Konfigūruokite laiko vietos funkciją „Commerce“ štabe

Laiko vietos turi būti nustatytos kiekvienam atsiėmimo pristatymo būdui „Commerce“ štabe taip, kad pardavimo taškas ir e-komercijos kanalai į juos rodytų.

- Tik vienas laiko tarpo šablonas gali būti susietas su kiekviena parduotuve ar kanalu.
- Kiekviena laiko vieta, kuri yra sukurta, turi būti unikali kiekvienam pristatymo būdui kiekviename šablone.
- Po to, kai laiko vietos funkcija sukonfigūruota, laiko vietos kalendorius bus prieinamas pasirinktoms parduotuvėms ar jų grupėms. Jis taip pat matomas POS nuorodai.

Norėdami konfigūruoti laiko vietos funkciją „Commerce“ štabe, atlikite šiuos žingsnius.

1. Eikite į **„Commerce“** \> **Kanalo nustatymai** \> **Atsiėmimo parduotuvėje laiko vieta**.
1. Rinkitės **Naujas** tam, kad sukurtumėte naują laiko vietos šabloną. Norėdami naudoti esamą šabloną, pasirinkite šabloną kairiojoje srityje.
1. Įverskite vertes  **Laiko vietos ID** ir **Aprašo** laukelius.
1. „FastTab“**Užsakymo atsiėmimas - Laiko nustatymai** rinkitės **Įtraukti**.
1. Teksto laukelyje **Užsakymo atsiėmimas - Laiko nustatymai** nustatykite datos intervalą, pristatymo būdą, veikiančias pristatymo valandas, veikiančias dienas, laiko vietos intervalą, vietas vienam intervalui ir kitus nustatymus.

    Jei laiko vietos bus statiškos numatytai ateičiai, nustatykite **Pabaigos datos** laukelį į **Niekada**.

    > [!NOTE]
    > Galite sukurti keletą šablonų, tačiau tik vienas gali būti susietas su vienu kanalu ar parduotuve.

    ![Užsakymo atsiėmimas - Laiko nustatymų teksto laukelis.](../dev-itpro/media/Curbside_timeslot_Settings_Page.PNG)

1. Pabaigus, rinkitės **Gerai**.
1. Jei laiko vietos per dieną gali skirtis, sukurkite papildomus įrašus **Užsakymo atsiėmimas - Laiko nustatymai** „FastTab“ tam, kad užtikrintumėte, jog datos ir laikai nepersidengtų.
1. „FastTab“ **Prekybos kanalai** rinkitės **Įtraukti** tam, kad susietumėte laiko vietos šabloną su parduotuvėmis ar kanalais, kuriuose jie bus naudojami.
1. Teksto laukelyje **Rinktis organizacijos mazgus** naudokite rodyklių mygtukus, kad pasirinktumėte (ar panaikintumėte pasirinktas) parduotuves, regionus ir organizacijas, su kuriomis šablonas bus susietas.

    <!-- ![HQ Timeslot overview.](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

1. Pabaigus, rinkitės **Gerai**.
1. Puslapyje **Paskirstymo grafikas** vykdykite **1070** ir **1135** darbus taip, kad sinchronizuotumėte datą su kanalais.

## <a name="time-slot-selection-for-pos-orders"></a>Laiko vietos pasirinkimas POS užsakymams

POS, užsakymą ar užsakymo eilutę nustačius atsiėmimui, kasininkas gali pasirinkti atsiėmimą parduotuvėje ar vietoje ir laiką bei laiko vietą. Jei klientas turi kitos parduotuvės paėmimo užsakymą, kasininkas gali pasirinkti datas, kada toje parduotuvėje bus galima paimti prekes. Parduotuvių peržvalgoje bus pateikta nuoroda į datas ir parduotuvių darbo laiką.

Tolesnis paveikslėlis rodo laiko vietos pavyzdžio pasirinkimą POS užsakymui.

![Laiko vietos pasirinkimo pavyzdys POS užsakymui.](../dev-itpro/media/Curbside_timeslot_POS.png)

## <a name="time-slot-selection-for-e-commerce-orders"></a>Laiko vietos pasirinkimas e-komercijos užsakymams

Dėl informacijos, kaip padaryti laiko vietos pasirinkimą prieinamą e-komercijos užsakymams, žr. [Atsiėmimo informacijos modulis](../pickup-info-module.md).

> [!NOTE]
> Vartotojai gali peržiūrėti ar redaguoti atsiėmimo laiko vietas „Commerce“ svetainės išsiregistravimo puslapyje tik, jei atsiėmimo informacijos modulis buvo įtrauktas į tą puslapį. Jei išsiregistravimo puslapis neapima atsiėmimo informacijos modulio, užsakymai bus padaromi neleidžiant vartotojams nurodyti ar peržiūrėti laiko vietos informacijos.

Tolesnis paveikslėlis rodo laiko vietos pavyzdžio pasirinkimą e-komercijos užsakymui, kai atsiėmimo laiko vieta buvo pasirinkta.

![Elektroninės prekybos užsakymo pavyzdys, kai atsiėmimo laiko vieta buvo pasirinkta.](../dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="time-slot-selection-for-call-center-orders"></a>Laiko vietos pasirinkimas skambučių centro užsakymams

Jei skambučių centro programa, skambučių centro agentai gali pasirinkti atsiėmimo parduotuvę ar vietą, taip pat kaip datos ir vietos laiką kaip parodyta tolesniame paveikslėlyje.

![Skambučių centro užsakymo pavyzdys, kai atsiėmimo laiko vieta buvo pasirinkta.](../dev-itpro/media/Curbside_timeslot_callcenter.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Paėmimo informacijos modulis](../pickup-info-module.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]