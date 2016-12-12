---
layout: standalone
title: Gaia Code
---

[Gaia DR1 Paper](https://arxiv.org/pdf/1609.04172v1.pdf)

    select gaia.source_id, gaia.hip,
    gaia.phot_g_mean_mag+5*log10(gaia.parallax)-10 as g_mag_abs,
    hip.b_v
    from "I/337/tgas" as gaia
    inner join "I/311/hip2" as hip
    on gaia.hip = hip.hip
    where gaia.parallax/gaia.parallax_error >= 5 and
    hip.e_b_v > 0.0 and hip.e_b_v <= 0.05 and
    2.5/log(10)*gaia.phot_g_mean_flux_error/gaia.phot_g_mean_flux <= 0.05
