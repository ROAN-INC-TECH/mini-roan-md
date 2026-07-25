# ⚽ MINI ROAN MD — WhatsApp Bot (Web Pairing Edition)
> Thème : Lionel Messi / GOAT — Dev : **MR ROAN**

Version web de ONYXX MD : le pairing WhatsApp se fait maintenant depuis une page web (plus besoin de Telegram).

## Installation

```bash
npm install
npm start
```

Le serveur démarre sur `http://localhost:3000` (ou le `PORT` défini dans `.env`).

## Utilisation

1. Ouvrez la page web
2. Entrez le numéro WhatsApp (indicatif compris, sans `+`)
3. Cliquez sur **Générer le code**
4. Sur le téléphone : WhatsApp → Appareils connectés → Connecter un appareil → Se connecter avec un numéro
5. Entrez le code affiché sur la page

## Structure

- `server.js` — API web (Express) : génère les codes de pairing, liste/supprime les sessions
- `whatsapp.js` — logique Baileys (sessions, reconnexion, auto-join...)
- `commands.js` — toutes les commandes du bot WhatsApp (`.menu`, `.ai`, etc.)
- `public/index.html` — interface web de pairing
- `index.js` — point d'entrée (démarre `server.js`)

## Déploiement (Render)

- Build command : `npm install`
- Start command : `npm start`
- Variable d'env : `PORT` (fournie automatiquement par Render)
