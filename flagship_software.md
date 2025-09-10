# Research Clusters or Focus Areas

- Earth System Modeling
- Environment & Climate
- Geohazards
- Space Geodesy & Mission Support

# Flagship Software

*Objective*: equip widening universities with operational, shared tools and skills 
to produce trusted, high-impact, state-of-the-art space-geodesy products & solutions, 
FAIR-by-design (Findable, Accessible, Interoperable, Reusable), open-source, reproducible, 
and service-ready (*SOPs, SLAs, QA dashboards*). This directly delivers the call’s goals 
on institutional reform, digital capacity, skills, and uptake.

- SOPs: Standard Operating Procedures
- SLAs: Service Level Agreements
- QA dashboards: Quality Assurance dashboards

In a nutshell:

- POD Suite: IGS/ILRS/IDS-compliant precise orbits with QC metrics and DOI’d benchmarks; open APIs, containerised, mission-ready and reference-frame strengthening.
- Coastal Altimetry Processor: Delay-Doppler near-shore & inland-water levels, tide-gauge-validated, cross-mission harmonised; FAIR datasets + dashboards for ports, planners, civil protection.
- Gravity Change Processor: GRACE/GRACE-FO mass-change time series & maps, GIA/leakage-corrected with uncertainties; CF-NetCDF/Zarr + DOIs, ready for drought/ice-loss policy use.
- GNSS Deformation & Early-Warning: cleaned station time series, velocity/strain maps, and simple alerts (API/webhooks); standards-aligned and operations-ready.

**Catchy Phrases**:
Evaluator-friendly signals: FAIR-by-design, standards-compliant, vendor-neutral, containerised & reproducible, micro-credentials/train-the-trainer, CoARA-aligned recognition of software/data, measurable KPIs (uptime, latency, accuracy, adoption), and a sustainability pathway (service catalogue + SLAs).

## Earth System Modeling

**Gravity Change Processor (GRACE/GRACE-FO)** Turn GRACE/GRACE-FO data into 
operational, FAIR mass-change products (basin/ice/hydrology) that universities 
can run, teach, and reuse.

System goals
- Reproducible end-to-end pipeline from L2/L2B inputs → basin/gridded mass anomalies + uncertainties.
- Operable by HEI teams (containers, CI/CD, monitoring, SOPs).
- FAIR products (NetCDF/CF & Zarr with DOIs, APIs, catalogs).
- Scalable to HPC or cloud.

*Applications*: basin-scale water storage (drought/groundwater), cryosphere mass balance, sea-level budget closure, and surface-loading signals.

*Users*: HEI researchers, national geodetic/hydrological agencies, space-agency cal/val teams, civil protection and regional planners.

*Products*: basin time series, gridded mass-change maps, uncertainty/QC layers, all via APIs with DOIs for reproducibility.

*Use cases*: water allocation & drought warning, glacier/ice-sheet monitoring, coastal planning, infrastructure risk from long-term loading.

*Importance*: turns GRACE/GRACE-FO into operable, FAIR capacity at widening HEIs—standardised, teachable, and ready for evidence-based policy.


Technical
* Ingest GRACE/GRACE-FO L2 (spherical harmonics, or mascons), convert to equivalent water height, and apply standard filters/destriping.
* Integrate over areas of interest (basins, ice sheets) to produce mass-change time series and gridded maps, with uncertainty estimates.
* Apply GIA corrections to isolate present-day mass change, and add leakage corrections where needed.
* Outputs come with QC/provenance and can be cross-checked against altimetry, hydrology, or GNSS loading.

## Environment & Climate

**Coastal Altimetry Processor (SAR-mode)** Turn multi-mission SAR altimetry into 
operational, FAIR coastal sea-level and inland-water products that universities 
can run, teach, and reuse.

System goals

- Reproducible end-to-end pipeline from L1b/L2 → shoreline/inland-water levels + uncertainties.
- Operable by HEI teams (containers, CI/CD, monitoring, SOPs).
- FAIR products (NetCDF/CF & Zarr with DOIs, APIs, catalogs).
- Scalable to HPC/cloud; supports NRT/NTC low-latency modes.

*Applications*: coastal sea-level trends/variability, storm-surge readiness, port/harbor operations, flood/drought monitoring for rivers/lakes, model validation/assimilation.

*Users*: HEI researchers, hydrographic/met agencies, port authorities, coastal planners, civil protection & water-resource managers.

*Products*: virtual-station time series (coast, rivers, lakes), high-res coastal sea-level grids, uncertainty/QC layers, mission harmonisation/bias files, all via APIs with DOIs.

*Use cases*: berth downtime planning, storm-surge early actions, regional sea-level planning, hydrological drought tracking, assimilation into coastal models.

*Importance*: closes the near-shore “altimetry gap” for widening HEIs—standardised, teachable indicators ready for operations and policy.

