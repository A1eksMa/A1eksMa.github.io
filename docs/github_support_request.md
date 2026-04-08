**Subject:** GitHub Actions blocked after token compromise — requesting reinstatement

Hello,

My GitHub Actions have been blocked following a security incident on April 6, 2026. I'm writing to request reinstatement after completing full remediation.

**What happened:**
One of my servers was compromised, which led to the leak of a GitHub personal access token. The attacker used it to create 8 repositories (named `g-XXXXXXXXX-XXXX`) and run Monero mining workflows via GitHub Actions.

**Remediation steps I've taken:**
- Immediately revoked the compromised token
- Isolated and decommissioned the compromised server
- Deleted all malicious repositories created by the attacker
- Reviewed and revoked all suspicious OAuth apps, tokens, and SSH keys
- Enabled two-factor authentication on my account
- Issued a new token with minimal required scopes

**Current status:**
All 8 malicious repositories have been removed. GitHub billing shows $0.00 net charges — no financial impact. No further unauthorized activity has been detected.

I understand why Actions was disabled and I take full responsibility for securing my infrastructure. I'm confident the vulnerability has been eliminated.

Could you please reinstate GitHub Actions for my account (`A1eksMa`)?

Thank you.
