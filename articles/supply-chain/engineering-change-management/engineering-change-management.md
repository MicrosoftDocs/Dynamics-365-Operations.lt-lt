---
title: Valdyti inžinerinių produktų keitimus
description: Šioje temoje pateikta informacija apie inžinerinių keitimų valdymą. Inžinerinių keitimų valdymas suteikia struktūruotus procesus inžinerinių produktų valdymo keitimams, nuo siūlymo, užklausų ir keitimų atlikimo iki peržiūros ir keitimų patvirtinimo, jų poveikio vertinimo esančioms perlaidoms ir jų sekimo.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEcmRequestSelection,EngChgEcmRequestProducts,EngChgEcmRequestPriorityChart,EngChgEcmRequestListPage,EngChgEcmRequestFilteredPart,EngChgEcmRequestDetails,EngChgEcmReason,EngChgEcmProjTableInformation,EngChgEcmProductRoute,EngChgEcmProductRelease,EngChgEcmProductPreview, EngChgEcmWhereUsed, EngChgEcmInventTrans,EngChgEcmHeaderSelection,EngChgEcmHeaderPreviewPart,EngChgEcmHeaderFilteredPart,EngChgEcmHeaderDetails, EngChgCaseWhereUsedAnalysis, EngChgCaseValidatorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 55952a9b1c25b806ee4a21ef1982c5b15a41adeb9c9bfdf2fccb8c9da242ffdb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714335"
---
# <a name="manage-changes-to-engineering-products"></a>Valdyti inžinerinių produktų keitimus

[!include [banner](../includes/banner.md)]

Inžinerinių keitimų valdymas suteikia struktūruotus procesus keitimų valdymui ir inžineriniams produktams. Galite naudoti *inžinerinių pakeitimų užklausą* procesą, kad siūlytumėte ir prašytumėte keitimų ir tada naudoti *inžinerinių keitimų užsakymo* procesą, kad iš tiesų atliktumėte tuos pakeitimus. Vartotojas gali sukurti inžinerinių keitimų užklausas ar inžinerinių keitimų užsakymas ir tuomet sutvarkyti juos peržiūrai ir patvirtinimui bei jų poveikio vertinimui esančioms perlaidoms ir jų sekimo.

## <a name="engineering-change-requests"></a>Inžinerinių pakeitimų užklausos

Inžinerinių keitimų užklausos procesas jums leidžia apimti keitimų užklausas iš visų atitinkamų skyrių į savo bendrovę. Nesvarbu, ar dirbate kaip inžinierius ar Gamyboje, Ištekliuose, Sandėlyje ar Prekybos skyriuje: visi žmonės gali naudoti inžinerinių pakeitimų užklausą į užklausos keitimą. Šis keitimas gali tapti idėja naujam produktui, problema, kurią suradote dirbdami savo vietoje su esančiu produktu, pasiūlymas jo gerinimui ar bet kas kita.

Kai asmuo pateikia užklausą keitimui, *peržiūros ir patvirtinimo* procesą tvarko darbo eiga, kuri nustato, kas turi patvirtinti keitimą (pavyzdžiui, produkto savininkas).

Norėdami nustatyti darbo eigą inžinerijos keitimo užsakymams ar inžinerijos keitimo užklausoms, eikite į **Inžinerijos keitimo valdymas \> Inžinerijos darbo eigos**. Rinkitės **Naujas**, pasirinkite, ar darbo eiga bus naudojama siekiant peržiūrėti inžinerijos keitimo užsakymus ar inžinerijos keitimo užklausas ir tuomet konfigūruokite darbo eigą.

Dėl daugiau informacijos apie darbo eigas, žr. [Darbo eigos sistemos apžvalga](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md). Išsamesnės informacijos apie produkto savininkus rasite [Produkto savininkai](product-owner.md).

### <a name="create-a-new-engineering-change-request"></a>Kurti naują inžinerinių pakeitimų užklausą

Norėdami sukurti inžinerinių pakeitimų užklausą, atlikite vieną iš šių žingsnių.

- Eikite į **Inžinerinių pakeitimų valdymas \> Bendri \> Inžinerinių pakeitimų valdymas \> Inžinerinių pakeitimų užklausos** ir tuomet pasirinkite **Naujas** veiksmų juostoje.
- Atverkite **Produkto išsamios informacijos** puslapį dėl esančio inžinerinio produkto. Tada veiksmų juostoje, skirtuke **Inžinierius**, **Inžinerinių pakeitimų valdymas** grupėje rinkitės **Inžinerinių pakeitimų užklausos \> Nauja inžinerinių pakeitimų užklausa**.

