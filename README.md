# 💡 RepuFi – Rent-a-Reputation

**RepuFi** is a decentralized reputation lending protocol where **trusted users (Backers)** can vouch for **low-rep users (Borrowers)** by staking PAS tokens and issuing on-chain **SoulBound Tokens (SBTs)**. This builds a trust layer for Web3 platforms like DAOs, grant programs, and job portals.

🔗 **Live Demo:** [https://repufi.vercel.app](https://repufi.vercel.app)  

---

## 🧠 Core Philosophy

### 🔍 AI-Powered Reputation

- RepuFi uses an **AI-based reputation scoring engine** that analyzes **11 GitHub profile features**:
  - Followers
  - Following
  - Public repos
  - Stars received
  - Forks
  - Contributions
  - Commit history
  - Gists
  - Activity frequency
  - Account age
  - Recent activity streak

- A **GitHub score (0–10)** is generated:
  - 📉 **< 7** → *Low rep (Borrower)*
  - 📈 **≥ 7** → *High rep (Backer)*

---

## 🧩 How RepuFi Works

### 👥 Two User Roles

| Role       | Description |
|------------|-------------|
| 👨‍🎓 **Borrower** | A new user with low reputation who wants to gain trust in Web3. |
| 👨‍🔬 **Backer**   | A reputed user who vouches by staking tokens and issuing a trust badge (SBT). |

---

## 🔁 Vouch + Challenge Flow

### 1. Backer Vouches for Borrower

- Backer connects wallet
- Chooses a borrower (with GitHub score < 7)
- Stakes PAS tokens as a **trust guarantee**
- RepuFi mints a **VouchNFT (SBT)** to both:
  - Backer and Borrower wallets
  - Metadata includes:
    - 🪪 Backer and Borrower address
    - 📜 Reason for vouching
    - 💰 Staked PAS amount
    - 📊 GitHub score snapshot
    - ⏳ Expiry date (30 days)
    - 🖼️ SVG badge image
    - 🧠 AI-reputation metadata (via Pinata/IPFS)

### 2. Borrower Uses the SBT

- Borrower uses the SBT to:
  - Apply for grants
  - Access exclusive DAOs
  - Get verified badges
  - Request micro-loans
  - Apply for jobs

### 3. Third-Party Challenge (New Feature)

- Any user can **challenge** a Borrower if they suspect fraud
- Admin reviews:
  - ✅ If challenge is **valid**:
    - Backer’s stake is **slashed**
  - ❌ If challenge is **invalid**:
    - Stake remains locked until expiry

---

## 🧠 Smart Contract Logic

| Function           | Description                                                  |
|--------------------|--------------------------------------------------------------|
| `createVouch()`    | Backer stakes PAS and mints the Vouch SBT                    |
| `releaseStake()`   | Backer withdraws stake after expiry if no valid challenges   |
| `slashStake()`     | Admin slashes the stake on confirmed fraud/challenge         |

✅ **Soulbound** — VouchNFTs are **non-transferable**  
📁 **On-chain** — All vouches recorded on PassetHub Testnet  
🌐 **Metadata** — GitHub score snapshot and custom SVG stored on **Pinata/IPFS**

---

## 🌐 Job Portal Integration

- Employers can **verify a developer’s reputation** from the RepuFi protocol
- A Chrome extension fetches GitHub ID + Wallet Address from the site:
  - If a valid SBT exists, it is displayed as proof of verified backing
  - If none exists or the SBT has expired, the candidate appears unvouched

🔗 [Try It Out](https://jobportal-eosin-eta.vercel.app)

---

## 🔮 Future Roadmap

- ✅ Third-party Challenge Feature *(Done)*
- 🔁 Trust Marketplace (Paid Vouching)
- 🏅 Reputation Streaks & Leaderboard
- 🔗 Multi-platform ID Integration (Gitcoin, Lens)
- 🧾 DAO-based reputation voting via SBTs
- 🔓 Unlockable Access via SBTs (e.g., grants, forums)

---

## 📢 Contributor

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/bansal-ishaan">
        <img src="https://avatars.githubusercontent.com/bansal-ishaan" width="80px;" alt=""/>
        <br /><sub><b>Ishaan Bansal</b></sub>
      </a>
    </td>
    <!-- Add more contributors below by duplicating the <td> block -->
  </tr>
</table>

---

## 💬 Have Feedback?

Open an issue or reach out to any of the contributors on GitHub.  
We’d love to hear how RepuFi can support your Web3 journey 🚀
