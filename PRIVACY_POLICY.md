# Privacy Policy

**Effective date:** 3 October 2026  
**Last updated:** 3 October 2026

> **Draft for a personal, self-hosted tool.** Before publishing, replace every bracketed operator/contact field, confirm the software behavior, and obtain jurisdiction-specific advice if you distribute or operate it for others. This document is informational and is not legal advice.

This Privacy Policy explains how **[operator's legal name or chosen public name]** (“Operator,” “I,” or “me”) handles information in **Discord Custom RPC** (the “Software”). Contact: **[public privacy contact email or contact page]**.

## At a glance

- The Software runs on your device and has no Operator-operated account system, cloud service, analytics, advertising, or telemetry.
- Configuration is stored locally in a `config.json` file. The Software does not send that file to the Operator.
- When you start or update a Rich Presence, the activity you configured is sent from the Software to the Discord desktop client over the local Discord IPC interface. Discord may then process or display it under Discord's own policies and your settings.
- This policy describes the Software's behavior, not Discord's or any external website's data practices.

## 1. Information handled by the Software

### Configuration you enter

The Software handles the Discord Application ID, preview name, activity text, activity type, timestamps, asset keys and descriptions, party information, button labels and URLs, and other Rich Presence fields you choose to enter. It saves the validated configuration locally in `data/config.json` by default, or in the directory selected through `RPC_DATA_DIR`. The app attempts to create the directory with owner-only permissions on systems that support those permissions and writes the file with restrictive permissions; actual protection depends on the operating system, filesystem, and your device settings.

### Discord connection status

While running, the Software keeps transient connection and status information in process memory, including whether Discord is connected, the last successful update time, errors, and the Discord username/display name returned during the local RPC handshake. This status is shown by the local interface. The Software does not write this status history to a log or transmit it to the Operator.

### Web requests to the local interface

The interface communicates with the local Node.js server on loopback (by default `127.0.0.1:3210`). The server accepts local state and configuration requests and does not intentionally collect browser identifiers, cookies, IP addresses, or request logs. Standard operating-system, browser, or hosting logs outside the Software may differ; the Operator does not receive them through the Software.

## 2. Information sent to Discord or other parties

When you choose **Start** or **Apply**, the Software sends your configured Rich Presence activity to the Discord desktop client through Discord's local IPC interface. The status response may also include the Discord username/display name exposed by that local handshake. The Software does not use a Discord OAuth flow, collect your password or token, or contact an Operator-operated backend.

Discord determines what information it processes, retains, and displays after receiving the activity. Other Discord users may see presence information depending on Discord's settings and product behavior. Review [Discord's Privacy Policy](https://discord.com/privacy), [Terms of Service](https://discord.com/terms), and applicable [Developer Terms and Policies](https://support-dev.discord.com/hc/en-us/categories/360000656491-Developer-Policies-Terms).

You may place URLs in activity fields, buttons, or asset fields. The Software passes supported activity values to Discord; it does not fetch those URLs itself as part of normal operation. Discord, a viewer's client, or an external host may make network requests when displaying or opening the content. Those parties' privacy terms apply.

## 3. Purposes and legal basis

The Software uses configuration and transient connection status only to provide the local interface, persist your settings, connect to Discord, and show whether an activity was applied. There is no Operator-side processing or monetization of this data through the Software. If the Operator later adds any hosted feature, account, analytics, diagnostics upload, or other data collection, this policy must be updated before that feature is enabled.

Where privacy law requires a legal basis for processing, the Operator relies on the local operation you request and your choice to configure and apply an activity. Discord separately determines its own legal bases and purposes.

## 4. Retention and deletion

Configuration remains in the local data directory until you change or delete it. To remove it, stop the Software and delete `config.json` from the configured data directory. If you uninstall the Software, check and remove that data directory separately if you no longer need it. The Operator has no copy to delete. Temporary data in memory is ordinarily cleared when the process exits; operating systems may handle memory, backups, or storage differently.

You can stop sharing a presence by selecting **Stop** in the interface or closing the Software. The Software asks Discord to clear the current activity when stopping cleanly. Discord's handling of previously received activity is governed by Discord's policies and retention practices.

## 5. Security

The server binds to loopback and applies host and cross-origin checks. Local storage permissions are requested where supported. These measures reduce exposure but cannot guarantee security of a device, operating system, Discord client, browser, or local environment. Keep your device and configuration directory protected, and avoid putting secrets or sensitive personal information in activity fields.

## 6. Children

The Software is not designed specifically for children. You are responsible for meeting the age requirements that apply to your use of Discord and this Software. Discord's own age requirements and policies apply to your Discord account.

## 7. Your privacy rights

Because the Software stores configuration locally and does not send it to the Operator, access, correction, export, or deletion is generally performed directly by you on your device. You may contact the Operator at **[public privacy contact email or contact page]** with a privacy question. If you believe the Operator has information about you outside the Software, identify the relevant interaction so it can be investigated.

Privacy rights vary by location. This policy does not waive rights that cannot be waived. **[Before publishing, identify the Operator/controller, applicable jurisdiction-specific rights, and any required representative or regulator contact if relevant.]**

## 8. International transfers and third-party services

The Operator does not operate a server that transfers Software data across borders. Discord and any external service you choose may process information in other countries under their own terms and safeguards. Consult their privacy notices for details.

## 9. Changes and contact

The Operator may revise this Policy if the Software changes or legal requirements change. A revised version will show a new “Last updated” date. Material changes to data handling should be explained before they take effect.

Privacy contact: **[public privacy contact email or contact page]**.  
Operator: **[operator's legal name or chosen public name]**.

---

## Implementation review checklist

Before release, confirm all of the following against the version you publish:

- No analytics, crash reporter, remote API, or automatic update service has been added.
- The default and configured data directories match the instructions you give users.
- No server access/error logs or support uploads contain user configuration or identifiers.
- Contact and controller details, applicable rights, and any required jurisdictional disclosures are complete.