Nauja keitimo užklausa yra sukurta. Dabar galite nustatyti laukelius kiekviename „FastTab“, kaip aprašyta tolesniuose poskyriuose.

#### <a name="general-fasttab"></a>Bendras „FastTab“ skirtukas

„FastTab“ **Bendri** leidžia jums pateikti bendrą keitimų užklausos aprašą. Tolesnė lentelė aprašo laukelius šiame „FastTab“.

| Laukas | aprašymas |
|---|---|
| Keitimo užklausa | Įveskite inžinerinių pokyčių užklausos vardą. |
| Kreipinys | Įveskite tekstą, kuris trumpai aprašo ar nustato pokyčius užklausoje. |
| Pirmenybė | Pasirinkite vertę norėdami nurodyti, kokio pirmenybinio lygio yra pokytis. Galite tinkinti esamas savo įmonės vertes, kaip būtina. (Dėl daugiau informacijos, žr. [Sukurti bendras vertes inžinerinio pokyčio valdymui](engineering-change-management-setup.md).) |
| Kategorija | Pasirinkite vertę, kad aprašytumėte pokyčio tipą, kurio prašote. Galite tinkinti esamas savo įmonės vertes, kaip būtina. (Dėl daugiau informacijos, žr. [Sukurti bendras vertes inžinerinio pokyčio valdymui](engineering-change-management-setup.md).) |
| Svarba | Pasirinkite vertę, kad nurodytumėte problemos sunkumą, kurią reikia pataisyti įgyvendinant užklausą. Galite tinkinti esamas savo įmonės vertes, kaip būtina. (Dėl daugiau informacijos, žr. [Sukurti bendras vertes inžinerinio pokyčio valdymui](engineering-change-management-setup.md).) |
| Pageidauja | Užklausą sukūrusio vartotojo vardas. |
| Įjungta | Sukurto užklausos data. |
| Būsena | Užklausos būsena. Pirmą kartą sukūrus užklausą, būsena yra *Sukurta*. Patvirtinus užklausą, jos būsena pasikeičia į *Patvirtinta*. Jei susijęs pakeitimo užsakymas buvo sukurtas užklausai, pokyčio būsena yra *Sekama*. |
| Pakeitimų užsakymas | Užsakymo numerio keitimui, jei keitimo užklausa buvo sekama per keitimo užsakymą. |

#### <a name="information-fasttab"></a>„FastTab“ su informacija

„FastTab“ su **Informacija** jums leidžia įtraukti daugiau informacijos apie užklausą.

Norėdami įtraukti eilutę į tinklelį, rinkitės **Naujas** įrankių juostoje virš tinklelio ir tada rinkitės vieną iš tolesnių parinkčių:

- **Failas** – Įkelkite failą.
- **Paveikslėlis** – Įkelkite paveikslėlio failą.
- **Pastaba** – Įveskite pastabą tiesiai į tinklelį.
- **URL** – Įveskite URL tiesiai į tinklelį.

Tolesnė lentelė aprašo laukelius kiekvienoje eilutėje.

| Laukas | aprašymas |
|---|---|
| Sukūrimo data ir laikas | Laikas ir data, kai eilutė buvo sukurta. |
| Tipas | Šio tipo informacija, kuriai eilutė buvo sukurta (failas, paveikslėlis, pastaba ar URL). |
| aprašymas | Įveskite eilutės aprašą. |
| Apribojimai | Vertė, kuri rodo, ar įtraukta informacija atėjo iš vidaus ar išorės šaltinio. |
| Pridėta | Pasirinktas žymimas laukelis rodo, ar eilutė apima priedą (failą ar paveikslėlį). Norėdami atsisiųsti priedą, pasirinkite eilutę ir tada pasirinkite **Atverti** įrankių juostoje virš tinklelio. |

#### <a name="products-fasttab"></a>Produktų „FastTab“

„FastTab“ **Produktai** jums leidžia išvardyti visus produktus paveiktus pokyčio užklausos. Galite naudoti mygtukus įrankių juostoje, kad įtrauktumėte į tinklelį produktus arba panaikintumėte juos.

