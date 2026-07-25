<div align="right">

🇹🇷 [Türkçe](README.tr.md)

</div>

<div align="center">

# ArgilCAD

**AI-powered parametric CAD**

Generate precise, editable parametric 3D models from natural language. Real CAD, AI speed.

[Website](https://argildesign.com/products/argilcad) · [Pricing](https://argildesign.com/products/argilcad/pricing.html) · [Support](https://argildesign.com/support.html)

![ArgilCAD screenshot](assets/screenshot.png)

</div>

---

## 📥 Download

All official releases are published on the [**Releases**](../../releases) page of this repository. The links below always point to the newest version.

| Platform | File | Download |
|----------|------|----------|
| macOS (Apple Silicon) | `ArgilCAD-macos.dmg` | [Latest](../../releases/latest/download/ArgilCAD-macos.dmg) |
| Windows (64-bit) | `ArgilCAD-windows-setup.exe` | [Latest](../../releases/latest/download/ArgilCAD-windows-setup.exe) |

⭐ Star or 👁 Watch this repository to get notified about new versions.

Always download ArgilCAD from this repository or from [argildesign.com](https://argildesign.com/products/argilcad). Downloads from any other source are not official and may be unsafe.

## 💻 System Requirements

| | macOS | Windows |
|---|-------|---------|
| OS version | macOS 11 Big Sur or later | Windows 10 / 11 (64-bit) |
| Architecture | **Apple Silicon only** (M1, M2, M3, M4 …) | x64 |
| Other | Internet connection required for AI features | Internet connection required for AI features |

> ⚠️ **Intel-based Macs are not supported yet.** ArgilCAD currently ships only
> for Apple Silicon. On an Intel Mac the app will launch but the built-in CAD
> engine cannot start, so model generation will not work. Intel support is
> planned for a future release.
>
> Not sure which Mac you have?  → **Apple menu → About This Mac**. If *Chip*
> says "Apple M1/M2/M3/M4", you're on Apple Silicon. If *Processor* says
> "Intel", please wait for the Intel build.

## 🔧 Installation

### macOS (Apple Silicon)

1. Check that your Mac has an Apple Silicon chip (**Apple menu → About This Mac → Chip**). Intel Macs are not supported yet.
2. Download `ArgilCAD-macos.dmg` from the [Releases](../../releases) page.
3. Open the DMG and drag **ArgilCAD** into your **Applications** folder.
4. Launch ArgilCAD from Applications. The app is signed and notarized by Apple, so it opens without warnings.

### Windows

1. Download `ArgilCAD-windows-setup.exe` from the [Releases](../../releases) page.
2. Verify the download — see [Verifying your download](#-verifying-your-download) below.
3. Run the installer and follow the steps.
4. Launch ArgilCAD from the Start menu.

> ⚠️ **This build is not code-signed yet.** Windows SmartScreen will show
> *"Windows protected your PC"* and list the publisher as **Unknown publisher**.
> That is expected for an unsigned installer — it does not mean the file has been
> tampered with. To continue, click **More info → Run anyway**.
>
> Because Windows cannot show you a publisher name to check, do these two things
> instead: download the installer **only** from this repository or from
> [argildesign.com](https://argildesign.com/products/argilcad), and verify its
> SHA-256 checksum before running it. Code signing is planned for a future release.

## 🔒 Verifying your download

Every asset on the [Releases](../../releases) page shows a `sha256:` digest next to
the file name. Compare it with the checksum of the file you downloaded — the two
must match exactly.

**Windows** (PowerShell, in the folder containing the download):

```powershell
Get-FileHash .\ArgilCAD-windows-setup.exe -Algorithm SHA256
```

**macOS** (Terminal):

```bash
shasum -a 256 ArgilCAD-macos.dmg
```

If the values differ, delete the file and download it again. Never run an
installer whose checksum does not match.

On macOS this is optional: the DMG is signed and notarized by Apple, so macOS
verifies its integrity and origin for you before it opens. On Windows the
checksum is currently your only way to confirm the installer is genuine, since
the build is not yet code-signed.

## 🐛 Feedback & Support

- Found a bug? [Open an issue](../../issues/new/choose)
- Need help? Visit our [Support page](https://argildesign.com/support.html)

## 🔗 Links

- [Product page](https://argildesign.com/products/argilcad)
- [Pricing](https://argildesign.com/products/argilcad/pricing.html)
- [Support](https://argildesign.com/support.html)
- [Privacy Policy](https://argildesign.com/privacy.html)
- [Terms of Service](https://argildesign.com/terms.html)
- [Refund Policy](https://argildesign.com/refund.html)

## 📄 License

ArgilCAD is proprietary software by **Argil Design**. This repository hosts release binaries and documentation only; it does not contain source code. Use of ArgilCAD is subject to the [Terms of Service](https://argildesign.com/terms.html).
