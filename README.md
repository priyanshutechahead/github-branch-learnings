# Git Branching & Workflow Diagram

[ MAIN LEDGER ] ──(v2.1 Live App)─────────────────────────────────────────────► [ MERGED & LIVE ]
     │                                                                                ▲
     │ 1. BRANCH (Take a Copy)                                                        │ 4. MERGE
     ▼                                                                                │  (Integrate Code)
[ FEATURE BRANCH ] ──► `feature/sec-402_high-value-fraud-alert`                       │
                             │                                                        │
                             │ 2. TASK & COMMITS (Write Code)                         │
                             ▼                                                        │
                      ┌────────────────────────────────────────┐                      │
                      │ TASK: [SEC-402] Implement fraud alert  │                      │
                      │       for transfers > $10,000          │                      │
                      └────────────────────────────────────────┘                      │
                             │                                                        │
                             │ 3. PULL REQUEST (The Audit & Review)                   │
                             ▼                                                        │
                      ┌────────────────────────────────────────┐                      │
                      │ 📝 DESCRIPTION:                        │                      │
                      │    - Context: 2026 AML Regulations     │                      │
                      │    - Changes: Updated TransferService  │                      │
                      │    - Test: Sent $10,500 P2P check      │                      │
                      │                                        │                      │
                      │ ✍️ SIGNATURES:                         │                      │
                      │    - Signed-off-by: Sarah Jenkins      │──────────────────────┘
                      │    - Reviewed-by: Marcus Vance         │
                      └────────────────────────────────────────┘


# Code-to-Vault Hierarchy (Block View)
### Think of it as a shipping container. The Branch is the box, and everything else sits neatly inside it:

📦 BRANCH: feature/sec-402_high-value-fraud-alert
 │
 ├── 🏷️ TASK: [SEC-402] Trigger fraud alert for P2P transfers > $10,000
 │    │
 │    ├── 📝 DESCRIPTION
 │    │    ├── 💡 Context: Meet 2026 AML compliance laws.
 │    │    ├── ⚙️ Changes: Added logic to TransferService.ts + SMS OTP.
 │    │    └── 🧪 Testing: Verified $9,999 passes; $10,501 flags.
 │    │
 │    └── ✍️ SIGNATURES
 │         ├── Signed-off-by: Sarah Jenkins <s.jenkins@securebank.com>
 │         └── Reviewed-by: Marcus Vance <m.vance@securebank.com>
