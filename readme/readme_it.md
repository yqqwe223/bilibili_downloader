# 🎬 Analizzatore di Video Bilibili

> Uno strumento leggero, veloce e versatile per estrarre contenuti video da Bilibili (Versione educativa e di ricerca)

[🌐 Demo online](https://twittervideodownloaderx.com/bilibili_downloader_it) • [📝 Guida all'uso](#-guida-alluso) • [❓ Domande frequenti](#-domande-frequenti)

---

## 📋 Panoramica del progetto

Questo progetto è uno strumento di analisi video basato sul web, progettato per estrarre in modo sicuro i metadati delle risorse multimediali da video pubblici sulla piattaforma Bilibili (哔哩哔哩), offrendo opzioni di conversione del formato e salvataggio locale. Non richiede installazione di software client né registrazione di account: utilizzalo direttamente dal tuo browser.

> ⚠️ **Avviso importante**: Questo strumento è destinato esclusivamente all'apprendimento personale, alla ricerca tecnica e all'uso entro limiti ragionevoli. Si prega di rispettare le [Linee guida della Community Bilibili](https://www.bilibili.com/blackboard/protocol.html), la 《Legge sul diritto d'autore della Repubblica Popolare Cinese》 e altre normative applicabili. Rispetta il lavoro dei creator; non utilizzare i contenuti scaricati per scopi commerciali o per violare i diritti di terzi.

---

## ✨ Funzionalità principali

- 🔗 **Analisi dei link**: Compatibile con URL standard di video/animazioni Bilibili; rilevamento automatico di episodi e opzioni di risoluzione disponibili
- 📥 **Esportazione multi-formato**:
  - Flusso video originale (supporta risoluzioni pubbliche come 1080P/720P, ecc.)
  - Estrazione audio → Formato MP3 (pratico per ascoltare lezioni/musica offline)
  - Clip video → Conversione in GIF animata (ideale per creare meme/dimostrazioni educative)
- 🌍 **Interfaccia multilingue**: Supporto per italiano, inglese, cinese, giapponese, coreano e altre lingue
- 📱 **Compatibilità multipiattaforma**: Funziona perfettamente su Chrome / Firefox / Safari / Edge; esperienza ottimizzata per dispositivi mobili e tablet
- 🔒 **Privacy prioritaria**: Nessun accesso a account Bilibili richiesto, nessuna raccolta di dati personali; processo di analisi completamente anonimo
- ⚡ **Elaborazione rapida**: Analisi completata in media in 5-10 secondi; supporto per richieste simultanee ed elaborazione in batch

---

## 🚀 Avvio rapido

### Utilizzo online (consigliato)
1. Accedi a [https://twittervideodownloaderx.com/bilibili_downloader_it](https://twittervideodownloaderx.com/bilibili_downloader_it)
2. Copia il link del video di destinazione (esempio: `https://www.bilibili.com/video/BV1xx411c7mD`)
3. Incolla il link nel campo di input → Clicca sul pulsante 「Analizza」
4. Seleziona la risoluzione e il formato desiderati → Salva il file seguendo le indicazioni del browser

### Distribuzione locale (per sviluppatori)
```bash
# Clonare il repository
git clone https://github.com/your-repo/bili-video-parser.git

# Installare le dipendenze
cd bili-video-parser && npm install

# Configurare le variabili d'ambiente (opzionale)
cp .env.example .env

# Avviare il server di sviluppo
npm run dev
```

> 💡 Nota: Questo progetto utilizza un'architettura basata su Node.js + Express. Consulta la documentazione dettagliata di distribuzione in `/docs/DEPLOY.md`

---

## 🛠 Stack tecnologico

| Modulo | Tecnologie utilizzate |
|--------|------------------------|
| Frontend | Vue 3 + TypeScript + Vite |
| Backend | Node.js + Express + Axios |
| Elaborazione video | ffmpeg.wasm (conversione leggera lato client) |
| Proxy di inoltro | Cloudflare Workers / Middleware personalizzato |
| Internazionalizzazione | vue-i18n + Pacchetti lingua JSON |

---

## 📚 Guida all'uso

### Flusso operativo di base
```
1. Ottenere il link del video
   └─ Apri il video di destinazione su Bilibili → Copia l'URL dalla barra degli indirizzi del browser

2. Inviare la richiesta di analisi
   └─ Incolla il link nel campo di input dello strumento → Clicca su 「Avvia analisi」

3. Selezionare la configurazione di output
   ├─ 🎬 Scarica video: Scegli la risoluzione (360P/720P/1080P, ecc. - solo opzioni pubbliche)
   ├─ 🎵 Estrai audio: Genera file MP3 (ideale per ascoltare lezioni/musica offline)
   └─ 🎞 Genera GIF: Crea animazione da intervallo di tempo specificato (consigliato: ≤15 secondi)

4. Salvare il file
   └─ La risorsa si aprirà in una nuova scheda → Clic destro/menu → 「Salva con nome」
```

### Consigli per l'uso su dispositivi mobili
- iOS Safari: Pulsante Condividi → 「Salva in File」
- Android Chrome: Tenere premuta l'anteprima del video → 「Scarica video」
- Se il video si riproduce automaticamente: Clicca su `⋮` nell'angolo in alto a destra del player → Seleziona 「Scarica」

---

## ❓ Domande frequenti

**D: Dove vengono salvati i file scaricati?**  
R: I file vengono salvati nella cartella di download configurata nel tuo browser. Puoi verificare o modificare questo percorso nelle impostazioni del browser.

**D: Posso analizzare contenuti esclusivi per membri o che richiedono l'accesso?**  
R: No. Questo strumento funziona solo con video impostati come pubblici e rispetta le impostazioni di accesso del contenuto originale.

**D: La qualità immagine/audio viene ridotta dopo la conversione?**  
R: I download video mantengono il bitrate originale della risoluzione selezionata. Il formato MP3 utilizza una codifica standard a 128 kbps. Il formato GIF ottimizza il framerate in base alla durata per bilanciare dimensioni del file e fluidità.

**D: La cronologia dei download o la cache vengono memorizzate?**  
R: No. Tutte le risorse vengono trasmesse direttamente al dispositivo dell'utente tramite un proxy temporaneo; il server non conserva alcuna richiesta o file multimediale.

**D: Cosa fare se l'analisi fallisce?**  
R: Si prega di verificare: ① Che il link punti a un video pubblico valido ② Che la connessione internet sia stabile ③ Provare con un altro browser. Se il problema persiste, non esitare a segnalarlo tramite una Issue.

---

## ⚖️ Conformità normativa e Clausola di esonero da responsabilità

- Questo strumento **non elude né viola alcuna misura di protezione tecnica** della piattaforma; si limita a ottenere metadati tramite interfacce pubbliche
- L'utente è responsabile di verificare che il proprio utilizzo sia conforme alla legislazione locale e ai termini di servizio della piattaforma
- Casi d'uso consigliati: Archiviazione personale per l'apprendimento, dimostrazioni educative, materiale di riferimento per la creazione di contenuti... sempre nel quadro dell'uso equo (Fair Use)
- Se si individuano contenuti che potrebbero violare diritti, si prega di contattare il canale ufficiale tramite il [modulo di segnalazione copyright di Bilibili](https://www.bilibili.com/blackboard/help.html#copyright)

---

## 🤝 Guida ai contributi

Accogliamo con piacere le tue Pull Request e segnalazioni di Issue! Prima di contribuire, si prega di consultare:
- [Standard di codice](/CONTRIBUTING.md)
- [Guida alla traduzione multilingue](/locales/README.md)
- [Requisiti di sicurezza e conformità](/SECURITY.md)

---

## 📄 Licenza

Questo progetto è pubblicato sotto la [Licenza MIT](/LICENSE). Può essere utilizzato gratuitamente a fini educativi e di ricerca. Per uso commerciale, si prega di verificare attentamente il rispetto delle normative legali applicabili.

---

> 🌟 Se questo strumento ti è stato utile, non esitare a ✨assegnargli una Stella (Star)! Il tuo supporto è la più grande motivazione per continuare a mantenere e migliorare questo progetto~

*Ultimo aggiornamento: Maggio 2026 | Versione: v1.0.0*