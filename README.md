# Cheap Ubuntu VPS: What $21.99/Year Buys, Which RackNerd Plan Is Enough, and What Year Two Costs (Full Plan Table)

RackNerd's cheapest KVM plan is **$21.99 a year**: 1 vCore, 1 GB RAM, 20 GB SSD, 3 TB of transfer on a 1 Gbps port, one dedicated IPv4, billed annually. That works out to $1.83 a month for a real Ubuntu box with root access, and it undercuts every mainstream host in the comparison table below by a wide margin.

For most people that 1 GB box is one size too small. If Docker, a database and a web server share the machine, take the 2 GB at $35.99/year. If you're running two or three sites, or a small app with Postgres behind it, the 4 GB at $59.99/year is the one worth buying.

> **Quick pick:** 1 GB at $21.99/year for a single low-traffic site, a WireGuard endpoint or a test box. 2 GB at $35.99/year for Docker plus a database. 4 GB at $59.99/year for multi-site hosting or a small app stack. 👉 [See the current RackNerd VPS specials and prices](https://bit.ly/RacKnerd)

Below: every plan on the specials page, the year-one versus year-two math, where the savings actually come from, and the two things to check before you pay.

## Every RackNerd VPS special, side by side

All of these are KVM, RAID-10 SSD, 1 Gbps port, one dedicated IPv4, full root SSH access, provisioned on order. Prices are USD, billed annually.

| Plan | vCPU / RAM | SSD | Monthly transfer | Price | Order |
| --- | --- | --- | --- | --- | --- |
| 1 GB KVM | 1 vCore / 1 GB | 20 GB | 3,000 GB @1 Gbps | $21.99/yr (~$1.83/mo) | [Order the 1 GB KVM](https://bit.ly/RacKnerd) |
| 2 GB KVM | 2 vCore / 2 GB | 35 GB | 5,000 GB @1 Gbps | $35.99/yr (~$3.00/mo) | [Order the 2 GB KVM](https://bit.ly/RacKnerd) |
| 4 GB KVM | 2 vCore / 4 GB | 60 GB | 7,000 GB @1 Gbps | $59.99/yr (~$5.00/mo) | [Order the 4 GB KVM](https://bit.ly/RacKnerd) |
| 6 GB KVM | 6 vCore / 6 GB | 100 GB | 12,000 GB @1 Gbps | $89.99/yr (~$7.50/mo) | [Order the 6 GB KVM](https://bit.ly/RacKnerd) |
| 8 GB KVM | 7 vCore / 8 GB | 150 GB | 20,000 GB @1 Gbps | $119.99/yr (~$10.00/mo) | [Order the 8 GB KVM](https://bit.ly/RacKnerd) |

The same page also lists three Windows KVM plans, included here so the lineup is complete rather than because they belong in an Ubuntu shortlist:

| Plan | vCPU / RAM | SSD | Monthly transfer | Price |
| --- | --- | --- | --- | --- |
| Windows 2.5 GB | 1 vCore / 2.5 GB | 40 GB | 3,500 GB @1 Gbps | $69.00/yr |
| Windows 4 GB | 3 vCore / 4 GB | 60 GB | 6,000 GB @1 Gbps | $115.00/yr |
| Windows 12 GB | 4 vCore / 12 GB | 160 GB | 12,000 GB @1 Gbps | $289.00/yr |

## Which plan most people don't need

The 6 GB and 8 GB tiers exist for a reason, and it isn't "more WordPress." RackNerd ships a one-click app library inside its ctrl control panel, and the memory floors are steep: OpenClaw wants at least 8 GB, Hermes Agent, AnythingLLM, Ollama and LibreChat want 4 GB or more, while n8n and Coolify are comfortable from 2 GB. That's the real dividing line in this lineup. If you're installing a local model or an agent stack, you need the 4 GB box at minimum and probably the 8 GB one. If you're not, the extra cores on the 6 GB plan (six of them, against two on the 4 GB) sit idle on a single-site workload.

Two cores, 4 GB and 60 GB of SSD covers a LEMP stack, a couple of low-traffic sites and a small Docker compose file. That's most of the people searching for a cheap Ubuntu VPS.

## Year one versus year two: the part the price table hides

RackNerd quotes the amount you actually pay for twelve months. $21.99 is the first year, and it is also the number you'll see on the renewal invoice if the same special is still running when the term ends. These are promotional specials, so confirm the renewal amount with support before you prepay several years; what you don't have to model is a teaser monthly rate that silently triples.

That's not how most of this market prices. Hostinger advertises its KVM 1 at $6.49/mo, but the checkout takes **$155.76 for 24 months upfront** and the plan renews at **$11.99/mo** for the next term. Contabo's €4.40/mo on Cloud VPS 4 is explicitly "for the first 24 months" against a €5.50 list price. Both are legitimate structures; both make the advertised monthly figure a first-term number rather than a run rate.

Put them next to each other on comparable specs and the gap gets uncomfortable. Hostinger's KVM 1 gives you 1 vCPU, 4 GB RAM, 50 GB NVMe and 4 TB of bandwidth: $155.76 for the first two years, then $287.76 for the following two at the renewal rate, or **$443.52 over four years**. RackNerd's 4 GB special gives you 2 vCore, 4 GB RAM, 60 GB SSD and 7 TB of transfer at **$59.99 a year**, or **$239.96 over four years** if the price holds. You pay less per year and get a second core.

Monthly billing is the low-risk entry point. RackNerd's standard KVM line starts at **$2.24/month** on monthly terms, which is $26.88 over a year against $21.99 for the annual special. The annual deal saves you about 18% and fixes the price for twelve months. 👉 [Compare the annual specials against monthly billing](https://bit.ly/RacKnerd)

## Ubuntu 22.04, 24.04 or 26.04?

RackNerd lists Ubuntu among the operating systems you can select at order time, alongside Debian, AlmaLinux, Rocky Linux, CentOS and Fedora, with custom ISO installs available through a support ticket. The plan price is set by cores, RAM and disk, so the Ubuntu release isn't a line item. Choose on support horizon:

- **Ubuntu 22.04 LTS** gets standard security updates until May 2027.
- **Ubuntu 24.04 LTS** until May 2029.
- **Ubuntu 26.04 LTS** until May 2031.

LTS releases carry five years of Canonical support; the interim releases between them get about nine months. That's the whole argument for staying on LTS on a box you're not going to babysit. 24.04 is the sensible default for a new deployment in late 2026: it has three and a half years of updates left and the widest pool of current tutorials and package builds. Pick 26.04 if you want the longest runway and your stack supports it, and 22.04 only if something you depend on hasn't been rebuilt for newer releases.

Changing your mind later is cheap. ctrl can reinstall the OS from the panel, and there's an HTML5 VNC console for recovery and manual installs.

## Where a cheap Ubuntu VPS actually saves money, and where it doesn't

The vCPU count is the least interesting number on any budget host's spec sheet. These are the three that change your bill.

**Transfer metering.** RackNerd publishes a hard number on every plan, from 3,000 GB to 20,000 GB, and doesn't call it unlimited. Compare that with Contabo's "Unlimited Traffic\*" on its Cloud VPS line, where the asterisk's conditions aren't on the plan card, or with providers that count only egress and let inbound traffic run free. A stated 3 TB is easier to plan around than an unlimited claim with a fair-use clause behind it.

**Port speed.** Every RackNerd special runs a 1 Gbps port. Contabo's €5.50 tier gives you 200 Mbit/s, rising to 800 Mbit/s only on the €25 tier. Some competitors advertise far more (Arct Cloud lists up to 25 Gbps across its plans). For a single site or a small API, 1 Gbps is not your bottleneck; for a backup restore at 3 a.m., it matters more than two extra cores.

**Backups.** RackNerd's specials are unmanaged and self-backup. There's no bundled snapshot allowance in the plan table. Elsewhere in this market snapshots are billed separately (Arct Cloud charges $0.04/GB/month, and automatic daily backups cost 20% of the server's monthly price), while Hostinger bundles weekly backups and a real-time snapshot into its plans. Budget a few dollars a month for off-network backup storage and treat it as part of the server's cost, because it is.

One more thing the spec sheet won't tell you: RackNerd doesn't publish a formal uptime SLA for these plans, and LowEndTalk users have reported occasional downtime on heavily loaded budget nodes, usually resolved quickly. That's the trade you're making at this price. Keep your own backups from day one and don't put anything on a $21.99 box that can't survive an hour offline.

## Price check against other cheap Ubuntu VPS

Entry-level plans, verified from each provider's own pages. Currencies and billing periods differ, so read the last column before comparing.

| Provider | Entry plan | Specs | Price | Billing note |
| --- | --- | --- | --- | --- |
| RackNerd | 1 GB KVM | 1 vCore / 1 GB / 20 GB SSD / 3 TB | $21.99/yr (~$1.83/mo) | Annual, USD |
| RackNerd | 4 GB KVM | 2 vCore / 4 GB / 60 GB SSD / 7 TB | $59.99/yr (~$5.00/mo) | Annual, USD |
| Arct Cloud | cvm.pico | 1 vCPU / 1 GB / 15 GB NVMe / 1 TB egress | $3.89/mo | Monthly, USD |
| Hostinger | KVM 1 | 1 vCPU / 4 GB / 50 GB NVMe / 4 TB | $6.49/mo | $155.76 for 24 months upfront, renews $11.99/mo |
| Contabo | Cloud VPS 4 | 4 vCPU / 8 GB / 100 GB SSD / 200 Mbit/s | €5.50/mo list, €4.40/mo first 24 months | EUR, intro pricing |
| ColossusCloud | G5.1 | 2 vCPU / 1 GB / 100 GB / 2 TB | $5.00/mo or $0.007/hr | Monthly or hourly, 14-day refund |
| Liquid Web | General Ubuntu VPS | Managed | $17/mo | Page dated Dec 2024, not a current quote |

Two things worth pulling out of that table. ColossusCloud's $5.00 gets you two cores and 100 GB of disk but only 1 GB of RAM; Contabo's €4.40 gets you 8 GB of RAM but a 200 Mbit/s port and a price that steps up after two years. Liquid Web's $17 figure is from a page last updated in December 2024 and shouldn't be read as today's rate. RackNerd's advantage is that the annual number is small enough that the per-month equivalent lands under everyone else's entry price, including the two-core 4 GB configuration.

## Matching a plan to what you're running

- **One small site, a proxy, a VPN endpoint, a monitoring node.** 1 GB at $21.99/year. Ubuntu 24.04 plus Nginx and a static or lightly cached site fits comfortably.
- **Docker with two or three containers, or a database that isn't tiny.** 2 GB at $35.99/year. MySQL or Postgres alongside an app server will use most of 1 GB once the page cache settles.
- **Two or three sites, a Node or Python app with Postgres, a self-hosted n8n or Coolify instance.** 4 GB at $59.99/year. This is the plan most readers should end up on.
- **A local model, an agent stack, or anything with "Ollama" in the install notes.** 8 GB at $119.99/year. The 4 GB plan is the floor for LibreChat or AnythingLLM and it will feel tight.

## Questions people ask before ordering

**Can I upgrade later without reinstalling?** ctrl includes an upgrade path from the panel. As with any host, take a backup first; resizing usually means a reboot and sometimes a disk migration.

**Can I switch from Ubuntu to Debian or AlmaLinux?** Yes. ctrl reinstalls the OS, which wipes the disk, so back up anything you care about. Custom ISOs go through a support ticket.

**Is there a money-back guarantee?** RackNerd doesn't advertise a 30-day refund window the way Hostinger does. The published policy excludes refunds for terms-of-service violations such as spam, cryptocurrency mining or outbound DDoS, excludes anything held as account credit, and notes that a chargeback on a suspended service can carry a **$125 to $250** administrative fee. Requesting immediate cancellation starts a 24-hour termination countdown without returning what you've paid. If you're unsure whether the box suits your workload, start on the $2.24 monthly plan, run it for a month, then move to the annual special.

**How many IPv4 addresses do I get?** One dedicated IPv4 is included on every special listed above, which is worth checking because it's the first thing budget hosts trim.

**Which datacenter should I pick?** RackNerd runs roughly 20 locations across North America, Europe and Asia, including Los Angeles, Dallas, New York, Chicago, Seattle, San Jose, Atlanta, Ashburn, Tampa, Toronto, Amsterdam, London, Dublin and Strasbourg. Each location publishes speed test files and a looking glass, so you can measure the route from your own connection before you order instead of guessing from a map.

**Is it managed?** No. You get root and a control panel; the OS, the firewall rules and the application stack are yours. Support covers the platform, not your Nginx config.

## Before you check out

Two decisions carry all the risk here. Pick the datacenter nearest the people using the server, not the one nearest you, and test it with the location's speed test file first. Then decide the billing term: monthly at $2.24 if you're trialling, annual at $21.99 if you already know the workload fits.

The rest is arithmetic. A 1 GB box at $21.99 a year, or a 4 GB box with two cores at $59.99, both come with a dedicated IPv4, a 1 Gbps port and a stated bandwidth allowance rather than an asterisk. 👉 [Check current RackNerd VPS pricing and availability](https://bit.ly/RacKnerd)
