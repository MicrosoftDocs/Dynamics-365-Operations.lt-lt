---
title: Kainos parametrai
description: Šiame straipsnyje aprašomi įvairūs būstinės kainos ir nuolaidos valdymo Microsoft Dynamics 365 Commerce parametrai.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-11
ms.openlocfilehash: 4bc8cb16e7960d26adbb9590b4ad83cf46b02838
ms.sourcegitcommit: 6fd44fc6e9a7bad197cab58c36ec25a555724cf1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410475"
---
# <a name="pricing-settings"></a>Kainos parametrai

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šiame straipsnyje aprašomi įvairūs būstinės kainos ir nuolaidos valdymo Microsoft Dynamics 365 Commerce parametrai. Šie parametrai įgalina organizacijas apibrėžti kainodaros elgseną jų "Commerce" sprendimu, kad būtų patenkinti konkretūs verslo poreikiai.

## <a name="company-level-pricing-settings"></a>Įmonės lygio kainodaros parametrai

Dauguma kainų parametrų yra įmonės lygyje, o " **Commerce Headquarters" galima rasti "Commerce \> " parametruose Kainos** ir nuolaidos.

### <a name="best-price-and-compound-concurrency-control-model"></a>Geriausios kainos ir jungimo nuolaidų vienalaikiškumo valdymo modelis

Geriausia **kaina ir sudėtinis sukainojimo** kontrolės modelio parametras nustato, kaip kainodaros variklis apdoroja kelias **nuolaidas** **geriausios** kainos ar sudėtiinio sukainojimo režimu. 

Jei parametras nustatytas **kaip Geriausia kaina ir sudėtinis prioritetas,** niekada nededa į prioritetų sudėtinis kiekius, visos sudėtiniai nuolaidos, **kurių** kainų prioritetas toks pats, yra sudedamos. Tada sudėtinis rezultatas **konkuruoja** su visomis geriausios kainos nuolaidomis, kurių prioritetas toks pats, taikoma geriausia kaina, o visų nuolaidų, kurių prioritetas žemesnis, nepaisoma.

Jei parametras nustatytas kaip Geriausia kaina tik **prioritete, visada** sudėsite prioritetus, **visos** sudėtinės nuolaidos yra laikomos **geriausiomis kainų** nuolaidomis. Pagal kainos prioritetą laimėti tik viena nuolaida. Jei ta viena nuolaida yra **geriausia** **kaina** arba sudėtinė nuolaida, ji sudedama su visomis papildomomis kainomis arba sudėtinomis nuolaidomis, kurių kainų prioritetas žemesnis.**·** **·**

### <a name="discount-compound-behavior"></a>Nuolaidų jungimo būdas

**Nuolaidų sudėties veikimo** būdo parametras nustato, kaip kainodaros variklis apskaičiuoja keletą sudėtinės nuolaidos nuolaidų.

Jei parametras nustatytas kaip **Sudėtinis**, viena nuolaida kaupiamuoju būdu taikoma kita nuolaida. Jei originalioje kaina nustatyta **Sudėtinis** mokestis, visos nuolaidos apdorojamos nepriklausomai viena nuo kitos ir taikomos tai pačiai prad nurodytai kainai.

Pavyzdžiui, norite sudėti 10 procentų nuolaidas ir 20 procentų nuolaidas produktui, kurio pradinė kaina yra $100. Jei nuolaidų sudėtinio **veikimo parametrą** **nustatote** kaip Sudėtinis, galutinė kaina bus $72 (100 90&times;% 80% &times; USD). Jei pradinę **kainą** nustatote kaip Sudėtinis, galutinė kaina bus $70 (100 USD – $10 – $20).

### <a name="enable-competition-between-exclusive-threshold-and-other-periodic-discounts"></a>Įjungti išimtinės ribinės vertės ir kitų laikotarpio nuolaidų konkurencijos teisę

