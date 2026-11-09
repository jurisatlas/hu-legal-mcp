# Hungary Legal Research MCP Server (`hu-legal-mcp`)

**[Magyar](#lang-hu) | [English Documentation](#english-documentation)**

---

<a id="lang-hu"></a>
## Jogi MCP Szerver (Jogszabályok és Bírósági Határozatok) (`hu-legal-mcp`) — Magyar

### A tárolóról (Repository)

Ez a tároló egy Model Context Protocol (MCP) szervert tartalmaz, amely összeköti az Ön által használt AI alkalmazást (Claude Desktop, Cursor, Windsurf, VS Code / Copilot, Cline vagy Antigravity) a Nemzeti Jogszabálytárral (`njt.hu`) és a Bírósági Határozatok Gyűjteményével (`eakta.birosag.hu` — 113 járásbíróság, 20 törvényszék, 5 ítélőtábla, a Kúria és az Alkotmánybíróság).

### Gyors telepítés (AI alkalmazás kiválasztása)

1. **Letöltés:** Kattintson a jobb felső sarokban a **`<> Code` -> `Download ZIP`** gombra, és csomagolja ki a mappát.
2. **Indítás:** Kattintson duplán a **`Click_Here_To_Install_Windows.bat`** (Windows) vagy **`Click_Here_To_Install_Mac.command`** (macOS) fájlra.
3. **AI kliens kiválasztása:** Jelölje be a használt AI programokat (Claude, Cursor, Windsurf, VS Code, Antigravity), kattintson a telepítésre, majd indítsa újra az AI alkalmazást.

**Biztonsági megjegyzés:** A telepítő kizárólag olvasási (read-only) módban működik, és nem fér hozzá a számítógépén lévő személyes fájlokhoz.

### Bírósági szintek és hivatalos források

| Bírósági szint | Lefedett bíróságok |
|:---|:---|
| **Elsőfok (113 Járásbíróság)** | 113 Járásbíróságok (District Courts across Hungary) |
| **Másodfok (20 Törvényszék és 5 Ítélőtábla)** | 20 Törvényszékek (Regional Courts) & 5 Ítélőtáblák (Regional Courts of Appeal: Budapest, Debrecen, Győr, Pécs, Szeged) |
| **Kúria és Alkotmánybíróság** | Kúria (Supreme Court of Hungary) & Alkotmánybíróság (Constitutional Court) |

- **Nemzeti Jogszabálytár (njt.hu):** [https://njt.hu](https://njt.hu) (`njt.hu`, `net.jogtar.hu`, `magyarkozlony.hu`)
- **Bírósági Határozatok Gyűjteménye BHGY (eakta.birosag.hu — Járásbíróságok, Törvényszékek, Ítélőtáblák & Kúria):** [https://eakta.birosag.hu/anonimizalt-hatarozatok](https://eakta.birosag.hu/anonimizalt-hatarozatok) (`birosag.hu`, `eakta.birosag.hu`, `kuria-birosag.hu`, `alkotmanybirosag.hu`)

---

<a id="english-documentation"></a>
## English Documentation

Model Context Protocol (MCP) server providing live, read-only access to **Hungary (HU)** legislation, official gazettes, multi-tier judicial decisions (First Instance, Regional/Cantonal/Appellate, and Supreme/Constitutional courts, including HTML and PDF full-text extraction), and statutory citation verification across all major AI clients (**ChatGPT Desktop, OpenAI Codex CLI, Claude Desktop, Claude Code CLI, Cursor, Windsurf, VS Code / GitHub Copilot / Cline / Roo Code, Google Antigravity / Gemini CLI, Perplexity, and Continue.dev**).

---

### Interactive Desktop Setup (Select Your AI Assistant)

This package includes a graphical installer for legal practitioners and non-technical users that lets you select which AI application(s) you use:

1. **Download:** Click **`<> Code`** at the top right of this repository, select **`Download ZIP`**, and extract the folder to your computer.
2. **Run the Setup Utility:**
   - **Windows:** Double-click `Click_Here_To_Install_Windows.bat`
   - **macOS:** Double-click `Click_Here_To_Install_Mac.command`
3. **Select Your AI Client(s) & Connect:** Check the box(es) for the AI assistant(s) installed on your computer (**ChatGPT Desktop & OpenAI Codex CLI**, **Claude Desktop & Claude Code CLI**, **Cursor**, **Windsurf**, **VS Code / GitHub Copilot / Cline / Roo Code**, **Google Antigravity / Gemini CLI**, or **Perplexity / Continue.dev**), click **Install to Selected AI Clients**, and restart your selected AI application.

**System Integrity Note:** The setup utility operates strictly in read-only mode with respect to your personal files and documents. It installs an isolated Python runtime inside the extracted folder and registers the server entry only in the AI client configuration files you select.

---

### Multi-Tier Judicial Hierarchy & Live Indexed National Archives

This server performs live queries across the full judicial hierarchy and official legal archives of **Hungary**, extracting full text from both HTML pages and official court/gazette PDF judgments:

| Judicial Tier | Covered Courts & Tribunals |
|:---|:---|
| **Tier 1 — First Instance** | 113 Járásbíróságok (District Courts across Hungary) |
| **Tier 2 — Regional / Cantonal / Appellate** | 20 Törvényszékek (Regional Courts) & 5 Ítélőtáblák (Regional Courts of Appeal: Budapest, Debrecen, Győr, Pécs, Szeged) |
| **Tier 3 — Supreme & Constitutional** | Kúria (Supreme Court of Hungary) & Alkotmánybíróság (Constitutional Court) |

#### Official Portals & Live Indexed Domains

- **National Legislation & Official Gazette:** Nemzeti Jogszabálytár (njt.hu) — [https://njt.hu](https://njt.hu)
  - *Indexed Legislation Domains:* `njt.hu`, `net.jogtar.hu`, `magyarkozlony.hu`
- **Court Decisions & Jurisprudence Archives:** Bírósági Határozatok Gyűjteménye BHGY (eakta.birosag.hu — Járásbíróságok, Törvényszékek, Ítélőtáblák & Kúria) — [https://eakta.birosag.hu/anonimizalt-hatarozatok](https://eakta.birosag.hu/anonimizalt-hatarozatok)
  - *Indexed Judicial & Open Case Law Domains:* `birosag.hu`, `eakta.birosag.hu`, `kuria-birosag.hu`, `alkotmanybirosag.hu`

---

### Available MCP Tools

| Tool | Description |
|:---|:---|
| `search_legislation` | Searches enacted statutes, codes, decrees, and official gazette publications in Hungary. |
| `search_case_law` | Searches national jurisprudence and open judicial archives for Hungary. |
| `search_tiered_court_decisions` | Filters case law specifically by judicial instance (`first_instance`, `appellate_regional`, `supreme_constitutional`) or specific regional/cantonal/district court. |
| `list_court_hierarchy` | Returns the complete 3-tier court structure and supported regional court filters for Hungary. |
| `get_legal_document_markdown` | Retrieves full statutory or judicial texts (both HTML and official `.pdf` court judgments) and converts them into clean Markdown. |
| `verify_citation` | Validates statutory and case law citations against official registries. |

---

<details>
<summary><b>Manual Configuration for Developers (Optional)</b></summary>

```json
{
  "mcpServers": {
    "hu-legal-mcp": {
      "command": "uvx",
      "args": [
        "--from",
        "https://github.com/jurisatlas/hu-legal-mcp/archive/refs/heads/main.zip",
        "hu-legal-mcp"
      ]
    }
  }
}
```
</details>