Sąrašas yra tik informaciniais tikslais. Dėl to, galite įtraukti kiek norite susijusių produktų. Jei sukuriate pokyčio užklausą iš **Produkto išsamios informacijos** puslapio apie esamą produktą, tas produktas turi būti įvardytas **Produktai** „FastTab“ po to, kai įrašote užsakymo įrašą.

#### <a name="source-fasttab"></a>Šaltinio „FastTab“

„FastTab“ **Šaltinis** leidžia jums sekti keitimo užklausos pradžios tašką. Jis naudingas, jei norite pažiūrėti, ar keitimo užklausa buvo sukurta iš prekybos užsakymo, kas ją sukūrė ir kurioje bendrovėje.

### <a name="evaluate-the-business-impact-of-a-change-request-and-send-notifications"></a>Įvertinkite keitimo užklausos verslo poveikį ir siųskite pranešimus

Jei norite peržiūrėti keitimo užklausą, ieškokite priklausinių. Tokiu būdu, galite įvertinti keitimo užklausos poveikį atviroms perlaidoms, tokioms kaip prekybos, gamybos užsakymai ir turimas inventorius. Kai peržiūrite keitimo užklausas, galite siųsti pranešimus žmonėms, kurie yra atsakingi už įvairių tipų susijusių užsakymų įvykdymą.

#### <a name="review-affected-transactions-block-selected-transactions-and-send-notifications"></a>Peržiūrėkite paveiktas operacijas, užblokuokite pasirinktas operacijas ir siųskite pranešimus

Norėdami peržiūrėti paveiktas operacijas, užblokuoti pasirinktas operacijas ir siųsti susijusius pranešimus, atlikite šiuos veiksmus.

1. Eikite į **Inžinerinių pakeitimų valdymas \> Bendri \> Inžinerinių pakeitimų valdymas \>Inžinerinių pakeitimų užklausos**.
1. Atvėrus esamą keitimo užklausą ar pasirinkus **Nauja** veiksmų juostoje tam, kad sukurtumėte naują keitimo užklausą.
1. Veiksmų juostoje skirtuke **Keitimo užklausa** grupėje **Verslo poveikis** rinkitės vieną iš tolesnių mygtukų:

    - **Ieškoti** – Nuskaito visas atviras perlaidas ir tada atveria **Verslo poveikis atvirai perlaidai** teksto laukelį, kuriame įvardytos visos perlaidos, kurias paveiks pokytis.
    - **Peržiūrėti ankstesnę paiešką** – Atverkite **Verslo poveikio atviroms perlaidoms** teksto laukelį, kuriame įrašyti ankstesnės paieškos rezultatai. (Nauja paieška nebaigta.)

