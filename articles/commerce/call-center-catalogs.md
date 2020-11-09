---
title: Skambučių centro katalogai
description: Šioje temoje aprašyta konkreti skambučių centro funkcija, skirta katalogams „Dynamics 365 Commerce“.
author: josaw1
manager: AnnBe
ms.date: 05/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9abe493746719d2e229ef09c2eb5f436b91b2171
ms.sourcegitcommit: 776758a0ff95c3c7398986095104d1d2b9814514
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/24/2020
ms.locfileid: "4107284"
---
# <a name="call-center-catalogs"></a>Skambučių centro katalogai

[!include [banner](includes/banner.md)]

Šioje temoje aprašyta konkreti skambučių centro funkcija, susieta su katalogo galimybėmis „Dynamics 365 Commerce“.

„Commerce“ pateiktas katalogo funkcijas galima naudoti keliais tikslais. Iš pradžių katalogo funkcijos buvo sukurtos trečiosios šalies „e-Commerce“ integravimams palaikyti. Katalogo sąranka leido įmonėms kurti produktų ir atributų, kuriuos galima paskelbti išoriškai, kad juos vartotų trečiosios šalies „e-Commerce“ sprendimas, grupes.

Įtraukus skambučių centro kanalo palaikymą, katalogo koncepcija buvo išplėsta įtraukiant papildomų palaikymo galimybių ir valdymo funkcijų, susijusių su įprastais tiesioginės vartotojo rinkodaros katalogais. Tiesioginio vartotojo įmonė dažnai gamins spausdintus katalogus, kurie vėliau bus siunčiami vienam ar keliems klientų segmentams. Šiuose kataloguose paprastai bus skelbiamos konkrečios akcijos ar pasiūlymai, kurie bus apmokėti tik tada, jei klientas užsakymo kūrimo metu pateiks katalogo identifikacijos kodą.

Tiesioginės vartotojo rinkodaros įmonės visą dėmesį teikia sekdamos atsakymus į šiuos katalogus, kad užtikrintų, jog gamybos ir siuntimo išlaidos bus pagrįstos. Kad atsakymą būtų galima sekti, paprastai ant katalogo nugarėlės atspausdinamas kodas, kurio bus prašoma ir kuris bus naudojamas, kai katalogo gavėjas telefonu pateiks užsakymą (dabar kodą paprastai galima įvesti klientui užsakymą pateikus internetu). Nors šiam kodui identifikuoti naudojama keletas pramonėje vartojamų sąvokų (įskaitant sąvokas „raktinis kodas“, „reklaminis kodas“, „katalogo kodas“, „šaltinio kodas“), šį kodą „Commerce“ vadinsime **Šaltinio kodo ID**.

## <a name="basic-catalog-setup"></a>Pagrindinio katalogo sąranka

Eikite į **Mažmeninė prekyba ir prekyba** \> **Katalogai ir asortimentai** \> **Visi katalogai** ir sukonfigūruokite savo katalogą.

