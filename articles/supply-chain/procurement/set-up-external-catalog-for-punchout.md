---
title: Išorinio katalogo nustatymas el. įsigijimų išėjimo laikui žymėti
description: Šioje temoje aprašoma, kaip naudojant išorinį arba išėjimo katalogą galima iš tiekėjo rinkti pasiūlymo informaciją ir ją įtraukti į paraišką.
author: mkirknel
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchVendorPortalRequests, CatExternalCatalogConfiguration, CatCXMLCartLogList
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5dc6a38b1a9eebdee64762671bb501e5e1294399
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433970"
---
# <a name="set-up-an-external-catalog-for-punchout-e-procurement"></a>Išorinio katalogo nustatymas el. įsigijimų išėjimo laikui žymėti

[!include [banner](../includes/banner.md)]

Naudodami išorinį katalogą galite užtikrinti, kad produktų ir kainų informacija, kurią vėliau apdorojate „Supply Chain Management“, yra tiksli ir naujausia. Paraišką tada galima patvirtinti ir konvertuoti į pirkimo užsakymą, o užsakymą galima perduoti tiekėjui.

Kai išorinis katalogo nustatytas ir darbuotojas rengia paraišką, bus galima pasirinkti ją nukreipti į išorinę svetainę, išorinį katalogą ir grąžinti išorinėje svetainėje sukurtą pirkinių krepšelį. Šis ryšys paremtas cXML protokolu ir jį reikia nustatyti tarp pirkimo ir pardavimo organizacijų sistemų.

Kad būtų galima nustatyti ryšį, jūsų tiekėjas turi pateikti informaciją, kurią naudosite konfigūruodami išorinį katalogą, pvz., tapatybę, pirkėjo įmonės domeną, pavyzdžiui, duomenų universalios numeracijos sistemą (DUNS) ir DUNS numerį, kredencialus ir URL, kuriuo galima pasiekti tiekėjo katalogą.

## <a name="setting-up-an-external-catalog"></a>Išorinio katalogo nustatymas

Išorinis katalogas turi leisti pirkimo paraišką įvedusį darbuotoją nukreipti į išorinę svetainę, kurioje galima rinktis produktus. Produktai, kuriuos darbuotojas pasirenka iš išorinio katalogo, pateikiami su naujausia kainų informacija ir dabar juos galima įtraukti į pirkimo paraišką. Norima, kad darbuotojai negalėtų pateikti užsakymo išorinėje svetainėje. Nustatydami išorinį katalogą turite užtikrinti, kad svetainėje, kurią gali pasiekti išorinis katalogas, būtų renkama pasiūlymų informacija, o ne pateikiamas tikras užsakymas.

### <a name="to-set-up-an-external-vendor-catalog-complete-the-following-tasks"></a>Norėdami nustatyti išorinį tiekėjo katalogą, atlikite tolesnes užduotis.

