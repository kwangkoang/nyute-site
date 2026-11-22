---
layout: default
title: Nyute Privacy Policy
---

[Home](./) · [한국어](privacy.html) · [Terms (Korean)](terms.html)

# Nyute Privacy Policy

> **Draft for review:** This document describes the current 0.3.0 candidate. Items marked `[TO CONFIRM]` require verification against actual operations and contracts. Do not publish this draft while those items remain unresolved.

- Data controller: Nyute operator **Gyuri Kim**
- Privacy contact: **Gyuri Kim**
- Email: **rnflrn65@gmail.com**
- Effective date: **[actual effective date — TO CONFIRM]**

Nyute is a Chrome extension for recording and revisiting moments in supported videos, including YouTube and Netflix, using notes, images and subtitles. This policy explains information processed on your device and through sign-in, synchronization, analytics, AI and support features.

## 1. Information and purposes

| Category | Information processed | Purpose |
| --- | --- | --- |
| Notes and attachments | Note text, images, creation and modification times, timestamps and saved subtitles | Create, display, edit, search, revisit, back up and restore records |
| Video and playback information | Supported video identifiers, URLs, titles, channel or series and episode information, thumbnails, avatars and playback positions | Associate records with videos, display lists and return to saved moments |
| Preferences | Theme, language, display size, note visibility, pins, groups, recent records, subtitle preferences and related settings | Preserve your experience and synchronize supported preferences |
| Search and autocomplete | Processing of entered search queries, selected keywords, and selection history or frequencies stored on the device | Local search and improved autocomplete suggestions |
| Account and authentication | Google name, email, profile picture, account identifier, authentication and refresh tokens, and session information | Authenticate your account, maintain sign-in, switch accounts, authorize sync and AI requests, and delete accounts |
| Usage analytics | Browser identifiers and feature events described in Section 3 | Measure feature usage, success, failure and reliability, and improve Nyute |
| AI requests | Video identifier, selected interval, language, request identifier, authentication information, generated results, job status and usage | Provide requested subtitles or translation, save or reuse results, enforce limits and handle duplicate requests |
| Support | Submitted email, message, inquiry type, language and extension version | Respond to inquiries, investigate issues and improve the service |
| Connection and security | Network information such as connection IP, request times and status, and necessary diagnostics | Process requests, prevent abuse and investigate security or reliability issues |

Notes and images are processed when you create, attach or import them. Account information is processed when you authenticate or use account features; AI information when you request an AI feature; and support information when you submit an inquiry. Current analytics collection conditions are described in Section 3.

Nyute does not provide a general browser-history logging feature that records all websites you visit. Information about supported video pages and playback positions is processed for video-note features. Nyute does not ask you to enter your Google password into Nyute and currently has no payment-card entry feature.

**[Before publication: CONFIRM the legal basis for each purpose, required notices and consents, required versus optional processing, and consequences of declining.]**

## 2. Storage, sign-in and synchronization

Notes, images, preferences and some usage state are stored in your browser's extension storage. Authentication credentials are stored separately within the extension's origin, including its private database, to maintain sign-in and refresh tokens.

When you use sign-in and synchronization, the records and preferences covered by those features, including notes, images, subtitles and video information, may be processed on Google/Firebase servers. **Nyute is not a service in which all information stays exclusively on your device.** Review the feature notices for synchronization scope, account changes and handling of local records.

To display video metadata and images, Nyute may request resources from YouTube, Netflix or image servers. Those services may receive the requested resource or video identifier and network information needed for the connection.

## 3. Analytics and collection controls

**In the current 0.3.0 candidate, analytics is on by default, and installation or usage events may be transmitted whether or not you sign in with Google.** The product configuration of November 23, 2026 disables the signup notice popup. You can use notes with analytics turned off. This describes the current implementation.

An explicit opt-out previously saved on this browser is preserved. Default collection and setting changes are not recorded as agreement through a consent popup.

