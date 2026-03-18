⚡ NEURO CORE — WHATSAPP ENGINE

<p align="center">
  <img src="https://i.imgur.com/Z6X9X9R.gif" width="300"/>
</p>«“Engineered for control. Built for dominance.”»

---

✦ OVERVIEW

Neuro Core is a refined WhatsApp engine powered by Baileys — optimized for speed, precision, and stability.

Built using direct websocket communication without browser dependency, this system provides full control over automation, messaging flow, and interaction systems.

---

⚙️ CORE FEATURES

- Custom pairing system with improved stability
- Fixed authentication & reconnect issues
- Interactive messages, buttons & native flow support
- Efficient session management system
- Multi-device WhatsApp support
- Lightweight and modular architecture
- Suitable for bots, automation, and advanced communication systems

---

🚀 GETTING STARTED

Begin by installing dependencies and running the engine:

npm install
npm run build
npm start

Minimal setup — maximum control.

---

🧠 CORE FUNCTIONS

Check ID Channel

Get channel ID from URL

await sock.newsletterId(url)

Check Banned Number

Check WhatsApp number status

await sock.checkWhatsApp(target)

---

📡 SEND MESSAGE DOCUMENTATION

Status Group Message V2

await sock.sendMessage(target, {
  groupStatusMessage: {
    text: "Neuro System Active"
  }
});

---

Album Message (Multiple Images)

await sock.sendMessage(target, { 
  albumMessage: [
    { image: img1, caption: "Frame 1" },
    { image: { url: "URL IMAGE" }, caption: "Frame 2" }
  ] 
}, { quoted: m });

---

Event Message

await sock.sendMessage(target, { 
  eventMessage: { 
    isCanceled: false,
    name: "Neuro Event",
    description: "Execution Layer",
    location: {
      degreesLatitude: 0,
      degreesLongitude: 0,
      name: "Neuro Node"
    },
    joinLink: "https://call.whatsapp.com/",
    startTime: "1763019000",
    endTime: "1763026200",
    extraGuestsAllowed: false
  } 
}, { quoted: m });

---

Poll Result Message

await sock.sendMessage(target, { 
  pollResultMessage: { 
    name: "System Vote",
    pollVotes: [
      {
        optionName: "YES",
        optionVoteCount: "999"
      },
      {
        optionName: "NO",
        optionVoteCount: "1"
      }
    ] 
  } 
}, { quoted: m });

---

🧩 INTERACTIVE MESSAGE

Simple Interactive Message

await sock.sendMessage(target, {
  interactiveMessage: {
    header: "Neuro Core",
    title: "System Access",
    footer: "milz666",
    buttons: [
      {
        name: "cta_copy",
        buttonParamsJson: JSON.stringify({
          display_text: "COPY CODE",
          id: "NEURO-001",
          copy_code: "ACTIVE"
        })
      }
    ]
  }
}, { quoted: m });

---

Interactive Message with Native Flow

await sock.sendMessage(target, {    
  interactiveMessage: {      
    header: "Neuro Core",
    title: "Flow Control",
    footer: "milz666",
    image: { url: "https://example.com/image.jpg" },
    nativeFlowMessage: {        
      messageParamsJson: JSON.stringify({
        limited_time_offer: {
          text: "Unlock System",
          url: "https://example.com",
          copy_code: "NEURO",
          expiration_time: Date.now() * 999
        },
        bottom_sheet: {
          in_thread_buttons_limit: 2,
          divider_indices: [1,2,3],
          list_title: "Neuro Menu",
          button_title: "Execute"
        }
      }),
      buttons: [
        {
          name: "cta_copy",
          buttonParamsJson: JSON.stringify({
            display_text: "COPY",
            id: "NEURO",
            copy_code: "ACTIVE"
          })
        }
      ]
    }      
  }  
}, { quoted: m });

---

Interactive Message with Thumbnail

await sock.sendMessage(target, {
  interactiveMessage: {
    header: "Neuro Core",
    title: "System UI",
    footer: "milz666",
    image: { url: "https://example.com/image.jpg" },
    buttons: [
      {
        name: "cta_copy",
        buttonParamsJson: JSON.stringify({
          display_text: "COPY",
          id: "123456",
          copy_code: "ACTIVE"
        })
      }
    ]
  }
}, { quoted: m });

---

🧬 ADVANCED FEATURES

Product Message

await sock.sendMessage(target, {
  productMessage: {
    title: "Neuro Product",
    description: "Advanced System Module",
    thumbnail: { url: "https://example.com/image.jpg" },
    productId: "NEURO001",
    retailerId: "CORE001",
    url: "https://example.com",
    priceAmount1000: 50000,
    currencyCode: "USD"
  }
}, { quoted: m });

---

Request Payment Message

await sock.sendMessage(target, {
  requestPaymentMessage: {
    currency: "USD",
    amount: 10000000,
    from: m.sender
  }
}, { quoted: m });

---

⚠️ WARNING

Use this system responsibly.
Improper usage may result in restrictions from WhatsApp.

---

✦ WHY NEURO CORE

Because this is not just another library.

This is:

- control over system behavior
- precision in message execution
- stability for long-running automation

---

⚡ FINAL

«“Control the flow. Break the limits.”»
