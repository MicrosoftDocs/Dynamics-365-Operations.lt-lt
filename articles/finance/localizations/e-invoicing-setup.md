---
title: Elektroninių SF nustatymas
description: Šioje temoje paaiškinama, kaip nustatyti elektroninių SF išrašymo priedą „Microsoft Dynamics 365 Finance” ir „Dynamics 365 Supply Chain Management”.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 9aac18155fbc7a87554ac0521cd9f40d11eba9e2
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890836"
---
# <a name="set-up-electronic-invoicing"></a>Elektroninių SF nustatymas

[!include [banner](../includes/banner.md)]


Elektroninių SF išrašymo priedo funkcijos nustatymas yra procesas, kurio metu reikia sukurti reikiamą konfigūraciją naudojant „Regulatory Configuration Services” (RCS) aplinką ir publikuoti šią konfigūraciją elektroninių SF išrašymo priedo serveryje. Nustatymas leidžia kurti konfigūruojamas taisykles, įjungiančias elektroninių SF išrašymo priedą, kad būtų galima naudoti saugų protokolą internete siekiant palaikyti ryšį ir keistis duomenimis su trečiosios šalies objektu žiniatinklio tarnybose.

Konfigūravimas paremtas elektroninių ataskaitų (ER) formato konfigūracija kaip priemone kurti turinį, siunčiamą ir gaunamą naudojant skaitmeninius failus. Jis taip pat paremtas ryšio veiksmų valdymu, kad galėtų siųsti užklausas ir gauti atsakymus iš trečiosios šalies žiniatinklio tarnybų bei nereikalautų rašyti kodo.

## <a name="overview"></a>Peržiūra

„El. SF išrašymo funkcija” yra bendras išteklių, sukonfigūruotų ir publikuotų siekiant naudoti elektroninių SF išrašymo priedo serverį, pavadinimas. Funkcijos nustatymas be viso kito apima ER konfigūracijos formatų naudojimą konfigūruojamiems eksportavimo ir importavimo failams kurti ir veiksmų bei veiksmų srautų naudojimą konfigūruojamų taisyklių kūrimui įgalinti, kad būtų galima siųsti užklausas, importuoti atsakymus ir analizuoti atsakymo turinį.

Toliau pateiktame paveikslėlyje vaizduojama pagrindiniai elektroninių SF išrašymo priedo funkcijos komponentai.

![Elektroninių SF išrašymo priedo funkcijos apžvalga](media/e-Invoicing-services-feature-setup-Overview-e-Invoicing-feature.png)

Funkcijos nustatymas gali skirtis priklausomai nuo šalies ar regiono arba verslo reikalavimų, nes SF formatai ir veiksmų srautai skiriasi.

## <a name="set-up-the-electronic-invoicing-feature"></a>Elektroninių SF funkcijų nustatymas

Nustatymo procesas turi būti atliktas jūsų RCS aplinkoje. Atlikite toliau pateiktus veiksmus, norėdami sukurti naują elektroninių SF išrašymo priedo funkciją.

1. Prisijunkite prie jūsų RCS aplinkos.
2. RCS pasirinkus dalį **Visuotinės funkcijos**, esančią darbo srityje **Funkcijos**, pasirinkite plytelę **Elektroninių SF priedas**.
3. Puslapyje **Elektroninių SF išrašymo priedo funkcijos** pasirinkite **Importuoti**, norėdami importuoti ER duomenų modelio konfigūraciją iš visuotinės saugyklos.
4. Pasirinkite **Įtraukti**, norėdami sukurti elektroninių SF išrašymo priedo funkciją. Šią funkciją galite kurti nuo pradžių arba išvesti ją iš esamos elektroninių SF išrašymo priedo funkcijos.

    ![Elektroninių SF išrašymo priedo funkcijos įtraukimas](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature.png)

> [!NOTE]
> Kuriant naują elektroninių SF išrašymo priedo funkciją, ji turi versijos numerį, o numatytoji būsena nustatyta į **Juodraštis**.

### <a name="configurations"></a>Konfigūracijos

