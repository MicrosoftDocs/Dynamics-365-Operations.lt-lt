---
title: "Gamybos subrangos darbų valdymas"
description: "Šioje temoje paaiškinama, kaip subrangos operacijos valdomos programoje „Microsoft Dynamics 365 for Operations“. Kitaip tariant, paaiškinama, kaip tiekėjas valdo ištekliui priskirtas gamybos operacijas."
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

# <a name="manage-subcontracting-work-in-production"></a>Gamybos subrangos darbų valdymas

[!include[banner](../includes/banner.md)]


Šioje temoje paaiškinama, kaip subrangos operacijos valdomos programoje „Microsoft Dynamics 365 for Operations“. Kitaip tariant, paaiškinama, kaip tiekėjas valdo ištekliui priskirtas gamybos operacijas.

[Gamybos procesuose](production-process-overview.md) darbą gali atlikti ištekliai, kurie priklauso arba kuriuos administruoja tiekėjai. Paprastai tiekėjo ištekliai naudojami norint patenkinti periodiškai išaugusį poreikį, kuris viršija įmonės išteklių pajėgumą. Tiekėjas taip pat gali pasiūlyti specialių [išteklių resursų](resource-capabilities.md) arba išteklių už mažesnę kainą.  

Atsižvelgiant į gamybos procese naudojamus tiekėjo išteklius, [maršrutui](routes-operations.md) dažnai priskiriami papildomi logistiniai reikalavimai, kadangi medžiagas ir pusiau baigtus produktus pirmiausia reikia atgabenti į tiekėjo teritoriją. Tada subrangos operacijos produktus reikia perkelti į kitai operacijai priskirtą vietą arba į baigtų prekių sandėlį.  

Kai naudojamos subrangos operacijos arba veiklos, jos turi įtakos visiems operacijų etapams, nuo gamyboje, įkainojime, prognozių nustatyme, ir planavime reikalingų operacijų apibrėžimo iki medžiagų, pusiau baigtų produktų ir baigtų prekių logistikos valdymo. Galiausiai reikia atlikti pačių išteklių apskaitos ir išlaidų kontrolės procesus.  

Naudojant vidinius išteklius, paprastai laikotarpiui priskiriamas fiksuotas kainos tarifas. Tačiau subrangos išteklių kaina priklauso nuo susijusios paslaugos pirkimo kainos. Paslauga apibrėžiama kaip dar vienas produktas ir ji naudojama tam tikros subrangos operacijos įsigijimo ir pirkimo procesams valdyti.  

Šiuo metu programoje „Microsoft Dynamics 365 for Operations“ pusiau baigti produktai nėra aiškiai apibrėžti. Jei gamybos užsakymui įvykdyti reikalinga daugiau nei viena operacija, kad žaliavos būtų paverstos baigta preke, baigta prekė vėl registruojama atsargose tik atliekant paskutinę operaciją. Ankstesnių operacijų metu pagaminti pusiau baigti produktai nurodomi nebaigtoje gamyboje (NG), bet jie atsargose nėra registruojami arba sekami. Nors maršrutus ir KS galite skaidyti į daug mažesnių vienetų, taikant tokį metodą padidėja produktų, KS ir maršrutų, kuriuos reikia valdyti, skaičius.  

Gamybos operacijų subrangos darbą galima modeliuoti dviem būdais. Šie būdai vienas nuo kito skiriasi tuo, kaip subrangos procesą galima modeliuoti: kaip procese galima nurodyti pusiau baigtus produktus ir kaip galima valdyti išlaidas.

-   Gamybos užsakymų arba paketinių užsakymų maršruto operacijų subranga
    -   Paslaugos produktas turi būti laikomas produktas ir turi būti KS dalis.
    -   Šis būdas palaiko „pirmasis į, pirmasis iš“ (FIFO) arba standartinę kainą.
    -   Pusiau baigtus produktus procese nurodo paslaugos produktas.
    -   Išlaidų kontrolė paskirsto išlaidas, susijusias su subrangos darbu, medžiagų išlaidoms.
-   Subrangos arba gamybos eigos veiklos „lean“ gamybos eigoje
    -   Paslauga yra nelaikomas produktas ir ji nėra KS dalis.
    -   Taikant šį būdą pirkimo sutartys naudojamos kaip aptarnavimo sutartys.
    -   Taikant šį būdą naudojamas įkainojimas atvirkštine tvarka.
    -   Šis būdas suteikia galimybę vykdyti sujungtą ir asinchroninį įsigijimą. (Medžiagų srautas nepriklauso nuo įsigijimo proceso.)
    -   Išlaidų kontrolė paskirsto subrangos darbą į nuosavą išlaidų paskirstymo bloką.

