---
title: „Inventory Visibility“ papildinio apžvalga
description: Šiame straipsnyje paaiškinama, kas yra atsargų matomumas, ir aprašo jo funkcijas.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: overview
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dd790bcaada0c1a05e46b4edacaa31fc4e15be92
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762813"
---
# <a name="inventory-visibility-add-in-overview"></a>„Inventory Visibility“ papildinio apžvalga

[!include [banner](../includes/banner.md)]

Atsargų matomumo priedas (*dar* vadinamas atsargų matomumo paslauga) teikia nepriklausomą ir ypač keičiamą mikrotarninę tarnybą, kuri įgalina realiuoju laiku turimų atsargų keitimų registravimus ir matomumo stebėjimą visuose jūsų duomenų šaltiniuose ir kanaluose. Tai platforma, kuri leidžia valdyti savo visuotines atsargas naudojant funkcijas, kurias sudaro (bet tuo neapsiribojama) šis sąrašas:

- Centrališkai sekite vėliausią atsargų būseną (pvz., turimos, užsakytos, nupirktos, perduotos, grąžintos ir sulaikytos) tarp visų jūsų duomenų šaltinių, sandėlių ir vietų, prijungdami savo tiekimo grandinės valdymo arba trečiosios šalies logistikos duomenų šaltinius (pvz., užsakymų valdymo sistemas, \[trečiosios šalies įmonės išteklių planavimo ERP\] sistemas, \[pardavimo EKA\] sistemas ir sandėlių valdymo sistemas) prie atsargų matomumo tarnybos.
- Pateikti užklausą dėl turimų atsargų prieinamumo ir trūkumo bei gauti skubius atsakymus tiesiogiai kviečiant atsargų matomumo tarnybą.
- Stenkitės išvengti perpildimo, ypač kai jūsų poreikis gaunamas iš skirtingų kanalų, nes atsargų matomumo paslaugoje galima rezervuoti realiuoju laiku.
- Geriau valdykite žadėtus užsakymus ir klientų tikisi, suteikdami tikslias dabartines ar sekamas datas, kad galima pridėjimo prie užsakymo (ATP) funkcija galėtų apskaičiuoti numatomas užsakymų vykdymo datas.

## <a name="extensibility"></a>Išplečiamumas

Atsargų matomumo tarnyba yra labai extensible, nes duomenų įvestis ir išeiga nėra apribota "Microsoft" programomis. Išorinės sistemos gali pasiekti tarnybą per RESTful programos programavimo sąsajas (API). Be to, kad naudojami kiti susiejimai, kurie pateikiami tiekimo grandinės valdymo duomenų šaltiniui ir dimensijoms, galite integruoti atsargų matomumą su keliomis trečiųjų šalių sistemomis nustatydami papildomus duomenų šaltinius, atsargų būsenos matus (vadinamus *faktiniais* matais atsargų matomumo paslaugoje) ir atsargų dimensijas naudodami konfigūravimo programą. Tokiu būdu galite lanksčiai pateikti užklausą ir pakeisti savo kelis duomenų šaltinius ir iš anksto nustatytas atsargų dimensijas.

Be to, kadangi atsargų matomumas sukurtas Microsoft Dataverse, jo duomenis galima naudoti kuriant ir integruojant.Power Apps Taip pat galite kurti Power BI pritaikytas skelbimų skelbimų sritis, kurios atitinka jūsų verslo poreikius.

## <a name="scalability"></a>Mastelio

Atsargų matomumo tarnybą galima padidinti arba sumažinti, tai priklauso nuo jūsų duomenų apimties. Dydžio nustatymo patirtis dažniausiai yra nuosekli ir ji priklauso nuo Microsoft platformos komandos, remiantis automatiniu operacijų duomenų tūrio aptikimu ir įvertinimu.

Šioje iliustracijoje parodyta atsargų matomumo architektūra.

[<img src="media/inventory-visibility-architecture.png" alt="Inventory Visibility architecture." title=" Atsargų matomumo architektūra" width="720" />](media/inventory-visibility-architecture.png)

## <a name="feature-highlights"></a>Svarbiausi funkcijų aspektai

### <a name="get-a-global-view-of-real-time-inventory"></a>Gauti visuotinį realiuoju laiku turimų atsargų rodinį

Atsargų matomumas užtikrina, kad visuose kanaluose, vietose ir sandėliuose visada turite prieigą prie naujausiais atsargų kiekiais. Jei turite gauti atsargų įrašų, jums bus naudingiausia naudoti šią programą, norint palaikyti kasdieninį įmonės veiklos veiklą. Visos faktiškai turimos atsargos, parduoti kiekiai ir nupirkti kiekiai šiame langelyje yra galimi. Taip pat, norėdami gauti išsamią informaciją realiuoju laiku, galite konfigūruoti ir kitus faktinių atsargų duomenis (pvz., grąžintas, sulaikytas ir užregistruotas duomenis). Atsargų matomumas gali efektyviai apdoroti milijonais atsargų keitimo įrašų. Šie duomenys gali būti sudedami ir atspindėti vėliausiu aptarnavimo atsargų kiekiu, per sekundę ar minutę, atsižvelgiant į duomenų registravimo intervalą. Norėdami gauti daugiau informacijos, žr. [atsargų matomumo viešas API](inventory-visibility-api.md).