Konfigūracijos saugo ER formato konfigūracijas, kurių reikia transformacijoms ir failų, kurie bus iškeisti palaikant ryšį su trečiosios šalies žiniatinklio tarnybomis, kūrimui. Elektroninių SF išrašymo priedo funkcija gali turėti tiek ER failo formato konfigūracijų, kiek reikia, remiantis integravimo techninėmis specifikacijomis, kurias pateikia žiniatinklio tarnybos teikėjas.

Atlikite toliau pateiktus veiksmus, norėdami įtraukti ER formatų į elektroninių SF išrašymo priedo funkciją.

1. Puslapio **Elektroninių SF išrašymo priedo funkcijos** skirtuke **Konfigūracijos** pasirinkite **Įtraukti**, kad įtrauktumėte ER failo formato konfigūracijas, skirtas elektroninių SF išrašymo priedo funkcijai.

    ![Elektroninių SF išrašymo priedo funkcijos konfigūracijų įtraukimas](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Kurdami elektroninių SF išrašymo priedo funkciją nuo pradžių, turite neautomatiniu būdu įtraukti visas ER failo formato konfigūracijas. Kai išvedate elektroninių SF išrašymo priedo funkciją iš esamos funkcijos, ER failo formato konfigūracijos sukuriamos automatiškai, nes jos perduodamos iš pradinės elektroninių SF išrašymo priedo funkcijos.

2. Pasirinkite **Redaguoti**, kad būtų atidarytas puslapis **Formato dizaino įrankis**, kuriame galite redaguoti ER failo formato konfigūraciją.

    ![Elektroninių SF išrašymo priedo funkcijos konfigūracijų redagavimas](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > Redaguojant formatą, konfigūracijos versijos būsena nustatoma į **Juodraštis**.

3. Norėdami pakeisti failo formato konfigūraciją, naudokite puslapį **Formato dizaino įrankis**. Daugiau informacijos žr. [Elektroninių dokumentų konfigūracijų kūrimas](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md).

    ![Formato dizaino įrankio puslapis](media/e-Invoicing-services-feature-setup-ER-Format-designer.png)

### <a name="feature-setups"></a>Funkcijos nustatymai

Funkcijos nustatymai apima trečiosios šalies žiniatinklio tarnybos ryšių ir saugos taisykles. Elektroninių SF išrašymo priedo funkcija gali turėti tiek funkcijos nustatymų, kiek reikia, remiantis verslo taisykle, kurią norite įvykdyti.

Atlikite toliau pateiktus veiksmus, norėdami įtraukti funkcijos nustatymų į elektroninių SF išrašymo priedo funkciją.

1. Puslapio **Elektroninių SF išrašymo priedo funkcijos** skirtuke **Nustatymai** pasirinkite **Įtraukti**, kad įtrauktumėte funkcijos nustatymų į elektroninių SF išrašymo priedo funkciją.

    ![Elektroninių SF išrašymo priedo funkcijos nustatymų įtraukimas](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Setups.png)

    > [!NOTE]
    > Kurdami elektroninių SF išrašymo priedo funkciją nuo pradžių, turite neautomatiniu būdu įtraukti visus reikiamus funkcijos nustatymus. Kai išvedate elektroninių SF išrašymo priedo funkciją iš esamos funkcijos, visi funkcijos nustatymai sukuriami automatiškai, nes jie perduodami iš pradinės elektroninių SF išrašymo priedo funkcijos.

2. Pasirinkite **Redaguoti**, norėdami redaguoti funkcijos versijos nustatymą.

    ![Elektroninių SF išrašymo priedo funkcijos nustatymų redagavimas](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Setups.png)

3. Norėdami konfigūruoti veiksmus, taikymo taisykles ir kintamuosius, naudokite puslapį **Funkcijos versijos nustatymas**.

    ![Veiksmai, taikymo taisyklės ir kintamieji](media/e-Invoicing-services-feature-setup-View-Actions-Applicability-Rules-Variables.png)

### <a name="actions"></a>Veiksmai

Veiksmai yra iš anksto apibrėžtas operacijų, kurios vykdomos eilės tvarka, sąrašas. Šis sąrašas nurodo veiksmų, kurių reikia, kad būtų galima pilnai įvykdyti elektroninių SF išrašymo priedo funkciją, paskirstymą. Veiksmai toje pačioje elektroninių SF išrašymo priedo funkcijoje gali apimti abiejų krypčių ryšį: užklausos siuntimo į paskirties vietą ir atsakymo gavimo bei jo turinio analizavimo.

Kiekviename veiksme yra iš anksto nustatytas parametrų, būtinų veiksmui įvykdyti, sąrašas. Papildomi parametrai gali būti pateikti pasirinktinai.

#### <a name="actions-fasttab"></a>„FastTab“ Veiksmai

Puslapio **Funkcijos versijų nustatymas** skirtuko **Veiksmai** „FastTab“ **Veiksmai**, atlikite vieną ar abu toliau pateiktus veiksmus, skirtus veiksmams valdyti.

- Pasirinkite **Naujas** ar **Naikinti** , norėdami įtraukti naujų veiksmų arba panaikinti esamus.
- Pasirinkite **Aukštyn** arba **Žemyn**, norėdami perkelti pažymėtus veiksmus tinklelyje aukštyn arba žemyn ir pakeisti tvarką, kuria jie vykdomi. Veiksmai vykdomi tokia tvarka, kokia jie rodomi tinklelyje – iš viršaus į apačią.

![Veiksmų valdymas](media/e-Invoicing-services-feature-setup-Manage-Actions.png)

Toliau pateikta lentelė aprašo laukus, pasiekiamus „FastTab” **Veiksmai**.

| Laukas        | Aprašas |
|--------------|-------------|
| Veiksmas       | Yra aštuoni iš anksto nustatyti veiksmai.<ul><li><strong>Pasirašyti dokumentą</strong></li><li><strong>FileStoreActionName</strong></li><li><strong>Pakeisti dokumentą</strong></li><li><strong>Apdoroti atsakymą</strong></li><li><strong>Iškviesti REST žiniatinklio tarnybą</strong></li><li><strong>Iškviesti Meksikos PAC tarnybą</strong></li><li><strong>Iškviesti Brazilijos SEFAZ tarnybą</strong></li><li><strong>Iškviesti Italijos SDI tarnybą</strong></li></ul> |
| Veiksmo pavadinimas  | Veiksmo pavadinimas ir jo vykdymo tvarka. |
| Aprašas  | Veiksmo aprašas. |
| Įjungti kartojimą | Pasirinktas žymės langelis nurodo, kad veiksmą galima kartoti, jei ankstesnis bandymas nesėkmingas. |
| Pakartoti veiksmą | Kartojimo įvykio metu tai kartojamas veiksmas. Kartojimas baigiamas dabartiniame veiksme (kartojimas įskaitomas). Parametrai **Minimalus atsilikimas** ir **Maksimalus atsilikimas** nurodo mažiausią ir didžiausią veiksmų, kurie turi šiuos parametrus, kartojimų skaičių. |

#### <a name="parameters-fasttab"></a>„FastTab” Parametrai

„FastTab” **Parametrai** pateikia veiksmo, pasirinkto „FastTab” **Veiksmai**, parametrus.

![„FastTab” Parametrai](media/e-Invoicing-services-feature-setup-View-Actions-Parameters.png)

Toliau pateikta lentelė aprašo laukus, pasiekiamus „FastTab” **Parametrai**.

| Laukas       | Aprašas |
|-------------|-------------|
| Pavadinimas / vardas ir (arba) pavardė        | Iš anksto nustatytas parametrų sąrašas. Daugiau informacijos žr. skyriuje [Parametrų sąrašas pagal veiksmą](#list-of-parameters-by-action). |
| Aprašas | Parametro aprašas. |
| Reikšmė       | Parametro reikšmė. |

#### <a name="list-of-parameters-by-action"></a>Parametrų sąrašas pagal veiksmą

Pasiekiami parametrai skiriasi, atsižvelgiant į veiksmą, pasirinktą „FastTab” **Veiksmai**.

###### <a name="action-sign-document"></a>Veiksmas: Pasirašyti dokumentą

| Parametras                             | Aprašas |
|---------------------------------------|-------------|
| Įvesties failas                            | Įvesties XML dokumento failas, kurį reikia pasirašyti naudojant elektroninį parašą. |
| Sertifikato pavadinimas                      | Sertifikato pavadinimas saugykloje. |
| Parašo tipas                        | Naudojamas parašo tipas. |
| Parašo būdo pavadinimas                 | Parašo būdo, naudojamo elektroniniam parašui generuoti, pavadinimas. |
| Suvestinės būdo pavadinimas                    | Suvestinės būdas, naudojamas generuojant suvestinės eilutę skaitmeniniame paraše. |
| Kanonizacijos būdo pavadinimas          | Kanonizacijos būdas, naudojamas parašo maišai skaičiuoti. |
| Nuorodos atributo pavadinimas              | Atributo pavadinimas, nurodantis, kur parašo elemente turi būti įterptas nuorodos ID. |
| Pasirašomojo elemento pavadinimas               | Dokumento XML elemento, kurį reikia pasirašyti naudojant elektroninį parašą, pavadinimas. Jei nenurodytas joks elementas, pasirašoma dokumento šaknis. |
| Elemento, skirto parašui įterpti, pavadinimas   | XML elemento, į kurį turi būti įterptas sugeneruotas skaitmeninis parašas, pavadinimas. Jei nenurodytas joks elementas, parašas įterpiamas į dokumento šaknį. |
| XLST failas su suvestinės transformacija       | Išplėstinės stiliaus aprašų kalbos transformacijų (XSLT) failas, kuriame yra suvestinės transformacijos taisyklės, skirtos elektroninio parašo suvestinės eilutei generuoti. |
| Kelias, skirtas suvestinės eilutei įterpti          | Kelias formatu **\<elementName\>.\<Attribute.Path\>** vietos, kur turi būti įterpta sugeneruota suvestinės eilutė. |
| Sertifikato numerio vieta           | Elemento ir atributo, kuriuose turi būti pateiktas sertifikato numeris, pavadinimai. |
| Sertifikato duomenų vieta          | Elemento ir atributo, kuriuose turi būti įterpti sertifikato duomenys (base64), pavadinimai. |
| Sertifikato numeris užkoduotas ASCII formatu | Reikšmė, nurodanti, ar sertifikato numeris užkoduotas ASCII formatu. |

###### <a name="action-filestoreactionname"></a>Veiksmas: FileStoreActionName

| Parametras  | Aprašas |
|------------|-------------|
| Įvesties failas | Įvesties failas, kurį norite saugoti. |

###### <a name="action-transform-document"></a>Veiksmas: Pakeisti dokumentą

| Parametras                       | Aprašas |
|---------------------------------|-------------|
| Įvesties failas                      | Šaltinio failas, pateikiantis veiksmo duomenis, kuriuos reikia vykdyti. |
| Kryptis                       | Reikšmė, nurodanti, ar turi būti naudojamas importavimo, ar eksportavimo formatas. |
| Konfigūracijos ID                | Formatas, kurį reikia vykdyti. |
| Konfigūracijos versija           | Jei nenurodyta jokia konfigūracijos versija, bus naudojama naujausia versija. |
| Konfigūracijos integravimo taškas | Šaltinio failas, pateikiantis ataskaitų vykdymo laiko duomenis. |

###### <a name="action-process-response"></a>Veiksmas: Apdoroti atsakymą

| Parametras                    | Aprašas |
|------------------------------|-------------|
| Įvesties failas                   | Atsakymas, kurį reikia analizuoti. |
| Ataskaitų konfigūracijų sąrašas | Konfigūracijų, naudojamų atsakymams analizuoti, sąrašas. |

###### <a name="action-call-rest-web-service"></a>Veiksmas: Iškviesti REST žiniatinklio tarnybą

| Parametras                   | Aprašas |
|-----------------------------|-------------|
| Tinklo tarnybos URL             | URL, į kurį siunčiamos užklausos. |
| Žiniatinklio užklausos skirtasis laikas         | Maksimalus laikas (milisekundėmis), per kurį laukiama žiniatinklio tarnybos atsakymo. |
| Užklausos operacijos tipas      | HTTP užklausos operacijos tipas (pvz., **GAUTI**, **REGISTRUOTI** arba **NAIKINTI**). |
| Sertifikatų pavadinimai           | Sertifikatų pavadinimai. |
| Atsakymo teksto kodavimas      | Numatomas HTTP atsakymo teksto kodavimas, kad būtų galima tinkamai iššifruoti. |
| HTTP užklausos turinio tipas   | HTTP užklausos turinio tipo antraštės įvestis. |
| HTTP užklausos turinio tekstas   | HTTP užklausos tekstas. (Teksto gali nebūti.) |
| HTTP parametrų užklausos reikšmės | Parametrų užklausos reikšmės, naudojamos norint užpildyti URL kintamųjų parametrais. |
| Užklausos maršrutas               | HTTP užklausos maršruto kelias. Kintamųjų parametrus galima įrašyti į notaciją **\{paramName\}**. Pavyzdys: **„api/{id}/submit”**. |
| Maršruto parametrų sąrašas        | Maršruto parametrai rakto vertės notacijoje, naudojami kintamiesiems įtraukti į maršrutą. |
| Pasirinktinės HTTP antraštės         | Pasirinktinės HTTP antraštės, kurias reikia įtraukti į užklausą. |
| HTTP užklausos slapukai        | Slapukų rakto vertės notacijoje, kuriuos reikia įvesti į HTTP slapukų antraštės užklausą, sąrašas. |
| Saugos protokolas           | Saugos protokolas, kuris bus naudojamas palaikyti ryšį tarp HTTP užklausų ir serverio. (Pagal numatytuosius nustatymus naudojama transportavimo lygmens saugos \[TLS\] 1.2 versija.) |

###### <a name="action-call-mexican-pac-service"></a>Veiksmas: Iškviesti Meksikos PAC tarnybą

| Parametras                | Aprašas |
|--------------------------|-------------|
| Įvesties failas               | Failas, kuriame yra XML duomenys, kurie bus siunčiami į tinklo tarnybą kaip metodo įvesties parametras. |
| URL adresas              | Žiniatinklio tarnybos adresas (galinis punktas). |
| Žiniatinklio būdo (veiksmo) pavadinimas | Žiniatinklio būdo (veiksmo), kuris turi būti vykdomas, pavadinimas. |
| Sertifikatai             | Sertifikato grandinė, kurios reikia kliento autentifikavimui, kurį atlieka žiniatinklio tarnyba. Kliento sertifikatas turėtų būti paskutinis grandinėje esantis sertifikatas. Šakninis ir tarpinis sertifikatai turėtų būti pirmieji. |
| Žiniatinklio užklausos skirtasis laikas      | Maksimalus laikas (milisekundėmis), per kurį laukiama žiniatinklio tarnybos atsakymo. |
| Kartojimo intervalas           | Intervalas tarp bandymų iškviesti ir atsakymo gavimo iš žiniatinklio tarnybos. Jei nenurodytas joks intervalas, po pirmo nesėkmingo iškvietimo nebus atlikti papildomi bandymai. |
| Mėginimų skaičius              | Didžiausias pakartotinių bandymų iškviesti ir gauti atsakymą iš žiniatinklio tarnybos skaičius. |
| Kartoti iki               | Maksimalus laikas (milisekundėmis), per kurį pakartotiniai iškvietimai gali būti tęsiami. |
| Minimalus atsilikimas         | Mažiausias atsilikimo dažnis, skirtas eksponentiniam pakartotinių bandymų intervalų skaičiavimui. |
| Maksimalus atsilikimas         | Didžiausias atsilikimo dažnis, skirtas eksponentiniam pakartotinių bandymų intervalų skaičiavimui. |
| Saugos protokolas        | Saugos protokolas, kuris bus naudojamas palaikyti ryšį tarp HTTP užklausų ir serverio. (Pagal numatytuosius nustatymus naudojama TLS 1.2 versija.) |

###### <a name="action-call-brazilian-sefaz-service"></a>Veiksmas: Iškviesti Brazilijos SEFAZ tarnybą

| Parametras                | Aprašas |
|--------------------------|-------------|
| Įvesties failas               | Failas, kuriame yra XML duomenys, kurie bus siunčiami į tinklo tarnybą kaip metodo įvesties parametras. |
| URL adresas              | Žiniatinklio tarnybos adresas (galinis punktas). |
| Žiniatinklio būdo (veiksmo) pavadinimas | Žiniatinklio būdo (veiksmo), kuris turi būti vykdomas, pavadinimas. |
| Sertifikatai             | Sertifikato grandinė, kurios reikia kliento autentifikavimui, kurį atlieka žiniatinklio tarnyba. Kliento sertifikatas turėtų būti paskutinis grandinėje esantis sertifikatas. Šakninis ir tarpinis sertifikatai turėtų būti pirmieji. |
| Žiniatinklio užklausos skirtasis laikas      | Maksimalus laikas (milisekundėmis), per kurį laukiama žiniatinklio tarnybos atsakymo. |
| Kartojimo intervalas           | Intervalas tarp bandymų iškviesti ir atsakymo gavimo iš žiniatinklio tarnybos. Jei nenurodytas joks intervalas, po pirmo nesėkmingo iškvietimo nebus atlikti papildomi bandymai. |
| Mėginimų skaičius              | Didžiausias pakartotinių bandymų iškviesti ir gauti atsakymą iš žiniatinklio tarnybos skaičius. |
| Kartoti iki               | Maksimalus laikas (milisekundėmis), per kurį pakartotiniai iškvietimai gali būti tęsiami. |
| Minimalus atsilikimas         | Mažiausias atsilikimo dažnis, skirtas eksponentiniam pakartotinių bandymų intervalų skaičiavimui. |
| Maksimalus atsilikimas         | Didžiausias atsilikimo dažnis, skirtas eksponentiniam pakartotinių bandymų intervalų skaičiavimui. |
| Saugos protokolas        | Saugos protokolas, kuris bus naudojamas palaikyti ryšį tarp HTTP užklausų ir serverio. (Pagal numatytuosius nustatymus naudojama TLS 1.2 versija.) |

###### <a name="action-call-italian-sdi-service"></a>Veiksmas: Iškviesti Italijos SDI tarnybą

| Parametras                | Aprašas |
|--------------------------|-------------|
| Įvesties failas               | Failas, kuriame yra XML duomenys, kurie bus siunčiami į tinklo tarnybą kaip metodo įvesties parametras. |
| URL adresas              | Žiniatinklio tarnybos adresas (galinis punktas). |
| Žiniatinklio būdo (veiksmo) pavadinimas | Žiniatinklio būdo (veiksmo), kuris turi būti vykdomas, pavadinimas. |
| Sertifikatai             | Sertifikato grandinė, kurios reikia kliento autentifikavimui, kurį atlieka žiniatinklio tarnyba. Kliento sertifikatas turėtų būti paskutinis grandinėje esantis sertifikatas. Šakninis ir tarpinis sertifikatai turėtų būti pirmieji. |
| Žiniatinklio užklausos skirtasis laikas      | Maksimalus laikas (milisekundėmis), per kurį laukiama žiniatinklio tarnybos atsakymo. |
| Kartojimo intervalas           | Intervalas tarp bandymų iškviesti ir atsakymo gavimo iš žiniatinklio tarnybos. Jei nenurodytas joks intervalas, po pirmo nesėkmingo iškvietimo nebus atlikti papildomi bandymai. |
| Mėginimų skaičius              | Didžiausias pakartotinių bandymų iškviesti ir gauti atsakymą iš žiniatinklio tarnybos skaičius. |
| Kartoti iki               | Maksimalus laikas (milisekundėmis), per kurį pakartotiniai iškvietimai gali būti tęsiami. |
| Minimalus atsilikimas         | Mažiausias atsilikimo dažnis, skirtas eksponentiniam pakartotinių bandymų intervalų skaičiavimui. |
| Maksimalus atsilikimas         | Didžiausias atsilikimo dažnis, skirtas eksponentiniam pakartotinių bandymų intervalų skaičiavimui. |
| Saugos protokolas        | Saugos protokolas, kuris bus naudojamas palaikyti ryšį tarp HTTP užklausų ir serverio. (Pagal numatytuosius nustatymus naudojama TLS 1.2 versija.) |

### <a name="applicability-rules"></a>Taikymo taisyklės

Pritaikymo taisyklės leidžia kurti logines taisykles, apibrėžiančias funkcijos nustatymo naudojimo kontekstą. Taigi, verslo dokumento, kuris siunčiamas apdoroti, konteksto ir taikymo taisyklių kriterijų atitikimas nustato, kuri elektroninių SF išrašymo priedo funkcija naudojama apdorojant tą pateikimą.

#### <a name="set-up-applicability-rules"></a>Taikymo taisyklių nustatymas

1. Puslapio **Funkcijos versijos nustatymas** skirtuke **Taikymo taisyklės** pasirinkite **Nauja**, kad įtrauktumėte taikymo taisyklę.

    ![Taikymo taisyklių valdymas](media/e-Invoicing-services-feature-setup-Manage-Actions-Applicability-rules.png)

2. Tinklelyje pasirinkite sąlygas, kurias reikia sugrupuoti.
3. Pasirinkite **Grupuoti sąlygą**.

    ![Sąlygų grupavimas](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-clause.png)

    Kai sąlygos grupuojamos, į tinklelį įtraukiamas naujas stulpelis. Šis stulpelis nurodo sugrupuotų sąlygų loginį operatorių.

    ![Sugrupuotų sąlygų loginis operatorius](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-criterias.png)

Norėdami išgrupuoti sąlygas, pasirinkite sugrupuotas sąlygas, kurias norite išgrupuoti, ir pasirinkite **Išgrupuoti sąlygą**.

![Sąlygų išgrupavimas](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-UnGroup-criterias.png)

> [!NOTE]
> Kai išgrupuojate sąlygą, visada pradėkite nuo giliausio grupavimo lygio.

Toliau pateikta lentelė aprašo laukus, pasiekiamus skirtuke **Taikymo taisyklės**.

| Laukas         | Aprašas |
|---------------|-------------|
| Ir (arba)        | Loginis operatorius. |
| Laukas         | Laukas, kurį reikia naudoti taisyklei sukurti. |
| Operatoriaus tipas | Operatoriaus tipas:<ul><li>Lygu</li><li>Nelygu</li><li>Daugiau nei / mažiau nei</li><li>Daugiau arba lygu / mažiau arba lygu</li><li>Apima</li><li>Prasideda</li></ul> |
| Reikšmė         | Taisyklės kriterijus. |

### <a name="variables"></a>Kintamieji

Galite kurti kintamuosius ir juos naudoti kaip konkretaus veiksmo parametro įvesties reikšmę. Be to, galite juos naudoti keisdamiesi informacija tarp elektroninių SF išrašymo priedo paslaugų ir kliento, kuri yra konkretaus veiksmo vykdymo rezultatas ir pateikimų srauto dalis.

#### <a name="set-up-variables"></a>Nustatyti kintamuosius

- Puslapio **Funkcijos versijos nustatymas** skirtuke **Kintamieji** pasirinkite **Naujas** arba **Naikinti**, norėdami valdyti kintamuosius.

    ![Kintamųjų valdymas](media/e-Invoicing-services-feature-setup-Manage-Variables.png)

Toliau pateikta lentelė aprašo laukus, pasiekiamus skirtuke **Kintamieji**.

| Laukas       | Aprašas |
|-------------|-------------|
| Pavadinimas        | Kintamojo pavadinimas. |
| Aprašas | Trumpas kintamojo aprašas. |
| Tipas        | Kintamojo tipas:<ul><li><strong>Pastovus</strong> – kintamojo turinys yra fiksuotas.</li><li><strong>Iš kliento</strong> – kintamojo turinys įsigyjamas iš „Microsoft Dynamics 365” kliento pateikimo proceso vykdymo metu.</li><li><strong>Klientui</strong> – „Microsoft Dynamics 365” klientas pateikia kintamojo turinį importavimui pateikimo proceso vykdymo metu.</li></ul> |
| Duomenų tipas   | Kintamojo duomenų tipas:<ul><li>Bulio logika</li><li>Data</li><li>Numeris</li><li>UUID</li><li>Eilutė</li><li>Failas</li></ul> |
| Reikšmė       | Kintamojo reikšmė arba veiksmo, kuris nustato kintamojo reikšmę, pavadinimas. |

### <a name="validate-the-feature-setup"></a>Funkcijos nustatymo tikrinimas

- Puslapio **Funkcijos versijos nustatymas**  veiksmų srityje pasirinkite **Tikrinti**, norėdami tikrinti funkcijos versijos nustatymą.

   ![Mygtuko Tikrinti pasirinkimas](media/e-Invoicing-services-feature-setup-Select-Validate-Button.png)

Tikrinimo metu tikrinamas visos konfigūracijos vientisumas. Pavyzdžiui, jei konkretus veiksmo parametras yra privalomas, tačiau jo reikšmė lieka tuščia, tikrinimas aptinka šį nenuoseklumą ir jūs gaunate įspėjimą.

## <a name="environments"></a>Aplinkos

Elektroninių SF išrašymo priedo aplinka turi būti susieta su elektroninių SF išrašymo priedo funkcija ir įjungta. Elektroninių SF išrašymo priedo aplinkos turi būti sukurtos ir publikuojamos iš anksto, naudojant globalizacijos funkcijų konfigūraciją jūsų organizacijos RCS abonemente.

Atlikite toliau pateiktus veiksmus, norėdami įjungti elektroninių SF išrašymo priedo funkcijos elektroninių SF išrašymo priedo aplinką.

1. Puslapio **Elektroninių SF išrašymo priedo funkcijos** skirtuke **Aplinkos** pasirinkite **Įjungti**, kad įtrauktumėte elektroninių SF išrašymo priedo aplinką.
2. Lauke **Galioja nuo** įveskite datą, kada nauja aplinka įsigalioja.

![Elektroninių SF išrašymo priedo aplinkos įjungimas](media/e-Invoicing-services-feature-setup-Select-Enable-e-Invoicing-feature-Environment.png)

## <a name="organizations"></a>Organizacijos

Elektroninių SF išrašymo priedo funkciją galima bendrinti keliose organizacijose.

- Puslapio **Elektroninių SF išrašymo priedo funkcijos** skirtuke **Organizacijos** pasirinkite **Bendrinti su**, kad įtrauktumėte organizaciją, su kuria norite bendrinti elektroninių SF išrašymo priedo funkciją.

Norėdami nustoti bendrinti elektroninių SF išrašymo priedo funkciją su organizacija, pasirinkite **Atšaukti bendrinimą**.

## <a name="versions"></a>Versijos

Versijos padeda valdyti elektroninių SF išrašymo priedo funkcijos ciklą valdant jos būseną. Galite sukurti naują esamos elektroninių SF išrašymo priedo funkcijos versiją arba, kai visa elektroninių SF išrašymo priedo funkcijos konfigūracija baigta, galite pakeisti šios funkcijos būseną į **Baigta**, o tada į **Publikuoti**.

### <a name="create-a-new-version-of-an-existing-electronic-invoicing-feature"></a>Naujos esamos elektroninių SF išrašymo priedo funkcijos versijos kūrimas

1. Puslapio **Elektroninių SF išrašymo priedo funkcijos** kairėje pusėje esančiame tinklelyje pasirinkite elektroninių SF išrašymo priedo funkciją.
2. Skirtuke **Versijos** pasirinkite **Nauja**, kad įtrauktumėte naują elektroninių SF išrašymo priedo funkcijos versiją.

### <a name="change-the-status-of-the-electronic-invoicing-feature"></a>Elektroninių SF išrašymo priedo funkcijos būsenos keitimas

Atlikite toliau pateiktus veiksmus, norėdami valdyti elektroninių SF išrašymo priedo funkcijos ciklą.

1. Puslapio **Elektroninių SF išrašymo priedo funkcijos** kairėje pusėje esančiame tinklelyje pasirinkite elektroninių SF išrašymo priedo funkciją.
2. Skirtuke **Versijos** pasirinkite **Keisti būseną** ir pakeiskite būseną iš **Juodraštis** į **Baigta**.
3. Esate paraginami patvirtinti, kad norite užbaigti elektroninių SF išrašymo priedo funkcijos ir visų jos komponentų konfigūraciją. Pasirinkite **Taip**, norėdami patvirtinti veiksmą, arba **Ne**, norėdami atšaukti.

    > [!NOTE]
    > Pasirinkus **Taip**, konfigūracijos versijų, kurios yra elektroninių SF išrašymo priedo funkcijos komponentai, būsena automatiškai pasikeičia iš **Juodraštis** į **Baigta**.

4. Pasirinkite **Keisti būseną** ir pakeiskite būseną iš **Baigta** į **Publikuoti**.
5. Esate paraginami patvirtinti, kad norite publikuoti elektroninių SF išrašymo priedo funkciją ir visus jos komponentus visuotinėje saugykloje. Pasirinkite **Taip**, norėdami patvirtinti veiksmą, arba **Ne**, norėdami atšaukti.

    > [!NOTE]
    > Pasirinkus **Taip**, konfigūracijos versijų būsena automatiškai pasikeičia iš **Baigta** į **Bendrinama**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]