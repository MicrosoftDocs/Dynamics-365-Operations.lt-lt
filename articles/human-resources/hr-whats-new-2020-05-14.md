---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. gegužės 14 d.)
description: Šioje temoje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2020 m. gegužės 14 d.
author: Darinkramer
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 76ca497cc7fabf737c8a0ee71363f22fd4201ea8
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528502"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. gegužės 14 d.)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources” funkcijos. Pakeitimai taikomi 8.1.3244 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo „Lifecycle Services“ (LCS) palaikymo numerius kaip nuorodą.

## <a name="platform-changes"></a>Platformų pakeitimai

Platformos pakeitimai yra įtraukti į šios savaitės leidimą. Daugiau informacijos žr. [„Finance and Operations” programų 10.0.10 versijos platformos naujinimai (2020 m. gegužės mėn.)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34). Šiame leidime yra įrašytų rodinių klaidų pataisymų ir pakeitimų.
 
## <a name="ensure-common-data-service-picklists-are-consistent-with-leave-enums-436343"></a>Užtikrinti, kad „Common Data Service“ išrinkimo dokumentai atitiktų atostogų išvardijimus (436343)

„Common Data Service“ išrinkimo dokumentai dabar atitinka atostogų išvardijimus.

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a>Leisti vartotojams konfigūruoti atostogų užklausų darbo eigą pagal užklausų kiekį (300044)

Vartotojai gali konfigūruoti atostogų užklausų darbo eigas pagal užklausų kiekį.
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a>Nauja darbuotojo forma duomenis pateikia meniu Rodinys, kai įjungta Išplėstinė sauga (403185)

Šiame leidime išspręsta, kaip veikia darbuotojų peržiūra juridinių subjektų funkcijose, kai yra įgalinta išplėstinė prieiga ir pasiekiami kitų įmonių darbuotojai.

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a>Leisti vykdyti vieno plano ar vienos įmonės atostogų kaupimus (318844)

Šiuo pakeitimu galite vykdyti įmonės arba plano kaupimus.
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a>Rodyti pareigų etato ekvivalentą (FTE) užregistruotų darbuotojų formoje (414658)

FTE reikšmė iš darbuotojo pareigų nustato darbuotojo kaupimo koeficientą, kai prie atostogų tipo įjungta FTE parinktis. Dabar šis laukas yra įtrauktas į formą **Užregistruoti darbuotojai** ir dialogo langą **Masinė registracija**.

## <a name="add-leave-balance-expiration-batch-job-431266"></a>Įtraukti atostogų balanso galiojimo pabaigos paketinę užduotį (431266)

Dabar galima kasdien vykdoma nauja paketinė užduotis. Atėjus galiojimo datai, ji sumažina likusį atostogų balansą.

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a>Kai asmeniniai darbuotojo kontaktai eksportuojami naudojant darbuotojo asmeninių kontaktinių asmenų objektą, neeksportuojami asmeniniai kontaktai su pirminiu ryšio tipu (345893)

Duomenų objektas **Darbuotojo asmeninis kontaktinis asmuo** (**HcmPersonalContactPersonEntity** (DMF) ir **PersonalContactPerson** („OData“)) negalėjo eksportuoti asmeninių kontaktų, kurių ryšio tipas yra **Pirminis**. Šis problema išspręsta asmeniniams kontaktams, sukurtiems po šio pakeitimo. Esami asmeniniai kontaktai, kurių tipas yra **Pirminis**, bus sutvarkyti vėlesniame leidime.

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a>Priežasčių kodai rodomi skirtinguose scenarijuose, kai jie yra pažymėti kaip Atostogos ir neatvykimas, o supaprastinta darbuotojo forma yra suaktyvinta (434163)

Kai įgalinsate supaprastintą darbuotojo įrašą, šis pakeitimas apriboja priežasčių kodus (tik kodai Atostogos ir neatvykimas).

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a>Peržiūros funkcija Priskirti atostogų planą darbuotojams ateityje rodo klaidą (433555)

Šis pakeitimas ištaiso klaidą, kai atostogų plane yra priskirti du atostogų tipai, ir jūs bandote priskirti darbuotoją.

## <a name="getting-started-banner-appears-for-all-users-441731"></a>Reklaminė juosta Darbo pradžia rodoma visiems vartotojams (441731)

Šiuo pakeitimu reklaminė juosta Darbo pradžia yra paslėpta vartotojams, kurie nėra sistemos administratoriai arba duomenų valdymo administratoriai. 

## <a name="the-common-data-service-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a>„Common Data Service“ darbininko adreso objektas veikia kitaip nei „Human Resources“ datos ir laiko įsigaliojimo datos (425071)

Šis pakeitimas suvienodina adresų informaciją tam tikruose scenarijuose pagal adreso datas.

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a>Nepavyksta įtraukti priedo prie patvirtintos atostogų užklausos (425407)

Šios savaitės leidimas leis įtraukti priedus prie patvirtintų atostogų užklausų, nekeičiant atostogų užklausos.

## <a name="in-preview"></a>Peržiūros režimu

## <a name="leave-suspension"></a>Atostogų sustabdymas

Programoje „Human Resources” galite sustabdyti darbuotojo atostogas ir neatvykimą. Atostogų sustabdymas sustabdo pasirinktų atostogų tipų atostogų kaupimus. Jei sustabdymas įvyksta po to, kai kaupimas buvo apdorotas, atostogų sustabdymas sukuria proporcingai paskirstytą darbuotojo atostogų balanso koregavimą. Daugiau informacijos žr. [Atostogų sulaikymas](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Vartotojo patirties naujinimas nurodyti, jog kaupimas sustabdytas (429550)

Dabar vartotojo patirtis nurodo, kad plano kaupimas buvo sustabdytas.

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>Nurodytų atostogų tipų atostogų kaupimo sustabdymas (272447)

Šiame leidime personalas gali sukurti taisyklę, skirtą sustabdyti darbuotojų, įvedusių atostogų užklausas neapmokamoms atostogoms, atostogų kaupimus. Neapmokamos atostogos gali būti tipas, tačiau tai neprivaloma. Galite sustabdyti bet kokias atostogas, pagrįstas kitu atostogų tipu.

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>DMF objektas pasiekiamas kaupimo sustabdymams (429549)

DMF objektas dabar pasiekiamas kaupimo sustabdymams.

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>Priežasties kodo įtraukimas į kaupimo sustabdymus (429547)

Į kaupimo sustabdymus įtraukti priežasties kodai.

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>Perėjimo iš „Human Resources“ parametrų į atostogų ir neatvykimų parametrus pradžia

Šiame leidime pradedama jungti „Human Resources“ parametrus su atostogų ir neatvykimų parametrais.

## <a name="carry-forward-rules"></a>Perkėlimo taisyklės

Galite nurodyti perkėlimo atostogų tipą, skirtą perkėlimo balansams ir į kurį perkeliami perkeliamų balansų koregavimai. Pavyzdžiui, jei darbuotojas perkelia 10 dienų, toms 10 dienų galite pasirinkti kitą atostogų tipą. Daugiau informacijos žr. [Atostogų ir neatvykimų tipų konfigūravimas](hr-leave-and-absence-types.md).

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]