Jei nustatyta išimtinės **ribinės vertės ir kitų periodinių nuolaidų parametro konkurentas Įgalinti, kainų sistema nustato išimtines ribines** **nuolaidos** vertes esant išimtinėms ne ribinėms nuolaidoms. Vis dar taikomas kainos prioritetas. Išlieka ir geriausios **kainos bei** sudėtinės **ribinės** nuolaidos veikimo būdas. Kitaip tariant, jie nekonkuruoja su nuolaidos verte, kurios nėra slenkstis.

### <a name="manual-line-discount-and-system-discount"></a>Rankiniu būdu įvedamos eilutės nuolaida ir sistemos nuolaida

Rankiniu **būdu nustatomos eilutės nuolaidos ir sistemos** nuolaidos nuostatos nustato, kaip kainų variklis tai pačiai eilutei taiko rankiniu būdu nustato eilutės nuolaidą ir sistemos nuolaidą. Neautomatiniu būdu eilutės nuolaidą galima sudėti sistemos nuolaidos viršuje arba pakeisti sistemos nuolaidą. Kai neautomatiniu būdu sudeda eilutės nuolaidą ir sistemos nuolaidą, skaičiavimo logika atitinka nuolaidos sudėties **veikimo būdo parametrą**. Bendra rankiniu būdu taikoma nuolaida, taikoma visam užsakymui, neatitinka to parametro.

### <a name="keep-items-on-the-same-sales-line-for-discount-price-rounding"></a>Laikykite prekes toje pačioje pardavimo eilutėje, kad būtų suapvalinta nuolaidos kaina

Kartais kiekio nuolaidos sumos negalima lygiai padalinti iš tinkamumo kiekio (pvz., jei nuolaidos suma yra $10 trijų nupirktų vienetų). Tokiais atvejais, prekių **išlaikyti** prekes toje pačioje pardavimo eilutėje, kad kainos nuolaidos apvalinimo parametras nustato, kaip taikomas kainodaros variklis ir paskirsto nuolaidos sumą. Jei parametras nustatytas kaip **Taip**, nuolaidos suma taikoma visa ir nėra išskaidyta. Jei nustatyta Ne, nuolaidos **suma** padalijama tinkamumo kiekiui ir apvalinama. Pavyzdžiui, $10 vieneto nuolaidos suma padalinta į $3.33 vienetui, $3.33 į antrąjį vienetą ir $3.34 trečio vieneto nuolaida.

### <a name="apply-discounts-to-key-in-price-products"></a>Taikyti nuolaidas raktui kainos produktuose

Taikomos **nuolaidos raktui** kainos produktų parametruose nustato, ar nuolaidas galima taikyti kartu su "klaviatūra įvedamos kainos", kurios įvedamos į kasos metodą (EKA). Produkto **konfigūracijos kainos** nustatymo raktas nurodo, ar produktas palaiko kainą, į9-100.

### <a name="apply-discounts-to-price-overrides"></a>Taikyti nuolaidas kainos perrašymams

Kainos **perrašymo parametrui taikomos nuolaidos** nurodo, ar nuolaidas galima taikyti kartu su kainų perrašymais.

### <a name="distribute-discounts-for-least-expensive-discounts"></a>Paskirstyti nuolaidas pigiausioms nuolaidoms

Nuolaidos prekių iš prekių sutapti, kurios naudoja skaičiavimo tipą "pigiausia", parametre Paskirstyti nuolaidas pigiausioms nuolaidoms nustatoma, **ar** kainos variklis paskirsto nuolaidą eilutėms.

Jei parametras nustatytas kaip **Ne**, nuolaida taikoma tik pigiausioms eilutėms. Pvz., jei "2 pirkti" nuolaida yra "gauti 1 nemokamą" nuolaidas, pigiausia prekė bus nemokama, o kitos dvi prekės liks už visą kainą. Tokiu atveju klientas, kuris grąžina abi prekes už visą kainą, vis tiek nemokamai gaus trečiąją prekę. Dėl šio scenarijaus mažmenininkas gali prarasti.

Jei parametras nustatytas kaip **Taip**, kainos variklis paskirsto nuolaidą visose taikomose eilutėse. Šis parametras gali padėti sumažinti grąžinimų nuostolius.

