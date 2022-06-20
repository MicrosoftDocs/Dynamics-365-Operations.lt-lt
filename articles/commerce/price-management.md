---
title: Mažmeninės prekybos pardavimo kainos valdymas
description: Šiame straipsnyje aprašomos pardavimo kainų kūrimo ir valdymo koncepcijos Dynamics 365 Commerce.
author: ShalabhjainMSFT
ms.date: 07/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16c948e6e14309f4e340bf622fac42b14e6ee591
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887015"
---
# <a name="retail-sales-price-management"></a>Mažmeninės prekybos pardavimo kainos valdymas

[!include [banner](includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie pardavimo kainų kūrimo ir valdymo procesą Dynamics 365 Commerce. Pagrindinis dėmesys skiriamas šio proceso apimamoms koncepcijoms ir įvairių konfigūravimo parinkčių poveikiui pardavimo kainoms.

## <a name="terminology"></a>Terminologija

Šiame straipsnyje naudojami tokie terminai.

| Semestras | Apibrėžimas, naudojimas ir pastabos |
|---|---|
| Kaina | Suma, už kurią parduodamas vienas produkto vienetas elektroninio kasos aparato (EKA) kliento programoje arba pardavimo užsakyme. Šiame straipsnyje terminas kaina *visada* nurodo pardavimo kainą, o ne atsargų kainą ar savikainą. |
| Bazinė kaina | Kaina, kuri nustatoma išleisto produkto lauke **kaina**. |
| Prekybos sutarties kaina | Kaina, nustatyta produktui arba jo variantui pagal **Kaina (pardavimai)** tipo prekybos sutartį. |
| Geriausia kaina | Kai produktui galima pritaikyti daugiau nei vieną kainą arba nuolaidą, tai yra mažiausia kainos suma ir (arba) didžiausia nuolaidos suma, sudaranti mažiausią įmanomą grynąją sumą, kurią turi mokėti klientas. Šiame straipsnyje geriausios kainos sąvoka visada vadinama "geriausia kaina". Ši geriausia kaina skiriasi nuo ir neturėtų būti painiojama su **Geriausios kainos** išvardijimo verte, taikoma nuolaidos sutapimo režimui. |

## <a name="price-groups"></a>Kainų grupės

Kainų grupės yra kainų ir nuolaidų valdymo pagrindas „Commerce“. Kainų grupės yra naudojamos priskiriant kainas ir nuolaidas „Commerce“ prekybos objektams (t. y. kanalams, katalogams, priskyrimams ir lojalumo programoms). Kainų grupės naudojamos visoms kainoms ir nuolaidoms, todėl prieš pradedant labai svarbu suplanuoti, kaip jas naudosite.

Pati savaime kainų grupė yra tik pavadinimas, aprašymas ir, pasirinktinai, kainodaros prioritetas. Svarbiausia, ką reikėtų atsiminti apie kainų grupes, yra tai, kad jas naudojant yra valdomi įvairūs ryšiai, kurie nuolaidas ir kainas sieja su prekybos „Commerce“ objektais.

Toliau pateikta iliustracija parodo, kaip naudojamos kainų grupės. Atkreipkite dėmesį, kad šioje iliustracijoje „Kainų grupė“ yra tiesiogine to žodžio prasme kainų ir nuolaidų valdymo centre. „Commerce“ objektai, kuriais galite valdyti skirtingas kainas ir nuolaidas, yra kairėje, o patys kainų ir nuolaidų įrašai yra dešinėje.

![Kainų grupės.](./media/PriceGroups.png "Kainų grupės")

Kuriant kainų grupes, nereikėtų naudoti vienos kainų grupės kelių tipų „Commerce“ objektams. Antraip gali būti sunku nustatyti, kodėl operacijai taikoma būtent tokia kaina ar nuolaida.

Raudona punktyrinė linija iliustracijoje rodo, kad „Commerce“ palaiko pagrindinę „Microsoft Dynamics 365“ kainų grupės, nustatomos tiesiogiai klientui, funkciją. Tačiau šiuo atveju gaunate tik pardavimo kainos prekybos sutartis. Jei norite taikyti konkretaus kliento kainas, nerekomenduojame kainų grupes nustatyti tiesiogiai klientui. Vietoje to reikėtų naudoti priskyrimus. 

Turėkite omenyje, kad jei kainos grupė nustatyta klientui, šios kainų grupės bus susietos su šiam klientui sukurtų užsakymų pardavimo užsakymo antrašte. Jei vartotojas pakeičia kainos grupę užsakymo antraštėje, senoji kainos grupė bus pakeista naująja kainos grupe tik dabartiniam užsakymui. Pavyzdžiui, senoji kainos grupė neturės įtakos dabartiniam užsakymui, bet vis dar bus susieta su klientu būsimiems užsakymams.

Tolesniuose skyriuose pateikiama daugiau informacijos apie „Commerce“ objektus, kuriais galite nustatyti skirtingas kainas, kai naudojamos kainų grupės. Kainų ir nuolaidų sukonfigūravimas visiems šiems objektams yra dviejų veiksmų procesas. Šiuos veiksmus galima atlikti bet kuria tvarka. Tačiau logiška tvarka yra pirma nustatyti kainų grupes objektams, nes tikėtina, kad šis veiksmas bus vienkartinis nustatymas, atliekamas diegimo metu. Tada, sukūrus kainas ir nuolaidas, galima nustatyti kainų grupes atskiroms kainoms ir nuolaidoms.

### <a name="channels"></a>Kanalai

Prekybos sektoriuje yra labai įprasta skirtinguose kanaluose nustatyti skirtingas kainas. Du pagrindiniai veiksniai, darantys įtaką konkrečių kanalų kainoms, yra išlaidos ir vietos rinkos sąlygos.

- **Išlaidos** – kuo toliau kanalas yra nuo produkto šaltinio, tuo daugiau kainuoja tą produktą sandėliuoti. Pvz., švieži maisto produktai gali būti laikomi ribotą laiką ir jiems taikomi specialūs gamybos reikalavimai (pvz., augimo sezonas). Tikėtina, kad žiemą šviežios salotos kainuos daugiau šiaurės klimato šalyse nei pietų klimato šalyse. Jei reikia nustatyti kainas platesnėje geografinėje zonoje veikiantiems kanalams, tikriausiai norėsite nustatyti skirtingas kainas skirtinguose kanaluose.
- **Vietos rinkos sąlygos** – parduotuvė, kuri turi tiesioginį konkurentą kitoje gatvės pusėje bus daug jautresnė kainai nei parduotuvė, kuri šalia neturės tiesioginio konkurento.

### <a name="affiliations"></a>Priskyrimai

Bendras priskyrimo apibrėžimas yra ryšys arba sąsaja su grupe. „Commerce“ priskyrimais vadinamos klientų grupės. Priskyrimai yra daug lankstesnė priemonė kainų ir nuolaidų taikymui klientams nei pagrindinė „Microsoft Dynamics 365“ klientų grupės ir nuolaidos grupės koncepcija. Visų pirma, priskyrimą galima taikyti ir kainoms, ir nuolaidoms, o ne mažmeninėje prekyboje kiekvieno tipo kaina ir nuolaida turi atskirą grupę. Be to, klientas gali priklausyti keliems priskyrimams, bet tik vienai kiekvieno tipo ne mažmeninės prekybos kainų grupei. Galiausiai, nors priskyrimus galima nustatyti ir taip, kad jie būtų susieti su klientu, tačiau tai nėra būtina. EKA pagalba, anoniminiams vartotojams galima taikyti ad hoc priskyrimą. Tipinis anoniminio priskyrimo nuolaidos pavyzdys yra nuolaida senjorams arba studentams, kai klientas gali gauti nuolaidą tiesiog parodęs grupės narystės kortelę.

Priskyrimai dažniausiai siejami su nuolaidomis, tačiau jų pagalba galite taikyti ir kainų diferencijavimą. Pvz., kai mažmeninis pardavėjas parduoda darbuotojui, jis gali norėti pakeisti pardavimo kainą užuot pritaikęs nuolaidą įprastai kainai. Kitas pavyzdys – mažmeninis pardavėjas, kuris parduoda tiek privatiems, tiek verslo klientams, verslo klientams gali pasiūlyti geresnes kainas priklausomai nuo jų perkamo kiekio. Priskyrimai leidžia taikyti abu minėtus scenarijus.

### <a name="loyalty-programs"></a>Lojalumo programos

Kainų ir nuolaidų prasme lojalumo programos iš esmės yra tik priskyrimas, turintis specialų pavadinimą. Lojalumo programai, kaip ir priskyrimui, galima nustatyti ir kainas, ir nuolaidas. Tačiau tai, kaip klientai operacijos ar užsakymo metu gauna lojalumo kainas, skiriasi nuo to, kaip jie gauna priskyrimo kainas. Klientai gali gauti lojalumo kainas tik jei į operaciją yra įtraukta lojalumo kortelė. Į operaciją įtraukus lojalumo kortelę, įtraukiama ir lojalumo programa. Tada lojalumo programa leidžia pritaikyti specialias kainas ir nuolaidas.

Lojalumo programos gali turėti kelias pakopas, o skirtingose pakopose gali būti skirtingos nuolaidos. Tokiu būdu mažmenininkai dažniems klientams gali suteikti didesnį atlygį ir tam nereikės rankiniu būdu šių klientų įtraukti į specialią grupę.

Be kainų ir nuolaidų, lojalumo programos turi ir kitų funkcijų. Tačiau, kainų ir nuolaidų požiūriu, tai yra tas pats kaip ir priskyrimai.

### <a name="catalogs"></a>Katalogai

Kai kurie mažmenininkai naudoja fizinius arba virtualius katalogus, kuriuose reklamuoja produktus ir nustato jų kainas tam tikroms klientų grupėms. Įvairiuose savo kataloguose šie mažmenininkai gali taikyti kainų diferencijavimą kaip savo tikslinės rinkodaros per katalogą verslo modelio dalį. „Microsoft Dynamics 365“ palaiko šią funkciją leisdama nustatyti konkrečiam katalogui taikomas nuolaidas ir kainas – lygiai taip pat, kaip ir nustatant konkrečiam kanalui arba konkrečiam priskyrimui taikomas nuolaidas. Redaguodami katalogą, galite su katalogu susieti kainų grupes, kaip kad jas galite susieti su kanalu, priskyrimu ar lojalumo programa.

### <a name="best-practices-for-price-groups"></a>Geriausia kainų grupių praktika

Nenaudokite vienos kainų grupės kelių tipų objektams. Vietoje to, naudokite vieną kainų grupių rinkinį kanalams, kitą kainų grupių rinkinį priskyrimams arba lojalumo programoms ir t. t. Galite naudoti priešdėlį arba priesagą kainų grupės pavadinime, kad vizualiai sugrupuotumėte savo naudojamas įvairių tipų kainų grupes.

Venkite kainų grupę nustatyti tiesiogiai klientui. Vietoje to, naudokite priskyrimą. Tokiu būdu klientams galite priskirti visų tipų kainas ir nuolaidas, o ne vien pardavimo kainos prekybos sutartis.

## <a name="pricing-priority"></a>Kainodaros prioritetas

Pats kainodaros prioritetas yra tik skaičius ir aprašymas. Kainodaros prioritetai gali būti taikomi kainų grupėms arba tiesiogiai nuolaidoms. Naudojant kainodaros prioritetus, jie leidžia mažmenininkui nepaisyti geriausios kainos principo ir kontroliuoti, kuria tvarka produktams bus taikomos kainos ir nuolaidos. Aukštesnis kainodaros prioriteto numeriui teikiama pirmenybė prieš žemesnį kainodaros prioriteto numerį. Be to, jei kaina ar nuolaida turi kokį nors prioriteto numerį, visos žemesnius prioriteto numerius turinčios kainos ir nuolaidos bus ignoruojamos.

Kaina ir nuolaida gali būti taikoma pagal du skirtingus kainodaros prioritetus, nes kainodaros prioritetai kainoms ir nuolaidoms yra taikomi atskirai.

Norėdami kainodaros prioritetą taikyti kainoms, kainų grupei turite priskirti kainodaros prioritetą, o tada tai kainos grupei sukurti pardavimo kainos prekybos sutartį.

Kainodaros prioriteto funkcija buvo įvesta tam atvejui, jei mažmenininkas tam tikrose parduotuvėse norėtų taikyti aukštesnes kainas. Pvz., mažmenininkas nustatė JAV Rytų pakrantei nustatė regionines kainas, bet kai kuriems produktams Niujorko parduotuvėse nori taikyti aukštesnes kainas, nes šiame mieste kai kuriuos produktus parduoti kainuoja brangiau ir (arba) vietinė rinka sugebės pakelti aukštesnę kainą.

Kaip aprašyta šio straipsnio skyriuje "Geriausia kaina", kainos modulis paprastai pasirenka mažesnę nei dvi kainas. Todėl mažmenininkas paprastai negali taikyti aukštesnės iš dviejų kainų parduotuvėje, turinčioje ir Rytų pakrantės, ir Niujorko kainų grupes. Norėdamas išspręsti šią problemą, kai dar nebuvo įvesta kainodaros prioriteto funkcija, mažmenininkas kainas kiekvienam produktui turėjo nurodyti du kartus ir turėjo nepriskirti abiejų kainų grupių. Arba mažmenininkas turėjo sukurti papildomų kainų grupių, kad atskirtų aukštesnes kainas turinčius produktus nuo produktų, kurie turi įprastas žemesnes kainas.

O štai kainodaros prioriteto funkcija mažmenininkui leidžia parduotuvės kainoms sukurti kainodaros prioritetą, kuris yra aukštesnis už regioninių kainų kainodaros prioritetą. Arba mažmenininkas gali sukurti kainodaros prioritetą tik parduotuvių kainoms, o regioninėms kainoms palikti numatytąjį kainodaros prioritetą, kuris yra 0 (nulis). Abu nustatymai padeda užtikrinti, kad parduotuvių kainos visada turės pirmenybę prieš regionines kainas.

### <a name="pricing-priority-example"></a>Kainodaros prioriteto pavyzdys

Pažiūrėkime į pavyzdį, kur parduotuvių kainoms taikoma pirmenybė prieš kitas kainas.

Nacionalinis mažmenininkas daugumą kainų nustato pagal regioną, o regionų yra keturi: Šiaurės Rytų, Pietryčių, Vidurio Vakarų ir Vakarų. Jis nustatė keletą brangių rinkų, kurios gali pakelti didesnes kainas. Šios rinkos yra Niujorkas, Čikaga ir San Francisko įlankos regionas.

Šiame pavyzdyje bandysime įsigilinti į Šiaurės Rytų regioną. 1 parduotuvė yra Bostone, o 2 parduotuvė – Manhetene. Su Bostono parduotuvės kanalu yra susietos dvi kainų grupės: Šiaurės Rytų ir 1 parduotuvės. Su Manheteno parduotuvės kanalu yra susietos trys kainų grupės: Šiaurės Rytų, Niujorko ir 2 parduotuvės.

Mažmenininkas nustato du kainodaros prioritetus: didelės išlaidos turi prioriteto numerį 5, o parduotuvės kainos turi prioriteto numerį 10. (Atminkite, kad pagal numatytąjį nustatymą kainodaros prioritetas yra 0 \[nulis\], o aukštesnį prioriteto numerį turinti kaina ar nuolaida yra taikoma prieš žemesnio prioriteto numerio kainą ar nuolaidą.) Šiaurės Rytų kainų grupei yra palikta numatytoji kainodaros prioriteto vertė **0** (nulis). Niujorko kainų grupei yra nustatyta kainodaros prioriteto vertė **5**, nes Niujorkas yra brangi rinka. 1 ir 2 parduotuvių kainų grupėms nustatytas kainodaros prioritetas yra **10**.

Mažmenininkas parduoda du produktus: 1 produktą – marškinėlius, ir 2 produktą – madingus konkretaus prekės ženklo džinsus.

| Produktas | Šiaurės Rytų kaina | Niujorko kaina | Parduotuvės kaina |
|---|---|---|---|
| Marškinėliai | 15 $ | Nenustatyta | Nenustatyta |
| Madingi džinsai | 50 $ | 70 $ | Nenustatyta |

Marškinėliai parduodami už tą pačią kainą (t. y., 15 $) ir Bostono, ir Manheteno parduotuvėse, nes Šiaurės Rytų kainų grupėje nustatyta tik viena kaina, kuri yra susieta su abiem kanalais. Madingi džinsai Bostono parduotuvėje parduodami už 50 $, nes ta kaina yra vienintelė, kurią galima taikyti toje parduotuvėje. Tačiau Manheteno parduotuvėje galimos dvi kainos: 50 $ ir 70 $. Niujorko kainodaros prioriteto vertė 5 yra aukštesnė už Šiaurės Rytų kainų grupės kainodaros prioriteto vertę 0 (nulis), todėl EKA sistemoje bus taikoma 70 $ kaina.

> [!NOTE]
> Kiekvienam kainodaros prioritetui reikalingas pilnas perėjimas per mažmeninės prekybos kainodaros mechanizmo logiką. Todėl, norint išlaikyti kainų ir nuolaidų skaičiavimo efektyvumą, kainodaros prioritetus reikėtų naudoti saikingai.

## <a name="types-of-prices"></a>Kainų tipai

„Microsoft Dynamics 365“ produkto kainą galite nustatyti trijose vietose:

- Tiesiogiai produktui (bazinė kaina)
- Pardavimo kainos prekybos sutartyje
- Kainos koregavime

Bazinė kaina ir prekybos sutarties kaina yra pagrindinės „Dynamics 365“ dalys ir yra prieinamos, net jei nesinaudojate „Commerce“. Kainų koregavimo funkcija galima tik „Commerce“. Kitame skyriuje pateikta daugiau informacijos apie kiekvieną iš šių kainos nustatymo parinkčių ir yra paaiškinta, kaip šios parinktys veikia kartu.

## <a name="setting-prices"></a>Kainų nustatymas

### <a name="base-price"></a>Bazinė kaina

Lengviausia produkto kainą nustatyti yra tiesiogiai konkrečiam produktui. Vertė, kurią nustatote tiesiogiai produktui, dažnai vadinama bazine produkto kaina. Bazinę kainą galima nustatyti puslapio **Išleisto produkto informacija** skirtuko **Parduoti** lauke **Kaina**. Jūsų įvesta vertė rodoma bendrovės valiuta. Pagal numatytuosius nustatymus, kaina yra nurodyta už 1 matavimo vienetą, kurį galima nustatyti skirtuko **Parduoti** lauke **Vienetas**. Faktinė produkto vieneto kaina priklauso nuo matavimo vieneto, kainos kiekio ir valiutos.

Jei produkto kaina visiems yra vienoda, bazinė kaina yra efektyviausias būdas valdyti šio produkto kainą. Net jei kainoms nustatyti naudojate prekybos sutartis, taip pat galite nustatyti bazinę produkto kainą. Tada, jei nenorite naudoti **Visos** prekybos sutarties, turite atsarginę kainą, kuri naudojama, kai prekybos sutartis nėra taikoma.

Jei kanalo valiuta skiriasi nuo įmonės valiutos, bazinė to kanalo kaina nustatoma konvertuojant nustatyto produkto kainos valiutą.

Nors kainos vieneto atvejų pasitaiko retai, kainodaros mechanizmas jį palaiko. Jei yra nustatyta kita kainos kiekio vertė nei **0** (nulis), vieneto kaina yra lygi Kaina ÷ Kainos vienetas. Pvz., jei produkto kaina yra 10,00 $, o kainos vienetas yra 50, 1 vieneto kaina yra 0,20 $ (= 10,00 $ ÷ 50).

### <a name="sales-price-trade-agreement"></a>Pardavimo kainos prekybos sutartis

Naudodami prekybos sutarčių žurnalą, galite kurti kiekvieno produkto pardavimo kainos prekybos sutartis. „Microsoft Dynamics 365“ yra trys klientų aprėptys, taikomos pardavimo kainos prekybos sutartims: **Lentelė**, **Grupė** ir **Visos**. Klientų aprėptis nustato, kuriems klientams bus taikoma atitinkama pardavimo kainos prekybos sutartis.

**Lentelės** pardavimo kainos prekybos sutartis yra skirta vienam klientui, kuris nustatomas tiesiogiai prekybos sutartyje. Tai nėra įprastas verslas–vartotojui (B2C) scenarijus. Tačiau jei taip atsitinka, kainodaros mechanizmas, nustatydamas kainą, naudoja prekybos sutartis **Lentelė**.

**Grupės** pardavimo kainos prekybos sutarties tipas yra dažniausiai naudojamas. Išorės „Commerce“, **Grupės** pardavimo kainos prekybos sutartys yra skirtos paprastai klientų grupei. Tačiau „Commerce“ klientų grupės sąvoka platesnė, jai priskiriama bendresnė kainų grupė. Kainų grupę galima susieti su kanalu, priskyrimu, lojalumo programa ar katalogu. Išsamesnės informacijos apie kainų grupes žr. ankstesniame šio straipsnio skyriuje "Kainų grupės".

> [!NOTE]
> Prekybos sutarties kaina visada naudojama prieš bazinę kainą.

### <a name="price-adjustment"></a>Kainos koregavimas

Kaip galima suprasti iš pavadinimo, kainos koregavimas yra skirtas keisti kainą, kuri buvo nustatyta tiesiogiai produktui arba nustatyta naudojant prekybos sutartį. Kainos koregavimą galima naudoti tik kainai sumažinti, ne jai padidinti. Kainos koregavimas rekomenduojamas mažmenininkams norint kurti, sekti ir valdyti savo produktų kainos sumažinimus per tam tikrą laiką.

Kainos koregavimai būna trijų tipų: procentinis sumažinimas, suminis sumažinimas ir kainos. Vykdant pardavimo operaciją, visada taikomas procentinio sumažinimo arba suminio sumažinimo kainos koregavimo tipas. Tačiau kainos tipo kainos koregavimas yra taikomas tik tada, jei pakoreguota kaina yra mažesnė už kainą, kuri buvo nustatyta naudojant bazinę kainą arba prekybos sutarties kainą. Todėl, jei pakoreguota kaina viršija nekoreguotą kainą, kainos koregavimas nėra naudojamas.

## <a name="determining-price-for-a-product-in-a-transaction"></a>Produkto kainos nustatymas atliekant operaciją

Skaičiuojant kainą ir nuolaidą operacijos metu, taikomas geriausios kainos klientui principas. Pagal šį principą, jei yra daugiau nei viena kaina, naudojama mažiausia iš jų. Be to, naudojamas toks nuolaidų derinys, kuris suteikia didžiausią nuolaidos sumą visai operacijai. Kai kuriais atvejais vienam produktui turi būti taikoma mažesnė nuolaida, kad būtų galima pritaikyti papildomas nuolaidas kitiems operacijos produktams.

Vienintelė geriausios kainos klientui principo išimtis yra galimybė taikyti nuolaidą prekių rinkiniui pagal pigesnes nuolaidas. Ši galimybė leidžia taikyti mažmenininkui palankias pigesnes nuolaidas, kai produktai yra pasirinkti ir sugrupuoti. Todėl kai sandoris apima daugiau produktų, nei reikalaujama norint gauti pigiausią nuolaidą, kainodaros mechanizmas parenka produktus, kurie klientui sukuria mažiausią įmanomą nuolaidos sumą.

Kainodaros mechanizmas grąžina tris kiekvieno produkto kainas: bazinę kainą, prekybos sutarties kainą ir aktyvią kainą.

Bazinė kaina yra tiesiog produkto ypatybė visiems visur yra vienoda.

Pardavimo kainos prekybos sutartyje, jei parinkčiai **Rasti kitą** yra nustatyta vertė **Taip**, kaip prekybos sutarties kaina yra naudojama mažiausia rasta taikytinų pardavimo kainos prekybos sutarčių kaina. Prekybos sutartis galima rasti pagal kainų grupes arba paskyros kodą **VISOS**. Taip pat prekybos sutartis galima priskirti tiesiogiai klientui. Jei parinkčiai **Rasti kitą** nustatyta vertė **Ne**, naudojama pirmoji rasta prekybos sutarties kaina. Jei pardavimo kainos prekybos sutarčių nerandama, tuomet prekybos sutarties kaina nustatoma lygi bazinei kainai.

Aktyvi kaina apskaičiuojama prekybos sutarties kainai pritaikant didžiausią kainos koregavimą, kurį galima pritaikyti atitinkamam produktui. Jei kainos koregavimų nerasta, arba jei apskaičiuota aktyvi kaina yra didesnė nei prekybos sutarties kaina, aktyvi kaina prilyginama prekybos sutarties kainai. Atminkite, kad kainos koregavimu negalima padidinti produkto kainos. Taikytinus kainos koregavimus galima rasti naudojant tik tas kainų grupes, kurios yra priskirtos kanalui, katalogui, priskyrimui ar lojalumo programai.

## <a name="category-price-rules"></a>Kategorijos kainų taisyklės

Kategorijos kainų taisyklių funkcija „Commerce“ leidžia lengvai sudaryti naujas prekybos sutartis su visais šios kategorijos produktais. Ši funkcija taip pat leidžia automatiškai rasti esamas kategorijos produktų prekybos sutartis ir nutraukti jų galiojimą.

Pasirinkus esamų prekybos sutarčių galiojimo nutraukimą, sistema sukuria naują prekybos sutarčių žurnalą toje produktų kategorijoje, kuri turi aktyvią prekybos sutartį. Tačiau žurnalas turi būti užregistruojamas rankiniu būdu. Be to, kategorijos kainų taisyklės gali rasti esamas prekybos sutartis tik tada, jei naudojate tokią pačią kainų taisyklę (t. y., jei sukuriate naują kainų taisyklę, kuri naudoja tą pačią kategoriją kaip ir prieš tai). Jei nenaudojate tokios pačios kainų taisyklės, esamų prekybos sutarčių galiojimas nebus nutrauktas.

Kainas galima padidinti ar sumažinti naudojant kategorijos kainų taisyklių laukus **Kainų taisyklė** ir **Kainos pagrindas**.

- Lauke **Kainų taisyklė** pasirinkite, kokio tipo kainos pokytį naudoti:

    - **Antkainis** – kainos pagrindo procentas, naudojamas pardavimo kainai apskaičiuoti. Pvz., produktas, kuris kainuoja 10,00 ir yra parduodamas už 15,00, turi 50 procentų antkainį.
    - **Marža** – pelno sumai apskaičiuoti naudojamas pardavimo kainos procentas. Pvz., produktas, kuris kainuoja 10,00 ir yra parduodamas už 15,00, turi 33,3 procentų maržą.
    - **Fiksuota suma** – prie kainos pagrindo pridedama suma, naudojama pardavimo kainai apskaičiuoti. Pvz., produkto, kuris kainuoja 10,00 ir yra parduodamas už 15,00, fiksuota suma yra 5,00.

- Lauke **Kainos pagrindas** pasirinkite norimos keisti kainos tipą:

    - **Bazinė savikaina** – tiekėjui mažmenininko sumokėta suma.
    - **Bazinė kaina** – pardavimo kaina prieš pritaikant prekybos sutartis ir kainos koregavimus.
    - **Dabartinė kaina** – pardavimo kaina pritaikius prekybos sutartis ir kainos koregavimus.

Norėdami nesunkiai atnaujinti įvairių produktų iš skirtingų produktų kategorijų kainas, galite naudoti papildomas produktų kategorijas kartu su kategorijos kainų taisyklėmis.

## <a name="best-practices"></a>Geriausia praktika

Kanalų duomenų bazėse dažnai naudojama „Microsoft SQL Server Express“ dėl nedidelių kaštų (nemokama). Atminkite, kad „SQL Server Express“ turi aparatūros apribojimų ir duomenų dydžio limitų. Tinkamai nesuplanavus, galima greitai pasiekti „SQL Server Express“ duomenų dydžio limitus. Tai galioja ne tik kainodarai, bet ir kitoms produkto sritims. Štai keletas geriausios praktikos pavyzdžių, kurie gali padėti sumažinti duomenų dydį:

- Jei naudojate prekybos sutartis ir jūsų kainos pasikeičia, senų prekybos sutarčių galiojimą reikėtų nutraukti nustačius jų pabaigos datą. Laikui bėgant, šis metodas padeda sumažinti kanalų duomenų bazėse laikomų prekybos sutarčių skaičių. Tai taip pat padeda sumažinti kiekį duomenų, kuriuos turi apdoroti kainos skaičiavimo algoritmas.
- Jei kainos skiriasi priklausomai nuo produkto varianto, apsvarstykite galimybę naudoti produkto bazinę kainą kaip labiausiai įprastą kainos variantą. Tuomet prekybos sutartis naudokite tik tiems kainų variantams, kurie yra išimtys. Šis metodas padeda sumažinti prekybos sutarčių įrašų skaičių. Importuoti duomenis į „Microsoft Dynamics 365“ yra labai paprasta, todėl gali kilti pagunda kiekvienam kiekvieno produkto variantui importuoti po atskirą prekybos sutartį. Tačiau dėl to bus sukurta daug prekybos sutarčių, kurios turi tą pačią vertę. Todėl tai gali bereikalingai padidinti duomenų dydį.
- „Commerce“ apdoroja su variantais susijusias kainas nuo konkrečiausios iki mažiausiai konkrečios. Jei produkto dimensija neturi poveikio kainai, jai nereikės nustatyti prekybos sutarčių. Pvz., produktas būna trijų spalvų ir keturių dydžių, bet kaina skiriasi tik pagal dydį. Jei kiekvienam variantui nustatysite po prekybos sutartį, sukursite 12 įrašų. Vietoje to, galite nustatyti prekybos sutartį tik kiekvienam dydžiui, o spalvos dimensiją palikti tuščią. Tokiu atveju sukursite tik keturis įrašus.

    Arba, jei ne kiekviena dimensijos vertė lemia skirtingą kainą, galite nustatyti vieną prekybos sutartį bendrajam produktui ir visas produkto dimensijas palikti tuščias. Tada nustatykite po atskirą prekybos sutartį tik toms dimensijos vertėms, kurios lemia skirtingą kainą. Pvz., jei XXL dydis kainuoja brangiau, bet visi kiti dydžiai kainuoja tiek pat, jums reikės tik dviejų prekybos sutarčių: vienos bendrajam produktui ir vienos XXL dydžiui.

## <a name="prices-that-include-tax-vs-prices-that-exclude-tax"></a>Kainos su mokesčiais ir kainos be mokesčių

Kai nustatote pardavimo kainas „Dynamics 365“, jūs nenurodote, ar į nustatomą kainos vertę įskaičiuojami mokesčiai. Vertė yra tiesiog kaina. Tačiau parametras **Į kainą įtrauktas PVM**, esantis kanaluose, leidžia konfigūruoti kanalus taip, kad į kainas būtų įtraukiamas arba neįtraukiamas mokestis. Šis parametras nustatomas kanale ir gali skirtis net toje pačioje įmonėje.

Jei dirbate ir su mokesčius apimančiomis ir neapimančiomis kainomis, labai svarbu teisingai nustatyti kainas, nes, pakeitus kanalo parametrą **Kaina su PVM**, bendra kliento mokama suma bus skirtinga.

## <a name="differences-between-commerce-pricing-and-non-commerce-pricing"></a>Skirtumai tarp mažmeninės „Commerce“ kainodaros ir ne mažmeninės „Commerce“ kainodaros

Kainų apskaičiavimui visais kanalais naudojamas vienas kainodaros mechanizmas: Skambučių centras, Mažmeninė parduotuvė ir Internetinės parduotuvės. Tai padeda taikyti suvienodintus „Commerce“ scenarijus.

Kainodara skirta dirbti su mažmeninės „Commerce“ subjektais, o ne „Commerce“ subjektais. Tiksliau sakant, ji skirta nustatyti kainoms pagal parduotuvę, o ne pagal sandėlį.

„Commerce“ prekybos kainodaros mechanizmas **nepalaiko** toliau pateikiamų kainodaros funkcijų.

- Kainų nustatymas pagal vietos arba vietos ir sandėlio saugojimo dimensijas nepalaikomas. Jei prekybos sutartyse nurodysite tik vietos dimensiją, kainodaros mechanizmas nepaisys vietos ir prekybos sutartis bus taikoma visoms vietoms. Jei nurodysite ir vietą, ir sandėlį, tada elgesys yra nenurodytas / netikrintas, nes tikimasi, kad pardavėjai naudoja parduotuvės kainų grupes kiekvienos parduotuvės / sandėlio kainoms kontroliuoti.
- Atributais grindžiama kainodara nepalaikoma.
- Tiekėjo nuolaidos perėjimas nepalaikomas.
- Bendroji valiutos funkcija nepalaikoma, pvz., net jei prekybos sutartyje įjungtas **bendrosios valiutos perjungimo** funkcijos, vis tiek ši prekybos sutartis galios tik prekybos sutartyje nurodytai valiutai.
- Naudojant standartinį „Supply Chain Management“ kainodaros mechanizmą palaikomas kainos skaičiavimas pagal „Pageidaujamą siuntimo datą“ ir „Pageidaujamą gavimo data“ kartu su dabartine data. Tačiau mažmeninės prekybos kainodara šiuo metu nepalaiko šių verčių. Taip yra todėl, kad dėl B2C scenarijų klientai negali tikėtis, kad pageidaujama pristatymo data galėtų paveikti prekės kainą. Kai kuriais atvejais mažmenininkai naudoja teik B2B, tiek B2C operacijas. B2B operacijose įprasta pakeisti kainas pagal pristatymo datas. Šie mažmenininkai gali naudoti „Supply Chain Management“ kainodarą savo B2B verslui ir mažmeninės prekybos kainodarą savo B2C verslui. Mažmeninės prekybos kainodara prasideda tik tada, kai programos vartotojas yra įtraukiamas kaip skambučių centro vartotojas, todėl mažmenininkai gali priskirti konkrečius vartotojus, kurie dirbs su „Supply Chain Management“ kainodara, ir kelis vartotojus, kurie dirbs su mažmeninės prekybos kainodara, t. y. šie vartotojai turi būti įtraukti kaip skambučių centro vartotojai. Be to, reikia įjungti ypatybę **Naudoti šios dienos datą kainoms apskaičiuoti** dalyje **Prekybos parametrai> kainos ir nuolaidos > įvairios**. Tokiu būdu jie gali toliau naudoti gautinų sumų parametro reikšmę pageidaujamai siuntimo datai arba pageidaujamai gavimo datai, kad būtų galima nustatyti „Supply Chain Management“ kainodarą, bet mažmeninės prekybos kainodarai ir toliau bus naudojama šiandienos data.

Be to, toliau nurodytas „Commerce“ kainų funkcijas palaiko **tik** kainodaros mechanizmas:

- Kaina nustatoma pagal produkto dimensijas, nuo konkrečiausio varianto kainos iki mažiausiai konkretaus varianto kainos iki bendrojo produkto kainos. Kainai, kuri yra nustatyta naudojant dvi produkto dimensijas (pvz., spalvos ir dydžio), teikiama pirmenybė prieš kainą, kuri yra nustatyta naudojant tik vieną produkto dimensiją (pvz., dydžio).
- Ta pačia kainų grupe galima kontroliuoti kainas ir nuolaidas.

## <a name="pricing-api-enhancements"></a>Kainodaros API patobulinimai

Kaina yra vienas iš svarbiausių veiksnių, nuo kurių priklauso daugelio klientų pirkimo sprendimai, ir dauguma klientų prieš įsigydami palygina kainas įvairiose svetainėse. Siekdami užtikrinti, kad būtų pateiktos konkurencingos kainos, mažmenininkai atidžiai stebi savo konkurentus ir dažnai organizuoja akcijas. Siekiant padėti šiems mažmenininkams pritraukti klientų, labai svarbu, kad atliekant produktų paiešką, naudojantis naršymo funkcija, sąrašais ir produkto informacijos puslapiu būtų rodomos tiksliausios kainos.

Būsimame prekybos leidime **GetActivePrices** naudojantis taikomojo programavimo sąsaja (API) nurodomos „Commerce“ kainos, kurios apima paprastas nuolaidas (pavyzdžiui, vienos eilutės nuolaidas, kurios nepriklauso nuo kitų krepšelyje esančių prekių). Tokiu būdu rodomos kainos beveik atitinka faktinę sumą, kurią klientai moka už prekes. Ši API apima visų tipų paprastas nuolaidas: pagal priskyrimą, pagal lojalumą, pagal katalogą ir pagal kanalą. Be to, API nurodomi pavadinimai ir pateikiama informacija apie taikomas nuolaidas, kad mažmenininkai galėtų pateikti išsamesnį kainos aprašymą ir sukurti skubos jausmą, jei nuolaidos galiojimo laikas greitai baigsis.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
