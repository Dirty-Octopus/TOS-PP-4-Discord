# Terms of Service

**Effective date:** 3 October 2026  
**Last updated:** 3 October 2026

> **Draft for a personal, self-hosted tool.** Before publishing, replace every bracketed operator/contact field and confirm that the description still matches the software you distribute. This document is informational and is not legal advice.

These Terms govern your use of **Discord Custom RPC** (the “Software”), a locally run tool that lets you prepare Rich Presence activity details and send them to the Discord desktop client through Discord's local IPC interface. The Software is provided by **[operator's legal name or chosen public name]** (“Operator,” “I,” or “me”). Contact: **[public contact email or contact page]**.

## 1. Acceptance and eligibility

By installing, running, or using the Software, you agree to these Terms. If you do not agree, do not use it. You must be legally able to accept these Terms where you live. If you use the Software for another person or organization, you confirm that you are authorized to accept these Terms for them.

## 2. What the Software does

The Software runs on your device and provides a local interface for creating, saving, starting, updating, and stopping Discord Rich Presence. It is not a hosted Discord service, does not log in to your Discord account, and does not provide a Discord bot. You need a compatible Discord desktop client and any application configuration required by Discord.

The Software currently listens on the loopback interface (`127.0.0.1`). Its configuration is saved as `config.json` in its local data directory (`data` by default, or `RPC_DATA_DIR` if configured). You are responsible for protecting that directory and your device. Anyone with access to your device or that directory may be able to view or change the saved configuration.

## 3. Your use and content

You are responsible for the activity text, links, images, identifiers, and other values you enter or send. You agree not to use the Software to:

- violate applicable law, another person's rights, or Discord's Terms of Service, Developer Terms, Developer Policy, or other applicable rules;
- impersonate another person or mislead people about your identity, activity, or affiliation;
- send unlawful, abusive, threatening, discriminatory, or otherwise harmful content;
- include links or material you do not have the right to use, or use the Software to distribute malware, conduct fraud, or facilitate unauthorized access;
- interfere with Discord or another person's systems, evade technical restrictions, or use the Software in a way that creates unreasonable security or operational risk.

You retain any rights you have in content you enter. You grant the Operator no ownership of that content. You understand that, when you start or update an activity, the Software sends the configured activity to the Discord client, and Discord may process and display it under Discord's own terms and privacy policy. Activity text, links, and presence details may be visible to other Discord users according to your Discord settings and Discord's product behavior. Do not put secrets or sensitive personal information in activity fields.

## 4. Discord and third-party services

Discord is an independent service. The Operator does not control Discord, its availability, features, moderation, data handling, or decisions. Your use of Discord remains subject to Discord's applicable terms and policies. The Software is unofficial and is not sponsored, endorsed, or administered by Discord Inc. Discord's names and marks belong to their respective owners.

If you enter external URLs or configure Discord application assets, those third parties may receive requests or information when Discord or a viewer loads or opens them. Their terms and privacy practices apply separately.

## 5. Changes, availability, and termination

The Software is provided for personal use and may change, become unavailable, or be discontinued at any time. The Operator may update these Terms by publishing a revised version with a new “Last updated” date. Changes apply prospectively from publication. If you continue to use the Software after a change, that indicates acceptance where permitted by law; otherwise stop using it.

You may stop using the Software at any time. The Operator may suspend or end any support or distribution offered by the Operator if you materially breach these Terms or if continued operation is not reasonably possible.

## 6. Warranty disclaimer

To the extent permitted by law, the Software is provided “as is” and “as available,” without promises that it will be error-free, secure, compatible with every Discord release, or continuously available. The Operator disclaims implied warranties only to the extent the law allows. Nothing in these Terms removes a consumer right or other protection that cannot legally be excluded.

## 7. Limitation of liability

To the extent permitted by law, the Operator will not be liable for indirect, incidental, special, consequential, exemplary, or punitive loss arising from use of or inability to use the Software, including loss of data, reputation, or business opportunity. Nothing in these Terms excludes or limits liability that cannot legally be excluded or limited, including liability for fraud, intentional misconduct, or any mandatory consumer remedy.

## 8. Governing law and contact

These Terms are subject to the mandatory laws and consumer protections that apply where you live. **[Before publishing, specify the Operator's jurisdiction and a governing-law/forum clause only after confirming it is appropriate and enforceable.]**

Questions or notices about these Terms: **[public contact email or contact page]**.

---

## Service facts to keep accurate

- This is a locally run, single-user tool; it does not provide a hosted account or cloud sync.
- The app stores its configuration locally. The Operator does not receive it through this Software.
- The app communicates with Discord through a local IPC connection. Discord's own service receives the activity when you apply it.
- Do not describe this as a guarantee of anonymity or privacy on Discord; Discord and user-selected external asset hosts have their own data practices.
