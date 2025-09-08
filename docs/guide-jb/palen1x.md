---
title: palen1x
description: Guida per l'utilizzo di palen1x
---

palen1x è un ambiente Linux avviabile che ti permette di eseguire velocemente palera1n su device compatibili.

:::danger
Non è possibile utilizzare palen1x da macchina virtuale o simili (VirtualBox, VMWare, WSL, ecc).
Questa guida non funzionerà e non riceverete supporto.
:::

:::warning
Se stai usando un computer con CPU AMD Ryzen potresti riscontrare problemi. Se puoi usa un Mac/PC con Intel
:::

Su dispositivi con A11, **devi disattivare il codice di sblocco** e non potrai utilizzare nessuna funzionalità SEP (FaceID/TouchID, codice di sblocco, Apple Pay...) finché non torni nello stato non jailbroken.

Inoltre, se il tuo device A11 è su iOS 16+ e hai impostato un codice di sblocco in passato, dovraii formattarlo prima di procedere.


## Requisiti

1. Una USB Drive da 128MB o più
2. L'ultima versione di [palen1x](https://github.com/palera1n/palen1x/releases) (scegli la versione x86_64)
3. L'ultima versione di [Balena Etcher](https://etcher.balena.io/#download-etcher)

## Rendere la chiavetta avviabile

1. Inserisci la chiavetta nel PC (la USB verrà formattata quindi fai il backup degli eventuali file a te importanti)
1. Installa Balena Etcher e aprilo
2. Clicca su Seleziona Immagine e seleziona il file `palen1x-v-x.x.x-x86_64.iso`
3. Scegli la chiavetta inserita
4. Premi `Flash` e attendi la fine del caricamento

## Avviare palen1x

1. Riavvia il PC ed entra nel BIOS (ogni scheda madre ha un tasto/combinazione di tasti differente per farlo, cerca online)
2. Disattiva il Secure Boot
3. Cerca il menu di boot e seleziona la USB

## Eseguire palera1n

:::warning
Usa un cavo USB-A e **non** un cavo USB-C
:::

1. Da palen1x, seleziona `Shell`
2. Digita `palera1n -l`
3. Segui le info a schermo per entrare in DFU

:::	info
Alcuni device potrebbero bloccarsi in pongoOS.
Per risolvere:
* Premi `ctrl` + `C`
* Riesegui il comando `palera1n -l`
:::

Quando il device si avvia, apri l'app palera1n loader e tocca Sileo. Ti chiederà poi di inserire un passcode e Sileo sarà visibile nella schermata home.

:::info
Per rieseguire il JB, dovrai rifare questi step
:::
