<div align="center">
  <h1>✨ Kriszz Hayanasi.</h1>
  <p><em>Custom WhatsApp library built upon Baileys — enhanced, modernized, and elegant ✨</em></p>

  <img src="https://raw.githubusercontent.com/KriszzTzy/Database/main/uploads/1761960111729.jpeg" width="300" alt="Banner" />


  
---

  <p>
    <a href="https://www.npmjs.com/package/@kriszz-hayanasi/baileys">
      <img src="https://img.shields.io/npm/v/@kriszz-hayanasi/baileys?color=blueviolet&label=version&logo=npm" alt="npm version" />
    </a>
    <a href="https://www.npmjs.com/package/@kriszz-hayanasi/baileys">
      <img src="https://img.shields.io/npm/dt/@kriszz-hayanasi/baileys?color=blueviolet&label=downloads&logo=npm" alt="npm downloads" />
    </a>
    <a href="https://whatsapp.com/channel/0029VapYyKEGufIpsd3Rja2C">
      <img src="https://img.shields.io/badge/Join-WhatsApp%20Channel-25D366?logo=whatsapp&logoColor=white" alt="WhatsApp Channel" />
    </a>
  </p>
</div>
<p align="center">
  <a href="https://elaina-bail.vercel.app">
    <img src="https://img.shields.io/badge/Dokumentasi-Baileys-blue?style=for-the-badge&logo=readthedocs&logoColor=white" alt="Lihat Dokumentasi">
  </a>
</p>

---

## 📌 Overview

> `Kriszz Bails` is a refined version of the Baileys library with cleaner API usage, exclusive features like album messaging, newsletter controls, and full-size profile uploads — tailored for modern WhatsApp automation needs.

> `Update`
+ All update information is now redirected to the WhatsApp channel 
[!]<a href="https://whatsapp.com/channel/0029VapYyKEGufIpsd3Rja2C">
      <img src="https://img.shields.io/badge/Join-WhatsApp%20Channel-25D366?logo=whatsapp&logoColor=white" alt="WhatsApp Channel" />
    </a>

## 📦 Installation

### Via `package.json` Fork Baileys (NPM)
@whiskeysockets/baileys
```json
"dependencies": {
  "@whiskeysockets/baileys": "npm:@kriszz-hayanasi/baileys"
}
```
@adiwajsing/baileys
```json
"dependencies": {
  "@adiwajshing/baileys": "npm:@kriszz-hayanasi/baileys"
}
```
baileys
```json
"dependencies": {
  "baileys": "npm:@kriszz-hayanasi/baileys"
}
```

Or via terminal
```bash
npm install npm:@kriszz-hayanasi/baileys
```