1. Dialogo lange **Verslo poveikis atviroms operacijoms** pateikiamas skirtukų rinkinys, iš kurių kiekvienas rodo tam tikro tipo paveiktų operacijų sąrašą (**Pardavimo užsakymai**, **Pirkimo užsakymai**, **Gamybos užsakymai**, **Atsargos** ir taip toliau). Kiekviename skirtuke taip pat yra rodomas skaičius, nurodantis paveiktų to tipo operacijų skaičių. Pasirinkite skirtuką, kad peržiūrėtumėte aktualų sąrašą.
1. Norėdami dirbti su operacija sąraše, pasirinkite ją ir vieną iš šių įrankių juostos mygtukų:

    - **Peržiūrėti operaciją** – Atidaro pasirinktą operacijos įrašą.
    - **Blokuoti užsakymą** – Šis mygtukas galimas tik **Pardavimo užsakymų** skirtuke Pasirinkite jį, kad užblokuotumėte pasirinktą pardavimo užsakymą.
    - **Blokuoti eilutę** – Šis mygtukas galimas tik **Pirkimo užsakymų** skirtuke Pasirinkite jį, kad užblokuotumėte pasirinktą pirkimo užsakymo eilutę.
    - **Pranešti atsakingam asmeniui** – Šis mygtukas galimas tik **Pardavimo užsakymų** skirtuke Pasirinkite jį, kad išsiųstumėte pranešimą apie pakeitimą vartotojui, atsakingam už pasirinktą pardavimo užsakymą.
    - **Pranešti užsisakiusiam asmeniui** – Šis mygtukas galimas tik **Pirkimo užsakymų** skirtuke Pasirinkite jį, kad išsiųstumėte pranešimą apie pakeitimą vartotojui, atlikusiam pasirinktą pirkimo užsakymą.
    - **Pranešti apie gamybą** – Šis mygtukas galimas tik **Gamybos užsakymų** skirtuke Skirtingai nuo pardavimo ir pirkimo užsakymų, gamybos užsakymuose nėra vieno vartotojo, kuris nustatytas kaip pilnai atsakingas už juos. Vietoj to, keli prižiūrėtojai arba planuotojai įprastai vadovauja konkrečiai vietai arba gamybos daliai (pavyzdžiui, konkretiems ištekliams arba išteklių grupėms). Todėl, kai pasirenkate šį mygtuką, visi vartotojai, atsakingi už bet kuriuos išteklius, susijusius su pasirinktu gamybos užsakymu, gauna pranešimą apie pakeitimą.
    - **Pranešti rengėjui** – Šis mygtukas galimas tik **Pirkimo paraiškų** skirtuke Pasirinkite jį, kad išsiųstumėte pranešimą apie pakeitimą vartotojui, nustatytam kaip pasirinktos pirkimo paraiškos rengėjui.
    - **Pranešti atsakingam pardavėjui** – Šis mygtukas galimas tik **Pasiūlymų** skirtuke Pasirinkite jį, kad išsiųstumėte pranešimą apie pakeitimą vartotojui, atsakingam už pasirinktą pasiūlymą.
    - **Nurašyti** – Šis mygtukas galimas tik **Atsargų** skirtuke Pasirinkite jį, jei norite nurašyti pasirinktas atsargas.
    - **Peržiūrėti retrospektyvą** – Atidaro pasirinktos operacijos veiksmų retrospektyvą naudodamas **Verslo poveikio atviroms operacijoms** dialogo langą. (Pavyzdžiui, retrospektyva parodo, ar pranešimai buvo išsiųsti, ar operacijos buvo užblokuotos.) 
    - **Peržiūrėti visas operacijas** – Atidaromas pilnas visų operacijų sąrašas, o ne tik atidarytos operacijos.

#### <a name="review-and-process-change-notifications-for-transactions"></a>Peržiūrėkite ir apdorokite operacijų pakeitimų pranešimus

Galite skaityti ir apdoroti pakeitimų pranešimus, kuriuos gaunate šiais būdais:

- Tačiau gamybos užsakymų atveju, pranešimai apie operacijų, už kurias esate atsakingi, pakeitimus atsiranda Veiksmų centre. Mygtukas **Rodyti pranešimus** (skambučio simbolis), esantis dešinėje naršymo meniu pusėje, nurodo, kada pranešimas jums bus pasiekiamas Veiksmų centre. Pasirinkite mygtuką **Rodyti pranešimus** Veiksmų centrui atidaryti ir pranešimams peržiūrėti.
- Norėdami peržiūrėti visus gamybos užsakymus, kuriems buvo išsiųstas inžinerinis pranešimas, eikite į **Gamybos užsakymai \> Gamybos užsakymai \> Visi gamybos užsakymai**. Tada Veiksmų juostos skirtuke **Gamybos užsakymas**, esančiame **Inžinerinio pakeitimų užklausų** grupėje, pasirinkite **Inžineriniai pranešimai** tam, kad atidarytumėte **Inžinerinių pranešimų** puslapį.
- Gamybos užsakymuose galite pasirinkti peržiūrėti tik tuos pakeitimų pranešimus, kurie taikomi jūsų valdomiems gamybos ištekliams. Veiksmų srities **Gamybos vietos valdymo** darbo srityje pasirinkite **Konfigūruoti mano darbo sritį** puslapio filtravimui, kad jame būtų pateikta tik informacija apie jūsų valdomus gamybos vienetus, grupes ir (arba) išteklius. Skyriaus **Suvestinė** plytelėje, pavadintoje **Gamybos užsakymai su pakeistais produktai**, rodomas pranešimų, atitinkančių jūsų filtro parametrus, skaičius. Pasirinkite šią plytelę, kad atidarytumėte **Inžinerinių pranešimų** puslapį, kuriame rodomas pilnas operacijų, atitinkančių jūsų filtro kriterijus, sąrašas.

Kai peržiūrite gamybos užsakymo pranešimus **Inžinerijos pranešimų** puslapyje, galite vadovautis saitais į susijusius pakeitimo arba gamybos užsakymus, pasirinkdami stulpelių vertes arba naudodami susijusias komandas Veiksmų srityje. Įvertinę pakeitimą ir kaip reikalinga, atšaukę ar modifikavę gamybos užsakymus, galite pažymėti pranešimą kaip išspręstą. Pasirinkite pranešimą, o tada Veiksmų srityje pasirinkite **Išspręsti**. Pranešimas yra pašalinamas iš visų vartotojų rodinių.

