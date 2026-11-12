---
layout: page
title: "Informativa sulla privacy di TapRoutine"
lang: it-IT
permalink: /it/
description: "Informazioni sulla privacy e sull’uso dei dati di TapRoutine per Android."
eyebrow: "Privacy e uso dei dati"
brand_label: "Privacy"
home_label: "Pagina iniziale dell’informativa sulla privacy di TapRoutine"
footer_label: "TapRoutine · Android"
contact_label: "Contatti"
---

<p class="last-updated">Ultimo aggiornamento: 12 novembre 2026</p>
<nav class="language-nav" aria-label="Selezione della lingua">
<a href="{{ '/' | relative_url }}" lang="pt-BR">Português (Brasil)</a>
<a href="{{ '/en/' | relative_url }}" lang="en-US">English</a>
<a href="{{ '/es/' | relative_url }}" lang="es-419">Español</a>
<a href="{{ '/fr/' | relative_url }}" lang="fr-FR">Français</a>
<a href="{{ '/de/' | relative_url }}" lang="de-DE">Deutsch</a>
<span aria-current="page" lang="it-IT">Italiano</span>
<a href="{{ '/ja/' | relative_url }}" lang="ja-JP">日本語</a>
</nav>

## Informazioni su questa versione dell'app

TapRoutine è un'app Android in anteprima che consente di configurare una routine per un'app scelta, programmarla sul dispositivo, eseguire i passaggi definiti dall'utente e controllare punti dello schermo in base al colore. L'APK esaminato ha l'identificativo del pacchetto `io.github.vitoriotaz.taproutine`, `minSdk` 24, `targetSdk` 36 e `android:allowBackup=true`. Le conclusioni di questo testo si riferiscono a questo APK di anteprima e potrebbero non essere applicabili alle versioni future.

## Dati creati o consultati dall'app

- **Routine e impostazioni dell'utente:** possono includere il nome della routine; il nome e l'identificativo del pacchetto dell'app scelta; orari, giorni e fuso orario; passaggi e gesti (come tocchi, scorrimenti, attese, il comando Indietro o la schermata iniziale) e le relative posizioni; colore, punto e tolleranza usati per il controllo; e parametri come la frequenza dei controlli e l'eventuale riapertura dell'app di destinazione. Le impostazioni possono includere anche il Guardiano e una schermata alternativa, con un'altra sequenza preconfigurata.
- **App disponibili per la selezione:** TapRoutine consulta Android per mostrare le app per cui è disponibile un'attività di avvio. L'utente sceglie l'app di destinazione; il nome e l'identificativo del pacchetto scelti vengono conservati nella routine locale.
- **Informazioni temporanee sulla finestra in primo piano:** mentre il servizio di accessibilità di TapRoutine è attivo, riceve gli eventi Android `TYPE_WINDOW_STATE_CHANGED` e mantiene in memoria il nome del pacchetto comunicato dal sistema. Il servizio non legge l'albero dell'interfaccia, i testi, i campi né altri contenuti dello schermo.
- **Dati e registri locali:** le routine e i log possono contenere orari, il pacchetto dell'app di destinazione, l'avanzamento e l'esito dei passaggi e dei tentativi, dettagli tecnici degli errori e valori del colore, punti/posizioni e risoluzione dello schermo. Le `SharedPreferences` memorizzano anche il consenso relativo all'informativa, nonché gli stati e gli orari delle programmazioni e del Guardiano.
- **Acquisizione temporanea per il controllo del colore:** durante un controllo, l'app acquisisce temporaneamente in memoria l'intero schermo attualmente visualizzato per calcolare soltanto il colore medio di un'area di 3×3 pixel nel punto indicato. L'acquisizione può avvenire durante i controlli della routine, nel rilevamento di una schermata alternativa e tramite il Guardiano; non è necessariamente limitata alla finestra o all'app di destinazione. Questa funzione richiede Android 11 o versioni successive. L'app non salva deliberatamente l'acquisizione in un file. È temporanea e, nel normale flusso, le risorse associate vengono rilasciate dopo il calcolo.

## Come vengono utilizzati i dati

I dati vengono utilizzati sul dispositivo per salvare e caricare la routine, programmarne l'esecuzione, eseguire i passaggi definiti dall'utente, confrontare il colore nel punto configurato e registrare i risultati. In base alla configurazione, il colore può selezionare una sequenza alternativa già preconfigurata o attivare l'azione preconfigurata del Guardiano. L'app non inventa azioni né interpreta il testo o il contenuto dello schermo per decidere cosa fare.

## Trattamento, archiviazione e trasmissione

Le routine e i registri sono conservati nell'archiviazione locale privata dell'app. Le `SharedPreferences` mantengono anche i dati descritti sopra, compresi il consenso relativo all'informativa e gli stati e gli orari delle programmazioni e del Guardiano. Il pacchetto della finestra rilevato dal servizio viene mantenuto in memoria. L'acquisizione dello schermo è temporanea; l'app non la salva deliberatamente in un file e, nel normale flusso, rilascia le risorse associate.