### <a name="manually-calculate-multi-line-prices-and-discounts"></a>Rankiniu būdu apskaičiuoti kelių eilučių kainas ir nuolaidas

Rankiniu **būdu skaičiuojant kelių eilučių kainas ir nuolaidų nustatymus nustatoma, ar kainos variklis** naudoja EKA programos ir skambučių centro kanalo atidėtos kainos ir nuolaidos skaičiavimą. Jei parametras **nustatytas** kaip Taip, kainos nustatymo sistema ne iš karto apskaičiuoja kelių eilučių nuolaidas (pvz., kiekio nuolaidas, ribines nuolaidas ir nuolaidos prekių kiekiui), kai EKA programoje arba skambučių centro kanale kuriamas arba redaguojamas pardavimo užsakymas.

> [!NOTE]
> Naudojant "Commerce" 10.0.30 ir ankstesnę versiją kelių **eilučių** kainų ir nuolaidų parametrų nustatymas valdo tik skambučių centro kanalą. Atskiras rankiniu **būdu skaičiuokite kelių** prekių nuolaidų parametrą funkcijų šablone, valdysite kainų apskaičiavimo būdą EKA programoje. "Commerce" versijoje 10.0.31 du parametrai yra konsoliduoti į vieną įmonės lygio parametrą.

### <a name="retention-period-in-days"></a>Užlaikymo laikotarpis dienomis

Užlaikymo **laikotarpis** dienomis nurodo, kiek dienų turi būti po galiojimo datos (jei nustatyta galiojimo data) arba nuo uždraustos datos (jei galiojimo data nėra nustatyta), kiek dienų nuolaida turėtų būti sistemiškai panaikinta. Jei parametras nustatytas kaip **0** (nulis), automatiškai nebus ištrinta.

> [!NOTE]
> Naudojant "Commerce" 10.0.30 ir ankstesnę versiją šis parametras pavadinimu "Dienų skaičius", **po kurių nebegaliojanti nuolaida turi būti panaikinta**.

### <a name="coupon-bar-code"></a>Kupono brūkšninis kodas

Kupono **brūkšninio kodo** parametras nurodo, kuris konkretus brūkšninis kodas naudojamas kupono brūkšniniams kodams generuoti. Vartotojai gali pasirinkti vieną iš anksto apibrėžtų brūkšninių kodų, kurie sukonfigūruoti brūkšninio **kodo nustatymo** puslapyje. Daugiau informacijos apie brūkšninius kodus ir brūkšninių kodų skaičių skaičių sekos rasite [Brūkšninių kodų](set-up-bar-codes.md) nustatymas [ir Brūkšninių kodų skaičių sekos nustatymas](set-up-bar-code-masks.md).

### <a name="coupon-code-must-be-manually-applied-to-return-transactions"></a>Kupono kodas turi būti taikomas neautomatiškai grąžinimo operacijoms

Kupono **kodas turi būti taikomas rankiniu būdu grąžinimo operacijų parametrui** taikomas tik grąžinimo operacijoms, kurios nebuvo pateiktos pardavimo kvitui. Nustatykite parametrą Ne **,** jei kupono kodai turėtų būti automatiškai taikomi operacijai. Nustatykite ją kaip **Taip,** jei kupono kodus reikia įtraukti į operaciją rankiniu būdu.

### <a name="use-sales-agreements-set-up-for-the-organization"></a>Naudoti organizacijai nustatytas pardavimo sutartis

Jei nustatyta organizacijos parametro "verslas verslui" (B2B) **·** **užsakymų pardavimo sutarčių naudojimas, nustatytas kaip Taip**, kainodaros variklis naudoja pardavimo sutartis, kurios nustatomos organizacijai vartotojo klientų hierarchijoje, kad nustatytų kaina pagal sutartį. Jei parametras nustatytas **kaip Ne** arba jei kliento hierarchija nėra nustatyta, kainos variklis ieško pardavimo sutarčių, kurios nustatytos vartotojui, kad nustatytų kainą pagal sutartį. Daugiau informacijos apie B2B [el. komercijos klientų hierarchijas ieškokite B2B verslo partnerių valdymas naudojant klientų hierarchijas](b2b/partners-customer-hierarchies.md).