### <a name="create-a-change-order-from-a-change-request"></a>Sukurkite pokyčių užsakymą iš užklausos

Inžinierius gaunantis inžinerijos pokyčių užklausą gali sukurti inžinerijos pokyčių užsakymą tiesiai iš **Inžinerijos pokyčių užklausų** puslapio. Veiksmų juostoje skirtuke **Pokyčių užklausa** grupėje **INžinerijos pokyčių užsakymas** rinkitės **Kopijuoti nuorodą ir produktus**.

## <a name="engineering-change-orders"></a>Inžinerinių pakeitimų užsakymai

Inžinerinių keitimų užsakymai pateikia struktūruotą procesą keitimų inžinerijos produktams padarymą. Siūlote keitimus naudodami inžinerijos duomenų kopiją. Realūs pagrindiniai duomenys yra nepaveikti. Dėl daugiau informacijos apie inžinerijos duomenis, žr. [Inžinerijos versijos ir inžinerijos produkto kategorijos](engineering-versions-product-category.md).

Galite sukurti inžinerinio keitimo užklausa patvirtinamą, pagrįstą patvirtinta inžinerinių keitimų užklausa. Inžinieriai taip pat gali sukurti inžinerinių keitimų užsakymus nuo pradžios. Galite įtraukti keletą produktų į vieną inžinerinių keitimų užsakymą atlikdami vieną iš šių veiksmų:

- Rankiniu būdu pasirinkite produktus.
- Naudokite komplektavimo specifikaciją (KS), kad įtrauktumėte produktus, kurie yra žemesnėje produkto struktūroje (tai yra, vaikiškoje).
- Naudokite paiešką, kad įtrauktumėte produktus, kurie yra aukštesnėje produkto struktūroje (tai yra, tėvų).

Po to, kai pokyčių užklausa baigta, peržiūrėkite ir patvirtinkite procesą vykdydami darbo eigą. Galite nustatyti kitas darbo eigas pagal pirmenybę ir sunkumą.

Norėdami nustatyti darbo eigą inžinerijos keitimo užsakymams ar inžinerijos keitimo užklausoms, eikite į **Inžinerijos keitimo valdymas \> Inžinerijos darbo eigos**. Rinkitės **Naujas**, pasirinkite, ar darbo eiga bus naudojama siekiant peržiūrėti inžinerijos keitimo užsakymus ar inžinerijos keitimo užklausas ir tuomet konfigūruokite darbo eigą.

Dėl daugiau informacijos apie darbo eigas, žr. [Darbo eigos sistemos apžvalga](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).

Toliau pateikiami tipiniai akcininkai, kurie gali patvirtinti inžinerijos pokyčio užsakymą:

- **Produkto savininkai** – Išsamesnės informacijos apie produkto savininkus rasite [Produkto savininkai](product-owner.md).
- **Atsakingas komandos vadovas** – Laukelis **Inžinierius** rodinyje **Antraštė** inžinerinių pokyčių užsakymas rodo inžinierių, kuris sukūrė inžinerinių pokyčių užsakymą. Jei inžinierius priklauso komandai, kuri nustatyta sistemoje, laukelis **Atsakingas** rodo tos komandos lyderį.
- **Finansų skyrius** – Finansų skyriui gali reikėti peržvelgti atvejus, kai keitimas apima didelius kaštus.

Galite pasirinkti, ar inžinerinių pokyčių užsakymas bus sutvarkomas tiesiogiai po jo patvirtinimo kaip darbo eigos dalis, ar tvarkymas turi būti atliekamas vėliau kaip rankinis žingsnis. Inžinerinių pokyčių užsakymo tvarkymo metu, inžineriniai duomenys realiame produkte yra naujinami.

Jums peržiūrint pokyčių užsakymą veiksmų juostoje, skirtuke **Pokyčių užklausa** grupėje **Verslo poveikis** rinkitės **Paieška** tam, kad įvertintumėte siūlyto atvirų perlaidų keitimo poveikį, tokį kaip prekybos užsakymai, gamybos užsakymai ar turimas inventorius. Rezultatai yra rodomi **Verslo poveikis atviroms perlaidoms** teksto laukelyje, kuriame galite pasirinkti paveiktas perlaidas ir tada naudoti komandas įrankių juostoje, kad peržiūrėtumėte daugiau informacijos, įspėtumėte atsakingą vartotoją ar perlaidą užblokuotumėte.