Il codice dell'APK esaminato non implementa account, server, sincronizzazione, analytics, annunci, pagamenti né chiamate di rete proprie. Ciò non significa che nessuna copia possa uscire dal dispositivo: il Backup automatico di Android/Google può copiare i dati come descritto nella sezione seguente. Anche l'app scelta come destinazione può avere proprie connessioni e pratiche relative ai dati, che non sono controllate da TapRoutine.

Se scegli di contattare l'assistenza via e-mail, il messaggio e l'indirizzo utilizzati per inviarlo saranno trasmessi dal tuo servizio di posta elettronica affinché possiamo riceverli e rispondere. Si tratta di un'azione esterna avviata da te, non di una chiamata di rete propria di TapRoutine.

## Backup automatico di Android/Google

Nell'APK di anteprima esaminato, `android:allowBackup` è impostato su `true`. Se il Backup automatico di Android è attivo, Android può copiare i file privati dell'app e i dati delle `SharedPreferences` — che possono includere routine, log, consenso e stati/orari delle programmazioni e del Guardiano — nell'account Google/Drive dell'utente, in base al servizio Android. Il comportamento dipende dalle impostazioni di backup, dalla versione di Android e dal dispositivo.

Questo backup è un servizio di Android/Google, non un invio di TapRoutine al server dello sviluppatore. L'app e lo sviluppatore non hanno accesso alla copia di backup. La cancellazione dei dati locali o la disinstallazione dell'app non devono essere intese come garanzia della rimozione di una copia separata che il servizio di backup potrebbe conservare.

## Conservazione e opzioni dell'utente

La routine e i registri rimangono nell'archiviazione dell'app finché non vengono sostituiti o rimossi. Il pulsante **Limpar** (in portoghese, “Cancella”) del prototipo elimina il registro delle esecuzioni. Se il registro diventa molto grande, il prototipo può anche rimuovere le voci più vecchie e conservare quelle più recenti. Il salvataggio di una configurazione modificata sostituisce la routine locale; l'annullamento della programmazione interrompe l'esecuzione programmata, ma di per sé non elimina la configurazione salvata. Per rimuovere i dati locali dell'app, usa i controlli di archiviazione di Android per cancellare i dati dell'app oppure disinstallala; ciò non garantisce la rimozione di una copia di backup separata, se presente. Il sistema operativo potrebbe mostrare nomi diversi per questi controlli.

## Servizi e autorizzazioni Android

- **Servizio di accessibilità di Android:** deve essere attivato dall'utente nelle impostazioni di sistema per eseguire i gesti configurati e svolgere i controlli. Riceve gli eventi `TYPE_WINDOW_STATE_CHANGED` e mantiene in memoria il pacchetto comunicato dal sistema; non legge l'albero, i testi o i campi dell'interfaccia. L'acquisizione temporanea dello schermo viene utilizzata per calcolare il colore medio descritto sopra.
- **`SCHEDULE_EXACT_ALARM`:** è relativa alla programmazione di allarmi esatti. Se Android non consente allarmi esatti, la programmazione può essere meno precisa e subire ritardi.
- **`RECEIVE_BOOT_COMPLETED`:** consente al modulo di ricevere l'evento di riavvio del dispositivo per gestire la riprogrammazione delle routine.
- **`WAKE_LOCK`:** consente di mantenere attivo il dispositivo durante un'esecuzione che deve proseguire in background.
- **`KILL_BACKGROUND_PROCESSES`:** è relativa all'azione preconfigurata di terminare in background il processo dell'app di destinazione quando la routine ne prevede la riapertura.
- **`POST_NOTIFICATIONS`:** è relativa alla visualizzazione di notifiche locali, per esempio quelle che riportano un risultato.

La disponibilità, la concessione e le modalità di autorizzazione di queste autorizzazioni sono controllate da Android e possono variare in base alle impostazioni, alla versione del sistema e al dispositivo; questo testo non presuppone che ciascuna generi una specifica richiesta di autorizzazione durante l'esecuzione. Concedi solo le autorizzazioni che ritieni necessarie per le funzioni desiderate.

## Età prevista

Questa versione beta di TapRoutine è destinata a persone adulte di **18 anni o più**; non è stata progettata per bambini o adolescenti.

## Modifiche future

Le funzioni e le pratiche qui descritte corrispondono all'APK di anteprima esaminato e potrebbero cambiare. Se una versione futura inizierà a raccogliere, trasmettere, condividere o conservare altri dati, oppure aggiungerà servizi, la politica dovrà essere aggiornata per rispecchiare tale versione prima della distribuzione. Consulta la versione della politica associata alla build approvata.

## Contatti

Per domande o richieste relative a questa politica: [vitoriotaz@gmail.com](mailto:vitoriotaz@gmail.com).
