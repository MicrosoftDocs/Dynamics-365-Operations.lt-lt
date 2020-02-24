---
title: Pasirinktinės saugyklos vietos, skirtos sugeneruotiems dokumentams, nurodymas
description: Šioje temoje paaiškinama, kaip išplėsti elektroninio ataskaitų (ER) formatų sugeneruotų dokumentų saugojimo vietų sąrašą.
author: NickSelin
manager: AnnBe
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: 45a2335d7a661ddc1d8907c56ae8193387f44e26
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030871"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a><span data-ttu-id="5f055-103">Pasirinktinės saugyklos vietos, skirtos sugeneruotiems dokumentams, nurodymas</span><span class="sxs-lookup"><span data-stu-id="5f055-103">Specify a custom storage location for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5f055-104">Elektroninių ataskaitų (ER) sistemos programavimo sąsaja (API) suteikia galimybę išplėsti ER formatų sugeneruotų dokumentų saugojimo vietų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="5f055-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="5f055-105">Šioje temoje pateikiama pagrindinių užduočių, kurias turite atlikti, kad įtrauktumėte pasirinktinę saugojimo vietą, apžvalga.</span><span class="sxs-lookup"><span data-stu-id="5f055-105">This topic includes an overview of the main tasks that you must complete to add a custom storage location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5f055-106">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="5f055-106">Prerequisites</span></span>