## <a name="channel-level-pricing-settings"></a>Kanalo lygio kainodaros parametrai

Toliau pateikti parametrai įgalina organizacijas valdyti kainodaros elgseną konkrečiuuose pardavimo kanaluose.

### <a name="enable-order-price-control"></a>Įgalinti užsakymo kainos kontrolę

Parametras **Įgalinti užsakymo kainos** kontrolę yra iškvietimų **centro** konfigūracijos puslapio bendrajame **"** FastTab". Parametras nustato, ar kainos variklis nustato kainos perrašymo operacijos apribojimą skambučių centro kanale. Jis veikia kartu su parametru **Leisti koreguoti** kainą produkto lygiu.

Jei užsakymo kainos valdymas išjungtas, bet kuris skambučių centro vartotojas gali keisti kainą skambučių centro kanalo pardavimo eilutėse, nepaisant to, ar atitinkami produktai leidžia koreguoti kainą.

Jei užsakymo kainos valdymas įjungtas, tik produktai, **·** **kurių parametras Leisti koreguoti kainą nustatytas kaip Taip**, leidžia perrašyti kainą skambučių centro kanalo pardavimo užsakymuose, o priežasties kodas turi būti nurodytas atitinkamose pardavimo eilutėse. Skambučių centro vartotojas **gali** **pakeisti pardavimo kainą tik iki savikainos antkainio procento vertės, kuri nustatyta "Retail" ir "Commerce \> Channel \>" nustatymo skambučių centro \> nustatymo nepaisymo teisės.** Jei kainos perrašymo suma viršija šį procentą, vartotojas turi pateikti užklausą, kuri tada bus apdorota naudojant iš anksto nustatytą "Commerce" darbo eigą peržiūrai ir patvirtinimui. Daugiau informacijos apie "Commerce Workflows", žr. darbo [eigos sistemos peržiūrą](/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system).

## <a name="product-level-pricing-settings"></a>Produkto lygio kainodaros parametrai

Toliau nurodyti parametrai produkto lygiu taikomos kainodaros taisyklės, randama organizacijos produkto **konfigūracijos** puslapyje.

### <a name="allow-price-adjust"></a>Leisti koreguoti kainą

Jei parametras **Leisti koreguoti kainą** nustatytas kaip **Taip**, kainos perrašymo galima taikyti skambučių centro kanalo pardavimo užsakymų produktui.

### <a name="key-in-price"></a>Įvesti kainą

Kainos **nustatymo raktas nustato**, ar pagrindinė kaina yra privaloma, kai produktas įtraukiamas į EKA pardavimo operaciją. Ji taip pat apibrėžia atitinkamus kainos vertės apribojimus.

### <a name="zero-price-valid"></a>Nulinė kaina tinkama

Nulinis **kainos galiojantis** parametras nurodo, ar iš anksto nustatytos, sistemos apskaičiuotos, ar rankiniu būdu pakoreguotos produkto pardavimo kainos gali būti 0 (nulis). Nustatykite parametrą **Taip**, jei leidžiama nulinė kaina. Šį parametrą taip pat galima nurodyti "Commerce" produktų hierarchijos kategorijų lygyje.

### <a name="prevent-all-discounts"></a>Neleisti jokių nuolaidų

Nustačius parametrą **Uždrausti visas nuolaidas** **kaip Taip**, visų tipų nuolaidos (įskaitant neautomatines nuolaidas) neleidžiama taikyti produktui. Šį parametrą taip pat galima nurodyti "Commerce" produktų hierarchijos kategorijų lygyje.

> [!NOTE]
> Šis parametras neapriboja kainos perrašymo operacijos, nes ši operacija nustato kainą ir nėra laikomas nuolaida.

### <a name="prevent-manual-discounts"></a>Neleisti rankiniu būdu įvedamų nuolaidų