Analytics may include a randomly generated browser-installation identifier; session, attempt, exposure and search identifiers; feature names and entry paths; clicks, saves, failures, durations and counts; platform; UI language; extension version; country code; and administrator classification. A browser identifier can link activity from the same installation and should not be described as fully anonymous.

Events pass through a Cloudflare relay to Google Analytics 4 (GA4) and PostHog. **Note text, attached images, raw search queries, original video IDs, video titles, video URLs, email addresses and authentication tokens are excluded from the analytics event allowlist.** This restriction applies to analytics; account, sync, AI and support features process information necessary for their own functions.

Country codes are derived from country-level connection information provided by Cloudflare. The relay is configured not to forward your original connection IP in GA4 or PostHog events, but Cloudflare and request-processing infrastructure process IP and other network information for connections and abuse prevention.

Use **Settings → Privacy and usage statistics → Share usage statistics** to change collection. Turning it off stops future transmission. **View statistics collection details** opens the information in Settings. Switching collection on or off does not display a popup.

The following developer page also provides connection tests and a local analytics identifier reset:

```text
chrome-extension://lhoadmkanjibideekhlfkcdhidgopoea/analytics-setup.html
```

The page currently uses Korean labels. **저장** means Save, and **연결 해제 · 설정 삭제** disables collection and resets this browser's analytics identifier and settings. Controls apply separately to each browser installation. Resetting local settings does not delete historical events already sent to analytics providers. Contact us under Section 8 to request deletion of historical information.

Settings apply separately to each browser; signing in or syncing does not transfer these settings to another device. Browsers marked as development or test devices suppress regular usage events. Connection tests also require collection to be enabled on this browser.

Nyute uses analytics to maintain and improve its features and measure reliability. Nyute does not sell personal information or use it for behaviorally targeted advertising.

## 4. AI subtitles

When you request AI subtitles, authentication information, video identifier, selected interval, language and request identifier are sent to the subtitle service hosted on Cloudflare. After authentication and limit checks, the server may send a video URL, interval, instructions and other necessary input to the AI provider actually used, such as Google Gemini. The currently inspected subtitle-request path does not submit your entire personal note collection or attached images as input.

Generated subtitles, processing state and usage records are processed to return results, handle cancellations and duplicates, enforce limits and investigate failures. Results for the same public video interval may be reused for another signed-in user's matching request. Personal notes and attached images are excluded from that shared subtitle output.

**Whether an AI provider retains inputs or outputs or uses them to improve its services depends on the actual product, billing and contractual configuration.** We do not make a blanket claim that provider training or human review is excluded. The applicable conditions must be completed below.

**[Before publication: CONFIRM actual AI providers and products, paid or unpaid processing terms, input/output retention, training and human review, reuse and deletion scope, processing countries, and permitted ages and regions.]**

## 5. External providers and international processing

| External service | Information transmitted or processed | Purpose |
| --- | --- | --- |
| Google/Firebase | Account and authentication information; supported synchronized records, images, video information and preferences | Sign-in, account management and synchronization |
| Cloudflare | Analytics, AI and support requests; connection and security information | Relay, server and storage operation, security and usage management |
| Google Analytics 4 | Analytics described in Section 3 | Measure feature usage, performance and reliability |
| PostHog, using a US Cloud endpoint in the current code | Analytics described in Section 3 | Measure feature usage, performance and reliability |
| Actual AI providers, such as Google Gemini | AI inputs and outputs described in Section 4 | Requested subtitle processing |
| Discord | Submitted support email, message, inquiry type, language and extension version | Operator review and response in a private channel |

Provider processing is also governed by applicable contracts and policies. Whether a provider acts as a processor or an independent third-party recipient must be determined from its actual role and the relevant agreement.

For international transfers, we identify recipients and contacts, countries, information transferred, timing and method, purposes, retention, legal basis, and methods and consequences of declining.

