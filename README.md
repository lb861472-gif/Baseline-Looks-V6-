# Baseline

Baseline is an iOS app built with Capacitor.

The iOS app can be built through Codemagic and distributed as an unsigned IPA for installation through SideStore.

> **Important:** The IPA produced by this project is intentionally unsigned. SideStore is used to sign and install the IPA on your device.

---

## Requirements

- iPhone or iPad running iOS/iPadOS 15.0 or newer
- Apple Account
- Windows, macOS, or Linux computer for the initial SideStore installation
- Wi-Fi connection
- USB cable for the initial setup

SideStore's current installation process uses **iLoader** and **LocalDevVPN**.

Official SideStore documentation:

- https://docs.sidestore.io/
- https://docs.sidestore.io/docs/installation/prerequisites
- https://docs.sidestore.io/docs/installation/install

---

# Installing SideStore

Before installing Baseline, you need SideStore installed on your iPhone.

## 1. Install LocalDevVPN

On your iPhone:

1. Open the App Store.
2. Search for **LocalDevVPN**.
3. Install it.
4. Do not connect it yet unless instructed below.

SideStore requires LocalDevVPN to communicate with the services it needs for installing and refreshing apps.

LocalDevVPN must be connected whenever you install, update, or refresh apps through SideStore.

---

## 2. Install iLoader on your computer

On your computer, follow the official SideStore prerequisites:

https://docs.sidestore.io/docs/installation/prerequisites

Download the version of **iLoader** appropriate for your operating system.

### Windows

Windows 8 or newer is supported.

32-bit Windows and Windows 10 on ARM are not supported.

SideStore recommends installing iTunes as part of the Windows setup. The current SideStore documentation recommends the version of iTunes supplied directly by Apple.

---

## 3. Connect your iPhone

Connect your iPhone to your computer using a USB cable.

Unlock your iPhone.

If your iPhone asks:

> Trust This Computer?

Tap:

**Trust**

and enter your iPhone passcode.

---

## 4. Install SideStore

Open **iLoader** on your computer.

1. Sign in with your Apple Account.
2. Select your iPhone.
3. Choose:

**Install SideStore (Stable)**

Follow the prompts until installation finishes.

Official installation instructions:

https://docs.sidestore.io/docs/installation/install

---

# Trust SideStore on iPhone

After SideStore has been installed, you may need to manually trust it.

On your iPhone:

1. Open **Settings**.
2. Go to:

**General → VPN & Device Management**

3. Under **Developer App**, select the Apple Account associated with SideStore.
4. Tap **Trust [your Apple Account]**.
5. Confirm the trust prompt.

Depending on your iOS version, you may also need to enable **Developer Mode**:

**Settings → Privacy & Security → Developer Mode**

Enable it and allow the device to restart if prompted.

---

# Finish SideStore setup

After SideStore has been trusted:

1. Open **LocalDevVPN**.
2. Tap **Connect**.
3. Open **SideStore**.
4. Sign in using the same Apple Account used during the iLoader installation.
5. Open **My Apps**.
6. Find SideStore.
7. Tap the **7 DAYS** counter next to SideStore to refresh it.

If SideStore asks whether you want to revoke or create a new signing certificate, follow the prompt and allow it to refresh.

At this point SideStore should be ready to install apps.

---

# Installing Baseline

## 1. Download the IPA

Download the latest Baseline IPA from the project's releases/build artifacts.

The file should have an `.ipa` extension, for example:

```text
unsigned.ipa