### <a name="engineering-change-orders-in-engineering-or-operational-companies"></a>Inžinerinių pokyčių užsakymai inžinerijos ar veikiančiose bendrovėse

Kaip aprašyta [Inžinerinės bendrovės ir duomenų turėjimo taisyklės](engineering-org-data-ownership-rules.md), produkto duomenys, kuriuos galite redaguoti keičiasi priklausomai nuo juridinio asmens tipo, kuriame dirbate (inžinerinėje ar vykdančioje bendrovėje). Duomenų nuosavybės taisyklės taip pat taikomos inžinerijos pokyčių užsakymams. Dėl to, priklausomai nuo jūsų sukurto inžinerinių pokyčių užsakymo juridiniame asmenyje, skirtingai pokyčių tipai gali būti sukurti. Štai keletas pavyzdžių:

- Inžinerijos pokyčių užsakymas *inžinerijos bendrovėje*, galite atlikti pagrindinius pokyčius inžinerijos duomenims. Pavyzdžiui, galite sukurti naujas produkto versijos, keisti produkto struktūrą per BOM ir keisti inžinerijos atributų vertę. Kiekvienam paveiktam produktui pasirinkite vieną iš tolesnių verčių **Poveikio** laukelyje:

    - **Jokių** – Naujinkite esančia produkto versiją (versijos naujinimas).
    - **Nauja versija** – Kurkite naują versiją pagrįstą pasirinkto produkto versija.
    - **Nauja produktas** – Kurkite visai naują produktą ar jo variantą pagrįstą pasirinkto produkto versija.
    - **Naujas variantas** – Kurkite naują variantą pagrįstą pasirinkto produkto versiją. Bus nukopijuota jos BOM ir maršruto informacija.

- Inžinerijos pokyčių užsakymas *veikimo bendrovėje*, galite keisti logistinius produkto duomenis. Pavyzdžiui, galite praturtinti esantį BOM su nustatymais šaltinių, įtraukti vietinius maršrutus ar vietinius BOM ir papildyti BOM įtraukdami naujas BOM eilutės pakavimo medžiagoms, sutepimo skysčiams ar instrukcijoms vietine kalba. Papildymai, kuriuos daro vartotojai vykdančiojoje bendrovėje bus išsaugoti, kai nauji naujiniai siunčiami iš inžinerijos bendrovės. Dėl daugiau informacijos, žr. [Inžinerijos bendrovės ir duomenų turėjimo taisyklės](engineering-org-data-ownership-rules.md).

    Kai inžinerijos pokyčių užsakymai tvarkomi inžinerijos bendrovėje, gaminiai sukuriami ir (arba) naujinami tik inžinerijos bendrovėje. Dėl to, jei pagrindiniai duomenys turi būti naujinami, turite paleisti produktus į vykdymo bendroves.

- Galite leisti produktus tiesiai iš inžinerijos pokyčių užsakymų. Atverkite pokyčio užsakymą ir tada veiksmų juostoje skirtuke **Pokyčių užsakymas** grupėje **Produkto leidimai** rinkitės **Leidžiamo produkto struktūra**. Procesas veikia taip kaip jis veikia jums leidžiant produktus iš **Leidžiami produktai** puslapio. Dėl daugiau informacijos, žr. [Leidžiamo produkto struktūros](release-product-structure.md).
- Galite išleisti produktus automatiniu būdu iš inžinerijos keitimų užsakymų pagal šiuos faktorius:

    - Pakartotiniai išleidimai bendrovėms, kuriose produktai buvo anksčiau išleisti. Rinkitės **Ieškoti** tam, kad nuskaitytumėte ankstesnius leidimus ir tada rinkitės **Peržiūrėti** tam, kad peržiūrėtumėte rezultatus. Puslapis **Rodinys** rodo ankstesnius produktų leidimus ir galite pasirinkti, kuriuos produktus norite leisti iš naujo. Tada užverkite **Rodinio** puslapį ir rinkitės **Tvarkyti** tam, kad pakartotinai išleistumėte pasirinktus produktus.
    - Automatinio leidimo nustatymai leidimo inžinerijos produkto kategorijos valdymui. Galite atlikti šį leidimą kaip darbo eigos dalį. Kai **surinkti leidimo pasiūlymo** blokavimas naudojamas, išleidimo pasiūlymas bus užpildytas su papildomo leidimo pasiūlymais (žr. ankstesnį prekių sąrašą) ir produktai bus išleisti į bendroves, jei **Automatinio leidimo** žymimas laukelis pasirinktas leidimo inžinerinių produkto kategorijos valdyme. Galite rinktis **Peržiūrėti** tam, kad peržiūrėtumėte rezultatus kaip aprašyta ankstesniame prekių sąraše. Produktai taip pat bus išleisti, jei **tvarkymo išleidimo pasiūlymo** blokavimas naudojamas. Jums pasirinktus tik surinkti išleidimo pasiūlymą kaip darbo eigos dalį, galite rankiniu būdu pradėti išleidimą pasirinkę **Tvarkyti**, kaip aprašyta ankstesniame sąraše.

