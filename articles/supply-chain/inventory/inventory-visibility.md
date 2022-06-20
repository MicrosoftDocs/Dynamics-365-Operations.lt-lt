---
title: Atsargų matomumo papildinio apžvalga
description: Šiame straipsnyje paaiškinama, kas yra atsargų matomumas, ir aprašo jo funkcijas.
author: yufeihuang
ms.date: 03/18/2022
ms.topic: overview
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 782545ea38a209eb4430607f5bca96e4e930efdc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897638"
---
# <a name="inventory-visibility-add-in-overview"></a>Atsargų matomumo papildinio apžvalga

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

## <a name="feature-highlights"></a>Svarbiausi funkcijų aspektai

### <a name="get-a-global-view-of-real-time-inventory"></a>Gauti visuotinį realiuoju laiku turimų atsargų rodinį

Atsargų matomumas užtikrina, kad visuose kanaluose, vietose ir sandėliuose visada turite prieigą prie naujausiais atsargų kiekiais. Jei turėsite atsargų įrašus, jums bus naudingiausia naudotis juo, kad būtų galima palaikyti kasdieninį įmonės veiklos veiklą. Visos faktiškai turimos atsargos, parduoti kiekiai ir nupirkti kiekiai šiame langelyje yra galimi. Taip pat, norėdami gauti išsamią informaciją realiuoju laiku, galite konfigūruoti ir kitus faktinių atsargų duomenis (pvz., grąžintas, sulaikytas ir užregistruotas duomenis). Atsargų matomumas gali efektyviai apdoroti milijonais atsargų keitimo įrašų. Šie duomenys gali būti sudedami ir atspindėti vėliausiu aptarnavimo atsargų kiekiu, per sekundę ar minutę, atsižvelgiant į duomenų registravimo intervalą. Norėdami gauti daugiau informacijos, žr. [atsargų matomumo viešas API](inventory-visibility-api.md).

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>Švelniai rezervavimas, kad nebūtų perrašomi visi užsakymo kanalai

Švelniai *rezervavimas* leidžia priskirti arba pažymėti konkrečius kiekius, kad būtų patenkintas užsakymas ar poreikis. Švelniai rezervavimas neturi įtakos faktinėms atsargoms, *tačiau* jis atima iš rezervuotinas atsargų kiekio ir pateikia atnaujintą kiekį būsimam užsakymo įvykdymams. Ši funkcija bus naudinga, jei pardavimo užklausos arba užsakymai patenka į jūsų verslą iš vieno ar daugiau kanalų arba duomenų šaltinių, kurie nepatenka į jūsų įrašo sistemos įmonės išteklių planavimo (ERP) sistemą.

Jei atsargų matomumo paslaugoje naudojate ne soft reservations, turite palaukti, kol užsakymas bus sinchronizuotas su jūsų ERP sistema ir kad sistema jį apdorotų, kad būtų apdorotas faktinių atsargų kiekio atnaujinimas. Paprastai šiame procese yra labai didelė gaištis. Tačiau švelniai rezervavimai įsigalioja kiekvieną kartą, kai pardavimo užklausa arba užsakymas generuojamas pardavimo kanaluose. Dėl to jos padeda išvengti perrašomos situacijos, nes užtikrina, kad jūsų užsakymai pagal ERP sistemą nebus atsieti vienas nuo kito. Švelniai rezervavimai taip pat užtikrina, kad galite įvykdyti visus žadėtuosius užsakymus. Todėl jie padeda patenkinti klientų lūkesčius ir išlaikyti klientų lojalumą. Dėl daugiau informacijos, žr. [Inventoriaus matomumo rezervavimas](inventory-visibility-reservations.md).

### <a name="immediate-response-of-atp-dates-confirmation"></a>Tiesioginis ATP datų patvirtinimo atsakymas

Matomumas jūsų būsimose projekto atsargose (įskaitant tiekimo, poreikio ir turimų atsargų duomenis) yra svarbus, nes tai padeda jūsų įmonei pasiekti šiuos tikslus:

- Sumažinti atsargų lygius, norint sumažinti atsargų valdymo išlaidas.
- Supaprastinti vidinio užsakymo apdorojimą, kad pardavėjai galėtų skaičiuoti siuntimą ir pristatymo datas remdamų užsakė produktų pasiekiamumą.
- Suteikdami kitą prieinamą datą, galite patenkinti, kada klientai gali tikėtis, kad atsargose netaps atsargose esanti prekė.

ATP funkciją lengva patvirtinti pagal savo kasdieninio užsakymo vykdymo procesą. Svarbiausia, kaip ir kiti atsargų matomumo pasiūlymai, ATP funkcija yra visuotinė *ir realiuoju laiku*. Todėl galite nustatyti kelias ATP skaičiavimo formules, kad būtų pateiktos visos atsargų prieinamumo užklausos, kurios apima visus jūsų verslo kanalus ir duomenų šaltinius. Daugiau informacijos ieškokite turimų [atsargų matomumo grafikuose ir prieinamose atsargose](inventory-visibility-available-to-promise.md).

### <a name="compatibility-with-advanced-warehouse-management-items"></a>Suderinamumas su išplėstinėmis sandėlio valdymo prekėmis

"Microsoft"perteikti papildomą integravimą su išplėstiniu sandėlio valdymu (WHS), kad sandėlio valdymo klientai taip pat galėtų naudotis atsargų matomumo paslaugos teikiama nauda. Per 2022 bangos 1 leidimą (vieša kovo mėn. peržiūra) atsargų tarnyba palaiko užklausas dėl sandėlio valdymo ir atp. Soft reservation ir paskirstymo funkcija bus palaikoma whS klientams, paskesnėje bangoje. Daugiau informacijos ieškokite sandėlio valdymo [ir sandėlio valdymo prekių atsargų matomumo palaikymas](inventory-visibility-whs-support.md).

## <a name="licensing"></a>Licencijavimas

Atsargų matomumo tarnyba prieinama šiose versijose:

- **Atsargų matomumo priedas, skirtas "Microsoft Dynamics 365 Supply Chain Management** " – įmonėms, turinčioms galiojančią tiekimo grandinės valdymo licenciją, atsargų matomumas galimas be papildomos licencijos išlaidų. Galite pradėti jį išbandyti šiandien. Diegimo informacijos ieškokite Įdiekite [ir nustatykite atsargų matomumą](inventory-visibility-setup.md).
- **Atsargų matomumo tarnyba kaip IOM** komponentas – ši versija skirta arba išmaniojo užsakymų valdymo (IOM) klientams arba įmonėms, kurios nenaudoja tiekimo grandinės valdymo kaip savo ERP sistemos. Licencija įtraukiama į IOM grupę. Norėdami gauti daugiau informacijos, žr. Išmaniojo [užsakymų valdymo peržiūra](/dynamics365/intelligent-order-management/overview).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