Nustatydami parametrą **Uždrausti rankiniu būdu taikomas nuolaidas** **kaip Taip**, eilutės ar operacijų nuolaidų rankiniu būdu negalite taikyti produktui. Vis dar galima taikyti visas kitas nuolaidas. Šį parametrą taip pat galima nurodyti "Commerce" produktų hierarchijos kategorijų lygyje.

> [!NOTE]
> Šis parametras neapriboja kainos perrašymo operacijos, nes ši operacija nustato kainą ir nėra laikomas nuolaida.

### <a name="prevent-retail-discounts"></a>Neleisti mažmeninės prekybos nuolaidų

Jei parametras Neleisti mažmeninės prekybos nuolaidų nustatytas **kaip** Taip, **paprastas**, **kiekis**,**ribinė** vertė, **·** **nuolaidos** prekių kiekiui ir gabenimo nuolaidos negali būti taikomos produktui.**·** Visas kitas nuolaidas (įskaitant neautomatines nuolaidas) vis tiek galima taikyti.

### <a name="prevent-tender-based-discounts"></a>Neleisti mokėjimo priemone grindžiamų nuolaidų

Jei parametras **Uždrausti mokėjimo priemones pagrįstas nuolaidas** **nustatytas** kaip Taip, **produktui** negalima taikyti mokėjimo priemonės nuolaidos. Visas kitas nuolaidas (įskaitant neautomatines nuolaidas) vis tiek galima taikyti.

Mažmenininkai dažnai pasirenka neįtraukti kai kurių produktų, pvz., naujų prekių arba prekių pagal poreikį, iš prekių nuolaidų (pvz., paprastos nuolaidos ir kiekio nuolaidos). Tačiau, jei klientas sumoka naudodamas pageidaujamą mokėjimo priemonė, vis tiek gali norėti taikyti mokėjimo priemonėje taikomas nuolaidas, pagal kurias mokama. Norėdami pasiekti šį rezultatą **mažmenininkai** **gali nustatyti parametrą Neleisti naudoti visų nuolaidų ir Neleisti naudoti mokėjimo priemonių nuolaidų parametrų kaip Ne** **·** **ir** Apsaugokite mažmeninės prekybos nuolaidas **ir** apsaugokite rankiniu būdu nustatomų nuolaidų parametrus kaip **Taip.**

## <a name="deprecated-or-removed-settings"></a>Pasenusi arba pašalinti parametrai

Šie kainos nustatymai yra pašalinti arba suplanuoti pašalinti Dynamics 365 Commerce.

