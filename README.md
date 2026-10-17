# GL.iNet VPN subscription lists

Public domain and IP routing subscriptions for the GL.iNet VPN client Subscription URL feature. The [generator repository](https://github.com/marcomc/glinet-vpn-subscription-generator) contains the source code, configuration, tests, and publication workflow. This repository publishes only the generated files, [coverage report](reports/coverage.json), and usage and licensing metadata.

Other OpenWrt VPN clients can use these lists when their policy importer accepts the same one-rule-per-line domain and CIDR syntax.

## Contents

- [Quick start](#quick-start)
- [Choose a subscription](#choose-a-subscription)
- [Subscription URLs](#subscription-urls)
- [Migration](#migration)
- [Compatibility and limitations](#compatibility-and-limitations)
- [Updates and attribution](#updates-and-attribution)

## Quick start

Copy the Raw link address for the subscription you want and paste it into the GL.iNet VPN client's **Subscription URL** field. These examples are useful starting points:

| Routing selection | Raw subscription | Notes |
| --- | --- | --- |
| Google | [google-all-combined-v4.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-all-combined-v4.txt) | Domains and attributable IPv4 CIDRs |
| Netflix | [netflix-all-combined-v4.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/netflix/netflix-all-combined-v4.txt) | Domains and attributable IPv4 CIDRs |
| OpenAI | [openai-all-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/openai/openai-all-domains.txt) | Domains only; published OpenAI IPs cover ChatGPT Voice servers, not general web/API destinations |

Select **Specified Domain / IP List → Subscription URL**, paste the link, then select **Detect**. Confirm zero failed rules and test traffic through the intended VPN tunnel. If your firmware does not accept mixed domain/CIDR rules, choose a `-domains.txt` or `-ips-v4.txt` file instead. Browse the [complete catalog](#subscription-urls) for other providers and variants.

## Choose a subscription

Choose a file listed under [`output/`](output/), then use its Raw URL. For example, `google/google-all-domains.txt` is a domain-only Google subscription.

| Suffix | Contents | Use |
| --- | --- | --- |
| `-domains.txt` | Domains | Most broadly documented GL.iNet subscription format |
| `-ips-v4.txt` | IPv4 CIDRs | IPv4-only IP routing |
| `-ips-v6.txt` | IPv6 CIDRs | Use only after testing IPv6 import and routing on your firmware |
| `-ips.txt` | IPv4 and IPv6 CIDRs | Use when both address families are supported |
| `-combined-v4.txt` | Domains and IPv4 CIDRs | Use when the importer accepts mixed rules |
| `-combined-v6.txt` | Domains and IPv6 CIDRs | Use after testing mixed rules and IPv6 routing |
| `-combined.txt` | Domains and available CIDRs | Use after testing mixed rules and both address families |

IP variants exist only where an attributable provider-specific source is available. A provider-level IP range may serve several services and does not imply exclusive ownership by one service.

## Subscription URLs

Use the **Raw** URL of the desired file in the GL.iNet VPN client's Subscription URL field. The table is regenerated from the coverage report with each list update.
Use a `-combined-v4.txt` list when the tunnel has no IPv6 route.

<!-- BEGIN GENERATED CATALOG -->

Last successful update: `2026-10-17T07:54:42+00:00`. The table contains all 67 published files.

| Provider / service | Subscription URL | Domains | IPv4 CIDRs | IPv6 CIDRs |
| --- | --- | ---: | ---: | ---: |
| amazon / all | [amazon-all-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/amazon/amazon-all-domains.txt) | 249 | 0 | 0 |
| anthropic / all | [anthropic-all-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/anthropic/anthropic-all-domains.txt) | 9 | 0 | 0 |
| apple / all | [apple-all-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/apple/apple-all-domains.txt) | 1795 | 0 | 0 |
| cloudflare / all | [cloudflare-all-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/cloudflare/cloudflare-all-domains.txt) | 76 | 0 | 0 |
| google / ads | [google-ads-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-ads-domains.txt) | 7 | 0 | 0 |
| google / all | [google-all-combined-v4.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-all-combined-v4.txt) | 1133 | 297 | 0 |
| google / all | [google-all-combined-v6.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-all-combined-v6.txt) | 1133 | 0 | 97 |
| google / all | [google-all-combined.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-all-combined.txt) | 1133 | 297 | 97 |
| google / all | [google-all-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-all-domains.txt) | 1133 | 0 | 0 |
| google / all | [google-all-ips-v4.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-all-ips-v4.txt) | 0 | 297 | 0 |
| google / all | [google-all-ips-v6.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-all-ips-v6.txt) | 0 | 0 | 97 |
| google / all | [google-all-ips.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-all-ips.txt) | 0 | 297 | 97 |
| google / apis | [google-apis-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-apis-domains.txt) | 24 | 0 | 0 |
| google / cloud | [google-cloud-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-cloud-domains.txt) | 4 | 0 | 0 |
| google / core | [google-core-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-core-domains.txt) | 2 | 0 | 0 |
| google / docs | [google-docs-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-docs-domains.txt) | 3 | 0 | 0 |
| google / drive | [google-drive-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-drive-domains.txt) | 5 | 0 | 0 |
| google / gemini | [google-gemini-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-gemini-domains.txt) | 46 | 0 | 0 |
| google / gmail | [google-gmail-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-gmail-domains.txt) | 3 | 0 | 0 |
| google / maps | [google-maps-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-maps-domains.txt) | 2 | 0 | 0 |
| google / meet | [google-meet-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-meet-domains.txt) | 2 | 0 | 0 |
| google / other | [google-other-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-other-domains.txt) | 848 | 0 | 0 |
| google / photos | [google-photos-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-photos-domains.txt) | 2 | 0 | 0 |
| google / play | [google-play-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-play-domains.txt) | 8 | 0 | 0 |
| google / youtube | [google-youtube-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/google/google-youtube-domains.txt) | 178 | 0 | 0 |
| meta / all | [meta-all-combined-v4.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/meta/meta-all-combined-v4.txt) | 560 | 79 | 0 |
| meta / all | [meta-all-combined-v6.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/meta/meta-all-combined-v6.txt) | 560 | 0 | 40 |
| meta / all | [meta-all-combined.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/meta/meta-all-combined.txt) | 560 | 79 | 40 |
| meta / all | [meta-all-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/meta/meta-all-domains.txt) | 560 | 0 | 0 |
| meta / all | [meta-all-ips-v4.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/meta/meta-all-ips-v4.txt) | 0 | 79 | 0 |
| meta / all | [meta-all-ips-v6.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/meta/meta-all-ips-v6.txt) | 0 | 0 | 40 |
| meta / all | [meta-all-ips.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/meta/meta-all-ips.txt) | 0 | 79 | 40 |
| microsoft / all | [microsoft-all-combined-v4.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/microsoft/microsoft-all-combined-v4.txt) | 999 | 31 | 0 |
| microsoft / all | [microsoft-all-combined-v6.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/microsoft/microsoft-all-combined-v6.txt) | 999 | 0 | 51 |
| microsoft / all | [microsoft-all-combined.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/microsoft/microsoft-all-combined.txt) | 999 | 31 | 51 |
| microsoft / all | [microsoft-all-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/microsoft/microsoft-all-domains.txt) | 999 | 0 | 0 |
| microsoft / all | [microsoft-all-ips-v4.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/microsoft/microsoft-all-ips-v4.txt) | 0 | 31 | 0 |
| microsoft / all | [microsoft-all-ips-v6.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/microsoft/microsoft-all-ips-v6.txt) | 0 | 0 | 51 |
| microsoft / all | [microsoft-all-ips.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/microsoft/microsoft-all-ips.txt) | 0 | 31 | 51 |
| netflix / all | [netflix-all-combined-v4.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/netflix/netflix-all-combined-v4.txt) | 32 | 36 | 0 |
| netflix / all | [netflix-all-combined-v6.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/netflix/netflix-all-combined-v6.txt) | 32 | 0 | 86 |
| netflix / all | [netflix-all-combined.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/netflix/netflix-all-combined.txt) | 32 | 36 | 86 |
| netflix / all | [netflix-all-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/netflix/netflix-all-domains.txt) | 32 | 0 | 0 |
| netflix / all | [netflix-all-ips-v4.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/netflix/netflix-all-ips-v4.txt) | 0 | 36 | 0 |
| netflix / all | [netflix-all-ips-v6.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/netflix/netflix-all-ips-v6.txt) | 0 | 0 | 86 |
| netflix / all | [netflix-all-ips.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/netflix/netflix-all-ips.txt) | 0 | 36 | 86 |
| openai / all | [openai-all-combined-v4.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/openai/openai-all-combined-v4.txt) | 63 | 23 | 0 |
| openai / all | [openai-all-combined.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/openai/openai-all-combined.txt) | 63 | 23 | 0 |
| openai / all | [openai-all-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/openai/openai-all-domains.txt) | 63 | 0 | 0 |
| openai / all | [openai-all-ips-v4.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/openai/openai-all-ips-v4.txt) | 0 | 23 | 0 |
| openai / all | [openai-all-ips.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/openai/openai-all-ips.txt) | 0 | 23 | 0 |
| spotify / all | [spotify-all-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/spotify/spotify-all-domains.txt) | 26 | 0 | 0 |
| telegram / all | [telegram-all-combined-v4.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/telegram/telegram-all-combined-v4.txt) | 24 | 7 | 0 |
| telegram / all | [telegram-all-combined-v6.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/telegram/telegram-all-combined-v6.txt) | 24 | 0 | 4 |
| telegram / all | [telegram-all-combined.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/telegram/telegram-all-combined.txt) | 24 | 7 | 4 |
| telegram / all | [telegram-all-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/telegram/telegram-all-domains.txt) | 24 | 0 | 0 |
| telegram / all | [telegram-all-ips-v4.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/telegram/telegram-all-ips-v4.txt) | 0 | 7 | 0 |
| telegram / all | [telegram-all-ips-v6.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/telegram/telegram-all-ips-v6.txt) | 0 | 0 | 4 |
| telegram / all | [telegram-all-ips.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/telegram/telegram-all-ips.txt) | 0 | 7 | 4 |
| tiktok / all | [tiktok-all-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/tiktok/tiktok-all-domains.txt) | 32 | 0 | 0 |
| x / all | [x-all-combined-v4.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/x/x-all-combined-v4.txt) | 26 | 16 | 0 |
| x / all | [x-all-combined-v6.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/x/x-all-combined-v6.txt) | 26 | 0 | 3 |
| x / all | [x-all-combined.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/x/x-all-combined.txt) | 26 | 16 | 3 |
| x / all | [x-all-domains.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/x/x-all-domains.txt) | 26 | 0 | 0 |
| x / all | [x-all-ips-v4.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/x/x-all-ips-v4.txt) | 0 | 16 | 0 |
| x / all | [x-all-ips-v6.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/x/x-all-ips-v6.txt) | 0 | 0 | 3 |
| x / all | [x-all-ips.txt](https://raw.githubusercontent.com/marcomc/glinet-vpn-subscription-lists/main/output/x/x-all-ips.txt) | 0 | 16 | 3 |

<!-- END GENERATED CATALOG -->

Provider directories currently include Amazon, Anthropic, Apple, Cloudflare, Google, Meta, Microsoft, Netflix, OpenAI, Spotify, Telegram, TikTok, and X. Google service labels cover core services and accounts, APIs and Firebase, Gmail, YouTube, Drive, Docs, Maps, Photos, Meet, Cloud, Ads, Play, and Gemini; `other` holds unclassified Google domains, and `all` is their union. Check [coverage](reports/coverage.json) for source attribution and limitations.

## Migration

The former `marcomc/glinet-vpn-rules` repository was renamed to the generator and its generated output was moved here. Existing URLs such as `https://raw.githubusercontent.com/marcomc/glinet-vpn-rules/main/output/google/google-all.txt` return HTTP 404. Replace the repository name in each configured Subscription URL with `glinet-vpn-subscription-lists`, then choose the desired variant above. A GitHub repository redirect does not keep the old Raw URLs working.

Combined lists now use `-combined.txt`, `-combined-v4.txt`, and `-combined-v6.txt` instead of `-all.txt`, `-all-v4.txt`, and `-all-v6.txt`. Plain `<name>.txt` domain aliases are removed; use `<name>-domains.txt`. Update any saved Subscription URLs to the canonical filename.

## Compatibility and limitations

- GL.iNet documents domain and IPv4 CIDR subscriptions. Firmware support for IPv6 CIDRs and mixing domains with CIDRs must be verified on the target router. The [generator's router-format fixtures](https://github.com/marcomc/glinet-vpn-subscription-generator/tree/main/tests/fixtures/router) provide small import tests for IPv4, IPv6, and mixed syntax.
- After import, check the detected rule count and route real IPv4 and IPv6 traffic through the intended VPN tunnel. A successful import alone does not prove routing.
- Encrypted or external DNS, direct IP connections, and IPv6 paths outside the VPN policy can bypass domain-based policies.
- Shared cloud allocations and DNS-derived IP addresses are excluded from provider IP lists. See [source attribution](DATA-LICENSES.md) and the coverage report for provenance and update timestamps.
- OpenAI IP variants include only official ChatGPT Voice server CIDRs for UDP port 3478; they do not cover ChatGPT web or API destinations. GL.iNet's IP subscription rules are address based and can also route other traffic to those servers. OpenAI crawler and integration CIDRs describe OpenAI-originated connections and are excluded. Microsoft's official 365 endpoint feed does not cover every Microsoft product.
- Provider and community feeds can omit changing regional endpoints or third-party dependencies; use the coverage report to inspect each list's source scope.

## Updates and attribution

Only the [generator workflow](https://github.com/marcomc/glinet-vpn-subscription-generator/blob/main/.github/workflows/update-lists.yml) publishes updates here. It runs when the generator's `main` branch changes, daily at 03:17 UTC, or on manual dispatch; new upstream data never changes the generator repository. See [license scope](LICENSE) and [data sources and licenses](DATA-LICENSES.md). The router's own automatic subscription refresh depends on its firmware and has not been verified.

Report missing or incorrect rules and propose new sources in the [generator repository](https://github.com/marcomc/glinet-vpn-subscription-generator/issues/new/choose).
