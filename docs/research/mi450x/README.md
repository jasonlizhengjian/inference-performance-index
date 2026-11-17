# AMD MI450X

**IPI: 2.5787545195414094 GB300e (2.579 rounded).**

Calculated with the v1 four-model, log-speed 50–400 tokens/s/request methodology,
including separately provisioned prefill. This is a modeled extension, not a
hardware benchmark or a change to the frozen headline release.

## Specifications used

| Per-GPU input | Value |
| --- | ---: |
| HBM4 capacity | 288 GB |
| HBM bandwidth | 23.3 TB/s |
| Dense BF16 tensor throughput | 5.033 PFLOP/s |
| Dense FP8 tensor throughput | 20.133 PFLOP/s |
| Dense FP4 tensor throughput | 40.265 PFLOP/s |
| Scale-up bandwidth, bidirectional | 3.6 TB/s |
| Modeled scale-up bandwidth, outbound | 1.8 TB/s |
| Helios scale-up domain / chip budget | 72 GPUs |

GB and TB use decimal units. Sources: AMD's [MI450X specifications](https://www.amd.com/en/products/accelerators/instinct/mi400/mi450x.html)
and [MI450X brochure](https://www.amd.com/content/dam/amd/en/documents/products/accelerators/instinct/amd-instinct-mi450x-brochure.pdf).

All other settings retain the published [MI455X profile](../../../reference/2026-10-15/hardware/mi455x_deployment.yaml)
and [deployment policy](../../../reference/2026-10-15/catalog.json), including
FP4 expert modeling, memory guards and zero modeled collective startup latency.
The existing AMD FP4 proxy and collective-efficiency assumptions are not
independently calibrated. Both decode and prefill layouts and batches were
re-searched; the unchanged MI455X control reproduced its frozen score exactly.