| Parametras | Nurašimo arba šalinimo priežastis | Apeikvojimo arba šalinimo būsena |
|---------|-----------------------------------|-------------------------------|
| Persidengiančių nuolaidų tvarkymas | "Commerce" parametruose pateikėme šį parametrą, kad galėtume valdyti, kaip kainų nustatymo variklis ieško ir nustato geriausią nuolaidų kombinaciją, kurią reikia taikyti. Pasirinktis **Geriausia** nuolaida galioja skaičiuojant kainą, naudojant visas galimas nuolaidų kombinacijas. Geriausio **našumo** pasirinktis yra optimizuota pasirinktis, naudojanti heuristic algoritmą ir ribinės vertės vertinimo metodą, siekiant nustatyti prioritetą, įvertinti ir nustatyti geriausią derinį laiku. Kodų **pagrindo subalansuotų** skaičiavimų pasirinktis veikia taip pat kaip **našumui užtikrinti**. Todėl iš esmės tai yra pasikartojanti pasirinktis. Siekiant padidinti našumą, kainos nustatymo variklis atnaujintas taip, kad jis turėtų tik **geriausią našumą kaip** standartinę pasirinktį. Todėl šis parametras nebetaiko naudojamas. | Pasenusi 10.0.21 leidime ir bus pašalinta 2022 m. spalio mėn. |
| Leisti koreguoti kainą, kad būtų padidinta produkto kaina | Pateikėme šį parametrą, kad kontroliuojame, ar kainos koregavimo funkcija gali padidinti produkto kainas. Jei parametras išjungtas, organizacijos gali naudoti kainos koregavimo funkciją tik produkto vieneto kainai nustatyti, kad ji būtų mažesnė už bazinę kainą ir prekybos sutarties pardavimo kainą. Mes pasenusiai įtraukėme šį parametrą, nes kainos koregavimo funkcija buvo atnaujinta taip, kad palaiko dvi savaites atliekamus koregavimus (padidėjimą ar sumažėjimą) langelyje. | Naudotas 10.0.30 leidime ir bus pašalintas 2023 m. spalio mėn. |
| Įgalinti parduotuvės kainų ataskaitą | Mes pateikėme šį parametrą, kad galėtume **valdyti**, ar kainos ataskaitos funkciją galima naudoti parduotuvės konfigūravimo puslapyje. Mes pasenusiai įtraukėme šį parametrą, nes parduotuvės konfigūravimo puslapis buvo atnaujintas taip, kad visada **pateikia kainos** ataskaitą kaip standartinę funkciją. | Naudotas 10.0.31 leidime ir bus pašalintas 2023 m. spalio mėn. |
| Skaičiuojant kainas naudoti šiandienos datą | Kainų Dynamics 365 Supply Chain Management nustatymo sistema palaiko kainos skaičiavimą, pagrįstą pageidaujama siuntimo data arba pageidaujama gavimo data kartu su šiandienos data. "Commerce Pricing" modulis palaiko tik šiandienos data pagrįstus kainų skaičiavimus. Klientams, kurie naudoja tiekimo grandinės valdymo ir komercijos galimybes, **pateikėme** šį parametrą ir rekomenduojama, kad klientai visada jį nustatytų kaip Taip, kad du kainų sistemų klientai galėtų veikti kartu. Nuvertinime šį parametrą, nes jis iš esmės nekeičia skaičiavimo veikimo būdo, todėl jis yra perteklinis. | Naudotas 10.0.31 leidime ir bus pašalintas 2023 m. spalio mėn. |
| Maksimali kaina | Šį parametrą pateikėme funkcijų šablone, kad galėtume valdyti, ar tik produktus, kurių pardavimo kaina yra mažesnė už nurodytą maksimalią kainą, galima parduoti per EKA konkrečiose parduotuvėse. Dėl mažos funkcijų naudojimo nuvertinsime šį parametrą. | Naudotas 10.0.31 leidime ir bus pašalintas 2023 m. spalio mėn. |
| Taikomos kainos nuolaidos | Šis parametras buvo skirtas valdyti, ar kainos ir nuolaidos suapvalintos vieneto kainos lygyje arba pardavimo eilutės lygyje, skaičiuojant kainą. Mes jį pasenusiame, nes jo nereikia naudoti bet kurioje dabartinio kodo pagrindo vietoje. | Naudotas 10.0.31 leidime ir bus pašalintas 2023 m. spalio mėn. |
| Rankiniu būdu skaičiuoti kelių prekių nuolaidas | Pateikėme šį parametrą, kad kontroliuojame, ar kainų modulis naudoja mažmeninės prekybos kanalo atidėtų kainų skaičiavimą. Jei parametras **nustatytas kaip Taip**, kainos nustatymo sistema ne iš karto apskaičiuoja kelių eilučių nuolaidas (pvz., kiekio nuolaidas, ribines nuolaidas ir nuolaidos prekių kiekiui), kai EKA programoje kuriamas arba redaguojamas pardavimo užsakymas. Nusprendėme konsoliduoti šį parametrą naudojant panašius "Commerce" parametrų nustatymus, kad būtų galima atlikti kanalų valdiklį. | Naudotas 10.0.31 leidime ir bus pašalintas 2023 m. spalio mėn. |

Visas pašalintų arba pasenusių funkcijų sąrašas pateikiamas, žr Dynamics 365 Commerce. Pašalintos [arba pasenusios funkcijos, kurios yra .Dynamics 365 Commerce](get-started/removed-deprecated-features-commerce.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