## <a name="subcontracting-of-route-operations"></a>Maršruto operacijų subranga
Norėdami naudoti gamybos arba paketinių užsakymų maršruto operacijų subrangą, paslaugos įsigijime naudojamas paslaugos produktas turi būti nurodytas kaip tipo **Paslauga** produktas. Be to, turi būti priskirta prekių modelių grupė, kurios parinktis **Laikomas produktas**, esanti dalyje **Atsargų strategija**, nustatyta į **Taip**. Ši parinktis nustato, ar produktas produkto gavimo dokumente nurodomas kaip atsargos (**Laikomas produktas**  =  **Taip**), ar jis įtraukiamas į pelno ir nuostolių sąskaitą (**Laikomas produktas**  =  **Ne**). Nors šis elgesys gali atrodyti prieštaringas, jis paremtas faktu, kad tik šią strategiją turintys produktai sukurs atsargų operacijas, kurias galima naudoti išlaidų kontrolėje, norint apskaičiuoti suplanuotas išlaidas ir nustatyti faktines išlaidas, kai gamybos užsakymas baigtas.  

Tam, kad paslauga būtų įtraukiama į planavimą ir išlaidų skaičiavimą, ji turi būti įtraukta į KS. KS eilutė turi būti tipo **Tiekėjas** ir ji turi būti paskirstyta maršruto operacijai, kuriai paskirstyta paslauga. Ši maršruto operacija privalo turėti įkainojimo išteklių ir ištekliaus reikalavimą, kurie nurodo tipo **Tiekėjas** išteklių, sujungiantį operaciją ir susijusią paslaugą su atitinkama tiekėjo sąskaita.  

Kai naudojama ši konfigūracija, įvertinus gamybos užsakymą sukuriamas susijusios paslaugos produkto pirkimo užsakymas. Paslaugos pirkimo užsakymas naudojamas kaip subrangos operacijų pagrindas. Subrangos darbą galima valdyti gamybos kontrolės sąrašo puslapyje **Subrangos darbas**. Subrangos darbas naudojamas norint siųsti žaliavas ir pusiau baigtą produktą tiekėjui besiruošiant operacijai. Jis taip pat naudojamas norint subrangos operacijos galutinį produktą gauti prekių gavime, kur paslaugos produktas naudojamas pusiau baigto produkto gavimui nustatyti. Kai gaunama pirkimo užsakymo eilutė, gamybos operacija atnaujinama kaip baigta.  

Gamybos užsakyme gali būti daug operacijų ir kiekviena operacija gali būti paskirstyta kitam tiekėjui. Todėl galutiniam gamybos užsakymui įvykdyti gali reikėti kelių pirkimo užsakymų.

