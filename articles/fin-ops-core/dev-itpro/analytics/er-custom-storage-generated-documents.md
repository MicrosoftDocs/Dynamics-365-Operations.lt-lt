---
title: Pasirinktinės saugyklos vietos, skirtos sugeneruotiems dokumentams, nurodymas
description: Šioje temoje paaiškinama, kaip išplėsti elektroninio ataskaitų (ER) formatų sugeneruotų dokumentų saugojimo vietų sąrašą.
author: NickSelin
manager: AnnBe
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: b71ad5a9701922eb94b1d611e2d3f6a945ce6c06
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562243"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a>Pasirinktinės saugyklos vietos, skirtos sugeneruotiems dokumentams, nurodymas

[!include[banner](../includes/banner.md)]

Elektroninių ataskaitų (ER) sistemos programavimo sąsaja (API) suteikia galimybę išplėsti ER formatų sugeneruotų dokumentų saugojimo vietų sąrašą. Šioje temoje pateikiama pagrindinių užduočių, kurias turite atlikti, kad įtrauktumėte pasirinktinę saugojimo vietą, apžvalga.

## <a name="prerequisites"></a>Būtinieji komponentai

Turite įdiegti topologiją, kuri palaiko nuolatinę komponavimo versiją. (Daugiau informacijos žr. [Visuotinis topologijų, palaikančių nuolatinio komponavimo versijų ir bandymo automatizavimo funkciją, diegimas](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Jums reikia vieno iš toliau nurodytų vaidmenų prieigos prie šios topologijos.

- Elektroninės ataskaitos kūrėjas
- Elektroninės ataskaitos funkcijų konsultantas
- Sistemos administratorius

Taip pat jums reikia prieigos prie šios topologijos kūrimo aplinkos.

## <a name="create-or-import-an-er-format-configuration"></a>ER formato konfigūracijos kūrimas arba importavimas

Esamoje topologijoje [sukurkite naują ER formatą](tasks/er-format-configuration-2016-11.md), kad generuotumėte dokumentus, kurių pasirinktinę saugojimo vietą planuojate įtraukti. Taip pat galite [importuoti esamą ER formatą į šią topologiją](general-electronic-reporting-manage-configuration-lifecycle.md).

![Formato dizaino įrankio puslapis](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> Jūsų kuriamame arba importuojamame ER formate turi būti bent vienas iš toliau nurodytų formato elementų.
>
> - Failas
> - Aplankas
> - Sujungimas
> - Priedas

## <a name="create-a-new-document-type"></a>Naujo dokumento tipo kūrimas

Norėdami nurodyti, kaip dokumentai, kuriuos generuoja ER formatas, turi būti nukreipiami, turite sukonfigūruoti [Elektroninių ataskaitų (ER) paskirties vietos](electronic-reporting-destinations.md). Kiekvienoje ER paskirties vietoje, kuri sukonfigūruota saugoti sugeneruotus dokumentus kaip failus, turite nurodyti dokumentų valdymo sistemos dokumento tipą. Galima naudoti skirtingus dokumentų tipus norint nukreipti dokumentus, kuriuos sugeneruoja skirtingi ER formatai.

1. Įtraukite anksčiau sukurto arba importuoto ER formato [dokumento tipą](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management). Toliau pateiktame paveikslėlyje dokumento tipas yra **FileX**.
2. Norėdami atskirti šį dokumento tipą nuo kitų dokumentų tipų, įtraukite tam tikrą raktažodį į jo pavadinimą. Pavyzdžiui, toliau pateiktame paveikslėlyje pavadinimas yra **(VIETINIS) aplankas**.
3. Lauke **Klasė** nurodykite **Pridėti failą**.
4. Lauke **Grupė** nurodykite **Failas**.

![Puslapis Dokumentų tipai](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> Dokumentų tipai priklauso nuo įmonės. Norėdami naudoti ER formatą ir sukonfigūruotą paskirties vietą keliose įmonėse, turite sukonfigūruoti atskirą dokumento tipą, skirtą kiekvienai įmonei.

## <a name="review-source-code"></a>Šaltinio kodo peržiūra

Peržiūrėkite klasės **ERDocuManagement** metodo **insertFile()** kodą. Atkreipkite dėmesį, kad įvykis **AttachingFile()** paleidžiamas pridedant sugeneruotą failą prie įrašo.


```xpp
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

Įvykis **AttachingFile()** paleidžiamas, kai apdorojamos toliau nurodytos ER paskirties vietos.

- **Archyvas** – kai naudojama ši paskirties vieta, lentelėje ERFormatMappingRunJobTable sukuriamas naujas paleisto ER formato įrašas. Šio įrašo lauke **Suarchyvuota** nustatoma reikšmė **False**. Je ER formatas įvykdomas sėkmingai, sugeneruotas dokumentas pridedamas prie šio įrašo ir paleidžiamas įvykis **AttachingFile()**. Dokumento tipas, pasirinktas šioje ER paskirties vietoje, nurodo pridėto failo saugojimo vietą („Microsoft Azure“ saugyklos arba „Microsoft SharePoint“ aplankas).
- **Užduoties archyvas** – kai naudojama ši paskirties vieta, lentelėje ERFormatMappingRunJobTable sukuriamas naujas paleisto ER formato įrašas. Šio įrašo lauke **Suarchyvuota** nustatoma reikšmė **True**. Je ER formatas įvykdomas sėkmingai, sugeneruotas dokumentas pridedamas prie šio įrašo ir paleidžiamas įvykis **AttachingFile()**. ER parametruose sukonfigūruoto dokumento tipas nurodo pridėto failo saugojimo vietą („Azure“ saugyklos arba „SharePoint“ aplankas).

![Elektroninių ataskaitų parametrų puslapis](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a>ER paskirties vietos konfigūravimas

1. Sukonfigūruokite vieno iš anksčiau minėtų sukurto arba importuoto ER formato elementų (failo, aplanko, susijungimo arba priedo) suarchyvuotą paskirties vietą. Patarimų žr. [ER paskirties vietų konfigūravimas](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).
2. Naudoti anksčiau įtrauktą sukonfigūruotos paskirties vietos dokumento tipą. (Pavyzdžiui, šioje temoje dokumento tipas yra **FileX**.)

![Dialogo langas Paskirties vietos parametrai](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a>Šaltinio kodo modifikavimas

1. Įtraukite naują klasę į savo „Microsoft Visual Studio“ projektą ir parašykite kodą, kad užsiprenumeruotumėte pirmiau paminėtą įvykį **AttachingFile()**. (Daugiau informacijos apie naudojamo šablono išplėtimą žr. [Atsakymas naudojant EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) Pavyzdžiui, naujoje klasėje parašykite kodą, kuris atlieka toliau nurodytus veiksmus.

    1. Saugokite sugeneruotus failus serverio, kuriame veikia programos objektų serverio (AOS) tarnyba, vietinės failų sistemos aplanke.
    2. Saugokite šiuos sugeneruoti failus tik kai naudojamas naujas dokumento tipas (pvz., tipas **FileX**, kurio pavadinime yra raktažodis „(VIETINIS)“) ir failas yra pridėtas prie įrašo ER vykdymo užduočių žurnale.

    ```xpp
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. Perkurkite savo projektą.

## <a name="run-the-er-format-that-you-created-or-imported"></a>Sukurto arba importuoto ER formato vykdymas

1. Vykdykite sukurtą arba importuotą ER formatą.
2. Pasirinkite **Organizacijos administravimas \> Elektroninės ataskaitos \> Elektroninės ataskaitos užduotys**. Raskite sukurtą šios vykdymo užduoties įrašą, prie kurio pridėtas sugeneruotas failas.
3. Raskite tą patį sugeneruotą failą aplanke **C:\\0**.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų (ER) paskirties vietos](electronic-reporting-destinations.md)
- [Išplečiamumo pagrindinis puslapis](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]