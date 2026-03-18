### Milz-Official Whatsapp Baileys

<p align="center">
  <img src="https://g.top4top.io/p_3676rfdq11.jpg" width="300" />
</p>WhatsApp Baileys Enhanced Core is a refined version of the original Baileys library, designed to provide a more stable, flexible, and developer-friendly experience when building WhatsApp automation systems.

Built on websocket technology without requiring a browser, this library allows direct interaction with WhatsApp services while maintaining performance and efficiency. This version focuses on improving pairing reliability, fixing common connection issues, and extending support for advanced interactive messaging.

It is suitable for developers building bots, automation systems, customer service tools, or any real-time communication platform that requires stability and control.

---
```
Main Features

- Improved pairing system with better stability
- Fixes common authentication and reconnect issues
- Supports interactive messages, buttons, and native flow
- Efficient session management for long-running systems
- Compatible with latest WhatsApp multi-device features
- Lightweight and modular structure
- Easy integration into existing Node.js applications
```
---

**Getting Started**

Install dependencies and run the project:
```shell
npm install
npm run build
npm start
```
---

# Basic Functions

**Get Channel ID**
```javascript
await sock.newsletterId(url)
```
---

**Check WhatsApp Number**
```javascript
await sock.checkWhatsApp(target)
```
---

# Send Message Examples

**Status Group Message**
```javascript
await sock.sendMessage(target, {
  groupStatusMessage: {
    text: "Hello World"
  }
});
```
---

**Album Message**
```javascript
await sock.sendMessage(target, {
  albumMessage: [
    { image: image1, caption: "First image" },
    { image: { url: "URL" }, caption: "Second image" }
  ]
}, { quoted: m });
```
---

**Event Message**
```javascript
await sock.sendMessage(target, {
  eventMessage: {
    isCanceled: false,
    name: "Hello World",
    description: "Event description",
    location: {
      degreesLatitude: 0,
      degreesLongitude: 0,
      name: "Location"
    },
    joinLink: "https://call.whatsapp.com/",
    startTime: "1763019000",
    endTime: "1763026200",
    extraGuestsAllowed: false
  }
}, { quoted: m });
```
---

**Poll Result Message**
```javascript
await sock.sendMessage(target, {
  pollResultMessage: {
    name: "Poll Example",
    pollVotes: [
      {
        optionName: "Option 1",
        optionVoteCount: "100"
      },
      {
        optionName: "Option 2",
        optionVoteCount: "50"
      }
    ]
  }
}, { quoted: m });
```
---

Interactive Messages
```javascript
Simple Interactive Message

await sock.sendMessage(target, {
  interactiveMessage: {
    header: "Hello World",
    title: "Hello World",
    footer: "powered by milz666",
    buttons: [
      {
        name: "cta_copy",
        buttonParamsJson: JSON.stringify({
          display_text: "Copy Code",
          id: "123456",
          copy_code: "ABC123XYZ"
        })
      }
    ]
  }
}, { quoted: m });
```
---

**Interactive Message with Native Flow**
```javascript
await sock.sendMessage(target, {
  interactiveMessage: {
    header: "Hello World",
    title: "Hello World",
    footer: "MilzOfficial",
    image: { url: "https://example.com/image.jpg" },
    nativeFlowMessage: {
      messageParamsJson: JSON.stringify({
        limited_time_offer: {
          text: "Example",
          url: "https://example.com",
          copy_code: "CODE",
          expiration_time: Date.now() * 999
        }
      }),
      buttons: [
        {
          name: "cta_copy",
          buttonParamsJson: JSON.stringify({
            display_text: "Copy Code",
            id: "123456",
            copy_code: "ABC123XYZ"
          })
        }
      ]
    }
  }
}, { quoted: m });
```
---

**Interactive Message with Thumbnail**
```javascript
await sock.sendMessage(target, {
  interactiveMessage: {
    header: "Hello World",
    title: "Hello World",
    footer: "milz666",
    image: { url: "https://example.com/image.jpg" },
    buttons: [
      {
        name: "cta_copy",
        buttonParamsJson: JSON.stringify({
          display_text: "Copy Code",
          id: "123456",
          copy_code: "ABC123XYZ"
        })
      }
    ]
  }
}, { quoted: m });
```
---

# Advanced Features

**Product Message**
```javascript
await sock.sendMessage(target, {
  productMessage: {
    title: "Product Example",
    description: "Product description",
    thumbnail: { url: "https://example.com/image.jpg" },
    productId: "PROD001",
    retailerId: "RETAIL001",
    url: "https://example.com",
    priceAmount1000: 50000,
    currencyCode: "USD"
  }
}, { quoted: m });
```
---

**Request Payment Message**
```javascript
await sock.sendMessage(target, {
  requestPaymentMessage: {
    currency: "USD",
    amount: 10000000,
    from: m.sender
  }
}, { quoted: m });
```
---

**Why This Version?**

> This version focuses on stability, cleaner implementation, and better developer experience compared to the default version.

It is designed for real-world usage where reliability and maintainability matter.

---

Notes

- Make sure to handle session storage properly
- Always test features in a controlled environment
- Keep dependencies up to date

---

# License

**MIT License**

---
***Created by [MilzOfficial](https://t.me/milzstore)***