<span data-ttu-id="5f055-107">Turite įdiegti topologiją, kuri palaiko nuolatinę komponavimo versiją.</span><span class="sxs-lookup"><span data-stu-id="5f055-107">You must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="5f055-108">(Daugiau informacijos žr. [Visuotinis topologijų, palaikančių nuolatinio komponavimo versijų ir bandymo automatizavimo funkciją, diegimas](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Jums reikia vieno iš toliau nurodytų vaidmenų prieigos prie šios topologijos.</span><span class="sxs-lookup"><span data-stu-id="5f055-108">(For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="5f055-109">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="5f055-109">Electronic reporting developer</span></span>
- <span data-ttu-id="5f055-110">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="5f055-110">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="5f055-111">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="5f055-111">System administrator</span></span>

<span data-ttu-id="5f055-112">Taip pat jums reikia prieigos prie šios topologijos kūrimo aplinkos.</span><span class="sxs-lookup"><span data-stu-id="5f055-112">You must also have access to the development environment for this topology.</span></span>

## <a name="create-or-import-an-er-format-configuration"></a><span data-ttu-id="5f055-113">ER formato konfigūracijos kūrimas arba importavimas</span><span class="sxs-lookup"><span data-stu-id="5f055-113">Create or import an ER format configuration</span></span>

<span data-ttu-id="5f055-114">Esamoje topologijoje [sukurkite naują ER formatą](tasks/er-format-configuration-2016-11.md), kad generuotumėte dokumentus, kurių pasirinktinę saugojimo vietą planuojate įtraukti.</span><span class="sxs-lookup"><span data-stu-id="5f055-114">In the current topology, [create a new ER format](tasks/er-format-configuration-2016-11.md) to generate documents that you plan to add a custom storage location for.</span></span> <span data-ttu-id="5f055-115">Taip pat galite [importuoti esamą ER formatą į šią topologiją](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="5f055-115">Alternatively, [import an existing ER format into this topology](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![Formato dizaino įrankio puslapis](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> <span data-ttu-id="5f055-117">Jūsų kuriamame arba importuojamame ER formate turi būti bent vienas iš toliau nurodytų formato elementų.</span><span class="sxs-lookup"><span data-stu-id="5f055-117">The ER format that you create or import must contain at least one of the following format elements:</span></span>
>
> - <span data-ttu-id="5f055-118">Failas</span><span class="sxs-lookup"><span data-stu-id="5f055-118">File</span></span>
> - <span data-ttu-id="5f055-119">Aplankas</span><span class="sxs-lookup"><span data-stu-id="5f055-119">Folder</span></span>
> - <span data-ttu-id="5f055-120">Sujungimas</span><span class="sxs-lookup"><span data-stu-id="5f055-120">Merger</span></span>
> - <span data-ttu-id="5f055-121">Priedas</span><span class="sxs-lookup"><span data-stu-id="5f055-121">Attachment</span></span>

## <a name="create-a-new-document-type"></a><span data-ttu-id="5f055-122">Naujo dokumento tipo kūrimas</span><span class="sxs-lookup"><span data-stu-id="5f055-122">Create a new document type</span></span>

<span data-ttu-id="5f055-123">Norėdami nurodyti, kaip dokumentai, kuriuos generuoja ER formatas, turi būti nukreipiami, turite sukonfigūruoti [Elektroninių ataskaitų (ER) paskirties vietos](electronic-reporting-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="5f055-123">To specify how documents that an ER format generates are routed, you must configure [Electronic reporting (ER) destinations](electronic-reporting-destinations.md).</span></span> <span data-ttu-id="5f055-124">Kiekvienoje ER paskirties vietoje, kuri sukonfigūruota saugoti sugeneruotus dokumentus kaip failus, turite nurodyti dokumentų valdymo sistemos dokumento tipą.</span><span class="sxs-lookup"><span data-stu-id="5f055-124">In each ER destination that is configured to store generated documents as files, you must specify a document type of the Document management framework.</span></span> <span data-ttu-id="5f055-125">Galima naudoti skirtingus dokumentų tipus norint nukreipti dokumentus, kuriuos sugeneruoja skirtingi ER formatai.</span><span class="sxs-lookup"><span data-stu-id="5f055-125">Different document types can be used to route documents that different ER formats generate.</span></span>

1. <span data-ttu-id="5f055-126">Įtraukite anksčiau sukurto arba importuoto ER formato [dokumento tipą](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management).</span><span class="sxs-lookup"><span data-stu-id="5f055-126">Add a new [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) for the ER format that you created or imported earlier.</span></span> <span data-ttu-id="5f055-127">Toliau pateiktame paveikslėlyje dokumento tipas yra **FileX**.</span><span class="sxs-lookup"><span data-stu-id="5f055-127">In the illustration that follows, the document type is **FileX**.</span></span>
2. <span data-ttu-id="5f055-128">Norėdami atskirti šį dokumento tipą nuo kitų dokumentų tipų, įtraukite tam tikrą raktažodį į jo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="5f055-128">To differentiate this document type from other document types, include a specific keyword in its name.</span></span> <span data-ttu-id="5f055-129">Pavyzdžiui, toliau pateiktame paveikslėlyje pavadinimas yra **(VIETINIS) aplankas**.</span><span class="sxs-lookup"><span data-stu-id="5f055-129">For example, in the illustration that follows, the name is **(LOCAL) folder**.</span></span>
3. <span data-ttu-id="5f055-130">Lauke **Klasė** nurodykite **Pridėti failą**.</span><span class="sxs-lookup"><span data-stu-id="5f055-130">In the **Class** field, specify **Attach file**.</span></span>
4. <span data-ttu-id="5f055-131">Lauke **Grupė** nurodykite **Failas**.</span><span class="sxs-lookup"><span data-stu-id="5f055-131">In the **Group** field, specify **File**.</span></span>

![Puslapis Dokumentų tipai](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> <span data-ttu-id="5f055-133">Dokumentų tipai priklauso nuo įmonės.</span><span class="sxs-lookup"><span data-stu-id="5f055-133">Document types are company-specific.</span></span> <span data-ttu-id="5f055-134">Norėdami naudoti ER formatą ir sukonfigūruotą paskirties vietą keliose įmonėse, turite sukonfigūruoti atskirą dokumento tipą, skirtą kiekvienai įmonei.</span><span class="sxs-lookup"><span data-stu-id="5f055-134">To use an ER format with a configured destination in multiple companies, you must configure a separate document type in each company.</span></span>

## <a name="review-source-code"></a><span data-ttu-id="5f055-135">Šaltinio kodo peržiūra</span><span class="sxs-lookup"><span data-stu-id="5f055-135">Review source code</span></span>

<span data-ttu-id="5f055-136">Peržiūrėkite klasės **ERDocuManagement** metodo **insertFile()** kodą.</span><span class="sxs-lookup"><span data-stu-id="5f055-136">Review the code of the **insertFile()** method of the **ERDocuManagement** class.</span></span> <span data-ttu-id="5f055-137">Atkreipkite dėmesį, kad įvykis **AttachingFile()** paleidžiamas pridedant sugeneruotą failą prie įrašo.</span><span class="sxs-lookup"><span data-stu-id="5f055-137">Notice that the **AttachingFile()** event is raised while the generated file is attached to a record.</span></span>

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

<span data-ttu-id="5f055-138">Įvykis **AttachingFile()** paleidžiamas, kai apdorojamos toliau nurodytos ER paskirties vietos.</span><span class="sxs-lookup"><span data-stu-id="5f055-138">The **AttachingFile()** event is raised when the following ER destinations are processed:</span></span>

- <span data-ttu-id="5f055-139">**Archyvas** – kai naudojama ši paskirties vieta, lentelėje ERFormatMappingRunJobTable sukuriamas naujas paleisto ER formato įrašas.</span><span class="sxs-lookup"><span data-stu-id="5f055-139">**Archive** – When this destination is used, a new record for the ER format that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="5f055-140">Šio įrašo lauke **Suarchyvuota** nustatoma reikšmė **False**.</span><span class="sxs-lookup"><span data-stu-id="5f055-140">The **Archived** field in this record is set to **False**.</span></span> <span data-ttu-id="5f055-141">Je ER formatas įvykdomas sėkmingai, sugeneruotas dokumentas pridedamas prie šio įrašo ir paleidžiamas įvykis **AttachingFile()**.</span><span class="sxs-lookup"><span data-stu-id="5f055-141">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="5f055-142">Dokumento tipas, pasirinktas šioje ER paskirties vietoje, nurodo pridėto failo saugojimo vietą („Microsoft Azure“ saugyklos arba „Microsoft SharePoint“ aplankas).</span><span class="sxs-lookup"><span data-stu-id="5f055-142">The document type that is selected in this ER destination determines the storage location for the attached file (Microsoft Azure Storage or a Microsoft SharePoint folder).</span></span>
- <span data-ttu-id="5f055-143">**Užduoties archyvas** – kai naudojama ši paskirties vieta, lentelėje ERFormatMappingRunJobTable sukuriamas naujas paleisto ER formato įrašas.</span><span class="sxs-lookup"><span data-stu-id="5f055-143">**Job archive** – When this destination is used, a new record for the ER form that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="5f055-144">Šio įrašo lauke **Suarchyvuota** nustatoma reikšmė **True**.</span><span class="sxs-lookup"><span data-stu-id="5f055-144">The **Archived** field in this record is set to **True**.</span></span> <span data-ttu-id="5f055-145">Je ER formatas įvykdomas sėkmingai, sugeneruotas dokumentas pridedamas prie šio įrašo ir paleidžiamas įvykis **AttachingFile()**.</span><span class="sxs-lookup"><span data-stu-id="5f055-145">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="5f055-146">ER parametruose sukonfigūruoto dokumento tipas nurodo pridėto failo saugojimo vietą („Azure“ saugyklos arba „SharePoint“ aplankas).</span><span class="sxs-lookup"><span data-stu-id="5f055-146">The document type that is configured in the ER parameters determines the storage location for the attached file (Azure Storage or a SharePoint folder).</span></span>

![Elektroninių ataskaitų parametrų puslapis](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a><span data-ttu-id="5f055-148">ER paskirties vietos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="5f055-148">Configure an ER destination</span></span>

1. <span data-ttu-id="5f055-149">Sukonfigūruokite vieno iš anksčiau minėtų sukurto arba importuoto ER formato elementų (failo, aplanko, susijungimo arba priedo) suarchyvuotą paskirties vietą.</span><span class="sxs-lookup"><span data-stu-id="5f055-149">Configure the archived destination for one of the previously mentioned elements (file, folder, merger, or attachment) of the ER format that you created or imported.</span></span> <span data-ttu-id="5f055-150">Patarimų žr. [ER paskirties vietų konfigūravimas](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span><span class="sxs-lookup"><span data-stu-id="5f055-150">For guidance, see [ER Configure destinations](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span></span>
2. <span data-ttu-id="5f055-151">Naudoti anksčiau įtrauktą sukonfigūruotos paskirties vietos dokumento tipą.</span><span class="sxs-lookup"><span data-stu-id="5f055-151">Use the document type that you added earlier for the configured destination.</span></span> <span data-ttu-id="5f055-152">(Pavyzdžiui, šioje temoje dokumento tipas yra **FileX**.)</span><span class="sxs-lookup"><span data-stu-id="5f055-152">(For the example in this topic, the document type is **FileX**.)</span></span>

![Dialogo langas Paskirties vietos parametrai](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a><span data-ttu-id="5f055-154">Šaltinio kodo modifikavimas</span><span class="sxs-lookup"><span data-stu-id="5f055-154">Modify source code</span></span>

1. <span data-ttu-id="5f055-155">Įtraukite naują klasę į savo „Microsoft Visual Studio“ projektą ir parašykite kodą, kad užsiprenumeruotumėte pirmiau paminėtą įvykį **AttachingFile()**.</span><span class="sxs-lookup"><span data-stu-id="5f055-155">Add a new class to your Microsoft Visual Studio project, and write code to subscribe to the **AttachingFile()** event that was mentioned earlier.</span></span> <span data-ttu-id="5f055-156">(Daugiau informacijos apie naudojamo šablono išplėtimą žr. [Atsakymas naudojant EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) Pavyzdžiui, naujoje klasėje parašykite kodą, kuris atlieka toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5f055-156">(For more information about the extensibility pattern that is used, see [Respond by using EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) For example, in the new class, write code that performs the following actions:</span></span>

    1. <span data-ttu-id="5f055-157">Saugokite sugeneruotus failus serverio, kuriame veikia programos objektų serverio (AOS) tarnyba, vietinės failų sistemos aplanke.</span><span class="sxs-lookup"><span data-stu-id="5f055-157">Store generated files in a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    2. <span data-ttu-id="5f055-158">Saugokite šiuos sugeneruoti failus tik kai naudojamas naujas dokumento tipas (pvz., tipas **FileX**, kurio pavadinime yra raktažodis „(VIETINIS)“) ir failas yra pridėtas prie įrašo ER vykdymo užduočių žurnale.</span><span class="sxs-lookup"><span data-stu-id="5f055-158">Store these generated files only when the new document type (for example, the **FileX** type that has the "(LOCAL)" keyword in its name) is used while a file is attached to the record in the ER execution job log.</span></span>

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

2. <span data-ttu-id="5f055-159">Perkurkite savo projektą.</span><span class="sxs-lookup"><span data-stu-id="5f055-159">Rebuild your project.</span></span>

## <a name="run-the-er-format-that-you-created-or-imported"></a><span data-ttu-id="5f055-160">Sukurto arba importuoto ER formato vykdymas</span><span class="sxs-lookup"><span data-stu-id="5f055-160">Run the ER format that you created or imported</span></span>

1. <span data-ttu-id="5f055-161">Vykdykite sukurtą arba importuotą ER formatą.</span><span class="sxs-lookup"><span data-stu-id="5f055-161">Execute the ER format that you created or imported.</span></span>
2. <span data-ttu-id="5f055-162">Pasirinkite **Organizacijos administravimas \> Elektroninės ataskaitos \> Elektroninės ataskaitos užduotys**.</span><span class="sxs-lookup"><span data-stu-id="5f055-162">Go to **Organization administration \> Electronic reporting \> Electronic reporting jobs**.</span></span> <span data-ttu-id="5f055-163">Raskite sukurtą šios vykdymo užduoties įrašą, prie kurio pridėtas sugeneruotas failas.</span><span class="sxs-lookup"><span data-stu-id="5f055-163">Find the record that was created for this execution job, and that has the generated file attached to it.</span></span>
3. <span data-ttu-id="5f055-164">Raskite tą patį sugeneruotą failą aplanke **C:\\0**.</span><span class="sxs-lookup"><span data-stu-id="5f055-164">Explore the local **C:\\0** folder to find same generated file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5f055-165">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="5f055-165">Additional resources</span></span>

- [<span data-ttu-id="5f055-166">Elektroninių ataskaitų (ER) paskirties vietos</span><span class="sxs-lookup"><span data-stu-id="5f055-166">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="5f055-167">Išplečiamumo pagrindinis puslapis</span><span class="sxs-lookup"><span data-stu-id="5f055-167">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)