### <a name="central-inventory-adjustment"></a>Centrinio atsargų koregavimas

Atsargų matomumas leidžia išorinėms sistemoms iškviesti SAVO API, kad būtų užregistruoti atsargų pakeitimai. Pakeitimai įsigalios atsargų matomumo metu. Todėl turimos atsargos atimamos iš karto.

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>Švelniai rezervavimas, kad nebūtų perrašomi visi užsakymo kanalai

Švelniai *rezervavimas* leidžia priskirti arba pažymėti konkrečius kiekius, kad būtų patenkintas užsakymas ar poreikis. Švelniai rezervavimas neturi įtakos faktinėms atsargoms, *tačiau* jis atima iš rezervuotinas atsargų kiekio ir pateikia atnaujintą kiekį būsimam užsakymo įvykdymams. Ši funkcija bus naudinga, jei pardavimo užklausos arba užsakymai patenka į jūsų verslą iš vieno ar daugiau kanalų arba duomenų šaltinių, kurie nepatenka į jūsų įrašo sistemos įmonės išteklių planavimo (ERP) sistemą.

Jei atsargų matomumo paslaugoje naudojate neįprastus rezervavimus, turite palaukti, kol užsakymas bus sinchronizuotas su jūsų ERP sistema ir kad ji būtų atnaujinta pagal faktinių atsargų kiekį. Paprastai šiame procese yra labai didelė gaištis. Tačiau švelniai rezervavimai įsigalioja kiekvieną kartą, kai pardavimo užklausa arba užsakymas generuojamas pardavimo kanaluose. Dėl to jos padeda išvengti perrašomos situacijos, nes užtikrina, kad jūsų užsakymai pagal ERP sistemą nebus atsieti vienas nuo kito. Švelniai rezervavimai taip pat užtikrina, kad galite įvykdyti visus žadėtuosius užsakymus. Todėl jie padeda patenkinti klientų lūkesčius ir išlaikyti klientų lojalumą. Dėl daugiau informacijos, žr. [Inventoriaus matomumo rezervavimas](inventory-visibility-reservations.md).

### <a name="immediate-response-of-atp-quantity-and-dates"></a>Tiesioginis ATP kiekio ir datų atsakymas

Matomumas jūsų būsimose projekto atsargose (įskaitant tiekimo, poreikio ir turimų atsargų duomenis) yra svarbus, nes tai padeda jūsų įmonei pasiekti šiuos tikslus:

- Sumažinti atsargų lygius, norint sumažinti atsargų valdymo išlaidas.
- Supaprastinti vidinio užsakymo apdorojimą, kad pardavėjai galėtų skaičiuoti siuntimą ir pristatymo datas remdamų užsakė produktų pasiekiamumą.
- Suteikdami kitą prieinamą datą, galite patenkinti, kada klientai gali tikėtis, kad atsargose netaps atsargose esanti prekė.

ATP funkciją lengva patvirtinti pagal savo kasdieninio užsakymo vykdymo procesą. Svarbiausia, kaip ir kiti atsargų matomumo pasiūlymai, ATP funkcija yra visuotinė *ir realiuoju laiku*. Todėl galite nustatyti kelias ATP skaičiavimo formules, kad būtų pateiktos visos atsargų prieinamumo užklausos, kurios apima visus jūsų verslo kanalus ir duomenų šaltinius. Daugiau informacijos ieškokite turimų [atsargų matomumo grafikuose ir prieinamose atsargose](inventory-visibility-available-to-promise.md).

### <a name="preallocate-your-stock-to-important-channels-or-customers-with-inventory-allocation"></a>Iš anksto paskirstyti savo atsargas svarbiems kanalams arba klientams naudojant atsargų paskirstymą

Atsargų matomumo paskirstymo funkcija leidžia apsaugoti ir apsaugoti savo vertingas turimų atsargų atsargas svarbiuose kanaluose, klientų grupėse ar vietose. Kai atsargos yra paskirstytos, atsargų suvartojimas apribotas iki paskirstyto telkinio, o visi į telkinį palikti kiekiai bus atskaityti beveik realiuoju laiku, kad atspindėtų kiekį, kuris vis dar galimas suvartojimui. Daugiau informacijos rasite atsargų [matomumo atsargų paskirstyme](inventory-visibility-allocation.md).

