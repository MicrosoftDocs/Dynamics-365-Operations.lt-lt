---
title: "Valdyti subrangos darbų gamyboje"
description: "Šioje temoje aiškinama, kaip subrangovo operacijos valdomos Microsoft Dynamics 365 operacijoms. Kitaip tariant, ji paaiškina, kaip valdoma gamybos operacijas, kurios yra priskiriamos prie išteklių tiekėjo."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LeanDocumentServiceCreation, PlanActivity, ProdBOMVendorListPage, ProdRoute, ProdTable, ProdTableListPage, PurchAgreementSubcontractorLookup, RouteTable, WrkCtrResourceGroup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268174
ms.assetid: fe47c498-4f48-42a2-a0cf-5436c19ab3ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 79430358bebd93fd96f1169d22737d3537dbfc08
ms.lasthandoff: 03/31/2017


---

# <a name="manage-subcontracting-work-in-production"></a>Valdyti subrangos darbų gamyboje

Šioje temoje aiškinama, kaip subrangovo operacijos valdomos Microsoft Dynamics 365 operacijoms. Kitaip tariant, ji paaiškina, kaip valdoma gamybos operacijas, kurios yra priskiriamos prie išteklių tiekėjo.

Į [gamybos procesai](production-process-overview.md), darbas gali būti padaryta iš išteklių, kurie priklauso arba kuriuos administruoja pardavėjai. Paprastai, tiekėjo ištekliai naudojami lygio periodiškai perteklinės paklausos, kad pranoksta galimybes įmonės nuosavų išteklių. Tiekėjas taip pat galės pasiūlyti konkrečias [išteklių pajėgumus](resource-capabilities.md)ar išteklių už mažesnę kainą.  

Atsižvelgdamas į tiekėjo išteklius, kurie yra naudojami gamybos proceso metu, a [maršruto](routes-operations.md) dažnai turi papildomų logistikos reikalavimus, nes medžiagos ir pusgaminiai, pirmiausia turi būti vežami į tiekėjo svetainėje. Tuomet dėl subrangos sutartis vykdoma veikla turi būti vežami arba į vietą, kurioje yra skirstoma į kitą operaciją arba gatavų prekių sandėlio.  

Kai naudojamos subranga operacijų ar veikla, jie turi įtakos visiems etapams operacijas, operacijas, kurių reikia gamybai, įkainojimo, prognozavimo, planavimo ir planavimo, valdymo, logistikos, medžiagų, pusgaminių ir gatavų prekių apibrėžimas. Galiausiai šių išteklių reikia jų pačių procesų apskaitos ir išlaidų kontrolę.  

Vidaus išteklių, paprastai pastoviųjų išlaidų tarifą skiriama laikotarpiui. Priešingai, subrangovų išteklių sąnaudų yra pagrįstas pirkimo kainą, susijusį darbą. Paslauga apibrėžiama kaip kito produkto, ir yra naudojamas viešųjų pirkimų ir pirkimo procesus konkrečios užsakytos operacijos.  

Šiuo metu nėra aiškaus sąvokos pusgaminių Microsoft Dynamics 365 operacijoms. Gamybos užsakymas, kuris reikalauja daugiau nei vieną operaciją siekiant paversti gataviems gerą žaliavos, gataviems gerą registruojamas atgal į atsargas tik paskutinę operaciją. Pusgaminiai, kurie ankstesnėse operacijose gamina apskaitomi nebaigtos gamybos (NG), bet jie nėra paskelbtas ar sekami atsargų. Nors keliai ir komplektavimo specifikacijos (KS) galite padalinti į kelis mažesnius, šis metodas padidina produktų, KS ir maršrutus, kurie turi būti valdomi.  

Yra du būdai modeliavimo subrangos darbus gavybos operacijoms vykdyti. Šie metodai skiriasi tuo, kad subrangos procesas gali būti modeliuojama, taip, kad pusgaminių būtų atstovaujama procese, ir tvarkomi taip, kad išlaidų kontrolės būdas.