## <a name="follow-up-on-an-engineering-change-request-via-an-engineering-change-order"></a>Sekite inžinerinių keitimų užklausą per inžinerinių keitimų užsakymą.

Kai tik inžinerinio keitimo užklausa patvirtinama, galite laikytis jos per inžinerijos keitimo užsakymą. Galite derinti keletą inžinerijos keitimo užklausų į vieną inžinerijos keitimo užsakymą. Vienas inžinerijos keitimo užsakymas gal net turėti keletą produktų. (Dažniausiai naudosite šią prieigą kai tas pats pakeitimas turi būti taikomas keliems produktams.) Nepaisant to, negalite sukurti kelių inžinerijos keitimo užsakymų iš vienos inžinerijos keitimo užklausos.

Norėdami sekti keitimo užklausą per keitimo užsakymą, atverkite keitimo užklausą ir tada veiksmų juostoje **Keisti užsakymą** skirtuke, grupėje **Inžinerinių keitimų užsakymas** rinkitės **Kopijuoti nuorodą ir produktus**. Galite tada pasirinkti esamą inžinerinių keitimų užsakymą, kad sujungtumėte keitimą su juo arba galite sukurti šį užsakymą tai konkrečiai užklausai.

## <a name="engineering-change-order-report"></a>Inžinerinių pakeitimų užsakymo ataskaita

Inžinerinių keitimų užsakymo ataskaitos aprašo keitimus, kurie atliekami inžinerinių keitimų užsakyme. Jie naudingi tiek per, tiek ir po peržiūros ir patvirtinimo proceso.

Norėdami peržiūrėti inžinerinių keitimų užsakymo ataskaitą, atverkite atitinkamą keitimo užsakymą ir tada veiksmų juostoje **Keisti užsakymą** skirtuke, grupėje **Peržiūrėti** rinkitės **Inžinerinių keitimų užsakymo ataskaita**.

## <a name="fields-on-an-engineering-change-order"></a>Laukeliai inžinerijos keitimo užsakyme

Didžioji dalis laukelių inžinerijos keitimo užsakymuose yra tokie patys kaip ir išleistuose produktuose, inžinerijos versijose, dokumentuose, KS (eilutėse) ir maršrutuose (operacijose). Nepaisant to, laukeliai tolesnėje lentelėje yra unikalūs keitimo užsakymams.

| Laukas | aprašymas |
|---|---|
| Inžinerinių pakeitimų priežastys | Pasirinkite paveikto produkto keitimo priežastį. |
| Pakeitimo aprašas | Įveskite keitimo aprašą. |
| Reikalingi specialūs įrankiai | Nurodykite, ar specialūs įrankiai būtini keitimo taikymui. |
| Inžinerinių medžiagų pristatymas | Pasirinkite medžiagų utilizavimo kodą bet kurioms atliekoms, kurios padaromos taikant keitimą. |
| Reikalingas kliento patvirtinimas | Nurodykite, ar kliento patvirtinimas yra būtinas prieš keitimo taikymą. |
| Gautas kliento patvirtinimas | Nurodykite kliento patvirtinimo būseną. |
| Aplinkos sveikata ir sauga | Nurodykite, ar aplinkos sveikatos ir saugos taisyklės taikomos keitimui. Jei taip, galite tada pasirinkti taikomas taisykles. |

Galite naudoti **Laikymo/kopijavimo keitimo informacijos** mygtuką, kad kopijuotumėte keitimo informaciją tarp paveiktų produktų.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
