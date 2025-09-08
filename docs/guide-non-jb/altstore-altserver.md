---
title: Installare AltServer/AltStore
description: Guida per l'installazione di AltServer/AltStore
sidebar_position: 1
---

:::info
È consigliato seguire la guida per [Installare SideStore](sidestore.md) in quanto possiede le stesse funzionalità di AltStore eliminando la necessità di un computer ogni volta che si intende installare/refreshare un'app
:::

![img](https://telegra.ph/file/43388be4a77e3ead5a11e.png)

## Cos'è AltStore

AltStore è un'applicazione iOS (in modalità sandbox) che ti consente di installare (tramite sideloading) le app essenzialmente "ingannando" il tuo telefono, facendogli credere che stia installando app che tu stesso hai creato, quando in realtà può essere qualsiasi app.

## Cos'è AltServer

AltServer è un'applicazione per macOS e Windows che ti consente di installare Altstore nel tuo telefono oppure di installare (tramite sideloading) qualunque app direttamente dal tuo computer.

### Come funziona

AltStore è un app store alternativo per dispositivi che non richiede jailbreak.

A differenza di altri store non ufficiali reperibili da Safari, AltStore non si basa su certificati aziendali che Apple ha più volte bloccato, si basa invece su una funzione per sviluppatori che ti consente di utilizzare il tuo ID Apple per installare app.

### Premesse

1. AltStore ed AltServer richiedono le credenziali d'accesso di un ID Apple per comunicare a tuo nome con i server per sviluppatori di Apple.

2. Apple limita gli account sviluppatore gratuiti a generare **solo 10 App ID** per settimana. Gli App ID non possono essere eliminati, scadono automaticamente dopo una settimana.

Ogni app ed estensione per app installate con AltStore devono registrare un **App ID**.

AltStore rinnoverà automaticamente gli App ID per tutte le app attive ogni volta che stanno per scadere. Per farlo il dispositivo dovrà collegarsi ad AltServer: via cavo, via Wi-Fi oppure tramite AltDaemon (qualora si avesse il jailbreak).

AltStore per connettersi al computer, su cui è installato AltServer, necessità che siano aperte in background le applicazioni di AltServer e Mail (solo per macOS).

![img](https://telegra.ph/file/32575a0f65bd1b3202506.png)

Per visualizzare la sezione App IDs occorre accedere alla sezione "My Apps" e cliccare sulla scritta verde "View App IDs".

3. Gli **account sviluppatore gratuiti sono limitati ad installare** contemporaneamente **solo 3 app**. Per ovviare a questo problema è possibile disattivare le app.

Le app inattive vengono sottoposte a backup e disinstallate in modo che non vengano conteggiate nel totale. Nel momento in cui le app verranno reinstallate, verranno recuperati i tutti i loro dati. È possibile esportare i backup della relativa app altrove, ad esempio su un servizio di Cloud, per poi essere ripristinato in un secondo momento.

![img](https://telegra.ph/file/24ae3201502f69f3f2d16.png)

Effettuando un Haptic Touch sull'app sarà possibile effettuare un Backup dei dati e disattivare l'app.

### Compatibilità

1. Richiede che il dispositivo abbia: 
    - iOS/iPadOS 12.2 o superiori per utilizzare AltStore.
    - iOS/iPadOS per utilizzare il sideload di AltServer.

2. Richiede un computer con:
    - macOS 11 o successivi
    - Windows 10/11 (con iTunes e iCloud in versione .exe)
        - iTunes e iCloud installati attraverso il Microsoft Store non vanno bene.

**Disinstallare iTunes e iCloud dal Microsoft Store:**

- Dalle *Impostazioni* di Windows recarsi nella sezione *App e funzionalità*.
- Tramite la barra di ricerca cercare con la parola apple.
- Disinstallare *iTunes, iCloud* ed tutti i relativi driver di funzionamento *Supporto applicazioni Apple*.
- Effettuare un riavvio del computer.

### Download

È possibile scaricare AltServer dalla pagina [altstore.io](https://altstore.io/).

Link di download diretti:

- AltServer per [Mac](https://cdn.altstore.io/file/altstore/altserver.zip)
- AltServer per [Windows](https://cdn.altstore.io/file/altstore/altinstaller.zip)
    - iTunes [64 bit](https://www.apple.com/itunes/download/win64) o [32 bit](https://www.apple.com/itunes/download/win32)
    - [iCloud](https://updates.cdn-apple.com/2020/windows/001-39935-20200911-1A70AA56-F448-11EA-8CC0-99D41950005E/iCloudSetup.exe)

### AltServer Mac

- Scaricato **AltServer**, spostarlo nella cartella *Applicazioni* del Mac. 
- Dalla pagina *Applicazioni* del Finder aprire AltServer con tasto destro **Apri**. 
- Confermare l’avviso di apertura cliccando **Apri**.
- Guardando nella Menu Bar, in alto a sinistra dello schermo si troverà l’icona di AltServer.

![img](https://telegra.ph/file/c5d797b6388fcdd7971de.png)

- Cliccare nella sezione **Install Mail Plug-in.**

*AltServer richiede un plug-in di Mail per recuperare le informazioni necessarie sul tuo ID Apple che invierà ad Apple per poter firmare le App.*

- Cliccare su **Install Plug-in** e autorizzare l’operazione inserendo la password del Mac.
- Autorizzare l’operazione inserendo la password del Mac.
- Lanciare l’applicazione **Mail**. Recarsi in *Preferenze > Generali* *> Gestisci plugin…*
- Abilitare il Plugin *AltPlugin.mailbundle* e cliccare **Applica e riavvia e-mail**.

![img](https://telegra.ph/file/f53f15173f6d643636daa.png)

- **Lasciare aperta l’app Mail** per tutte le operazioni successive. 
- Collegare il dispositivo sbloccato al computer e Autorizzare il dispositivo. 
- A questo punto decidere se procedere con l'installare [AltStore](#altstore) oppure eseguire il [Sideload](#sideload-applicazioni-da-altserver) diretto di una app.

### AltServer Windows

- Scaricato il file altinstaller.zip, unzipparlo ed estrarre il suo contenuto in una cartella. 
- Lanciare il setup.exe per dar via all’installazione.   
- Avviare AltServer, apparirà come un’icona nell’area di notifica della barra delle applicazioni di Windows, in basso a destra.

![img](https://telegra.ph/file/af7fac6f98369ff95becf.png)

- Collegare il dispositivo sbloccato al computer e Autorizzare il dispositivo. 
- A questo punto decidere se procedere con l'installare [AltStore](#altstore) oppure eseguire il [Sideload](#sideload-applicazioni-da-altserver) diretto di una app.

### AltStore

- Dal Menu di AltServer cliccare su **Install AltStore...** e selezionare il dispositivo.
- Inserire l’e-mail e la password del proprio ID Apple.
- Attendere qualche secondo, **AltStore** verrà installato nel dispositivo.
- Controllare nel primo posto disponibile della Home Screen vi sia installata l'applicazione di AltStore.
- In base alla tua versione segui i seguenti passaggi:
- **iOS 14** o **inferiori**

1. Accedere in *Impostazioni* → *Generali* → *Preferenze* → *Gestisci dispositivo* → *APP SVILUPPATORE* e cliccare sulla propria e-mail. Cliccare su **Verifica**.

- **iOS 15**

1. Accedere in *Impostazioni* → *Generali* → *VPN, DNS e gestione dispositivi* → *APP SVILUPPATORE* e cliccare sulla propria e-mail. Cliccare su **Verifica**.

- **iOS 16** o **superiori**

1. Accedere in *Impostazioni* → *Generali* → *VPN, DNS e gestione dispositivi* → *APP SVILUPPATORE* e cliccare sulla propria e-mail. Cliccare su **Verifica**.
2. Abilitare, solo la prima volta, la seguente opzione in *Impostazioni* → *Privacy e sicurezza* → *Modalità sviluppatore*, successivamente confermare l'avviso di riavvio del dispositivo.
3. Sbloccato il dispositivo confermare l'avviso di *Attivare la modalità sviluppatore?* premendo **Attiva**. Inserire il codice di blocco del dispositivo.

- Aprire l'applicazione di AltStore. Alla domanda *"AltStore" vorrebbe inviarti delle notifiche* si consiglia di consentire le notifiche, in modo da avvisarci in caso di scadenza dei certificati.
- Accedere alla sezione *Settings* → *ACCOUNT* e cliccare sul tasto *Sing in with Apple ID*. 
- Inserire l’e-mail e la password del proprio ID Apple.
- Accedere alla sezione **My Apps**.
- Premere il tasto **+** per poter importare il file .ipa della applicazione da installare.

### Sideload Applicazioni da AltServer

- Premere il tasto **Alt** (**Option**) **⌥** (macOS) o **Shift** **⇧** (Windows).
- Aprire il menu di AltServer.
- Al posto della scritta Install AltStore... si visualizzerà l'opzione **Sideload .ipa…** e selezionare il dispositivo.

[Video](https://telegra.ph/file/e449bcd97dbbc2e0a4081.mp4)

Visualizzazione da macOS

![img](https://telegra.ph/file/d31bbfcc2188408d55146.png)

Visualizzazione da Windows

- Si aprirà il menu del File Manager, cercare e selezionare l'applicazione con estensione .ipa desiderata. Cliccare su **Open**.
- Inserire l’e-mail e la password del proprio ID Apple.
- Attendere qualche secondo, la vostra applicazione verrà installata nel dispositivo. 
- Controllare nel primo posto disponibile della Home Screen vi sia installata l'applicazione.
- In base alla tua versione segui i seguenti passaggi:
- **iOS 14** o **inferiori**

1. Accedere in *Impostazioni* → *Generali* → *Preferenze* → *Gestisci dispositivo* → *APP SVILUPPATORE* e cliccare sulla propria e-mail. Cliccare su **Verifica**.

- **iOS 15**

1. Accedere in *Impostazioni* → *Generali* → *VPN, DNS e gestione dispositivi* → *APP SVILUPPATORE* e cliccare sulla propria e-mail. Cliccare su **Verifica**.

- **iOS 16** o **superiori**

1. Accedere in *Impostazioni* → *Generali* → *VPN, DNS e gestione dispositivi* → *APP SVILUPPATORE* e cliccare sulla propria e-mail. Cliccare su **Verifica**.
2. Abilitare, solo la prima volta, la seguente opzione in *Impostazioni* → *Privacy e sicurezza* → *Modalità sviluppatore*, successivamente confermare l'avviso di riavvio del dispositivo.
3. Sbloccato il dispositivo confermare l'avviso di *Attivare la modalità sviluppatore?* premendo **Attiva**. Inserire il codice di blocco del dispositivo.

- Ora siete in grado di poter utilizzare la vostra applicazione.

#### Guida realizzata da [Jailbreak Italia](https://t.me/JailbreakItalia)©️