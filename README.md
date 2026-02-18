# Kelp Spore Dispersal and Connectivity Modeling

Lagrangian particle tracking of kelp spore dispersal in British
Columbia coastal waters using a high-resolution FVCOM hydrodynamic
model coupled with OpenDrift and OceanParcels.

## Hydrodynamic Model

**FVCOM v4.4.10** unstructured mesh:
- **Nodes:** 804,082
- **Elements:** 1,431,768 triangles
- **Coastal resolution:** 0.25 km
- **Offshore resolution:** ~11 km
- **Vertical layers:** 11 sigma levels
- **Domain:** British Columbia coast (47.5°N–56.5°N)

### Forcing
- **Tides:** TPXO10 (13 tidal constituents)
- **Ocean:** CMEMS global ocean currents and temperature
- **Atmosphere:** CMEMS wind stress
- **Rivers:** Fraser River discharge

## Particle Tracking

Kelp spore biology parameters:
- Spore viability: 48 hours
- Settlement depth: 2–30 m
- Sinking velocity: 0.5 mm/s
- Vertical turbulent mixing: enabled

Implemented in both **OpenDrift** and **OceanParcels** for
cross-validation.

## Seeding Locations
16 known kelp forest sites across British Columbia.

## Outputs
- Spore dispersal trajectories
- Settlement probability maps
- Connectivity matrices between kelp beds

## Requirements
```
FVCOM v4.4.10 (Fortran, compiled separately)
python >= 3.10
opendrift, oceanparcels, netCDF4, xarray, numpy,
matplotlib, cartopy
```

## License
MIT