Technical
* Ingest SAR-mode altimetry (e.g., Sentinel-3, CryoSat-2, SARAL) L1b/L2; collocate with coastlines, tide gauges, river/lake polygons.
* Apply coastal waveform retracking & classification; land-contamination screening; stack/along-track averaging.
* Apply geophysical corrections: ocean/solid/pole tides, DAC/inverse barometer, wet/dry tropo, SSB; consistent reference/datum.
* Build virtual stations (coast & inland); compute time series, uncertainties, and QC flags (sea state, rain, ice).
* Cross-calibrate missions, remove offsets/drifts; generate gridded products; publish FAIR artifacts & APIs; cross-check vs tide gauges, GNSS, and models.

## GeoHazards

**GNSS Deformation & Early-Warning Toolkit** Turn continuous GNSS raw data into 
operational, FAIR deformation time series, velocity/strain fields, and alert 
signals—capacity first, validation R&I minimal.

System goals

- Reproducible pipeline from GNSS streams/RINEX → cleaned time series → velocities/strain → alerts.
- Operable by HEIs (containers, CI/CD, monitoring, SOPs) for near-real-time and daily modes.
- FAIR products (NetCDF/CSV/Zarr + DOIs, searchable catalogs, stable APIs).
- Scalable on HPC/cloud; resilient to data gaps/outliers.

*Applications*: earthquake swarm awareness, landslide/slow slip monitoring, volcano unrest tracking, mining/subsidence, infrastructure health (dams, pipelines, rail).

*Users*: HEI researchers, civil-protection & seismic/geodetic agencies, transport/energy utilities, insurers/reinsurers.

*Products*: station ENU time series with QC/uncertainty, velocity fields, strain tensors/maps, transient flags, site-specific thresholds, machine-readable alert feed (API/webhooks).

*Use cases*: evacuation/readiness triggers, targeted inspections, asset risk dashboards, hazard-map updates, post-event deformation assessment.

*Importance*: gives widening HEIs an operational deformation service they can run/teach, aligned with standards and ready for authorities.

Technical

* Ingest GNSS (RINEX/RTCM, NTRIP) + metadata; interface to established solvers (e.g., PPP/PPP-AR or network solutions) with containerised wrappers.
* Build cleaned time series (ENU): cycle-slip repair, step detection (equipment/quakes), seasonal/noise modeling; uncertainty per epoch.
* Estimate velocities/acceleration; derive strain tensors on grids; propagate errors; publish maps and station products.
* Transient detection: CUSUM/Bayesian change-points, sliding-window trend tests; configurable site thresholds and hysteresis.
* Alerting: rule-based severity, latency budgets, audit logs; deliver via API/email/SMS integrations.

## Space Geodesy & Mission Support

**POD Suite (GNSS • DORIS • SLR)** Turn multi-tech tracking (GNSS, DORIS, SLR) into 
operational, FAIR precise orbits and ancillary products for mission cal/val and 
analysis—capacity first, validation R&I minimal.

System goals

- Reproducible pipeline from tracking data → SP3 precise orbits, clocks/EOP, residuals + uncertainties.
- Operable by HEIs (containers, CI/CD, monitoring, SOPs) in NRT and reprocessing modes.
- FAIR products (SP3, SINEX, QC reports with DOIs; searchable catalogs & stable APIs).
- Standards-compliant (ITRF/IERS conventions; IGS/ILRS/IDS formats) and scalable on HPC/cloud.

*Applications*: mission commissioning & cal/val, precise geolocation, reference-frame upkeep, altimetry & gravity processor inputs, cross-tech consistency checks.

*Users*: HEI analysis teams, space-agency cal/val groups, IGS/ILRS/IDS analysis centers, national geodetic agencies, satellite operators.

*Products*: SP3 orbits; clock/EOP series; station solutions (SINEX); QC metrics (SLR/DORIS/GNSS residuals, day-boundary overlaps); quick-look dashboards; DOI’d benchmark runs.

*Use cases*: rapid NRT orbits for operations, reprocessing campaigns, SLR residual quality gates, DORIS Doppler health, altimetry POD improvements, inter-tech validation.

*Importance*: equips widening HEIs with a mission-grade POD capability they can operate and teach—raising participation in global services and mission support.

Technical

* Ingest RINEX 3 GNSS, DORIS tracking, and ILRS CRD SLR normals; manage auxiliary models (gravity/tides, SRP macro-models, atmospheres).
* Estimation via batch LS / square-root Kalman with configurable force models; produce SP3c orbits + clock/EOP; adhere to ITRF.
* Cal/val hooks: SLR residual RMS, DORIS Doppler residuals, GNSS day-overlap errors, orbit comparison vs references; automated acceptance thresholds.
* Predefined mission profiles (e.g., altimetry/EO LEOs); containerised solvers; CI/CD, provenance, signed images.
* R&I limited to WP3.3: validation & inter-comparison against community solutions; uncertainty/error budgets; no new estimation algorithms in the capacity pipeline.

