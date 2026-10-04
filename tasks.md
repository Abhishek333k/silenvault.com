# SilenVault Tasks & Architecture Roadmap

---

## 📌 Active & Queued Tasks

### 1. Physical-Digital Twin Business Card (`silenvault.com/vcard`)
- **Status**: 🟢 **Implemented & Refined**
- **Core Concept**: 
  - Rather than using an exaggerated sci-fi or neon tech design, the digital vCard acts as a **1:1 digital twin of the real physical SilenVault business card template**.
  - Provides instant brand recognition and executive credibility across all SilenVault business verticals (digital platforms, e-commerce, tools, games, enterprise, physical goods).
- **Architecture Highlights**:
  - **Front Face**: Realistic 3.5" x 2" physical card aspect ratio with satin matte carbon paper finish, subtle foil border highlights, metallic SilenVault Crest (`assets/img/SILENVAULT_CREST.webp`), and executive typography (Abhishek Ramesh, Founder & Core Architect).
  - **Back Face (3D Flip)**: Interactive tactile flip revealing the high-contrast physical card reverse side with the live QR code.
    - **Native Mobile Contact Form Auto-Fill**: The QR code dynamically encodes the full RFC-compliant `BEGIN:VCARD` data payload directly via client-side `qrcode.min.js`. When scanned with any native smartphone camera (iOS or Android), it does NOT reload the web page—it triggers the OS native prompt to immediately open the device's Contacts app pre-filled with all details (Name, Title, Org, Phones, Email, Web, Address) ready to save with a single tap.
  - **Action Deck**: 
    - Hero CTA: Save Contact to Phone (`abhishek-ramesh-silenvault.vcf`).
    - Quick Action Pills: Direct Call, Email, Website, Flip QR.
    - One-tap Copy Dossier: Quick copy for numbers, email, and address with floating toast feedback.
    - Full JSON-LD schema metadata for search indexing.
- **Roadmap & Future Enhancements**:
  - [x] **Direct vCard Camera Integration**: QR code renders vCard contact payload locally with zero external API/network reliance.
  - [ ] **Print Specification Sync**: Once the physical offset/foil printing vendor finishes the dies (hot-stamping silver/cyan foil, embossed crest), calibrate the web CSS colors and gradients to 100% match the physical batch.
  - [ ] **Physical NFC Card Writing**: Burn `https://silenvault.com/vcard` to physical NFC business cards (NTAG215 / NTAG216 chips) for tap-to-share.
  - [ ] **Offline PWA / Service Worker**: Add lightweight service worker caching so the vCard loads instantly in 0ms even in low-signal conference halls.

---

### 2. Multi-Store Delivery & Checkout Integration
- **Status**: 🟡 **Queued**
- **Context**: SilenVault Store (`store.silenvault.com`), checkout flow, digital asset delivery system, and inventory management.
- **Goals**: Establish custom digital product delivery pipelines for asset packs, wallpapers, and software downloads.

---

### 3. Subdomain Ecosystem Maintenance & SEO
- **Status**: 🟡 **Ongoing**
- **Context**: Ensuring consistent brand identity across `silenvault.com`, `tools.silenvault.com`, `games.silenvault.com`, `store.silenvault.com`.
