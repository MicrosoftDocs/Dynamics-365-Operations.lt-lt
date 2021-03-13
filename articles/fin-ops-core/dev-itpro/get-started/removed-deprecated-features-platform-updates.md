---
title: Pašalintos arba nebenaudojamos platformos funkcijos
description: Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama šalinti iš „Finance and Operations“ programų platformos naujinių.
author: sericks007
manager: AnnBe
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: d57182aa34c4897ef3703d0f8ed08d032c261170
ms.sourcegitcommit: 79621e667cd7f48ba3bdbf2731f6f33d8e9f57f6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5154092"
---
# <a name="removed-or-deprecated-platform-features"></a>Pašalintos arba nebenaudojamos platformos funkcijos

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama šalinti iš „Finance and Operations“ programų platformos naujinių.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Šis sąrašas skirtas suteikti jums informacijos apie pašalintas ir nebenaudojamas funkcijas, kad galėtumėte geriau planuoti savo darbą. 

Išsamios informacijos apie „Finance and Operations“ programų objektus rasite skyriuje [Techninės informacijos ataskaitos](https://docs.microsoft.com/dynamics/s-e/). Galite palyginti skirtingas šių ataskaitų versijas, kad sužinotumėte apie objektus, kurie buvo pakeisti ar pašalinti kiekvienoje iš „Finance and Operations“ programų versijų.

## <a name="feature-removed-effective-january-28-2021"></a>Funkcija bus pašalinta nuo 2021 m. sausio mėn 28 d.

### <a name="batch-job-to-handle-sql-index-defragmentation"></a>Paketinė užduotis SQL indekso defragmentavimui apdoroti

|   |  |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Ši funkcija buvo pašalinta norint sumažinti klientų rodyklės valdymo vykdymo, stebėjimo ir priežiūros pridėtines išlaidas. |
| **Pakeitė kita funkcija?**   | Ateityje rodyklės priežiūrą atliks „Microsoft” tarnybos. Tai bus daroma nuolat, nepaveikiant vartotojo darbo krūvių. |
| **Paveiktos produkto sritys**         | „Finance and Operations” programėlės|
| **Visuotinio diegimo parinktis**              | Debesies diegimas – paveikia „Microsoft” valdomas gamybos ir 2‑5 pakopų smėlio dėžės aplinkas. |
| **Būsena**                         | Ši funkcija yra pašalinta. |


## <a name="platform-updates-for-version-10017-of-finance-and-operations-apps"></a>„Finance and Operations” programų 10.0.17 versijos platformos naujinimai

> [!IMPORTANT]
> 10.0.17 versija prieinama kaip peržiūros versijos leidimo dalis. Turinys ir funkcijos gali būti keičiami. Norėdami apie peržiūros leidimus gauti daugiau informacijos, žr. [DUK apie vienos versijos paslaugų naujinimus](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).

### <a name="visual-studio-2015"></a>„Visual Studio 2015“

|   |  |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Norint, kad būtų palaikomos naujausios „Visual Studio” versijos, reikia atlikti tam tikrus X + + plėtinių, skirtų „Visual Studio”, keitimus. Šie pakeitimai nesuderinami su „Visual Studio” 2015. |
| **Pakeitė kita funkcija?**   | „Visual Studio 2017” bus pakeista „Visual Studio 2015” kaip įdiegta ir reikalinga versija. |
| **Paveiktos produkto sritys**         | „Visual Studio“ kūrimo įrankiai |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nebenaudojama. Atnaujinus, ankstesni X++ įrankiai bus pašalinti iš 2015 m. „Visual Studio”, o atnaujinti įrankiai nebus įdiegti 2015 m. „Visual Studio”. Tai neturės įtakos nuomojamoms komponavimo versijoms. Komponavimo versijos virtualiosios mašinos pardavimo galimybės (komponavimo versijos apibrėžimas) turi būti atnaujintos rankiniu būdu tam, kad pakeisti priklausomybę iš „MSBuild 14.0” (2015 m. „Visual Studio”) į „MSBuild 15.0” (2017 m. „Visual Studio”), kaip aprašyta [Senstelėjusių pardavimo galimybių atnaujinimas „Azure” Pardavimo galimybės](../dev-tools/pipeline-msbuild-update.md). |

### <a name="user-avatar"></a>Vartotojo pseudoportretas 

|   |  |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Vartotojo pseudoportretas, rodomas dešinėje naršymo juostos pusėje, buvo nuskaitytas naudojant API iš „Dynamics 365” antraštės valdiklio, kuris yra nerekomenduojamas. |
| **Pakeitė kita funkcija?**   | Vietoj to vartotojai matys savo inicialus naršymo juostos apskritime. Tai tas pats vaizdinis elementas, šiuo metu naudojamas programavimo mašinose. |
| **Paveiktos produkto sritys**         | Žiniatinklio klientas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Pašalinta iš 10.0.17 versijos |

### <a name="enterprise-portal-ep-deprecation"></a>Įmonės portalo (EP) netinkamumas  

|   |  |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Metaduomenų artefaktai, susieti su 2012 m. „Dynamics AX” įmonės portalu (EP), yra nerekomenduojami, nes EP niekada nebuvo palaikomas „Finance and Operations” programose. |
| **Pakeitė kita funkcija?**   | Ne |
| **Paveiktos produkto sritys**         | Žiniatinklio klientas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nebenaudojama. Numatyta, kad visas EP kodas bus pašalintas 2021 m. spalio mėn leidime. |

## <a name="platform-updates-for-version-10015-of-finance-and-operations-apps"></a>„Finance and Operations” programų 10.0.15 versijos platformos naujinimai

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>„Internet Explorer 11“ palaikymas „Dynamics 365“ yra nutrauktas

|   |  |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Nuo 2020 m. gruodžio „Microsoft Internet Explorer 11“ palaikymas visuose „Dynamics 365“ produktuose yra nutraukiamas, o „Internet Explorer 11“ nebus palaikomas nuo 2021m. rugpjūčio.<br><br>Tai paveiks klientus, kurie naudoja „Dynamics 365“ produktus, skirtus naudoti „Internet Explorer 11“ sąsają. Nuo 2021m. rugpjūčio „Internet Explorer 11“ nebus palaikomas tokiuose „Dynamics 365“ produktuose. |
| **Pakeitė kita funkcija?**   | Rekomenduojame klientams naudoti „Microsoft Edge“.|
| **Paveiktos produkto sritys**         | Visi „Dynamics 365“ produktai |
| **Visuotinio diegimo parinktis**              | Visos|
| **Būsena**                         | Nebenaudojama. „Internet Explorer 11“ nebus palaikoma nuo 2021 m. rugpjūčio.|


### <a name="visual-studio-add-in-to-apply-metadata-hotfixes"></a>„Visual Studio“ papildinys, skirtas metaduomenų karštųjų pataisų pritaikymui

|   |  |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Metaduomenų karštosios pataisos nepalaikomos pristačius [vienos versijos](../../fin-ops/get-started/one-version.md) paslaugų naujinimus, kurie buvo pateikti 2018 m. liepą kartu su 8.1 versija. |
| **Pakeitė kita funkcija?**   | Nėra atskirų metaduomenų karštųjų pataisų, kurios būtų skirtos palaikomoms versijoms. Vietoje jų taikomi kaupiamieji kokybiniai naujinimai. |
| **Paveiktos produkto sritys**         | „Visual Studio“ papildiniai |
| **Visuotinio diegimo parinktis**              | Kūrimo virtualieji įrenginiai |
| **Būsena**                         | 10.0.15 versijoje papildinys nebėra įtrauktas į „Visual Studio“ įrankius. |


## <a name="platform-updates-for-version-10014-of-finance-and-operations-apps"></a>„Finance and Operations” programų 10.0.14 versijos platformos naujinimai

### <a name="online-users-page"></a>Prisijungusių vartotojų puslapis 

|   |  |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Tai yra ankstesnio kliento/serverio architektūroje sukurtas senstelėjęs puslapis. Šiame puslapyje pateikta informacija ne visada tiksli ir dėl to gali būti paini ir klaidinanti. |
| **Pakeitė kita funkcija?**   | Sekančiame atnaujinime pateiksime naują puslapį.|
| **Paveiktos produkto sritys**         | Sistemos administravimas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Iki 2021 m. spalio ši forma bus pašalinta.   |


## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>„Finance and Operations” programų 10.0.13 versijos platformos naujinimai


### <a name="custom-code-defined-in-ssrs-report-properties"></a>Tinkintas kodas nustatytas SSRS ataskaitos ypatybėse 

|   |  |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Bendrai, tinkintas kodas siūlo apribotas naudas ir tuo pat metu reikalauja reikšmingų šaltinių papildymų ir paramos skyrimo. Tinkintas kodas daugiausiai naudojamas ataskaitų autorių siekiant iškviesti viešus metodus iš tinkinto kodo surinkimo. Nepaisant to, debesyje patalpintos paslaugos nepalaiko sąsajų su tinkintais susirinkimais SSRS ataskaitoms. |
| **Pakeitė kita funkcija?**   | Ataskaitų autoriai gali pasirinkti, ar tęsti susiejimą su viešomis .NET API matematikos, pavertimo ir formato veiksmams iš bet kurios teksto laukelio išraiškos. Dėl išsamesnės informacijos, žr. [Įtraukti kodą į ataskaitą (SSRS)](https://docs.microsoft.comsql/reporting-services/report-design/add-code-to-a-report-ssrs?view=sql-server-ver15).  |
| **Paveiktos produkto sritys**         | Programos ataskaitos projektavimo papildomas rinkinys turi tinkintą kodą. |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Su versija 10.0.13, užpildymo įrankis pradės išduoti perspėjimus instancijoms, kuriose tinkintas kodas yra aptiktas SSRS ataskaitos sąvokoje. Tam, kad išspręstumėte šią problemą, atverkite ataskaitos projektavimo sąvoka ir pašalinkite visus tinkintus kodo artefaktus. Šis pranešimas bus pakeistas užpildymo klaida ateities atnaujinimuose.   |

### <a name="upgrade-of-three-jquery-component-libraries"></a>Trijų „jQuery” komponentų bibliotekų atnaujinimas 

|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Trijų „jQuery” komponentų bibliotekos atnaujintos dėl saugumo spragų, kad būtų tvarkoma valiuta.   
| **Pakeitė kita funkcija?**   | Šiose bibliotekose matysis pakeitimai: „jQuery” (3.5.0 versiją iš 2.1.4 versijos), „jQuery UI” (1.12.1 versiją iš 1.11.4 versijos), „jQuery qTip” (3.0.3 versiją iš 2.2.1 versijos). „jQuery” internetu pateikė perkėlimo nurodymus.  |
| **Paveiktos produkto sritys**         | Išplėstiniai valdikliai, ypač pasirinktinis „JavaScript” kodas, naudojantis pasenusias arba pašalintas API |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | 10.0.13 versijoje/platformos atnaujinime Nr. 37 klientai gali pasirinktinai perkelti į naujausias bibliotekas įjungdami „Atnaujinti tris „jQuery” komponentų bibliotekas” funkciją. Perkėlimas į naujausias bibliotekas bus privalomas nuo 2021 m. balandžio mėnesio leidimo, kad būtų skirta laiko paveiktoms API perkelti.   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>Esamas tinklelio valdymas/forceLegacyGrid() API

|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Esamas tinklelio valdymas yra pakeičiamas nauju tinklelio valdymu. |
| **Pakeitė kita funkcija?**   | [Naujas tinklelio valdymas](../..//fin-ops/get-started/grid-capabilities.md) |
| **Paveiktos produkto sritys**         | Žiniatinklio klientas |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | 10.0.13 versijoje naujas tinklelio valdymas yra bendrai prieinamas ir klientai gali pasirinktinai įjungti šią funkciją. Naujas tinklelio valdymas taps privalomas 2021 m. spalio mėn. leidime. Kai naujas tinklelio valdymas tamp privalomas, **forceLegacyGrid()** API nebebus apdovanota. |

### <a name="personalization-without-saved-views"></a>Personalizavimas be įrašytų peržiūrų 

|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Personalizavimo papildoma sistema buvo perdaryta su naujomis įrašytomis peržiūros funkcijomis taip, kad ji galėtų geriau veikti ir siūlytų papildomas galimybes. |
| **Pakeitė kita funkcija?**   | Įrašyti rodiniai |
| **Paveiktos produkto sritys**         | Žiniatinklio klientas |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | 10.0.13 versijoje/platformos atnaujinimas 37, įrašyta peržiūros funkcija yra dažniausiai prieinama, o klientai gali pasirinktinai ją įjungti. Išsaugotų peržiūrų funkcija taps privaloma 2021 m. spalio mėn. leidime. |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>„Finance and Operations” programų 10.0.12 versijos platformos naujinimai

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Tinklelio arba grupės valdiklio formų plėtiniai, kuriuose yra netinkamų laukų nuorodų

|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Tinklelio arba grupės valdiklių duomenų grupės ypatybė naudojama automatiškai rodyti visus laukų grupės laukus. Tinklelyje arba grupės valdiklyje, pridėtame prie plėtinio, gali būti laukų, kurie nebėra apibrėžti laukų grupėje, arba jame gali būti trūkstamų laukų, kurie apibrėžti laukų grupėje. Tai gali sukelti nenuoseklų veikimą apdorojimo laiko metu. Platformos naujiniai, skirti „Finance and Operations” programų 10.0.12 versijai, dabar klasifikuoja šią problemą kaip kompiliatoriaus *įspėjimą*. Norėdami išspręsti šią problemą, atidarykite formos plėtinį ir jį įrašykite.
| **Pakeitė kita funkcija?**   | Atliekant būsimą naujinimą, šis kompiliatoriaus įspėjimas bus pakeistas kompiliavimo klaidos pranešimu. |
| **Paveiktos produkto sritys**         | „Visual Studio“ kūrimo įrankiai |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Kompiliatoriaus įspėjimas pristatytas platformos naujiniuose, skirtuose „Finance and Operations” programų versijai 10.0.12. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>„Finance and Operations” programų 10.0.11 versijos platformos naujinimai

### <a name="explicit-safe-lists-for-self-service-environments"></a>Išsamūs baltieji sąrašai savitarnos aplinkoms

|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | IP perkėlimo procesas į baltuosius sąrašus pasikeitė. Savitarna nebepalaiko IP baltųjų sąrašų. |
| **Pakeitė kita funkcija?**   | Daugiau informacijos rasite [„Azure Active Directory” sąlyginės prieigos konfigūracija](https://docs.microsoft.com/appcenter/general/configuring-aad-conditional-access).|
| **Paveiktos produkto sritys**         | Sauga |
| **Visuotinio diegimo parinktis**              | Debesis |
| **Būsena**                         | **Nuvertėjęs:** Ši funkcija yra visiškai pasenusi savitarnos diegimui. |

### <a name="visual-studio-2015"></a>„Visual Studio 2015“

|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Norint, kad būtų palaikomos naujausios „Visual Studio” versijos, reikia atlikti tam tikrus X + + plėtinių, skirtų „Visual Studio”, keitimus. Šie pakeitimai nesuderinami su „Visual Studio” 2015. |
| **Pakeitė kita funkcija?**   | „Visual Studio 2017” bus pakeista „Visual Studio 2015” kaip įdiegta ir reikalinga versija. |
| **Paveiktos produkto sritys**         | „Visual Studio“ kūrimo įrankiai |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Virtualiosiose mašinose, kurios naudojamos 10.0.13 (platformos atnaujinimas Nr. 37) arba naujesnėje versijoje, yra „Visual Studio 2017“. Versija 10.0.16 (platformos atnaujinimas Nr. 40) yra galutinis leidimas, palaikantis „Visual Studio 2015“. Virtualiųjų mašinų, kuriose veikia tik „Visual Studio 2015“, negalės atnaujinti į versiją 10.0.17 (platformos atnaujinimas Nr. 41). |

### <a name="field-groups-containing-invalid-field-references"></a>Laukų grupės, kuriose pateiktos netinkamos laukų nuorodos

|   |  |
|------------|--------------------|
| **Nebenaudojimo/pašalinimo priežastis** | Lentelės metaduomenų aprašuose gali būti laukų grupių, kuriose yra netinkamų laukų nuorodų. Įdiegus šias laukų grupes gali kiti vykdymo gedimų programose „Financial Reporting“ ir „Microsoft SQL Server Reporting Services“ (SSRS). 23 platformos naujinimas pristatė kompiliatoriaus *įspėjimą*, kuris įgalina šios metaduomenų problemos sprendimą. „Finance and Operations” programų 10.0.11 versijos platformos naujinimai klasifikuoja šią problemą kaip kompiliatoriaus *klaidą*.<p>Norėdami ištaisyti šią klaidą, atlikite toliau nurodytus veiksmus.</p><ol><li>Pašalinkite netinkamą lauko nuorodą iš lentelės lauko grupės aprašo.</li><li>Perkompiliuokite.</li><li>Įsitikinkite, kad pašalintos visos klaidos.</li></ol> |
| **Pakeitė kita funkcija?**   | Ši kompiliatoriaus klaida visam laikui pakeičia kompiliatoriaus įspėjimą.  |
| **Paveiktos produkto sritys**         | „Visual Studio“ kūrimo įrankiai |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | **Nebenaudojama:** „Finance and Operations” programų 10.0.11 versijos platformos naujinimuose kompiliatoriaus įspėjimas yra kompiliatoriaus klaida. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>ISV licencijos, sukurtos naudojant SHA1 maišos algoritmą

|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Pasikeitė nepriklausomo programinės įrangos tiekėjo (ISV) licencijų kūrimo procesas. Daugiau informacijos žr. [Nepriklausomo programinės įrangos tiekėjo (ISV) licencijavimas](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes). |
| **Pakeitė kita funkcija?**   | Taip. Norėdami sukurti licencijas, naudokite „Windows PowerShell”. |
| **Paveiktos produkto sritys**         | „Visual Studio“ kūrimo įrankiai |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | <strong>Nebenaudojama:</strong> ISV licencijos, sukurtos naudojant SHA1 maišos algoritmą. Šis algoritmas priklausė nuo sertifikatų, sukurtų naudojant priemonę „MakeCert”, ir ši priemonė nebenaudojama.<p><strong>Nebenaudojama:</strong> SHA1 naudojimas saugos arba maišos tikslais. SHA1 nustos veikti 2021 m. pradžioje. Todėl jos nebereikėtų naudoti.<p><strong>Pašalinta:</strong> transportavimo lygmens saugos (TLS) 1.0 ir 1.1 versijų gaunamų ir siunčiamų užklausų palaikymas. |

## <a name="platform-update-32"></a>Platformos „update 32“

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Darbo eigos užklausos keitimo dialogo lange nebėra vartotojų pasirinkimo išplečiamojo sąrašo
|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Dėl sąrašo galėjo kilti saugos problemų, nes keitimo užklausa galėjo būti nusiųsta nenumatytam vartotojui. Taip pat kilo tinkamumo naudoti problema, nes vartotojas buvo verčiamas nustatyti darbo eigos iniciatorių ir pasirinkti jį rankiniu būdu.  |
| **Pakeitė kita funkcija?**   | Ne |
| **Paveiktos produkto sritys**         | Darbo eiga |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Vartotojų pasirinkimo išplečiamasis sąrašas buvo pašalintas iš „Platform update 32“ keitimo užklausos dialogo lango. Užklausos keitimo užklausos bus automatiškai siunčiamos iniciatoriui, kaip numatyta. Norėdami gauti daugiau informacijos apie šią funkciją, žr. skyrių [Darbo eigos patvirtinimo procesų veiksmai](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Sunumeruoti dokumentai, kuriuos generuoja debesies paslauga, nebepalaiko įterptųjų detalizuotų nuorodų 
|   |  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Naršymo URL, įterpti į paslaugos generuojamus dokumentus, gali būti slaptų verslo duomenų. Norėdami apsaugoti kliento duomenis, saugumo sumetimais pašalinsime įterptųjų detalizuotų nuorodų, esančių dokumentuose, palaikymą. Dėl šio pakeitimo vartotojai galės kurti dokumentus našiai ir interaktyviai.  |
| **Pakeitė kita funkcija?**   | nr. |
| **Paveiktos produkto sritys**         | Ataskaitos |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Ši funkcija yra šalinama iš paslaugos.<br><br>Šiuolaikinis klientas siūlo daugybę galimybių, kaip kurti vaizdus, kuriuose yra automatiškai sugeneruotų nuorodų, padedančių naršyti programoje. Rekomenduojama paslaugoje esančius sunumeruotus dokumentus naudoti išoriniams ryšiams, kurie gavėjams siunčiami el. paštu, archyvuojami ir spausdinami. Patobulinome dokumentų peržiūrą tiesiogiai naršyklėje, per kurią suteikiama tiesioginė prieiga prie vietinių spausdintuvų. Daugiau informacijos ieškokite [„PDF dokumentų peržiūra naudojant įdėtąją peržiūros programą“](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Ankstesni pranešimai apie pašalintas arba nebenaudojamas funkcijas
Norėdami sužinoti daugiau apie funkcijas, kurios buvo pašalintos arba nebenaudojamos ankstesniuose leidimuose, žr. skyrių [Ankstesniuose leidimuose pašalintos arba nebenaudojamos funkcijos](../migration-upgrade/deprecated-features.md).

