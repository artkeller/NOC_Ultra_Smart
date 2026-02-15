# Security Policy & Compliance (CRA Art. 14 Compliant)

## 🛡️ Cyber Resilience Act (CRA) Statement
This project is a **non-commercial open-source project** as defined in the Recitals of the EU Cyber Resilience Act. It is developed and maintained with a focus on maximum transparency and integrity. By providing the `/CRA` documentation suite, this project exceeds the standard requirements for open-source security documentation.

## 🔒 Security Architecture (Security by Design)
Following the **ARTKELLER Purist Standard**, security is integrated into the core architecture:
1. **Zero-Dependency:** No `npm`, `yarn`, or third-party package managers are used. This eliminates 100% of common supply-chain vulnerabilities.
2. **Client-Side Execution:** The application runs entirely within the user's browser environment. 
3. **Data Privacy:** No personal data is transmitted to external servers. All configuration data is stored exclusively in the browser's `localStorage`.
4. **Integrity:** Code integrity is maintained via Git commit hashes and served over TLS-encrypted GitHub Pages.

## 🤝 Coordinated Vulnerability Disclosure (CVD)
Although the attack surface is minimal due to the static architecture, we take security seriously and follow the guidelines of Art. 14 CRA.

### Reporting a Vulnerability
Please report security concerns directly to: **artkeller@gmx.de**

### Handling Process (Art. 14(1) & (2))
1. **Acknowledgement:** Receipt of the report will be confirmed within 48 hours.
2. **Analysis & Fix:** As 100% of the code is internally owned, remediation is performed without reliance on third-party vendors.
3. **Disclosure:** A VEX (Vulnerability Exploitability eXchange) update will be published in the [/CRA](/CRA  "/CRA") directory.

## ⚠️ Responsible Use
- **External Links:** Exercise caution when clicking links within the panel if untrusted URLs have been added for monitoring.
- **Physical Access:** Since data resides in `localStorage`, it is accessible to anyone with physical access to the device's browser.

## 🌐 Infrastructure Note
This project is hosted on GitHub Pages (USA). No personal user data is processed or stored by the maintainer.