## <a name="subcontracting-of-production-flow-activities"></a>Subrangos arba gamybos eigos veiklos
[lean manufacturing](lean-manufacturing-overview.md) sprendimas subrangos darbą modeliuoją kaip paslaugą, kuri susijusi su [gamybos eigos](http://ax.help.dynamics.com/en/wiki/create-a-production-flow-version/) veikla (užduočių vedlio tema). Todėl šio tipo subranga dar vadinama [veikla pagrįsta subranga.](activity-based-subcontracting.md) Pristatytas specialus išlaidų grupės tipas **Tiesioginė subranga** ir subrangos paslaugos nėra baigtų prekių KS dalis. Kai naudojate „lean manufacturing“, visos veiklos nurodomos naudojant „kanban“, kurias galima susieti su viena ar keliomis gamybos eigos veiklomis. Šis apibūdinimas yra panašus į gamybos užsakymų apibrėžimą. Tačiau gamybos užsakymai visada turi būti pasibaigti baigtu produktu, pusiau baigtam produktui tiekti galite kurti „kanban“. Nereikia įtraukti naujo produkto ir KS lygio.  

Kadangi „kanban“ taisyklės gali būti labai dinamiškos, gamybos eigoje galite modeliuoti skirtingas to pačio produkto tiekimo parinktis. Kai naudojate „lean“ subrangą, medžiagų srautas ir finansų srautas yra aiškiai atskirti. Visą medžiagų srautą nurodo „kanban“ veiklos. Paslaugos produktų gamybos užsakymus ir tų paslaugų gavimo registravimą galima automatizuoti, atsižvelgiant į gamybos eigos „kanban“ užduočių būseną. „Kanban“ užduotis galima pradėti ir baigti net prieš sukuriant pirkimo užsakymus. Subrangos dokumentus (paslaugos pirkimo užsakymą ir pirkimo gavimo dokumentą) galima sujungti pagal laikotarpį ir paslaugą. Todėl mažą pirkimo dokumentų ir eilučių skaičių galima išlaikyti net itin pasikartojančiose operacijose, kai tiekėjai subrangos paslaugas teikia vieningu srautu.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Gamybos eigos subrangos modeliavimas

[„lean“ gamybos eigoje](lean-manufacturing-modeling-lean-organization.md) proceso veiklą galima apibrėžti kaip subrangos veiklą, kai ji paskirstoma darbo elementui (išteklių grupei), kuriai priskirtas vieno tiekėjo išteklius. Kai darbo elementą atlieka subrangovai, susijusias proceso veiklas reikia susieti su aktyvia pirkimo sutarties eilute, kurioje yra paslaugos prekė ir paslaugos kaina. Veiklos paslaugos sutartis taip pat apibrėžia „kanban“ užduoties produkto kiekio ir galutinio paslaugos kiekio skaičiavimo koeficientą. Galite pasirinkti , ar paslaugos kiekis skaičiuojamas pagal užduočių skaičių, pateiktą užduočių prekių produktų kiekį, ar pagal bendrą produktų kiekį (šis bendras kiekis apima nurašytus produktus).  

Perkėlimo veiklas taip pat galima apibrėžti kaip subrangovų veiklas. Šis apibrėžimas taikomas netiesiogiai, kai jūs pasirenkate už siuntimo ir perkėlimo veiklą atsakingą šalį. Kai pasirenkate **Siuntėjas** arba **Gavėjas**, jei atitinkamas šaltinis arba paskirties sandėlis yra tiekėjo valdomas sandėlis, veikla laikoma subrangos veikla. Kai pasirenkate **Vežėjas**, veikla visada yra subrangos veikla. Subrangos perkėlimo veiklą (kaip ir subrangos procesų veiklas) reikia prijungti prie paslaugos sutarties prieš aktyvinant gamybos eigą.

### <a name="backflush-costing"></a>Įkainojimas atvirkštine tvarka

Subrangos darbo išlaidų apskaita yra visiškai integruota į „lean manufacturing“ įkainojimo sprendimą (įkainojimas atvirkštine tvarka). Kai paslaugos pirkimo užsakymo gavimo dokumentas arba kai išrašomos SF, paslaugos išlaidos yra paskirstomos gamybos eigoje. Taikant įkainojimą atvirkštine tvarka, subrangos paslaugų nuokrypis apskaičiuojamas subalansuojant gautų produktų standartinių išlaidų subrangos bloką ir faktinius gautus kiekius bei paslaugų kiekius, kurių SF išrašyta.

## <a name="material-supply-for-subcontracted-operations"></a>Subrangos operacijų medžiagų tiekimas
Pusiau baigtus produktus ir kitas susijusias medžiagas reikia perkelti į vietą, kurioje atliekamas faktinis darbas. Kai naudojate subrangos operacijas ir veiklas, šis perkėlimas yra dažnai susijęs su papildomu perkėlimu į tiekėjo valdomą vietą. KS medžiagą paskirstydami subrangos operacijai patvirtinate, kad medžiagą reikia suskirstyti į etapus paskirstyto ištekliaus išteklių grupės įvesties vietoje. Tada bendrasis planavimas arba „lean“ papildymas tiekia medžiagą į tą vietą.  

Norint modeliuoti tiekėjo teritorijoje esančias atsargas, geriausia nurodyti tiekėjo valdomą sandėlį. Tiekėjo valdomą sandėlį galite lengvai nurodyti sukurdami naują sandėlį ir priskirdami tiekėjo sąskaitą. Tą medžiagą reikia perkelti tiekėjui prieš atliekant operaciją, todėl tiekėjo valdomą sandėlį turėtumėte paskirstyti išteklių grupės, kuriai priklauso išteklius, įvesties sandėliui.  

Norėdami papildyti medžiagos atsargas šiame sandėlyje, galite naudoti kelias toliau nurodytas strategijas.

-   Perkėlimo užsakymai
-   Perkėlimo žurnalai
-   Išėmimo „kanban“
-   Tiesioginis pirkimas į tiekėjo vietą

Pusiau baigti produktai yra šios taisyklės išimtis. Norėdami perkelti pusiau baigtus produktus, galite naudoti tik tolesnes parinktis.

-   Gamyboje ir paketiniuose užsakymuose pusiau baigtus produktus galima perkelti tik logiškai, naudojant sąrašo puslapyje **Subrangos darbas** esantį išrinkimo dokumentų žurnalą. Šis žurnalas sukurs pristatymo pažymos dokumentą, kurį naudojant galima perkelti pusiau baigtus produktus ir žaliavas tiekėjui.
-   Gamybos eigoje vykdant subrangos operacijas, pusiau baigtų produktų perkėlimas dokumentuojamas tiekėjo vietovėje, išėmimo kvituose ir gamybos „kanban“. Norėdami modeliuoti tiesioginę perkėlimo veiklą, gamybos „kanban“ galite pabaigti papildoma perkėlimo veikla.

**Pastaba.** Vieno gamybos užsakymo gamybos maršrutas negali vesti į kelias teritorijas. Ši taisyklės taip pat taikoma subrangos darbui. Todėl tiekėjo valdomas medžiagų saugojimo vietas nurodantys sandėliai turi būti apibrėžti toje pačioje teritorijoje kaip maršrute naudojami vidiniai ištekliai. Nors gamybos eigos gali vesti į kelias teritorijas, jos negali pusiau baigtų produktų perkelti iš vienos teritorijos į kitą, nes tokia operacija pakeičia išlaidų kontekstą.  

Paprastai subrangos išteklių grupės išeigos sandėlis ir vieta yra tiesiogiai paskirstomos į kito operacijos veiksmo sandėlį arba vietą maršrute arba gamybos eigoje. Ši sąranka padeda sumažinti teikiamų užduočių ataskaitų kiekį arba papildomų perkėlimo operacijų, kurias reikia modeliuoti, skaičių.




