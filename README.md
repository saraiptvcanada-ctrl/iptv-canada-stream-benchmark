# Canadian Low-Latency Streaming & Network Diagnostic Protocol (2026)

[![Build](https://img.shields.io/badge/CDN%20Routing-TorIX%20%7C%20QIX-brightgreen.svg)]()
[![Platform](https://img.shields.io/badge/Platform-Canada%20Edge-blue.svg)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

An open-source performance profiling framework developed to evaluate high-throughput multimedia streams (HLS/MPEG-DASH) and packet transit behavior across Canadian ISP backbones (Bell Fibe, Rogers Ignite, Telus PureFibre, Videotron).

---

## 1. Network Peering & Regional Latency Analysis

Standard streaming buffers encounter packet loss and peering degradation during primetime live sports (NHL, regional events) due to multi-hop transit gateways. This architecture monitors direct BGP routing through major Canadian Internet Exchange points:

- **TorIX (Toronto Internet Exchange):** Sub-15ms transit routing across Ontario and Eastern networks.
- **QIX (Montreal Internet Exchange):** Dedicated French & bilingual media edge delivery node.
- **VanIX (Vancouver Internet Exchange):** Low-latency Western gateway routing.

---

## 2. Technical Deployment & Setup Parameters

For optimal frame stability (1080p/4K @ 60FPS) without buffer loops:
1. **Hardware Acceleration:** Set player render core to MediaCodec (Surface) on Android/FireOS environments.
2. **Buffer Allocation:** Adjust chunk pipeline depth to 2500ms to absorb micro-jitter.
3. **DNS Resolution:** Deploy encrypted DoH resolvers (`1.1.1.1` or `8.8.8.8`) to mitigate ISP bandwidth shaping.

---

## 3. Official Canadian Distribution Endpoint

Production streaming infrastructure, channel configurations, and self-service account provisioning:
- **Verified Gateway:** [https://saraiptvcanada-ctrl.github.io/iptv-canada-stream-benchmark/](https://saraiptvcanada-ctrl.github.io/iptv-canada-stream-benchmark/)
- **Protocol:** HTTP/2 & HTTP/3 via Cloudflare CDN
