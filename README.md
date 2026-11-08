# Cloud Based Web Server: What It Is, When a VPS Isn't Enough, and What You'll Pay (SpinServers Plans Compared)

A cloud based web server is a virtual machine that serves your site from a provider's pooled hardware. The practical test for whether you're getting cloud rather than a rented slice of one physical box comes down to two questions: if the host machine dies, does another take over automatically, and can you add RAM without a migration? Plenty of cheap plans labelled "cloud" answer no to both.

This guide covers what the four hosting environments actually mean, the three shapes cloud hosting ships in, the market price range you should have in your head before you shop, and where SpinServers' lineup sits inside that picture. SpinServers sells KVM virtual servers from $12.00/month and pre-built dedicated servers from $79.00/month, billed monthly, in two US locations.

> **Quick pick:** for a single site or app moving off shared hosting, the KVM 2 vCPU / 2 GB plan with 40 GB SSD at $12.00/month covers it. If a shared slice has stopped keeping up and you want the whole machine, the pre-built Intel Xeon E3-1280 v5 gives you 4 cores, 32 GB RAM, 1 TB NVMe and 30 TB of transfer for $79.00/month in Dallas or San Jose.
> 👉 [See SpinServers' current KVM VPS and dedicated server plans](https://bit.ly/Spinservers)

## Every SpinServers plan currently on the price list

Two product lines, both quoted in USD per month. The KVM VPS tiers are virtual servers carved from shared infrastructure; the dedicated tiers are single-tenant bare metal. Every VPS listing includes a 1 Gbps port, one IPv4 and one IPv6 address, and RAID-10 SSD storage below the top tier.

| Plan | vCPU / RAM | Storage | Price (USD/mo) | Best for | Order |
| --- | --- | --- | --- | --- | --- |
| KVM 2 vCPU 2 GB | 2 / 2 GB | 40 GB SSD | $12.00 (listed as "starting from") | First site, dev box, small app | [Check this plan](https://bit.ly/Spinservers) |
| Simple Application Server 6 vCPU | 6 / 8 GB | 120 GB RAID-10 SSD | Shown on the plan card | WordPress, small business sites | [Check this plan](https://bit.ly/Spinservers) |
| Simple Application Server 8 vCPU | 8 / 8 GB | 160 GB RAID-10 SSD | Shown on the plan card | Several sites, growing traffic | [Check this plan](https://bit.ly/Spinservers) |
| Simple Application Server 12 vCPU | 12 / 12 GB | 160 GB RAID-10 SSD | Featured tier, from $62.00 | Busier apps, databases under load | [Check this plan](https://bit.ly/Spinservers) |
| Simple Application Server 16 vCPU (Intel Xeon) | 16 / 16 GB | 320 GB RAID-10 SSD | Shown on the plan card | Heavy apps, multi-site stacks | [Check this plan](https://bit.ly/Spinservers) |
| Advanced Application Server 32 vCPU (Intel Xeon) | 32 / 32 GB | 500 GB SSD | Shown on the plan card | Production workloads, big databases | [Check this plan](https://bit.ly/Spinservers) |
| Intel Xeon E3-1280 v5 (Dallas) | 4 / 32 GB | 1 TB NVMe | $79.00 | Single busy site, CI, game server | [Check this plan](https://bit.ly/Spinservers) |
| Intel Xeon E3-1280 v5 (San Jose) | 4 / 32 GB | 1 TB NVMe | $79.00 | Same, West Coast latency | [Check this plan](https://bit.ly/Spinservers) |
| Dual Intel Xeon Gold 6148 (Dallas) | 40 / 256 GB | 3.8 TB SSD | $235.00 | Virtualization hosts, large databases | [Check this plan](https://bit.ly/Spinservers) |
| Dual Intel Xeon Platinum 8173M (Dallas) | 56 / 512 GB | 7.7 TB SSD | $390.00 | Heavy compute, many VMs | [Check this plan](https://bit.ly/Spinservers) |

Monthly transfer runs from 8 TB on the 6 vCPU tier through 10 TB on the 8 and 12 vCPU tiers, 15 TB on the 16 vCPU and 20 TB on the 32 vCPU plan. The four dedicated servers above are the pre-built configurations that provision instantly; the dedicated server pages also let you configure CPU, RAM, storage and bandwidth beyond these four.

Three things about that table that aren't obvious:

**Only two VPS prices appear in the page's headline blocks.** The $12.00 entry plan and the $62.00 featured tier are the figures SpinServers promotes. The rest are quoted per plan card, so open the card before you budget. None of the four dedicated plans publishes a renewal price, which is unusual enough to be worth asking about in the cart.

**No money-back guarantee is published.** A third-party review of the dedicated line notes that month-to-month services generally carry no refund policy, and SpinServers' own pages don't advertise one. Treat the first month as the trial.

**Port 25 is closed by default on every VPS.** You can request it via ticket with a justification, and SpinServers reserves the right to refuse. If you plan to send mail from the server itself, that changes your architecture or your choice of provider.

## Where "cloud" stops meaning anything

Web hosting comes in four environments: shared, where many domains sit on one server and share its cost and its ceiling; dedicated, where you lease one or more servers nobody else touches; managed, where the provider handles security, software upgrades and backups; and VPS, where a hypervisor carves isolated virtual machines out of a single physical server. The last one is what most "cloud VPS" products actually are.

The technical difference between a VPS and cloud hosting is what happens around the instance. A virtual private server lives on a limited set of machines, so it inherits their limits. Cloud hosting puts your content on virtual servers spread across a network, which produces three properties a single-slice VPS doesn't have: redundancy, where data is replicated across nodes and another node picks up the workload when hardware fails; elasticity, where CPU, RAM and storage get added to the instance without physically migrating it; and geographic distribution, where you deploy instances near your visitors instead of serving everyone from one building.

That gives you a usable filter. Ask whether the provider can move your workload to another node without you filing a ticket, and whether resources can change without a rebuild. If yes to both, you're buying cloud in the sense that matters. If no, you're buying a virtual server with a marketing label, which is fine as long as you're paying VPS money for it.

The terminology is genuinely inconsistent across the industry. AWS describes its Lightsail product as VPS instances while calling the wider EC2 catalogue cloud servers. Some hosts refer to a VPS as a private cloud. The definitions don't reconcile, so judge by the two questions rather than the label on the pricing page.

## Three shapes of cloud hosting, and which one you're shopping for

**A fixed-capacity virtual server.** You pick vCPU, RAM and storage, pay a flat monthly rate, and get a defined amount of each. Billing is predictable, the provider manages the hardware layer, and you manage everything above the operating system. This is the shape nearly every small and mid-sized site actually needs, and it's what SpinServers' KVM line is.

**A network of virtual machines across regions.** You run several instances in different locations behind a load balancer, often with a CDN in front. It costs more and takes more operational work, and it earns that cost when you have users on multiple continents or a compliance rule about where data sits.

**Serverless.** The provider handles the operating system, the runtime and the scaling; you deploy code and get billed when requests arrive. Traffic spikes don't change your service level because scaling is automatic. It suits teams with unpredictable load or no infrastructure experience, at the cost of control and of pricing that's harder to forecast.

Billing follows the shape. Fixed-capacity plans are flat monthly subscriptions, usually rolling. Serverless and hyperscale instances bill per second or per hour. A traditional dedicated server is capital expenditure: hardware, rack space, power, cooling and maintenance contracts paid up front regardless of how hard the machine works. Cloud capacity turns that into operating expenditure that tracks actual use, which is why short projects and spiky workloads land on cloud and long-running, steady, high-utilisation workloads sometimes still land on bare metal.

## What a cloud web server should cost

Market anchors, from Contabo's published comparison (12-month term, VAT included, verified August 2026): shared hosting runs roughly €1–4/month, a Contabo Cloud VPS 4 with 4 vCPU, 8 GB RAM and 100 GB SSD starts at €4.40/month, and an AWS EC2 t3.micro works out to about $8.50/month. Those three numbers are not like-for-like. The Contabo figures assume a year's commitment and include VAT; the AWS figure is on-demand pricing that varies with usage. Use them as a range, not a benchmark.

SpinServers sits above the bargain end at $12.00/month for 2 vCPU and 2 GB. What the difference buys is a 1 Gbps port, RAID-10 SSD and 8–10 TB of monthly transfer on the mid tiers, billed month to month rather than on a 12-month contract. If your priority is the lowest possible number for a hobby site, cheaper VPS plans exist. If you want to avoid a year-long commitment while still getting real bandwidth, the entry price is competitive.

The dedicated side is where the arithmetic gets more interesting. $79.00/month for 32 GB of RAM, 1 TB of NVMe and 30 TB of transfer is a lot of machine for the money, and the 40-core, 256 GB configuration at $235.00 undercuts most cloud instances of comparable memory once you annualise them. The trade is flexibility: you can't scale a dedicated box by dragging a slider.

👉 [Compare the $79 dedicated configuration against the rest of SpinServers' lineup](https://bit.ly/Spinservers)

## Who patches the server, and what downtime costs

Security in cloud hosting is shared. The provider patches its own systems and the hardware layer. On self-managed cloud hosting, you update the operating system, the applications and the libraries yourself. Serverless and managed services shift more of that responsibility to the provider. SpinServers lists its servers as unmanaged with full root access, so the patching is yours, and so is the firewall configuration and whatever hardening your stack needs.

The value of redundancy shows up in the incident numbers. A 2023 Uptime Institute survey, cited in Liquid Web's 2026 write-up of the findings, reported that more than two-thirds of organisational outages cost at least $100,000. A 2023 IBM survey put the average cost of a data breach at $4.45 million. Those are 2023 figures reported second-hand, not current measurements, but the order of magnitude explains why a single-node VPS with no failover is a reasonable bet for a brochure site and a poor one for a checkout flow.

SpinServers lists a 99.99% uptime SLA on its status page and runs a DDoS-protected, multihomed network, with private Layer 2 networking available between your own servers. For a single-tenant box, that's the relevant set of protections: network-level filtering and a monthly-settled service credit rather than automatic failover.

## Who SpinServers fits, and who should keep looking

It fits developers and infrastructure teams who want root on a fixed monthly bill and know what to do with it. The dedicated line supports Linux, Windows and ESXi installs with IPMI or iKVM remote management, cPanel and Plesk are available as control panels, and the 10 Gbps options matter if you're pushing serious traffic between machines. Private Layer 2 networking between your own servers is the sort of feature that costs extra elsewhere.

It doesn't fit four common cases. If you want someone else to manage WordPress, run updates and handle backups, an unmanaged server is the wrong purchase. If your users are mostly in Europe or Asia, Dallas and San Jose will cost you latency, and SpinServers' footprint is US-only. If your traffic is genuinely spiky, a fixed-capacity plan means paying for the peak all month; a platform with automatic scaling handles that better. If you need a written refund window before committing, none is published here.

## Questions people ask before buying

**Can a cloud web server run WordPress?** Yes. The 2 vCPU / 2 GB plan handles a small site with caching in place; step to the 6 vCPU / 8 GB tier once you're running plugins, a page builder and real traffic, because PHP workers and MySQL both want RAM.

**Can I upgrade later?** Ask before you buy. SpinServers doesn't advertise live resizing on the KVM VPS page, and with fixed-capacity virtual servers an upgrade usually means moving to the next plan. If you expect to double in six months, start one tier higher than today's needs.

**Is billing hourly or monthly?** Monthly, in USD, on both product lines. If you want per-second billing where a test server costs cents, that's a hyperscaler feature, not something these plans offer.

**Where does my data sit?** Dallas or San Jose. Both are US locations, which matters if you have data-residency obligations.

**Do I have to patch it myself?** Yes. Root access comes with the responsibility.

## Picking one

Match the shape to the workload and the price follows. A single low-traffic site or a staging environment goes on the $12.00 KVM plan. A production site with steady traffic and a database goes on the 6 or 8 vCPU tier. Several busy sites, or one that needs the whole machine, go on the $79 dedicated server, which is also the cheapest way here to get 32 GB of RAM. Multi-region audiences need instances in more than one location with a CDN in front, and SpinServers' two US datacenters only solve that if your users are in North America.

Before you pay, confirm three things in the cart: the billing term and whether the price recurs at the same rate (no renewal price is published for the dedicated plans), the refund position, and whether you need port 25 opened for mail.

👉 [View SpinServers' current plans and start an order](https://bit.ly/Spinservers)