### <a name="compatibility-with-wms-items"></a>Suderinamumas su WMS prekėmis

"Microsoft"pagal tai, kad galėtų teikti ne "box" integravimą su sandėlio valdymo procesais (WMS), kad WMS klientai taip pat galėtų naudotis atsargų matomumo paslaugos teikiama nauda. Per 2022 bangos 1 leidimą (vieša kovo mėn. peržiūra) atsargų tarnyba palaiko WMS turimos prekės užklausas ir ATP. WMS klientams, kurie yra kitą bangą, bus palaikoma švelniai rezervavimo ir paskirstymo funkcija. Daugiau informacijos ieškokite WMS [prekių atsargų matomumo palaikymas](inventory-visibility-whs-support.md).

Šioje iliustracijoje pateikiama aukšto lygio esamų priemonių suvestinė ir nurodoma, kaip jas galima išdėstyti duomenų sraute.

[<img src="media/inventory-visibility-feature-overview.png" alt="Inventory Visibility feature overview." title=" Atsargų matomumo priemonės peržiūra" width="720" />](media/inventory-visibility-feature-overview.png)

## <a name="licensing"></a>Licencijavimas

Atsargų matomumo tarnyba prieinama šiose versijose:

- **Atsargų matomumo priedas, skirtas "Microsoft Dynamics 365 Supply Chain Management** " – įmonėms, turinčioms galiojančią tiekimo grandinės valdymo licenciją, atsargų matomumas galimas be papildomų išlaidų. Kadangi atsargų matomumas yra pagrįstas Microsoft Power Platform, jis taikomas sandėliavimo Microsoft Power Platform pajėgumui ir API limitams. Jūsų tiekimo grandinės valdymo licencija turėtų apimti numatytąjį saugojimą ir API pajėgumą. Jei jums reikia daugiau saugojimo ir API pajėgumo, galite pirkti profesinę licenciją. Išsamesnės informacijos apie numatytąjį API paskirstymą ir profesinę licenciją ieškokite Užklausos [ribos ir paskirstymai](/power-platform/admin/api-request-limits-allocations) bei [Licencijavimo peržiūra Microsoft Power Platform](/power-platform/admin/pricing-billing-skus). Naudodami numatytuosius saugojimo ir API paskirstymus, šiandien galite pradėti bandyti naudoti priedą Atsargų matomumas. Diegimo informacijos ieškokite Įdiekite [ir nustatykite atsargų matomumą](inventory-visibility-setup.md). Jei įvertintas API ir saugojimo naudojimas viršija standartinį paskirstymą, galite susisiekti su savo pardavimo atstovu ir paprašyti jų susisiekti su platformos komanda, kad ši būtų išimtis.
- **Atsargų matomumo tarnyba kaip IOM** komponentas – ši versija skirta arba išmaniojo užsakymų valdymo (IOM) klientams arba įmonėms, kurios nenaudoja tiekimo grandinės valdymo kaip savo ERP sistemos. Licencija yra įtraukta į išmaniojo užsakymų valdymo grupę. Norėdami gauti daugiau informacijos, žr. Išmaniojo [užsakymų valdymo peržiūra](/dynamics365/intelligent-order-management/overview).

## <a name="inventory-visibility-terminology"></a>Atsargų matomumo terminologija

Svarbu suprasti šias sąvokas ir terminus, kai dirbate su atsargų matomumo priedo:

- **Duomenų šaltinis** – duomenų šaltinis rodo sistemai, iš kurios yra jūsų duomenys.
- **Dimensijos** – dimensijos identifikuoja produkto charakteristikas. Jos gali būti sandėliavimo dimensijos (pvz., svetainė ar sandėlis) arba produkto dimensijos (pvz., spalva, dydis arba stilius).
- **Faktiniai** matai – faktiniai matai, kurie matuoja skirtingas atsargų būsenas, pvz., turimos atsargos, nupirktos, užsakytas arba parduotas.
- **Apskaičiuoti duomenys** – skaičiuojami duomenys yra kiekybiniai duomenys, apskaičiuojami iš faktinių priemonių rinkinio. Pvz., bendra *turima* apskaičiuota priemonė apskaičiuojama taip *: Nupirkta* + *·* – *Užsakyta* – *Parduota*.
- **Skaidinys** – skaidinys apibrėžia hierarchiją, kaip atsargų matomumas paskirstys gautus duomenis. Šiuo metu numatytasis skaidinys yra svetainė ir vieta.
- **Indeksų** hierarchija – indeksų hierarchija toliau apibrėžia, kaip norite pateikti užklausą apie atsargas ir gauti rezultatus, kurie yra išsamesni.

Daugiau informacijos apie šiuos terminus ir sąvokas ieškokite Konfigūruoti [atsargų matomumą](inventory-visibility-configuration.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