-   Subrangos maršruto operacijas, gamybos ar partijos užsakymai
    -   Paslaugų produktas turi būti aprūpintas produktas, ir tai turi būti KS.
    -   Šis metodas palaiko pirmoji, pirmas iš (FIFO) arba normatyvinę savikainą.
    -   Pusgaminiai atstovauja paslaugų produkto procese.
    -   Ry¹iù kainos tikrinimas paskirsto išlaidas, susijusias su subrangovų darbą iki medžiagų sąnaudų.
-   Subrangos sutarčių sudarymas gamybos srauto veiklos lanksčiosios gamybos srautas
    -   Paslauga yra atsargose paslaugos produktas, ir tai ne dalis KS.
    -   Šis metodas naudoja pirkimo sutartys kaip paslaugų sutartis.
    -   Šis metodas naudoja padėčių kainuoja.
    -   Šis metodas leidžia apibendrinti ir asinchroninis paėmimui. (Medžiagų srauto nepriklauso viešojo pirkimo procedūros).
    -   Išlaidų kontrolės skiria subrangovo darbas savo išlaidų paskirstymas bloke.

## <a name="subcontracting-of-route-operations"></a>Subrangos maršruto operacijų
Naudotis subranga nukreipimo operacijas gamybos ar partijos pavedimus, paslaugos produktas, kuris yra naudojamas viešųjų pirkimų tarnybos turi būti apibrėžiamas kaip produktas, **paslaugų** tipo. Be to, ji turi būti atsargų modelio grupė, kuri turi ir **Stocked produkto** variantas pagal **atsargų politikos** lygi **taip**. Ši parinktis nurodo, ar produktas yra apskaitytos kaip atsargų pirkimą (**Stocked produkto** = **taip**), arba ar produkto savikaina pelno ir nuostolio sąskaitoje (**Stocked produkto** = **Nr**). Nors taip gali pasirodyti prieštaringa, tai dėl to, kad tik tie produktai, kurie turi šios politikos bus sukurti atsargų operacijos, kuri gali būti naudojama išlaidų kontrolės skaičiuoti suplanuotos išlaidos ir nustatyti faktinę savikainą, kai pateiktas gamybos užsakymas baigiamas.  

Reikia atsižvelgti į planavimo ir išlaidų apskaičiavimas, paslaugos įrašoma į KS. KS eilutės turi būti su **tiekėjo** tipo, ir ji turi būti priskirta maršruto operacijos, kad paslauga būtų skiriama. Šio maršruto operacijos turi turėti įkainojimo išteklių ir išteklių reikalavimas, kad nukreipkite žymiklį į šaltinį, **tiekėjo** tipo, kuris jungia operacija ir susijusį darbą į atitinkamą tiekėjo sąskaitą.  

Naudojant šią konfigūraciją, pirkimo užsakymą sukurtas susijusį darbą produktas, remiantis įvertinti gamybos užsakymą. Pirkimo užsakymo paslauga yra naudojamas kaip inkaras subrangos sutartis vykdoma veikla. Subrangovo darbas gali būti valdomas per į **sudaryta subrangos darbus** sąrašo puslapį gamybos kontrolė. Subrangovo darbas naudojamas išsiųsti žaliavos ir, galiausiai, pusiau pabaigtų gaminių paruošimas operacijai, pardavėjui. Jis taip pat naudojamas gauti galutinį produktą rangovų veiklos prekių gavimui, kur paslaugos produktas yra naudojamas nustatyti pusgaminių atvykimo. Gavus pirkimo užsakymo eilutėje, gamybos operacija atnaujinama kaip atliktą.  

Gamybos užsakymas gali turėti daug operacijų, ir kiekvienos operacijos gali būti priskirtas prie kito tiekėjo. Todėl iki galo gamybos užsakymo gali sukelti daug užsakymų.