1. Įsigijimo kategorijų hierarchijos nustatymas. Norėdami gauti daugiau informacijos, žr. [Įsigijimo kategorijų hierarchijų strategijų nustatymas](tasks/set-up-policies-procurement-category-hierarchies.md).
2. Užregistruokite tiekėją Tiekimo grandinės valdyme. Kad galėtumėte nustatyti konfigūracijas, kurias naudodami pasieksite išorinį tiekėjo katalogą, tiekėją ir jo kontaktą turite nustatyti tarnyboje „Microsoft Dynamics 365“. Išorinio katalogo tiekėją taip pat reikia įtraukti į pasirinktą įsigijimo kategoriją. Norėdami gauti daugiau informacijos apie tiekėjų registravimą, žr. [Tiekėjo bendradarbiavimo vartotojų valdymas](manage-vendor-collaboration-users.md). Norėdami gauti informacijos apie tai, kaip tiekėjus priskirti įsigijimo kategorijai, žr. [Tiekėjų tvirtinimas konkrečioms įsigijimo kategorijoms](tasks/approve-vendors-specific-procurement-categories.md).
3. Įsitikinkite, kad nustatyti tiekėjo naudojami matavimo vienetai ir valiuta. Norėdami gauti informacijos apie tai, kaip sukurti matavimo vienetą, žr. [Matavimo vienetų tvarkymas](../pim/tasks/manage-unit-measure.md).
4. Naudodami tiekėjo išorinio katalogo svetainės reikalavimus sukonfigūruokite išorinį tiekėjo katalogą. Daugiau informacijos apie šią užduotį žr. [Tiekėjo išorinio katalogo konfigūravimas](#configure-the-external-vendor-catalog).
5. Išbandykite tiekėjo išorinio katalogo konfigūracijas, kad patikrintumėte, ar parametrai yra tinkami, ir ar galite pasiekti išorinį tiekėjo katalogą. Naudodami veiksmą **Tikrinti parametrus** patikrinkite savo nustatytą užklausos nustatymo pranešimą. Dėl šio pranešimo išorinio tiekėjo katalogo svetainė turi būti atidaryta naršyklės lange. Tikrinimo metu negalite iš tiekėjo užsakyti prekių ir paslaugų. Norėdami užsakyti prekes ir paslaugas, tiekėjo katalogą turite pasiekti iš pirkimo paraiškos.
6. Naudodami puslapyje **Išoriniai katalogai** esantį mygtuką **Aktyvinti katalogą** išorinį katalogą suaktyvinkite. Darbuotojai išorinį katalogą galės naudoti tik jį suaktyvinus. Bet kuriuo metu galite išjungti išorinio katalogo suaktyvinimą.


## <a name="configure-the-external-vendor-catalog"></a>Tiekėjo išorinio katalogo konfigūravimas

Šiame skyriuje pateikiama daugiau informacijos apie ankstesniame skyriuje nurodytą 4 užduotį.

1. Įveskite tiekėjo išorinio katalogo pavadinimą ir aprašą. Jūsų įvestas pavadinimas bus rodomas ant krepšelio, nurodančio išorinį katalogą ir rodomo paraišką sukūrusiems darbuotojams. Spustelėję krepšelį darbuotojai gali atidaryti katalogą tiekėjo išorinio katalogo svetainėje.
2. Naudodami veiksmą **Išorinio katalogo vaizdas** įtraukite vaizdą. Vaizdas bus rodomas ant krepšelio, nurodančio išorinį katalogą ir rodomo paraišką sukūrusiems darbuotojams. Atkreipkite dėmesį, kad vaizdo plotis ir aukštis turi būti lygūs. Kitaip vaizdas nebus rodomas tinkamai.
3. Pasirinkite, ar tiekėjo išorinio katalogo svetainė turi būti rodoma tame pačiame naršyklės lange, kuriame darbuotojas sukūrė paraišką, ar ji turi būti atidaroma naujame lange.
4. Pasirinkite katalogo tiekėją. Sąraše **Juridiniai subjektai** eilutėmis pateikti visi juridiniai subjektai, kuriuose nustatytas tiekėjas. Norėdami, kad vartotojai produktų užklausas galėtų teikti tiesiogiai tiekėjo kataloge tik kai kuriuose juridiniuose subjektuose, prie kiekvieno juridinio subjekto, kuriame norite nustatyti katalogo pasiekiamumą, galite naudoti mygtukus **Neleisti prieigos** arba **Leisti prieigą**.
5. Lauke **Numatytoji galiojimo pabaiga (dienomis)** įveskite skaičių dienų, kurių metu galioja iš išorinio katalogo gautas pasiūlymas ir kurį naudojant galima pirkti iš išorinio tiekėjo. Sukūrus pasiūlymą ir jį gavus iš tiekėjo išorinio katalogo svetainės, pasiūlymas galioja nuo dabartinės sistemos datos ir galioja tokį dienų skaičių, kurį įrašėte šiame lauke.
6. Spustelėkite mygtuką **Įtraukti**, kad įsigijimo kategorijas pradėtumėte sieti su išoriniu katalogu.Tada sąraše Kategorijos pavadinimas pasirinkite kategoriją. Kategorijų sąrašas yra įsigijimo kategorijų, su kuriomis tiekėjas susietas visuose nustatytuose jo juridiniuose subjektuose, antaibis.

    > [!NOTE]
    > Įsigijimo strategijos naudojamos leidžiant arba ribojant perkančio juridinio subjekto arba priimančio valdymo vieneto prieigą prie kategorijų.Norint išeiti į išorinį katalogą, reikia leisti prieigą prie bent vienos su katalogu susietos įsigijimo kategorijos.

7. Nustatykite cXML sąrankos užklausos pranešimą, kuris bus išsiųstas tiekėjui. Automatiškai sugeneruotas pranešimo formatas yra minimalus šablonas, kurio reikia norint pradėti seansą. Įveskite žymių reikšmes.

Sistemos sugeneruotą pranešimo šabloną galite bet kuriuo metu iš naujo įkelti spustelėdami **Atkurti pranešimo formatą**. 
Atkreipkite dėmesį, kad, atkūrus pranešimo formatą, dabartinį pranešimą pakeis automatiškai sugeneruotas pranešimo formatas, kurio žymės yra tuščios.

### <a name="cxml-setup-message"></a>cXML sąrankos pranešimas
Toliau galite rasti į šabloną įtrauktų žymių aprašą.

| Laukas | aprašymas | 
|---------|---------|
|< Header >< From >< Credential domain=”” >|Pirkėjo įmonės domenas.|
|< Header >< From >< Credential>< Identity >< /Identity > | Pirkėjo įmonės tapatybė.|
|< Header >< To >< Credential domain=”” > | Tiekėjo įmonės domenas.|
|< Header >< To >< Credential>< Identity >< /Identity> | Tiekėjo įmonės tapatybė.|
|< Header >< Sender >< Credential domain=”” > | Pirkėjo įmonės domenas.|
|< Header >< Sender >< Credential >< Identity >< /Identity> | Pirkėjo įmonės tapatybė.|
|< Header >< Sender >< Credential >< SharedSecret >< /SharedSecret >|Pirkėjo įmonės bendrinamas slaptasis raktas.|
|< Request deploymentMode=”” >|Visuotinė bandomoji arba gamybos įdiegtis.|
|< Request >< PunchOutSetupRequest >< SupplierSetup >< URL >< /URL>|Tiekėjo išėjimo galinio punkto URL.|

### <a name="extrinsic-elements"></a>Neesminiai elementai

Išorinis elementas yra papildoma informacija, pvz., išeinančio vartotojo vardas. Išorinis elementas nustatomas išeinant ir jį galima siųsti užklausos nustatymo pranešime.
Jūsų tiekėjas gali reikalauti neesminį elementą gauti sąrankos užklausoje. Tokiu atveju neesminį elementą turite įtraukti į neesminių elementų sąrašą, esantį puslapio **Išorinis katalogas** skyriuje **Pranešimo formatas**.
Nurodykite neesminio elemento pavadinimą, kurį galėtų atpažinti tiekėjas, ir susiekite jį su reikšme. Reikšmių parinktys: Vartotojo vardas, Vartotojo el. pašto adresas arba Atsitiktinė reikšmė.
Daugiau informacijos apie cXML protokolą rasite [cXML.org svetainėje](http://cxml.org/).

## <a name="post-back-message"></a>Grįžtamojo registravimo pranešimas
Grįžtamojo registravimo pranešimas – tai iš tiekėjo gaunamas pranešimas, kai vartotojas išsiregistruoja iš išorinės svetainės ir grįžta į Tiekimo grandinės valdymą. Grįžtamojo registravimo pranešimų konfigūruoti negalima. Pranešimai paremti cXML protokolo apibrėžtimi.Čia pateikiama informacija, kuri gali būti siunčiama grįžtamojo registravimo pranešime, kuris gaunamas paraiškos eilutėje.

| Iš tiekėjo gautas pranešimas | Nukopijuota į paraiškos eilutę|
|------------------------------|----------------------------------------------------------|
|< ItemIn quantity=”” > |Kiekis|
|< ItemIn>< ItemID >< SupplierPartID >< /SupplierPartID >|Išorinis prekės ID|
|< ItemDetail>< UnitPrice >< Money currency=”” >| Valiuta|
|< ItemDetail >< UnitPrice >< Money >< /Money >| Vnt. kaina|
|< ItemDetail >< Description ShortName=”” >|Produkto pavadinimas|
|< ItemDetail >< Description >< /Description >|Įtraukta į prekės aprašą; produkto pavadinimas, jei nenurodyta ShortName.|
|< ItemDetail >< UnitOfMeasure >< /UnitOfMeasure >|Vienetas|
|< ItemDetail >< Classification >< /Classification >|Įtraukta į prekės aprašą|
|< ItemDetail >< Classification domain=”” >|Įtraukta į prekės aprašą|

## <a name="delete-an-external-catalog"></a>Išorinio katalogo naikinimas
Panaikinti išorinį katalogą galite naudodami puslapyje esantį veiksmą Naikinti.

Jei pateikta produkto iš tiekėjo išorinio katalogo užklausa, tiekėjo išorinio katalogo panaikinti negalima. Vietoj to tiekėjo išorinio katalogo būsena nustatoma kaip neaktyvi. Jei norite pašalinti prieigą prie tiekėjo išorinio katalogo svetainės, tačiau nenorite jos panaikinti, išorinio katalogo būseną pakeiskite į Neaktyvus.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Pirkimo „cXML“ patobulinimai](purchasing-cxml-enhancements.md)
- [Išorinių katalogų naudojimas el. įsigijimų išėjimo laikui žymėti](use-external-catalogs-for-punchout.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]