Importing (**for those who don't fork another repository**)

ESM
```bash
import makeWASocket from '@rexxhayanasi/elaina-bail'
```

CJS
```bash
const { default: makeWASocket } = require('@rexxhayanasi/elaina-bail')
```


---

## 🌟 Key Features

| Category         | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| 📢 Channels       | Seamlessly send messages to WhatsApp Channels.                              |
| 🖱️ Buttons         | Create interactive messages with button options and quick replies.          |
| 🖼️ Albums          | Send grouped images or videos as an album (carousel-like format).          |
| 👤 LID Grouping    | Handle group operations using the latest @lid addressing style.             |
| 🤖 AI Message Style | Add a stylized “AI” icon to messages.                                      |
| 📷 HD Profile Pics | Upload full-size profile pictures without cropping.                        |
| 🔐 Pairing Code    | Generate custom alphanumeric pairing codes.                                |
| 🛠️ Dev Experience  | Reduced noise from logs with optimized libsignal printouts.                 |

---

## 💡 Use Case Examples

<details>
<summary><strong>📬 Newsletter Control</strong></summary>

```javascript
// Create a newsletter
await sock.newsletterCreate("Elaina Updates");

// Change description
await sock.newsletterUpdateDescription("elaina@newsletter", "Fresh updates weekly");

// Send a reaction to a channel message
await sock.newsletterReactMessage("elaina@newsletter", "175", "🔥");
```

</details>

<details>
<summary><strong>📌 Interactive Messaging</strong></summary>

```javascript
const buttons = [
  { buttonId: 'btn1', buttonText: { displayText: 'Click Me' }, type: 1 },
  { buttonId: 'btn2', buttonText: { displayText: 'Visit Site' }, type: 1 }
];

const msg = {
  text: "Choose one:",
  footer: "From Elaina with love 💜",
  buttons,
  headerType: 1
};

await sock.sendMessage(id, msg, { quoted: null });
```

</details>

<details>
<summary><strong>🖼️ Send Album</strong></summary>

```javascript
const media = [
  { image: { url: "https://example.com/pic1.jpg" } },
  { video: { url: "https://example.com/clip.mp4" } }
];

await sock.sendMessage(id, { album: media, caption: "Memories 💫" }, { quoted: null });
```

</details>

<details>
<summary><strong>🔐 Pairing with Custom Code</strong></summary>

```javascript
const code = await sock.requestPairingCode("62xxxxxxxxxx", "ELAINA01");
console.log("Your Pairing Code:", code);
```

</details>

<details>
<summary><strong>📊 Poll Creation</strong></summary>

```javascript
const pollMessage = {
  name: "Favorite Color?",
  values: ["Red", "Blue", "Green"],
  selectableCount: 1
};

await sock.sendMessage(id, { poll: pollMessage });
```

</details>

<details>
<summary><strong>📍 Location Sharing</strong></summary>

```javascript
const locationMessage = {
  degreesLatitude: 37.422,
  degreesLongitude: -122.084,
  name: "Googleplex",
  address: "1600 Amphitheatre Pkwy, Mountain View, CA 94043"
};

await sock.sendMessage(id, { location: locationMessage });
```

</details>

<details>
<summary><strong>👥 Group Management</strong></summary>

```javascript
// Create group
const group = await sock.groupCreate("My New Group", [number1, number2]);

// Add participants
await sock.groupAdd(group.id, [number3, number4]);

// Change group description
await sock.groupUpdateDescription(group.id, "This is our awesome group!");
```

</details>

---

**Note:** Replace `id` with the actual recipient ID and `sock` with your WhatsApp socket connection variable.

 ---
 
## 🐞 Found a Bug?

Please open an issue at  [ *UNCOMING WEBSITE* ]
Or contact the maintainer directly via WhatsApp:

<p align="center">
  <a href="https://wa.me/972568184368?text=hai, kay?" target="_blank">
    <img alt="WhatsApp" src="https://img.shields.io/badge/Chat%20on%20WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white">
  </a>
</p>

---

<details>
  <summary>🙏 <strong>TQTO (Thanks To)</strong></summary>

Terima kasih kepada pihak-pihak yang telah memberikan dukungan, inspirasi, dan kontribusi secara langsung maupun tidak langsung dalam pengembangan proyek ini:

- **Allah SWT**  
  For all His grace and ease.

- **Parent**  
  For your continued love, prayers, and support.

- **[Nstar-Y / Nstar-bail](https://github.com/Nstar-Y)**  
  As an initial foundation and reference in the development of this system.

- **[Kriszz Hayanasi](https://github.com/KriszzTzy)** (Me)  
  The main developer of this project.

</details>

> [!CAUTION]
> Built on top of the WhiskeySockets/Baileys project. All original core logic credits go to their team. Kriszz Bails extends it with thoughtful UX and DX improvements.

---

### 🙌 Contributors outside the Baileys code

Thanks to the following awesome contributors who help improve this project 💖

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/KriszzTzy">
        <img src="https://avatars.githubusercontent.com/u/194907727?v=4" width="80px;" style="border-radius:50%;" alt="Matstoree"/>
        <br />
        <sub><b>Kriszz</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/RexxHayanasi">
        <img src="https://avatars.githubusercontent.com/u/150516773?v=4" width="80px;" style="border-radius:50%;" alt="Matstoree"/>
        <br />
        <sub><b>Rexx</b></sub>
      </a>
    </td>
<td align="center">
      <a href="https://github.com/kiuur">
        <img src="https://avatars.githubusercontent.com/u/182334162?v=4" width="80px;" style="border-radius:50%;" alt="Matstoree"/>
        <br />
        <sub><b>Kyuu</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/iconic05">
        <img src="https://avatars.githubusercontent.com/u/197745110?v=4" width="80px;" style="border-radius:50%;" alt="iconic05"/>
        <br />
        <sub><b>iconic05</b></sub>
      </a>
    </td>
  </tr>
</table>