## <a name="subcontracting-of-production-flow-activities"></a>Subrangos gamyba srauto veiklos
Į [tausojančios gamybos](lean-manufacturing-overview.md)tirpalas modelių subrangos darbų, kaip paslauga, kuri yra susijusi su veikla, [gamybos srauto](http://ax.help.dynamics.com/en/wiki/create-a-production-flow-version/) (užduoties vadovas tema). Todėl šio tipo subranga yra taip pat vadinama [veikla pagal subrangos sutarčių sudarymą.](activity-based-subcontracting.md) Speciali kaina grupės tipą, **tiesioginės užsakomosios paslaugos**, buvo įvesta, ir subrangos paslaugas neįeinančias baigtos prekės KS. Naudojant tausojančios gamybos, kanbans, kurie gali būti susiję su vieno ar kelių gamybos srauto valdymo veiklą apibrėžia visose veiklos srityse. Iki šiol šis paaiškinimas skamba kaip paaiškinimas gamybos užsakymų. Tačiau kadangi gamybos užsakymus visada turi baigtis su galutinio produkto, galite sukurti kanbans tiekti pusiau pabaigtų gaminių. Jūs neturite įdiegti naują produktą ir KS lygyje.  

Nes kanban taisykles gali būti labai dinamiški, galite modeliuoti įvairių variantų dėl to paties produkto gamybos srautui. Kai naudojate liesą subrangos sutarčių sudarymas, medžiagų srauto ir finansinio srauto yra griežtai atskirti. Visų medžiagų srauto atstovauja kanban veikla. Pirkimo užsakymų paslaugų produktų ir paslaugų gavimo darbai gali būti automatizuoti, priklausomai nuo būsenos gamybiniu kanban darbo vietų. Kanban darbo vietų gali būti pradėtas ir net prieš pirkimo užsakymų yra sukurta. Subrangos dokumentus (pirkimo užsakymas ir pirkimo kvitas paslaugos) būtų galima kaupti ir paslaugas. Todėl pirkimo dokumentuose ir eilučių skaičius gali būti laikomas nedidelis, net ir labai pasikartojantis veiksmų tais atvejais, kai pardavėjai subrangovo paslaugas vientisas srautas.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Subrangos produkcijos srautų modeliavimas

Mieste yra [liesos gamybos srauto](lean-manufacturing-modeling-lean-organization.md), proceso veikla galima apibūdinti kaip subrangovui, kai jis paskirstomas darbas langelį (išteklių grupės), kuriame yra vieno tiekėjo išteklių. Kai darbas ląstelė samdo subrangovus, susijusius procesus veikla turi būti siejama su aktyvaus pirkimo sutarties eilutės, kuriose yra aptarnaujamos prekės ir paslaugos kainą. Paslaugų sutarties veiklos taip pat apibrėžia apskaičiuojant santykį tarp kanban darbo produktų kiekis ir nustatytas paslaugų kiekis. Galite pasirinkti, ar aptarnavimo kiekis apskaičiuojamas pagal skaičių darbo vietų, geras produkto kiekis, kuris pranešė darbams, arba viso produkto kiekį (Šis bendras kiekis apima į atliekas nurašytų gaminių).  

Perdavimo veikla taip pat galima apibrėžti kaip subrangovai. Šis apibrėžimas atsiranda netiesiogiai pasirinkus atsakingoji šalis už laivybos perdavimo veikla. Kai **siuntėjo** ar **gavėjas**, jei šaltinio arba paskirties sandėlyje yra tiekėjo valdomą sandėlį, veikla laikoma trečiąja. Kai **vežėjų**, veikla visada samdo subrangovus. Kaip subrangovo proceso veiklas, subrangovų perdavimo veikla turi būti prijungtas prie aptarnavimo sutarties prieš gamybos srautas gali būti aktyvuota.

### <a name="backflush-costing"></a>Įkainojimas atvirkštine tvarka

Subrangovų darbo sąnaudų apskaitos yra visiškai integruota į kainuoja, tausojančios gamybos sprendimas (padėčių kainuoja). Užregistravus pirkimo užsakymo gavimo paslauga, arba kai kyla, duomenys į SF, paslauga yra paskirstoma gamybos srauto. Padėčių kainuoja, subrangovo paslaugos dispersija yra apskaičiuojamas atsverdama subrangos blokas, Normatyvinė savikaina gautus produktus nuo faktinio gavo ir išrašytoje SF paslaugų kiekius.

## <a name="material-supply-for-subcontracted-operations"></a>Medžiagų tiekimo už subrangovų veiklą
Pusgaminiai ir kitų susijusių medžiagų turi perkelti į tą vietą, kur fiziškai atliekamas darbas. Kai naudojate subrangovo operacijoms ir veiklai, šis perdavimas dažnai yra susijęs su papildomas transporto tiekėjo eksploatuojamos svetainėje. Skiriant medžiagos KS su rangovų veikla, jūs pareiškiate, kad medžiaga turi būti pastatytas įvesties vietos išteklių grupės priskirti ištekliai. Bendrojo planavimo arba liesos papildymo tada parengia medžiagą į tą vietą.  

Modelio aprašas, kad yra tiekėjo svetainėje, tai geriausia pramonėje apibrėžti tiekėjo valdomą sandėlį. Galite lengvai nustatyti tiekėjo valdomos sandėlio naują sandėlį kūrimas ir priskyrimas tiekėjo sąskaitą. Dokumentais pagrįsti, kad medžiaga turi būti perduota tiekėjui prieš operaciją galima atlikti, jums turėtų paskirstyti įvesties sandėlio išteklių grupės, kuri turi išteklių tiekėjo valdomos sandėlyje.  

Papildyti medžiagos šiame sandėlyje, galite naudoti keletą strategijų:

-   Perkėlimo užsakymai
-   Perkėlimo žurnalai
-   Panaikinimo kanbans
-   Tiesioginis pirkimas į tiekėjo vietą

Pusgaminiai yra šios taisyklės išimtis. Norėdami perkelti pusgaminiai, galite naudoti tik šias parinktis:

-   Gamybos ir partijos pavedimus, pusgaminiai gali būti persiųsti tik logiškai naudojant išrinkimo iš to **sudaryta subrangos darbus** sąrašo puslapį. Šiame leidinyje bus sukurti važtaraštyje dokumentą, kuris gali būti naudojamas perduoti pusgaminius ir žaliavas, tiekėjui.
-   Už subrangovų veiklą gamybos srautai, perdavimo pusgaminių parduotame panaikinti arba gamybos kanbans vietoje tiekėjo gavimo. Modeliuoti aiškiai perdavimo veikla, galite baigti gamybos kanban su papildoma perdavimo veiklą.

**Pastaba:** gamybos maršruto gamybos užsakymo negalima kirsti keliose svetainėse. Ši taisyklė taip pat taikoma subrangovo darbas. Todėl, sandėliai, atstovauti tiekėjo valdomos medžiagos vietose turi būti nurodytas toje pačioje vietoje kaip vidaus išteklių, kurie yra naudojami maršrutą. Nors gamybos srautai gali kirsti svetaines, jie negali vežti pusgaminiai iš vienos svetainės į kitą, todėl, kad ta veikla reiškia pakeisti išlaidų kontekste.  

Paprastai produkcijos sandėlio ir vietoje užsakytos išteklių grupės tiesiogiai priskiriamas sandėlio ir kitas žingsnis į maršrutą arba gamybos srauto operacijos vietą. Šis nustatymas padeda sumažinti darbo ataskaitos, kuri atsiranda arba skaičių papildomų perdavimo operacijas, kurios turi būti modeliuojama.


