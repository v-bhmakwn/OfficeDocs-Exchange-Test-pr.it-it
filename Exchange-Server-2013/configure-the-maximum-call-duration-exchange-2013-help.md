﻿---
title: 'Configurare la durata massima di chiamata: Exchange 2013 Help'
TOCTitle: Configurare la durata massima di chiamata
ms:assetid: 01aa40d2-f918-472b-bace-158222143484
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Ee423535(v=EXCHG.150)
ms:contentKeyID: 50479907
ms.date: 05/22/2018
mtps_version: v=EXCHG.150
ms.translationtype: MT
---

# Configurare la durata massima di chiamata

 

_**Si applica a:** Exchange Online, Exchange Server 2013, Exchange Server 2016_

_**Ultima modifica dell'argomento:** 2012-11-09_

È possibile specificare il numero massimo di minuti per cui una chiamata in arrivo può rimanere connessa al sistema senza essere trasferita a un numero di interno valido prima che sia terminata. Per la maggior parte delle organizzazioni, l'impostazione predefinita per questo valore deve essere di: 30 minuti. Questa impostazione viene applicata a tutte le chiamate, incluse le chiamate in ingresso da Outlook Voice Access, le chiamate vocali interne all'organizzazione, le chiamate vocali dirette agli operatori automatici di messaggistica unificata e le chiamate fax provenienti da utenti esterni all'organizzazione.

Il valore di questa impostazione può essere compreso tra 10 e 120. L'impostazione di un valore troppo basso può causare la disconnessione delle chiamate in arrivo prima del loro completamento. Ad esempio, se l'organizzazione riceve molti messaggi fax di grandi dimensioni, è possibile che si desideri aumentare questo valore rispetto all'impostazione predefinita, così da consentire la ricezione di tutte le pagine dei fax.

Per altre attività relative ai dial plan di messaggistica unificata, vedere [Procedure di messaggistica unificata dial plan](um-dial-plan-procedures-exchange-2013-help.md).

## Che cosa è necessario sapere prima di iniziare?

  - Tempo stimato per il completamento: Meno di 1 minuto.

  - Per eseguire queste procedure, è necessario disporre delle autorizzazioni appropriate. Per sapere quali autorizzazioni sono necessarie, vedere "Dial plan di messaggistica unificata" nell'argomento [Autorizzazioni della messaggistica unificate](unified-messaging-permissions-exchange-2013-help.md).

  - È necessario confermare la creazione del dial plan di messaggistica unificata prima di eseguire le procedure. Per la procedura dettagliata, vedere [Creazione di un dial plan di messaggistica unificata](create-a-um-dial-plan-exchange-2013-help.md).

  - Per informazioni sui tasti di scelta rapida che è possibile utilizzare con le procedure in questo argomento, vedere [Tasti di scelta rapida nell'interfaccia di amministrazione di Exchange](keyboard-shortcuts-in-the-exchange-admin-center-exchange-online-protection-help.md).


> [!TIP]
> Problemi? È possibile richiedere supporto nei forum di Exchange. I forum sono disponibili sui seguenti siti: <A href="https://go.microsoft.com/fwlink/p/?linkid=60612">Exchange Server</A>, <A href="https://go.microsoft.com/fwlink/p/?linkid=267542">Exchange Online</A> o <A href="https://go.microsoft.com/fwlink/p/?linkid=285351">Exchange Online Protection</A>..



## Operazione desiderata?

## Utilizzo dell'interfaccia di amministrazione di Exchange per la configurazione della durata massima delle chiamate

1.  Nell'interfaccia di amministrazione di Exchange, navigare a **Messaggistica unificata** \> **Dial plan di messaggistica unificata**.

2.  Nella visualizzazione elenco, selezionare il dial plan di messaggistica unificata che si desidera modificare, quindi fare clic su **Modifica**![Icona Modifica](images/JJ218640.6f53ccb2-1f13-4c02-bea0-30690e6ea71d(EXCHG.150).gif "Icona Modifica").

3.  Nella pagina **Dial plan di messaggistica unificata**, fare clic su **Configura**.

4.  In **Impostazioni**, immettere il numero massimo di minuti in **Durata massima della chiamata (minuti)**.

5.  Fare clic su **Salva**.

## Configurazione della durata massima della chiamata tramite Shell

In questo esempio viene impostata la durata massima della chiamata su 10 minuti su un dial plan di messaggistica unificata denominato `MyUMDialPlan`.

    Set-UMDialPlan -identity MyUMDialPlan -MaxCallDuration 10