Sukūrę naują katalogą pirmiausia turite jį susieti su vienu ar keliais kanalais. Tą galima atlikti „FastTab“ skirtuke **Prekybos kanalai** , kuris pateiktas formoje **Katalogo sąranka**. Spustelėkite **Įtraukti** ir pasirinkite vieną ar kelis kanalus. Kuriant katalogą galima naudoti tik su jūsų pasirinktu kanalu susietus elementus [asortimentus](https://docs.microsoft.com/dynamics365/unified-operations/retail/assortments).

Norint įtraukti produktus į katalogą, reikia pasirinkti naršymo hierarchiją. Naršymo hierarchija palaikys katalogo kategorijos struktūrą. Turite išsirinkti vieną iš naršymo hierarchijų, susietą su kanalais, pasirinktą „FastTab“ skirtuke **Prekybos kanalai** , pateikiamą puslapyje **Katalogas**. Jei naršymo kanalas anksčiau su kanalu susietas nebuvo, eikite į parinktį **Mažmeninė prekyba ir prekyba** \> **Kanalo sąranka** \> **Kanalo kategorijos ir produkto atributai** , kad susietumėte numatytąją naršymo hierarchiją su savo kanalais.

Meniu skirtuke **Katalogai** , pateikiamame puslapyje **Katalogo sąranka** , spustelėkite **Įtraukti produktų** ir sukonfigūruokite produktus, kurios reikia įtraukti į katalogą, arba pasirinkite mazgą naršymo hierarchijoje (pasirinkus mazgą bus pakeista ekrano pateiktis ir leista produktus įtraukti tiesiai į katalogo kategoriją).

Spustelėkite viršutinį katalogo hierarchijos mazgą, kad grįžtumėte į pagrindinį katalogo antraštės rodinį. Jei reikia, „FastTab“ skirtuke **Bendra** sukonfigūruokite įsigaliojimo ir galiojimo pabaigos datas.

Kad katalogu galėtumėte naudotis, prieš tai jį reikia paskelbti. Spustelėkite parinktį **Tikrinti katalogą** , pateikiamą meniu **Katalogai** , kad apdorotumėte tikrinimą. Šį veiksmą atlikti būtina, o jį atlikus bus patikrinta, ar reikiama sąranka atlikta tiksliai. Norėdami pamatyti tikrinimo duomenis, spustelėkite parinktį **Peržiūrėti rezultatus**. Jei randama klaidų, duomenis turite pataisyti ir patikrinimą kartoti tol, kol jis bus atliktas sėkmingai.

Patvirtinę patikrinimą, meniu spustelėkite parinktį **Darbo eiga** ir pradėkite patvirtinimo darbo eigą. Spustelėkite parinktį **Pateikti** , pateiktą srityje **Darbo eiga** , ir įvykdykite procesą. Darbo eigos veiksmus ir įgaliotus vartotojus konfigūruokite parinktyje **Mažmeninė prekyba ir prekyba** \> **Būstinės sąranka** \> **Prekybos darbo eigos**. Darbo eigoje bus apibrėžti veiksmai, reikalingi tam, kad katalogo būsena būtų pakeista į **Patvirtinta**. Kai kataloge bus nustatyta būsena **Patvirtinta** , galėsite spustelėti parinktį **Publikuoti** , pateiktą meniu **Katalogai** , ir užbaigsite procesą. Kai kataloge bus nustatyta būsena **Paskelbta** , galėsite jį naudoti skambučių centro užsakymo įvedimo srityje bei katalogo procesams siųsti.

## <a name="use-catalogs-to-drive-sales-order-pricing-and-promotions"></a>Katalogų naudojimas pardavimo užsakymo kainoms ir akcijoms didinti valdyti

Katalogą apibrėžti naudojant jį kartu su skambučių centru iš esmės reikia tam, kad būtų galima sukonfigūruoti konkrečias kainas ir akcijas, skirtas tam katalogui. Iš šio katalogo užsakymus atliekantiems klientams nurodytos kainos ir akcijos skambučių centro užsakymo įvedimo srityje bus taikomos tada, jei į katalogo **šaltinio kodo ID** bus taikomas užsakymo antraštei arba eilutėms.

Norėdami sukonfigūruoti konkrečias katalogo kainas, pasirinkite parinktį **Kainų grupės** , pateiktą skirtuke **Katalogai** , kad su dialogu susietumėte vieną ar daugiau kainų grupių. Visos prekybos sutartys, kainos koregavimo žurnalai ir papildomos nuolaidos (ribinė reikšmė, kiekis, prekių rinkinys), susietos su ta pačia kainų grupe, bus taikomos, kai klientai užsakymus atliks iš šio katalogo.

„FastTab“ skirtuke **Šaltinio kodai** spustelėkite **Įtraukti** ir įtraukite į šį katalogą vieną ar kelis **šaltinio kodo ID** identifikatorius. Tai kodas, kuris bus taikomas skambučių centre įvedant užsakymą pardavimo užsakymo antraštėje (ir eilutėse). Šis kodas naudojamas pardavimo užsakymui su katalogu ir galiausiai su kainų grupėmis bei specialiomis sukonfigūruotomis kainomis ir akcijomis susieti.

## <a name="use-the-source-id-to-track-costs-and-response-rates"></a>Šaltinio ID naudojimas išlaidoms ir atsakymų greičiui sekti

Apibrėždami **šaltinio kodo ID** pasirinktinai galite susieti šį ID su **tikslinės rinkos ID**. **Tikslinės rinkos ID** galima apibrėžti parinktyje **Mažmeninė prekyba ir prekyba** \> **Klientai** \> **Tikslinė rinka**. Tikslinė rinka – tai klientų ir (arba) potencialių klientų, priklausančių vartotojo apibrėžtam segmentui, sąrašas. Susiejus kliento arba potencialaus kliento duomenis su šaltinio kodo ID, galima padidinti katalogo gavėjų matomumą. Jei klientas yra susietas su tiksline rinka, o ta tikslinė rinka yra susieta su aktyviu šaltinio kodo ID / katalogu, kokius katalogus klientas gavo skambučių centro vartotojai galės matyti pasirinkę meniu parinktį **Šaltinio kodai** , esančią meniu skirtuke **Klientai** , puslapyje **Klientų aptarnavimas**. Įvedant užsakymą, skambučių centro vartotojai užsakymo įvedimo antraštėje pasirinkę išplečiamąjį sąrašą **Šaltinis** taip pat gali matyti specialius katalogus, kurie buvo išsiųsti klientui. Pakeitus filtrą iš **Visi** į **Tiksliniai** vartotojas galės matyti konkrečius aktyvius katalogus, kurie buvo išsiųsti klientui. Tai naudinga tose situacijose, kai klientas galimai pamiršta savo katalogą ar negali jo rasti arba nuskaityti katalogo kodo, kai raginama sukurti pardavimo užsakymą.

Su katalogu galima susieti kelis šaltinio kodo ID. Paprastai to reikia, kai įmonė nori sekti atsakymų greitį pagal skirtingus segmentus. Įmonės suteiks unikalų katalogo kodą skirtingiems kliento segmentams, kas leis sekti atsakymų greitį iki pat segmento lygio vykstant tam tikram katalogo įvykiui.

Pasirinkus tam tikrą **šaltinio kodo ID** įrašą ir spustelėjus parinktį **Informacija** , „FastTab“ skirtuke **Šaltinio kodai** bus pateikta papildomų laukų, kuriuose bus galima užfiksuoti pardavimo projekcijas, siuntimo išlaidas ir siuntimo datas. Šie duomenys bus naudingi atliekant išsamią katalogo efektyvumo analizę. Vartotojai gali grįžti į šį puslapį per tam tikrą laiką ir pasinaudoję mygtukais **Šaltinio kodo analizė** bei **Palyginti akcijas** paleisti analizės ataskaitas, pagrįstas dabartiniais pardavimo duomenimis, ir palyginti išlaidų bei biudžeto sumas su faktinėmis.

## <a name="configure-catalog-specific-order-and-item-scripts"></a>Užsakymas iš konkretaus katalogo ir prekės scenarijai

Kai skambučių centre kuriamas pardavimo užsakymas, galima naudoti ekrane pateiktus scenarijus. Šiuose tekstiniuose scenarijuose gali būti pateikta papildoma informacija, kurią vartotojas turi pranešti klientui, arba tai gali būti vidinės pastabos / priminimai, kuriuos skambučių centro vartotojas turi peržiūrėti ir į jas atitinkamai reaguoti, kai kuriamas pardavimo užsakymas.

Dažnai naudinga turėti skirtingus scenarijų rinkinius skirtingiems katalogams. „FastTab“ skirtuke **Scenarijai** iš anksto apibrėžtus scenarijus galima susieti su katalogu. Pasinaudokite lauku **Laikas** ir nustatykite, ar scenarijus bus rodomas užsakymo pradžioje (vos tik šaltinio kodo ID bus įvestas užsakymo antraštėje), ar užsakymo pabaigoje (pardavimo užsakymo suvestinės formoje).

Katalogo hierarchijoje pasirinkę mazgą ir dirbdami su duomenimis, pateiktais „FastTab“ skirtuke **Produktai** , vartotojai pasinaudodami veiksmu **Scenarijai** taip pat gali susieti konkrečius katalogų arba prekių scenarijus.

## <a name="configure-catalog-specific-up-sell-and-cross-sell-items"></a>Konkrečiame kataloge pateiktų papildomo / kryžminio pardavimo prekių konfigūravimas

Susieti papildomo / kryžminio pardavimo pasiūlymus su preke galima produktų sąrankoje, bet kai kuriais atvejais įmonė gali panorėti reklamuoti specialias papildomo / kryžminio pardavimo prekes klientams, užsisakantiems konkretų produktą iš konkretaus katalogo. „FastTab“ skirtuke **Produktai** pasirinkite prekę ir spustelėkite **Papildomo / kryžminio pardavimo prekės** , kad klientams, perkantiems pasirinktą prekę iš katalogo, produktus sukonfigūruotumėte kaip parduodamus papildomai arba kryžminiu būdu. Įvedant skambučių centro užsakymą, konkretaus katalogo papildomo / kryžminio pardavimo prekės bus rodomas ekrane vietoje įprastų papildomo / kryžminio pardavimo produktų, kurie tai prekei buvo sukonfigūruoti atlikus įprastą produkto konfigūraciją.

Papildomo / kryžminio pardavimo prekės taip pat gali pasižymėti scenarijų funkcijų privalumais, kad būtų rodomi konkretūs pranešimai, kuriuos vartotojas matys, kai įvedant užsakymą bus rodomos papildomo / kryžminio pardavimo prekės. Scenarijai, susieti su papildomo / kryžminio pardavimo produktais ir sukonfigūruoti specialiai pagal katalogo produktą, bus rodomi tik tada, kai to katalogo šaltinio kodas bus taikomas skambučių centre įvedant užsakymą.

## <a name="catalog-page-analysis"></a>Katalogo puslapio analizė

Skirtuke **Katalogai** naudojantis pateiktomis parinktimis galima sukonfigūruoti funkciją **Katalogo puslapiai**. Ši funkcija leidžia apibrėžti konkrečius spausdinto katalogo puslapius ir puslapių tipus bei susijusias išlaidas.

Produktų kataloge konfigūruodami produktus, naudokite veiksmą **Produkto puslapio maketas** ir apibrėžkite konkrečius puslapius, puslapių procentą bei puslapyje apie prekę pateiktos informacijos padėtį. Sukonfigūravus šiuos duomenis vartotojai galės pasinaudoti ataskaitos **Katalogo srities analizės ataskaita** teikiamomis galimybėmis. Šią ataskaitą rasite apsilankę parinktyje **Mažmeninė prekyba ir prekyba** \> **Skambučių centro ataskaitos** \> **Katalogo srities analizės** ataskaita. Šioje ataskaitoje analizuojami pardavimai, vykdomi kataloge (pardavimo užsakymai, kuriuose katalogo šaltinio ID buvo susietas su užsakymo antrašte ar eilute) ir su juo susietas puslapių ir išlaidų procentas, kad būtų galima pateikti įprastą tiesioginės rinkodaros ataskaitą **Kvadratinio colio analizė**.

## <a name="catalog-requests"></a>Katalogo užklausos

Kadangi katalogai konfigūruojami ir skelbiami „Commerce“, galima pasinaudoti funkcija **Siųsti katalogą**. Ši funkcija pasiekiama puslapiuose **Kliento ieška** ir **Klientų aptarnavimas**. Pasirinkę kliento įrašą per sritį **Kliento ieška** arba peržvelgdami pasirinktą kliento sąskaitą srityje **Klientų aptarnavimas** , vartotojai gali pasirinkti parinktį **Siųsti katalogą** , kuria pasinaudojus bus atidarytas dialogo langas ir vartotojas galės rinktis iš paskelbtų ir aktyvių katalogų sąrašo. Vartotojas gali pasirinkti siųsti katalogą ir kiekį bei konkretų šaltinio kodo ID. Spustelėjus mygtuką **Siųsti** užklausa bus išsaugota, todėl ja vėliau bus galima pasinaudoti spausdinant ataskaitą į **Katalogo užklausos**. Šią ataskaitą rasite apsilankę parinktyje **Mažmeninė prekyba ir prekyba** \> **Skambučių centro ataskaitos** \> **Katalogo užklausų ataskaita**. Joje bus pateiktos visos katalogo užklausos, įskaitant kliento, pateikusio katalogo užklausą, vardo, pavardės ir adreso informaciją. Šią ataskaitą galima naudoti viduje arba duomenis galima perduoti trečiajai šaliai, kuri palaiko išorinius procesus, naudojamus tada, kai katalogas klientui siunčiamas faktiškai.

## <a name="additional-features"></a>Papildomos funkcijos

Skirtuke **Katalogai** taip pat pasiekiamos parinktys, skirtos **mokėjimo grafikui** ir **nemokamiems produktams** konfigūruoti. Jei su katalogu susietas šaltinio kodo ID taikomas skambučių centre vedant užsakymą, klientas galės įsigyti nemokamų produktų arba, kaip apibrėžta, pasinaudoti specialiais katalogo mokėjimo grafikais. Jei reikia taikyti apribojimą, kad klientas galėtų rinktis tik iš mokėjimo grafikų, susietų su savo katalogu, o ne iš visų aktyvių sistemoje esančių mokėjimo grafikų, ties vienu arba keliais šaltinio kodo ID, kuriems reikia taikyti apribojimą, galite pasirinkti žymės langelį **Leisti tik katalogo planus**.

## <a name="additional-notes"></a>Papildomos pastabos

Tuo metu, kai šaltinio kodo ID taikomas skambučių centro pardavimo užsakymui, jis naudojamas nustatant kainas, akcijas, scenarijus ir papildomą / kryžminį pardavimą, būdingą konkrečiam katalogui. Sistema nedraus ir leis pardavimo užsakyme užsakyti produktą, kurio nėra kataloge. Jei užsakoma prekė, kuri nepriklauso tam katalogui, sistema prekės kainai arba akcijoms pirmiausia taikys tą **kainų grupę** , kuri apibrėžta skambučių centro kanale ( **Mažmeninė prekyba ir prekyba** \> **Kanalai** \> **Skambučių centrai** \> **Visi skambučių centrai** ). Jei konkreti kanalo kaina nerandama, bus taikoma bazinė prekės pardavimo kaina.