**[Before publication: CONFIRM each provider's exact legal entity, contacts, role and international-transfer details. Verify processing locations and global network arrangements against the actual accounts and contracts.]**

## 6. Retention and deletion

Nyute retains information for the period necessary for its purposes and applicable legal obligations, and deletes information that is no longer needed through the relevant storage and provider processes. Specific operational periods must be completed below.

| Information | Retention and deletion |
| --- | --- |
| Device notes, images and settings | May remain until removed from that device. Exported backup files are managed separately by you. |
| Server account and synchronized data | Account-deletion or other applicable requests initiate the deletion process. Server completion and backup deletion periods: **[TO CONFIRM]**. |
| Account-deletion upload-prevention records | The deleted account's identifier and lock status may remain separately. Necessity, retention period and legal basis: **[TO CONFIRM]**. |
| GA4 and PostHog analytics | Actual retention settings and treatment of raw events, aggregates and backups, including deletion methods: **[TO CONFIRM]**. |
| AI requests, usage, generated results and shared caches | Provider-specific periods, expiration and cleanup schedules: **[TO CONFIRM]**. |
| Support and Discord records | Post-resolution retention and deletion process: **[TO CONFIRM]**. |
| Server/security logs and backups | Information recorded, access, retention and deletion schedules: **[TO CONFIRM]**. |

Electronic records are deleted through appropriate storage controls and recovery-prevention measures. Where law requires retention, the relevant information, legal basis and period are identified and separated from other uses. **[Applicable statutory retention items, grounds and periods — TO CONFIRM]**.

## 7. Security measures

The inspected implementation uses HTTPS for external transfers, separates authentication storage within the extension's origin and validates message senders and requests. Analytics events use allowlisted fields and values, and analytics server secrets are not included in extension files.

**[Before publication: CONFIRM actual production access controls, encryption at rest, backup/log protection and other measures in operation.]**

## 8. Your rights and deletion requests

Subject to applicable law, you may request access, correction, deletion, restriction of processing or withdrawal of consent. You or your authorized representative may contact **rnflrn65@gmail.com**. We may verify identity or authority to the extent necessary to protect accounts and other people's information.

You may delete individual records or request account deletion through available features. We explain the scope, applicable legal exceptions and outcome of requests. Stopping future collection and deleting existing information are separate operations.

**Uninstalling Nyute, clearing browser storage or revoking Google account access does not by itself delete all server account data, synchronized records or historical analytics.** Use the account-deletion feature or contact us to request server-side deletion. Conversely, removing local records or uninstalling the extension may remove unsynchronized notes and the local analytics identifier.

Because analytics identifiers are separate from Google accounts, deleting historical analytics may require additional information identifying the relevant browser installation. Account deletion does not automatically delete historical analytics held by providers or backup files you previously exported.

## 9. Children and younger users

**[Before publication: CONFIRM ages permitted for the service and its AI features, whether children under 14 in Korea may use the service, and any required parental consent, verification and rights procedures.]**

Legal representatives may send questions about a child's information to the email above. We do not state that the service is available to every age group or that particular child-protection procedures are already implemented without verifying the service policy and provider requirements.

## 10. Limited use of Google API information

Nyute uses and transfers information received from Google APIs in accordance with the Limited Use requirements of the Google API Services User Data Policy. Account information is used within the disclosed authentication, account-management and feature purposes. It is not sold or provided for personalized advertising.

Google's standard account-consent screen concerns the Google permissions requested. Approval on that screen, or publication of this policy, is not treated as automatically satisfying every required processing or optional analytics consent.

## 11. Policy changes

When this policy changes, we publish the changes and a new effective date. New purposes, recipients or other material changes are disclosed before taking effect, and additional consent is obtained where required by law.

## 12. Contact and complaints

- Data controller: **Gyuri Kim**
- Privacy contact: **Gyuri Kim**
- Email: **rnflrn65@gmail.com**

You may also use applicable supervisory-authority, complaint or dispute-resolution procedures. Information about the relevant procedures in Korea is available through the [Personal Information Protection Portal](https://www.privacy.go.kr/).
